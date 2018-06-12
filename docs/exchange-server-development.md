---
title: Desarrollo de Exchange y Exchange Online
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: f33d1093-75ba-4ff2-8d15-b0bf73a401bf
description: Encuentre documentación detallada para desarrolladores para Exchange Server, incluido Exchange Online como parte de Office 365, Exchange Online, Exchange 2013, la API administrada EWS, Exchange 2010 y Exchange 2007.
ms.openlocfilehash: b933bd1bdc6dfcbe4941f23dbee9a587745c7bd7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19762993"
---
# <a name="exchange-online-and-exchange-development"></a>Desarrollo de Exchange y Exchange Online

Encuentre documentación detallada para desarrolladores para Exchange Server, incluido Exchange Online como parte de Office 365, Exchange Online, Exchange 2013, la API administrada EWS, Exchange 2010 y Exchange 2007. 

Puede utilizar el procedimiento para, obtener iniciales, nuevas características y documentación de referencia de API para desarrollar herramientas para obtener acceso y administrar datos de buzón de correo de servicios, sitios Web, los equipos de escritorio y dispositivos móviles y para crear soluciones personalizadas para correo electrónico, calendario, contactos, y otros elementos que se almacenan en Exchange Online o en un servidor de Exchange 2013. 

Puede usar Servicios Web Exchange (EWS), la detección automática, las aplicaciones de correo para Office u otras API para desarrollar sus aplicaciones. Esta página le ayuda a elegir la tecnología de Exchange de la derecha.

## <a name="exchange-developer-content"></a>Contenido de desarrollador de Exchange  

Use la tabla siguiente para identificar el contenido de la API relacionada y la tecnología que le ayudarán a cumplir los objetivos de desarrollo.  
  
|Si va a crear…|Empiece aquí|
|:-----|:-----|
|Una aplicación basada en REST para tener acceso a Exchange Online como parte de Office 365|[API de REST de Office 365 para correo, calendarios y contactos](exchange-web-services/office-365-rest-apis-for-mail-calendars-and-contacts.md) |
|Una aplicación sensible al contexto para mostrar información en Outlook, Outlook Web App u OWA para dispositivos |[Aplicaciones de correo de Outlook y EWS en Exchange](exchange-web-services/mail-apps-for-outlook-and-ews-in-exchange.md) |
|Un cliente de buzón de correo que no se basa en .NET Framework o Java |[Explore la API administrada de EWS, EWS y servicios web de Exchange](exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) |
|Un cliente de buzón de correo que utiliza .NET Framework para tener acceso a EWS |[Empezar a trabajar con aplicaciones de cliente de la API administrada de EWS](exchange-web-services/get-started-with-ews-managed-api-client-applications.md) |
|Un cliente de buzón de correo que utiliza Java para tener acceso a EWS |[API de Java EWS en GitHub](https://github.com/OfficeDev/ews-java-api) |
|Una aplicación que personaliza la interfaz de usuario de Outlook o se basa en la lógica de negocios de Outlook  |[Referencia de VBA para Outlook](https://msdn.microsoft.com/en-us/VBA/VBA-Outlook) |
|Una aplicación que se dirige a Exchange Online o Exchange 2013 que necesita para migrar desde una versión anterior de Exchange  |[Migrar a las tecnologías de Exchange](migrating-to-exchange-online-and-exchange-2013-technologies.md) |
|Una herramienta de administración personalizada que usa Windows PowerShell desde código administrado   |[Shell de administración de Exchange](management/exchange-management-shell.md) |
|Una solución de copia de seguridad o restauración de datos de Exchange  |[Copia de seguridad y restauración para Exchange](backup-restore/backup-and-restore-for-exchange-2013.md) |
|Una extensión para admitir el acceso a mensajes en la canalización de transporte   |[Los agentes de transporte en Exchange](transport-agents/transport-agents-in-exchange-2013.md)  |
|Un cliente de buzón de correo para un dispositivo móvil   |[Exchange ActiveSync](https://technet.microsoft.com/en-us/library/aa998357.aspx) |
   
## <a name="exchange-interactions-with-custom-applications"></a>Interacciones de Exchange con aplicaciones personalizadas

Algunas de estas tecnologías permiten que las aplicaciones funcionen con datos almacenados en Exchange, y otras se utilizan para administrar y controlar el servidor de Exchange. En muchos casos, puede usar más de una tecnología o más de un lenguaje de programación para realizar una tarea, lo que posibilita usar las tecnologías y los lenguajes con los que está familiarizado. Por ejemplo, puede establecer propiedades en elementos en el almacén de Exchange mediante Mail REST API, EWS o API administrada EWS.
  
Exchange interactúa con las aplicaciones personalizadas de varias maneras, según la arquitectura de la aplicación y la funcionalidad. En esencia, Exchange no solo transporta mensajes, sino que también mantiene los buzones, ejecuta aplicaciones basadas en formularios y mucho más.

|Interacción de Exchange|Descripción|
|:-----|:-----|
|**Transporte de mensajes**|Exchange actúa como un servidor de correo estándar para aplicaciones que envían mensajes.<br/>Exchange incluye varias API que transfieren mensajes, incluidos REST, EWS y API administrada EWS.<br/>Además, las aplicaciones pueden utilizar los agentes de transporte para responder a medida que Exchange procesa y entrega los mensajes. |
|**Almacenamiento de buzones** |Exchange proporciona una estructura jerárquica de carpetas, elementos y propiedades para las aplicaciones que tienen acceso a los datos almacenados en los buzones.<br/>Puede tener acceso a esa información almacenada mediante una combinación de estilos de objeto de base de datos y componentes.<br/>Puede realizar consultas en los datos, e Exchange administra el acceso a los datos almacenados en función de los permisos de usuario y almacén.<br/>Las aplicaciones que manejan datos de los buzones suelen usan REST, EWS o API administrada EWS.|
|**Servidor enterprise administrado** |Exchange funciona como un servidor administrado para las aplicaciones que administran servidores y almacenes de Exchange.<br/>Pueden configurar, controlar y supervisar la actividad actual y el estado de los servidores de Exchange en toda la organización.<br/>Las aplicaciones de administración de Exchange usan Shell de administración de Exchange para administrar servidores de Exchange. |
   
## <a name="see-also"></a>Ver también

- [Referencia de API de servidor de Exchange](https://msdn.microsoft.com/en-us/library/dn186243(v=exchg.150).aspx)
- [Leer sobre Exchange en los blogs de Office](https://www.microsoft.com/en-us/microsoft-365/blog/) 
- [Obtener ejemplos de código básicos para Exchange 2013](https://code.msdn.microsoft.com/office/Exchange-2013-101-Code-3c38582c)
- [Obtener la API administrada de EWS (depósito)](https://github.com/OfficeDev/ews-managed-api/blob/master/README.md)
- [Obtener soporte técnico para Exchange Server](https://support.microsoft.com/en-us/getsupport?oaspworkflow=start_1.0.0.0&wf=0&wfname=productselection&gprid=730&x=13&y=7&st=1&wfxredirect=1&sd=gn&ccsid=635890984021344661&forceorigin=esmc)


