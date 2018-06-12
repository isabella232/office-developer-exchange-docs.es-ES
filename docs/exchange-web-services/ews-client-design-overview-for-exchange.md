---
title: Información general sobre el diseño de cliente EWS para Exchange
manager: sethgros
ms.date: 3/11/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: b26f67aa-7c66-4d7d-98b3-746f26ab37f4
description: Obtenga información sobre las consideraciones de diseño para el desarrollo con EWS para Exchange.
ms.openlocfilehash: ea0e1ad3f8402d19a6163f3320a2a17f08f3ea2a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763011"
---
# <a name="ews-client-design-overview-for-exchange"></a>Información general sobre el diseño de cliente EWS para Exchange

Obtenga información sobre las consideraciones de diseño para el desarrollo con EWS para Exchange. 
  
En este artículo se proporciona información general acerca del diseño de una aplicación de servicios Web de Exchange (EWS). Puede usar esta información para determinar si EWS es la API adecuada para su aplicación y, si es así, ¿qué tipo de implementación de cliente debe usar. En este artículo también proporciona información de las prácticas recomendada para el diseño de aplicaciones que pueden tener como destino Office 365, Exchange Online y versiones de Exchange comenzando con Exchange 2007, en una base de código y los puntos de decisión importante para la identificación de Exchange local servidores frente a identificación de Exchange Online.
  
## <a name="is-ews-the-right-api-for-your-application"></a>¿Es EWS la API adecuada para su aplicación?
<a name="IsEWSRight"> </a>

Antes de comenzar a diseñar la aplicación, es importante tener en cuenta si EWS es la API adecuada para usted. Si está desarrollando en el servidor de Exchange o Exchange Online, EWS es la tecnología de acceso de cliente preferido. Desarrollo de acceso de cliente para las versiones de Exchange a partir de Exchange 2007 se ha centrado principalmente en EWS. Nueva funcionalidad de acceso de cliente que se implementa en Outlook usa EWS, incluidas las características de fuera de oficina (OOF) y la disponibilidad de Exchange 2007 y la funcionalidad de sugerencias de correo electrónico y obtener salones introducida en Exchange 2010. Esto representa una inversión confirman en EWS para socios internos y externos que desarrollan aplicaciones de cliente de Exchange.
  
EWS es la API de acceso de cliente principal para las aplicaciones de cliente de Exchange. Sin embargo, en algunos casos, es posible que tenga en cuenta otras API de Exchange para el desarrollo de aplicaciones cliente. Por ejemplo, Exchange ActiveSync ofrece las siguientes ventajas a través de EWS:
  
- Se ha con acortado la estructura XML para hacer un protocolo más compacto que Exchange ActiveSync.  
- Exchange ActiveSync contiene un mecanismo de directivas para controlar el acceso de cliente y para proporcionar soluciones de mensajería móviles de otra empresa sólida.
    
