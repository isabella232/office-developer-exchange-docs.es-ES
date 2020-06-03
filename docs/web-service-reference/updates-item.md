---
title: Actualizaciones (elemento)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Updates
api_type:
- schema
ms.assetid: 5c1a855e-390d-4713-9d10-6e86ca392814
description: El elemento updates contiene un conjunto de elementos que definen los cambios de las propiedades de elemento de anexión, establecimiento y eliminación.
ms.openlocfilehash: 6902ea4d3d3d9adc074745d5642cdfa6d91a9163
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456356"
---
# <a name="updates-item"></a><span data-ttu-id="fbd7c-103">Actualizaciones (elemento)</span><span class="sxs-lookup"><span data-stu-id="fbd7c-103">Updates (Item)</span></span>

<span data-ttu-id="fbd7c-104">El elemento **updates** contiene un conjunto de elementos que definen los cambios de las propiedades de elemento de anexión, establecimiento y eliminación.</span><span class="sxs-lookup"><span data-stu-id="fbd7c-104">The **Updates** element contains a set of elements that define append, set, and delete changes to item properties.</span></span> 
  
- [<span data-ttu-id="fbd7c-105">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="fbd7c-105">UpdateItem</span></span>](updateitem.md)
  
- [<span data-ttu-id="fbd7c-106">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="fbd7c-106">ItemChanges</span></span>](itemchanges.md)
  
- [<span data-ttu-id="fbd7c-107">ItemChange</span><span class="sxs-lookup"><span data-stu-id="fbd7c-107">ItemChange</span></span>](itemchange.md)
  
- [<span data-ttu-id="fbd7c-108">Actualizaciones (elemento)</span><span class="sxs-lookup"><span data-stu-id="fbd7c-108">Updates (Item)</span></span>](updates-item.md)
  
```xml
<Updates>
   <AppendToItemField/>
   <SetItemField/>
   <DeleteItemField/>
</Updates>
```

<span data-ttu-id="fbd7c-109">**NonEmptyArrayOfItemChangeDescriptionsType**</span><span class="sxs-lookup"><span data-stu-id="fbd7c-109">**NonEmptyArrayOfItemChangeDescriptionsType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="fbd7c-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="fbd7c-110">Attributes and elements</span></span>

<span data-ttu-id="fbd7c-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="fbd7c-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fbd7c-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="fbd7c-112">Attributes</span></span>

<span data-ttu-id="fbd7c-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="fbd7c-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fbd7c-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="fbd7c-114">Child elements</span></span>

|<span data-ttu-id="fbd7c-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="fbd7c-115">**Element**</span></span>|<span data-ttu-id="fbd7c-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fbd7c-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fbd7c-117">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="fbd7c-117">AppendToItemField</span></span>](appendtoitemfield.md) <br/> |<span data-ttu-id="fbd7c-118">Representa los datos que se van a anexar a una propiedad única de un elemento durante una [operación UpdateItem](updateitem-operation.md).</span><span class="sxs-lookup"><span data-stu-id="fbd7c-118">Represents data to append to a single property of an item during an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="fbd7c-119">SetItemField</span><span class="sxs-lookup"><span data-stu-id="fbd7c-119">SetItemField</span></span>](setitemfield.md) <br/> |<span data-ttu-id="fbd7c-120">Representa una actualización de una propiedad única de un elemento en una [operación UpdateItem](updateitem-operation.md).</span><span class="sxs-lookup"><span data-stu-id="fbd7c-120">Represents an update to a single property of an item in an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="fbd7c-121">DeleteItemField</span><span class="sxs-lookup"><span data-stu-id="fbd7c-121">DeleteItemField</span></span>](deleteitemfield.md) <br/> |<span data-ttu-id="fbd7c-122">Representa una operación para eliminar una propiedad determinada de un elemento durante una [operación UpdateItem](updateitem-operation.md).</span><span class="sxs-lookup"><span data-stu-id="fbd7c-122">Represents an operation to delete a given property from an item during an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="fbd7c-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="fbd7c-123">Parent elements</span></span>

|<span data-ttu-id="fbd7c-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="fbd7c-124">**Element**</span></span>|<span data-ttu-id="fbd7c-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fbd7c-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fbd7c-126">ItemChange</span><span class="sxs-lookup"><span data-stu-id="fbd7c-126">ItemChange</span></span>](itemchange.md) <br/> |<span data-ttu-id="fbd7c-127">Contiene un identificador de elemento y las actualizaciones que se aplican al elemento.</span><span class="sxs-lookup"><span data-stu-id="fbd7c-127">Contains an item identifier and the updates to apply to the item.</span></span>  <br/> <span data-ttu-id="fbd7c-128">La siguiente es la expresión XPath a este elemento:`/UpdateItem/ItemChanges/ItemChange[i]`</span><span class="sxs-lookup"><span data-stu-id="fbd7c-128">The following is the XPath expression to this element:  `/UpdateItem/ItemChanges/ItemChange[i]`</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fbd7c-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fbd7c-129">Remarks</span></span>

<span data-ttu-id="fbd7c-130">Las actualizaciones que se definen mediante este elemento se realizan en el elemento identificado por los elementos [Itemid](itemid.md), [OccurrenceItemId](occurrenceitemid.md)o [RecurringMasterItemId](recurringmasteritemid.md) .</span><span class="sxs-lookup"><span data-stu-id="fbd7c-130">The updates that are defined by this element are performed on the item that is identified by the [ItemId](itemid.md), [OccurrenceItemId](occurrenceitemid.md), or [RecurringMasterItemId](recurringmasteritemid.md) elements.</span></span> 
  
<span data-ttu-id="fbd7c-131">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="fbd7c-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fbd7c-132">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="fbd7c-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fbd7c-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="fbd7c-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fbd7c-134">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="fbd7c-134">Schema Name</span></span>  <br/> |<span data-ttu-id="fbd7c-135">esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="fbd7c-135">types schema</span></span>  <br/> |
|<span data-ttu-id="fbd7c-136">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="fbd7c-136">Validation File</span></span>  <br/> |<span data-ttu-id="fbd7c-137">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="fbd7c-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="fbd7c-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="fbd7c-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="fbd7c-139">Falso</span><span class="sxs-lookup"><span data-stu-id="fbd7c-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fbd7c-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="fbd7c-140">See also</span></span>

- [<span data-ttu-id="fbd7c-141">Operación UpdateItem</span><span class="sxs-lookup"><span data-stu-id="fbd7c-141">UpdateItem operation</span></span>](updateitem-operation.md)
- [<span data-ttu-id="fbd7c-142">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="fbd7c-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

