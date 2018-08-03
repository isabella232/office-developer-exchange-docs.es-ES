---
title: API de Outlook de Microsoft Graph para correo, calendarios y contactos
manager: sethgros
ms.date: 07/27/2018
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3b2e71a6-5fa5-4008-b243-d3a6e9173b3d
description: Busque información sobre la API de Microsoft Graph que puede usar para tener acceso al correo, calendarios y contactos en Office 365 o Exchange Online.
ms.openlocfilehash: 3065de389157345afd5ed07e302ace99e2048bdf
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353297"
---
# <a name="microsoft-graph-rest-apis-for-mail-calendars-and-contacts"></a><span data-ttu-id="83fff-103">API de REST de Microsoft Graph para correo, calendarios y contactos</span><span class="sxs-lookup"><span data-stu-id="83fff-103">Office 365 REST APIs for mail, calendars, and contacts</span></span>

<span data-ttu-id="83fff-104">Busque información sobre las API de Microsoft Graph que puede usar para tener acceso al correo, calendarios y contactos en Office 365 o Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="83fff-104">Find information about the Office 365 APIs that you can use to access mail, calendars, and contacts in Office 365 or Exchange Online.</span></span>

<span data-ttu-id="83fff-105">Office 365 y Exchange Online ofrecen una nueva forma de trabajar con correo electrónico, calendarios y contactos.</span><span class="sxs-lookup"><span data-stu-id="83fff-105">Office 365 and Exchange Online provide a new way to work with email, calendars, and contacts.</span></span> <span data-ttu-id="83fff-106">Las API de REST de Microsoft Graph de correo, calendario y contactos ofrecen una forma eficaz y sencilla de obtener acceso a los datos de Exchange y manipularlos.</span><span class="sxs-lookup"><span data-stu-id="83fff-106">The Mail, Calendar, and Contact REST APIs provide a powerful, easy-to-use way to access and manipulate Exchange data.</span></span> <span data-ttu-id="83fff-107">Estas API se basan en estándares abiertos: OAuth versión 2.0 para la autenticación y la versión 4.0 de OData y JSON para la abstracción de datos.</span><span class="sxs-lookup"><span data-stu-id="83fff-107">These APIs are based on open standards: OAuth version 2.0 for authentication, and OData version 4.0 and JSON for data abstraction.</span></span> <span data-ttu-id="83fff-108">Esto proporciona las siguientes ventajas:</span><span class="sxs-lookup"><span data-stu-id="83fff-108">This provides the following advantages:</span></span>

- <span data-ttu-id="83fff-109">Como estas API requieren OAuth para la autenticación, no es necesario que la aplicación controle ni almacene las credenciales de usuario.</span><span class="sxs-lookup"><span data-stu-id="83fff-109">Because these APIs require OAuth for authentication, your application does not have to handle or store user credentials.</span></span>

- <span data-ttu-id="83fff-p102">OAuth permite solicitar permisos con ámbito estrecho para datos de usuario. Por ejemplo, puede diseñar la aplicación para que solicite permiso y lea únicamente el calendario de un usuario.</span><span class="sxs-lookup"><span data-stu-id="83fff-p102">OAuth makes it possible to request tightly scoped permissions to user data. For example, you might design your application to request permission and read only a user's calendar.</span></span>

## <a name="work-with-email-and-mail-folders"></a><span data-ttu-id="83fff-112">Trabajar con las carpetas de correo electrónico y correo</span><span class="sxs-lookup"><span data-stu-id="83fff-112">Work with email and mail folders</span></span>

<span data-ttu-id="83fff-p103">Puede usar la [API de correo](https://developer.microsoft.com/graph/docs/concepts/outlook-mail-concept-overview) para obtener, crear, actualizar, eliminar, mover, copiar y enviar correo electrónico. También puede obtener, crear, actualizar y eliminar carpetas de correo.</span><span class="sxs-lookup"><span data-stu-id="83fff-p103">You can use the [Mail API](https://developer.microsoft.com/graph/docs/concepts/outlook-mail-concept-overview) to get, create, update, delete, move, copy, and send email. You can also get, create, update, and delete mail folders.</span></span> 
  
## <a name="work-with-events-calendars-and-calendar-groups"></a><span data-ttu-id="83fff-115">Trabajar con grupos de calendario, calendarios y eventos</span><span class="sxs-lookup"><span data-stu-id="83fff-115">Work with events, calendars, and calendar groups</span></span>

<span data-ttu-id="83fff-p104">Puede usar la [API de calendario](https://developer.microsoft.com/graph/docs/concepts/outlook-calendar-concept-overview) para obtener, crear, actualizar y eliminar eventos. También puede obtener, crear, actualizar y eliminar calendarios y grupos de calendario.</span><span class="sxs-lookup"><span data-stu-id="83fff-p104">You can use the [Calendar API](https://developer.microsoft.com/graph/docs/concepts/outlook-calendar-concept-overview) to get, create, update, and delete events. You can also get, create, update, and delete calendar groups and calendars.</span></span> 
  
## <a name="work-with-contacts-and-contact-folders"></a><span data-ttu-id="83fff-118">Trabajar con contactos y carpetas de contactos</span><span class="sxs-lookup"><span data-stu-id="83fff-118">Work with contacts and contact folders</span></span>

<span data-ttu-id="83fff-p105">Puede usar la [API de contactos](https://developer.microsoft.com/graph/docs/concepts/outlook-contacts-concept-overview) para obtener, crear, actualizar y eliminar los contactos en el buzón de un usuario. También puede obtener carpetas de contactos.</span><span class="sxs-lookup"><span data-stu-id="83fff-p105">You can use the [Contacts API](https://developer.microsoft.com/graph/docs/concepts/outlook-contacts-concept-overview) to get, create, update, and delete contacts in a user's mailbox. You can also get contact folders.</span></span> 
  
## <a name="next-steps"></a><span data-ttu-id="83fff-121">Siguientes pasos</span><span class="sxs-lookup"><span data-stu-id="83fff-121">Next steps</span></span>

<span data-ttu-id="83fff-122">Entre en la página [Documentación de Microsoft Graph](https://developer.microsoft.com/graph/docs/concepts/overview) para obtener más información sobre las API de correo, calendario y contactos y consultar las instrucciones para la configuración de su entorno y la introducción a las API.</span><span class="sxs-lookup"><span data-stu-id="83fff-122">Head over to the [Developing on the Office 365 platform](https://developer.microsoft.com/graph/docs/concepts/overview) page to get more information about the Mail, Calendar, and Contacts APIs, including guidance for setting up your environment and getting started with the APIs.</span></span> 

<span data-ttu-id="83fff-123">Consulte también los [inicios rápidos](https://developer.microsoft.com/graph/quick-start) y los [ejemplos de códigos](https://developer.microsoft.com/office/gallery/?filterBy=Samples,Microsoft%20Graph) para ver esas API en funcionamiento.</span><span class="sxs-lookup"><span data-stu-id="83fff-123">Also be sure to check out the starter projects and code samples to see these APIs in action.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="83fff-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="83fff-124">See also</span></span>

- [<span data-ttu-id="83fff-125">Documentación de Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="83fff-125">Microsoft Graph documentation</span></span>](https://developer.microsoft.com/graph/docs/concepts/overview)   

