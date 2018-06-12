---
title: DeleteFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteFolder
api_type:
- schema
ms.assetid: e37963f4-af9e-4481-b389-16175711e66d
description: El elemento DeleteFolder define una solicitud para eliminar las carpetas de un buzón en el almacén de Exchange.
ms.openlocfilehash: d31f98f26f537104e40b303de4199f45c65f49c7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764094"
---
# <a name="deletefolder"></a><span data-ttu-id="cf9de-103">DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="cf9de-103">DeleteFolder</span></span>

<span data-ttu-id="cf9de-104">El elemento **DeleteFolder** define una solicitud para eliminar las carpetas de un buzón en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="cf9de-104">The **DeleteFolder** element defines a request to delete folders from a mailbox in the Exchange store.</span></span> 
  
```XML
<DeleteFolder DeleteType="">
   <FolderIds/>
</DeleteFolder>
```

 <span data-ttu-id="cf9de-105">**DeleteFolderType**</span><span class="sxs-lookup"><span data-stu-id="cf9de-105">**DeleteFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cf9de-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="cf9de-106">Attributes and elements</span></span>

<span data-ttu-id="cf9de-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="cf9de-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cf9de-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="cf9de-108">Attributes</span></span>

|<span data-ttu-id="cf9de-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="cf9de-109">**Attribute**</span></span>|<span data-ttu-id="cf9de-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cf9de-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cf9de-111">**DeleteType**</span><span class="sxs-lookup"><span data-stu-id="cf9de-111">**DeleteType**</span></span> <br/> |<span data-ttu-id="cf9de-112">Describe cómo se elimina una carpeta.</span><span class="sxs-lookup"><span data-stu-id="cf9de-112">Describes how a folder is deleted.</span></span> <span data-ttu-id="cf9de-113">Este atributo es necesario.</span><span class="sxs-lookup"><span data-stu-id="cf9de-113">This attribute is required.</span></span>  <br/> |
   
#### <a name="deletetype-attribute"></a><span data-ttu-id="cf9de-114">Atributo DeleteType</span><span class="sxs-lookup"><span data-stu-id="cf9de-114">DeleteType attribute</span></span>

|<span data-ttu-id="cf9de-115">**Valor**</span><span class="sxs-lookup"><span data-stu-id="cf9de-115">**Value**</span></span>|<span data-ttu-id="cf9de-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cf9de-116">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cf9de-117">HardDelete</span><span class="sxs-lookup"><span data-stu-id="cf9de-117">HardDelete</span></span>  <br/> |<span data-ttu-id="cf9de-118">Permanentemente se quita una carpeta desde el almacén.</span><span class="sxs-lookup"><span data-stu-id="cf9de-118">A folder is permanently removed from the store.</span></span>  <br/> |
|<span data-ttu-id="cf9de-119">SoftDelete</span><span class="sxs-lookup"><span data-stu-id="cf9de-119">SoftDelete</span></span>  <br/> |<span data-ttu-id="cf9de-120">Se mueve una carpeta para el volcado de archivos si el volcado de archivos está habilitado.</span><span class="sxs-lookup"><span data-stu-id="cf9de-120">A folder is moved to the dumpster if the dumpster is enabled.</span></span>  <br/> |
|<span data-ttu-id="cf9de-121">MoveToDeletedItems</span><span class="sxs-lookup"><span data-stu-id="cf9de-121">MoveToDeletedItems</span></span>  <br/> |<span data-ttu-id="cf9de-122">Una carpeta se mueve a la carpeta Elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="cf9de-122">A folder is moved to the Deleted Items folder.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="cf9de-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="cf9de-123">Child elements</span></span>

|<span data-ttu-id="cf9de-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="cf9de-124">**Element**</span></span>|<span data-ttu-id="cf9de-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cf9de-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cf9de-126">FolderIds</span><span class="sxs-lookup"><span data-stu-id="cf9de-126">FolderIds</span></span>](folderids.md) <br/> |<span data-ttu-id="cf9de-127">Contiene una matriz de identificadores de carpeta que se usa para identificar las carpetas para eliminar.</span><span class="sxs-lookup"><span data-stu-id="cf9de-127">Contains an array of folder identifiers that are used to identify folders to delete.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="cf9de-128">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="cf9de-128">Parent elements</span></span>

<span data-ttu-id="cf9de-129">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="cf9de-129">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="cf9de-130">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="cf9de-130">Text value</span></span>

<span data-ttu-id="cf9de-131">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="cf9de-131">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cf9de-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cf9de-132">Remarks</span></span>

<span data-ttu-id="cf9de-133">Las opciones **MoveToDeletedItems** y **HardDelete** son transaccionales, lo que significa que el tiempo de una llamada al servicio Web completa, la base de datos ha movido el elemento a la carpeta Elementos eliminados o quita permanentemente el elemento de la base de datos de Exchange.</span><span class="sxs-lookup"><span data-stu-id="cf9de-133">The **MoveToDeletedItems** and **HardDelete** options are transactional, which means that by the time a Web service call completes, the database has moved the item to the Deleted Items folder or permanently removed the item from the Exchange database.</span></span> <span data-ttu-id="cf9de-134">Este comportamiento es el mismo para MicrosoftExchange Server 2007 y Exchange Server 2010.</span><span class="sxs-lookup"><span data-stu-id="cf9de-134">This behavior is the same for MicrosoftExchange Server 2007 and Exchange Server 2010.</span></span> 
  
<span data-ttu-id="cf9de-135">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="cf9de-135">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cf9de-136">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="cf9de-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cf9de-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="cf9de-137">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="cf9de-138">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="cf9de-138">Schema Name</span></span>  <br/> |<span data-ttu-id="cf9de-139">Esquema de mensaje</span><span class="sxs-lookup"><span data-stu-id="cf9de-139">Message schema</span></span>  <br/> |
|<span data-ttu-id="cf9de-140">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="cf9de-140">Validation File</span></span>  <br/> |<span data-ttu-id="cf9de-141">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="cf9de-141">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="cf9de-142">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="cf9de-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="cf9de-143">False</span><span class="sxs-lookup"><span data-stu-id="cf9de-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cf9de-144">Ver también</span><span class="sxs-lookup"><span data-stu-id="cf9de-144">See also</span></span>

- [<span data-ttu-id="cf9de-145">Operación DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="cf9de-145">DeleteFolder operation</span></span>](deletefolder-operation.md)

