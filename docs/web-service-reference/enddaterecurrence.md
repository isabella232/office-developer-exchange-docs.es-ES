---
title: EndDateRecurrence
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- EndDateRecurrence
api_type:
- schema
ms.assetid: a5ee2504-db84-49ee-870c-cca9269f2e26
description: El elemento EndDateRecurrence describe la fecha de inicio y la fecha de finalización de un patrón de periodicidad de elemento.
ms.openlocfilehash: 73450bf69c6b122e806d85011975159e348ad740
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764408"
---
# <a name="enddaterecurrence"></a><span data-ttu-id="6286a-103">EndDateRecurrence</span><span class="sxs-lookup"><span data-stu-id="6286a-103">EndDateRecurrence</span></span>

<span data-ttu-id="6286a-104">El elemento **EndDateRecurrence** describe la fecha de inicio y la fecha de finalización de un patrón de periodicidad de elemento.</span><span class="sxs-lookup"><span data-stu-id="6286a-104">The **EndDateRecurrence** element describes the start date and the end date of an item recurrence pattern.</span></span> 
  
```xml
<EndDateRecurrence>
   <StartDate/>
   <EndDate/>
</EndDateRecurrence>
```

 <span data-ttu-id="6286a-105">**EndDateRecurrenceRangeType**</span><span class="sxs-lookup"><span data-stu-id="6286a-105">**EndDateRecurrenceRangeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6286a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="6286a-106">Attributes and elements</span></span>

<span data-ttu-id="6286a-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="6286a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6286a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="6286a-108">Attributes</span></span>

<span data-ttu-id="6286a-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="6286a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6286a-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6286a-110">Child elements</span></span>

|<span data-ttu-id="6286a-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="6286a-111">**Element**</span></span>|<span data-ttu-id="6286a-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6286a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6286a-113">StartDate (periodicidad)</span><span class="sxs-lookup"><span data-stu-id="6286a-113">StartDate (Recurrence)</span></span>](startdate-recurrence.md) <br/> |<span data-ttu-id="6286a-114">Representa la fecha de comienzo de una tarea periódica o elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="6286a-114">Represents the start date of a recurring task or calendar item.</span></span>  <br/> |
|[<span data-ttu-id="6286a-115">EndDate (periodicidad)</span><span class="sxs-lookup"><span data-stu-id="6286a-115">EndDate (Recurrence)</span></span>](enddate-recurrence.md) <br/> |<span data-ttu-id="6286a-116">Representa la fecha de finalización de una tarea periódica o elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="6286a-116">Represents the end date of a recurring task or calendar item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6286a-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6286a-117">Parent elements</span></span>

|<span data-ttu-id="6286a-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="6286a-118">**Element**</span></span>|<span data-ttu-id="6286a-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6286a-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6286a-120">Periodicidad (RecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="6286a-120">Recurrence (RecurrenceType)</span></span>](recurrence-recurrencetype.md) <br/> |<span data-ttu-id="6286a-121">Contiene el patrón de periodicidad para los elementos de calendario y las convocatorias de reunión.</span><span class="sxs-lookup"><span data-stu-id="6286a-121">Contains the recurrence pattern for calendar items and meeting requests.</span></span>  <br/> |
|[<span data-ttu-id="6286a-122">Periodicidad (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="6286a-122">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="6286a-123">Contiene el patrón de periodicidad para las tareas repetitivas.</span><span class="sxs-lookup"><span data-stu-id="6286a-123">Contains the recurrence pattern for recurring tasks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6286a-124">Notas</span><span class="sxs-lookup"><span data-stu-id="6286a-124">Remarks</span></span>

<span data-ttu-id="6286a-125">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="6286a-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6286a-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="6286a-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6286a-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6286a-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6286a-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="6286a-128">Schema name</span></span>  <br/> |<span data-ttu-id="6286a-129">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="6286a-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="6286a-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="6286a-130">Validation file</span></span>  <br/> |<span data-ttu-id="6286a-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6286a-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6286a-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="6286a-132">Can be empty</span></span>  <br/> |<span data-ttu-id="6286a-133">False</span><span class="sxs-lookup"><span data-stu-id="6286a-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6286a-134">Ver también</span><span class="sxs-lookup"><span data-stu-id="6286a-134">See also</span></span>



- [<span data-ttu-id="6286a-135">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="6286a-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

