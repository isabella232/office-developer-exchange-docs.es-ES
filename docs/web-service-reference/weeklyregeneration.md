---
title: WeeklyRegeneration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- WeeklyRegeneration
api_type:
- schema
ms.assetid: f128fdaa-ca3d-4614-8e55-f25e76a67b6c
description: El elemento WeeklyRegeneration describe la frecuencia, en semanas, en el que se vuelve a generar una tarea.
ms.openlocfilehash: 36cd3cc5c180f2b2cf53708e7787d0595f518def
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840999"
---
# <a name="weeklyregeneration"></a><span data-ttu-id="c1621-103">WeeklyRegeneration</span><span class="sxs-lookup"><span data-stu-id="c1621-103">WeeklyRegeneration</span></span>

<span data-ttu-id="c1621-104">El elemento **WeeklyRegeneration** describe la frecuencia, en semanas, en el que se vuelve a generar una tarea.</span><span class="sxs-lookup"><span data-stu-id="c1621-104">The **WeeklyRegeneration** element describes the frequency, in weeks, in which a task is regenerated.</span></span> 
  
```xml
<WeeklyRegeneration>
   <Interval/>
</WeeklyRegeneration>
```

 <span data-ttu-id="c1621-105">**WeeklyRegeneratingPatternType**</span><span class="sxs-lookup"><span data-stu-id="c1621-105">**WeeklyRegeneratingPatternType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c1621-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c1621-106">Attributes and elements</span></span>

<span data-ttu-id="c1621-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c1621-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c1621-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c1621-108">Attributes</span></span>

<span data-ttu-id="c1621-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c1621-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c1621-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c1621-110">Child elements</span></span>

|<span data-ttu-id="c1621-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="c1621-111">**Element**</span></span>|<span data-ttu-id="c1621-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c1621-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c1621-113">Interval</span><span class="sxs-lookup"><span data-stu-id="c1621-113">Interval</span></span>](interval.md) <br/> |<span data-ttu-id="c1621-114">Define el intervalo, en semanas, ya que la tarea se completó, después del cual se vuelve a generar una nueva tarea.</span><span class="sxs-lookup"><span data-stu-id="c1621-114">Defines the interval, in weeks, since the task was completed, after which a new task is regenerated.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c1621-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c1621-115">Parent elements</span></span>

|<span data-ttu-id="c1621-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="c1621-116">**Element**</span></span>|<span data-ttu-id="c1621-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c1621-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c1621-118">Periodicidad (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="c1621-118">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="c1621-119">Contiene información sobre la periodicidad para las tareas repetitivas.</span><span class="sxs-lookup"><span data-stu-id="c1621-119">Contains recurrence information for recurring tasks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c1621-120">Notas</span><span class="sxs-lookup"><span data-stu-id="c1621-120">Remarks</span></span>

<span data-ttu-id="c1621-121">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="c1621-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c1621-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c1621-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c1621-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c1621-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c1621-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c1621-124">Schema Name</span></span>  <br/> |<span data-ttu-id="c1621-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="c1621-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="c1621-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c1621-126">Validation File</span></span>  <br/> |<span data-ttu-id="c1621-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c1621-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c1621-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c1621-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="c1621-129">False</span><span class="sxs-lookup"><span data-stu-id="c1621-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c1621-130">Ver también</span><span class="sxs-lookup"><span data-stu-id="c1621-130">See also</span></span>



- [<span data-ttu-id="c1621-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="c1621-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

