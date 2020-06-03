---
title: Empezar a usar los servicios web de Exchange
manager: sethgros
ms.date: 2/26/2019
ms.audience: Developer
ms.assetid: e1b07a92-0595-4bf1-bd6b-c07e66a8c923
description: Obtenga información para ayudarle a empezar a utilizar EWS y otros servicios web en Exchange.
localization_priority: Priority
ms.openlocfilehash: 5980e22599585aa376890a414e0e8e7c7c5c707a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463758"
---
# <a name="start-using-web-services-in-exchange"></a>Empezar a usar los servicios web de Exchange

Obtenga información para ayudarle a empezar a utilizar EWS y otros servicios web en Exchange.
  
Los [servicios Web de Exchange](explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) proporcionan acceso a los datos de buzón almacenados en Exchange Online, Exchange online como parte de Office 365 y las versiones locales de Exchange a partir de exchange Server 2007, y permiten crear aplicaciones personalizadas que se pueden usar para administrar dicha información de acuerdo con los requisitos de la organización. Aunque el intervalo de aplicaciones de servicio EWS y Web que se pueden crear es prácticamente infinito, se aplican algunos conceptos fundamentales para cualquier tipo de aplicación. En esta sección se proporciona información sobre los conceptos fundamentales con los que debe estar familiarizado para empezar a usar EWS y otros servicios web en Exchange. 
  
## <a name="build-your-knowledge"></a>Crear sus conocimientos
<a name="bk_Knowledge"> </a>

Independientemente de si usa .NET Framework u otra plataforma para desarrollar la aplicación de servicio Web, le interesará conocer algunos conceptos importantes antes de comenzar el proyecto de desarrollo. 
  
**Tabla 1. Conceptos de servicios Web**

