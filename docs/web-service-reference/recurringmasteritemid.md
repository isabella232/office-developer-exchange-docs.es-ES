---
title: RecurringMasterItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RecurringMasterItemId
api_type:
- schema
ms.assetid: 5800b58c-f3d7-4d8f-acc0-d13e02f4e258
description: El elemento RecurringMasterItemId identifica un elemento principal de periodicidad mediante la identificación de los identificadores de uno de los elementos de repeticiones relacionados.
ms.openlocfilehash: 896a9ce95d619e7bb44c8158288bc4f62ce417d9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529885"
---
# <a name="recurringmasteritemid"></a><span data-ttu-id="4c3cd-103">RecurringMasterItemId</span><span class="sxs-lookup"><span data-stu-id="4c3cd-103">RecurringMasterItemId</span></span>

<span data-ttu-id="4c3cd-104">El elemento **RecurringMasterItemId** identifica un elemento principal de periodicidad mediante la identificación de los identificadores de uno de los elementos de repeticiones relacionados.</span><span class="sxs-lookup"><span data-stu-id="4c3cd-104">The **RecurringMasterItemId** element identifies a recurrence master item by identifying the identifiers of one of its related occurrence items.</span></span> 
  
```XML
<RecurringMasterItemId OccurrenceId="" ChangeKey="" />
```

 <span data-ttu-id="4c3cd-105">**RecurringMasterItemIdType**</span><span class="sxs-lookup"><span data-stu-id="4c3cd-105">**RecurringMasterItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4c3cd-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="4c3cd-106">Attributes and elements</span></span>

<span data-ttu-id="4c3cd-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="4c3cd-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4c3cd-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="4c3cd-108">Attributes</span></span>

|<span data-ttu-id="4c3cd-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="4c3cd-109">**Attribute**</span></span>|<span data-ttu-id="4c3cd-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4c3cd-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4c3cd-111">**OccurrenceId**</span><span class="sxs-lookup"><span data-stu-id="4c3cd-111">**OccurrenceId**</span></span> <br/> |<span data-ttu-id="4c3cd-112">Identifica una única ocurrencia de un elemento maestro periódico.</span><span class="sxs-lookup"><span data-stu-id="4c3cd-112">Identifies a single occurrence of a recurring master item.</span></span> <span data-ttu-id="4c3cd-113">Este atributo es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4c3cd-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="4c3cd-114">**ChangeKey**</span><span class="sxs-lookup"><span data-stu-id="4c3cd-114">**ChangeKey**</span></span> <br/> |<span data-ttu-id="4c3cd-115">Identifica una versión específica de una ocurrencia única de un elemento maestro periódico.</span><span class="sxs-lookup"><span data-stu-id="4c3cd-115">Identifies a specific version of a single occurrence of a recurring master item.</span></span> <span data-ttu-id="4c3cd-116">Además, el elemento maestro periódico también se identifica porque éste y la única instancia contendrán la misma clave de cambio.</span><span class="sxs-lookup"><span data-stu-id="4c3cd-116">Additionally, the recurring master item is also identified because it and the single occurrence will contain the same change key.</span></span> <span data-ttu-id="4c3cd-117">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="4c3cd-117">This attribute is optional.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4c3cd-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4c3cd-118">Child elements</span></span>

<span data-ttu-id="4c3cd-119">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="4c3cd-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4c3cd-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="4c3cd-120">Parent elements</span></span>

|<span data-ttu-id="4c3cd-121">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="4c3cd-121">**Element**</span></span>|<span data-ttu-id="4c3cd-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4c3cd-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4c3cd-123">GlobalItemIds</span><span class="sxs-lookup"><span data-stu-id="4c3cd-123">GlobalItemIds</span></span>](globalitemids.md) <br/> |<span data-ttu-id="4c3cd-124">Contiene la colección de identificadores de elemento para todos los elementos de conversación en un buzón.</span><span class="sxs-lookup"><span data-stu-id="4c3cd-124">Contains the collection of item identifiers for all conversation items in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="4c3cd-125">ItemChange</span><span class="sxs-lookup"><span data-stu-id="4c3cd-125">ItemChange</span></span>](itemchange.md) <br/> |<span data-ttu-id="4c3cd-126">Contiene un identificador de elemento y las actualizaciones que se aplican al elemento.</span><span class="sxs-lookup"><span data-stu-id="4c3cd-126">Contains an item identifier and the updates to apply to the item.</span></span> <br/> <br/> <span data-ttu-id="4c3cd-127">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="4c3cd-127">The following is the XPath expression to this element:</span></span> <br/> <br/>  `/UpdateItem/ItemChanges/ItemChange[i]` <br/> |
|[<span data-ttu-id="4c3cd-128">ItemIds</span><span class="sxs-lookup"><span data-stu-id="4c3cd-128">ItemIds</span></span>](itemids.md) <br/> | <span data-ttu-id="4c3cd-129">Contiene las identidades únicas de los elementos, los elementos de ocurrencia y los elementos maestros periódicos que se usan para eliminar, enviar, obtener, mover o copiar elementos en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="4c3cd-129">Contains the unique identities of items, occurrence items, and recurring master items that are used to delete, send, get, move, or copy items in the Exchange store.</span></span> <br/> <br/>  <span data-ttu-id="4c3cd-130">Las siguientes son las expresiones XPath de este elemento:</span><span class="sxs-lookup"><span data-stu-id="4c3cd-130">The following are the XPath expressions to this element:</span></span>  <br/><br/>  `/DeleteItem/ItemIds` <br/>  `/SendItem/ItemIds` <br/>  `/GetItem/ItemIds` <br/>  `/MoveItem/ItemIds` <br/>  `/CopyItem//ItemIds` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4c3cd-131">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="4c3cd-131">Text value</span></span>

<span data-ttu-id="4c3cd-132">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4c3cd-132">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4c3cd-133">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4c3cd-133">Remarks</span></span>

<span data-ttu-id="4c3cd-134">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="4c3cd-134">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="example"></a><span data-ttu-id="4c3cd-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4c3cd-135">Example</span></span>

<span data-ttu-id="4c3cd-136">En el ejemplo siguiente se identifica el elemento maestro periódico mediante la identificación de una de sus repeticiones con el identificador 56lkjh6.</span><span class="sxs-lookup"><span data-stu-id="4c3cd-136">The following example identifies the recurring master item by identifying one of its occurrences with the identifier 56lkjh6.</span></span>
  
```XML
<RecurringMasterItemId OccurrenceId="56lkjh6" />
```

## <a name="element-information"></a><span data-ttu-id="4c3cd-137">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="4c3cd-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4c3cd-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="4c3cd-138">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4c3cd-139">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="4c3cd-139">Schema Name</span></span>  <br/> |<span data-ttu-id="4c3cd-140">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="4c3cd-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="4c3cd-141">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="4c3cd-141">Validation File</span></span>  <br/> |<span data-ttu-id="4c3cd-142">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="4c3cd-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4c3cd-143">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="4c3cd-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="4c3cd-144">Falso</span><span class="sxs-lookup"><span data-stu-id="4c3cd-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4c3cd-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="4c3cd-145">See also</span></span>

- [<span data-ttu-id="4c3cd-146">OccurrenceItemId</span><span class="sxs-lookup"><span data-stu-id="4c3cd-146">OccurrenceItemId</span></span>](occurrenceitemid.md)
- [<span data-ttu-id="4c3cd-147">Operación FindConversation</span><span class="sxs-lookup"><span data-stu-id="4c3cd-147">FindConversation operation</span></span>](findconversation-operation.md)

