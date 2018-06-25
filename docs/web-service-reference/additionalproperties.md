---
title: AdditionalProperties
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AdditionalProperties
api_type:
- schema
ms.assetid: 7a269aed-dcfd-4c3e-9e14-094e53828101
description: El elemento AdditionalProperties identifica propiedades adicionales para su uso en GetItem, UpdateItem, CreateItem, FindItem o solicitudes FindFolder.
ms.openlocfilehash: 64e4f1ee6b24cf8015b7893dc4a904ca8b32d58e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763404"
---
# <a name="additionalproperties"></a><span data-ttu-id="f984b-103">AdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="f984b-103">AdditionalProperties</span></span>

<span data-ttu-id="f984b-104">El elemento **AdditionalProperties** identifica propiedades adicionales para su uso en [GetItem](getitem.md), [UpdateItem](updateitem.md), [CreateItem](createitem.md), [FindItem](finditem.md)o solicitudes [FindFolder](findfolder.md) .</span><span class="sxs-lookup"><span data-stu-id="f984b-104">The **AdditionalProperties** element identifies additional properties for use in [GetItem](getitem.md), [UpdateItem](updateitem.md), [CreateItem](createitem.md), [FindItem](finditem.md), or [FindFolder](findfolder.md) requests.</span></span> 
  
```xml
<AdditionalProperties>
   <ExtendedFieldURI/>
   <FieldURI/>
   <IndexedFieldURI/>
</AdditionalProperties>
```

 <span data-ttu-id="f984b-105">**NonEmptyArrayOfPathsToElementType**</span><span class="sxs-lookup"><span data-stu-id="f984b-105">**NonEmptyArrayOfPathsToElementType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f984b-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f984b-106">Attributes and elements</span></span>

<span data-ttu-id="f984b-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f984b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f984b-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="f984b-108">Attributes</span></span>

<span data-ttu-id="f984b-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f984b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f984b-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f984b-110">Child elements</span></span>

