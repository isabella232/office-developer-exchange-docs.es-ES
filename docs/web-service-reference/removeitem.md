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
ms.openlocfilehash: 6897363eba602e6a135ad255822197f9296dd44a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837108"
---
# <a name="removeitem"></a><span data-ttu-id="a3271-103">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="a3271-103">RemoveItem</span></span>

<span data-ttu-id="a3271-104">El elemento **RemoveItem** representa un objeto de respuesta que se usa para quitar un elemento de reunión cuando se recibe un mensaje MeetingCancellation.</span><span class="sxs-lookup"><span data-stu-id="a3271-104">The **RemoveItem** element represents a response object that is used to remove a meeting item when a MeetingCancellation message is received.</span></span> 
  
```xml
<RemoveItem ObjectName="">
   <ReferenceItemId/>
</RemoveItem>
```

 <span data-ttu-id="a3271-105">**RemoveItemType**</span><span class="sxs-lookup"><span data-stu-id="a3271-105">**RemoveItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a3271-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a3271-106">Attributes and elements</span></span>

<span data-ttu-id="a3271-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a3271-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a3271-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="a3271-108">Attributes</span></span>

|<span data-ttu-id="a3271-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="a3271-109">**Attribute**</span></span>|<span data-ttu-id="a3271-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a3271-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a3271-111">**ObjectName**</span><span class="sxs-lookup"><span data-stu-id="a3271-111">**ObjectName**</span></span> <br/> |<span data-ttu-id="a3271-112">Representa el nombre de la clase de objeto de respuesta RemoveItem como una cadena en inglés.</span><span class="sxs-lookup"><span data-stu-id="a3271-112">Represents the name of the RemoveItem reply object class as an English string.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a3271-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a3271-113">Child elements</span></span>

|<span data-ttu-id="a3271-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="a3271-114">**Element**</span></span>|<span data-ttu-id="a3271-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a3271-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a3271-116">ReferenceItemId</span><span class="sxs-lookup"><span data-stu-id="a3271-116">ReferenceItemId</span></span>](referenceitemid.md) <br/> |<span data-ttu-id="a3271-117">Identifica el elemento al que hace referencia el objeto de respuesta de RemoveItem.</span><span class="sxs-lookup"><span data-stu-id="a3271-117">Identifies the item to which the RemoveItem response object refers.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a3271-118">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a3271-118">Parent elements</span></span>

|<span data-ttu-id="a3271-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="a3271-119">**Element**</span></span>|<span data-ttu-id="a3271-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a3271-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a3271-121">Elementos (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="a3271-121">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="a3271-122">Contiene una matriz de elementos que desea crear en la carpeta que se identifica con el elemento [ID (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) .</span><span class="sxs-lookup"><span data-stu-id="a3271-122">Contains an array of items to create in the folder that is identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
|[<span data-ttu-id="a3271-123">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="a3271-123">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="a3271-124">Contiene una colección de todos los objetos de respuesta que están asociados con un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="a3271-124">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a3271-125">Notas</span><span class="sxs-lookup"><span data-stu-id="a3271-125">Remarks</span></span>

 <span data-ttu-id="a3271-126">**RemoveItem** sólo es válido para un [MeetingCancellation](meetingcancellation.md).</span><span class="sxs-lookup"><span data-stu-id="a3271-126">**RemoveItem** is valid only for a [MeetingCancellation](meetingcancellation.md).</span></span> <span data-ttu-id="a3271-127">De lo contrario, se produce un error.</span><span class="sxs-lookup"><span data-stu-id="a3271-127">Otherwise, an error is thrown.</span></span>
  
> [!NOTE]
> <span data-ttu-id="a3271-128">El [ItemClass](itemclass.md) de cancelación de la reunión es IPM. Schedule.Meeting.Canceled.</span><span class="sxs-lookup"><span data-stu-id="a3271-128">The [ItemClass](itemclass.md) for a meeting cancellation is IPM.Schedule.Meeting.Canceled.</span></span> 
  
<span data-ttu-id="a3271-129">Para quitar un [MeetingRequest](meetingrequest.md) y el asociado [CalendarItem](calendaritem.md), utilice el objeto de respuesta [DeclineItem](declineitem.md) en lugar de **RemoveItem**.</span><span class="sxs-lookup"><span data-stu-id="a3271-129">To remove a [MeetingRequest](meetingrequest.md) and the associated [CalendarItem](calendaritem.md), use the [DeclineItem](declineitem.md) response object instead of **RemoveItem**.</span></span>
  
 <span data-ttu-id="a3271-130">**RemoveItem** no se admite para el acceso de delegado.</span><span class="sxs-lookup"><span data-stu-id="a3271-130">**RemoveItem** is not supported for delegate access.</span></span> 
  
<span data-ttu-id="a3271-131">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="a3271-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a3271-132">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a3271-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a3271-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a3271-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a3271-134">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a3271-134">Schema Name</span></span>  <br/> |<span data-ttu-id="a3271-135">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="a3271-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="a3271-136">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a3271-136">Validation File</span></span>  <br/> |<span data-ttu-id="a3271-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a3271-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a3271-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a3271-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="a3271-139">False</span><span class="sxs-lookup"><span data-stu-id="a3271-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a3271-140">Ver también</span><span class="sxs-lookup"><span data-stu-id="a3271-140">See also</span></span>



- [<span data-ttu-id="a3271-141">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="a3271-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

