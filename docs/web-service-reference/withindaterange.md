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
description: El elemento WithinDateRange especifica el intervalo de fechas en el que se deben recibir los mensajes entrantes para que se aplique la condición o excepción.
ms.openlocfilehash: ef5fb15b64ee4f7060f907818c4ebd4367ced5e7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461852"
---
# <a name="withindaterange"></a><span data-ttu-id="b11db-103">WithinDateRange</span><span class="sxs-lookup"><span data-stu-id="b11db-103">WithinDateRange</span></span>

<span data-ttu-id="b11db-104">El elemento **WithinDateRange** especifica el intervalo de fechas en el que se deben recibir los mensajes entrantes para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="b11db-104">The **WithinDateRange** element specifies the date range within which incoming messages have to have been received in order for the condition or exception to apply.</span></span> 
  
```XML
<WithinDateRange>
     <StartDateTime/>
     <EndDateTime/>
</WithinDateRange>
```

 <span data-ttu-id="b11db-105">**RulePredicateDateRangeType**</span><span class="sxs-lookup"><span data-stu-id="b11db-105">**RulePredicateDateRangeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b11db-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b11db-106">Attributes and elements</span></span>

<span data-ttu-id="b11db-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b11db-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b11db-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="b11db-108">Attributes</span></span>

<span data-ttu-id="b11db-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="b11db-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b11db-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b11db-110">Child elements</span></span>

|<span data-ttu-id="b11db-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b11db-111">**Element**</span></span>|<span data-ttu-id="b11db-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b11db-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b11db-113">StartDateTime</span><span class="sxs-lookup"><span data-stu-id="b11db-113">StartDateTime</span></span>](startdatetime.md) <br/> |<span data-ttu-id="b11db-114">Especifica el período de tiempo de la regla e indica que la condición de la regla se cumple después de este valor.</span><span class="sxs-lookup"><span data-stu-id="b11db-114">Specifies the rule time period and indicates that the rule condition is met after this value.</span></span>  <br/> |
|[<span data-ttu-id="b11db-115">EndDateTime</span><span class="sxs-lookup"><span data-stu-id="b11db-115">EndDateTime</span></span>](enddatetime.md) <br/> |<span data-ttu-id="b11db-116">Especifica el período de tiempo de la regla e indica que la condición de la regla se cumple antes que este valor.</span><span class="sxs-lookup"><span data-stu-id="b11db-116">Specifies the rule time period and indicates that the rule condition is met before this value.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b11db-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b11db-117">Parent elements</span></span>

|<span data-ttu-id="b11db-118">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b11db-118">**Element**</span></span>|<span data-ttu-id="b11db-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b11db-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b11db-120">Condiciones</span><span class="sxs-lookup"><span data-stu-id="b11db-120">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="b11db-121">Representa las condiciones que, cuando se cumplan, desencadenarán las acciones de regla de una regla.</span><span class="sxs-lookup"><span data-stu-id="b11db-121">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="b11db-122">Excepciones</span><span class="sxs-lookup"><span data-stu-id="b11db-122">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="b11db-123">Representa todas las condiciones de excepción de regla disponibles para una regla de bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="b11db-123">Represents all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b11db-124">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="b11db-124">Text value</span></span>

<span data-ttu-id="b11db-125">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b11db-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b11db-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b11db-126">Remarks</span></span>

<span data-ttu-id="b11db-127">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="b11db-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b11db-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b11db-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b11db-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="b11db-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b11db-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b11db-130">Schema Name</span></span>  <br/> |<span data-ttu-id="b11db-131">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="b11db-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b11db-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b11db-132">Validation File</span></span>  <br/> |<span data-ttu-id="b11db-133">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="b11db-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b11db-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b11db-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="b11db-135">Verdadero</span><span class="sxs-lookup"><span data-stu-id="b11db-135">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b11db-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="b11db-136">See also</span></span>



- [<span data-ttu-id="b11db-137">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="b11db-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

