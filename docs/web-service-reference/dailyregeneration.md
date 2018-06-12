---
title: DailyRegeneration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DailyRegeneration
api_type:
- schema
ms.assetid: cafb57e4-c518-45e0-b565-2babd0dab1df
description: El elemento DailyRegeneration describe la frecuencia, en días, en el que se vuelve a generar una tarea.
ms.openlocfilehash: 356f7fd2672b2ad87d17e597c52e9f12273ce3c6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764020"
---
# <a name="dailyregeneration"></a><span data-ttu-id="1ac14-103">DailyRegeneration</span><span class="sxs-lookup"><span data-stu-id="1ac14-103">DailyRegeneration</span></span>

<span data-ttu-id="1ac14-104">El elemento **DailyRegeneration** describe la frecuencia, en días, en el que se vuelve a generar una tarea.</span><span class="sxs-lookup"><span data-stu-id="1ac14-104">The **DailyRegeneration** element describes the frequency, in days, in which a task is regenerated.</span></span> 
  
```xml
<DailyRegeneration>
   <Interval/>
</DailyRegeneration>
```

<span data-ttu-id="1ac14-105">**DailyRegeneratingPatternType**</span><span class="sxs-lookup"><span data-stu-id="1ac14-105">**DailyRegeneratingPatternType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="1ac14-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="1ac14-106">Attributes and elements</span></span>

<span data-ttu-id="1ac14-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="1ac14-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1ac14-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="1ac14-108">Attributes</span></span>

<span data-ttu-id="1ac14-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1ac14-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1ac14-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1ac14-110">Child elements</span></span>

|<span data-ttu-id="1ac14-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="1ac14-111">**Element**</span></span>|<span data-ttu-id="1ac14-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1ac14-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1ac14-113">Interval</span><span class="sxs-lookup"><span data-stu-id="1ac14-113">Interval</span></span>](interval.md) <br/> |<span data-ttu-id="1ac14-114">Define el intervalo, en días, entre dos elementos periódicos consecutivos.</span><span class="sxs-lookup"><span data-stu-id="1ac14-114">Defines the interval, in days, between two consecutive recurring items.</span></span> <span data-ttu-id="1ac14-115">El valor debe ser en el intervalo de 1 a 999.</span><span class="sxs-lookup"><span data-stu-id="1ac14-115">The value must be in the range of 1 to 999.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1ac14-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="1ac14-116">Parent elements</span></span>

|<span data-ttu-id="1ac14-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="1ac14-117">**Element**</span></span>|<span data-ttu-id="1ac14-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1ac14-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1ac14-119">Periodicidad (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="1ac14-119">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="1ac14-120">Contiene información sobre la periodicidad para las tareas repetitivas.</span><span class="sxs-lookup"><span data-stu-id="1ac14-120">Contains recurrence information for recurring tasks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1ac14-121">Notas</span><span class="sxs-lookup"><span data-stu-id="1ac14-121">Remarks</span></span>

<span data-ttu-id="1ac14-122">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="1ac14-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1ac14-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="1ac14-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1ac14-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1ac14-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1ac14-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="1ac14-125">Schema name</span></span>  <br/> |<span data-ttu-id="1ac14-126">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="1ac14-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="1ac14-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="1ac14-127">Validation file</span></span>  <br/> |<span data-ttu-id="1ac14-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1ac14-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1ac14-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="1ac14-129">Can be empty</span></span>  <br/> |<span data-ttu-id="1ac14-130">False</span><span class="sxs-lookup"><span data-stu-id="1ac14-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1ac14-131">Ver también</span><span class="sxs-lookup"><span data-stu-id="1ac14-131">See also</span></span>

- [<span data-ttu-id="1ac14-132">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="1ac14-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

