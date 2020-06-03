---
title: OccurrenceItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OccurrenceItemId
api_type:
- schema
ms.assetid: 4a15bbc3-5b93-4193-b9ec-da32f0a9a552
description: El elemento OccurrenceItemId identifica una única ocurrencia de un elemento periódico.
ms.openlocfilehash: 37c3a2442afb3302bca88ef0301e98013ff0319b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468379"
---
# <a name="occurrenceitemid"></a><span data-ttu-id="6f1b5-103">OccurrenceItemId</span><span class="sxs-lookup"><span data-stu-id="6f1b5-103">OccurrenceItemId</span></span>

<span data-ttu-id="6f1b5-104">El elemento **OccurrenceItemId** identifica una única ocurrencia de un elemento periódico.</span><span class="sxs-lookup"><span data-stu-id="6f1b5-104">The **OccurrenceItemId** element identifies a single occurrence of a recurring item.</span></span> 
  
```XML
<OccurrenceItemId RecurringMasterId="" ChangeKey="" InstanceIndex=""/>
```

<span data-ttu-id="6f1b5-105">**OccurrenceItemIdType**</span><span class="sxs-lookup"><span data-stu-id="6f1b5-105">**OccurrenceItemIdType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="6f1b5-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="6f1b5-106">Attributes and elements</span></span>

<span data-ttu-id="6f1b5-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="6f1b5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6f1b5-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="6f1b5-108">Attributes</span></span>

|<span data-ttu-id="6f1b5-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="6f1b5-109">**Attribute**</span></span>|<span data-ttu-id="6f1b5-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6f1b5-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6f1b5-111">**RecurringMasterId**</span><span class="sxs-lookup"><span data-stu-id="6f1b5-111">**RecurringMasterId**</span></span> <br/> |<span data-ttu-id="6f1b5-112">Identifica el maestro recurrente de un elemento periódico.</span><span class="sxs-lookup"><span data-stu-id="6f1b5-112">Identifies the recurring master of a recurring item.</span></span> <span data-ttu-id="6f1b5-113">Este atributo es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6f1b5-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="6f1b5-114">**ChangeKey**</span><span class="sxs-lookup"><span data-stu-id="6f1b5-114">**ChangeKey**</span></span> <br/> |<span data-ttu-id="6f1b5-115">Identifica una versión específica del maestro periódico o de una ocurrencia del elemento.</span><span class="sxs-lookup"><span data-stu-id="6f1b5-115">Identifies a specific version of the recurring master or an item occurrence.</span></span> <span data-ttu-id="6f1b5-116">Si el patrón recurrente o cualquiera de sus repeticiones cambia, el **changekey** cambia.</span><span class="sxs-lookup"><span data-stu-id="6f1b5-116">If either the recurring master or any of its occurrences change, the **ChangeKey** changes.</span></span> <span data-ttu-id="6f1b5-117">El **changekey** es el mismo para el maestro periódico y todas las repeticiones.</span><span class="sxs-lookup"><span data-stu-id="6f1b5-117">The **ChangeKey** is the same for the recurring master and all occurrences.</span></span>  <br/> |
|<span data-ttu-id="6f1b5-118">**InstanceIndex**</span><span class="sxs-lookup"><span data-stu-id="6f1b5-118">**InstanceIndex**</span></span> <br/> |<span data-ttu-id="6f1b5-119">Identifica el índice de la ocurrencia del elemento.</span><span class="sxs-lookup"><span data-stu-id="6f1b5-119">Identifies the index of the item occurrence.</span></span> <span data-ttu-id="6f1b5-120">Este atributo es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6f1b5-120">This attribute is required.</span></span> <span data-ttu-id="6f1b5-121">Este valor representa un número entero.</span><span class="sxs-lookup"><span data-stu-id="6f1b5-121">This value represents an integer.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="6f1b5-122">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6f1b5-122">Child elements</span></span>

<span data-ttu-id="6f1b5-123">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="6f1b5-123">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6f1b5-124">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6f1b5-124">Parent elements</span></span>

