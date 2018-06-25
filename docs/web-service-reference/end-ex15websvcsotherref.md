---
title: End
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- End
api_type:
- schema
ms.assetid: 72329821-32ff-495d-b6e5-fdc011003c2e
description: El elemento final representa el final de una duración.
ms.openlocfilehash: 90eea4fc545fae083e5675225665e517b502ba6f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764400"
---
# <a name="end"></a><span data-ttu-id="44f5c-103">End</span><span class="sxs-lookup"><span data-stu-id="44f5c-103">End</span></span>

<span data-ttu-id="44f5c-104">El elemento **final** representa el final de una duración.</span><span class="sxs-lookup"><span data-stu-id="44f5c-104">The **End** element represents the end of a duration.</span></span> 
  
```xml
<End/>
```

 <span data-ttu-id="44f5c-105">**DateTime**</span><span class="sxs-lookup"><span data-stu-id="44f5c-105">**DateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="44f5c-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="44f5c-106">Attributes and elements</span></span>

<span data-ttu-id="44f5c-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="44f5c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="44f5c-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="44f5c-108">Attributes</span></span>

<span data-ttu-id="44f5c-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="44f5c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="44f5c-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="44f5c-110">Child elements</span></span>

<span data-ttu-id="44f5c-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="44f5c-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="44f5c-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="44f5c-112">Parent elements</span></span>

|<span data-ttu-id="44f5c-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="44f5c-113">**Element**</span></span>|<span data-ttu-id="44f5c-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="44f5c-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="44f5c-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="44f5c-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="44f5c-116">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="44f5c-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="44f5c-117">FirstOccurrence</span><span class="sxs-lookup"><span data-stu-id="44f5c-117">FirstOccurrence</span></span>](firstoccurrence.md) <br/> |<span data-ttu-id="44f5c-118">Representa la primera aparición de un elemento periódico del calendario.</span><span class="sxs-lookup"><span data-stu-id="44f5c-118">Represents the first occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="44f5c-119">LastOccurrence</span><span class="sxs-lookup"><span data-stu-id="44f5c-119">LastOccurrence</span></span>](lastoccurrence.md) <br/> |<span data-ttu-id="44f5c-120">Representa la última aparición de un elemento periódico del calendario.</span><span class="sxs-lookup"><span data-stu-id="44f5c-120">Represents the last occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="44f5c-121">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="44f5c-121">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="44f5c-122">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="44f5c-122">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="44f5c-123">Repetición</span><span class="sxs-lookup"><span data-stu-id="44f5c-123">Occurrence</span></span>](occurrence.md) <br/> |<span data-ttu-id="44f5c-124">Representa una sola aparición de modificación de un elemento periódico del calendario.</span><span class="sxs-lookup"><span data-stu-id="44f5c-124">Represents a single modified occurrence of a recurring calendar item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="44f5c-125">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="44f5c-125">Text value</span></span>

<span data-ttu-id="44f5c-126">El valor de texto representa el final de una duración.</span><span class="sxs-lookup"><span data-stu-id="44f5c-126">The text value represents the end of a duration.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="44f5c-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="44f5c-127">Remarks</span></span>

<span data-ttu-id="44f5c-128">La operación UpdateItem puede establecer la hora de [Inicio](start.md) y **final** de un elemento del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="44f5c-128">The UpdateItem operation can set the [Start](start.md) and **End** time of an Exchange store item.</span></span> <span data-ttu-id="44f5c-129">En una solicitud UpdateItem, puede establecer la hora de [Inicio](start.md) sin establecer también la hora de **finalización** .</span><span class="sxs-lookup"><span data-stu-id="44f5c-129">In an UpdateItem request, you can set the [Start](start.md) time without also setting the **End** time.</span></span> <span data-ttu-id="44f5c-130">Esto puede producir un error si la hora de [Inicio](start.md) es posterior a la hora de **finalización** .</span><span class="sxs-lookup"><span data-stu-id="44f5c-130">This can cause an error if the [Start](start.md) time is later than the **End** time.</span></span> <span data-ttu-id="44f5c-131">Tenga en cuenta que las aplicaciones cliente deben realizar ajustes en la hora de **finalización** cuando se cambia la hora de [Inicio](start.md) con el fin de conservar la duración.</span><span class="sxs-lookup"><span data-stu-id="44f5c-131">Be aware that client applications must perform adjustments to the **End** time when that [Start](start.md) time is changed in order to preserve the duration.</span></span> 
  
 <span data-ttu-id="44f5c-132">**Nota** Si las fechas de [comienzo](start.md) y de **finalización** del elemento maestro periódico no tienen una fecha que es igual a la primera aparición de un patrón de periodicidad semanal, se pierde la información de desplazamiento de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="44f5c-132">**Note** The time zone offset information is lost if the [Start](start.md) and **End** dates of the recurring master item do not have a date that is equal to the first occurrence of a weekly recurrence pattern.</span></span> 
  
<span data-ttu-id="44f5c-133">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="44f5c-133">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="44f5c-134">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="44f5c-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="44f5c-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="44f5c-135">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="44f5c-136">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="44f5c-136">Schema Name</span></span>  <br/> |<span data-ttu-id="44f5c-137">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="44f5c-137">Types schema</span></span>  <br/> |
|<span data-ttu-id="44f5c-138">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="44f5c-138">Validation File</span></span>  <br/> |<span data-ttu-id="44f5c-139">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="44f5c-139">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="44f5c-140">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="44f5c-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="44f5c-141">False</span><span class="sxs-lookup"><span data-stu-id="44f5c-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="44f5c-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="44f5c-142">See also</span></span>



[<span data-ttu-id="44f5c-143">WeeklyRecurrence</span><span class="sxs-lookup"><span data-stu-id="44f5c-143">WeeklyRecurrence</span></span>](weeklyrecurrence.md)
  
 <span data-ttu-id="44f5c-144">**End**</span><span class="sxs-lookup"><span data-stu-id="44f5c-144">**End**</span></span>


- [<span data-ttu-id="44f5c-145">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="44f5c-145">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

