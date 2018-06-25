---
title: NumberedRecurrence
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- NumberedRecurrence
api_type:
- schema
ms.assetid: 53746909-ef21-4764-8715-a7769b943cca
description: El elemento NumberedRecurrence describe la fecha de inicio y el número de repeticiones de un elemento periódico.
ms.openlocfilehash: 01fbf831fa7ff378221d4db3d873af730ac564d8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836628"
---
# <a name="numberedrecurrence"></a><span data-ttu-id="c8848-103">NumberedRecurrence</span><span class="sxs-lookup"><span data-stu-id="c8848-103">NumberedRecurrence</span></span>

<span data-ttu-id="c8848-104">El elemento **NumberedRecurrence** describe la fecha de inicio y el número de repeticiones de un elemento periódico.</span><span class="sxs-lookup"><span data-stu-id="c8848-104">The **NumberedRecurrence** element describes the start date and the number of occurrences of a recurring item.</span></span> 
  
```xml
<NumberedRecurrence>
   <StartDate/>
   <NumberOfOccurrences/>
</NumberedRecurrence>
```

 <span data-ttu-id="c8848-105">**NumberedRecurrenceRangeType**</span><span class="sxs-lookup"><span data-stu-id="c8848-105">**NumberedRecurrenceRangeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c8848-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c8848-106">Attributes and elements</span></span>

<span data-ttu-id="c8848-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c8848-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c8848-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c8848-108">Attributes</span></span>

<span data-ttu-id="c8848-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c8848-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c8848-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c8848-110">Child elements</span></span>

|<span data-ttu-id="c8848-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="c8848-111">**Element**</span></span>|<span data-ttu-id="c8848-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c8848-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c8848-113">StartDate (periodicidad)</span><span class="sxs-lookup"><span data-stu-id="c8848-113">StartDate (Recurrence)</span></span>](startdate-recurrence.md) <br/> |<span data-ttu-id="c8848-114">Representa la fecha de comienzo de una tarea periódica o elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="c8848-114">Represents the start date of a recurring task or calendar item.</span></span>  <br/> |
|[<span data-ttu-id="c8848-115">NumberOfOccurrences</span><span class="sxs-lookup"><span data-stu-id="c8848-115">NumberOfOccurrences</span></span>](numberofoccurrences.md) <br/> |<span data-ttu-id="c8848-116">Contiene el número de repeticiones de un elemento periódico.</span><span class="sxs-lookup"><span data-stu-id="c8848-116">Contains the number of occurrences of a recurring item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c8848-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c8848-117">Parent elements</span></span>

|<span data-ttu-id="c8848-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="c8848-118">**Element**</span></span>|<span data-ttu-id="c8848-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c8848-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c8848-120">Periodicidad (RecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="c8848-120">Recurrence (RecurrenceType)</span></span>](recurrence-recurrencetype.md) <br/> |<span data-ttu-id="c8848-121">Contiene el patrón de periodicidad para los elementos de calendario y las convocatorias de reunión.</span><span class="sxs-lookup"><span data-stu-id="c8848-121">Contains the recurrence pattern for calendar items and meeting requests.</span></span>  <br/> |
|[<span data-ttu-id="c8848-122">Periodicidad (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="c8848-122">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="c8848-123">Contiene información sobre la periodicidad para las tareas repetitivas.</span><span class="sxs-lookup"><span data-stu-id="c8848-123">Contains recurrence information for recurring tasks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c8848-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c8848-124">Remarks</span></span>

<span data-ttu-id="c8848-125">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="c8848-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c8848-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c8848-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c8848-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c8848-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c8848-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c8848-128">Schema name</span></span>  <br/> |<span data-ttu-id="c8848-129">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="c8848-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="c8848-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c8848-130">Validation file</span></span>  <br/> |<span data-ttu-id="c8848-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c8848-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c8848-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c8848-132">Can be empty</span></span>  <br/> |<span data-ttu-id="c8848-133">False</span><span class="sxs-lookup"><span data-stu-id="c8848-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c8848-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="c8848-134">See also</span></span>



- [<span data-ttu-id="c8848-135">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="c8848-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

