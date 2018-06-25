---
title: Aplicaciones de EWS y la arquitectura de Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: c10f308a-65bb-4a0b-8fdd-b4a61503f0fd
description: Obtenga información sobre cómo funciona la EWS dentro de la arquitectura de Exchange y averigüe qué protocolos EWS se basa en.
ms.openlocfilehash: 1fbc1e68edbca829555fbbf1b9f0bc4723da9524
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763017"
---
# <a name="ews-applications-and-the-exchange-architecture"></a>Aplicaciones de EWS y la arquitectura de Exchange

Obtenga información sobre cómo funciona la EWS dentro de la arquitectura de Exchange y averigüe qué protocolos EWS se basa en.
  
Servicios Web de Exchange (EWS) es una API de multiplataforma que permite a las aplicaciones tener acceso a los elementos del buzón, como mensajes de correo electrónico, reuniones y contactos desde Exchange Online, Exchange Online como parte de Office 365, o versiones de Exchange a partir de local Exchange Server 2007. [Aplicaciones EWS](ews-application-types.md) puede tener acceso a los elementos del buzón local o remotamente mediante el envío de una solicitud en un mensaje XML basados en SOAP. El mensaje SOAP está incrustado en un mensaje de HTTP cuando se envía entre la aplicación y el servidor, lo que significa que, siempre que la aplicación puede publicar XML a través de HTTP, puede usar EWS para tener acceso a Exchange. 
  
## <a name="exchange-architecture-overview"></a>Introducción a la arquitectura de Exchange
<a name="bk_techarch"> </a>

Los diagramas siguientes muestran los métodos de autenticación y rutas de acceso de comunicación utilizadas por las aplicaciones de EWS al comunicarse con Exchange 2013 y Exchange Online. Desde la perspectiva de aplicación EWS, las rutas de comunicación son idénticas y los métodos de autenticación solo pueden variar ligeramente; la diferencia principal es la visibilidad que tiene en el back-end de Exchange.
  
**En la figura 1. Aplicación de EWS y la arquitectura de Exchange local**

![Ilustración que muestra una aplicación EWS en el contexto de la arquitectura de Exchange local. Para una descripción de los componentes de este diagrama, consulte los elementos 1 a 8 en el texto que sigue a esta y a la siguiente imagen.](media/Ex2013_ArchitecturesOverview.png)
  
La figura 2 muestra las mismas rutas de comunicación que se muestra en la figura 1, como se utiliza por las aplicaciones de EWS al comunicarse con Exchange Online.
  
**La figura 2. Aplicación de EWS y la arquitectura de Exchange Online**

![Ilustración que muestra una aplicación EWS en el contexto de la arquitectura de Exchange Online para una aplicación EWS. Para una descripción de los componentes de este diagrama, consulte los elementos 1, 2, 3, 6 y 9 en el texto que sigue a la imagen.](media/Ex2013_Architectures_Online.png)
  
Los siguientes son los componentes que se muestran en los diagramas:
  
1. Aplicación de EWS: Esto puede ser un [cliente, el portal o la aplicación de servicio](ews-application-types.md) y se puede instalar en un cliente o en un servidor de acceso de cliente de Exchange local. Si usa la API administrada de EWS para desarrollar la aplicación de EWS, los ensamblados de la API administrada de EWS deben instalarse en el cliente y [redistribuye por la aplicación](redistribution-requirements-for-the-ews-managed-api.md).
    
2. El mensaje SOAP XML: mensaje de XML, en una envoltura SOAP, incrustada en un mensaje HTTP/S que se ajusta al archivo Services.wsdl en el servidor de acceso de cliente. HTTPS es recomendable para Exchange local y se requiere para Exchange Online. 
    
3. Métodos de autenticación: básica, los mensajes EWS incluyen información de autenticación NTLM (autenticación integrada de Windows) o OAuth como parte de la carga HTTP. 
    
