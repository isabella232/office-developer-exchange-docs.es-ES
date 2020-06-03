---
title: ArchiveTag
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c4cb0718-37cd-41aa-86e7-b492c4bb86aa
description: El elemento ArchiveTag especifica el identificador de retención de la etiqueta de archivo establecida en un elemento o carpeta.
ms.openlocfilehash: 23167f3c96a6756fe4c6d915a4de91e815e620d9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464766"
---
# <a name="archivetag"></a><span data-ttu-id="410e4-103">ArchiveTag</span><span class="sxs-lookup"><span data-stu-id="410e4-103">ArchiveTag</span></span>

<span data-ttu-id="410e4-104">El elemento **ArchiveTag** especifica el identificador de retención de la etiqueta de archivo establecida en un elemento o carpeta.</span><span class="sxs-lookup"><span data-stu-id="410e4-104">The **ArchiveTag** element specifies the retention identifier of the archive tag set on an item or folder.</span></span> 
  
```XML
<ArchiveTag IsExplicit=""></ArchiveTag>
```

 <span data-ttu-id="410e4-105">**RetentionTagType**</span><span class="sxs-lookup"><span data-stu-id="410e4-105">**RetentionTagType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="410e4-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="410e4-106">Attributes and elements</span></span>

<span data-ttu-id="410e4-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="410e4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="410e4-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="410e4-108">Attributes</span></span>

|<span data-ttu-id="410e4-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="410e4-109">**Attribute**</span></span>|<span data-ttu-id="410e4-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="410e4-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="410e4-111">**IsExplicit**</span><span class="sxs-lookup"><span data-stu-id="410e4-111">**IsExplicit**</span></span> <br/> |<span data-ttu-id="410e4-112">Especifica si la Directiva de retención se establece explícitamente en un elemento o una carpeta o si se hereda de una carpeta principal.</span><span class="sxs-lookup"><span data-stu-id="410e4-112">Specifies whether the retention policy is explicitly set on an item or folder or whether it is inherited from a parent folder.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="410e4-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="410e4-113">Child elements</span></span>

<span data-ttu-id="410e4-114">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="410e4-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="410e4-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="410e4-115">Parent elements</span></span>

|<span data-ttu-id="410e4-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="410e4-116">**Element**</span></span>|<span data-ttu-id="410e4-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="410e4-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="410e4-118">Hubiera</span><span class="sxs-lookup"><span data-stu-id="410e4-118">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="410e4-119">Representa una carpeta que contiene principalmente elementos de calendario.</span><span class="sxs-lookup"><span data-stu-id="410e4-119">Represents a folder that primarily contains calendar items.</span></span>  <br/> |
|[<span data-ttu-id="410e4-120">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="410e4-120">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="410e4-121">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="410e4-121">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="410e4-122">Contacto</span><span class="sxs-lookup"><span data-stu-id="410e4-122">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="410e4-123">Representa un elemento de contacto en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="410e4-123">Represents a contact item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="410e4-124">Hubiera</span><span class="sxs-lookup"><span data-stu-id="410e4-124">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="410e4-125">Representa una carpeta de contactos contenida en un buzón.</span><span class="sxs-lookup"><span data-stu-id="410e4-125">Represents a contacts folder that is contained in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="410e4-126">DistributionList</span><span class="sxs-lookup"><span data-stu-id="410e4-126">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="410e4-127">Representa una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="410e4-127">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="410e4-128">Folder</span><span class="sxs-lookup"><span data-stu-id="410e4-128">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="410e4-129">Define una carpeta para crear, obtener, buscar, sincronizar o actualizar.</span><span class="sxs-lookup"><span data-stu-id="410e4-129">Defines a folder to create, get, find, synchronize, or update.</span></span>  <br/> |
|[<span data-ttu-id="410e4-130">Elemento</span><span class="sxs-lookup"><span data-stu-id="410e4-130">Item</span></span>](item.md) <br/> |<span data-ttu-id="410e4-131">Representa un elemento genérico del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="410e4-131">Represents a generic item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="410e4-132">Message</span><span class="sxs-lookup"><span data-stu-id="410e4-132">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="410e4-133">Representa un mensaje de correo electrónico de Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="410e4-133">Represents a Microsoft Exchange email message.</span></span>  <br/> |
|[<span data-ttu-id="410e4-134">PostItem</span><span class="sxs-lookup"><span data-stu-id="410e4-134">PostItem</span></span>](postitem.md) <br/> |<span data-ttu-id="410e4-135">Representa un elemento post en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="410e4-135">Represents a post item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="410e4-136">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="410e4-136">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="410e4-137">Representa una carpeta de búsqueda contenida en un buzón.</span><span class="sxs-lookup"><span data-stu-id="410e4-137">Represents a search folder that is contained in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="410e4-138">Tarea</span><span class="sxs-lookup"><span data-stu-id="410e4-138">Task</span></span>](task.md) <br/> |<span data-ttu-id="410e4-139">Representa una tarea del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="410e4-139">Represents a task in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="410e4-140">Hubiera</span><span class="sxs-lookup"><span data-stu-id="410e4-140">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="410e4-141">Representa una carpeta de tareas contenida en un buzón.</span><span class="sxs-lookup"><span data-stu-id="410e4-141">Represents a tasks folder that is contained in a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="410e4-142">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="410e4-142">Text value</span></span>

<span data-ttu-id="410e4-143">El valor de texto del elemento **ArchiveTag** es un GUID que identifica la Directiva de retención.</span><span class="sxs-lookup"><span data-stu-id="410e4-143">The text value of the **ArchiveTag** element is a GUID that identifies the retention policy.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="410e4-144">Comentarios</span><span class="sxs-lookup"><span data-stu-id="410e4-144">Remarks</span></span>

<span data-ttu-id="410e4-145">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="410e4-145">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="410e4-146">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="410e4-146">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="410e4-147">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="410e4-147">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="410e4-148">Namespace</span><span class="sxs-lookup"><span data-stu-id="410e4-148">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="410e4-149">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="410e4-149">Schema Name</span></span>  <br/> |<span data-ttu-id="410e4-150">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="410e4-150">Type schema</span></span>  <br/> |
|<span data-ttu-id="410e4-151">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="410e4-151">Validation File</span></span>  <br/> |<span data-ttu-id="410e4-152">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="410e4-152">types.xsd</span></span>  <br/> |
|<span data-ttu-id="410e4-153">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="410e4-153">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="410e4-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="410e4-154">See also</span></span>

- [<span data-ttu-id="410e4-155">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="410e4-155">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

