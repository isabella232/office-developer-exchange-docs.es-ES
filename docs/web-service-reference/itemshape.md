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
description: El elemento ItemShape identifica un conjunto de propiedades que se devolverán en una operación GetItem, la operación FindItem o la respuesta de operación SyncFolderItems.
ms.openlocfilehash: ffb666ee331b55a4f04cad076c705e4bec980e03
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458127"
---
# <a name="itemshape"></a><span data-ttu-id="7816a-103">ItemShape</span><span class="sxs-lookup"><span data-stu-id="7816a-103">ItemShape</span></span>

<span data-ttu-id="7816a-104">El elemento **ItemShape** identifica un conjunto de propiedades que se devolverán en una [operación GetItem](getitem-operation.md), la [operación FindItem](finditem-operation.md)o la respuesta de [operación SyncFolderItems](syncfolderitems-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="7816a-104">The **ItemShape** element identifies a set of properties to return in a [GetItem operation](getitem-operation.md), [FindItem operation](finditem-operation.md), or [SyncFolderItems operation](syncfolderitems-operation.md) response.</span></span> 
  
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

 <span data-ttu-id="7816a-105">**ItemResponseShapeType**</span><span class="sxs-lookup"><span data-stu-id="7816a-105">**ItemResponseShapeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7816a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="7816a-106">Attributes and elements</span></span>

<span data-ttu-id="7816a-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="7816a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7816a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="7816a-108">Attributes</span></span>

<span data-ttu-id="7816a-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="7816a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7816a-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7816a-110">Child elements</span></span>

|<span data-ttu-id="7816a-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7816a-111">**Element**</span></span>|<span data-ttu-id="7816a-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7816a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7816a-113">BaseShape</span><span class="sxs-lookup"><span data-stu-id="7816a-113">BaseShape</span></span>](baseshape.md) <br/> |<span data-ttu-id="7816a-114">Identifica la configuración básica de las propiedades que se devolverán en una respuesta de elemento o carpeta.</span><span class="sxs-lookup"><span data-stu-id="7816a-114">Identifies the basic configuration of properties to return in an item or folder response.</span></span>  <br/> |
|[<span data-ttu-id="7816a-115">IncludeMimeContent</span><span class="sxs-lookup"><span data-stu-id="7816a-115">IncludeMimeContent</span></span>](includemimecontent.md) <br/> |<span data-ttu-id="7816a-116">Especifica si se devuelve el contenido de extensiones multipropósito de correo Internet (MIME) de un elemento en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7816a-116">Specifies whether the Multipurpose Internet Mail Extensions (MIME) content of an item is returned in the response.</span></span>  <br/> |
|[<span data-ttu-id="7816a-117">BodyType</span><span class="sxs-lookup"><span data-stu-id="7816a-117">BodyType</span></span>](bodytype.md) <br/> |<span data-ttu-id="7816a-118">Identifica cómo se aplica formato al texto del cuerpo en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7816a-118">Identifies how the body text is formatted in the response.</span></span>  <br/> |
|[<span data-ttu-id="7816a-119">ConvertHtmlCodePageToUTF8</span><span class="sxs-lookup"><span data-stu-id="7816a-119">ConvertHtmlCodePageToUTF8</span></span>](converthtmlcodepagetoutf8.md) <br/> |<span data-ttu-id="7816a-120">Indica si el cuerpo HTML del elemento se convierte en UTF8.</span><span class="sxs-lookup"><span data-stu-id="7816a-120">Indicates whether the item HTML body is converted to UTF8.</span></span>  <br/> |
|[<span data-ttu-id="7816a-121">FilterHtmlContent</span><span class="sxs-lookup"><span data-stu-id="7816a-121">FilterHtmlContent</span></span>](filterhtmlcontent.md) <br/> |<span data-ttu-id="7816a-122">Especifica si está habilitado el filtrado de contenido HTML.</span><span class="sxs-lookup"><span data-stu-id="7816a-122">Specifies whether HTML content filtering is enabled.</span></span>  <br/> |
|[<span data-ttu-id="7816a-123">AdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="7816a-123">AdditionalProperties</span></span>](additionalproperties.md) <br/> |<span data-ttu-id="7816a-124">Identifica las propiedades adicionales que se devolverán en una respuesta.</span><span class="sxs-lookup"><span data-stu-id="7816a-124">Identifies additional properties to return in a response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7816a-125">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7816a-125">Parent elements</span></span>

|<span data-ttu-id="7816a-126">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7816a-126">**Element**</span></span>|<span data-ttu-id="7816a-127">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7816a-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7816a-128">GetItem</span><span class="sxs-lookup"><span data-stu-id="7816a-128">GetItem</span></span>](getitem.md) <br/> |<span data-ttu-id="7816a-129">Define una solicitud para recuperar elementos de un buzón de correo en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="7816a-129">Defines a request to retrieve items from a mailbox in the Exchange store.</span></span>  <br/> <span data-ttu-id="7816a-130">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="7816a-130">The following is the XPath expression to this element:</span></span>  <br/>  `/GetItem` <br/> |
|[<span data-ttu-id="7816a-131">FindItem</span><span class="sxs-lookup"><span data-stu-id="7816a-131">FindItem</span></span>](finditem.md) <br/> |<span data-ttu-id="7816a-132">Define una solicitud para buscar todos los elementos que se encuentran en una carpeta.</span><span class="sxs-lookup"><span data-stu-id="7816a-132">Defines a request to find all items that are contained in a folder.</span></span>  <br/> <span data-ttu-id="7816a-133">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="7816a-133">The following is the XPath expression to this element:</span></span>  <br/>  `/FindItem` <br/> |
|[<span data-ttu-id="7816a-134">SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="7816a-134">SyncFolderItems</span></span>](syncfolderitems.md) <br/> |<span data-ttu-id="7816a-135">Define una solicitud para sincronizar elementos en una carpeta de almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="7816a-135">Defines a request to synchronize items in an Exchange store folder.</span></span>  <br/> <span data-ttu-id="7816a-136">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="7816a-136">The following is the XPath expression to this element:</span></span>  <br/>  `/SyncFolderItems` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7816a-137">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="7816a-137">Text value</span></span>

<span data-ttu-id="7816a-138">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7816a-138">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7816a-139">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7816a-139">Remarks</span></span>

<span data-ttu-id="7816a-140">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="7816a-140">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7816a-141">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7816a-141">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7816a-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="7816a-142">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="7816a-143">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="7816a-143">Schema Name</span></span>  <br/> |<span data-ttu-id="7816a-144">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="7816a-144">Messages schema</span></span>  <br/> |
|<span data-ttu-id="7816a-145">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="7816a-145">Validation File</span></span>  <br/> |<span data-ttu-id="7816a-146">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="7816a-146">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7816a-147">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="7816a-147">Can be Empty</span></span>  <br/> |<span data-ttu-id="7816a-148">Falso</span><span class="sxs-lookup"><span data-stu-id="7816a-148">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7816a-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="7816a-149">See also</span></span>



[<span data-ttu-id="7816a-150">Operación GetItem</span><span class="sxs-lookup"><span data-stu-id="7816a-150">GetItem operation</span></span>](getitem-operation.md)
  
[<span data-ttu-id="7816a-151">Operación FindItem</span><span class="sxs-lookup"><span data-stu-id="7816a-151">FindItem operation</span></span>](finditem-operation.md)
  
[<span data-ttu-id="7816a-152">Operación SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="7816a-152">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)


- [<span data-ttu-id="7816a-153">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="7816a-153">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

