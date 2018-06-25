---
title: NoEndRecurrence
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- NoEndRecurrence
api_type:
- schema
ms.assetid: ab2ebd9c-388e-45f1-abf9-56e293ef123b
description: El elemento NoEndRecurrence describe la fecha de inicio de un patrón de periodicidad de elemento que no tiene una fecha de finalización definidas.
ms.openlocfilehash: fc3eae170f5c07e31d7a80b45836efd07d74e543
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836537"
---
# <a name="noendrecurrence"></a><span data-ttu-id="b8523-103">NoEndRecurrence</span><span class="sxs-lookup"><span data-stu-id="b8523-103">NoEndRecurrence</span></span>

<span data-ttu-id="b8523-104">El elemento **NoEndRecurrence** describe la fecha de inicio de un patrón de periodicidad de elemento que no tiene una fecha de finalización definidas.</span><span class="sxs-lookup"><span data-stu-id="b8523-104">The **NoEndRecurrence** element describes the start date of an item recurrence pattern that does not have a defined end date.</span></span> 
  
```xml
<NoEndRecurrence>
   <StartDate/>
</NoEndRecurrence>
```

 <span data-ttu-id="b8523-105">**NoEndRecurrenceRangeType**</span><span class="sxs-lookup"><span data-stu-id="b8523-105">**NoEndRecurrenceRangeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b8523-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b8523-106">Attributes and elements</span></span>

<span data-ttu-id="b8523-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b8523-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b8523-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="b8523-108">Attributes</span></span>

<span data-ttu-id="b8523-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b8523-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b8523-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b8523-110">Child elements</span></span>

|<span data-ttu-id="b8523-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="b8523-111">**Element**</span></span>|<span data-ttu-id="b8523-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b8523-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b8523-113">StartDate (periodicidad)</span><span class="sxs-lookup"><span data-stu-id="b8523-113">StartDate (Recurrence)</span></span>](startdate-recurrence.md) <br/> |<span data-ttu-id="b8523-114">Representa la fecha de comienzo de una tarea periódica o elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="b8523-114">Represents the start date of a recurring task or calendar item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b8523-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b8523-115">Parent elements</span></span>

|<span data-ttu-id="b8523-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="b8523-116">**Element**</span></span>|<span data-ttu-id="b8523-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b8523-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b8523-118">Periodicidad (RecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="b8523-118">Recurrence (RecurrenceType)</span></span>](recurrence-recurrencetype.md) <br/> |<span data-ttu-id="b8523-119">Contiene el patrón de periodicidad para los elementos de calendario y las convocatorias de reunión.</span><span class="sxs-lookup"><span data-stu-id="b8523-119">Contains the recurrence pattern for calendar items and meeting requests.</span></span>  <br/> |
|[<span data-ttu-id="b8523-120">Periodicidad (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="b8523-120">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="b8523-121">Contiene información sobre la periodicidad para las tareas repetitivas.</span><span class="sxs-lookup"><span data-stu-id="b8523-121">Contains recurrence information for recurring tasks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b8523-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b8523-122">Remarks</span></span>

<span data-ttu-id="b8523-123">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="b8523-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b8523-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b8523-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b8523-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b8523-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b8523-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b8523-126">Schema name</span></span>  <br/> |<span data-ttu-id="b8523-127">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="b8523-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="b8523-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b8523-128">Validation file</span></span>  <br/> |<span data-ttu-id="b8523-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b8523-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b8523-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b8523-130">Can be empty</span></span>  <br/> |<span data-ttu-id="b8523-131">False</span><span class="sxs-lookup"><span data-stu-id="b8523-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b8523-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="b8523-132">See also</span></span>



- [<span data-ttu-id="b8523-133">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="b8523-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