|<span data-ttu-id="6f1b5-125">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6f1b5-125">**Element**</span></span>|<span data-ttu-id="6f1b5-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6f1b5-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6f1b5-127">GlobalItemIds</span><span class="sxs-lookup"><span data-stu-id="6f1b5-127">GlobalItemIds</span></span>](globalitemids.md) <br/> |<span data-ttu-id="6f1b5-128">Contiene la colección de identificadores de elemento para todos los elementos de conversación en un buzón.</span><span class="sxs-lookup"><span data-stu-id="6f1b5-128">Contains the collection of item identifiers for all conversation items in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="6f1b5-129">ItemIds</span><span class="sxs-lookup"><span data-stu-id="6f1b5-129">ItemIds</span></span>](itemids.md) <br/> | <span data-ttu-id="6f1b5-130">Contiene las identidades únicas de los elementos, los elementos de ocurrencia y los elementos maestros periódicos que se usan para eliminar, enviar, obtener, mover o copiar elementos en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="6f1b5-130">Contains the unique identities of items, occurrence items, and recurring master items that are used to delete, send, get, move, or copy items in the Exchange store.</span></span> <br/><br/><span data-ttu-id="6f1b5-131">Las siguientes son las expresiones XPath de este elemento:</span><span class="sxs-lookup"><span data-stu-id="6f1b5-131">The following are the XPath expressions to this element:</span></span> <br/><br/>  `/DeleteItem/ItemIds` <br/>  `/SendItem/ItemIds` <br/>  `/GetItem/ItemIds` <br/><br/><span data-ttu-id="6f1b5-132">**Nota**: las operaciones [MoveItem](moveitem-operation.md) y [CopyItem](copyitem-operation.md) solo funcionan con elementos de calendario únicos y elementos de patrón periódicos.</span><span class="sxs-lookup"><span data-stu-id="6f1b5-132">**NOTE**: [MoveItem operation](moveitem-operation.md) and [CopyItem operation](copyitem-operation.md) only work with single calendar items and recurring master items.</span></span> <span data-ttu-id="6f1b5-133">Las repeticiones de elementos no son válidas con estas operaciones.</span><span class="sxs-lookup"><span data-stu-id="6f1b5-133">Item occurrences are invalid with these operations.</span></span>           |
|[<span data-ttu-id="6f1b5-134">ItemChange</span><span class="sxs-lookup"><span data-stu-id="6f1b5-134">ItemChange</span></span>](itemchange.md) <br/> |<span data-ttu-id="6f1b5-135">Contiene un identificador de elemento y las actualizaciones que se aplican al elemento.</span><span class="sxs-lookup"><span data-stu-id="6f1b5-135">Contains an item identifier and the updates to apply to the item.</span></span><br/><br/> <span data-ttu-id="6f1b5-136">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="6f1b5-136">The following is the XPath expression to this element:</span></span>  <br/>  `/UpdateItem/ItemChanges/ItemChange[i]` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6f1b5-137">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="6f1b5-137">Text value</span></span>

<span data-ttu-id="6f1b5-138">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="6f1b5-138">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6f1b5-139">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6f1b5-139">Remarks</span></span>

<span data-ttu-id="6f1b5-140">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="6f1b5-140">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="example"></a><span data-ttu-id="6f1b5-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6f1b5-141">Example</span></span>

<span data-ttu-id="6f1b5-142">En el ejemplo siguiente se identifica la cuarta ocurrencia de un elemento periódico que tiene la identidad 34vswe4.</span><span class="sxs-lookup"><span data-stu-id="6f1b5-142">The following example identifies the fourth occurrence of a recurring item that has the identity 34vswe4.</span></span>
  
```XML
<OccurrenceItemId RecurringMasterId="34vswe4" InstanceIndex="4" />
```

## <a name="element-information"></a><span data-ttu-id="6f1b5-143">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="6f1b5-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6f1b5-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="6f1b5-144">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6f1b5-145">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="6f1b5-145">Schema Name</span></span>  <br/> |<span data-ttu-id="6f1b5-146">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="6f1b5-146">Types schema</span></span>  <br/> |
|<span data-ttu-id="6f1b5-147">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="6f1b5-147">Validation File</span></span>  <br/> |<span data-ttu-id="6f1b5-148">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="6f1b5-148">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6f1b5-149">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="6f1b5-149">Can be Empty</span></span>  <br/> |<span data-ttu-id="6f1b5-150">Falso</span><span class="sxs-lookup"><span data-stu-id="6f1b5-150">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6f1b5-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="6f1b5-151">See also</span></span>

- [<span data-ttu-id="6f1b5-152">RecurringMasterItemId</span><span class="sxs-lookup"><span data-stu-id="6f1b5-152">RecurringMasterItemId</span></span>](recurringmasteritemid.md)
- [<span data-ttu-id="6f1b5-153">Operación FindConversation</span><span class="sxs-lookup"><span data-stu-id="6f1b5-153">FindConversation operation</span></span>](findconversation-operation.md)
- [<span data-ttu-id="6f1b5-154">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="6f1b5-154">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

