---
title: BaseShape
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- BaseShape
api_type:
- schema
ms.assetid: 42c04f3b-abaa-4197-a3d6-d21677ffb1c0
description: El elemento BaseShape identifica el conjunto de propiedades que se devolverá en una respuesta de elemento o carpeta.
ms.openlocfilehash: 9b3f00ff94fbfe6ad6373b16ad95eb9136f81c64
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44464493"
---
# <a name="baseshape"></a><span data-ttu-id="359bf-103">BaseShape</span><span class="sxs-lookup"><span data-stu-id="359bf-103">BaseShape</span></span>

<span data-ttu-id="359bf-104">El elemento **BaseShape** identifica el conjunto de propiedades que se devolverá en una respuesta de elemento o carpeta.</span><span class="sxs-lookup"><span data-stu-id="359bf-104">The **BaseShape** element identifies the set of properties to return in an item or folder response.</span></span> 
  
```xml
<BaseShape>IdOnly or Default or AllProperties</BaseShape>
```

 <span data-ttu-id="359bf-105">**DefaultShapeNamesType**</span><span class="sxs-lookup"><span data-stu-id="359bf-105">**DefaultShapeNamesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="359bf-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="359bf-106">Attributes and elements</span></span>

<span data-ttu-id="359bf-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="359bf-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="359bf-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="359bf-108">Attributes</span></span>

<span data-ttu-id="359bf-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="359bf-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="359bf-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="359bf-110">Child elements</span></span>

<span data-ttu-id="359bf-111">Ninguno</span><span class="sxs-lookup"><span data-stu-id="359bf-111">None</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="359bf-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="359bf-112">Parent elements</span></span>

|<span data-ttu-id="359bf-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="359bf-113">**Element**</span></span>|<span data-ttu-id="359bf-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="359bf-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="359bf-115">FolderShape</span><span class="sxs-lookup"><span data-stu-id="359bf-115">FolderShape</span></span>](foldershape.md) <br/> | <span data-ttu-id="359bf-116">Identifica las propiedades de carpeta que se incluirán en la respuesta GetFolder, FindFolder o SyncFolderHierarchy.</span><span class="sxs-lookup"><span data-stu-id="359bf-116">Identifies the folder properties to include in the GetFolder, FindFolder, or SyncFolderHierarchy response.</span></span><br/><br/><span data-ttu-id="359bf-117">Las siguientes son las expresiones XPath de este elemento:</span><span class="sxs-lookup"><span data-stu-id="359bf-117">The following are the XPath expressions to this element:</span></span><br/><br/>`/GetFolder/FolderShape` <br/>  `/FindFolder/FolderShape` <br/>  `/SyncFolderHierarchy/FolderShape` <br/> |
|[<span data-ttu-id="359bf-118">ItemShape</span><span class="sxs-lookup"><span data-stu-id="359bf-118">ItemShape</span></span>](itemshape.md) <br/> | <span data-ttu-id="359bf-119">Identifica el contenido y las propiedades de los elementos que se van a incluir en una respuesta GetItem, FindItem o SyncFolderItems.</span><span class="sxs-lookup"><span data-stu-id="359bf-119">Identifies the item properties and content to include in a GetItem, FindItem, or SyncFolderItems response.</span></span><br/><br/><span data-ttu-id="359bf-120">Las siguientes son las expresiones XPath de este elemento:</span><span class="sxs-lookup"><span data-stu-id="359bf-120">The following are the XPath expressions to this element:</span></span><br/><br/>`/GetItem/ItemShape` <br/>  `/FindItem/ItemShape` <br/>  `/SyncFolderItems/ItemShape` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="359bf-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="359bf-121">Text value</span></span>

<span data-ttu-id="359bf-122">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="359bf-122">A text value is required.</span></span> <span data-ttu-id="359bf-123">En la siguiente tabla se enumeran los valores de texto posibles.</span><span class="sxs-lookup"><span data-stu-id="359bf-123">The following table lists the possible text values.</span></span>
  
<span data-ttu-id="359bf-124">**Valores de texto para el elemento BaseShape**</span><span class="sxs-lookup"><span data-stu-id="359bf-124">**Text values for the BaseShape element**</span></span>

