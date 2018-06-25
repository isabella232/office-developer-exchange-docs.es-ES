---
title: SuppressReadReceipt
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SuppressReadReceipt
api_type:
- schema
ms.assetid: fc09bcc2-c003-4322-8315-d929bd0a9e2e
description: El elemento SuppressReadReceipt se usa para suprimir confirmaciones de lectura.
ms.openlocfilehash: de2eef68abd25c8208530ba5e98ab3278c8702d1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840604"
---
# <a name="suppressreadreceipt"></a><span data-ttu-id="a5e28-103">SuppressReadReceipt</span><span class="sxs-lookup"><span data-stu-id="a5e28-103">SuppressReadReceipt</span></span>

<span data-ttu-id="a5e28-104">El elemento **SuppressReadReceipt** se usa para suprimir confirmaciones de lectura.</span><span class="sxs-lookup"><span data-stu-id="a5e28-104">The **SuppressReadReceipt** element is used to suppress read receipts.</span></span> 
  
```xml
<SuppressReadReceipt>
   <ReferenceItemId/>
</SuppressReadReceipt>
```

 <span data-ttu-id="a5e28-105">**SuppressReadReceiptType**</span><span class="sxs-lookup"><span data-stu-id="a5e28-105">**SuppressReadReceiptType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a5e28-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a5e28-106">Attributes and elements</span></span>

<span data-ttu-id="a5e28-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a5e28-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a5e28-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="a5e28-108">Attributes</span></span>

<span data-ttu-id="a5e28-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a5e28-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a5e28-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a5e28-110">Child elements</span></span>

|<span data-ttu-id="a5e28-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="a5e28-111">**Element**</span></span>|<span data-ttu-id="a5e28-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a5e28-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a5e28-113">ReferenceItemId</span><span class="sxs-lookup"><span data-stu-id="a5e28-113">ReferenceItemId</span></span>](referenceitemid.md) <br/> |<span data-ttu-id="a5e28-114">Identifica el elemento al que hace referencia el objeto de respuesta.</span><span class="sxs-lookup"><span data-stu-id="a5e28-114">Identifies the item to which the response object refers.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a5e28-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a5e28-115">Parent elements</span></span>

|<span data-ttu-id="a5e28-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="a5e28-116">**Element**</span></span>|<span data-ttu-id="a5e28-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a5e28-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a5e28-118">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="a5e28-118">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> | <span data-ttu-id="a5e28-119">Describe todos los elementos que están adyacentes a una hora de reunión.</span><span class="sxs-lookup"><span data-stu-id="a5e28-119">Describes all items that are adjacent to a meeting time.</span></span>  <br/><br/>  <span data-ttu-id="a5e28-120">Las siguientes son algunas de las expresiones de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="a5e28-120">The following are some of the XPath expressions to this element:</span></span><br/>  <br/>  `/CalendarItem/AdjacentMeetings` <br/>  `/MeetingRequest/AdjacentMeetings` <br/>  `/SetItemField/CalendarItem/AdjacentMeetings` <br/>  `/AppendToItemField/CalendarItem/AdjacentMeetings` <br/>  `/AcceptItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/DeclineItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/TentativelyAcceptItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/SetItemField/CalendarItem/AdjacentMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/AppendToItemField/CalendarItem/AdjacentMeetings` <br/>  `/CreateAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/GetAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/> |
|[<span data-ttu-id="a5e28-121">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="a5e28-121">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> | <span data-ttu-id="a5e28-122">Describe todos los elementos que entran en conflicto con un tiempo de la reunión.</span><span class="sxs-lookup"><span data-stu-id="a5e28-122">Describes all items that conflict with a meeting time.</span></span> <br/> <br/>  <span data-ttu-id="a5e28-123">Las siguientes son algunas de las expresiones de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="a5e28-123">The following are some of the XPath expressions to this element:</span></span> <br/> <br/>  `/CalendarItem/ConflictingMeetings` <br/>  `/MeetingRequest/ConflictingMeetings` <br/>  `/SetItemField/CalendarItem/ConflictingMeetings` <br/>  `/AppendToItemField/CalendarItem/ConflictingMeetings` <br/>  `/AcceptItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/DeclineItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/TentativelyAcceptItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/SetItemField/CalendarItem/ConflictingMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/AppendToItemField/CalendarItem/ConflictingMeetings` <br/>  `/CreateAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/GetAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/> |
|[<span data-ttu-id="a5e28-124">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="a5e28-124">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="a5e28-125">Contiene una colección de todos los objetos de respuesta que están asociados con un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="a5e28-125">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="a5e28-126">Elementos (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="a5e28-126">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="a5e28-127">Contiene una matriz de elementos que desea crear en la carpeta que se identifica con el elemento [ID (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) .</span><span class="sxs-lookup"><span data-stu-id="a5e28-127">Contains an array of items to create in the folder that is identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a5e28-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a5e28-128">Remarks</span></span>

<span data-ttu-id="a5e28-129">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="a5e28-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a5e28-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a5e28-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a5e28-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a5e28-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a5e28-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a5e28-132">Schema Name</span></span>  <br/> |<span data-ttu-id="a5e28-133">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="a5e28-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="a5e28-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a5e28-134">Validation File</span></span>  <br/> |<span data-ttu-id="a5e28-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a5e28-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a5e28-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a5e28-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="a5e28-137">False</span><span class="sxs-lookup"><span data-stu-id="a5e28-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a5e28-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="a5e28-138">See also</span></span>

- [<span data-ttu-id="a5e28-139">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="a5e28-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

