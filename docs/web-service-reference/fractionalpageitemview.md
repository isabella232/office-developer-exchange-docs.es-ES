---
title: FractionalPageItemView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FractionalPageItemView
api_type:
- schema
ms.assetid: 4111afec-35e7-4c6f-b291-9bbba603f633
description: El elemento FractionalPageItemView describe dónde se inicia la vista paginada y el número máximo de elementos que se devuelven en una solicitud FindItem.
ms.openlocfilehash: cbf45838558873dc5846823c2d1b26cf2c8af514
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461313"
---
# <a name="fractionalpageitemview"></a><span data-ttu-id="c69aa-103">FractionalPageItemView</span><span class="sxs-lookup"><span data-stu-id="c69aa-103">FractionalPageItemView</span></span>

<span data-ttu-id="c69aa-104">El elemento **FractionalPageItemView** describe dónde se inicia la vista paginada y el número máximo de elementos que se devuelven en una solicitud [FindItem](finditem.md) .</span><span class="sxs-lookup"><span data-stu-id="c69aa-104">The **FractionalPageItemView** element describes where the paged view starts and the maximum number of items returned in a [FindItem](finditem.md) request.</span></span> 
  
[<span data-ttu-id="c69aa-105">FindItem</span><span class="sxs-lookup"><span data-stu-id="c69aa-105">FindItem</span></span>](finditem.md)
  
[<span data-ttu-id="c69aa-106">FractionalPageItemView</span><span class="sxs-lookup"><span data-stu-id="c69aa-106">FractionalPageItemView</span></span>](fractionalpageitemview.md)
  
```xml
<FractionalPageItemView MaxEntriesReturned="" Numerator="" Denominator=""/>
```

 <span data-ttu-id="c69aa-107">**FractionalPageViewType**</span><span class="sxs-lookup"><span data-stu-id="c69aa-107">**FractionalPageViewType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c69aa-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c69aa-108">Attributes and elements</span></span>

<span data-ttu-id="c69aa-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c69aa-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c69aa-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="c69aa-110">Attributes</span></span>

|<span data-ttu-id="c69aa-111">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="c69aa-111">**Attribute**</span></span>|<span data-ttu-id="c69aa-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c69aa-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c69aa-113">**MaxEntriesReturned**</span><span class="sxs-lookup"><span data-stu-id="c69aa-113">**MaxEntriesReturned**</span></span> <br/> |<span data-ttu-id="c69aa-114">Identifica el número máximo de resultados que se devolverá en la respuesta [FindItem](finditem.md) .</span><span class="sxs-lookup"><span data-stu-id="c69aa-114">Identifies the maximum number of results to return in the [FindItem](finditem.md) response.</span></span> <span data-ttu-id="c69aa-115">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="c69aa-115">This attribute is optional.</span></span> <span data-ttu-id="c69aa-116">Si no se especifica este atributo, la llamada devolverá todos los elementos disponibles.</span><span class="sxs-lookup"><span data-stu-id="c69aa-116">If this attribute is not specified, the call will return all available items.</span></span>  <br/> |
|<span data-ttu-id="c69aa-117">**Numera**</span><span class="sxs-lookup"><span data-stu-id="c69aa-117">**Numerator**</span></span> <br/> |<span data-ttu-id="c69aa-118">Representa el numerador del desplazamiento fraccionario desde el inicio del conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="c69aa-118">Represents the numerator of the fractional offset from the start of the result set.</span></span> <span data-ttu-id="c69aa-119">Este atributo es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c69aa-119">This attribute is required.</span></span> <span data-ttu-id="c69aa-120">El numerador debe ser igual o menor que el denominador.</span><span class="sxs-lookup"><span data-stu-id="c69aa-120">The numerator must be equal to or less than the denominator.</span></span> <span data-ttu-id="c69aa-121">Este atributo debe representar un valor integral que sea igual o mayor que cero.</span><span class="sxs-lookup"><span data-stu-id="c69aa-121">This attribute must represent an integral value that is equal to or greater than zero.</span></span>  <br/> <span data-ttu-id="c69aa-122">Para obtener más información, vea las notas más adelante en este tema.</span><span class="sxs-lookup"><span data-stu-id="c69aa-122">For more information, see Remarks later in this topic.</span></span>  <br/> |
|<span data-ttu-id="c69aa-123">**Denominador**</span><span class="sxs-lookup"><span data-stu-id="c69aa-123">**Denominator**</span></span> <br/> |<span data-ttu-id="c69aa-124">Representa el denominador del desplazamiento fraccionario desde el principio del número total de elementos del conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="c69aa-124">Represents the denominator of the fractional offset from the start of the total number of items in the result set.</span></span> <span data-ttu-id="c69aa-125">Este atributo es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c69aa-125">This attribute is required.</span></span> <span data-ttu-id="c69aa-126">Este atributo debe representar un valor integral que sea mayor que uno.</span><span class="sxs-lookup"><span data-stu-id="c69aa-126">This attribute must represent an integral value that is greater than one.</span></span>  <br/> <span data-ttu-id="c69aa-127">Para obtener más información, vea las notas más adelante en este tema.</span><span class="sxs-lookup"><span data-stu-id="c69aa-127">For more information, see Remarks later in this topic.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c69aa-128">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c69aa-128">Child elements</span></span>

<span data-ttu-id="c69aa-129">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c69aa-129">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c69aa-130">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c69aa-130">Parent elements</span></span>

