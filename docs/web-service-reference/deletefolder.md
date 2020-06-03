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
description: El elemento DeleteFolder define una solicitud para eliminar carpetas de un buzón de correo en el almacén de Exchange.
ms.openlocfilehash: eb705a47b78b19c79b2e87561ba3696ed40e09cd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458771"
---
# <a name="deletefolder"></a><span data-ttu-id="ee2c0-103">DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="ee2c0-103">DeleteFolder</span></span>

<span data-ttu-id="ee2c0-104">El elemento **DeleteFolder** define una solicitud para eliminar carpetas de un buzón de correo en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ee2c0-104">The **DeleteFolder** element defines a request to delete folders from a mailbox in the Exchange store.</span></span> 
  
```XML
<DeleteFolder DeleteType="">
   <FolderIds/>
</DeleteFolder>
```

 <span data-ttu-id="ee2c0-105">**DeleteFolderType**</span><span class="sxs-lookup"><span data-stu-id="ee2c0-105">**DeleteFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ee2c0-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ee2c0-106">Attributes and elements</span></span>

<span data-ttu-id="ee2c0-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ee2c0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ee2c0-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="ee2c0-108">Attributes</span></span>

|<span data-ttu-id="ee2c0-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="ee2c0-109">**Attribute**</span></span>|<span data-ttu-id="ee2c0-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ee2c0-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ee2c0-111">**DeleteType**</span><span class="sxs-lookup"><span data-stu-id="ee2c0-111">**DeleteType**</span></span> <br/> |<span data-ttu-id="ee2c0-112">Describe cómo se elimina una carpeta.</span><span class="sxs-lookup"><span data-stu-id="ee2c0-112">Describes how a folder is deleted.</span></span> <span data-ttu-id="ee2c0-113">Este atributo es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ee2c0-113">This attribute is required.</span></span>  <br/> |
   
#### <a name="deletetype-attribute"></a><span data-ttu-id="ee2c0-114">Atributo DeleteType</span><span class="sxs-lookup"><span data-stu-id="ee2c0-114">DeleteType attribute</span></span>

|<span data-ttu-id="ee2c0-115">**Valor**</span><span class="sxs-lookup"><span data-stu-id="ee2c0-115">**Value**</span></span>|<span data-ttu-id="ee2c0-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ee2c0-116">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ee2c0-117">HardDelete</span><span class="sxs-lookup"><span data-stu-id="ee2c0-117">HardDelete</span></span>  <br/> |<span data-ttu-id="ee2c0-118">Una carpeta se quita permanentemente de la tienda.</span><span class="sxs-lookup"><span data-stu-id="ee2c0-118">A folder is permanently removed from the store.</span></span>  <br/> |
|<span data-ttu-id="ee2c0-119">SoftDelete</span><span class="sxs-lookup"><span data-stu-id="ee2c0-119">SoftDelete</span></span>  <br/> |<span data-ttu-id="ee2c0-120">Si el contenedor está habilitado, se mueve una carpeta al contenedor.</span><span class="sxs-lookup"><span data-stu-id="ee2c0-120">A folder is moved to the dumpster if the dumpster is enabled.</span></span>  <br/> |
|<span data-ttu-id="ee2c0-121">MoveToDeletedItems</span><span class="sxs-lookup"><span data-stu-id="ee2c0-121">MoveToDeletedItems</span></span>  <br/> |<span data-ttu-id="ee2c0-122">Se mueve una carpeta a la carpeta elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="ee2c0-122">A folder is moved to the Deleted Items folder.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ee2c0-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ee2c0-123">Child elements</span></span>

|<span data-ttu-id="ee2c0-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ee2c0-124">**Element**</span></span>|<span data-ttu-id="ee2c0-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ee2c0-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ee2c0-126">FolderIds</span><span class="sxs-lookup"><span data-stu-id="ee2c0-126">FolderIds</span></span>](folderids.md) <br/> |<span data-ttu-id="ee2c0-127">Contiene una matriz de identificadores de carpeta que se usan para identificar las carpetas que se van a eliminar.</span><span class="sxs-lookup"><span data-stu-id="ee2c0-127">Contains an array of folder identifiers that are used to identify folders to delete.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ee2c0-128">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ee2c0-128">Parent elements</span></span>

<span data-ttu-id="ee2c0-129">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="ee2c0-129">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="ee2c0-130">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="ee2c0-130">Text value</span></span>

<span data-ttu-id="ee2c0-131">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ee2c0-131">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ee2c0-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ee2c0-132">Remarks</span></span>

<span data-ttu-id="ee2c0-133">Las opciones **MoveToDeletedItems** y **HardDelete** son transaccionales, lo que significa que cuando se completa una llamada de servicio Web, la base de datos movió el elemento a la carpeta elementos eliminados o quitó permanentemente el elemento de la base de datos de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ee2c0-133">The **MoveToDeletedItems** and **HardDelete** options are transactional, which means that by the time a Web service call completes, the database has moved the item to the Deleted Items folder or permanently removed the item from the Exchange database.</span></span> <span data-ttu-id="ee2c0-134">Este comportamiento es el mismo para MicrosoftExchange Server 2007 y Exchange Server 2010.</span><span class="sxs-lookup"><span data-stu-id="ee2c0-134">This behavior is the same for MicrosoftExchange Server 2007 and Exchange Server 2010.</span></span> 
  
<span data-ttu-id="ee2c0-135">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="ee2c0-135">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ee2c0-136">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ee2c0-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ee2c0-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="ee2c0-137">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ee2c0-138">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ee2c0-138">Schema Name</span></span>  <br/> |<span data-ttu-id="ee2c0-139">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="ee2c0-139">Message schema</span></span>  <br/> |
|<span data-ttu-id="ee2c0-140">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ee2c0-140">Validation File</span></span>  <br/> |<span data-ttu-id="ee2c0-141">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="ee2c0-141">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ee2c0-142">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ee2c0-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="ee2c0-143">Falso</span><span class="sxs-lookup"><span data-stu-id="ee2c0-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ee2c0-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="ee2c0-144">See also</span></span>

- [<span data-ttu-id="ee2c0-145">Operación DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="ee2c0-145">DeleteFolder operation</span></span>](deletefolder-operation.md)

