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
# <a name="office-365-rest-apis-for-mail-calendars-and-contacts"></a><span data-ttu-id="d9dc5-103">API de REST de Office 365 para correo, calendarios y contactos</span><span class="sxs-lookup"><span data-stu-id="d9dc5-103">Office 365 REST APIs for mail, calendars, and contacts</span></span>

<span data-ttu-id="d9dc5-104">Este documento puede incluir contenido relacionado con funciones o productos preliminares que pueden cambiar mucho antes del lanzamiento comercial final. Este documento se proporciona "tal cual" solamente con fines informativos y Microsoft no realiza ninguna garantía, explícita ni implícita, en el documento. Busque información sobre las API de Office 365 que puede usar para tener acceso al correo, calendarios y contactos en Office 365 o Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="d9dc5-104">Find information about the Office 365 APIs that you can use to access mail, calendars, and contacts in Office 365 or Exchange Online.</span></span>
  
<span data-ttu-id="d9dc5-p101">Office 365 y Exchange Online ofrecen una nueva forma de trabajar con correo electrónico, calendarios y contactos. Las API de REST de correo, calendario y contactos proporcionan una forma eficaz y sencilla para obtener acceso a los datos de Exchange y manipularlos. Estas API se basan en estándares abiertos: OAuth versión 2.0 para la autenticación y la versión 4.0 de OData y JSON para la abstracción de datos. Esto proporciona las siguientes ventajas:</span><span class="sxs-lookup"><span data-stu-id="d9dc5-p101">Office 365 and Exchange Online provide a new way to work with email, calendars, and contacts. The Mail, Calendar, and Contact REST APIs provide a powerful, easy-to-use way to access and manipulate Exchange data. These APIs are based on open standards: OAuth version 2.0 for authentication, and OData version 4.0 and JSON for data abstraction. This provides the following advantages:</span></span>
  
- <span data-ttu-id="d9dc5-109">Como estas API requieren OAuth para la autenticación, no es necesario que la aplicación controle ni almacene las credenciales de usuario.</span><span class="sxs-lookup"><span data-stu-id="d9dc5-109">Because these APIs require OAuth for authentication, your application does not have to handle or store user credentials.</span></span>
    
- <span data-ttu-id="d9dc5-p102">OAuth permite solicitar permisos con ámbito estrecho para datos de usuario. Por ejemplo, puede diseñar la aplicación para que solicite permiso y lea únicamente el calendario de un usuario.</span><span class="sxs-lookup"><span data-stu-id="d9dc5-p102">OAuth makes it possible to request tightly scoped permissions to user data. For example, you might design your application to request permission and read only a user's calendar.</span></span>
    
## <a name="work-with-email-and-mail-folders"></a><span data-ttu-id="d9dc5-112">Trabajar con las carpetas de correo electrónico y correo</span><span class="sxs-lookup"><span data-stu-id="d9dc5-112">Work with email and mail folders</span></span>

