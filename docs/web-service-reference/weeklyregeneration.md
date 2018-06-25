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
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840999"
---
# <a name="weeklyregeneration"></a><span data-ttu-id="caa9d-103">WeeklyRegeneration</span><span class="sxs-lookup"><span data-stu-id="caa9d-103">WeeklyRegeneration</span></span>

<span data-ttu-id="caa9d-104">El elemento **WeeklyRegeneration** describe la frecuencia, en semanas, en el que se vuelve a generar una tarea.</span><span class="sxs-lookup"><span data-stu-id="caa9d-104">The **WeeklyRegeneration** element describes the frequency, in weeks, in which a task is regenerated.</span></span> 
  
```xml
<WeeklyRegeneration>
   <Interval/>
</WeeklyRegeneration>
```

 <span data-ttu-id="caa9d-105">**WeeklyRegeneratingPatternType**</span><span class="sxs-lookup"><span data-stu-id="caa9d-105">**WeeklyRegeneratingPatternType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="caa9d-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="caa9d-106">Attributes and elements</span></span>

<span data-ttu-id="caa9d-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="caa9d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="caa9d-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="caa9d-108">Attributes</span></span>

<span data-ttu-id="caa9d-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="caa9d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="caa9d-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="caa9d-110">Child elements</span></span>

|<span data-ttu-id="caa9d-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="caa9d-111">**Element**</span></span>|<span data-ttu-id="caa9d-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="caa9d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="caa9d-113">Interval</span><span class="sxs-lookup"><span data-stu-id="caa9d-113">Interval</span></span>](interval.md) <br/> |<span data-ttu-id="caa9d-114">Define el intervalo, en semanas, ya que la tarea se completó, después del cual se vuelve a generar una nueva tarea.</span><span class="sxs-lookup"><span data-stu-id="caa9d-114">Defines the interval, in weeks, since the task was completed, after which a new task is regenerated.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="caa9d-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="caa9d-115">Parent elements</span></span>

|<span data-ttu-id="caa9d-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="caa9d-116">**Element**</span></span>|<span data-ttu-id="caa9d-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="caa9d-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="caa9d-118">Periodicidad (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="caa9d-118">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="caa9d-119">Contiene información sobre la periodicidad para las tareas repetitivas.</span><span class="sxs-lookup"><span data-stu-id="caa9d-119">Contains recurrence information for recurring tasks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="caa9d-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="caa9d-120">Remarks</span></span>

<span data-ttu-id="caa9d-121">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="caa9d-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="caa9d-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="caa9d-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="caa9d-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="caa9d-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="caa9d-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="caa9d-124">Schema Name</span></span>  <br/> |<span data-ttu-id="caa9d-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="caa9d-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="caa9d-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="caa9d-126">Validation File</span></span>  <br/> |<span data-ttu-id="caa9d-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="caa9d-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="caa9d-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="caa9d-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="caa9d-129">False</span><span class="sxs-lookup"><span data-stu-id="caa9d-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="caa9d-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="caa9d-130">See also</span></span>



- [<span data-ttu-id="caa9d-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="caa9d-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

