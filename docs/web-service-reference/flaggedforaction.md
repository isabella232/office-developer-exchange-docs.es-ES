---
title: FlaggedForAction
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FlaggedForAction
api_type:
- schema
ms.assetid: 6a08c48a-7b32-4754-8940-adbda55e8133
description: El elemento FlaggedForAction especifica la marca para el valor de la acción que debe aparecer en los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.
ms.openlocfilehash: 5b6e714512edcf12ded2c04f414d047b8622d305
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764671"
---
# <a name="flaggedforaction"></a><span data-ttu-id="c52c1-103">FlaggedForAction</span><span class="sxs-lookup"><span data-stu-id="c52c1-103">FlaggedForAction</span></span>

<span data-ttu-id="c52c1-104">El elemento **FlaggedForAction** especifica la marca para el valor de la acción que debe aparecer en los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="c52c1-104">The **FlaggedForAction** element specifies the flag for action value that must appear on incoming messages in order for the condition or exception to apply.</span></span> 
  
```XML
<FlaggedForAction/>
```

 <span data-ttu-id="c52c1-105">**FlaggedForActionType**</span><span class="sxs-lookup"><span data-stu-id="c52c1-105">**FlaggedForActionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c52c1-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c52c1-106">Attributes and elements</span></span>

<span data-ttu-id="c52c1-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c52c1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c52c1-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c52c1-108">Attributes</span></span>

<span data-ttu-id="c52c1-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c52c1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c52c1-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c52c1-110">Child elements</span></span>

<span data-ttu-id="c52c1-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c52c1-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c52c1-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c52c1-112">Parent elements</span></span>

|<span data-ttu-id="c52c1-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="c52c1-113">**Element**</span></span>|<span data-ttu-id="c52c1-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c52c1-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c52c1-115">Condiciones</span><span class="sxs-lookup"><span data-stu-id="c52c1-115">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="c52c1-116">Representa las condiciones que, cuando se cumplen los requisitos, se activará las acciones de regla para una regla.</span><span class="sxs-lookup"><span data-stu-id="c52c1-116">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="c52c1-117">Excepciones</span><span class="sxs-lookup"><span data-stu-id="c52c1-117">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="c52c1-118">Representa las excepciones que representan todas las condiciones de excepción de regla disponibles para una regla de bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="c52c1-118">Represents the exceptions that represent all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c52c1-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="c52c1-119">Text value</span></span>

<span data-ttu-id="c52c1-120">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="c52c1-120">A text value is required.</span></span> <span data-ttu-id="c52c1-121">Los siguientes son los posibles valores de texto para este elemento:</span><span class="sxs-lookup"><span data-stu-id="c52c1-121">The following are the possible text values for this element:</span></span>
  
- <span data-ttu-id="c52c1-122">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="c52c1-122">Any</span></span>
    
- <span data-ttu-id="c52c1-123">Llamada</span><span class="sxs-lookup"><span data-stu-id="c52c1-123">Call</span></span>
    
- <span data-ttu-id="c52c1-124">DoNotForward</span><span class="sxs-lookup"><span data-stu-id="c52c1-124">DoNotForward</span></span>
    
- <span data-ttu-id="c52c1-125">Realizar su seguimiento</span><span class="sxs-lookup"><span data-stu-id="c52c1-125">FollowUp</span></span>
    
- <span data-ttu-id="c52c1-126">PARA SU INFORMACIÓN</span><span class="sxs-lookup"><span data-stu-id="c52c1-126">FYI</span></span>
    
- <span data-ttu-id="c52c1-127">Forward</span><span class="sxs-lookup"><span data-stu-id="c52c1-127">Forward</span></span>
    
- <span data-ttu-id="c52c1-128">NoResponseNecessary</span><span class="sxs-lookup"><span data-stu-id="c52c1-128">NoResponseNecessary</span></span>
    
- <span data-ttu-id="c52c1-129">Leído</span><span class="sxs-lookup"><span data-stu-id="c52c1-129">Read</span></span>
    
- <span data-ttu-id="c52c1-130">Responder</span><span class="sxs-lookup"><span data-stu-id="c52c1-130">Reply</span></span>
    
- <span data-ttu-id="c52c1-131">ReplyToAll</span><span class="sxs-lookup"><span data-stu-id="c52c1-131">ReplyToAll</span></span>
    
- <span data-ttu-id="c52c1-132">Revisión</span><span class="sxs-lookup"><span data-stu-id="c52c1-132">Review</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c52c1-133">Notas</span><span class="sxs-lookup"><span data-stu-id="c52c1-133">Remarks</span></span>

<span data-ttu-id="c52c1-134">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="c52c1-134">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c52c1-135">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c52c1-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c52c1-136">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c52c1-136">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c52c1-137">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c52c1-137">Schema Name</span></span>  <br/> |<span data-ttu-id="c52c1-138">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="c52c1-138">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c52c1-139">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c52c1-139">Validation File</span></span>  <br/> |<span data-ttu-id="c52c1-140">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="c52c1-140">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c52c1-141">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c52c1-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="c52c1-142">Verdadero</span><span class="sxs-lookup"><span data-stu-id="c52c1-142">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c52c1-143">Ver también</span><span class="sxs-lookup"><span data-stu-id="c52c1-143">See also</span></span>



- [<span data-ttu-id="c52c1-144">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="c52c1-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

