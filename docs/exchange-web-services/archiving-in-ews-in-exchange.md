---
title: Archivado en EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 78ae179b-ae4f-4f64-911a-e0c70e0fa314
description: Obtenga información sobre el archivado en EWS en Exchange.
ms.openlocfilehash: b433b9f88905ee255720e8b341d560fa0e464975
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456216"
---
# <a name="archiving-in-ews-in-exchange"></a><span data-ttu-id="1be65-103">Archivado en EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="1be65-103">Archiving in EWS in Exchange</span></span>

<span data-ttu-id="1be65-104">Obtenga información sobre el archivado en EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="1be65-104">Learn about archiving in EWS in Exchange.</span></span>
  
<span data-ttu-id="1be65-105">Los buzones de archivo son buzones secundarios que están asociados a un usuario.</span><span class="sxs-lookup"><span data-stu-id="1be65-105">Archive mailboxes are secondary mailboxes that are associated with a user.</span></span> <span data-ttu-id="1be65-106">Los buzones de archivo se usan normalmente para administrar los límites de almacenamiento de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="1be65-106">Archive mailboxes are typically used to manage email storage limits.</span></span> <span data-ttu-id="1be65-107">Por ejemplo, es posible que los elementos de correo electrónico antiguos se muevan periódicamente de la bandeja de entrada al buzón de archivo.</span><span class="sxs-lookup"><span data-stu-id="1be65-107">For example, older email items might periodically be moved from the Inbox to the archive mailbox.</span></span> 
  
<span data-ttu-id="1be65-108">Exchange Online, Exchange online como parte de Office 365 y Exchange Server 2013 introducen dos nuevas operaciones de servicios web Exchange (EWS) que puede usar para archivar un conjunto de elementos de correo desde un buzón principal.</span><span class="sxs-lookup"><span data-stu-id="1be65-108">Exchange Online, Exchange Online as part of Office 365, and Exchange Server 2013 introduce two new Exchange Web Services (EWS) operations that you can use to archive a set of mail items from a primary mailbox.</span></span> <span data-ttu-id="1be65-109">Archivar elementos de la bandeja de entrada de esta manera conserva la jerarquía de carpetas de los elementos.</span><span class="sxs-lookup"><span data-stu-id="1be65-109">Archiving Inbox items in this way preserves the folder hierarchy of the items.</span></span> <span data-ttu-id="1be65-110">Además, los buzones de archivo ahora se pueden almacenar de forma local en un cliente, o de forma remota, de forma que sea prácticamente opaca para un usuario, mediante una ruta de acceso de carpeta que apunte al contenido del archivo.</span><span class="sxs-lookup"><span data-stu-id="1be65-110">In addition, archive mailboxes can now be stored either locally on a client, or remotely, in a way that is mostly opaque to a user, by using a folder path to point to the contents of the archive.</span></span>
  
## <a name="archiving-operations-in-ews"></a><span data-ttu-id="1be65-111">Operaciones de archivado en EWS</span><span class="sxs-lookup"><span data-stu-id="1be65-111">Archiving operations in EWS</span></span>

<span data-ttu-id="1be65-112">En la siguiente tabla se enumeran las operaciones de archivado que se introdujeron en Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="1be65-112">The following table lists the archiving operations that were introduced in Exchange 2013.</span></span> 
  
|<span data-ttu-id="1be65-113">**Nombre de operación**</span><span class="sxs-lookup"><span data-stu-id="1be65-113">**Operation name**</span></span>|<span data-ttu-id="1be65-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1be65-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1be65-115">ArchiveItem</span><span class="sxs-lookup"><span data-stu-id="1be65-115">ArchiveItem</span></span>](https://msdn.microsoft.com/library/1af216b3-13ea-498e-b4fc-23513755d731%28Office.15%29.aspx) <br/> |<span data-ttu-id="1be65-116">Mueve un elemento del buzón de correo principal al buzón de archivo.</span><span class="sxs-lookup"><span data-stu-id="1be65-116">Moves an item from the primary mailbox to the archive mailbox.</span></span>  <br/> |
|[<span data-ttu-id="1be65-117">CreateFolderPath</span><span class="sxs-lookup"><span data-stu-id="1be65-117">CreateFolderPath</span></span>](https://msdn.microsoft.com/library/5a10aa5e-3f25-4ec3-a0b9-284c30918a1f%28Office.15%29.aspx) <br/> |<span data-ttu-id="1be65-118">Crea un URI que apunta a la ubicación de almacenamiento del buzón de archivo.</span><span class="sxs-lookup"><span data-stu-id="1be65-118">Creates a URI that points to the storage location for the archive mailbox.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1be65-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="1be65-119">See also</span></span>

- [<span data-ttu-id="1be65-120">Desarrollar clientes de servicios web de Exchange</span><span class="sxs-lookup"><span data-stu-id="1be65-120">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)
    
- [<span data-ttu-id="1be65-121">Empezar a usar los servicios web de Exchange</span><span class="sxs-lookup"><span data-stu-id="1be65-121">Start using web services in Exchange</span></span>](start-using-web-services-in-exchange.md)
    
- [<span data-ttu-id="1be65-122">Introducción al diseño de EWS cliente de Exchange</span><span class="sxs-lookup"><span data-stu-id="1be65-122">EWS client design overview for Exchange</span></span>](ews-client-design-overview-for-exchange.md)
    

