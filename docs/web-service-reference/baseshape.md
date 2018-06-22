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
description: El elemento BaseShape identifica el conjunto de propiedades para devolver una respuesta de elemento o carpeta.
ms.openlocfilehash: 69b27d23fd75d4c1a274f31dfa419b759dbb2bbe
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763613"
---
# <a name="baseshape"></a><span data-ttu-id="f1458-103">BaseShape</span><span class="sxs-lookup"><span data-stu-id="f1458-103">BaseShape</span></span>

<span data-ttu-id="f1458-104">El elemento **BaseShape** identifica el conjunto de propiedades para devolver una respuesta de elemento o carpeta.</span><span class="sxs-lookup"><span data-stu-id="f1458-104">The **BaseShape** element identifies the set of properties to return in an item or folder response.</span></span> 
  
```xml
<BaseShape>IdOnly or Default or AllProperties</BaseShape>
```

 <span data-ttu-id="f1458-105">**DefaultShapeNamesType**</span><span class="sxs-lookup"><span data-stu-id="f1458-105">**DefaultShapeNamesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f1458-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f1458-106">Attributes and elements</span></span>

<span data-ttu-id="f1458-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f1458-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f1458-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="f1458-108">Attributes</span></span>

<span data-ttu-id="f1458-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f1458-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f1458-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f1458-110">Child elements</span></span>

<span data-ttu-id="f1458-111">Ninguno</span><span class="sxs-lookup"><span data-stu-id="f1458-111">None</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f1458-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f1458-112">Parent elements</span></span>

|<span data-ttu-id="f1458-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="f1458-113">**Element**</span></span>|<span data-ttu-id="f1458-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f1458-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f1458-115">FolderShape</span><span class="sxs-lookup"><span data-stu-id="f1458-115">FolderShape</span></span>](foldershape.md) <br/> | <span data-ttu-id="f1458-116">Identifica las propiedades de carpeta para incluir en la respuesta GetFolder, FindFolder o SyncFolderHierarchy.</span><span class="sxs-lookup"><span data-stu-id="f1458-116">Identifies the folder properties to include in the GetFolder, FindFolder, or SyncFolderHierarchy response.</span></span><br/><br/><span data-ttu-id="f1458-117">Los siguientes son las expresiones de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="f1458-117">The following are the XPath expressions to this element:</span></span><br/><br/>`/GetFolder/FolderShape` <br/>  `/FindFolder/FolderShape` <br/>  `/SyncFolderHierarchy/FolderShape` <br/> |
|[<span data-ttu-id="f1458-118">ItemShape</span><span class="sxs-lookup"><span data-stu-id="f1458-118">ItemShape</span></span>](itemshape.md) <br/> | <span data-ttu-id="f1458-119">Identifica las propiedades de elemento y el contenido que desea incluir en una respuesta GetItem, FindItem o SyncFolderItems.</span><span class="sxs-lookup"><span data-stu-id="f1458-119">Identifies the item properties and content to include in a GetItem, FindItem, or SyncFolderItems response.</span></span><br/><br/><span data-ttu-id="f1458-120">Los siguientes son las expresiones de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="f1458-120">The following are the XPath expressions to this element:</span></span><br/><br/>`/GetItem/ItemShape` <br/>  `/FindItem/ItemShape` <br/>  `/SyncFolderItems/ItemShape` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f1458-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="f1458-121">Text value</span></span>

<span data-ttu-id="f1458-122">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="f1458-122">A text value is required.</span></span> <span data-ttu-id="f1458-123">En la siguiente tabla se enumera los posibles valores de texto.</span><span class="sxs-lookup"><span data-stu-id="f1458-123">The following table lists the possible text values.</span></span>
  
<span data-ttu-id="f1458-124">**Valores de texto para el elemento BaseShape**</span><span class="sxs-lookup"><span data-stu-id="f1458-124">**Text values for the BaseShape element**</span></span>

