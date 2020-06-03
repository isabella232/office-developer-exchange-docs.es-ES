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
description: El elemento AdditionalProperties identifica propiedades adicionales para su uso en las solicitudes GetItem, UpdateItem, CreateItem, FindItem o FindFolder.
ms.openlocfilehash: 90a307ba4d5ece10e15d2cec56cf5042c3d38685
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455817"
---
# <a name="additionalproperties"></a><span data-ttu-id="ce643-103">AdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="ce643-103">AdditionalProperties</span></span>

<span data-ttu-id="ce643-104">El elemento **AdditionalProperties** identifica propiedades adicionales para su uso en las solicitudes [GetItem](getitem.md), [UpdateItem](updateitem.md), [CreateItem](createitem.md), [FindItem](finditem.md)o [FindFolder](findfolder.md) .</span><span class="sxs-lookup"><span data-stu-id="ce643-104">The **AdditionalProperties** element identifies additional properties for use in [GetItem](getitem.md), [UpdateItem](updateitem.md), [CreateItem](createitem.md), [FindItem](finditem.md), or [FindFolder](findfolder.md) requests.</span></span> 
  
```xml
<AdditionalProperties>
   <ExtendedFieldURI/>
   <FieldURI/>
   <IndexedFieldURI/>
</AdditionalProperties>
```

 <span data-ttu-id="ce643-105">**NonEmptyArrayOfPathsToElementType**</span><span class="sxs-lookup"><span data-stu-id="ce643-105">**NonEmptyArrayOfPathsToElementType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ce643-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ce643-106">Attributes and elements</span></span>

<span data-ttu-id="ce643-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ce643-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ce643-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="ce643-108">Attributes</span></span>

<span data-ttu-id="ce643-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="ce643-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ce643-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ce643-110">Child elements</span></span>