|<span data-ttu-id="f984b-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="f984b-111">**Element**</span></span>|<span data-ttu-id="f984b-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f984b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f984b-113">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="f984b-113">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="f984b-114">Identifica las propiedades extendidas de MAPI para obtener, establecer o crear.</span><span class="sxs-lookup"><span data-stu-id="f984b-114">Identifies extended MAPI properties to get, set, or create.</span></span>  <br/> |
|[<span data-ttu-id="f984b-115">FieldURI</span><span class="sxs-lookup"><span data-stu-id="f984b-115">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="f984b-116">Identifica las propiedades con frecuencia que se hace referencia mediante un identificador URI.</span><span class="sxs-lookup"><span data-stu-id="f984b-116">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="f984b-117">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="f984b-117">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="f984b-118">Identifica las propiedades de diccionario con frecuencia que se hace referencia mediante un identificador URI.</span><span class="sxs-lookup"><span data-stu-id="f984b-118">Identifies frequently referenced dictionary properties by URI.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f984b-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f984b-119">Parent elements</span></span>

|<span data-ttu-id="f984b-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="f984b-120">**Element**</span></span>|<span data-ttu-id="f984b-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f984b-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f984b-122">FolderShape</span><span class="sxs-lookup"><span data-stu-id="f984b-122">FolderShape</span></span>](foldershape.md) <br/> | <span data-ttu-id="f984b-123">Identifica las propiedades de carpeta para incluir en una respuesta [GetFolder](getfolder.md), [FindFolder](findfolder.md)o [SyncFolderHierarchy](syncfolderhierarchy.md) .</span><span class="sxs-lookup"><span data-stu-id="f984b-123">Identifies the folder properties to include in a [GetFolder](getfolder.md), [FindFolder](findfolder.md), or [SyncFolderHierarchy](syncfolderhierarchy.md) response.</span></span><br/><br/>  <span data-ttu-id="f984b-124">Los siguientes son las expresiones de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="f984b-124">The following are the XPath expressions to this element:</span></span><br/><br/>  `/FindFolder/FolderShape` <br/>  `/GetFolder/FolderShape` <br/>  `/SyncFolderHierarchy/FolderShape` <br/> |
|[<span data-ttu-id="f984b-125">ItemShape</span><span class="sxs-lookup"><span data-stu-id="f984b-125">ItemShape</span></span>](itemshape.md) <br/> | <span data-ttu-id="f984b-126">Identifica las propiedades de elemento y el contenido que desea incluir en una respuesta [GetItem](getitem.md), [FindItem](finditem.md)o [SyncFolderItems](syncfolderitems.md) .</span><span class="sxs-lookup"><span data-stu-id="f984b-126">Identifies the item properties and content to include in a [GetItem](getitem.md), [FindItem](finditem.md), or [SyncFolderItems](syncfolderitems.md) response.</span></span><br/><br/>  <span data-ttu-id="f984b-127">Los siguientes son las expresiones de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="f984b-127">The following are the XPath expressions to this element:</span></span><br/><br/>  `/GetItem/ItemShape` <br/>  `/FindItem/ItemShape` <br/>  `/SyncFolderItems/ItemShape` <br/> |
|[<span data-ttu-id="f984b-128">AttachmentShape</span><span class="sxs-lookup"><span data-stu-id="f984b-128">AttachmentShape</span></span>](attachmentshape.md) <br/> |<span data-ttu-id="f984b-129">Identifica las propiedades adicionales total del artículo para devolver en una respuesta a una solicitud de [GetItem](getitem.md) .</span><span class="sxs-lookup"><span data-stu-id="f984b-129">Identifies additional extended item properties to return in a response to a [GetItem](getitem.md) request.</span></span><br/><br/> <span data-ttu-id="f984b-130">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="f984b-130">The following is the XPath expression to this element:</span></span><br/><br/>  `/GetAttachment/AttachmentShape` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f984b-131">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f984b-131">Remarks</span></span>

<span data-ttu-id="f984b-132">No todos los elementos secundarios pueden usarse con [GetItem](getitem.md), [UpdateItem](updateitem.md), [CreateItem](createitem.md), [FindItem](finditem.md)o solicitudes [FindFolder](findfolder.md) .</span><span class="sxs-lookup"><span data-stu-id="f984b-132">Not all the child elements can be used with [GetItem](getitem.md), [UpdateItem](updateitem.md), [CreateItem](createitem.md), [FindItem](finditem.md), or [FindFolder](findfolder.md) requests.</span></span> <span data-ttu-id="f984b-133">La propiedad debe ser aplicable a la carpeta o elemento que se tiene acceso.</span><span class="sxs-lookup"><span data-stu-id="f984b-133">The property must be applicable to the folder or item that is accessed.</span></span> <span data-ttu-id="f984b-134">Utilice las propiedades extendidas para tener acceso a otras propiedades.</span><span class="sxs-lookup"><span data-stu-id="f984b-134">Use extended properties to access other properties.</span></span> <span data-ttu-id="f984b-135">Si la propiedad no existe para un elemento determinado, no se emitirá ningún elemento correspondiente en el XML resultante.</span><span class="sxs-lookup"><span data-stu-id="f984b-135">If the property does not exist for a given item, no corresponding element will be emitted into the resulting XML.</span></span> 
  
<span data-ttu-id="f984b-136">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="f984b-136">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
<span data-ttu-id="f984b-137">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="f984b-137">This element is optional.</span></span>
  
## <a name="example"></a><span data-ttu-id="f984b-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f984b-138">Example</span></span>

<span data-ttu-id="f984b-139">En el siguiente ejemplo de solicitud muestra cómo obtener a un asunto del elemento mediante el elemento **AdditionalProperties** .</span><span class="sxs-lookup"><span data-stu-id="f984b-139">The following request example shows how to get an item subject by using the **AdditionalProperties** element.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetItem xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" 
                  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject"/>
        </t:AdditionalProperties>
      </ItemShape>
      <ItemIds>
        <t:ItemId Id="ASkAS="/>
      </ItemIds>
    </GetItem>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a><span data-ttu-id="f984b-140">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f984b-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f984b-141">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f984b-141">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f984b-142">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f984b-142">Schema Name</span></span>  <br/> |<span data-ttu-id="f984b-143">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="f984b-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="f984b-144">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f984b-144">Validation File</span></span>  <br/> |<span data-ttu-id="f984b-145">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f984b-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f984b-146">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f984b-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="f984b-147">False</span><span class="sxs-lookup"><span data-stu-id="f984b-147">False</span></span>  <br/> |
   