|<span data-ttu-id="359bf-125">**Valor**</span><span class="sxs-lookup"><span data-stu-id="359bf-125">**Value**</span></span>|<span data-ttu-id="359bf-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="359bf-126">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="359bf-127">IdOnly</span><span class="sxs-lookup"><span data-stu-id="359bf-127">IdOnly</span></span>  <br/> |<span data-ttu-id="359bf-128">Devuelve solo el identificador de elemento o carpeta.</span><span class="sxs-lookup"><span data-stu-id="359bf-128">Returns only the item or folder ID.</span></span>  <br/> |
|<span data-ttu-id="359bf-129">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="359bf-129">Default</span></span>  <br/> |<span data-ttu-id="359bf-130">Devuelve un conjunto de propiedades que se definen como valores predeterminados para el elemento o carpeta.</span><span class="sxs-lookup"><span data-stu-id="359bf-130">Returns a set of properties that are defined as the default for the item or folder.</span></span>  <br/> |
|<span data-ttu-id="359bf-131">AllProperties</span><span class="sxs-lookup"><span data-stu-id="359bf-131">AllProperties</span></span>  <br/> |<span data-ttu-id="359bf-132">Devuelve todas las propiedades usadas por la capa de lógica empresarial de Exchange para crear una carpeta.</span><span class="sxs-lookup"><span data-stu-id="359bf-132">Returns all the properties used by the Exchange Business Logic layer to construct a folder.</span></span>  <br/> |
   
<span data-ttu-id="359bf-133">En la siguiente tabla se enumeran las propiedades predeterminadas que se devuelven para una solicitud FindFolder.</span><span class="sxs-lookup"><span data-stu-id="359bf-133">The following table lists the default properties that are returned for a FindFolder request.</span></span> <span data-ttu-id="359bf-134">Todas las subcarpetas de una carpeta determinada se devuelven en orden por nombre.</span><span class="sxs-lookup"><span data-stu-id="359bf-134">All subfolders of a given folder are returned in order by name.</span></span>
  
<span data-ttu-id="359bf-135">**Propiedades predeterminadas**</span><span class="sxs-lookup"><span data-stu-id="359bf-135">**Default properties**</span></span>

