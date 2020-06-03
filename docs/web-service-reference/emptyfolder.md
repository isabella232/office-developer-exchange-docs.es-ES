---
title: EmptyFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 502b2841-103d-4340-97d5-51a1db813fb2
description: El elemento EmptyFolder define una solicitud para vaciar una carpeta de un buzón de correo en el almacén de Exchange. Opcionalmente, también se pueden eliminar subcarpetas cuando se vacía la carpeta.
ms.openlocfilehash: a42e4e3f25741a96ee65fe6f87fc3236b68f4dc9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457280"
---
# <a name="emptyfolder"></a><span data-ttu-id="98ca0-104">EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="98ca0-104">EmptyFolder</span></span>

<span data-ttu-id="98ca0-105">El elemento **EmptyFolder** define una solicitud para vaciar una carpeta de un buzón de correo en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="98ca0-105">The **EmptyFolder** element defines a request to empty a folder in a mailbox in the Exchange store.</span></span> <span data-ttu-id="98ca0-106">Opcionalmente, también se pueden eliminar subcarpetas cuando se vacía la carpeta.</span><span class="sxs-lookup"><span data-stu-id="98ca0-106">Optionally, subfolders can also be deleted when the folder is emptied.</span></span> 
  
```XML
<EmptyFolder>
   <FolderIds/>
</EmptyFolder>
```

 <span data-ttu-id="98ca0-107">**EmptyFolderType**</span><span class="sxs-lookup"><span data-stu-id="98ca0-107">**EmptyFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="98ca0-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="98ca0-108">Attributes and elements</span></span>

<span data-ttu-id="98ca0-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="98ca0-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="98ca0-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="98ca0-110">Attributes</span></span>

|<span data-ttu-id="98ca0-111">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="98ca0-111">**Attribute**</span></span>|<span data-ttu-id="98ca0-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="98ca0-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="98ca0-113">**DeleteType**</span><span class="sxs-lookup"><span data-stu-id="98ca0-113">**DeleteType**</span></span> <br/> |<span data-ttu-id="98ca0-114">Especifica cómo se vacía una carpeta.</span><span class="sxs-lookup"><span data-stu-id="98ca0-114">Specifies how a folder is emptied.</span></span> <span data-ttu-id="98ca0-115">Este atributo es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="98ca0-115">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="98ca0-116">**DeleteSubFolders**</span><span class="sxs-lookup"><span data-stu-id="98ca0-116">**DeleteSubFolders**</span></span> <br/> |<span data-ttu-id="98ca0-117">Especifica si se van a eliminar las subcarpetas.</span><span class="sxs-lookup"><span data-stu-id="98ca0-117">Specifies whether subfolders are to be deleted.</span></span> <span data-ttu-id="98ca0-118">Este atributo es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="98ca0-118">This attribute is required.</span></span>  <br/> |
   
#### <a name="deletetype-attribute"></a><span data-ttu-id="98ca0-119">Atributo DeleteType</span><span class="sxs-lookup"><span data-stu-id="98ca0-119">DeleteType Attribute</span></span>

|<span data-ttu-id="98ca0-120">**Valor**</span><span class="sxs-lookup"><span data-stu-id="98ca0-120">**Value**</span></span>|<span data-ttu-id="98ca0-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="98ca0-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="98ca0-122">HardDelete</span><span class="sxs-lookup"><span data-stu-id="98ca0-122">HardDelete</span></span>  <br/> |<span data-ttu-id="98ca0-123">Los mensajes y las carpetas se eliminan permanentemente de la tienda.</span><span class="sxs-lookup"><span data-stu-id="98ca0-123">A messages and folders are permanently removed from the store.</span></span>  <br/> |
|<span data-ttu-id="98ca0-124">SoftDelete</span><span class="sxs-lookup"><span data-stu-id="98ca0-124">SoftDelete</span></span>  <br/> |<span data-ttu-id="98ca0-125">Si el contenedor está habilitado, los mensajes y las carpetas se mueven al contenedor.</span><span class="sxs-lookup"><span data-stu-id="98ca0-125">A messages and folders are moved to the dumpster if the dumpster is enabled.</span></span>  <br/> |
|<span data-ttu-id="98ca0-126">MoveToDeletedItems</span><span class="sxs-lookup"><span data-stu-id="98ca0-126">MoveToDeletedItems</span></span>  <br/> |<span data-ttu-id="98ca0-127">Los mensajes y las carpetas se mueven a la carpeta elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="98ca0-127">A messages and folders are moved to the Deleted Items folder.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="98ca0-128">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="98ca0-128">Child elements</span></span>

|<span data-ttu-id="98ca0-129">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="98ca0-129">**Element**</span></span>|<span data-ttu-id="98ca0-130">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="98ca0-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="98ca0-131">FolderIds</span><span class="sxs-lookup"><span data-stu-id="98ca0-131">FolderIds</span></span>](folderids.md) <br/> |<span data-ttu-id="98ca0-132">Contiene una matriz de identificadores de carpeta que se usan para identificar las carpetas que se van a eliminar.</span><span class="sxs-lookup"><span data-stu-id="98ca0-132">Contains an array of folder identifiers that are used to identify folders to delete.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="98ca0-133">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="98ca0-133">Parent elements</span></span>

<span data-ttu-id="98ca0-134">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="98ca0-134">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="98ca0-135">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="98ca0-135">Text value</span></span>

<span data-ttu-id="98ca0-136">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="98ca0-136">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="98ca0-137">Comentarios</span><span class="sxs-lookup"><span data-stu-id="98ca0-137">Remarks</span></span>

<span data-ttu-id="98ca0-138">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="98ca0-138">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="98ca0-139">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="98ca0-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="98ca0-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="98ca0-140">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="98ca0-141">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="98ca0-141">Schema Name</span></span>  <br/> |<span data-ttu-id="98ca0-142">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="98ca0-142">Message schema</span></span>  <br/> |
|<span data-ttu-id="98ca0-143">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="98ca0-143">Validation File</span></span>  <br/> |<span data-ttu-id="98ca0-144">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="98ca0-144">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="98ca0-145">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="98ca0-145">Can be Empty</span></span>  <br/> |<span data-ttu-id="98ca0-146">Falso</span><span class="sxs-lookup"><span data-stu-id="98ca0-146">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="98ca0-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="98ca0-147">See also</span></span>



[<span data-ttu-id="98ca0-148">Operación EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="98ca0-148">EmptyFolder operation</span></span>](emptyfolder-operation.md)

