---
title: API de Outlook de Microsoft Graph para correo, calendarios y contactos
manager: sethgros
ms.date: 07/27/2018
ms.audience: Developer
ms.assetid: 3b2e71a6-5fa5-4008-b243-d3a6e9173b3d
description: Busque información sobre la API de Microsoft Graph que puede usar para tener acceso al correo, calendarios y contactos en Office 365 o Exchange Online.
localization_priority: Priority
ms.openlocfilehash: 7ca77596afb59ffab76001abd495de7328d2dd29
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463870"
---
# <a name="microsoft-graph-rest-apis-for-mail-calendars-and-contacts"></a>API de REST de Microsoft Graph para correo, calendarios y contactos

Busque información sobre las API de Microsoft Graph que puede usar para tener acceso al correo, calendarios y contactos en Office 365, Exchange online o Exchange Server en implementaciones híbridas.

Office 365, Exchange Online y Exchange Server en implementaciones híbridas proporcionan una nueva forma de trabajar con el correo electrónico, los calendarios y los contactos. Las API de REST de Microsoft Graph de correo, calendario y contactos ofrecen una forma eficaz y sencilla de obtener acceso a los datos de Exchange y manipularlos. Estas API se basan en estándares abiertos: OAuth versión 2.0 para la autenticación y la versión 4.0 de OData y JSON para la abstracción de datos. Esto proporciona las siguientes ventajas:

- Como estas API requieren OAuth para la autenticación, no es necesario que la aplicación controle ni almacene las credenciales de usuario.

- OAuth permite solicitar permisos con ámbito estrecho para datos de usuario. Por ejemplo, puede diseñar la aplicación para que solicite permiso y lea únicamente el calendario de un usuario.

## <a name="work-with-email-and-mail-folders"></a>Trabajar con las carpetas de correo electrónico y correo

Puede usar la [API de correo](https://developer.microsoft.com/graph/docs/concepts/outlook-mail-concept-overview) para obtener, crear, actualizar, eliminar, mover, copiar y enviar correo electrónico. También puede obtener, crear, actualizar y eliminar carpetas de correo. 
  
## <a name="work-with-events-calendars-and-calendar-groups"></a>Trabajar con grupos de calendario, calendarios y eventos

Puede usar la [API de calendario](https://developer.microsoft.com/graph/docs/concepts/outlook-calendar-concept-overview) para obtener, crear, actualizar y eliminar eventos. También puede obtener, crear, actualizar y eliminar calendarios y grupos de calendario. 
  
## <a name="work-with-contacts-and-contact-folders"></a>Trabajar con contactos y carpetas de contactos

Puede usar la [API de contactos](https://developer.microsoft.com/graph/docs/concepts/outlook-contacts-concept-overview) para obtener, crear, actualizar y eliminar los contactos en el buzón de un usuario. También puede obtener carpetas de contactos. 
  
## <a name="next-steps"></a>Siguientes pasos

Entre en la página [Documentación de Microsoft Graph](https://developer.microsoft.com/graph/docs/concepts/overview) para obtener más información sobre las API de correo, calendario y contactos y consultar las instrucciones para la configuración de su entorno y la introducción a las API. 

Consulte también los [inicios rápidos](https://developer.microsoft.com/graph/quick-start) y los [ejemplos de códigos](https://developer.microsoft.com/office/gallery/?filterBy=Samples,Microsoft%20Graph) para ver esas API en funcionamiento. 
  
## <a name="see-also"></a>Vea también

- [Documentación de Microsoft Graph](https://developer.microsoft.com/graph/docs/concepts/overview)   
- [Requisitos locales para la API de REST](https://blogs.technet.microsoft.com/exchange/2016/09/26/on-premises-architectural-requirements-for-the-rest-api)   

