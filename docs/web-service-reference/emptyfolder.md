---
title: EmptyFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 502b2841-103d-4340-97d5-51a1db813fb2
description: El elemento EmptyFolder define una solicitud para vaciar una carpeta en un buzón en el almacén de Exchange. De forma opcional, también se pueden eliminar las subcarpetas cuando se vacía la carpeta.
ms.openlocfilehash: c72e11cea29e2e55c9c29754eec60e73bd1e4d9c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764385"
---
# <a name="emptyfolder"></a><span data-ttu-id="4f400-104">EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="4f400-104">EmptyFolder</span></span>

<span data-ttu-id="4f400-105">El elemento **EmptyFolder** define una solicitud para vaciar una carpeta en un buzón en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="4f400-105">The **EmptyFolder** element defines a request to empty a folder in a mailbox in the Exchange store.</span></span> <span data-ttu-id="4f400-106">De forma opcional, también se pueden eliminar las subcarpetas cuando se vacía la carpeta.</span><span class="sxs-lookup"><span data-stu-id="4f400-106">Optionally, subfolders can also be deleted when the folder is emptied.</span></span> 
  
```XML
<EmptyFolder>
   <FolderIds/>
</EmptyFolder>
```

 <span data-ttu-id="4f400-107">**EmptyFolderType**</span><span class="sxs-lookup"><span data-stu-id="4f400-107">**EmptyFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4f400-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="4f400-108">Attributes and elements</span></span>

<span data-ttu-id="4f400-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="4f400-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4f400-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="4f400-110">Attributes</span></span>

|<span data-ttu-id="4f400-111">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="4f400-111">**Attribute**</span></span>|<span data-ttu-id="4f400-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4f400-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4f400-113">**DeleteType**</span><span class="sxs-lookup"><span data-stu-id="4f400-113">**DeleteType**</span></span> <br/> |<span data-ttu-id="4f400-114">Especifica cómo se vacía una carpeta.</span><span class="sxs-lookup"><span data-stu-id="4f400-114">Specifies how a folder is emptied.</span></span> <span data-ttu-id="4f400-115">Este atributo es necesario.</span><span class="sxs-lookup"><span data-stu-id="4f400-115">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="4f400-116">**DeleteSubFolders**</span><span class="sxs-lookup"><span data-stu-id="4f400-116">**DeleteSubFolders**</span></span> <br/> |<span data-ttu-id="4f400-117">Especifica si las subcarpetas se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="4f400-117">Specifies whether subfolders are to be deleted.</span></span> <span data-ttu-id="4f400-118">Este atributo es necesario.</span><span class="sxs-lookup"><span data-stu-id="4f400-118">This attribute is required.</span></span>  <br/> |
   
#### <a name="deletetype-attribute"></a><span data-ttu-id="4f400-119">Atributo DeleteType</span><span class="sxs-lookup"><span data-stu-id="4f400-119">DeleteType Attribute</span></span>

|<span data-ttu-id="4f400-120">**Valor**</span><span class="sxs-lookup"><span data-stu-id="4f400-120">**Value**</span></span>|<span data-ttu-id="4f400-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4f400-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4f400-122">HardDelete</span><span class="sxs-lookup"><span data-stu-id="4f400-122">HardDelete</span></span>  <br/> |<span data-ttu-id="4f400-123">A los mensajes y carpetas se quitan definitivamente desde el almacén.</span><span class="sxs-lookup"><span data-stu-id="4f400-123">A messages and folders are permanently removed from the store.</span></span>  <br/> |
|<span data-ttu-id="4f400-124">SoftDelete</span><span class="sxs-lookup"><span data-stu-id="4f400-124">SoftDelete</span></span>  <br/> |<span data-ttu-id="4f400-125">A los mensajes y carpetas se mueven al volcado de archivos si el volcado de archivos está habilitado.</span><span class="sxs-lookup"><span data-stu-id="4f400-125">A messages and folders are moved to the dumpster if the dumpster is enabled.</span></span>  <br/> |
|<span data-ttu-id="4f400-126">MoveToDeletedItems</span><span class="sxs-lookup"><span data-stu-id="4f400-126">MoveToDeletedItems</span></span>  <br/> |<span data-ttu-id="4f400-127">A los mensajes y carpetas se mueven a la carpeta Elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="4f400-127">A messages and folders are moved to the Deleted Items folder.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4f400-128">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4f400-128">Child elements</span></span>

|<span data-ttu-id="4f400-129">**Element**</span><span class="sxs-lookup"><span data-stu-id="4f400-129">**Element**</span></span>|<span data-ttu-id="4f400-130">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4f400-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4f400-131">FolderIds</span><span class="sxs-lookup"><span data-stu-id="4f400-131">FolderIds</span></span>](folderids.md) <br/> |<span data-ttu-id="4f400-132">Contiene una matriz de identificadores de carpeta que se usa para identificar las carpetas para eliminar.</span><span class="sxs-lookup"><span data-stu-id="4f400-132">Contains an array of folder identifiers that are used to identify folders to delete.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4f400-133">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="4f400-133">Parent elements</span></span>

<span data-ttu-id="4f400-134">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4f400-134">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="4f400-135">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="4f400-135">Text value</span></span>

<span data-ttu-id="4f400-136">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4f400-136">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4f400-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4f400-137">Remarks</span></span>

<span data-ttu-id="4f400-138">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="4f400-138">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4f400-139">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="4f400-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4f400-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4f400-140">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="4f400-141">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="4f400-141">Schema Name</span></span>  <br/> |<span data-ttu-id="4f400-142">Esquema de mensaje</span><span class="sxs-lookup"><span data-stu-id="4f400-142">Message schema</span></span>  <br/> |
|<span data-ttu-id="4f400-143">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="4f400-143">Validation File</span></span>  <br/> |<span data-ttu-id="4f400-144">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="4f400-144">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4f400-145">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="4f400-145">Can be Empty</span></span>  <br/> |<span data-ttu-id="4f400-146">False</span><span class="sxs-lookup"><span data-stu-id="4f400-146">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4f400-147">Ver también</span><span class="sxs-lookup"><span data-stu-id="4f400-147">See also</span></span>



[<span data-ttu-id="4f400-148">Operación EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="4f400-148">EmptyFolder operation</span></span>](emptyfolder-operation.md)

