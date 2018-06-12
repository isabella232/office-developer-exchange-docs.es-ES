---
title: IndexedPageItemView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IndexedPageItemView
api_type:
- schema
ms.assetid: 6d1b0b04-cc35-4a57-bd7a-824136d14fda
description: El elemento IndexedPageItemView describe cómo paginada conversación o elemento se devuelve información para una operación FindItem o una solicitud de operación FindConversation.
ms.openlocfilehash: f1743e22087158c1889977f03774fccbc5577390
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19835919"
---
# <a name="indexedpageitemview"></a><span data-ttu-id="ffc4a-103">IndexedPageItemView</span><span class="sxs-lookup"><span data-stu-id="ffc4a-103">IndexedPageItemView</span></span>

<span data-ttu-id="ffc4a-104">El elemento **IndexedPageItemView** describe cómo paginada conversación o elemento se devuelve información para una solicitud de [operación de FindItem](finditem-operation.md) o [FindConversation](findconversation-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="ffc4a-104">The **IndexedPageItemView** element describes how paged conversation or item information is returned for a [FindItem operation](finditem-operation.md) or [FindConversation operation](findconversation-operation.md) request.</span></span> 
  
```XML
<IndexedPageViewItemView MaxEntriesReturned="" Offset="" BasePoint=""/>
```

 <span data-ttu-id="ffc4a-105">**IndexedPageViewType**</span><span class="sxs-lookup"><span data-stu-id="ffc4a-105">**IndexedPageViewType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ffc4a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ffc4a-106">Attributes and elements</span></span>

<span data-ttu-id="ffc4a-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ffc4a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ffc4a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="ffc4a-108">Attributes</span></span>

|<span data-ttu-id="ffc4a-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="ffc4a-109">**Attribute**</span></span>|<span data-ttu-id="ffc4a-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ffc4a-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ffc4a-111">**MaxEntriesReturned**</span><span class="sxs-lookup"><span data-stu-id="ffc4a-111">**MaxEntriesReturned**</span></span> <br/> |<span data-ttu-id="ffc4a-112">Describe el número máximo de elementos o conversaciones para devolver en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ffc4a-112">Describes the maximum number of items or conversations to return in the response.</span></span> <span data-ttu-id="ffc4a-113">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="ffc4a-113">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="ffc4a-114">**Offset**</span><span class="sxs-lookup"><span data-stu-id="ffc4a-114">**Offset**</span></span> <br/> |<span data-ttu-id="ffc4a-115">Describe el desplazamiento desde el **punto base**.</span><span class="sxs-lookup"><span data-stu-id="ffc4a-115">Describes the offset from the **BasePoint**.</span></span> <span data-ttu-id="ffc4a-116">Si el **punto base** es igual al principio, el desplazamiento es positivo.</span><span class="sxs-lookup"><span data-stu-id="ffc4a-116">If **BasePoint** is equal to Beginning, the offset is positive.</span></span> <span data-ttu-id="ffc4a-117">Si el **punto base** es igual a End, el desplazamiento se administra como si fuese negativo.</span><span class="sxs-lookup"><span data-stu-id="ffc4a-117">If **BasePoint** is equal to End, the offset is handled as if it were negative.</span></span> <span data-ttu-id="ffc4a-118">Esto identifica qué elemento o conversación será la primera entregar en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ffc4a-118">This identifies which item or conversation will be the first to be delivered in the response.</span></span> <span data-ttu-id="ffc4a-119">Este atributo es necesario.</span><span class="sxs-lookup"><span data-stu-id="ffc4a-119">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="ffc4a-120">**Punto base**</span><span class="sxs-lookup"><span data-stu-id="ffc4a-120">**BasePoint**</span></span> <br/> |<span data-ttu-id="ffc4a-121">Describe si la página de elementos o las conversaciones se iniciará desde el principio o al final del conjunto de elementos o las conversaciones que se encuentran mediante el uso de los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ffc4a-121">Describes whether the page of items or conversations will start from the beginning or the end of the set of items or conversations that are found by using the search criteria.</span></span> <span data-ttu-id="ffc4a-122">Buscar desde el final siempre busca hacia atrás.</span><span class="sxs-lookup"><span data-stu-id="ffc4a-122">Seeking from the end always searches backward.</span></span> <span data-ttu-id="ffc4a-123">Este atributo es necesario.</span><span class="sxs-lookup"><span data-stu-id="ffc4a-123">This attribute is required.</span></span>  <br/> |
   
#### <a name="basepoint-attribute"></a><span data-ttu-id="ffc4a-124">Atributo de punto base</span><span class="sxs-lookup"><span data-stu-id="ffc4a-124">BasePoint Attribute</span></span>

|<span data-ttu-id="ffc4a-125">**Valor**</span><span class="sxs-lookup"><span data-stu-id="ffc4a-125">**Value**</span></span>|<span data-ttu-id="ffc4a-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ffc4a-126">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ffc4a-127">Principio</span><span class="sxs-lookup"><span data-stu-id="ffc4a-127">Beginning</span></span>  <br/> |<span data-ttu-id="ffc4a-128">La vista de página comienza al principio del conjunto de conversación o elemento que se encuentra.</span><span class="sxs-lookup"><span data-stu-id="ffc4a-128">The paged view starts at the beginning of the found conversation or item set.</span></span>  <br/> |
|<span data-ttu-id="ffc4a-129">End</span><span class="sxs-lookup"><span data-stu-id="ffc4a-129">End</span></span>  <br/> |<span data-ttu-id="ffc4a-130">Se inicia la vista de página al final del conjunto de conversación o elemento que se encuentra.</span><span class="sxs-lookup"><span data-stu-id="ffc4a-130">The paged view starts at the end of the found conversation or item set.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ffc4a-131">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ffc4a-131">Child elements</span></span>

<span data-ttu-id="ffc4a-132">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ffc4a-132">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ffc4a-133">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ffc4a-133">Parent elements</span></span>

|<span data-ttu-id="ffc4a-134">**Element**</span><span class="sxs-lookup"><span data-stu-id="ffc4a-134">**Element**</span></span>|<span data-ttu-id="ffc4a-135">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ffc4a-135">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ffc4a-136">FindItem</span><span class="sxs-lookup"><span data-stu-id="ffc4a-136">FindItem</span></span>](finditem.md) <br/> |<span data-ttu-id="ffc4a-137">Define una solicitud para buscar elementos en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="ffc4a-137">Defines a request to find items in a mailbox.</span></span>  <br/> <span data-ttu-id="ffc4a-138">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="ffc4a-138">The following is the XPath expression to this element:</span></span>  <br/>  `/FindItem` <br/> |
|[<span data-ttu-id="ffc4a-139">FindConversation</span><span class="sxs-lookup"><span data-stu-id="ffc4a-139">FindConversation</span></span>](findconversation.md) <br/> |<span data-ttu-id="ffc4a-140">Define una solicitud para buscar las conversaciones en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="ffc4a-140">Defines a request to find conversations in a mailbox.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ffc4a-141">Notas</span><span class="sxs-lookup"><span data-stu-id="ffc4a-141">Remarks</span></span>