|<span data-ttu-id="ce643-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ce643-111">**Element**</span></span>|<span data-ttu-id="ce643-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ce643-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ce643-113">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="ce643-113">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="ce643-114">Identifica las propiedades MAPI extendidas para obtener, establecer o crear.</span><span class="sxs-lookup"><span data-stu-id="ce643-114">Identifies extended MAPI properties to get, set, or create.</span></span>  <br/> |
|[<span data-ttu-id="ce643-115">FieldURI</span><span class="sxs-lookup"><span data-stu-id="ce643-115">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="ce643-116">Identifica las propiedades a las que se hace referencia con frecuencia mediante el URI.</span><span class="sxs-lookup"><span data-stu-id="ce643-116">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="ce643-117">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="ce643-117">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="ce643-118">Identifica las propiedades de diccionario a las que se hace referencia con frecuencia por URI.</span><span class="sxs-lookup"><span data-stu-id="ce643-118">Identifies frequently referenced dictionary properties by URI.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ce643-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ce643-119">Parent elements</span></span>

|<span data-ttu-id="ce643-120">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ce643-120">**Element**</span></span>|<span data-ttu-id="ce643-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ce643-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ce643-122">FolderShape</span><span class="sxs-lookup"><span data-stu-id="ce643-122">FolderShape</span></span>](foldershape.md) <br/> | <span data-ttu-id="ce643-123">Identifica las propiedades de carpeta que se incluirán en una respuesta [GetFolder](getfolder.md), [FindFolder](findfolder.md)o [SyncFolderHierarchy](syncfolderhierarchy.md) .</span><span class="sxs-lookup"><span data-stu-id="ce643-123">Identifies the folder properties to include in a [GetFolder](getfolder.md), [FindFolder](findfolder.md), or [SyncFolderHierarchy](syncfolderhierarchy.md) response.</span></span><br/><br/>  <span data-ttu-id="ce643-124">Las siguientes son las expresiones XPath de este elemento:</span><span class="sxs-lookup"><span data-stu-id="ce643-124">The following are the XPath expressions to this element:</span></span><br/><br/>  `/FindFolder/FolderShape` <br/>  `/GetFolder/FolderShape` <br/>  `/SyncFolderHierarchy/FolderShape` <br/> |
|[<span data-ttu-id="ce643-125">ItemShape</span><span class="sxs-lookup"><span data-stu-id="ce643-125">ItemShape</span></span>](itemshape.md) <br/> | <span data-ttu-id="ce643-126">Identifica el contenido y las propiedades de los elementos que se van a incluir en una respuesta [GetItem](getitem.md), [FindItem](finditem.md)o [SyncFolderItems](syncfolderitems.md) .</span><span class="sxs-lookup"><span data-stu-id="ce643-126">Identifies the item properties and content to include in a [GetItem](getitem.md), [FindItem](finditem.md), or [SyncFolderItems](syncfolderitems.md) response.</span></span><br/><br/>  <span data-ttu-id="ce643-127">Las siguientes son las expresiones XPath de este elemento:</span><span class="sxs-lookup"><span data-stu-id="ce643-127">The following are the XPath expressions to this element:</span></span><br/><br/>  `/GetItem/ItemShape` <br/>  `/FindItem/ItemShape` <br/>  `/SyncFolderItems/ItemShape` <br/> |
|[<span data-ttu-id="ce643-128">AttachmentShape</span><span class="sxs-lookup"><span data-stu-id="ce643-128">AttachmentShape</span></span>](attachmentshape.md) <br/> |<span data-ttu-id="ce643-129">Identifica las propiedades adicionales de elementos extendidos que se devolverán en una respuesta a una solicitud [GetItem](getitem.md) .</span><span class="sxs-lookup"><span data-stu-id="ce643-129">Identifies additional extended item properties to return in a response to a [GetItem](getitem.md) request.</span></span><br/><br/> <span data-ttu-id="ce643-130">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="ce643-130">The following is the XPath expression to this element:</span></span><br/><br/>  `/GetAttachment/AttachmentShape` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ce643-131">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ce643-131">Remarks</span></span>

<span data-ttu-id="ce643-132">No todos los elementos secundarios se pueden usar con las solicitudes [GetItem](getitem.md), [UpdateItem](updateitem.md), [CreateItem](createitem.md), [FindItem](finditem.md)o [FindFolder](findfolder.md) .</span><span class="sxs-lookup"><span data-stu-id="ce643-132">Not all the child elements can be used with [GetItem](getitem.md), [UpdateItem](updateitem.md), [CreateItem](createitem.md), [FindItem](finditem.md), or [FindFolder](findfolder.md) requests.</span></span> <span data-ttu-id="ce643-133">La propiedad debe ser aplicable a la carpeta o al elemento al que se obtiene acceso.</span><span class="sxs-lookup"><span data-stu-id="ce643-133">The property must be applicable to the folder or item that is accessed.</span></span> <span data-ttu-id="ce643-134">Usar propiedades extendidas para obtener acceso a otras propiedades.</span><span class="sxs-lookup"><span data-stu-id="ce643-134">Use extended properties to access other properties.</span></span> <span data-ttu-id="ce643-135">Si la propiedad no existe para un elemento determinado, no se emitirá ningún elemento correspondiente en el XML resultante.</span><span class="sxs-lookup"><span data-stu-id="ce643-135">If the property does not exist for a given item, no corresponding element will be emitted into the resulting XML.</span></span> 
  
<span data-ttu-id="ce643-136">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="ce643-136">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
<span data-ttu-id="ce643-137">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="ce643-137">This element is optional.</span></span>
  
## <a name="example"></a><span data-ttu-id="ce643-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ce643-138">Example</span></span>

<span data-ttu-id="ce643-139">En el siguiente ejemplo de solicitud se muestra cómo obtener un elemento de asunto mediante el elemento **AdditionalProperties** .</span><span class="sxs-lookup"><span data-stu-id="ce643-139">The following request example shows how to get an item subject by using the **AdditionalProperties** element.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" 
                  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="element-information"></a><span data-ttu-id="ce643-140">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ce643-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ce643-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="ce643-141">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ce643-142">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ce643-142">Schema Name</span></span>  <br/> |<span data-ttu-id="ce643-143">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="ce643-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="ce643-144">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ce643-144">Validation File</span></span>  <br/> |<span data-ttu-id="ce643-145">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="ce643-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ce643-146">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ce643-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="ce643-147">Falso</span><span class="sxs-lookup"><span data-stu-id="ce643-147">False</span></span>  <br/> |
   