4. Equilibrador de carga, el equilibrador de carga distribuye el mensaje a un servidor de acceso de cliente en la matriz de servidores de acceso de cliente. Este componente sólo es visible en la arquitectura de Exchange local.
    
5. Matriz de servidores de acceso de cliente, los servidores de acceso de cliente están organizados en un grupo con equilibrio de carga que se llama una matriz de servidores de acceso de cliente. Servidores de acceso de clientes individuales proporcionan los servicios de proxy, redirección limitado y autenticación. Los propios servidores de acceso de cliente no hacen ninguna representación de datos y no hay datos se ponen en cola o almacenados en un servidor de acceso de cliente: fino y sin estado; simplemente se autentica la solicitud, se realiza una búsqueda de detección automática y, a continuación, los servidores proxy la solicitud al servidor de buzones. El servidor de acceso de cliente mantener una relación de 1:1 con el servidor de buzón de correo que hospeda los datos del usuario. Se usa el protocolo HTTP (protegido mediante SSL con un certificado autofirmado) entre el servidor acceso de cliente y el servidor de buzón de correo. Este componente sólo es visible en la arquitectura de Exchange local.
    
6. Servicio de detección automática: servicio de detección automática del realiza una detección de servicios mediante el acceso a servicios de dominio de Active Directory (AD DS) para recuperar la versión de buzón de correo y la ubicación del servidor de buzón de correo que hospeda la copia activa de los datos del usuario.
    
