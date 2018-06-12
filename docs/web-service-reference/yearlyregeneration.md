---
title: YearlyRegeneration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- YearlyRegeneration
api_type:
- schema
ms.assetid: 23538bca-738e-4319-944e-f459ff8a7eba
description: El elemento YearlyRegeneration describe la frecuencia, en años, en el que se vuelve a generar una tarea.
ms.openlocfilehash: d034be1ff70e92fd5e96118b9fd1eb3033737f6c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19841025"
---
# <a name="yearlyregeneration"></a><span data-ttu-id="b8d8e-103">YearlyRegeneration</span><span class="sxs-lookup"><span data-stu-id="b8d8e-103">YearlyRegeneration</span></span>

<span data-ttu-id="b8d8e-104">El elemento **YearlyRegeneration** describe la frecuencia, en años, en el que se vuelve a generar una tarea.</span><span class="sxs-lookup"><span data-stu-id="b8d8e-104">The **YearlyRegeneration** element describes the frequency, in years, in which a task is regenerated.</span></span> 
  
```xml
<YearlyRegeneratingPatternType>
   <Interval/>
</YearlyRegeneratingPatternType>
```

<span data-ttu-id="b8d8e-105">**YearlyRegeneratingPatternType**</span><span class="sxs-lookup"><span data-stu-id="b8d8e-105">**YearlyRegeneratingPatternType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="b8d8e-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b8d8e-106">Attributes and elements</span></span>

<span data-ttu-id="b8d8e-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b8d8e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b8d8e-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="b8d8e-108">Attributes</span></span>

<span data-ttu-id="b8d8e-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b8d8e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b8d8e-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b8d8e-110">Child elements</span></span>

|<span data-ttu-id="b8d8e-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="b8d8e-111">**Element**</span></span>|<span data-ttu-id="b8d8e-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b8d8e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b8d8e-113">Interval</span><span class="sxs-lookup"><span data-stu-id="b8d8e-113">Interval</span></span>](interval.md) <br/> |<span data-ttu-id="b8d8e-114">Define el intervalo, en años, durante el cual se vuelve a generar una nueva tarea después de la finalización de la tarea.</span><span class="sxs-lookup"><span data-stu-id="b8d8e-114">Defines the interval, in years, during which a new task is regenerated after the completion of the task.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b8d8e-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b8d8e-115">Parent elements</span></span>

|<span data-ttu-id="b8d8e-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="b8d8e-116">**Element**</span></span>|<span data-ttu-id="b8d8e-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b8d8e-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b8d8e-118">Periodicidad (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="b8d8e-118">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="b8d8e-119">Contiene información sobre la periodicidad para las tareas repetitivas.</span><span class="sxs-lookup"><span data-stu-id="b8d8e-119">Contains recurrence information for recurring tasks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b8d8e-120">Notas</span><span class="sxs-lookup"><span data-stu-id="b8d8e-120">Remarks</span></span>

<span data-ttu-id="b8d8e-121">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="b8d8e-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="b8d8e-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b8d8e-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b8d8e-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b8d8e-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b8d8e-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b8d8e-124">Schema Name</span></span>  <br/> |<span data-ttu-id="b8d8e-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="b8d8e-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="b8d8e-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b8d8e-126">Validation File</span></span>  <br/> |<span data-ttu-id="b8d8e-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b8d8e-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b8d8e-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b8d8e-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="b8d8e-129">False</span><span class="sxs-lookup"><span data-stu-id="b8d8e-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b8d8e-130">Ver también</span><span class="sxs-lookup"><span data-stu-id="b8d8e-130">See also</span></span>

- [<span data-ttu-id="b8d8e-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="b8d8e-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

