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
description: El elemento WeeklyRegeneration describe la frecuencia, en semanas, en la que se regenera una tarea.
ms.openlocfilehash: dc333e051fd2213942e629a3f2764c72abfaeba5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459752"
---
# <a name="weeklyregeneration"></a><span data-ttu-id="0694c-103">WeeklyRegeneration</span><span class="sxs-lookup"><span data-stu-id="0694c-103">WeeklyRegeneration</span></span>

<span data-ttu-id="0694c-104">El elemento **WeeklyRegeneration** describe la frecuencia, en semanas, en la que se regenera una tarea.</span><span class="sxs-lookup"><span data-stu-id="0694c-104">The **WeeklyRegeneration** element describes the frequency, in weeks, in which a task is regenerated.</span></span> 
  
```xml
<WeeklyRegeneration>
   <Interval/>
</WeeklyRegeneration>
```

 <span data-ttu-id="0694c-105">**WeeklyRegeneratingPatternType**</span><span class="sxs-lookup"><span data-stu-id="0694c-105">**WeeklyRegeneratingPatternType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0694c-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="0694c-106">Attributes and elements</span></span>

<span data-ttu-id="0694c-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="0694c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0694c-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="0694c-108">Attributes</span></span>

<span data-ttu-id="0694c-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="0694c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0694c-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0694c-110">Child elements</span></span>

|<span data-ttu-id="0694c-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="0694c-111">**Element**</span></span>|<span data-ttu-id="0694c-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0694c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0694c-113">Intervalo de</span><span class="sxs-lookup"><span data-stu-id="0694c-113">Interval</span></span>](interval.md) <br/> |<span data-ttu-id="0694c-114">Define el intervalo, en semanas, desde que se completó la tarea, después de la cual se regenera una nueva tarea.</span><span class="sxs-lookup"><span data-stu-id="0694c-114">Defines the interval, in weeks, since the task was completed, after which a new task is regenerated.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0694c-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0694c-115">Parent elements</span></span>

|<span data-ttu-id="0694c-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="0694c-116">**Element**</span></span>|<span data-ttu-id="0694c-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0694c-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0694c-118">Periodicidad (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="0694c-118">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="0694c-119">Contiene información de periodicidad para tareas periódicas.</span><span class="sxs-lookup"><span data-stu-id="0694c-119">Contains recurrence information for recurring tasks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0694c-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0694c-120">Remarks</span></span>

<span data-ttu-id="0694c-121">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="0694c-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0694c-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0694c-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0694c-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="0694c-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0694c-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="0694c-124">Schema Name</span></span>  <br/> |<span data-ttu-id="0694c-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="0694c-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="0694c-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="0694c-126">Validation File</span></span>  <br/> |<span data-ttu-id="0694c-127">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="0694c-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0694c-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="0694c-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="0694c-129">Falso</span><span class="sxs-lookup"><span data-stu-id="0694c-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0694c-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="0694c-130">See also</span></span>



- [<span data-ttu-id="0694c-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="0694c-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

