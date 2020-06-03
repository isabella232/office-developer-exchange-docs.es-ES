---
title: ItemChange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ItemChange
api_type:
- schema
ms.assetid: 5cb43b02-d444-4d9c-9075-cdc5a4427daf
description: El elemento ItemChange contiene un identificador de elemento y las actualizaciones que se aplican al elemento.
ms.openlocfilehash: 916ef1ba2c7a709ec1fd80ababd72999506773c4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459920"
---
# <a name="itemchange"></a><span data-ttu-id="be00a-103">ItemChange</span><span class="sxs-lookup"><span data-stu-id="be00a-103">ItemChange</span></span>

<span data-ttu-id="be00a-104">El elemento **ItemChange** contiene un identificador de elemento y las actualizaciones que se aplican al elemento.</span><span class="sxs-lookup"><span data-stu-id="be00a-104">The **ItemChange** element contains an item identifier and the updates to apply to the item.</span></span> 
  
- [<span data-ttu-id="be00a-105">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="be00a-105">UpdateItem</span></span>](updateitem.md) 
- [<span data-ttu-id="be00a-106">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="be00a-106">ItemChanges</span></span>](itemchanges.md)
- [<span data-ttu-id="be00a-107">ItemChange</span><span class="sxs-lookup"><span data-stu-id="be00a-107">ItemChange</span></span>](itemchange.md)
  
```xml
<ItemChange>
   <ItemId/>
   <Updates>...</Updates>
</ItemChange>
```

```xml
<ItemChange>
   <OccurrenceItemId>...</OccurrenceItemId>
   <Updates>...</Updates>
</ItemChange>
```

```xml
<ItemChange>
   <RecurringMasterItemId>...</RecurringMasterItemId>
   <Updates>...</Updates>
</ItemChange>
```

<span data-ttu-id="be00a-108">**ItemChangeType**</span><span class="sxs-lookup"><span data-stu-id="be00a-108">**ItemChangeType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="be00a-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="be00a-109">Attributes and elements</span></span>

<span data-ttu-id="be00a-110">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="be00a-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="be00a-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="be00a-111">Attributes</span></span>

<span data-ttu-id="be00a-112">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="be00a-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="be00a-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="be00a-113">Child elements</span></span>

|<span data-ttu-id="be00a-114">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="be00a-114">**Element**</span></span>|<span data-ttu-id="be00a-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="be00a-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="be00a-116">ItemId</span><span class="sxs-lookup"><span data-stu-id="be00a-116">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="be00a-117">Contiene el identificador único y la clave de cambio de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="be00a-117">Contains the unique identifier and change key of an item in the Exchange store.</span></span> <span data-ttu-id="be00a-118">Este elemento es obligatorio si no se usa el elemento [OccurrenceItemId](occurrenceitemid.md) o [RecurringMasterItemId](recurringmasteritemid.md) .</span><span class="sxs-lookup"><span data-stu-id="be00a-118">This element is required if the [OccurrenceItemId](occurrenceitemid.md) or [RecurringMasterItemId](recurringmasteritemid.md) element is not used.</span></span>  <br/> |
|[<span data-ttu-id="be00a-119">OccurrenceItemId</span><span class="sxs-lookup"><span data-stu-id="be00a-119">OccurrenceItemId</span></span>](occurrenceitemid.md) <br/> |<span data-ttu-id="be00a-120">Identifica una única ocurrencia de un elemento periódico.</span><span class="sxs-lookup"><span data-stu-id="be00a-120">Identifies a single occurrence of a recurring item.</span></span> <span data-ttu-id="be00a-121">Este elemento es obligatorio si se usa.</span><span class="sxs-lookup"><span data-stu-id="be00a-121">This element is required if used.</span></span> <span data-ttu-id="be00a-122">Este elemento es obligatorio si no se usa el elemento [RecurringMasterItemId](recurringmasteritemid.md) o [Itemid](itemid.md) .</span><span class="sxs-lookup"><span data-stu-id="be00a-122">This element is required if the [RecurringMasterItemId](recurringmasteritemid.md) or [ItemId](itemid.md) element is not used.</span></span>  <br/> |
|[<span data-ttu-id="be00a-123">RecurringMasterItemId</span><span class="sxs-lookup"><span data-stu-id="be00a-123">RecurringMasterItemId</span></span>](recurringmasteritemid.md) <br/> |<span data-ttu-id="be00a-124">Identifica un elemento principal de periodicidad mediante la identificación de uno de los identificadores de elementos de ocurrencia relacionados.</span><span class="sxs-lookup"><span data-stu-id="be00a-124">Identifies a recurrence master item by identifying one of its related occurrence items' identifiers.</span></span> <span data-ttu-id="be00a-125">Este elemento es obligatorio si se usa.</span><span class="sxs-lookup"><span data-stu-id="be00a-125">This element is required if used.</span></span> <span data-ttu-id="be00a-126">Este elemento es obligatorio si no se usa el elemento [OccurrenceItemId](occurrenceitemid.md) o [Itemid](itemid.md) .</span><span class="sxs-lookup"><span data-stu-id="be00a-126">This element is required if the [OccurrenceItemId](occurrenceitemid.md) or [ItemId](itemid.md) element is not used.</span></span>  <br/> |
|[<span data-ttu-id="be00a-127">Actualizaciones (elemento)</span><span class="sxs-lookup"><span data-stu-id="be00a-127">Updates (Item)</span></span>](updates-item.md) <br/> |<span data-ttu-id="be00a-128">Contiene una matriz que define los cambios de anexión, establecimiento y eliminación en las propiedades de elemento.</span><span class="sxs-lookup"><span data-stu-id="be00a-128">Contains an array that defines append, set, and delete changes to item properties.</span></span> <span data-ttu-id="be00a-129">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="be00a-129">This element is required.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="be00a-130">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="be00a-130">Parent elements</span></span>