|<span data-ttu-id="359bf-136">**Folder**</span><span class="sxs-lookup"><span data-stu-id="359bf-136">**Folder**</span></span>|<span data-ttu-id="359bf-137">**Propiedades predeterminadas**</span><span class="sxs-lookup"><span data-stu-id="359bf-137">**Default Properties**</span></span>|
|:-----|:-----|
|<span data-ttu-id="359bf-138">Bandeja de entrada</span><span class="sxs-lookup"><span data-stu-id="359bf-138">Inbox</span></span>  <br/> |<span data-ttu-id="359bf-139">FolderId, nombre para mostrar, número de no leídos, recuento total, número de subcarpetas</span><span class="sxs-lookup"><span data-stu-id="359bf-139">FolderId, display name, unread count, total count, subfolder count</span></span>  <br/> |
|<span data-ttu-id="359bf-140">Contactos</span><span class="sxs-lookup"><span data-stu-id="359bf-140">Contacts</span></span>  <br/> |<span data-ttu-id="359bf-141">FolderId, nombre para mostrar, recuento total, número de subcarpetas</span><span class="sxs-lookup"><span data-stu-id="359bf-141">FolderId, display name, total count, subfolder count</span></span>  <br/> |
|<span data-ttu-id="359bf-142">Calendar</span><span class="sxs-lookup"><span data-stu-id="359bf-142">Calendar</span></span>  <br/> |<span data-ttu-id="359bf-143">FolderId, nombre para mostrar, número de subcarpetas</span><span class="sxs-lookup"><span data-stu-id="359bf-143">FolderId, display name, subfolder count</span></span>  <br/> |
|<span data-ttu-id="359bf-144">Borradores</span><span class="sxs-lookup"><span data-stu-id="359bf-144">Drafts</span></span>  <br/> |<span data-ttu-id="359bf-145">FolderId, nombre para mostrar, número de no leídos, recuento total, número de subcarpetas</span><span class="sxs-lookup"><span data-stu-id="359bf-145">FolderId, display name, unread count, total count, subfolder count</span></span>  <br/> |
|<span data-ttu-id="359bf-146">Elementos eliminados</span><span class="sxs-lookup"><span data-stu-id="359bf-146">Deleted items</span></span>  <br/> |<span data-ttu-id="359bf-147">FolderId, nombre para mostrar, número de no leídos, recuento total, número de subcarpetas</span><span class="sxs-lookup"><span data-stu-id="359bf-147">FolderId, display name, unread count, total count, subfolder count</span></span>  <br/> |
|<span data-ttu-id="359bf-148">Otras carpetas</span><span class="sxs-lookup"><span data-stu-id="359bf-148">Other folders</span></span>  <br/> |<span data-ttu-id="359bf-149">FolderId, nombre para mostrar, número de no leídos, recuento total, número de subcarpetas</span><span class="sxs-lookup"><span data-stu-id="359bf-149">FolderId, display name, unread count, total count, subfolder count</span></span>  <br/> |
|<span data-ttu-id="359bf-150">Bandeja de salida</span><span class="sxs-lookup"><span data-stu-id="359bf-150">Outbox</span></span>  <br/> |<span data-ttu-id="359bf-151">FolderId, nombre para mostrar, número de no leídos, recuento total, número de subcarpetas</span><span class="sxs-lookup"><span data-stu-id="359bf-151">FolderId, display name, unread count, total count, subfolder count</span></span>  <br/> |
|<span data-ttu-id="359bf-152">Tareas</span><span class="sxs-lookup"><span data-stu-id="359bf-152">Tasks</span></span>  <br/> |<span data-ttu-id="359bf-153">FolderId, nombre para mostrar, recuento de vencidas, recuento total, número de subcarpetas</span><span class="sxs-lookup"><span data-stu-id="359bf-153">FolderId, display name, past due count, total count, subfolder count</span></span>  <br/> |
|<span data-ttu-id="359bf-154">Notas</span><span class="sxs-lookup"><span data-stu-id="359bf-154">Notes</span></span>  <br/> |<span data-ttu-id="359bf-155">FolderId, nombre para mostrar, recuento total, número de subcarpetas</span><span class="sxs-lookup"><span data-stu-id="359bf-155">FolderId, display name, total count, subfolder count</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="359bf-156">Comentarios</span><span class="sxs-lookup"><span data-stu-id="359bf-156">Remarks</span></span>

<span data-ttu-id="359bf-157">Para devolver propiedades además de las identificadas por el elemento [BaseShape](baseshape.md) , use el elemento [AdditionalProperties](additionalproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="359bf-157">To return properties in addition to those identified by the [BaseShape](baseshape.md) element, use the [AdditionalProperties](additionalproperties.md) element.</span></span> 
  
## <a name="example"></a><span data-ttu-id="359bf-158">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="359bf-158">Example</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindFolder Traversal="Shallow" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <FolderShape>
        <t:BaseShape>Default</t:BaseShape>
      </FolderShape>
      <ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox"/>
      </ParentFolderIds>
    </FindFolder>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a><span data-ttu-id="359bf-159">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="359bf-159">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="359bf-160">Namespace</span><span class="sxs-lookup"><span data-stu-id="359bf-160">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="359bf-161">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="359bf-161">Schema Name</span></span>  <br/> |<span data-ttu-id="359bf-162">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="359bf-162">Types schema</span></span>  <br/> |
|<span data-ttu-id="359bf-163">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="359bf-163">Validation File</span></span>  <br/> |<span data-ttu-id="359bf-164">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="359bf-164">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="359bf-165">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="359bf-165">Can be Empty</span></span>  <br/> |<span data-ttu-id="359bf-166">Falso</span><span class="sxs-lookup"><span data-stu-id="359bf-166">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="359bf-167">Vea también</span><span class="sxs-lookup"><span data-stu-id="359bf-167">See also</span></span>

- [<span data-ttu-id="359bf-168">FolderShape</span><span class="sxs-lookup"><span data-stu-id="359bf-168">FolderShape</span></span>](foldershape.md)
- [<span data-ttu-id="359bf-169">ItemShape</span><span class="sxs-lookup"><span data-stu-id="359bf-169">ItemShape</span></span>](itemshape.md)

