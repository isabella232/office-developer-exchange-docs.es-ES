---
title: AggregateOn
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AggregateOn
api_type:
- schema
ms.assetid: 9b0a03f2-3282-46e1-b1a0-cbb9a0fbe9bb
description: El elemento AggregateOn representa la propiedad que se usa para determinar el orden de los elementos agrupados de un conjunto de resultados FindItem agrupados.
ms.openlocfilehash: 04359c187ef11538d64f8f0d3ea2fe84bc3d048b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463569"
---
# <a name="aggregateon"></a><span data-ttu-id="95502-103">AggregateOn</span><span class="sxs-lookup"><span data-stu-id="95502-103">AggregateOn</span></span>

<span data-ttu-id="95502-104">El elemento **AggregateOn** representa la propiedad que se usa para determinar el orden de los elementos agrupados de un conjunto de resultados FindItem agrupados.</span><span class="sxs-lookup"><span data-stu-id="95502-104">The **AggregateOn** element represents the property that is used to determine the order of grouped items for a grouped FindItem result set.</span></span> 
  
- [<span data-ttu-id="95502-105">FindItem</span><span class="sxs-lookup"><span data-stu-id="95502-105">FindItem</span></span>](finditem.md)  
- [<span data-ttu-id="95502-106">GroupBy</span><span class="sxs-lookup"><span data-stu-id="95502-106">GroupBy</span></span>](groupby.md)
- [<span data-ttu-id="95502-107">AggregateOn</span><span class="sxs-lookup"><span data-stu-id="95502-107">AggregateOn</span></span>](aggregateon.md)
  
```xml
<AggregateOn>
   <FieldURI/>
</AggregateOn>
```

```xml
<AggregateOn>
   <IndexedFieldURI/>
</AggregateOn>
```

```xml
<AggregateOn>
   <ExtendedFieldURI/>
</AggregateOn>
```
 
<span data-ttu-id="95502-108">**AggregateOnType**</span><span class="sxs-lookup"><span data-stu-id="95502-108">**AggregateOnType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="95502-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="95502-109">Attributes and elements</span></span>

<span data-ttu-id="95502-110">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="95502-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="95502-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="95502-111">Attributes</span></span>

|<span data-ttu-id="95502-112">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="95502-112">**Attribute**</span></span>|<span data-ttu-id="95502-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="95502-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="95502-114">**Aggregate**</span><span class="sxs-lookup"><span data-stu-id="95502-114">**Aggregate**</span></span> <br/> | <span data-ttu-id="95502-115">Indica el valor máximo o mínimo de la propiedad identificada por el elemento [FieldURI](fielduri.md) que se usa para ordenar los grupos de elementos.</span><span class="sxs-lookup"><span data-stu-id="95502-115">Indicates the maximum or minimum value of the property identified by the [FieldURI](fielduri.md) element that is used for ordering the groups of items.</span></span><br/><br/><span data-ttu-id="95502-116">Los valores posibles son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="95502-116">The following are the possible values:</span></span>  <br/><br/><span data-ttu-id="95502-117">-Mínimo</span><span class="sxs-lookup"><span data-stu-id="95502-117">- Minimum</span></span>  <br/><span data-ttu-id="95502-118">-Máximo</span><span class="sxs-lookup"><span data-stu-id="95502-118">- Maximum</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="95502-119">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="95502-119">Child elements</span></span>

|<span data-ttu-id="95502-120">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="95502-120">**Element**</span></span>|<span data-ttu-id="95502-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="95502-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="95502-122">FieldURI</span><span class="sxs-lookup"><span data-stu-id="95502-122">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="95502-123">Identifica las propiedades a las que se hace referencia con frecuencia mediante el URI.</span><span class="sxs-lookup"><span data-stu-id="95502-123">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="95502-124">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="95502-124">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="95502-125">Identifica a los miembros individuales de un diccionario.</span><span class="sxs-lookup"><span data-stu-id="95502-125">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="95502-126">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="95502-126">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="95502-127">Identifica las propiedades MAPI extendidas para obtener, establecer o crear.</span><span class="sxs-lookup"><span data-stu-id="95502-127">Identifies extended MAPI properties to get, set, or create.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="95502-128">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="95502-128">Parent elements</span></span>

