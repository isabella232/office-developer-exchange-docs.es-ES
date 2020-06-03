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
ms.openlocfilehash: 000674e5b0bad9deea5aa4ac78d41135a922c755
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465943"
---
# <a name="numberedrecurrence"></a><span data-ttu-id="10206-103">NumberedRecurrence</span><span class="sxs-lookup"><span data-stu-id="10206-103">NumberedRecurrence</span></span>

<span data-ttu-id="10206-104">El elemento **NumberedRecurrence** describe la fecha de inicio y el número de repeticiones de un elemento periódico.</span><span class="sxs-lookup"><span data-stu-id="10206-104">The **NumberedRecurrence** element describes the start date and the number of occurrences of a recurring item.</span></span> 
  
```xml
<NumberedRecurrence>
   <StartDate/>
   <NumberOfOccurrences/>
</NumberedRecurrence>
```

 <span data-ttu-id="10206-105">**NumberedRecurrenceRangeType**</span><span class="sxs-lookup"><span data-stu-id="10206-105">**NumberedRecurrenceRangeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="10206-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="10206-106">Attributes and elements</span></span>

<span data-ttu-id="10206-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="10206-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="10206-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="10206-108">Attributes</span></span>

<span data-ttu-id="10206-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="10206-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="10206-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="10206-110">Child elements</span></span>

|<span data-ttu-id="10206-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="10206-111">**Element**</span></span>|<span data-ttu-id="10206-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="10206-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="10206-113">StartDate (periodicidad)</span><span class="sxs-lookup"><span data-stu-id="10206-113">StartDate (Recurrence)</span></span>](startdate-recurrence.md) <br/> |<span data-ttu-id="10206-114">Representa la fecha de inicio de una tarea periódica o un elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="10206-114">Represents the start date of a recurring task or calendar item.</span></span>  <br/> |
|[<span data-ttu-id="10206-115">NumberOfOccurrences</span><span class="sxs-lookup"><span data-stu-id="10206-115">NumberOfOccurrences</span></span>](numberofoccurrences.md) <br/> |<span data-ttu-id="10206-116">Contiene el número de repeticiones de un elemento periódico.</span><span class="sxs-lookup"><span data-stu-id="10206-116">Contains the number of occurrences of a recurring item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="10206-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="10206-117">Parent elements</span></span>

|<span data-ttu-id="10206-118">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="10206-118">**Element**</span></span>|<span data-ttu-id="10206-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="10206-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="10206-120">Recurrence (RecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="10206-120">Recurrence (RecurrenceType)</span></span>](recurrence-recurrencetype.md) <br/> |<span data-ttu-id="10206-121">Contiene el patrón de periodicidad para los elementos de calendario y las convocatorias de reunión.</span><span class="sxs-lookup"><span data-stu-id="10206-121">Contains the recurrence pattern for calendar items and meeting requests.</span></span>  <br/> |
|[<span data-ttu-id="10206-122">Periodicidad (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="10206-122">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="10206-123">Contiene información de periodicidad para tareas periódicas.</span><span class="sxs-lookup"><span data-stu-id="10206-123">Contains recurrence information for recurring tasks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="10206-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="10206-124">Remarks</span></span>

<span data-ttu-id="10206-125">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="10206-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="10206-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="10206-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="10206-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="10206-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="10206-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="10206-128">Schema name</span></span>  <br/> |<span data-ttu-id="10206-129">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="10206-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="10206-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="10206-130">Validation file</span></span>  <br/> |<span data-ttu-id="10206-131">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="10206-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="10206-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="10206-132">Can be empty</span></span>  <br/> |<span data-ttu-id="10206-133">Falso</span><span class="sxs-lookup"><span data-stu-id="10206-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="10206-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="10206-134">See also</span></span>



- [<span data-ttu-id="10206-135">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="10206-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

