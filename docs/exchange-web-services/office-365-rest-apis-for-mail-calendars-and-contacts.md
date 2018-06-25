---
title: API de REST de Office 365 para correo, calendarios y contactos
manager: sethgros
ms.date: 4/29/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3b2e71a6-5fa5-4008-b243-d3a6e9173b3d
description: Busque información sobre las API de Office 365 que puede usar para tener acceso al correo, calendarios y contactos en Office 365 o Exchange Online.
ms.openlocfilehash: d42d3ff0b68dfbf23d5a4eebb826a6d39a4ac116
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763291"
---
# <a name="office-365-rest-apis-for-mail-calendars-and-contacts"></a>API de REST de Office 365 para correo, calendarios y contactos

Este documento puede incluir contenido relacionado con funciones o productos preliminares que pueden cambiar mucho antes del lanzamiento comercial final. Este documento se proporciona "tal cual" solamente con fines informativos y Microsoft no realiza ninguna garantía, explícita ni implícita, en el documento. Busque información sobre las API de Office 365 que puede usar para tener acceso al correo, calendarios y contactos en Office 365 o Exchange Online.
  
Office 365 y Exchange Online ofrecen una nueva forma de trabajar con correo electrónico, calendarios y contactos. Las API de REST de correo, calendario y contactos proporcionan una forma eficaz y sencilla para obtener acceso a los datos de Exchange y manipularlos. Estas API se basan en estándares abiertos: OAuth versión 2.0 para la autenticación y la versión 4.0 de OData y JSON para la abstracción de datos. Esto proporciona las siguientes ventajas:
  
- Como estas API requieren OAuth para la autenticación, no es necesario que la aplicación controle ni almacene las credenciales de usuario.
    
- OAuth permite solicitar permisos con ámbito estrecho para datos de usuario. Por ejemplo, puede diseñar la aplicación para que solicite permiso y lea únicamente el calendario de un usuario.
    
## <a name="work-with-email-and-mail-folders"></a>Trabajar con las carpetas de correo electrónico y correo

Puede usar la [API de correo](http://msdn.microsoft.com/office/office365/api/mail-rest-operations%28Office.15%29.aspx) para obtener, crear, actualizar, eliminar, mover, copiar y enviar correo electrónico. También puede obtener, crear, actualizar y eliminar carpetas de correo. 
  
## <a name="work-with-events-calendars-and-calendar-groups"></a>Trabajar con grupos de calendario, calendarios y eventos

Puede usar la [API de calendario](http://msdn.microsoft.com/office/office365/api/calendar-rest-operations%28Office.15%29.aspx) para obtener, crear, actualizar y eliminar eventos. También puede obtener, crear, actualizar y eliminar calendarios y grupos de calendario. 
  
## <a name="work-with-contacts-and-contact-folders"></a>Trabajar con contactos y carpetas de contactos

Puede usar la [API de contactos](http://msdn.microsoft.com/office/office365/api/contacts-rest-operations%28Office.15%29.aspx) para obtener, crear, actualizar y eliminar los contactos en el buzón de un usuario. También puede obtener carpetas de contactos. 
  
## <a name="work-with-file-providers"></a>Trabajar con proveedores de archivos

Puede usar la [API de REST de proveedores de archivos](http://msdn.microsoft.com/library/8bab5403-de68-4b49-ab19-9a6470f2a2ce%28Office.15%29.aspx) para obtener, crear, actualizar y eliminar información sobre proveedores de archivos compatibles, como buzones, Dropbox, etc. 
  
## <a name="next-steps"></a>Pasos siguientes

Entre en la página [Desarrollo en la plataforma Office 365](http://msdn.microsoft.com/office/office365/howto/platform-development-overview%28Office.15%29.aspx) para obtener más información sobre las API de correo, calendario y contactos y consultar las instrucciones para la configuración de su entorno y la introducción a las API. Asegúrese también de desproteger los [proyectos inicial y ejemplos de código](http://msdn.microsoft.com/office/office365/howto/Starter-projects-and-code-samples%28Office.15%29.aspx) para ver estas API en acción. 
  
## <a name="see-also"></a>Vea también


- [Desarrollo en la plataforma Office 365](http://msdn.microsoft.com/office/office365/howto/platform-development-overview%28Office.15%29.aspx)
    
- [Creación de una aplicación ASP.NET MVC de Office 365](http://msdn.microsoft.com/office/office365/howto/Build-your-first-ASPNET-MVC-app%28Office.15%29.aspx)
    
- [Operaciones del REST de correo](http://msdn.microsoft.com/office/office365/api/mail-rest-operations%28Office.15%29.aspx)
    
- [Operaciones del REST de calendario](http://msdn.microsoft.com/office/office365/api/calendar-rest-operations%28Office.15%29.aspx)
    
- [Operaciones del REST de contactos](http://msdn.microsoft.com/office/office365/api/contacts-rest-operations%28Office.15%29.aspx)
    
- [Proyectos iniciales de las API de Office 365 y ejemplos de código](http://msdn.microsoft.com/office/office365/howto/Starter-projects-and-code-samples%28Office.15%29.aspx)
    

