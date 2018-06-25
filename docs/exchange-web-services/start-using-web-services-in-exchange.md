---
title: Empezar a usar servicios web de Exchange
manager: sethgros
ms.date: 2/27/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: e1b07a92-0595-4bf1-bd6b-c07e66a8c923
description: Obtenga información que le ayudarán a empezar a trabajar con EWS y otros servicios web de Exchange.
ms.openlocfilehash: 2f203c5634c29105feb39220c3ebdd9624bb49ec
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763301"
---
# <a name="start-using-web-services-in-exchange"></a>Empezar a usar servicios web de Exchange

Obtenga información que le ayudarán a empezar a trabajar con EWS y otros servicios web de Exchange.
  
Los [servicios web de Exchange](explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)proporcionan acceso a datos de los buzones almacenados en Exchange Online, Exchange Online como parte de Office 365 y las versiones locales de Exchange a partir de Exchange Server 2007 y permiten crear aplicaciones personalizadas que se puede usar para administrar esa información según los requisitos de su organización. Mientras que el intervalo de EWS y web de aplicaciones de servicio que se pueden crear es prácticamente infinito, se aplican ciertos conceptos fundamentales para cualquier tipo de aplicación. En esta sección se proporciona información sobre los conceptos fundamentales que necesita estar familiarizado con el fin de empezar a usar EWS y otros servicios web de Exchange. 
  
## <a name="build-your-knowledge"></a>Generar su conocimiento
<a name="bk_Knowledge"> </a>

Independientemente de si usa .NET Framework u otra plataforma para desarrollar la aplicación de servicio web, desea comprender algunos conceptos importantes antes de comenzar su proyecto de desarrollo. 
  
**La tabla 1. Conceptos de los servicios Web**

