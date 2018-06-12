---
title: LastOccurrence
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- LastOccurrence
api_type:
- schema
ms.assetid: c9ef0fcb-4265-4e60-9986-fff0f211d00b
description: El elemento LastOccurrence representa la última aparición de un elemento periódico del calendario.
ms.openlocfilehash: 2c8fdfc0005e86c9dda84a48ae1d3692b5134ca8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836209"
---
# <a name="lastoccurrence"></a><span data-ttu-id="8ec74-103">LastOccurrence</span><span class="sxs-lookup"><span data-stu-id="8ec74-103">LastOccurrence</span></span>

<span data-ttu-id="8ec74-104">El elemento **LastOccurrence** representa la última aparición de un elemento periódico del calendario.</span><span class="sxs-lookup"><span data-stu-id="8ec74-104">The **LastOccurrence** element represents the last occurrence of a recurring calendar item.</span></span> 
  
```xml
<LastOccurrence>
   <ItemId/>
   <Start/>
   <End/>
   <OriginalStart/>
</LastOccurrence>
```

 <span data-ttu-id="8ec74-105">**OccurrenceInfoType**</span><span class="sxs-lookup"><span data-stu-id="8ec74-105">**OccurrenceInfoType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8ec74-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="8ec74-106">Attributes and elements</span></span>

<span data-ttu-id="8ec74-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="8ec74-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8ec74-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="8ec74-108">Attributes</span></span>

<span data-ttu-id="8ec74-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="8ec74-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8ec74-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8ec74-110">Child elements</span></span>

|<span data-ttu-id="8ec74-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="8ec74-111">**Element**</span></span>|<span data-ttu-id="8ec74-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8ec74-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8ec74-113">ItemId</span><span class="sxs-lookup"><span data-stu-id="8ec74-113">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="8ec74-114">Contiene la clave única de identificador y el cambio de la última aparición de un elemento periódico del calendario.</span><span class="sxs-lookup"><span data-stu-id="8ec74-114">Contains the unique identifier and change key of the last occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="8ec74-115">Start</span><span class="sxs-lookup"><span data-stu-id="8ec74-115">Start</span></span>](start.md) <br/> |<span data-ttu-id="8ec74-116">Representa la hora de inicio de la última aparición de un elemento periódico del calendario.</span><span class="sxs-lookup"><span data-stu-id="8ec74-116">Represents the start time of the last occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="8ec74-117">End</span><span class="sxs-lookup"><span data-stu-id="8ec74-117">End </span></span>](end-ex15websvcsotherref.md) <br/> |<span data-ttu-id="8ec74-118">Representa la hora de finalización de la última aparición de un elemento periódico del calendario.</span><span class="sxs-lookup"><span data-stu-id="8ec74-118">Represents the end time of the last occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="8ec74-119">OriginalStart</span><span class="sxs-lookup"><span data-stu-id="8ec74-119">OriginalStart</span></span>](originalstart.md) <br/> |<span data-ttu-id="8ec74-120">Representa la hora de inicio original de la última aparición de un elemento periódico del calendario.</span><span class="sxs-lookup"><span data-stu-id="8ec74-120">Represents the original start time of the last occurrence of a recurring calendar item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8ec74-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="8ec74-121">Parent elements</span></span>

|<span data-ttu-id="8ec74-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="8ec74-122">**Element**</span></span>|<span data-ttu-id="8ec74-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8ec74-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8ec74-124">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="8ec74-124">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="8ec74-125">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="8ec74-125">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="8ec74-126">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="8ec74-126">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="8ec74-127">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="8ec74-127">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8ec74-128">Notas</span><span class="sxs-lookup"><span data-stu-id="8ec74-128">Remarks</span></span>

<span data-ttu-id="8ec74-129">Este elemento es válida si [CalendarItemType](calendaritemtype.md) tiene el valor RecurringMaster.</span><span class="sxs-lookup"><span data-stu-id="8ec74-129">This element is valid if [CalendarItemType](calendaritemtype.md) has the RecurringMaster value.</span></span> 
  
<span data-ttu-id="8ec74-130">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="8ec74-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8ec74-131">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="8ec74-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8ec74-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8ec74-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8ec74-133">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="8ec74-133">Schema name</span></span>  <br/> |<span data-ttu-id="8ec74-134">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="8ec74-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="8ec74-135">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="8ec74-135">Validation file</span></span>  <br/> |<span data-ttu-id="8ec74-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="8ec74-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8ec74-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="8ec74-137">Can be empty</span></span>  <br/> |<span data-ttu-id="8ec74-138">False</span><span class="sxs-lookup"><span data-stu-id="8ec74-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8ec74-139">Ver también</span><span class="sxs-lookup"><span data-stu-id="8ec74-139">See also</span></span>



- [<span data-ttu-id="8ec74-140">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="8ec74-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
  
[<span data-ttu-id="8ec74-141">Referencia EWS para Exchange</span><span class="sxs-lookup"><span data-stu-id="8ec74-141">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)

