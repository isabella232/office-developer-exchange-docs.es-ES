---
title: Desarrollo de Exchange Online y Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.assetid: f33d1093-75ba-4ff2-8d15-b0bf73a401bf
description: Encuentre documentación exhaustiva para desarrolladores de Exchange Server, incluido Exchange online como parte de Office 365 y versiones locales de Exchange Server.
localization_priority: Priority
ms.openlocfilehash: 12a29ca07801561e7a746603d795468d9cb7491f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528499"
---
# <a name="exchange-online-and-exchange-development"></a>Desarrollo de Exchange Online y Exchange

Encuentre documentación exhaustiva para desarrolladores de Exchange Server, incluido Exchange online como parte de Office 365 y versiones locales de Exchange Server.

Puede usar la documentación sobre cómo, introducción, nueva característica y referencia de la API para desarrollar herramientas de acceso y administración de datos de buzones desde servicios, sitios web, equipos de escritorio y dispositivos móviles, y para crear soluciones personalizadas para el correo electrónico, el calendario, los contactos y otros elementos que se almacenan en Exchange online o en un servidor Exchange 2010, 2013, 2016 y 2019.

Puede usar la API de Graph, la API de REST, los servicios web Exchange (EWS), la detección automática, los complementos de Outlook u otras API para desarrollar las aplicaciones. Esta página le ayudará a elegir la tecnología de Exchange más adecuada.

## <a name="exchange-developer-content"></a>Contenido para el desarrollador de Exchange

Use la tabla siguiente para identificar la tecnología y el contenido relacionado de la API que puede ayudarle a alcanzar sus objetivos de desarrollo.

> [!IMPORTANT]
> Microsoft Graph es la API recomendada para acceder a datos de Exchange Online. Las nuevas aplicaciones diseñadas para obtener acceso a datos de Exchange Online deben usar Microsoft Graph.

|Si va a crear…|Empiece aquí|
|:-----|:-----|
|Una aplicación basada en REST para tener acceso a Exchange Online como parte de Office 365.|[API de REST de Microsoft Graph para correo, calendarios y contactos](exchange-web-services/office-365-rest-apis-for-mail-calendars-and-contacts.md) |
|Una aplicación interactiva para mostrar información en Outlook, Outlook Web App o OWA para dispositivos. |[Complementos de Outlook y EWS en Exchange](exchange-web-services/mail-apps-for-outlook-and-ews-in-exchange.md) |
|Un cliente de buzón que no se basa en .NET Framework o Java. |[Explorar la API administrada EWS, EWS y servicios web de Exchange](exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) |
|Un cliente de buzón que utiliza .NET Framework para tener acceso a EWS |[Empezar a trabajar con aplicaciones de cliente de la API administrada EWS](exchange-web-services/get-started-with-ews-managed-api-client-applications.md) |
|Un cliente de buzón que utiliza Java para tener acceso a EWS |[API de Java EWS en GitHub](https://github.com/OfficeDev/ews-java-api) |
|Una aplicación que personaliza la interfaz de usuario de Outlook o se basa en la lógica de negocios de Outlook  |[Referencia de VBA para Outlook](https://msdn.microsoft.com/VBA/VBA-Outlook) |
|Una aplicación destinada a Exchange Online o Exchange 2013 que usted debe migrar de una versión anterior de Exchange.  |[Migrar a las tecnologías de Exchange](migrating-to-exchange-online-and-exchange-2013-technologies.md) |
|Una herramienta de administración personalizada que usa Windows PowerShell desde código administrado   |[Shell de administración de Exchange](management/exchange-management-shell.md) |
|Una solución para realizar copias de seguridad de datos de Exchange o para restaurarlos  |[Copia de seguridad y restauración para Exchange](backup-restore/backup-and-restore-for-exchange-2013.md) |
|Una extensión para la compatibilidad de acceso a mensajes en la canalización de transporte.   |[Agentes de transporte en Exchange](transport-agents/transport-agents-in-exchange-2013.md)  |
|Un cliente de buzón de correo para un dispositivo móvil   |[Exchange ActiveSync](https://technet.microsoft.com/library/aa998357.aspx) |

## <a name="exchange-interactions-with-custom-applications"></a>Interacciones de Exchange con aplicaciones personalizadas

Algunas de estas tecnologías permiten que las aplicaciones funcionen con datos almacenados en Exchange, y otras se utilizan para administrar y controlar el servidor de Exchange. En muchos casos, puede usar más de una tecnología o más de un lenguaje de programación para realizar una tarea, lo que posibilita usar las tecnologías y los lenguajes con los que está familiarizado. Por ejemplo, puede establecer propiedades en elementos en el almacén de Exchange mediante Mail REST API, EWS o API administrada EWS.

Exchange interactúa con las aplicaciones personalizadas de varias maneras, según la arquitectura de la aplicación y la funcionalidad. En esencia, Exchange no solo transporta mensajes, sino que también mantiene los buzones, ejecuta aplicaciones basadas en formularios y mucho más.

|Interacción de Exchange|Descripción|
|:-----|:-----|
|**Transporte de mensajes**|Exchange actúa como un servidor de correo estándar para las aplicaciones con envío de mensajes.<br/>Exchange incluye varias API que transfieren mensajes, incluidos REST, EWS y API administrada EWS.<br/>Asimismo, las aplicaciones pueden utilizar agentes de transporte para responder cuando los mensajes se procesan y se entregan en Exchange. |
|**Almacenamiento de buzones de correo** |Exchange proporciona una estructura jerárquica de carpetas, elementos y propiedades para aplicaciones que acceden a los datos almacenados en los buzones.<br/>Puede tener acceso a esa información almacenada mediante una combinación de estilos de objeto de base de datos y componentes.<br/>Puede realizar consultas en los datos, e Exchange administra el acceso a los datos almacenados en función de los permisos de usuario y almacén.<br/>Las aplicaciones que administran los datos de buzones normalmente usan REST, EWS o la API de administración EWS.|
|**Servidor de administración empresarial** |Exchange funciona como un servidor de administración para las aplicaciones que administran los almacenes y los servidores de Exchange.<br/>Pueden configurar, controlar y supervisar la actividad actual y el estado de los servidores de Exchange en toda la organización.<br/>Las aplicaciones de administración de Exchange usan el Shell de administración de Exchange para administrar los servidores de Exchange. |

## <a name="see-also"></a>Vea también

- 
  [Referencia de la API de servidor para Exchange](https://msdn.microsoft.com/library/dn186243(v=exchg.150).aspx)
- [Obtener información acerca de Exchange en los blogs de Office](https://www.microsoft.com/microsoft-365/blog/)
- [Obtener 101 ejemplos de código para Exchange 2013](https://code.msdn.microsoft.com/office/Exchange-2013-101-Code-3c38582c)
- [Obtener la API administrada EWS (GitHub)](https://github.com/OfficeDev/ews-managed-api/blob/master/README.md)
- [Obtener soporte técnico para Exchange Server](https://support.microsoft.com/getsupport?oaspworkflow=start_1.0.0.0&wf=0&wfname=productselection&gprid=730&x=13&y=7&st=1&wfxredirect=1&sd=gn&ccsid=635890984021344661&forceorigin=esmc)