<span data-ttu-id="d9dc5-p103">Puede usar la [API de correo](http://msdn.microsoft.com/office/office365/api/mail-rest-operations%28Office.15%29.aspx) para obtener, crear, actualizar, eliminar, mover, copiar y enviar correo electrónico. También puede obtener, crear, actualizar y eliminar carpetas de correo.</span><span class="sxs-lookup"><span data-stu-id="d9dc5-p103">You can use the [Mail API](http://msdn.microsoft.com/office/office365/api/mail-rest-operations%28Office.15%29.aspx) to get, create, update, delete, move, copy, and send email. You can also get, create, update, and delete mail folders.</span></span> 
  
## <a name="work-with-events-calendars-and-calendar-groups"></a><span data-ttu-id="d9dc5-115">Trabajar con grupos de calendario, calendarios y eventos</span><span class="sxs-lookup"><span data-stu-id="d9dc5-115">Work with events, calendars, and calendar groups</span></span>

<span data-ttu-id="d9dc5-p104">Puede usar la [API de calendario](http://msdn.microsoft.com/office/office365/api/calendar-rest-operations%28Office.15%29.aspx) para obtener, crear, actualizar y eliminar eventos. También puede obtener, crear, actualizar y eliminar calendarios y grupos de calendario.</span><span class="sxs-lookup"><span data-stu-id="d9dc5-p104">You can use the [Calendar API](http://msdn.microsoft.com/office/office365/api/calendar-rest-operations%28Office.15%29.aspx) to get, create, update, and delete events. You can also get, create, update, and delete calendar groups and calendars.</span></span> 
  
## <a name="work-with-contacts-and-contact-folders"></a><span data-ttu-id="d9dc5-118">Trabajar con contactos y carpetas de contactos</span><span class="sxs-lookup"><span data-stu-id="d9dc5-118">Work with contacts and contact folders</span></span>

<span data-ttu-id="d9dc5-p105">Puede usar la [API de contactos](http://msdn.microsoft.com/office/office365/api/contacts-rest-operations%28Office.15%29.aspx) para obtener, crear, actualizar y eliminar los contactos en el buzón de un usuario. También puede obtener carpetas de contactos.</span><span class="sxs-lookup"><span data-stu-id="d9dc5-p105">You can use the [Contacts API](http://msdn.microsoft.com/office/office365/api/contacts-rest-operations%28Office.15%29.aspx) to get, create, update, and delete contacts in a user's mailbox. You can also get contact folders.</span></span> 
  
## <a name="work-with-file-providers"></a><span data-ttu-id="d9dc5-121">Trabajar con proveedores de archivos</span><span class="sxs-lookup"><span data-stu-id="d9dc5-121">Work with file providers</span></span>

<span data-ttu-id="d9dc5-122">Puede usar la [API de REST de proveedores de archivos](http://msdn.microsoft.com/library/8bab5403-de68-4b49-ab19-9a6470f2a2ce%28Office.15%29.aspx) para obtener, crear, actualizar y eliminar información sobre proveedores de archivos compatibles, como buzones, Dropbox, etc.</span><span class="sxs-lookup"><span data-stu-id="d9dc5-122">You can use the [File Providers REST API](http://msdn.microsoft.com/library/8bab5403-de68-4b49-ab19-9a6470f2a2ce%28Office.15%29.aspx) to get, create, update, and delete information about supported file providers, such as mailbox, Dropbox, and so on.</span></span> 
  
## <a name="next-steps"></a><span data-ttu-id="d9dc5-123">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="d9dc5-123">Next steps</span></span>

<span data-ttu-id="d9dc5-p106">Entre en la página [Desarrollo en la plataforma Office 365](http://msdn.microsoft.com/office/office365/howto/platform-development-overview%28Office.15%29.aspx) para obtener más información sobre las API de correo, calendario y contactos y consultar las instrucciones para la configuración de su entorno y la introducción a las API. Asegúrese también de desproteger los [proyectos inicial y ejemplos de código](http://msdn.microsoft.com/office/office365/howto/Starter-projects-and-code-samples%28Office.15%29.aspx) para ver estas API en acción.</span><span class="sxs-lookup"><span data-stu-id="d9dc5-p106">Head over to the [Developing on the Office 365 platform](http://msdn.microsoft.com/office/office365/howto/platform-development-overview%28Office.15%29.aspx) page to get more information about the Mail, Calendar, and Contacts APIs, including guidance for setting up your environment and getting started with the APIs. Also be sure to check out the [starter projects and code samples](http://msdn.microsoft.com/office/office365/howto/Starter-projects-and-code-samples%28Office.15%29.aspx) to see these APIs in action.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d9dc5-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="d9dc5-126">See also</span></span>


- [<span data-ttu-id="d9dc5-127">Desarrollo en la plataforma Office 365</span><span class="sxs-lookup"><span data-stu-id="d9dc5-127">Developing on the Office 365 platform</span></span>](http://msdn.microsoft.com/office/office365/howto/platform-development-overview%28Office.15%29.aspx)
    
- [<span data-ttu-id="d9dc5-128">Creación de una aplicación ASP.NET MVC de Office 365</span><span class="sxs-lookup"><span data-stu-id="d9dc5-128">Building an Office 365 ASP.NET MVC app</span></span>](http://msdn.microsoft.com/office/office365/howto/Build-your-first-ASPNET-MVC-app%28Office.15%29.aspx)
    
- [<span data-ttu-id="d9dc5-129">Operaciones del REST de correo</span><span class="sxs-lookup"><span data-stu-id="d9dc5-129">Mail REST operations</span></span>](http://msdn.microsoft.com/office/office365/api/mail-rest-operations%28Office.15%29.aspx)
    
- [<span data-ttu-id="d9dc5-130">Operaciones del REST de calendario</span><span class="sxs-lookup"><span data-stu-id="d9dc5-130">Calendar REST operations</span></span>](http://msdn.microsoft.com/office/office365/api/calendar-rest-operations%28Office.15%29.aspx)
    
- [<span data-ttu-id="d9dc5-131">Operaciones del REST de contactos</span><span class="sxs-lookup"><span data-stu-id="d9dc5-131">Contacts REST operations</span></span>](http://msdn.microsoft.com/office/office365/api/contacts-rest-operations%28Office.15%29.aspx)
    
- [<span data-ttu-id="d9dc5-132">Proyectos iniciales de las API de Office 365 y ejemplos de código</span><span class="sxs-lookup"><span data-stu-id="d9dc5-132">Office 365 APIs starter projects and code samples</span></span>](http://msdn.microsoft.com/office/office365/howto/Starter-projects-and-code-samples%28Office.15%29.aspx)
    

