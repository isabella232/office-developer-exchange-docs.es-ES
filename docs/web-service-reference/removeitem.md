---
title: RemoveItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RemoveItem
api_type:
- schema
ms.assetid: 766878e3-9007-454f-8501-45139bc5c0e2
description: El elemento RemoveItem representa un objeto de respuesta que se usa para quitar un elemento de reunión cuando se recibe un mensaje MeetingCancellation.
ms.openlocfilehash: c0cd5c1f9894287ee78c2f7a65b8f4d3b943414e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467693"
---
# <a name="removeitem"></a><span data-ttu-id="105f9-103">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="105f9-103">RemoveItem</span></span>

<span data-ttu-id="105f9-104">El elemento **RemoveItem** representa un objeto de respuesta que se usa para quitar un elemento de reunión cuando se recibe un mensaje MeetingCancellation.</span><span class="sxs-lookup"><span data-stu-id="105f9-104">The **RemoveItem** element represents a response object that is used to remove a meeting item when a MeetingCancellation message is received.</span></span> 
  
```xml
<RemoveItem ObjectName="">
   <ReferenceItemId/>
</RemoveItem>
```

 <span data-ttu-id="105f9-105">**RemoveItemType**</span><span class="sxs-lookup"><span data-stu-id="105f9-105">**RemoveItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="105f9-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="105f9-106">Attributes and elements</span></span>

<span data-ttu-id="105f9-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="105f9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="105f9-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="105f9-108">Attributes</span></span>

|<span data-ttu-id="105f9-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="105f9-109">**Attribute**</span></span>|<span data-ttu-id="105f9-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="105f9-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="105f9-111">**ObjectName**</span><span class="sxs-lookup"><span data-stu-id="105f9-111">**ObjectName**</span></span> <br/> |<span data-ttu-id="105f9-112">Representa el nombre de la clase de objeto de respuesta de RemoveItem como una cadena en inglés.</span><span class="sxs-lookup"><span data-stu-id="105f9-112">Represents the name of the RemoveItem reply object class as an English string.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="105f9-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="105f9-113">Child elements</span></span>

|<span data-ttu-id="105f9-114">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="105f9-114">**Element**</span></span>|<span data-ttu-id="105f9-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="105f9-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="105f9-116">ReferenceItemId</span><span class="sxs-lookup"><span data-stu-id="105f9-116">ReferenceItemId</span></span>](referenceitemid.md) <br/> |<span data-ttu-id="105f9-117">Identifica el elemento al que hace referencia el objeto de respuesta RemoveItem.</span><span class="sxs-lookup"><span data-stu-id="105f9-117">Identifies the item to which the RemoveItem response object refers.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="105f9-118">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="105f9-118">Parent elements</span></span>

|<span data-ttu-id="105f9-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="105f9-119">**Element**</span></span>|<span data-ttu-id="105f9-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="105f9-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="105f9-121">Elementos (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="105f9-121">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="105f9-122">Contiene una matriz de elementos que se van a crear en la carpeta identificada por el elemento [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) .</span><span class="sxs-lookup"><span data-stu-id="105f9-122">Contains an array of items to create in the folder that is identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
|[<span data-ttu-id="105f9-123">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="105f9-123">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="105f9-124">Contiene una colección de todos los objetos de respuesta que están asociados a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="105f9-124">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="105f9-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="105f9-125">Remarks</span></span>

 <span data-ttu-id="105f9-126">**RemoveItem** solo es válido para [MeetingCancellation](meetingcancellation.md).</span><span class="sxs-lookup"><span data-stu-id="105f9-126">**RemoveItem** is valid only for a [MeetingCancellation](meetingcancellation.md).</span></span> <span data-ttu-id="105f9-127">De lo contrario, se produce un error.</span><span class="sxs-lookup"><span data-stu-id="105f9-127">Otherwise, an error is thrown.</span></span>
  
> [!NOTE]
> <span data-ttu-id="105f9-128">El [ItemClass](itemclass.md) de una cancelación de reunión es IPM. Program. Meeting. Canceled.</span><span class="sxs-lookup"><span data-stu-id="105f9-128">The [ItemClass](itemclass.md) for a meeting cancellation is IPM.Schedule.Meeting.Canceled.</span></span> 
  
<span data-ttu-id="105f9-129">Para quitar la propiedad [MeetingRequest](meetingrequest.md) y la [CalendarItem](calendaritem.md)asociada, use el objeto de respuesta [DeclineItem](declineitem.md) en lugar de **RemoveItem**.</span><span class="sxs-lookup"><span data-stu-id="105f9-129">To remove a [MeetingRequest](meetingrequest.md) and the associated [CalendarItem](calendaritem.md), use the [DeclineItem](declineitem.md) response object instead of **RemoveItem**.</span></span>
  
 <span data-ttu-id="105f9-130">No se admite **RemoveItem** para el acceso de delegado.</span><span class="sxs-lookup"><span data-stu-id="105f9-130">**RemoveItem** is not supported for delegate access.</span></span> 
  
<span data-ttu-id="105f9-131">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="105f9-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="105f9-132">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="105f9-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="105f9-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="105f9-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="105f9-134">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="105f9-134">Schema Name</span></span>  <br/> |<span data-ttu-id="105f9-135">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="105f9-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="105f9-136">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="105f9-136">Validation File</span></span>  <br/> |<span data-ttu-id="105f9-137">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="105f9-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="105f9-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="105f9-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="105f9-139">Falso</span><span class="sxs-lookup"><span data-stu-id="105f9-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="105f9-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="105f9-140">See also</span></span>



- [<span data-ttu-id="105f9-141">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="105f9-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