|<span data-ttu-id="95502-129">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="95502-129">**Element**</span></span>|<span data-ttu-id="95502-130">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="95502-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="95502-131">GroupBy</span><span class="sxs-lookup"><span data-stu-id="95502-131">GroupBy</span></span>](groupby.md) <br/> |<span data-ttu-id="95502-132">Especifica agrupaciones arbitrarias para consultas FindItem.</span><span class="sxs-lookup"><span data-stu-id="95502-132">Specifies arbitrary groupings for FindItem queries.</span></span>  <br/> <span data-ttu-id="95502-133">La siguiente es la expresión XPath a este elemento:`/FindItem/GroupBy`</span><span class="sxs-lookup"><span data-stu-id="95502-133">The following is the XPath expression to this element:  `/FindItem/GroupBy`</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="95502-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="95502-134">Remarks</span></span>

<span data-ttu-id="95502-135">La [operación FindItem](finditem-operation.md) puede devolver resultados agrupados.</span><span class="sxs-lookup"><span data-stu-id="95502-135">The [FindItem operation](finditem-operation.md) can return grouped results.</span></span> <span data-ttu-id="95502-136">Dentro de los resultados agrupados, todos los elementos que tienen el mismo valor para una determinada propiedad de agrupación se reúnen y presentan como elementos secundarios de ese grupo.</span><span class="sxs-lookup"><span data-stu-id="95502-136">Within grouped results, all items that have the same value for a given grouping property are gathered together and presented as children of that group.</span></span> <span data-ttu-id="95502-137">Por ejemplo, si agrupa por remitente, todos los mensajes de correo electrónico se organizan en grupos separados en función de si son del remitente A, del remitente B, etc.</span><span class="sxs-lookup"><span data-stu-id="95502-137">For example, if you group by sender, all e-mails are organized into separate groups based on whether they are from sender A, sender B, and so on.</span></span> <span data-ttu-id="95502-138">Estos grupos son elementos secundarios del grupo de remitentes.</span><span class="sxs-lookup"><span data-stu-id="95502-138">These groups are children of the sender group.</span></span> 
  
<span data-ttu-id="95502-139">Cada uno de los grupos dentro del grupo de remitentes contiene una colección de elementos, como los correos electrónicos reales que provienen de cada remitente.</span><span class="sxs-lookup"><span data-stu-id="95502-139">Each of the groups within the sender group contains a collection of items, such as the actual e-mails that came from each sender.</span></span> <span data-ttu-id="95502-140">Puede usar el elemento [SortOrder](sortorder.md) para ordenar los elementos dentro de un grupo.</span><span class="sxs-lookup"><span data-stu-id="95502-140">You can use the [SortOrder](sortorder.md) element to sort the items within a group.</span></span> <span data-ttu-id="95502-141">Sin embargo, para ordenar los grupos según los valores de propiedad de un elemento, debe usar agregación.</span><span class="sxs-lookup"><span data-stu-id="95502-141">To sort the groups based on an item's property values, however, you must use aggregation.</span></span> 
  
<span data-ttu-id="95502-142">Con agregación, el orden de los grupos se basa en una propiedad específica de los elementos dentro del grupo.</span><span class="sxs-lookup"><span data-stu-id="95502-142">With aggregation, the order of groups is based on a specific property of the items within the group.</span></span> <span data-ttu-id="95502-143">Cuando se usa la agregación para ordenar elementos dentro de un grupo, se debe identificar una propiedad representativa mediante la que se ordenan los grupos.</span><span class="sxs-lookup"><span data-stu-id="95502-143">When you use aggregation to sort items within a group, you must identify a representative property by which to sort the groups.</span></span> <span data-ttu-id="95502-144">Puede usar el elemento **AggregateOn** para especificar la propiedad Representative.</span><span class="sxs-lookup"><span data-stu-id="95502-144">You can use the **AggregateOn** element to specify the representative property.</span></span> 
  