<span data-ttu-id="ffc4a-142">Buscar desde el final implica mover para el origen identificado por el desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="ffc4a-142">Seeking from the end involves moving to the origin identified by the offset.</span></span> <span data-ttu-id="ffc4a-143">Además, el puntero se mueve de nuevo el número de registros solicitados.</span><span class="sxs-lookup"><span data-stu-id="ffc4a-143">Additionally, the pointer is moved back by the number of requested records.</span></span> <span data-ttu-id="ffc4a-144">Por ejemplo, si hay 100 registros y el desplazamiento es 25 desde el final, la búsqueda comienza desde 75.</span><span class="sxs-lookup"><span data-stu-id="ffc4a-144">For example, if there are 100 records and the offset is 25 from the end, the search starts from 75.</span></span> <span data-ttu-id="ffc4a-145">Si se devuelven 10 registros, el puntero se mueve hacia atrás un 10 adicionales a 65 de registros y devuelve los registros 65 a través de 75.</span><span class="sxs-lookup"><span data-stu-id="ffc4a-145">If 10 records are returned, the pointer is moved backward an additional 10 records to 65 and returns records 65 through 75.</span></span> <span data-ttu-id="ffc4a-146">El siguiente índice es 64.</span><span class="sxs-lookup"><span data-stu-id="ffc4a-146">The next index is 64.</span></span> <span data-ttu-id="ffc4a-147">El desplazamiento desde el final de una página siguiente es 100 menos 64 que es igual a 36.</span><span class="sxs-lookup"><span data-stu-id="ffc4a-147">The next offset from the end for a page is 100 minus 64 which equals 36.</span></span> <span data-ttu-id="ffc4a-148">36 es el valor para el desvío siguiente desde el final para obtener la siguiente página indizada.</span><span class="sxs-lookup"><span data-stu-id="ffc4a-148">36 is the value for the next offset from the end to get the next indexed page.</span></span>
  
