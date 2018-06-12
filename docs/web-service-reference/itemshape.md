---
title: ItemShape
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ItemShape
api_type:
- schema
ms.assetid: c5604161-bbc0-40bc-ad75-ff7e837d745f
description: El elemento ItemShape identifica un conjunto de propiedades para devolver en una operación GetItem, operación FindItem o SyncFolderItems respuesta de la operación.
ms.openlocfilehash: 95174a85a8fa05cb2612e1289d46c8db32b6e052
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836191"
---
# <a name="itemshape"></a><span data-ttu-id="ed5c2-103">ItemShape</span><span class="sxs-lookup"><span data-stu-id="ed5c2-103">ItemShape</span></span>

<span data-ttu-id="ed5c2-104">El elemento **ItemShape** identifica un conjunto de propiedades para devolver una respuesta [GetItem operation](getitem-operation.md), [operación FindItem](finditem-operation.md)o [SyncFolderItems](syncfolderitems-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="ed5c2-104">The **ItemShape** element identifies a set of properties to return in a [GetItem operation](getitem-operation.md), [FindItem operation](finditem-operation.md), or [SyncFolderItems operation](syncfolderitems-operation.md) response.</span></span> 
  
```XML
<ItemShape>
   <BaseShape/>
   <IncludeMimeContent/>
   <BodyType/>
   <FilterHtmlContent/>
   <ConvertHtmlCodePageToUTF8/>
   <AdditionalProperties/>
</ItemShape>
```

 <span data-ttu-id="ed5c2-105">**ItemResponseShapeType**</span><span class="sxs-lookup"><span data-stu-id="ed5c2-105">**ItemResponseShapeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ed5c2-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ed5c2-106">Attributes and elements</span></span>

<span data-ttu-id="ed5c2-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ed5c2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ed5c2-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="ed5c2-108">Attributes</span></span>

<span data-ttu-id="ed5c2-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ed5c2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ed5c2-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ed5c2-110">Child elements</span></span>

|<span data-ttu-id="ed5c2-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="ed5c2-111">**Element**</span></span>|<span data-ttu-id="ed5c2-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ed5c2-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ed5c2-113">BaseShape</span><span class="sxs-lookup"><span data-stu-id="ed5c2-113">BaseShape</span></span>](baseshape.md) <br/> |<span data-ttu-id="ed5c2-114">Identifica la configuración básica de propiedades para devolver una respuesta de elemento o carpeta.</span><span class="sxs-lookup"><span data-stu-id="ed5c2-114">Identifies the basic configuration of properties to return in an item or folder response.</span></span>  <br/> |
|[<span data-ttu-id="ed5c2-115">IncludeMimeContent</span><span class="sxs-lookup"><span data-stu-id="ed5c2-115">IncludeMimeContent</span></span>](includemimecontent.md) <br/> |<span data-ttu-id="ed5c2-116">Especifica si el contenido de extensiones multipropósito de correo Internet (MIME) de un elemento se devuelve en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ed5c2-116">Specifies whether the Multipurpose Internet Mail Extensions (MIME) content of an item is returned in the response.</span></span>  <br/> |
|[<span data-ttu-id="ed5c2-117">BodyType</span><span class="sxs-lookup"><span data-stu-id="ed5c2-117">BodyType</span></span>](bodytype.md) <br/> |<span data-ttu-id="ed5c2-118">Identifica cómo se da el formato de texto del cuerpo en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ed5c2-118">Identifies how the body text is formatted in the response.</span></span>  <br/> |
|[<span data-ttu-id="ed5c2-119">ConvertHtmlCodePageToUTF8</span><span class="sxs-lookup"><span data-stu-id="ed5c2-119">ConvertHtmlCodePageToUTF8</span></span>](converthtmlcodepagetoutf8.md) <br/> |<span data-ttu-id="ed5c2-120">Indica si el cuerpo HTML del elemento se convierte en UTF8.</span><span class="sxs-lookup"><span data-stu-id="ed5c2-120">Indicates whether the item HTML body is converted to UTF8.</span></span>  <br/> |
|[<span data-ttu-id="ed5c2-121">FilterHtmlContent</span><span class="sxs-lookup"><span data-stu-id="ed5c2-121">FilterHtmlContent</span></span>](filterhtmlcontent.md) <br/> |<span data-ttu-id="ed5c2-122">Especifica si está habilitado el filtrado de contenido HTML.</span><span class="sxs-lookup"><span data-stu-id="ed5c2-122">Specifies whether HTML content filtering is enabled.</span></span>  <br/> |
|[<span data-ttu-id="ed5c2-123">AdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="ed5c2-123">AdditionalProperties</span></span>](additionalproperties.md) <br/> |<span data-ttu-id="ed5c2-124">Identifica las propiedades adicionales para devolver en una respuesta.</span><span class="sxs-lookup"><span data-stu-id="ed5c2-124">Identifies additional properties to return in a response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ed5c2-125">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ed5c2-125">Parent elements</span></span>

|<span data-ttu-id="ed5c2-126">**Element**</span><span class="sxs-lookup"><span data-stu-id="ed5c2-126">**Element**</span></span>|<span data-ttu-id="ed5c2-127">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ed5c2-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ed5c2-128">GetItem</span><span class="sxs-lookup"><span data-stu-id="ed5c2-128">GetItem</span></span>](getitem.md) <br/> |<span data-ttu-id="ed5c2-129">Define una solicitud para recuperar elementos de un buzón en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ed5c2-129">Defines a request to retrieve items from a mailbox in the Exchange store.</span></span>  <br/> <span data-ttu-id="ed5c2-130">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="ed5c2-130">The following is the XPath expression to this element:</span></span>  <br/>  `/GetItem` <br/> |
|[<span data-ttu-id="ed5c2-131">FindItem</span><span class="sxs-lookup"><span data-stu-id="ed5c2-131">FindItem</span></span>](finditem.md) <br/> |<span data-ttu-id="ed5c2-132">Define una solicitud para buscar todos los elementos que están contenidos en una carpeta.</span><span class="sxs-lookup"><span data-stu-id="ed5c2-132">Defines a request to find all items that are contained in a folder.</span></span>  <br/> <span data-ttu-id="ed5c2-133">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="ed5c2-133">The following is the XPath expression to this element:</span></span>  <br/>  `/FindItem` <br/> |
|[<span data-ttu-id="ed5c2-134">SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="ed5c2-134">SyncFolderItems</span></span>](syncfolderitems.md) <br/> |<span data-ttu-id="ed5c2-135">Define una solicitud para sincronizar los elementos en una carpeta de almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ed5c2-135">Defines a request to synchronize items in an Exchange store folder.</span></span>  <br/> <span data-ttu-id="ed5c2-136">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="ed5c2-136">The following is the XPath expression to this element:</span></span>  <br/>  `/SyncFolderItems` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ed5c2-137">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="ed5c2-137">Text value</span></span>

<span data-ttu-id="ed5c2-138">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ed5c2-138">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ed5c2-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ed5c2-139">Remarks</span></span>

<span data-ttu-id="ed5c2-140">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="ed5c2-140">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ed5c2-141">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ed5c2-141">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ed5c2-142">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ed5c2-142">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ed5c2-143">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ed5c2-143">Schema Name</span></span>  <br/> |<span data-ttu-id="ed5c2-144">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="ed5c2-144">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ed5c2-145">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ed5c2-145">Validation File</span></span>  <br/> |<span data-ttu-id="ed5c2-146">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ed5c2-146">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ed5c2-147">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ed5c2-147">Can be Empty</span></span>  <br/> |<span data-ttu-id="ed5c2-148">False</span><span class="sxs-lookup"><span data-stu-id="ed5c2-148">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ed5c2-149">Ver también</span><span class="sxs-lookup"><span data-stu-id="ed5c2-149">See also</span></span>



[<span data-ttu-id="ed5c2-150">Operación GetItem</span><span class="sxs-lookup"><span data-stu-id="ed5c2-150">GetItem operation</span></span>](getitem-operation.md)
  
[<span data-ttu-id="ed5c2-151">Operación FindItem</span><span class="sxs-lookup"><span data-stu-id="ed5c2-151">FindItem operation</span></span>](finditem-operation.md)
  
[<span data-ttu-id="ed5c2-152">Operación SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="ed5c2-152">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)


- [<span data-ttu-id="ed5c2-153">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="ed5c2-153">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