<span data-ttu-id="95502-145">Cuando se identifica una propiedad representativa, se utiliza el atributo **Aggregate** para indicar si los grupos se ordenan según el valor máximo o mínimo de la propiedad identificada.</span><span class="sxs-lookup"><span data-stu-id="95502-145">When a representative property is identified, the **Aggregate** attribute is used to indicate whether the groups are sorted according to the maximum or the minimum value of the identified property.</span></span> <span data-ttu-id="95502-146">Si el atributo **Aggregate** se establece en Maximum, los grupos se ordenan comenzando por el valor mayor de la propiedad **AggregateOn** .</span><span class="sxs-lookup"><span data-stu-id="95502-146">If the **Aggregate** attribute is set to Maximum, the groups are sorted beginning with the largest value for the **AggregateOn** property.</span></span> <span data-ttu-id="95502-147">Si el atributo **Aggregate** se establece en Minimum, los grupos se ordenan comenzando por el valor menor de la propiedad **AggregateOn** .</span><span class="sxs-lookup"><span data-stu-id="95502-147">If the **Aggregate** attribute is set to Minimum, the groups are sorted beginning with the smallest value for the **AggregateOn** property.</span></span> 
  
<span data-ttu-id="95502-148">Por ejemplo, si desea emitir una consulta agrupada de FindItem, agrupando por remitente, pero desea ordenar los grupos para que el grupo con el mensaje de correo electrónico más reciente esté en la parte superior, puede agrupar por remitente y agregado por fecha y hora recibidas con un atributo **agregado** de máximo.</span><span class="sxs-lookup"><span data-stu-id="95502-148">For example, if you want to issue a FindItem grouped query, grouping by sender, but you want to order the groups so that the group with the most recent e-mail message is on top, you can group by sender and aggregate on date/time received with an **Aggregate** attribute of Maximum.</span></span> 
  
<span data-ttu-id="95502-149">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="95502-149">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="95502-150">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="95502-150">Example</span></span>

<span data-ttu-id="95502-151">En el siguiente ejemplo se muestra una solicitud FindItem y una respuesta agrupadas.</span><span class="sxs-lookup"><span data-stu-id="95502-151">The following example shows a grouped FindItem request and response.</span></span> <span data-ttu-id="95502-152">En el ejemplo se muestra una solicitud para devolver los elementos agrupados por la propiedad **ConversationTopic** .</span><span class="sxs-lookup"><span data-stu-id="95502-152">The example shows a request to return items grouped by the **ConversationTopic** property.</span></span> <span data-ttu-id="95502-153">Dos grupos, A y B, se devuelven en orden descendente según el valor máximo de la propiedad [DateTimeReceived](datetimereceived.md) .</span><span class="sxs-lookup"><span data-stu-id="95502-153">Two groups, A and B, are returned in descending order based on the maximum value of the [DateTimeReceived](datetimereceived.md) property.</span></span> 
  
