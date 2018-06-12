---
title: ModifiedOccurrences
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ModifiedOccurrences
api_type:
- schema
ms.assetid: 552932fc-b3b4-486e-8d73-32c0bb10bd68
description: El elemento ModifiedOccurrences contiene una matriz de periódica repeticiones del elemento de calendario que se han modificado para que sean diferentes que el elemento de patrón de periodicidad.
ms.openlocfilehash: 53f60740bcaa2de6713e1b6a3d2874153285645a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836472"
---
# <a name="modifiedoccurrences"></a><span data-ttu-id="27193-103">ModifiedOccurrences</span><span class="sxs-lookup"><span data-stu-id="27193-103">ModifiedOccurrences</span></span>

<span data-ttu-id="27193-104">El elemento **ModifiedOccurrences** contiene una matriz de periódica repeticiones del elemento de calendario que se han modificado para que sean diferentes que el elemento de patrón de periodicidad.</span><span class="sxs-lookup"><span data-stu-id="27193-104">The **ModifiedOccurrences** element contains an array of recurring calendar item occurrences that have been modified so that they are different than the recurrence master item.</span></span> 
  
```xml
<ModifiedOccurrences>
   <Occurrence/>
</ModifiedOccurrences>
```

 <span data-ttu-id="27193-105">**NonEmptyArrayOfOccurrenceInfoType**</span><span class="sxs-lookup"><span data-stu-id="27193-105">**NonEmptyArrayOfOccurrenceInfoType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="27193-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="27193-106">Attributes and elements</span></span>

<span data-ttu-id="27193-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="27193-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="27193-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="27193-108">Attributes</span></span>

<span data-ttu-id="27193-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="27193-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="27193-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="27193-110">Child elements</span></span>

|<span data-ttu-id="27193-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="27193-111">**Element**</span></span>|<span data-ttu-id="27193-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="27193-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="27193-113">Repetición</span><span class="sxs-lookup"><span data-stu-id="27193-113">Occurrence</span></span>](occurrence.md) <br/> |<span data-ttu-id="27193-114">Representa una sola aparición de modificación de un elemento periódico del calendario.</span><span class="sxs-lookup"><span data-stu-id="27193-114">Represents a single modified occurrence of a recurring calendar item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="27193-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="27193-115">Parent elements</span></span>

|<span data-ttu-id="27193-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="27193-116">**Element**</span></span>|<span data-ttu-id="27193-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="27193-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="27193-118">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="27193-118">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="27193-119">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="27193-119">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="27193-120">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="27193-120">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="27193-121">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="27193-121">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="27193-122">Notas</span><span class="sxs-lookup"><span data-stu-id="27193-122">Remarks</span></span>

<span data-ttu-id="27193-123">Este elemento es válida si [CalendarItemType](calendaritemtype.md) tiene el valor RecurringMaster.</span><span class="sxs-lookup"><span data-stu-id="27193-123">This element is valid if [CalendarItemType](calendaritemtype.md) has the RecurringMaster value.</span></span> 
  
<span data-ttu-id="27193-124">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="27193-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="27193-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="27193-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="27193-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="27193-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="27193-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="27193-127">Schema name</span></span>  <br/> |<span data-ttu-id="27193-128">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="27193-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="27193-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="27193-129">Validation file</span></span>  <br/> |<span data-ttu-id="27193-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="27193-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="27193-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="27193-131">Can be empty</span></span>  <br/> |<span data-ttu-id="27193-132">False</span><span class="sxs-lookup"><span data-stu-id="27193-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="27193-133">Ver también</span><span class="sxs-lookup"><span data-stu-id="27193-133">See also</span></span>



- [<span data-ttu-id="27193-134">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="27193-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