|<span data-ttu-id="f1458-125">**Valor**</span><span class="sxs-lookup"><span data-stu-id="f1458-125">**Value**</span></span>|<span data-ttu-id="f1458-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f1458-126">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f1458-127">IdOnly</span><span class="sxs-lookup"><span data-stu-id="f1458-127">IdOnly</span></span>  <br/> |<span data-ttu-id="f1458-128">Devuelve sólo el elemento o carpeta Id.</span><span class="sxs-lookup"><span data-stu-id="f1458-128">Returns only the item or folder ID.</span></span>  <br/> |
|<span data-ttu-id="f1458-129">Default</span><span class="sxs-lookup"><span data-stu-id="f1458-129">Default</span></span>  <br/> |<span data-ttu-id="f1458-130">Devuelve un conjunto de propiedades que se definen como el valor predeterminado para el elemento o la carpeta.</span><span class="sxs-lookup"><span data-stu-id="f1458-130">Returns a set of properties that are defined as the default for the item or folder.</span></span>  <br/> |
|<span data-ttu-id="f1458-131">AllProperties</span><span class="sxs-lookup"><span data-stu-id="f1458-131">AllProperties</span></span>  <br/> |<span data-ttu-id="f1458-132">Devuelve todas las propiedades de la capa de lógica de negocios de Exchange utilizadas para construir una carpeta.</span><span class="sxs-lookup"><span data-stu-id="f1458-132">Returns all the properties used by the Exchange Business Logic layer to construct a folder.</span></span>  <br/> |
   
<span data-ttu-id="f1458-133">En la siguiente tabla se enumera las propiedades predeterminadas que se devuelven para una solicitud de FindFolder.</span><span class="sxs-lookup"><span data-stu-id="f1458-133">The following table lists the default properties that are returned for a FindFolder request.</span></span> <span data-ttu-id="f1458-134">Todas las subcarpetas de una carpeta determinada se devuelven en orden por su nombre.</span><span class="sxs-lookup"><span data-stu-id="f1458-134">All subfolders of a given folder are returned in order by name.</span></span>
  
<span data-ttu-id="f1458-135">**Propiedades predeterminadas**</span><span class="sxs-lookup"><span data-stu-id="f1458-135">**Default properties**</span></span>

