---
title: ArchiveTag
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c4cb0718-37cd-41aa-86e7-b492c4bb86aa
description: El elemento ArchiveTag especifica el identificador de la retención de la etiqueta de archivo establecer en una carpeta o elemento.
ms.openlocfilehash: ae9c7d512981af3bf564bcb73a9a27c5c78217fc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763551"
---
# <a name="archivetag"></a><span data-ttu-id="0ad92-103">ArchiveTag</span><span class="sxs-lookup"><span data-stu-id="0ad92-103">ArchiveTag</span></span>

<span data-ttu-id="0ad92-104">El elemento **ArchiveTag** especifica el identificador de la retención de la etiqueta de archivo establecer en una carpeta o elemento.</span><span class="sxs-lookup"><span data-stu-id="0ad92-104">The **ArchiveTag** element specifies the retention identifier of the archive tag set on an item or folder.</span></span> 
  
```XML
<ArchiveTag IsExplicit=""></ArchiveTag>
```

 <span data-ttu-id="0ad92-105">**RetentionTagType**</span><span class="sxs-lookup"><span data-stu-id="0ad92-105">**RetentionTagType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0ad92-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="0ad92-106">Attributes and elements</span></span>

<span data-ttu-id="0ad92-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="0ad92-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0ad92-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="0ad92-108">Attributes</span></span>

|<span data-ttu-id="0ad92-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="0ad92-109">**Attribute**</span></span>|<span data-ttu-id="0ad92-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0ad92-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0ad92-111">**IsExplicit**</span><span class="sxs-lookup"><span data-stu-id="0ad92-111">**IsExplicit**</span></span> <br/> |<span data-ttu-id="0ad92-112">Especifica si la directiva de retención se establezca explícitamente en una carpeta o un elemento o si se hereda de una carpeta principal.</span><span class="sxs-lookup"><span data-stu-id="0ad92-112">Specifies whether the retention policy is explicitly set on an item or folder or whether it is inherited from a parent folder.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0ad92-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0ad92-113">Child elements</span></span>

<span data-ttu-id="0ad92-114">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0ad92-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0ad92-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0ad92-115">Parent elements</span></span>

|<span data-ttu-id="0ad92-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="0ad92-116">**Element**</span></span>|<span data-ttu-id="0ad92-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0ad92-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0ad92-118">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="0ad92-118">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="0ad92-119">Representa una carpeta que principalmente contiene los elementos del calendario.</span><span class="sxs-lookup"><span data-stu-id="0ad92-119">Represents a folder that primarily contains calendar items.</span></span>  <br/> |
|[<span data-ttu-id="0ad92-120">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="0ad92-120">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="0ad92-121">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="0ad92-121">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="0ad92-122">Contact</span><span class="sxs-lookup"><span data-stu-id="0ad92-122">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="0ad92-123">Representa un elemento de contacto en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="0ad92-123">Represents a contact item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="0ad92-124">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="0ad92-124">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="0ad92-125">Representa una carpeta de contactos que se encuentra en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="0ad92-125">Represents a contacts folder that is contained in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="0ad92-126">DistributionList</span><span class="sxs-lookup"><span data-stu-id="0ad92-126">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="0ad92-127">Representa una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="0ad92-127">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="0ad92-128">Folder</span><span class="sxs-lookup"><span data-stu-id="0ad92-128">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="0ad92-129">Define una carpeta para crear, obtener, buscar, sincronizar o actualizar.</span><span class="sxs-lookup"><span data-stu-id="0ad92-129">Defines a folder to create, get, find, synchronize, or update.</span></span>  <br/> |
|[<span data-ttu-id="0ad92-130">Item</span><span class="sxs-lookup"><span data-stu-id="0ad92-130">Item</span></span>](item.md) <br/> |<span data-ttu-id="0ad92-131">Representa un elemento genérico en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="0ad92-131">Represents a generic item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="0ad92-132">Message</span><span class="sxs-lookup"><span data-stu-id="0ad92-132">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="0ad92-133">Representa un mensaje de correo electrónico de Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="0ad92-133">Represents a Microsoft Exchange email message.</span></span>  <br/> |
|[<span data-ttu-id="0ad92-134">Objeto postItem</span><span class="sxs-lookup"><span data-stu-id="0ad92-134">PostItem</span></span>](postitem.md) <br/> |<span data-ttu-id="0ad92-135">Representa un elemento para exponer en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="0ad92-135">Represents a post item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="0ad92-136">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="0ad92-136">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="0ad92-137">Representa una carpeta de búsqueda que se encuentra en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="0ad92-137">Represents a search folder that is contained in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="0ad92-138">Tarea</span><span class="sxs-lookup"><span data-stu-id="0ad92-138">Task</span></span>](task.md) <br/> |<span data-ttu-id="0ad92-139">Representa una tarea en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="0ad92-139">Represents a task in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="0ad92-140">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="0ad92-140">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="0ad92-141">Representa una carpeta de tareas que se encuentra en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="0ad92-141">Represents a tasks folder that is contained in a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0ad92-142">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="0ad92-142">Text value</span></span>

<span data-ttu-id="0ad92-143">El valor de texto del elemento **ArchiveTag** es un GUID que identifica la directiva de retención.</span><span class="sxs-lookup"><span data-stu-id="0ad92-143">The text value of the **ArchiveTag** element is a GUID that identifies the retention policy.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="0ad92-144">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0ad92-144">Remarks</span></span>

<span data-ttu-id="0ad92-145">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0ad92-145">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="0ad92-146">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="0ad92-146">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0ad92-147">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0ad92-147">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0ad92-148">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0ad92-148">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0ad92-149">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="0ad92-149">Schema Name</span></span>  <br/> |<span data-ttu-id="0ad92-150">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="0ad92-150">Type schema</span></span>  <br/> |
|<span data-ttu-id="0ad92-151">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="0ad92-151">Validation File</span></span>  <br/> |<span data-ttu-id="0ad92-152">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0ad92-152">types.xsd</span></span>  <br/> |
|<span data-ttu-id="0ad92-153">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="0ad92-153">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="0ad92-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="0ad92-154">See also</span></span>

- [<span data-ttu-id="0ad92-155">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="0ad92-155">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

