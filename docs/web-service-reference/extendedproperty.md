---
title: Las extendedproperty
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
description: El elemento las extendedproperty identifica las propiedades de MAPI extendidas en carpetas y elementos.
ms.openlocfilehash: 99ede097d803d6fbf534cde0e77c08cec054bfa3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530610"
---
# <a name="extendedproperty"></a><span data-ttu-id="2e001-103">Las extendedproperty</span><span class="sxs-lookup"><span data-stu-id="2e001-103">ExtendedProperty</span></span>

<span data-ttu-id="2e001-104">El elemento **las extendedproperty** identifica las propiedades de MAPI extendidas en carpetas y elementos.</span><span class="sxs-lookup"><span data-stu-id="2e001-104">The **ExtendedProperty** element identifies extended MAPI properties on folders and items.</span></span> 
  
```xml
<ExtendedProperty>
   <ExtendedFieldURI/>
   <Values/>
</ExtendedProperty>
```

```xml
<ExtendedProperty>
   <ExtendedFieldURI/>
   <Value/>
</ExtendedProperty>
```

<span data-ttu-id="2e001-105">**ExtendedPropertyType**</span><span class="sxs-lookup"><span data-stu-id="2e001-105">**ExtendedPropertyType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="2e001-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="2e001-106">Attributes and elements</span></span>

<span data-ttu-id="2e001-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="2e001-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2e001-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="2e001-108">Attributes</span></span>

<span data-ttu-id="2e001-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="2e001-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2e001-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2e001-110">Child elements</span></span>

|<span data-ttu-id="2e001-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="2e001-111">**Element**</span></span>|<span data-ttu-id="2e001-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2e001-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2e001-113">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="2e001-113">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="2e001-114">Identifica una propiedad MAPI extendida para obtener, establecer o crear.</span><span class="sxs-lookup"><span data-stu-id="2e001-114">Identifies an extended MAPI property to get, set, or create.</span></span>  <br/> |
|[<span data-ttu-id="2e001-115">Valores</span><span class="sxs-lookup"><span data-stu-id="2e001-115">Values</span></span>](values.md) <br/> |<span data-ttu-id="2e001-116">Contiene una colección de valores para una propiedad MAPI extendida con varios valores.</span><span class="sxs-lookup"><span data-stu-id="2e001-116">Contains a collection of values for a multivalued extended MAPI property.</span></span>  <br/> |
|[<span data-ttu-id="2e001-117">Valor</span><span class="sxs-lookup"><span data-stu-id="2e001-117">Value</span></span>](value.md) <br/> |<span data-ttu-id="2e001-118">Contiene el valor de la propiedad extendida de MAPI de valor único.</span><span class="sxs-lookup"><span data-stu-id="2e001-118">Contains the value of single-valued MAPI extended property.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2e001-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="2e001-119">Parent elements</span></span>

|<span data-ttu-id="2e001-120">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="2e001-120">**Element**</span></span>|<span data-ttu-id="2e001-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2e001-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2e001-122">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="2e001-122">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="2e001-123">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="2e001-123">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="2e001-124">Contacto</span><span class="sxs-lookup"><span data-stu-id="2e001-124">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="2e001-125">Representa un elemento de contacto de Exchange.</span><span class="sxs-lookup"><span data-stu-id="2e001-125">Represents an Exchange contact item.</span></span>  <br/> |
|[<span data-ttu-id="2e001-126">DistributionList</span><span class="sxs-lookup"><span data-stu-id="2e001-126">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="2e001-127">Representa una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="2e001-127">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="2e001-128">Elemento</span><span class="sxs-lookup"><span data-stu-id="2e001-128">Item</span></span>](item.md) <br/> |<span data-ttu-id="2e001-129">Representa un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="2e001-129">Represents an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="2e001-130">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="2e001-130">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="2e001-131">Representa una cancelación de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="2e001-131">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="2e001-132">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="2e001-132">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="2e001-133">Representa una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="2e001-133">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="2e001-134">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="2e001-134">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="2e001-135">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="2e001-135">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="2e001-136">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="2e001-136">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="2e001-137">Representa una respuesta a una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="2e001-137">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="2e001-138">Message</span><span class="sxs-lookup"><span data-stu-id="2e001-138">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="2e001-139">Representa un mensaje de correo electrónico de Exchange.</span><span class="sxs-lookup"><span data-stu-id="2e001-139">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="2e001-140">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="2e001-140">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="2e001-141">Quita un elemento del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="2e001-141">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="2e001-142">Tarea</span><span class="sxs-lookup"><span data-stu-id="2e001-142">Task</span></span>](task.md) <br/> |<span data-ttu-id="2e001-143">Representa una tarea del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="2e001-143">Represents a task in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="2e001-144">Hubiera</span><span class="sxs-lookup"><span data-stu-id="2e001-144">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="2e001-145">Representa una carpeta que contiene principalmente elementos de calendario.</span><span class="sxs-lookup"><span data-stu-id="2e001-145">Represents a folder that primarily contains calendar items.</span></span>  <br/> |
|[<span data-ttu-id="2e001-146">Hubiera</span><span class="sxs-lookup"><span data-stu-id="2e001-146">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="2e001-147">Representa una carpeta de contactos en un buzón.</span><span class="sxs-lookup"><span data-stu-id="2e001-147">Represents a contacts folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="2e001-148">Folder</span><span class="sxs-lookup"><span data-stu-id="2e001-148">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="2e001-149">Representa una carpeta para crear, obtener, buscar, sincronizar o actualizar.</span><span class="sxs-lookup"><span data-stu-id="2e001-149">Represents a folder to create, get, find, synchronize, or update.</span></span>  <br/> |
|[<span data-ttu-id="2e001-150">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="2e001-150">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="2e001-151">Representa una carpeta de búsqueda contenida en un buzón.</span><span class="sxs-lookup"><span data-stu-id="2e001-151">Represents a search folder that is contained in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="2e001-152">Hubiera</span><span class="sxs-lookup"><span data-stu-id="2e001-152">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="2e001-153">Representa una carpeta de tareas contenida en un buzón.</span><span class="sxs-lookup"><span data-stu-id="2e001-153">Represents a tasks folder that is contained in a mailbox.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2e001-154">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2e001-154">Remarks</span></span>

<span data-ttu-id="2e001-155">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="2e001-155">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2e001-156">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="2e001-156">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2e001-157">Namespace</span><span class="sxs-lookup"><span data-stu-id="2e001-157">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2e001-158">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="2e001-158">Schema Name</span></span>  <br/> |<span data-ttu-id="2e001-159">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="2e001-159">Types schema</span></span>  <br/> |
|<span data-ttu-id="2e001-160">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="2e001-160">Validation File</span></span>  <br/> |<span data-ttu-id="2e001-161">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="2e001-161">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2e001-162">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="2e001-162">Can be Empty</span></span>  <br/> |<span data-ttu-id="2e001-163">Falso</span><span class="sxs-lookup"><span data-stu-id="2e001-163">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2e001-164">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e001-164">See also</span></span>

- [<span data-ttu-id="2e001-165">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="2e001-165">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