|<span data-ttu-id="f1458-136">**Folder**</span><span class="sxs-lookup"><span data-stu-id="f1458-136">**Folder**</span></span>|<span data-ttu-id="f1458-137">**Propiedades predeterminadas**</span><span class="sxs-lookup"><span data-stu-id="f1458-137">**Default Properties**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f1458-138">Bandeja de entrada</span><span class="sxs-lookup"><span data-stu-id="f1458-138">Inbox</span></span>  <br/> |<span data-ttu-id="f1458-139">FolderId, nombre para mostrar, count no leído, recuento total, recuento de subcarpeta</span><span class="sxs-lookup"><span data-stu-id="f1458-139">FolderId, display name, unread count, total count, subfolder count</span></span>  <br/> |
|<span data-ttu-id="f1458-140">Contacts</span><span class="sxs-lookup"><span data-stu-id="f1458-140">Contacts</span></span>  <br/> |<span data-ttu-id="f1458-141">FolderId, nombre para mostrar, el recuento total, el recuento de subcarpeta</span><span class="sxs-lookup"><span data-stu-id="f1458-141">FolderId, display name, total count, subfolder count</span></span>  <br/> |
|<span data-ttu-id="f1458-142">Calendar</span><span class="sxs-lookup"><span data-stu-id="f1458-142">Calendar</span></span>  <br/> |<span data-ttu-id="f1458-143">FolderId, nombre para mostrar, el recuento de subcarpeta</span><span class="sxs-lookup"><span data-stu-id="f1458-143">FolderId, display name, subfolder count</span></span>  <br/> |
|<span data-ttu-id="f1458-144">Drafts</span><span class="sxs-lookup"><span data-stu-id="f1458-144">Drafts</span></span>  <br/> |<span data-ttu-id="f1458-145">FolderId, nombre para mostrar, count no leído, recuento total, recuento de subcarpeta</span><span class="sxs-lookup"><span data-stu-id="f1458-145">FolderId, display name, unread count, total count, subfolder count</span></span>  <br/> |
|<span data-ttu-id="f1458-146">Elementos eliminados</span><span class="sxs-lookup"><span data-stu-id="f1458-146">Deleted items</span></span>  <br/> |<span data-ttu-id="f1458-147">FolderId, nombre para mostrar, count no leído, recuento total, recuento de subcarpeta</span><span class="sxs-lookup"><span data-stu-id="f1458-147">FolderId, display name, unread count, total count, subfolder count</span></span>  <br/> |
|<span data-ttu-id="f1458-148">Otras carpetas</span><span class="sxs-lookup"><span data-stu-id="f1458-148">Other folders</span></span>  <br/> |<span data-ttu-id="f1458-149">FolderId, nombre para mostrar, count no leído, recuento total, recuento de subcarpeta</span><span class="sxs-lookup"><span data-stu-id="f1458-149">FolderId, display name, unread count, total count, subfolder count</span></span>  <br/> |
|<span data-ttu-id="f1458-150">Bandeja de salida</span><span class="sxs-lookup"><span data-stu-id="f1458-150">Outbox</span></span>  <br/> |<span data-ttu-id="f1458-151">FolderId, nombre para mostrar, count no leído, recuento total, recuento de subcarpeta</span><span class="sxs-lookup"><span data-stu-id="f1458-151">FolderId, display name, unread count, total count, subfolder count</span></span>  <br/> |
|<span data-ttu-id="f1458-152">Tareas</span><span class="sxs-lookup"><span data-stu-id="f1458-152">Tasks</span></span>  <br/> |<span data-ttu-id="f1458-153">FolderId, nombre para mostrar, vencida count, recuento total, recuento de subcarpeta</span><span class="sxs-lookup"><span data-stu-id="f1458-153">FolderId, display name, past due count, total count, subfolder count</span></span>  <br/> |
|<span data-ttu-id="f1458-154">Notas</span><span class="sxs-lookup"><span data-stu-id="f1458-154">Notes</span></span>  <br/> |<span data-ttu-id="f1458-155">FolderId, nombre para mostrar, el recuento total, el recuento de subcarpeta</span><span class="sxs-lookup"><span data-stu-id="f1458-155">FolderId, display name, total count, subfolder count</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f1458-156">Notas</span><span class="sxs-lookup"><span data-stu-id="f1458-156">Remarks</span></span>

<span data-ttu-id="f1458-157">Para devolver propiedades además de las identificado por el elemento [BaseShape](baseshape.md) , use el elemento [AdditionalProperties](additionalproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="f1458-157">To return properties in addition to those identified by the [BaseShape](baseshape.md) element, use the [AdditionalProperties](additionalproperties.md) element.</span></span> 
  
## <a name="example"></a><span data-ttu-id="f1458-158">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f1458-158">Example</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindFolder Traversal="Shallow" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

## <a name="element-information"></a><span data-ttu-id="f1458-159">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f1458-159">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f1458-160">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f1458-160">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f1458-161">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f1458-161">Schema Name</span></span>  <br/> |<span data-ttu-id="f1458-162">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="f1458-162">Types schema</span></span>  <br/> |
|<span data-ttu-id="f1458-163">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f1458-163">Validation File</span></span>  <br/> |<span data-ttu-id="f1458-164">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f1458-164">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f1458-165">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f1458-165">Can be Empty</span></span>  <br/> |<span data-ttu-id="f1458-166">False</span><span class="sxs-lookup"><span data-stu-id="f1458-166">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f1458-167">Ver también</span><span class="sxs-lookup"><span data-stu-id="f1458-167">See also</span></span>

- [<span data-ttu-id="f1458-168">FolderShape</span><span class="sxs-lookup"><span data-stu-id="f1458-168">FolderShape</span></span>](foldershape.md)
- [<span data-ttu-id="f1458-169">ItemShape</span><span class="sxs-lookup"><span data-stu-id="f1458-169">ItemShape</span></span>](itemshape.md)