|**Concepto**|**Resumen**|
|:-----|:-----|
|[Arquitectura](ews-applications-and-the-exchange-architecture.md) <br/> |Obtenga información sobre cómo funciona EWS en la arquitectura de Exchange y los protocolos que usa.  <br/> |
|[Tipos de aplicación de EWS](ews-application-types.md) <br/> |Obtenga información sobre los tipos de aplicaciones más comunes que puede crear con EWS en Exchange.  <br/> |
|[Acceso a EWS](controlling-client-application-access-to-ews-in-exchange.md) <br/> |Los administradores de Exchange pueden limitar el acceso a EWS de forma global para toda la organización, para usuarios individuales y para aplicaciones individuales. Averigüe qué nivel de acceso es el más adecuado para usted.  <br/> |
|[Instalación](setting-up-your-ews-application.md) <br/> |Busque información sobre las tareas que debe completar para crear aplicaciones que usen la API administrada de EWS o EWS para comunicarse con Exchange.  <br/> |
|[Autenticación](authentication-and-ews-in-exchange.md) <br/> |Obtenga información sobre las opciones de autenticación para conectarse a Exchange Online y Exchange local.  <br/> |
|[Detección automática](autodiscover-for-exchange.md) <br/> |Obtenga información sobre el conjunto de servicios que puede usar para detectar el punto de conexión de dirección URL donde la cuenta de un usuario puede tener acceso a la información a través de EWS.  <br/> |
|[Servidor de buzones](https://technet.microsoft.com/library/jj150491%28v=exchg.150%29.aspx) <br/> |Descubra el repositorio principal de la información que está disponible para un cliente de EWS. EWS tiene acceso a un conjunto limitado de información almacenada en los servicios de dominio de Active Directory (AD DS).  <br/> |
|[Aplicaciones de correo para Outlook y EWS](mail-apps-for-outlook-and-ews-in-exchange.md) <br/> |Busque información sobre las aplicaciones de correo para Outlook y cómo funcionan con EWS en Exchange.  <br/> |
|[API de REST de Office 365 para correo, calendarios y contactos](office-365-rest-apis-for-mail-calendars-and-contacts.md) <br/> |Obtenga información sobre las API de Office 365 que puede usar para tener acceso al correo, calendarios y contactos en Exchange online como parte de Office 365.  <br/> |
|[La API administrada EWS](get-started-with-ews-managed-api-client-applications.md) <br/> |Busque información sobre la API de cliente preferida para desarrolladores de .NET Framework.  <br/> |
|[EWS](get-started-with-ews-client-applications.md) <br/> |Obtenga información sobre cómo crear su primera aplicación con las solicitudes y respuestas de XML de EWS.  <br/> |
|[Funcionalidad de EWS en versiones de producto de Exchange](ews-functionality-in-exchange-product-versions.md) <br/> |Descubra qué funcionalidad de EWS está disponible en la versión de Exchange.  <br/> |
|[Seguimiento y solución de problemas](how-to-trace-requests-responses-to-troubleshoot-ews-managed-api-applications.md) <br/> |Descubra cómo realizar un seguimiento de las solicitudes y respuestas de EWS para solucionar errores en la aplicación de la API administrada de EWS.  <br/> |
   
## <a name="create-your-first-application"></a>Crear la primera aplicación
<a name="create"> </a>

Si está listo para llegar a la empresa de escribir su primera aplicación cliente de .NET Framework o EWS, consulte Introducción a [las aplicaciones cliente de la API administrada de EWS](get-started-with-ews-managed-api-client-applications.md) o Introducción [a las aplicaciones cliente de EWS](get-started-with-ews-client-applications.md).
  
## <a name="get-code-samples"></a>Obtener ejemplos de código
<a name="samples"> </a>

Para buscar ejemplos de código y ejemplos que muestren cómo trabajar con EWS y otros servicios web en Exchange, consulte los siguientes recursos:
  
- [Ejemplos de código de Exchange](https://code.msdn.microsoft.com/exchange)
    
- [CodePlex](http://www.codeplex.com/)
    
- [Documentación de la API de Exchange](develop-web-service-clients-for-exchange.md)
    
- [Foro de desarrollo de Exchange](https://social.technet.microsoft.com/Forums/exchange/home?forum=exchangesvrdevelopment)
    
Hay muchos otros ejemplos disponibles en blogs, sitios de demostración de código y foros. También le recomendamos que descargue [EWSEditor](http://ewseditor.codeplex.com/). Este proyecto implementa la mayor parte de la funcionalidad de EWS; Aquí puede encontrar ejemplos de todas las funcionalidades principales de EWS.
  
Si no es desarrollador de .NET Framework, puede encontrar muchas bibliotecas de cliente en el desarrollo de EWS que usan Java, Python, PHP y otros lenguajes. 
  
## <a name="ask-questions-and-solve-problems"></a>Formular preguntas y solucionar problemas
<a name="questions"> </a>

¿Necesita ayuda para hacer cosas y no encuentra respuestas? Puede buscar en el [Foro de desarrollo de Exchange](https://social.technet.microsoft.com/Forums/exchange/home?forum=exchangesvrdevelopment) para averiguar si otra persona ha encontrado y resuelto el mismo problema. Una comunidad de colaboradores ha respondido a cientos de preguntas sobre el desarrollo de Exchange. También puede encontrar sitios, foros y blogs de terceros que cubren el desarrollo de Exchange y pueden tener la solución que está buscando. 
  
Póngase en contacto [con el soporte técnico de Microsoft](https://support.microsoft.com/) si necesita ayuda adicional. El equipo de soporte técnico para desarrolladores de Exchange cuenta con profesionales veteranos que pueden ayudarle a responder sus preguntas sobre el desarrollo de Exchange. 
  
## <a name="see-also"></a>Vea también

- [Explore la API administrada de EWS, EWS y servicios web de Exchange](explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) 
- [Introducción al diseño de EWS cliente de Exchange](ews-client-design-overview-for-exchange.md) 
- [Desarrollar clientes de servicios web de Exchange](develop-web-service-clients-for-exchange.md) 
- [Referencia de servicios web para Exchange](../web-service-reference/web-services-reference-for-exchange.md)
    

