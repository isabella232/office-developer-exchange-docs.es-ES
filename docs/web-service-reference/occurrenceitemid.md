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
description: El elemento OccurrenceItemId identifica una sola aparición de un elemento periódico.
ms.openlocfilehash: 073639ecbca6ffda872e9253b7c7e44c3541f13b
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353465"
---
# <a name="occurrenceitemid"></a><span data-ttu-id="edbf0-103">OccurrenceItemId</span><span class="sxs-lookup"><span data-stu-id="edbf0-103">OccurrenceItemId</span></span>

<span data-ttu-id="edbf0-104">El elemento **OccurrenceItemId** identifica una sola aparición de un elemento periódico.</span><span class="sxs-lookup"><span data-stu-id="edbf0-104">The **OccurrenceItemId** element identifies a single occurrence of a recurring item.</span></span> 
  
```XML
<OccurrenceItemId RecurringMasterId="" ChangeKey="" InstanceIndex=""/>
```

<span data-ttu-id="edbf0-105">**OccurrenceItemIdType**</span><span class="sxs-lookup"><span data-stu-id="edbf0-105">**OccurrenceItemIdType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="edbf0-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="edbf0-106">Attributes and elements</span></span>

<span data-ttu-id="edbf0-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="edbf0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="edbf0-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="edbf0-108">Attributes</span></span>

|<span data-ttu-id="edbf0-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="edbf0-109">**Attribute**</span></span>|<span data-ttu-id="edbf0-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="edbf0-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="edbf0-111">**RecurringMasterId**</span><span class="sxs-lookup"><span data-stu-id="edbf0-111">**RecurringMasterId**</span></span> <br/> |<span data-ttu-id="edbf0-112">Identifica al patrón periódico de un elemento periódico.</span><span class="sxs-lookup"><span data-stu-id="edbf0-112">Identifies the recurring master of a recurring item.</span></span> <span data-ttu-id="edbf0-113">Este atributo es necesario.</span><span class="sxs-lookup"><span data-stu-id="edbf0-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="edbf0-114">**ChangeKey**</span><span class="sxs-lookup"><span data-stu-id="edbf0-114">**ChangeKey**</span></span> <br/> |<span data-ttu-id="edbf0-115">Identifica una versión específica del patrón periódico o una ocurrencia del elemento.</span><span class="sxs-lookup"><span data-stu-id="edbf0-115">Identifies a specific version of the recurring master or an item occurrence.</span></span> <span data-ttu-id="edbf0-116">Si cambia el patrón periódico o cualquiera de sus apariciones, cambia el **ChangeKey** .</span><span class="sxs-lookup"><span data-stu-id="edbf0-116">If either the recurring master or any of its occurrences change, the **ChangeKey** changes.</span></span> <span data-ttu-id="edbf0-117">El **ChangeKey** es el mismo para el patrón de periódico y todas las apariciones.</span><span class="sxs-lookup"><span data-stu-id="edbf0-117">The **ChangeKey** is the same for the recurring master and all occurrences.</span></span>  <br/> |
|<span data-ttu-id="edbf0-118">**InstanceIndex**</span><span class="sxs-lookup"><span data-stu-id="edbf0-118">**InstanceIndex**</span></span> <br/> |<span data-ttu-id="edbf0-119">Identifica el índice de la aparición de elemento.</span><span class="sxs-lookup"><span data-stu-id="edbf0-119">Identifies the index of the item occurrence.</span></span> <span data-ttu-id="edbf0-120">Este atributo es necesario.</span><span class="sxs-lookup"><span data-stu-id="edbf0-120">This attribute is required.</span></span> <span data-ttu-id="edbf0-121">Este valor representa un número entero.</span><span class="sxs-lookup"><span data-stu-id="edbf0-121">This value represents an integer.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="edbf0-122">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="edbf0-122">Child elements</span></span>

<span data-ttu-id="edbf0-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="edbf0-123">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="edbf0-124">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="edbf0-124">Parent elements</span></span>

