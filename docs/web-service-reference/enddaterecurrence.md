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
description: El elemento EndDateRecurrence describe la fecha de inicio y la fecha de finalización de un patrón de periodicidad de un elemento.
ms.openlocfilehash: e8ae72012e5bcac8d8b2a06b6d3a9b3a7caf30d7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460151"
---
# <a name="enddaterecurrence"></a><span data-ttu-id="c9ced-103">EndDateRecurrence</span><span class="sxs-lookup"><span data-stu-id="c9ced-103">EndDateRecurrence</span></span>

<span data-ttu-id="c9ced-104">El elemento **EndDateRecurrence** describe la fecha de inicio y la fecha de finalización de un patrón de periodicidad de un elemento.</span><span class="sxs-lookup"><span data-stu-id="c9ced-104">The **EndDateRecurrence** element describes the start date and the end date of an item recurrence pattern.</span></span> 
  
```xml
<EndDateRecurrence>
   <StartDate/>
   <EndDate/>
</EndDateRecurrence>
```

 <span data-ttu-id="c9ced-105">**EndDateRecurrenceRangeType**</span><span class="sxs-lookup"><span data-stu-id="c9ced-105">**EndDateRecurrenceRangeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c9ced-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c9ced-106">Attributes and elements</span></span>

<span data-ttu-id="c9ced-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c9ced-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c9ced-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c9ced-108">Attributes</span></span>

<span data-ttu-id="c9ced-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c9ced-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c9ced-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c9ced-110">Child elements</span></span>

|<span data-ttu-id="c9ced-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c9ced-111">**Element**</span></span>|<span data-ttu-id="c9ced-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c9ced-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c9ced-113">StartDate (periodicidad)</span><span class="sxs-lookup"><span data-stu-id="c9ced-113">StartDate (Recurrence)</span></span>](startdate-recurrence.md) <br/> |<span data-ttu-id="c9ced-114">Representa la fecha de inicio de una tarea periódica o un elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="c9ced-114">Represents the start date of a recurring task or calendar item.</span></span>  <br/> |
|[<span data-ttu-id="c9ced-115">EndDate (periodicidad)</span><span class="sxs-lookup"><span data-stu-id="c9ced-115">EndDate (Recurrence)</span></span>](enddate-recurrence.md) <br/> |<span data-ttu-id="c9ced-116">Representa la fecha de finalización de una tarea periódica o un elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="c9ced-116">Represents the end date of a recurring task or calendar item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c9ced-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c9ced-117">Parent elements</span></span>

|<span data-ttu-id="c9ced-118">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c9ced-118">**Element**</span></span>|<span data-ttu-id="c9ced-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c9ced-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c9ced-120">Recurrence (RecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="c9ced-120">Recurrence (RecurrenceType)</span></span>](recurrence-recurrencetype.md) <br/> |<span data-ttu-id="c9ced-121">Contiene el patrón de periodicidad para los elementos de calendario y las convocatorias de reunión.</span><span class="sxs-lookup"><span data-stu-id="c9ced-121">Contains the recurrence pattern for calendar items and meeting requests.</span></span>  <br/> |
|[<span data-ttu-id="c9ced-122">Periodicidad (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="c9ced-122">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="c9ced-123">Contiene el patrón de periodicidad de las tareas periódicas.</span><span class="sxs-lookup"><span data-stu-id="c9ced-123">Contains the recurrence pattern for recurring tasks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c9ced-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c9ced-124">Remarks</span></span>

<span data-ttu-id="c9ced-125">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="c9ced-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c9ced-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c9ced-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c9ced-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="c9ced-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c9ced-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c9ced-128">Schema name</span></span>  <br/> |<span data-ttu-id="c9ced-129">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="c9ced-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="c9ced-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c9ced-130">Validation file</span></span>  <br/> |<span data-ttu-id="c9ced-131">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="c9ced-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c9ced-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c9ced-132">Can be empty</span></span>  <br/> |<span data-ttu-id="c9ced-133">Falso</span><span class="sxs-lookup"><span data-stu-id="c9ced-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c9ced-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="c9ced-134">See also</span></span>



- [<span data-ttu-id="c9ced-135">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="c9ced-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

