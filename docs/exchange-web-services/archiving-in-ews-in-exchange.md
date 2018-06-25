---
title: Archivado en EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 78ae179b-ae4f-4f64-911a-e0c70e0fa314
description: Obtenga información sobre el archivado en EWS en Exchange.
ms.openlocfilehash: bc282a7774bb74e57550bc663512987839324b83
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19762987"
---
# <a name="archiving-in-ews-in-exchange"></a><span data-ttu-id="165c6-103">Archivado en EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="165c6-103">Archiving in EWS in Exchange</span></span>

<span data-ttu-id="165c6-104">Obtenga información sobre el archivado en EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="165c6-104">Learn about archiving in EWS in Exchange.</span></span>
  
<span data-ttu-id="165c6-105">Buzones de archivo son buzones secundarios que están asociados con un usuario.</span><span class="sxs-lookup"><span data-stu-id="165c6-105">Archive mailboxes are secondary mailboxes that are associated with a user.</span></span> <span data-ttu-id="165c6-106">Buzones de archivo se suelen usar para administrar los límites de almacenamiento de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="165c6-106">Archive mailboxes are typically used to manage email storage limits.</span></span> <span data-ttu-id="165c6-107">Por ejemplo, los elementos de correo electrónico más antiguos es posible que periódicamente moverse desde la Bandeja de entrada para el buzón de archivo.</span><span class="sxs-lookup"><span data-stu-id="165c6-107">For example, older email items might periodically be moved from the Inbox to the archive mailbox.</span></span> 
  
<span data-ttu-id="165c6-108">Exchange Online, Exchange Online como parte de Office 365 y Exchange Server 2013 presentan dos nuevas operaciones de Exchange Web Services (EWS) que puede utilizar para archivar un conjunto de elementos de correo desde un buzón principal.</span><span class="sxs-lookup"><span data-stu-id="165c6-108">Exchange Online, Exchange Online as part of Office 365, and Exchange Server 2013 introduce two new Exchange Web Services (EWS) operations that you can use to archive a set of mail items from a primary mailbox.</span></span> <span data-ttu-id="165c6-109">Archivar los elementos de la Bandeja de entrada de este modo, conserva a la jerarquía de carpetas de los elementos.</span><span class="sxs-lookup"><span data-stu-id="165c6-109">Archiving Inbox items in this way preserves the folder hierarchy of the items.</span></span> <span data-ttu-id="165c6-110">Además, ahora se pueden almacenar buzones de archivo localmente en un cliente, o de forma remota, de una manera que sea opaca a un usuario, principalmente mediante el uso de una ruta de acceso de carpeta para que apunte al contenido del archivo.</span><span class="sxs-lookup"><span data-stu-id="165c6-110">In addition, archive mailboxes can now be stored either locally on a client, or remotely, in a way that is mostly opaque to a user, by using a folder path to point to the contents of the archive.</span></span>
  
## <a name="archiving-operations-in-ews"></a><span data-ttu-id="165c6-111">Las operaciones de EWS de archiving</span><span class="sxs-lookup"><span data-stu-id="165c6-111">Archiving operations in EWS</span></span>

<span data-ttu-id="165c6-112">En la siguiente tabla se enumera las operaciones de archivado que se introdujeron en Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="165c6-112">The following table lists the archiving operations that were introduced in Exchange 2013.</span></span> 
  
|<span data-ttu-id="165c6-113">**Nombre de la operación**</span><span class="sxs-lookup"><span data-stu-id="165c6-113">**Operation name**</span></span>|<span data-ttu-id="165c6-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="165c6-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="165c6-115">ArchiveItem</span><span class="sxs-lookup"><span data-stu-id="165c6-115">ArchiveItem</span></span>](http://msdn.microsoft.com/library/1af216b3-13ea-498e-b4fc-23513755d731%28Office.15%29.aspx) <br/> |<span data-ttu-id="165c6-116">Mueve un elemento desde el buzón principal para el buzón de archivo.</span><span class="sxs-lookup"><span data-stu-id="165c6-116">Moves an item from the primary mailbox to the archive mailbox.</span></span>  <br/> |
|[<span data-ttu-id="165c6-117">CreateFolderPath</span><span class="sxs-lookup"><span data-stu-id="165c6-117">CreateFolderPath</span></span>](http://msdn.microsoft.com/library/5a10aa5e-3f25-4ec3-a0b9-284c30918a1f%28Office.15%29.aspx) <br/> |<span data-ttu-id="165c6-118">Crea un identificador URI que señala a la ubicación de almacenamiento para el buzón de archivo.</span><span class="sxs-lookup"><span data-stu-id="165c6-118">Creates a URI that points to the storage location for the archive mailbox.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="165c6-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="165c6-119">See also</span></span>

- [<span data-ttu-id="165c6-120">Desarrollo de clientes de servicios web de Exchange</span><span class="sxs-lookup"><span data-stu-id="165c6-120">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)
    
- [<span data-ttu-id="165c6-121">Empezar a utilizar servicios web de Exchange</span><span class="sxs-lookup"><span data-stu-id="165c6-121">Start using web services in Exchange</span></span>](start-using-web-services-in-exchange.md)
    
- [<span data-ttu-id="165c6-122">Introducción al diseño de EWS cliente de Exchange</span><span class="sxs-lookup"><span data-stu-id="165c6-122">EWS client design overview for Exchange</span></span>](ews-client-design-overview-for-exchange.md)
    