7. Servicio EWS: servicio de la dirección URL de EWS se describe mediante tres archivos: Services.wsdl, Messages.xsd y Types.xsd, así como los ensamblados de la API administrada de EWS. Services.WSDL describe el contrato entre el cliente y el servidor, Messages.xsd define los mensajes de solicitud y respuesta SOAP y Types.xsd define los elementos usados en los mensajes SOAP. Messages.xsd y Types.xsd contienen siempre las versiones más recientes del esquema, aunque existen versiones anteriores del esquema. Tenga en cuenta que Services.wsdl, Messages.xsd y Types.xsd están disponibles en el servidor de acceso de cliente, pero no se utiliza realmente para la validación de esquema, se proporcionan sólo como referencia. Los ensamblados de la API administrada de EWS se proporcionan para las aplicaciones cliente EWS del servidor y se implementan en todos los roles de servidor de Exchange, no sólo los servidores de acceso de cliente. Este componente sólo es visible en la arquitectura de Exchange local.
    
    Disponibilidad de la característica se basa en la versión del esquema EWS que los objetivos de la aplicación. Debido a que los esquemas EWS están y forward-compatible, si se crea una aplicación que se dirige a una versión anterior de esquema, como Exchange 2007 SP1, la aplicación también funcionará con una versión posterior de esquema, como el servicio de Exchange 2010 SP2, así como Exchange Online. Debido a que las características y actualizaciones de característica controladas por el esquema, se recomienda usar el código común más antigua base destinado a las características EWS que se va a implementar en la aplicación cliente. Muchas aplicaciones pueden dirigir la versión Exchange2007_SP1, debido a que el esquema de Exchange 2007 SP1 contiene casi todas la funcionalidad principal de Exchange para trabajar con elementos y carpetas en el almacén de Exchange. Para obtener más información, vea [características de cliente EWS](ews-client-design-overview-for-exchange.md#EWSFeatures).
    
8. Grupo de disponibilidad de base de datos (DAG): Los servidores de buzones están organizados en un DAG altamente disponible, que se puede implementar en uno o varios centros de datos. El servidor de buzones contiene la base de datos de buzones de correo y administra toda la actividad de los buzones de correo activa en ese servidor. Todos los componentes que procesan, representan y almacenarán los datos están en el servidor de buzón de correo. Los clientes no se conectan directamente al servidor de buzón de correo; todas las conexiones se controlan mediante el servidor de acceso de cliente. Este componente sólo es visible en la arquitectura de Exchange local.
    
9. Exchange Online como parte de Office 365 y Exchange Online, la solución de mensajería hospedada que ofrece las características de Exchange como un servicio basado en la nube.
    
Cuando una aplicación EWS solicita información desde el almacén de Exchange, un mensaje de solicitud XML que cumple con el estándar de SOAP es creado y se envía al servidor de Exchange. Cuando el servidor de Exchange recibe la solicitud, comprueba las credenciales que se proporcionan por el cliente y analiza automáticamente el XML para los datos solicitados. El servidor, a continuación, crea una respuesta SOAP que contiene los datos XML que representa los objetos fuertemente tipados solicitados y sus propiedades. Los datos XML se envían a la aplicación en una respuesta HTTP. A continuación, la aplicación deserializa el código XML y usa los datos a la reforma los objetos fuertemente tipados.
  
## <a name="protocols-and-standards-that-ews-applications-must-support"></a>Protocolos y estándares que deben admitir aplicaciones EWS
<a name="bk_standards"> </a>

Para comunicarse con un servidor de Exchange, las aplicaciones de EWS deben admitir los siguientes protocolos y estándares.
  
**La tabla 1. Protocolos**

|**Protocolo**|**¿Cómo se usa**|
|:-----|:-----|
|HTTP/S  <br/> |Permite a las aplicaciones de EWS obtener acceso a datos de la base de datos de Exchange a través de la red, independientemente de si el cliente está en Internet o la intranet.  <br/> |
|SOAP 1.0  <br/> |Formularios de una envoltura alrededor de la carga de mensajería. EWS implementa el protocolo SOAP mediante el uso de distintas partes de la envoltura SOAP para habilitar la funcionalidad de diferente. El encabezado SOAP se usa para la suplantación y para proporcionar datos de control de versiones. El cuerpo SOAP proporciona información acerca de la operación para ejecutar y los datos que se envían a la operación. SOAP se basa en WSDL para describir las operaciones para llamar a.  <br/> |
|WSDL 1.0  <br/> |Describe los enlaces, las operaciones y las propiedades que se usan para llamar a las operaciones de EWS, en el archivo Services.wsdl. Este archivo, junto con los archivos de esquema que se hace referencia, materializa un contrato entre una aplicación de EWS y el servidor de Exchange y, a menudo se usa junto con las herramientas específicas del proveedor para crear aplicaciones específicas de la plataforma. El archivo WSDL se encuentra en el directorio virtual de EWS, que es la raíz del sitio Web.  <br/> |
|Transport Layer Security (TLS) o SSL  <br/> |Proporciona comunicaciones web seguras en Internet o en la intranet. TLS permite a las aplicaciones autenticar los servidores o, de forma opcional, los servidores para autenticar aplicaciones EWS. También proporciona un canal de seguridad mediante el cifrado de comunicaciones. TLS es la versión más reciente del protocolo de capa de Sockets seguros (SSL).  <br/> |
|XML/XSD  <br/> |Proporciona un formato de mensaje universal para el intercambio de información entre el servidor de Exchange y el cliente. XML proporciona datos complejo de base de datos de Exchange a las aplicaciones cliente, pero en una estructura definida. Lo bueno de XML es que permite incluso cuando una aplicación de EWS y el servidor no comparten una plataforma común para el intercambio de datos.  <br/> |
   
Además, las aplicaciones de EWS deben admitir los estándares de autenticación siguientes:
  
- Autenticación básica a través de SSL, para las aplicaciones que estén destinados a Exchange Online o Exchange local.
    
- Autenticación NTLM a través de SSL, para las aplicaciones que admiten Exchange local.
    
- Autenticación de token de OAuth 2.0, para las aplicaciones de socio de confianza y la interoperabilidad con Lync Server 2013 y SharePoint Server 2013.
    
## <a name="see-also"></a>Vea también


- [Empezar a utilizar servicios web de Exchange](start-using-web-services-in-exchange.md)
    
- [Tipos de aplicación de EWS](ews-application-types.md)
    
- [Introducción al diseño de EWS cliente de Exchange](ews-client-design-overview-for-exchange.md)
    

