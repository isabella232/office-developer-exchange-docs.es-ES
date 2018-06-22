---
title: DailyRecurrence
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DailyRecurrence
api_type:
- schema
ms.assetid: 0aaf265d-b723-49c6-8e9c-9ba60141e9ab
description: El elemento DailyRecurrence describe la frecuencia, en días, en el que se repite un elemento de calendario o una tarea.
ms.openlocfilehash: d02c1f7425372d60c10b40527dc5f0d65f923b45
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764016"
---
# <a name="dailyrecurrence"></a><span data-ttu-id="3f1b4-103">DailyRecurrence</span><span class="sxs-lookup"><span data-stu-id="3f1b4-103">DailyRecurrence</span></span>

<span data-ttu-id="3f1b4-104">El elemento **DailyRecurrence** describe la frecuencia, en días, en el que se repite un elemento de calendario o una tarea.</span><span class="sxs-lookup"><span data-stu-id="3f1b4-104">The **DailyRecurrence** element describes the frequency, in days, in which a calendar item or a task recurs.</span></span> 
  
```xml
<DailyRecurrence>
   <Interval/>
</DailyRecurrence>
```

<span data-ttu-id="3f1b4-105">**DailyRecurrencePatternType**</span><span class="sxs-lookup"><span data-stu-id="3f1b4-105">**DailyRecurrencePatternType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="3f1b4-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3f1b4-106">Attributes and elements</span></span>

<span data-ttu-id="3f1b4-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3f1b4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3f1b4-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="3f1b4-108">Attributes</span></span>

<span data-ttu-id="3f1b4-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3f1b4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3f1b4-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3f1b4-110">Child elements</span></span>

|<span data-ttu-id="3f1b4-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="3f1b4-111">**Element**</span></span>|<span data-ttu-id="3f1b4-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3f1b4-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3f1b4-113">Interval</span><span class="sxs-lookup"><span data-stu-id="3f1b4-113">Interval</span></span>](interval.md) <br/> |<span data-ttu-id="3f1b4-114">Define el intervalo, en días, entre dos elementos periódicos consecutivos.</span><span class="sxs-lookup"><span data-stu-id="3f1b4-114">Defines the interval, in days, between two consecutive recurring items.</span></span> <span data-ttu-id="3f1b4-115">El valor debe ser en comprendido entre 1 y 999.</span><span class="sxs-lookup"><span data-stu-id="3f1b4-115">The value must be in the range from 1 to 999.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3f1b4-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3f1b4-116">Parent elements</span></span>

|<span data-ttu-id="3f1b4-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="3f1b4-117">**Element**</span></span>|<span data-ttu-id="3f1b4-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3f1b4-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3f1b4-119">Periodicidad (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="3f1b4-119">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="3f1b4-120">Contiene información sobre la periodicidad para las tareas repetitivas.</span><span class="sxs-lookup"><span data-stu-id="3f1b4-120">Contains recurrence information for recurring tasks.</span></span>  <br/> |
|[<span data-ttu-id="3f1b4-121">Periodicidad (RecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="3f1b4-121">Recurrence (RecurrenceType)</span></span>](recurrence-recurrencetype.md) <br/> |<span data-ttu-id="3f1b4-122">Contiene el patrón de periodicidad para los elementos de calendario y las convocatorias de reunión.</span><span class="sxs-lookup"><span data-stu-id="3f1b4-122">Contains the recurrence pattern for calendar items and meeting requests.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3f1b4-123">Notas</span><span class="sxs-lookup"><span data-stu-id="3f1b4-123">Remarks</span></span>

<span data-ttu-id="3f1b4-124">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="3f1b4-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3f1b4-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3f1b4-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3f1b4-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3f1b4-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3f1b4-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3f1b4-127">Schema name</span></span>  <br/> |<span data-ttu-id="3f1b4-128">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="3f1b4-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="3f1b4-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3f1b4-129">Validation file</span></span>  <br/> |<span data-ttu-id="3f1b4-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3f1b4-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3f1b4-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3f1b4-131">Can be empty</span></span>  <br/> |<span data-ttu-id="3f1b4-132">False</span><span class="sxs-lookup"><span data-stu-id="3f1b4-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3f1b4-133">Ver también</span><span class="sxs-lookup"><span data-stu-id="3f1b4-133">See also</span></span>

- [<span data-ttu-id="3f1b4-134">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="3f1b4-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

