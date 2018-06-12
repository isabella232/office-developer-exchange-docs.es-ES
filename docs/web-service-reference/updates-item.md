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
description: El elemento de actualizaciones contiene un conjunto de elementos que definen append, establecer y eliminar los cambios realizados en las propiedades de elementos.
ms.openlocfilehash: 13df458c783b942e1c868853c41b6247119cf123
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840866"
---
# <a name="updates-item"></a><span data-ttu-id="3f3b7-103">Actualizaciones (elemento)</span><span class="sxs-lookup"><span data-stu-id="3f3b7-103">Updates (Item)</span></span>

<span data-ttu-id="3f3b7-104">El elemento de **actualizaciones** contiene un conjunto de elementos que definen append, establecer y eliminar los cambios realizados en las propiedades de elementos.</span><span class="sxs-lookup"><span data-stu-id="3f3b7-104">The **Updates** element contains a set of elements that define append, set, and delete changes to item properties.</span></span> 
  
- [<span data-ttu-id="3f3b7-105">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="3f3b7-105">UpdateItem</span></span>](updateitem.md)
  
- [<span data-ttu-id="3f3b7-106">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="3f3b7-106">ItemChanges</span></span>](itemchanges.md)
  
- [<span data-ttu-id="3f3b7-107">ItemChange</span><span class="sxs-lookup"><span data-stu-id="3f3b7-107">ItemChange</span></span>](itemchange.md)
  
- [<span data-ttu-id="3f3b7-108">Actualizaciones (elemento)</span><span class="sxs-lookup"><span data-stu-id="3f3b7-108">Updates (Item)</span></span>](updates-item.md)
  
```xml
<Updates>
   <AppendToItemField/>
   <SetItemField/>
   <DeleteItemField/>
</Updates>
```

<span data-ttu-id="3f3b7-109">**NonEmptyArrayOfItemChangeDescriptionsType**</span><span class="sxs-lookup"><span data-stu-id="3f3b7-109">**NonEmptyArrayOfItemChangeDescriptionsType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="3f3b7-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3f3b7-110">Attributes and elements</span></span>

<span data-ttu-id="3f3b7-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3f3b7-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3f3b7-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="3f3b7-112">Attributes</span></span>

<span data-ttu-id="3f3b7-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3f3b7-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3f3b7-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3f3b7-114">Child elements</span></span>

|<span data-ttu-id="3f3b7-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="3f3b7-115">**Element**</span></span>|<span data-ttu-id="3f3b7-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3f3b7-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3f3b7-117">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="3f3b7-117">AppendToItemField</span></span>](appendtoitemfield.md) <br/> |<span data-ttu-id="3f3b7-118">Representa los datos que se anexará a una sola propiedad de un elemento durante una [operación de UpdateItem](updateitem-operation.md).</span><span class="sxs-lookup"><span data-stu-id="3f3b7-118">Represents data to append to a single property of an item during an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="3f3b7-119">SetItemField</span><span class="sxs-lookup"><span data-stu-id="3f3b7-119">SetItemField</span></span>](setitemfield.md) <br/> |<span data-ttu-id="3f3b7-120">Representa una actualización para una única propiedad de un elemento en una [operación de UpdateItem](updateitem-operation.md).</span><span class="sxs-lookup"><span data-stu-id="3f3b7-120">Represents an update to a single property of an item in an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="3f3b7-121">DeleteItemField</span><span class="sxs-lookup"><span data-stu-id="3f3b7-121">DeleteItemField</span></span>](deleteitemfield.md) <br/> |<span data-ttu-id="3f3b7-122">Representa una operación para eliminar una propiedad determinada de un elemento durante una [operación de UpdateItem](updateitem-operation.md).</span><span class="sxs-lookup"><span data-stu-id="3f3b7-122">Represents an operation to delete a given property from an item during an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3f3b7-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3f3b7-123">Parent elements</span></span>

|<span data-ttu-id="3f3b7-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="3f3b7-124">**Element**</span></span>|<span data-ttu-id="3f3b7-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3f3b7-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3f3b7-126">ItemChange</span><span class="sxs-lookup"><span data-stu-id="3f3b7-126">ItemChange</span></span>](itemchange.md) <br/> |<span data-ttu-id="3f3b7-127">Contiene un identificador de elemento y las actualizaciones que se debe aplicar al elemento.</span><span class="sxs-lookup"><span data-stu-id="3f3b7-127">Contains an item identifier and the updates to apply to the item.</span></span>  <br/> <span data-ttu-id="3f3b7-128">La siguiente es la expresión de XPath para este elemento:`/UpdateItem/ItemChanges/ItemChange[i]`</span><span class="sxs-lookup"><span data-stu-id="3f3b7-128">The following is the XPath expression to this element:  `/UpdateItem/ItemChanges/ItemChange[i]`</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3f3b7-129">Notas</span><span class="sxs-lookup"><span data-stu-id="3f3b7-129">Remarks</span></span>

<span data-ttu-id="3f3b7-130">Las actualizaciones que se definen mediante este elemento se realizan en el elemento que se identifica con los elementos [ItemId](itemid.md), [OccurrenceItemId](occurrenceitemid.md)o [RecurringMasterItemId](recurringmasteritemid.md) .</span><span class="sxs-lookup"><span data-stu-id="3f3b7-130">The updates that are defined by this element are performed on the item that is identified by the [ItemId](itemid.md), [OccurrenceItemId](occurrenceitemid.md), or [RecurringMasterItemId](recurringmasteritemid.md) elements.</span></span> 
  
<span data-ttu-id="3f3b7-131">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="3f3b7-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3f3b7-132">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3f3b7-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3f3b7-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3f3b7-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3f3b7-134">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3f3b7-134">Schema Name</span></span>  <br/> |<span data-ttu-id="3f3b7-135">esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="3f3b7-135">types schema</span></span>  <br/> |
|<span data-ttu-id="3f3b7-136">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3f3b7-136">Validation File</span></span>  <br/> |<span data-ttu-id="3f3b7-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3f3b7-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3f3b7-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3f3b7-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="3f3b7-139">False</span><span class="sxs-lookup"><span data-stu-id="3f3b7-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3f3b7-140">Ver también</span><span class="sxs-lookup"><span data-stu-id="3f3b7-140">See also</span></span>

- [<span data-ttu-id="3f3b7-141">Operación UpdateItem</span><span class="sxs-lookup"><span data-stu-id="3f3b7-141">UpdateItem operation</span></span>](updateitem-operation.md)
- [<span data-ttu-id="3f3b7-142">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="3f3b7-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