<span data-ttu-id="ffc4a-149">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="ffc4a-149">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="example"></a><span data-ttu-id="ffc4a-150">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ffc4a-150">Example</span></span>

<span data-ttu-id="ffc4a-151">En el ejemplo siguiente se muestra una solicitud de [operación FindItem](finditem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="ffc4a-151">The following example shows a [FindItem operation](finditem-operation.md) request.</span></span> <span data-ttu-id="ffc4a-152">Cada elemento se devuelve con su identificador y el asunto.</span><span class="sxs-lookup"><span data-stu-id="ffc4a-152">Each item is returned with its ID and subject.</span></span> <span data-ttu-id="ffc4a-153">Un máximo de seis artículos se devuelven en la respuesta, tal como se especifica mediante el atributo **MaxEntriesReturned** .</span><span class="sxs-lookup"><span data-stu-id="ffc4a-153">A maximum of six items are returned in the response, as specified by the **MaxEntriesReturned** attribute.</span></span> <span data-ttu-id="ffc4a-154">Los elementos se muestran en orden ascendente agrupados por importancia.</span><span class="sxs-lookup"><span data-stu-id="ffc4a-154">The items are listed in ascending order grouped by importance.</span></span> <span data-ttu-id="ffc4a-155">Elementos de un grupo se agregan por asunto.</span><span class="sxs-lookup"><span data-stu-id="ffc4a-155">Items in a group are aggregated by subject.</span></span> 
  
```XML
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindItem Traversal="Shallow" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject"/>
        </t:AdditionalProperties>
      </ItemShape>
      <IndexedPageItemView MaxEntriesReturned="6" BasePoint="Beginning" Offset="0" />
      <GroupBy Order="Ascending">
        <t:FieldURI FieldURI="item:Importance"/>
        <t:AggregateOn Aggregate="Maximum">
          <t:FieldURI FieldURI="item:Subject"/>
        </t:AggregateOn>
      </GroupBy>
      <ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox"/>
      </ParentFolderIds>
    </FindItem>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a><span data-ttu-id="ffc4a-156">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ffc4a-156">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ffc4a-157">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ffc4a-157">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ffc4a-158">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ffc4a-158">Schema Name</span></span>  <br/> |<span data-ttu-id="ffc4a-159">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="ffc4a-159">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ffc4a-160">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ffc4a-160">Validation File</span></span>  <br/> |<span data-ttu-id="ffc4a-161">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ffc4a-161">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ffc4a-162">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ffc4a-162">Can be Empty</span></span>  <br/> |<span data-ttu-id="ffc4a-163">False</span><span class="sxs-lookup"><span data-stu-id="ffc4a-163">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ffc4a-164">Ver también</span><span class="sxs-lookup"><span data-stu-id="ffc4a-164">See also</span></span>



[<span data-ttu-id="ffc4a-165">Operación FindItem</span><span class="sxs-lookup"><span data-stu-id="ffc4a-165">FindItem operation</span></span>](finditem-operation.md)
  
[<span data-ttu-id="ffc4a-166">Operación de FindConversation</span><span class="sxs-lookup"><span data-stu-id="ffc4a-166">FindConversation operation</span></span>](findconversation-operation.md)


[<span data-ttu-id="ffc4a-167">Buscar elementos</span><span class="sxs-lookup"><span data-stu-id="ffc4a-167">Finding Items</span></span>](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

