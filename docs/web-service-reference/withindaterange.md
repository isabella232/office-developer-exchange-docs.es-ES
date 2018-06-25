---
title: WithinDateRange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- WithinDateRange
api_type:
- schema
ms.assetid: 226aeb15-016f-45ca-992a-c137ba09ca08
description: El elemento WithinDateRange especifica el intervalo de fechas dentro del cual los mensajes entrantes tienen que se han recibido en orden para la condición o la excepción que se debe aplicar.
ms.openlocfilehash: d85ef91c581008c2aafb06b1900c4514aebacd65
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19841001"
---
# <a name="withindaterange"></a><span data-ttu-id="76d08-103">WithinDateRange</span><span class="sxs-lookup"><span data-stu-id="76d08-103">WithinDateRange</span></span>

<span data-ttu-id="76d08-104">El elemento **WithinDateRange** especifica el intervalo de fechas dentro del cual los mensajes entrantes tienen que se han recibido en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="76d08-104">The **WithinDateRange** element specifies the date range within which incoming messages have to have been received in order for the condition or exception to apply.</span></span> 
  
```XML
<WithinDateRange>
     <StartDateTime/>
     <EndDateTime/>
</WithinDateRange>
```

 <span data-ttu-id="76d08-105">**RulePredicateDateRangeType**</span><span class="sxs-lookup"><span data-stu-id="76d08-105">**RulePredicateDateRangeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="76d08-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="76d08-106">Attributes and elements</span></span>

<span data-ttu-id="76d08-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="76d08-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="76d08-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="76d08-108">Attributes</span></span>

<span data-ttu-id="76d08-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="76d08-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="76d08-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="76d08-110">Child elements</span></span>

|<span data-ttu-id="76d08-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="76d08-111">**Element**</span></span>|<span data-ttu-id="76d08-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="76d08-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="76d08-113">StartDateTime</span><span class="sxs-lookup"><span data-stu-id="76d08-113">StartDateTime</span></span>](startdatetime.md) <br/> |<span data-ttu-id="76d08-114">Especifica la regla de período de tiempo y se indica que se cumple la condición de regla después de este valor.</span><span class="sxs-lookup"><span data-stu-id="76d08-114">Specifies the rule time period and indicates that the rule condition is met after this value.</span></span>  <br/> |
|[<span data-ttu-id="76d08-115">EndDateTime</span><span class="sxs-lookup"><span data-stu-id="76d08-115">EndDateTime</span></span>](enddatetime.md) <br/> |<span data-ttu-id="76d08-116">Especifica la regla de período de tiempo y se indica que se cumple la condición de regla antes de este valor.</span><span class="sxs-lookup"><span data-stu-id="76d08-116">Specifies the rule time period and indicates that the rule condition is met before this value.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="76d08-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="76d08-117">Parent elements</span></span>

|<span data-ttu-id="76d08-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="76d08-118">**Element**</span></span>|<span data-ttu-id="76d08-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="76d08-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="76d08-120">Condiciones</span><span class="sxs-lookup"><span data-stu-id="76d08-120">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="76d08-121">Representa las condiciones que, cuando se cumplen los requisitos, se activará las acciones de regla para una regla.</span><span class="sxs-lookup"><span data-stu-id="76d08-121">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="76d08-122">Excepciones</span><span class="sxs-lookup"><span data-stu-id="76d08-122">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="76d08-123">Representa todas las condiciones de excepción de regla disponibles para una regla de bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="76d08-123">Represents all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="76d08-124">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="76d08-124">Text value</span></span>

<span data-ttu-id="76d08-125">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="76d08-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="76d08-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="76d08-126">Remarks</span></span>

<span data-ttu-id="76d08-127">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="76d08-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="76d08-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="76d08-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="76d08-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="76d08-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="76d08-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="76d08-130">Schema Name</span></span>  <br/> |<span data-ttu-id="76d08-131">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="76d08-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="76d08-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="76d08-132">Validation File</span></span>  <br/> |<span data-ttu-id="76d08-133">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="76d08-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="76d08-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="76d08-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="76d08-135">Verdadero</span><span class="sxs-lookup"><span data-stu-id="76d08-135">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="76d08-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="76d08-136">See also</span></span>



- [<span data-ttu-id="76d08-137">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="76d08-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