|<span data-ttu-id="be00a-131">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="be00a-131">**Element**</span></span>|<span data-ttu-id="be00a-132">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="be00a-132">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="be00a-133">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="be00a-133">ItemChanges</span></span>](itemchanges.md) <br/> |<span data-ttu-id="be00a-134">Contiene una matriz de elementos [ItemChange](itemchange.md) que identifican los elementos y las actualizaciones que se aplican a los elementos.</span><span class="sxs-lookup"><span data-stu-id="be00a-134">Contains an array of [ItemChange](itemchange.md) elements that identify items and the updates to apply to the items.</span></span>  <br/> <span data-ttu-id="be00a-135">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="be00a-135">The following is the XPath expression to this element:</span></span>  <br/>  `/UpdateItem/ItemChanges` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="be00a-136">Comentarios</span><span class="sxs-lookup"><span data-stu-id="be00a-136">Remarks</span></span>

<span data-ttu-id="be00a-137">Solo se puede usar un elemento [Itemid](itemid.md), [OccurrenceItemId](occurrenceitemid.md)o [RecurringMasterItemId](recurringmasteritemid.md) en un elemento **ItemChange** .</span><span class="sxs-lookup"><span data-stu-id="be00a-137">Only a single [ItemId](itemid.md), [OccurrenceItemId](occurrenceitemid.md), or [RecurringMasterItemId](recurringmasteritemid.md) element can be used in an **ItemChange** element.</span></span> 
  
<span data-ttu-id="be00a-138">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="be00a-138">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="be00a-139">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="be00a-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="be00a-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="be00a-140">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="be00a-141">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="be00a-141">Schema Name</span></span>  <br/> |<span data-ttu-id="be00a-142">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="be00a-142">Types schema</span></span>  <br/> |
|<span data-ttu-id="be00a-143">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="be00a-143">Validation File</span></span>  <br/> |<span data-ttu-id="be00a-144">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="be00a-144">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="be00a-145">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="be00a-145">Can be Empty</span></span>  <br/> |<span data-ttu-id="be00a-146">Falso</span><span class="sxs-lookup"><span data-stu-id="be00a-146">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="be00a-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="be00a-147">See also</span></span>

- [<span data-ttu-id="be00a-148">Operación UpdateItem</span><span class="sxs-lookup"><span data-stu-id="be00a-148">UpdateItem operation</span></span>](updateitem-operation.md)