|<span data-ttu-id="c69aa-131">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c69aa-131">**Element**</span></span>|<span data-ttu-id="c69aa-132">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c69aa-132">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c69aa-133">FindItem</span><span class="sxs-lookup"><span data-stu-id="c69aa-133">FindItem</span></span>](finditem.md) <br/> |<span data-ttu-id="c69aa-134">Define una solicitud para buscar elementos en un buzón.</span><span class="sxs-lookup"><span data-stu-id="c69aa-134">Defines a request to find items in a mailbox.</span></span>  <br/> <span data-ttu-id="c69aa-135">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="c69aa-135">The following is the XPath expression to this element:</span></span>  <br/>  `/FindItem` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c69aa-136">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c69aa-136">Remarks</span></span>

<span data-ttu-id="c69aa-137">El desplazamiento de la vista paginada desde el principio del conjunto de elementos encontrados se describe mediante una fracción.</span><span class="sxs-lookup"><span data-stu-id="c69aa-137">The paged view offset from the start of the set of found items is described by a fraction.</span></span> <span data-ttu-id="c69aa-138">La fracción, definida por los atributos **numerador** y **denominador** , describe dónde comienza la página de información.</span><span class="sxs-lookup"><span data-stu-id="c69aa-138">The fraction, which is defined by the **Numerator** and **Denominator** attributes, describes where the page of information starts.</span></span> <span data-ttu-id="c69aa-139">Por ejemplo, si el **numerador** es igual a cuatro y el **denominador** es cinco, la página de la información devuelta comienza en una entrada que se encuentra cuatro-quintos de la forma en el conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="c69aa-139">For example, if **Numerator** equals four and **Denominator** equals five, the page of returned information starts at an entry located four-fifths of the way in to the result set.</span></span> 
  
<span data-ttu-id="c69aa-140">Si la fracción da como resultado cero, indica el inicio del conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="c69aa-140">If the fraction evaluates to zero, that indicates the start of the results set.</span></span> <span data-ttu-id="c69aa-141">Si la fracción da como resultado una, que indica el final del conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="c69aa-141">If the fraction evaluates to one, that indicates the end of the result set.</span></span>
  
> [!NOTE]
> <span data-ttu-id="c69aa-142">La fracción representa el punto de inicio de la página, no el número de resultados que se devolverán en el conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="c69aa-142">The fraction represents the start point of page, not how many results in the result set will be returned.</span></span> 
  
<span data-ttu-id="c69aa-143">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="c69aa-143">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="c69aa-144">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c69aa-144">Example</span></span>

<span data-ttu-id="c69aa-145">En el ejemplo siguiente se muestra una solicitud [FindItem](finditem.md) .</span><span class="sxs-lookup"><span data-stu-id="c69aa-145">The following example shows a [FindItem](finditem.md) request.</span></span> <span data-ttu-id="c69aa-146">La solicitud devuelve elementos de los resultados de búsqueda que se inician después del segundo tercio de todos los elementos del conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="c69aa-146">The request returns items from the search results that start after the second third of all the items in the result set.</span></span> 
  
```
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindItem Traversal="Shallow" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject"/>
        </t:AdditionalProperties>
      </ItemShape>
      <FractionalPageItemView MaxEntriesReturned="12" Numerator="2" Denominator="3"/>
      <GroupBy Order="Descending">
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

<span data-ttu-id="c69aa-147">Por ejemplo, si el conjunto de resultados contiene nueve elementos, la vista paginada devolverá hasta 12 elementos, a partir del elemento encontrados dos tercios de la forma en el conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="c69aa-147">For example, if the result set contains nine items, the paged view will return up to 12 items, starting at the item found two-thirds of the way in to the result set.</span></span> <span data-ttu-id="c69aa-148">En este caso, la página comienza en el séptimo elemento.</span><span class="sxs-lookup"><span data-stu-id="c69aa-148">In this case, the page starts at the seventh item.</span></span> <span data-ttu-id="c69aa-149">La página contendrá el séptimo, octavo y noveno elemento.</span><span class="sxs-lookup"><span data-stu-id="c69aa-149">The page will contain the seventh, eighth, and ninth items.</span></span> <span data-ttu-id="c69aa-150">Si el numerador se establece en cero, la vista de página devolverá todos los elementos del conjunto de resultados siempre que el número sea menor que el atributo **MaxEntriesReturned** .</span><span class="sxs-lookup"><span data-stu-id="c69aa-150">If the numerator is set to zero, the page view will return all the items in the result set as long as the number is less than the **MaxEntriesReturned** attribute.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="c69aa-151">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c69aa-151">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c69aa-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="c69aa-152">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c69aa-153">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c69aa-153">Schema Name</span></span>  <br/> |<span data-ttu-id="c69aa-154">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="c69aa-154">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c69aa-155">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c69aa-155">Validation File</span></span>  <br/> |<span data-ttu-id="c69aa-156">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="c69aa-156">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c69aa-157">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c69aa-157">Can be Empty</span></span>  <br/> |<span data-ttu-id="c69aa-158">Falso</span><span class="sxs-lookup"><span data-stu-id="c69aa-158">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c69aa-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="c69aa-159">See also</span></span>



[<span data-ttu-id="c69aa-160">Operación FindItem</span><span class="sxs-lookup"><span data-stu-id="c69aa-160">FindItem operation</span></span>](finditem-operation.md)


[<span data-ttu-id="c69aa-161">Buscar elementos</span><span class="sxs-lookup"><span data-stu-id="c69aa-161">Finding Items</span></span>](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

