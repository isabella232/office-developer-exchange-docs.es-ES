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
description: El elemento YearlyRegeneration describe la frecuencia, en años, en que se regenera una tarea.
ms.openlocfilehash: 7a6796c433bc54d145d5a769e01f9bba46897735
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457882"
---
# <a name="yearlyregeneration"></a><span data-ttu-id="0bfb2-103">YearlyRegeneration</span><span class="sxs-lookup"><span data-stu-id="0bfb2-103">YearlyRegeneration</span></span>

<span data-ttu-id="0bfb2-104">El elemento **YearlyRegeneration** describe la frecuencia, en años, en que se regenera una tarea.</span><span class="sxs-lookup"><span data-stu-id="0bfb2-104">The **YearlyRegeneration** element describes the frequency, in years, in which a task is regenerated.</span></span> 
  
```xml
<YearlyRegeneratingPatternType>
   <Interval/>
</YearlyRegeneratingPatternType>
```

<span data-ttu-id="0bfb2-105">**YearlyRegeneratingPatternType**</span><span class="sxs-lookup"><span data-stu-id="0bfb2-105">**YearlyRegeneratingPatternType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="0bfb2-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="0bfb2-106">Attributes and elements</span></span>

<span data-ttu-id="0bfb2-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="0bfb2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0bfb2-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="0bfb2-108">Attributes</span></span>

<span data-ttu-id="0bfb2-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="0bfb2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0bfb2-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0bfb2-110">Child elements</span></span>

|<span data-ttu-id="0bfb2-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="0bfb2-111">**Element**</span></span>|<span data-ttu-id="0bfb2-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0bfb2-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0bfb2-113">Intervalo de</span><span class="sxs-lookup"><span data-stu-id="0bfb2-113">Interval</span></span>](interval.md) <br/> |<span data-ttu-id="0bfb2-114">Define el intervalo, en años, durante el cual se vuelve a generar una nueva tarea una vez finalizada la tarea.</span><span class="sxs-lookup"><span data-stu-id="0bfb2-114">Defines the interval, in years, during which a new task is regenerated after the completion of the task.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0bfb2-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0bfb2-115">Parent elements</span></span>

|<span data-ttu-id="0bfb2-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="0bfb2-116">**Element**</span></span>|<span data-ttu-id="0bfb2-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0bfb2-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0bfb2-118">Periodicidad (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="0bfb2-118">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="0bfb2-119">Contiene información de periodicidad para tareas periódicas.</span><span class="sxs-lookup"><span data-stu-id="0bfb2-119">Contains recurrence information for recurring tasks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0bfb2-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0bfb2-120">Remarks</span></span>

<span data-ttu-id="0bfb2-121">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="0bfb2-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="0bfb2-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0bfb2-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0bfb2-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="0bfb2-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0bfb2-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="0bfb2-124">Schema Name</span></span>  <br/> |<span data-ttu-id="0bfb2-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="0bfb2-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="0bfb2-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="0bfb2-126">Validation File</span></span>  <br/> |<span data-ttu-id="0bfb2-127">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="0bfb2-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0bfb2-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="0bfb2-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="0bfb2-129">Falso</span><span class="sxs-lookup"><span data-stu-id="0bfb2-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0bfb2-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="0bfb2-130">See also</span></span>

- [<span data-ttu-id="0bfb2-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="0bfb2-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