|<span data-ttu-id="edbf0-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="edbf0-125">**Element**</span></span>|<span data-ttu-id="edbf0-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="edbf0-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="edbf0-127">GlobalItemIds</span><span class="sxs-lookup"><span data-stu-id="edbf0-127">GlobalItemIds</span></span>](globalitemids.md) <br/> |<span data-ttu-id="edbf0-128">Contiene la colección de identificadores de elemento para todos los elementos de la conversación en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="edbf0-128">Contains the collection of item identifiers for all conversation items in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="edbf0-129">ItemIds</span><span class="sxs-lookup"><span data-stu-id="edbf0-129">ItemIds</span></span>](itemids.md) <br/> | <span data-ttu-id="edbf0-130">Contiene las identidades únicas de los elementos, elementos de aparición y elementos maestros periódicos que se usan para eliminar, enviar, obtener, mover o copiar elementos en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="edbf0-130">Contains the unique identities of items, occurrence items, and recurring master items that are used to delete, send, get, move, or copy items in the Exchange store.</span></span> <br/><br/><span data-ttu-id="edbf0-131">Los siguientes son las expresiones de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="edbf0-131">The following are the XPath expressions to this element:</span></span> <br/><br/>  `/DeleteItem/ItemIds` <br/>  `/SendItem/ItemIds` <br/>  `/GetItem/ItemIds` <br/><br/><span data-ttu-id="edbf0-132">**Nota**: [operación de MoveItem](moveitem-operation.md) y [CopyItem](copyitem-operation.md) sólo funcionan con elementos de calendario único y elementos maestros periódicos.</span><span class="sxs-lookup"><span data-stu-id="edbf0-132">**NOTE**: [MoveItem operation](moveitem-operation.md) and [CopyItem operation](copyitem-operation.md) only work with single calendar items and recurring master items.</span></span> <span data-ttu-id="edbf0-133">Repeticiones de elemento no son válidas con estas operaciones.</span><span class="sxs-lookup"><span data-stu-id="edbf0-133">Item occurrences are invalid with these operations.</span></span>           |
|[<span data-ttu-id="edbf0-134">ItemChange</span><span class="sxs-lookup"><span data-stu-id="edbf0-134">ItemChange</span></span>](itemchange.md) <br/> |<span data-ttu-id="edbf0-135">Contiene un identificador de elemento y las actualizaciones que se debe aplicar al elemento.</span><span class="sxs-lookup"><span data-stu-id="edbf0-135">Contains an item identifier and the updates to apply to the item.</span></span><br/><br/> <span data-ttu-id="edbf0-136">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="edbf0-136">The following is the XPath expression to this element:</span></span>  <br/>  `/UpdateItem/ItemChanges/ItemChange[i]` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="edbf0-137">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="edbf0-137">Text value</span></span>

<span data-ttu-id="edbf0-138">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="edbf0-138">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="edbf0-139">Comentarios</span><span class="sxs-lookup"><span data-stu-id="edbf0-139">Remarks</span></span>

<span data-ttu-id="edbf0-140">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="edbf0-140">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="example"></a><span data-ttu-id="edbf0-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="edbf0-141">Example</span></span>

<span data-ttu-id="edbf0-142">En el ejemplo siguiente se identifica la aparición de un elemento periódico que tiene la identidad 34vswe4 cuarto.</span><span class="sxs-lookup"><span data-stu-id="edbf0-142">The following example identifies the fourth occurrence of a recurring item that has the identity 34vswe4.</span></span>
  
```XML
<OccurrenceItemId RecurringMasterId="34vswe4" InstanceIndex="4" />
```

## <a name="element-information"></a><span data-ttu-id="edbf0-143">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="edbf0-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="edbf0-144">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="edbf0-144">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="edbf0-145">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="edbf0-145">Schema Name</span></span>  <br/> |<span data-ttu-id="edbf0-146">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="edbf0-146">Types schema</span></span>  <br/> |
|<span data-ttu-id="edbf0-147">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="edbf0-147">Validation File</span></span>  <br/> |<span data-ttu-id="edbf0-148">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="edbf0-148">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="edbf0-149">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="edbf0-149">Can be Empty</span></span>  <br/> |<span data-ttu-id="edbf0-150">False</span><span class="sxs-lookup"><span data-stu-id="edbf0-150">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="edbf0-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="edbf0-151">See also</span></span>

- [<span data-ttu-id="edbf0-152">RecurringMasterItemId</span><span class="sxs-lookup"><span data-stu-id="edbf0-152">RecurringMasterItemId</span></span>](recurringmasteritemid.md)
- [<span data-ttu-id="edbf0-153">Operación FindConversation</span><span class="sxs-lookup"><span data-stu-id="edbf0-153">FindConversation operation</span></span>](findconversation-operation.md)
- [<span data-ttu-id="edbf0-154">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="edbf0-154">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

