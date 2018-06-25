---
title: ExtendedProperty
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ExtendedProperty
api_type:
- schema
ms.assetid: f9701409-b620-4afe-b9ee-4c1e95507af7
description: El elemento ExtendedProperty identifica las propiedades MAPI extendidas en carpetas y elementos.
ms.openlocfilehash: 6a0aecc732ef634c2258127fca89b19461e25762
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764525"
---
# <a name="extendedproperty"></a><span data-ttu-id="d5b09-103">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="d5b09-103">ExtendedProperty</span></span>

<span data-ttu-id="d5b09-104">El elemento **ExtendedProperty** identifica las propiedades MAPI extendidas en carpetas y elementos.</span><span class="sxs-lookup"><span data-stu-id="d5b09-104">The **ExtendedProperty** element identifies extended MAPI properties on folders and items.</span></span> 
  
```xml
<ExtendedProperty>
   <ExtendedFieldURI/>
   <Values/>
</ExtendedProperty>
```

 <span data-ttu-id="d5b09-105">**ExtendedPropertyType**</span><span class="sxs-lookup"><span data-stu-id="d5b09-105">**ExtendedPropertyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d5b09-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d5b09-106">Attributes and elements</span></span>

<span data-ttu-id="d5b09-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d5b09-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d5b09-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="d5b09-108">Attributes</span></span>

<span data-ttu-id="d5b09-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d5b09-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d5b09-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d5b09-110">Child elements</span></span>

|<span data-ttu-id="d5b09-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="d5b09-111">**Element**</span></span>|<span data-ttu-id="d5b09-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d5b09-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d5b09-113">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="d5b09-113">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="d5b09-114">Identifica una propiedad MAPI extendida para obtener, establecer o crear.</span><span class="sxs-lookup"><span data-stu-id="d5b09-114">Identifies an extended MAPI property to get, set, or create.</span></span>  <br/> |
|[<span data-ttu-id="d5b09-115">Values</span><span class="sxs-lookup"><span data-stu-id="d5b09-115">Values</span></span>](values.md) <br/> |<span data-ttu-id="d5b09-116">Contiene una colección de valores para una propiedad multivalor de MAPI extendida.</span><span class="sxs-lookup"><span data-stu-id="d5b09-116">Contains a collection of values for a multivalued extended MAPI property.</span></span>  <br/> |
|[<span data-ttu-id="d5b09-117">Valor</span><span class="sxs-lookup"><span data-stu-id="d5b09-117">Value</span></span>](value.md) <br/> |<span data-ttu-id="d5b09-118">Contiene el valor de la propiedad extendida de MAPI un solo valor.</span><span class="sxs-lookup"><span data-stu-id="d5b09-118">Contains the value of single-valued MAPI extended property.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d5b09-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d5b09-119">Parent elements</span></span>

|<span data-ttu-id="d5b09-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="d5b09-120">**Element**</span></span>|<span data-ttu-id="d5b09-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d5b09-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d5b09-122">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="d5b09-122">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="d5b09-123">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d5b09-123">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="d5b09-124">Contact</span><span class="sxs-lookup"><span data-stu-id="d5b09-124">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="d5b09-125">Representa un elemento de contacto de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d5b09-125">Represents an Exchange contact item.</span></span>  <br/> |
|[<span data-ttu-id="d5b09-126">DistributionList</span><span class="sxs-lookup"><span data-stu-id="d5b09-126">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="d5b09-127">Representa una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="d5b09-127">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="d5b09-128">Item</span><span class="sxs-lookup"><span data-stu-id="d5b09-128">Item</span></span>](item.md) <br/> |<span data-ttu-id="d5b09-129">Representa un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d5b09-129">Represents an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="d5b09-130">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="d5b09-130">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="d5b09-131">Representa la cancelación de la reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d5b09-131">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="d5b09-132">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="d5b09-132">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="d5b09-133">Representa una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d5b09-133">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="d5b09-134">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="d5b09-134">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="d5b09-135">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d5b09-135">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="d5b09-136">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="d5b09-136">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="d5b09-137">Representa una respuesta a la reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d5b09-137">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="d5b09-138">Message</span><span class="sxs-lookup"><span data-stu-id="d5b09-138">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="d5b09-139">Representa un mensaje de correo electrónico de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d5b09-139">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="d5b09-140">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="d5b09-140">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="d5b09-141">Quita un elemento desde el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d5b09-141">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="d5b09-142">Tarea</span><span class="sxs-lookup"><span data-stu-id="d5b09-142">Task</span></span>](task.md) <br/> |<span data-ttu-id="d5b09-143">Representa una tarea en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d5b09-143">Represents a task in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="d5b09-144">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="d5b09-144">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="d5b09-145">Representa una carpeta que principalmente contiene los elementos del calendario.</span><span class="sxs-lookup"><span data-stu-id="d5b09-145">Represents a folder that primarily contains calendar items.</span></span>  <br/> |
|[<span data-ttu-id="d5b09-146">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="d5b09-146">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="d5b09-147">Representa una carpeta de contactos en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="d5b09-147">Represents a contacts folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="d5b09-148">Folder</span><span class="sxs-lookup"><span data-stu-id="d5b09-148">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="d5b09-149">Representa una carpeta para crear, obtener, buscar, sincronizar o actualizar.</span><span class="sxs-lookup"><span data-stu-id="d5b09-149">Represents a folder to create, get, find, synchronize, or update.</span></span>  <br/> |
|[<span data-ttu-id="d5b09-150">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="d5b09-150">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="d5b09-151">Representa una carpeta de búsqueda que se encuentra en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="d5b09-151">Represents a search folder that is contained in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="d5b09-152">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="d5b09-152">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="d5b09-153">Representa una carpeta de tareas que se encuentra en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="d5b09-153">Represents a tasks folder that is contained in a mailbox.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d5b09-154">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d5b09-154">Remarks</span></span>

<span data-ttu-id="d5b09-155">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="d5b09-155">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d5b09-156">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d5b09-156">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d5b09-157">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d5b09-157">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d5b09-158">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d5b09-158">Schema Name</span></span>  <br/> |<span data-ttu-id="d5b09-159">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="d5b09-159">Types schema</span></span>  <br/> |
|<span data-ttu-id="d5b09-160">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d5b09-160">Validation File</span></span>  <br/> |<span data-ttu-id="d5b09-161">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d5b09-161">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d5b09-162">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d5b09-162">Can be Empty</span></span>  <br/> |<span data-ttu-id="d5b09-163">False</span><span class="sxs-lookup"><span data-stu-id="d5b09-163">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d5b09-164">Vea también</span><span class="sxs-lookup"><span data-stu-id="d5b09-164">See also</span></span>



- [<span data-ttu-id="d5b09-165">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="d5b09-165">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