> [!NOTE]
> Necesita una licencia con el fin de desarrollar a los clientes de Exchange ActiveSync. Para obtener información sobre las diferencias entre Exchange ActiveSync y EWS, consulte [elegir entre Exchange ActiveSync y Exchange Web Services (EWS)](http://msdn.microsoft.com/en-us/library/dn144954%28v=exchg.140%29.aspx). 
  
MAPI RPC sobre HTTP es otra opción de programación para aplicaciones de cliente de Exchange. Sin embargo, MAPI RPC sobre HTTP no proporciona una interfaz intuitiva para la comunicación entre los clientes y el servidor.
  
Para obtener más información sobre las tecnologías de desarrollo de Exchange, vea [Explorar la API administrada de EWS, EWS y web de servicios de Exchange](explore-the-ews-managed-api-ews-and-web-services-in-exchange.md).
  
## <a name="options-for-ews-client-development"></a>Opciones para el desarrollo de cliente EWS
<a name="EWSClientOptions"> </a>

Varias opciones están disponibles para el desarrollo en Exchange mediante el uso de EWS. La mejor opción para usted dependerá de la plataforma de desarrollo, herramientas, implementaciones disponibles y requisitos de la aplicación para su organización. Las siguientes son las cuatro opciones principales que están disponibles para crear aplicaciones de cliente EWS:
  
- La API administrada EWS
- La API de Java EWS
- Los servidores proxy generado automáticamente EWS
- Una API de cliente EWS personalizado
    
### <a name="ews-managed-api"></a>API administrada EWS

La [API administrada de EWS](http://aka.ms/ews-managed-api-readme) es un cliente de servicios web personalizados. Es la API de acceso de cliente estándar para las aplicaciones de .NET Framework. 
  
Las siguientes son algunas de las ventajas del uso de la API administrada de EWS:
  
- Proporciona un modelo de objetos intuitiva.   
- Simplifica la complejidad de la descripción del servicio en los archivos de esquema y WSDL.   
- Incluye la lógica empresarial de cliente.   
- Controla las solicitudes web y respuestas y serialización de objetos y deserialización.   
- Es compatible con Microsoft.
    
Sin embargo, tenga en cuenta que la API administrada de EWS no es una solución completa. Algunas de las funciones no se implementan en la API administrada de EWS. Aunque la API administrada de EWS no implementa toda la funcionalidad de EWS, sería la mejor opción para el desarrollo de aplicaciones cliente, por los motivos siguientes:
  
- Puede usar .NET Framework para el desarrollo.
- Implementa la detección automática además de la mayoría de las partes del modelo de objetos EWS.
- Implementa la lógica de negocios de lado cliente para trabajar con EWS, en la clase [ExchangeService](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) . 
    
Decide usar la API del servicio web EWS en lugar de la API administrada de EWS para cualquiera de las siguientes razones:
  
- La aplicación no usa .NET Framework. 
- No desea distribuir el ensamblado de la API administrada de EWS. 
- La aplicación usa características que no están implementadas en la API administrada de EWS.
    
Para obtener más información, vea [Introducción a las aplicaciones cliente de API administrada de EWS](get-started-with-ews-managed-api-client-applications.md).
  
> [!NOTE]
> [!NOTA] La API administrada EWS ya está disponible como un proyecto de código abierto en [GitHub](http://aka.ms/ews-managed-api-github). Puede usar la biblioteca de código abierto para: 
> - Contribuir con correcciones de errores y mejoras a la API. 
> - Obtener correcciones y mejoras antes de que estén disponibles en una versión oficial.
> - Tener acceso a una implementación más completa y actualizada de la API, para usarla como referencia o para crear nuevas bibliotecas en nuevas plataformas. 
> 
> Le agradecemos sus [contribuciones](https://github.com/OfficeDev/ews-managed-api/blob/master/CONTRIBUTING.md) a través de depósito. 
  
### <a name="ews-java-api"></a>API Java EWS

La API de Java de EWS es un proyecto de código abierto en [depósito](https://github.com/OfficeDev/ews-java-api) que puede ser actualizada y extendida por la Comunidad. Es asimilar similar a la [API administrada de EWS](http://msdn.microsoft.com/en-us/library/office/jj220535%28v=exchg.80%29.aspx) y utiliza solicitudes y respuestas SOAP de EWS por el cable. Aunque no se puede obtener acceso a todas las [operaciones de EWS SOAP](http://msdn.microsoft.com/library/cf6fd871-9a65-4f34-8557-c8c71dd7ce09%28Office.15%29.aspx) mediante el uso de la API de Java EWS, con la [creación de reciente](http://blogs.office.com/2014/08/28/open-sourcing-exchange-web-services-ews-java-api/) del proyecto de código abierto, buscamos a la Comunidad para cerrar esta brecha. Tenga en cuenta que Microsoft Support, con un contrato de soporte adecuados, abordará cualquier preguntas relacionadas con el protocolo SOAP de EWS, pero no la API de Java de EWS propio. La API de Java de EWS está disponible para descarga y la Comunidad contribución en [depósito](https://github.com/OfficeDev/ews-java-api).
  
### <a name="ews-autogenerated-proxies"></a>Servidores proxy EWS generado automáticamente

API de cliente generado automáticamente se generan a partir de WSDL de EWS y definiciones de esquema XML. Generadores de modelo de objetos de cliente están disponibles para muchos idiomas. En general, los modelos de objetos generado automáticamente administran objeto serialización y deserialización. No incluya la lógica empresarial y el proceso de autogeneración a menudo crea artefactos que realizar menos intuitivo para usar el modelo de objetos. Soporte de Exchange, explica el XML que es enviado y recibido por el cliente pero no en el modelo de objetos.
  
### <a name="custom-ews-client-api"></a>API de cliente EWS personalizada

Para algunas aplicaciones que usan un conjunto reducido de la funcionalidad EWS, es posible que cree a un cliente personalizado API para comunicarse con Exchange. Esto le permite consumir menos recursos del sistema. Esto es útil para los clientes que se ejecutan en dispositivos con limitaciones de memoria, como los clientes que ejecutan la Micro de .NET Framework.
  
## <a name="ews-client-features"></a>Características de cliente EWS
<a name="EWSFeatures"> </a>

Independientemente de la opción de desarrollo que elija, debe tener en cuenta cómo se implementan las características EWS en su cliente. Disponibilidad de la característica se basa en la versión del esquema EWS que los objetivos de la aplicación. Debido a que los esquemas EWS están con versiones anteriores y forward-compatible con, si se crea una aplicación que tiene como destino una versión anterior de esquema, como Exchange Server 2007 SP1, la aplicación también funcionará con una versión posterior de esquema, como el SP1 de Exchange Server 2013 servicio, así como Exchange Online. 
  
Debido a que las características y actualizaciones de característica controladas por el esquema, se recomienda usar el código común más antigua base destinado a las características EWS que se va a implementar en la aplicación cliente. Muchas aplicaciones pueden dirigir la versión Exchange2007_SP1, debido a que el esquema de Exchange 2007 SP1 contiene casi todas la funcionalidad principal de Exchange para trabajar con elementos y carpetas en el almacén de Exchange. Se recomienda mantener bifurcaciones de código para cada versión del esquema de EWS. Los siguientes son las versiones de esquema que están actualmente disponibles. 
  
```XML
  <xs:simpleType name="ExchangeVersionType">
    <xs:restriction base="xs:string">
      <xs:enumeration value="Exchange2007" />
      <xs:enumeration value="Exchange2007_SP1" />
      <xs:enumeration value="Exchange2010" />
      <xs:enumeration value="Exchange2010_SP1" />
      <xs:enumeration value="Exchange2010_SP2" />
      <xs:enumeration value="Exchange2013" />
      <xs:enumeration value="Exchange2013_SP1" />
    </xs:restriction>
  </xs:simpleType>
```

Las versiones de esquema se mantienen en el tipo simple **ExchangeVersionType** . 
  
Para obtener información acerca de las características que están disponibles en cada versión del esquema de EWS, consulte [las versiones de esquema EWS en Exchange](ews-schema-versions-in-exchange.md).
  
## <a name="in-this-section"></a>En esta sección
<a name="bk_inthissection"> </a>

- [Disponibilidad de característica del servicio Web de API de Exchange y la API administrada de EWS](web-service-api-feature-availability-in-exchange-and-the-ews-managed-api.md)
    
- [Versiones de esquema EWS en Exchange](ews-schema-versions-in-exchange.md)
    
- [Opciones de configuración para EWS en Exchange](configuration-options-for-ews-in-exchange.md)
    
- [Comparación de Exchange Online y la programación de cliente de Exchange local](comparing-exchange-online-and-exchange-on-premises-client-programming.md)
    
- [EWS limitación en Exchange](ews-throttling-in-exchange.md)
    
- [Requisitos de redistribución para la API administrada de EWS](redistribution-requirements-for-the-ews-managed-api.md)
    
- [Instrumentación de las solicitudes de cliente para EWS y REST en Exchange](instrumenting-client-requests-for-ews-and-rest-in-exchange.md)
    
## <a name="see-also"></a>Ver también
 
- [Empezar a utilizar servicios web de Exchange](start-using-web-services-in-exchange.md)
- [Desarrollo de clientes de servicios web de Exchange](develop-web-service-clients-for-exchange.md) 
- [Tipos de aplicación de EWS](ews-application-types.md)
    