|**Concepto**|**Resumen**|
|:-----|:-----|
|[Arquitectura](ews-applications-and-the-exchange-architecture.md) <br/> |Obtenga información sobre cómo funciona la EWS dentro de la arquitectura de Exchange y los protocolos que utiliza.  <br/> |
|[Tipos de aplicación de EWS](ews-application-types.md) <br/> |Obtenga información acerca de los tipos más comunes de aplicaciones que se pueden crear mediante el uso de EWS en Exchange.  <br/> |
|[Acceso a EWS](controlling-client-application-access-to-ews-in-exchange.md) <br/> |Los administradores de Exchange pueden limitar el acceso a EWS globalmente para toda la organización, para usuarios individuales y a las aplicaciones individuales. Averiguar qué nivel de acceso es el adecuado para usted.  <br/> |
|[Setup](setting-up-your-ews-application.md) <br/> |Encuentre información acerca de las tareas que necesita para llevar a cabo con el fin de crear aplicaciones que usan la API administrada de EWS o EWS para comunicarse con Exchange.  <br/> |
|[Autenticación](authentication-and-ews-in-exchange.md) <br/> |Obtenga información sobre las opciones de autenticación para conectarse a Exchange Online y Exchange local.  <br/> |
|[Detección automática](autodiscover-for-exchange.md) <br/> |Obtenga información sobre el conjunto de servicios que puede usar para detectar el extremo de la dirección URL donde una cuenta de usuario puede tener acceso a información a través de EWS.  <br/> |
|[Servidor de buzones](http://technet.microsoft.com/en-us/library/jj150491%28v=exchg.150%29.aspx) <br/> |Obtenga información acerca del repositorio principal de la información disponible para un cliente de EWS. EWS tiene acceso un limitado a conjunto de información almacenada en los servicios de dominio de Active Directory (AD DS).  <br/> |
|[Aplicaciones de correo para Outlook y EWS](mail-apps-for-outlook-and-ews-in-exchange.md) <br/> |Obtenga información acerca de las aplicaciones de correo para Outlook y cómo funcionan con EWS en Exchange.  <br/> |
|[API de REST de Office 365 para correo, calendarios y contactos](office-365-rest-apis-for-mail-calendars-and-contacts.md) <br/> |Obtenga información sobre las API de Office 365 que puede usar para tener acceso a correo, calendarios y contactos en Exchange Online como parte de Office 365.  <br/> |
|[La API administrada de EWS](get-started-with-ews-managed-api-client-applications.md) <br/> |Obtenga información sobre la API de cliente preferido para los programadores de .NET Framework.  <br/> |
|[EWS](get-started-with-ews-client-applications.md) <br/> |Obtenga información acerca de cómo crear su primera aplicación mediante el uso de EWS XML solicitudes y respuestas.  <br/> |
|[Funcionalidad EWS en versiones de producto de Exchange](ews-functionality-in-exchange-product-versions.md) <br/> |Averigüe qué funcionalidad EWS está disponible en la versión de Exchange.  <br/> |
|[Seguimiento y solucionar problemas](how-to-trace-requests-responses-to-troubleshoot-ews-managed-api-applications.md) <br/> |Descubra cómo realizar un seguimiento de las solicitudes EWS y respuestas con el fin de solucionar problemas de errores en la aplicación de la API administrada de EWS.  <br/> |
   
## <a name="create-your-first-application"></a>Crear su primera aplicación
<a name="create"> </a>

Si está listo para llegar a la empresa de escribir su primera .NET Framework o la aplicación de cliente EWS, vea [Introducción a las aplicaciones cliente de API administrada de EWS](get-started-with-ews-managed-api-client-applications.md) o [empezar a trabajar con las aplicaciones cliente EWS](get-started-with-ews-client-applications.md).
  
## <a name="get-code-samples"></a>Obtener ejemplos de código
<a name="samples"> </a>

Para obtener ejemplos de código y ejemplos que muestran cómo trabajar con EWS y otros servicios web de Exchange, consulte los siguientes recursos:
  
- [Ejemplos de código de Exchange](http://code.msdn.microsoft.com/exchange)
    
- [CodePlex](http://www.codeplex.com/)
    
- [Documentación de la API de Exchange](develop-web-service-clients-for-exchange.md)
    
- [Foro de desarrollo de Exchange](http://social.technet.microsoft.com/Forums/exchange/en-US/home?forum=exchangesvrdevelopment)
    
Muchos otros ejemplos están disponibles en blogs, sitios de demostración de código y foros. También se recomienda que descargue el [EWSEditor](http://ewseditor.codeplex.com/). Este proyecto implementa la mayor parte de la funcionalidad EWS; puede encontrar ejemplos de todas la funcionalidad básica de EWS aquí.
  
Si no es un programador de .NET Framework, puede encontrar muchas bibliotecas cliente ahí para el desarrollo de EWS que usan Java, Python, PHP y otros idiomas. 
  
## <a name="ask-questions-and-solve-problems"></a>Formular preguntas y resolver los problemas
<a name="questions"> </a>

¿Necesita ayuda para hacer cosas y no encuentra respuestas? Puede buscar en el [foro de desarrollo de Exchange](http://social.technet.microsoft.com/Forums/exchange/en-US/home?forum=exchangesvrdevelopment) para averiguar si alguien ha detectado y resuelto el mismo problema. Una comunidad de colaboradores ha respondido a cientos de preguntas sobre el desarrollo de Exchange. También puede encontrar sitios de otros fabricantes, foros y blogs que tratan el desarrollo de Exchange y es posible que tiene la solución que está buscando. 
  
Póngase en contacto con [soporte técnico de Microsoft](https://support.microsoft.com/) si necesita ayuda adicional. El equipo de soporte técnico para desarrolladores de Exchange cuenta con experimentados profesionales de TI que pueden ayudar a responder a sus preguntas sobre el desarrollo de Exchange. 
  
## <a name="see-also"></a>Vea también

- [Explore la API administrada de EWS, EWS y servicios web de Exchange](explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) 
- [Introducción al diseño de EWS cliente de Exchange](ews-client-design-overview-for-exchange.md) 
- [Desarrollo de clientes de servicios web de Exchange](develop-web-service-clients-for-exchange.md) 
- [Referencia de servicios Web de Exchange](../web-service-reference/web-services-reference-for-exchange.md)
    