```XML
<!-- EXAMPLE REQUEST -->
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                Traversal="Shallow">
      <ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="message:ConversationTopic"/>
          <t:FieldURI FieldURI="item:DateTimeReceived"/>
        </t:AdditionalProperties>    
      </ItemShape>
      <IndexedPageItemView BasePoint="Beginning" MaxEntriesReturned="20" Offset="0"/>
      <GroupBy Order="Ascending">
        <t:FieldURI FieldURI="message:ConversationTopic"/>
        <t:AggregateOn Aggregate="Maximum">
          <t:FieldURI FieldURI="item:DateTimeReceived"/>
        </t:AggregateOn>
      </GroupBy>
      <ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox"/>
      </ParentFolderIds>
    </FindItem>
  </soap:Body>
</soap:Envelope>
<!-- EXAMPLE RESPONSE -->
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="652" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="8" TotalItemsInView="8" IncludesLastItemInRange="true">
            <t:Groups>
              <t:GroupedItems>
                <t:GroupIndex>B</t:GroupIndex>
                <t:Items>
                  <t:Message>
                    <t:ItemId Id="AQAnAH=" ChangeKey="CQAAABY" />
                    <t:DateTimeReceived>2006-09-14T23:59:18Z</t:DateTimeReceived>
                    <t:ConversationTopic>B</t:ConversationTopic>
                  </t:Message>
                  <t:Message>
                    <t:ItemId Id="AQAnAHR=" ChangeKey="CQAAAw" />
                    <t:DateTimeReceived>2006-09-15T00:00:24Z</t:DateTimeReceived>
                    <t:ConversationTopic>B</t:ConversationTopic>
                  </t:Message>
                  <t:Message>
                    <t:ItemId Id="AQAnA==" ChangeKey="CQAAJXT" />
                    <t:DateTimeReceived>2006-09-15T00:22:45Z</t:DateTimeReceived>
                    <t:ConversationTopic>B</t:ConversationTopic>
                  </t:Message>
                </t:Items>
              </t:GroupedItems>
              <t:GroupedItems>
                <t:GroupIndex>A</t:GroupIndex>
                <t:Items>
                  <t:Message>
                    <t:ItemId Id="AQAnAAA==" ChangeKey="CQCJNe" />
                    <t:DateTimeReceived>2006-09-14T23:56:12Z</t:DateTimeReceived>
                    <t:ConversationTopic>A</t:ConversationTopic>
                  </t:Message>
                  <t:Message>
                    <t:ItemId Id="AQWgAA==" ChangeKey="CQAACJV6" />
                    <t:DateTimeReceived>2006-09-14T23:57:33Z</t:DateTimeReceived>
                    <t:ConversationTopic>A</t:ConversationTopic>
                  </t:Message>
                  <t:Message>
                    <t:ItemId Id="AAAA==" ChangeKey="CQA6CJXw" />
                    <t:DateTimeReceived>2006-09-15T00:23:31Z</t:DateTimeReceived>
                    <t:ConversationTopic>A</t:ConversationTopic>
                  </t:Message>
                </t:Items>
              </t:GroupedItems>
            </t:Groups>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </FindItemResponse>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="95502-154">Para ordenar los elementos de un grupo, use el elemento [SortOrder](sortorder.md) .</span><span class="sxs-lookup"><span data-stu-id="95502-154">To sort the items in a group, use the [SortOrder](sortorder.md) element.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="95502-155">Los identificadores de elemento y las claves de cambio se han abreviado para preservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="95502-155">The item identifiers and change keys have been shortened to preserve readability.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="95502-156">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="95502-156">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="95502-157">Namespace</span><span class="sxs-lookup"><span data-stu-id="95502-157">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="95502-158">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="95502-158">Schema Name</span></span>  <br/> |<span data-ttu-id="95502-159">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="95502-159">Types schema</span></span>  <br/> |
|<span data-ttu-id="95502-160">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="95502-160">Validation File</span></span>  <br/> |<span data-ttu-id="95502-161">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="95502-161">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="95502-162">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="95502-162">Can be Empty</span></span>  <br/> |<span data-ttu-id="95502-163">Falso</span><span class="sxs-lookup"><span data-stu-id="95502-163">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="95502-164">Vea también</span><span class="sxs-lookup"><span data-stu-id="95502-164">See also</span></span>

- [<span data-ttu-id="95502-165">Operación FindItem</span><span class="sxs-lookup"><span data-stu-id="95502-165">FindItem operation</span></span>](finditem-operation.md)
- [<span data-ttu-id="95502-166">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="95502-166">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="95502-167">Buscar elementos</span><span class="sxs-lookup"><span data-stu-id="95502-167">Finding Items</span></span>](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

