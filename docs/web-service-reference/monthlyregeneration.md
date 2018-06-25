---
title: MonthlyRegeneration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MonthlyRegeneration
api_type:
- schema
ms.assetid: 9a52ca97-a663-41fe-b61a-61d8c53833ca
description: El elemento MonthlyRegeneration describe la frecuencia, en meses, de los cuales se regenera la tarea.
ms.openlocfilehash: 3de8ab5a6a2134ad5c596bf2bcb073d881c89746
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836488"
---
# <a name="monthlyregeneration"></a><span data-ttu-id="c9527-103">MonthlyRegeneration</span><span class="sxs-lookup"><span data-stu-id="c9527-103">MonthlyRegeneration</span></span>

<span data-ttu-id="c9527-104">El elemento **MonthlyRegeneration** describe la frecuencia, en meses, de los cuales se regenera la tarea.</span><span class="sxs-lookup"><span data-stu-id="c9527-104">The **MonthlyRegeneration** element describes the frequency, in months, of which task is regenerated.</span></span> 
  
```xml
<MonthlyRegeneration>
   <Interval/>
</MonthlyRegeneration>
```

 <span data-ttu-id="c9527-105">**MonthlyRegeneratingPatternType**</span><span class="sxs-lookup"><span data-stu-id="c9527-105">**MonthlyRegeneratingPatternType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c9527-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c9527-106">Attributes and elements</span></span>

<span data-ttu-id="c9527-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c9527-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c9527-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c9527-108">Attributes</span></span>

<span data-ttu-id="c9527-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c9527-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c9527-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c9527-110">Child elements</span></span>

|<span data-ttu-id="c9527-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="c9527-111">**Element**</span></span>|<span data-ttu-id="c9527-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c9527-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c9527-113">Interval</span><span class="sxs-lookup"><span data-stu-id="c9527-113">Interval</span></span>](interval.md) <br/> |<span data-ttu-id="c9527-114">Define el intervalo de meses entre dos elementos periódicos consecutivos.</span><span class="sxs-lookup"><span data-stu-id="c9527-114">Defines the interval, in months, between two consecutive recurring items.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c9527-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c9527-115">Parent elements</span></span>

|<span data-ttu-id="c9527-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="c9527-116">**Element**</span></span>|<span data-ttu-id="c9527-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c9527-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c9527-118">Periodicidad (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="c9527-118">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="c9527-119">Contiene información sobre la periodicidad para las tareas repetitivas.</span><span class="sxs-lookup"><span data-stu-id="c9527-119">Contains recurrence information for recurring tasks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c9527-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c9527-120">Remarks</span></span>

<span data-ttu-id="c9527-121">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="c9527-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c9527-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c9527-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c9527-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c9527-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c9527-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c9527-124">Schema name</span></span>  <br/> |<span data-ttu-id="c9527-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="c9527-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="c9527-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c9527-126">Validation file</span></span>  <br/> |<span data-ttu-id="c9527-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c9527-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c9527-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c9527-128">Can be empty</span></span>  <br/> |<span data-ttu-id="c9527-129">False</span><span class="sxs-lookup"><span data-stu-id="c9527-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c9527-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="c9527-130">See also</span></span>



- [<span data-ttu-id="c9527-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="c9527-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

