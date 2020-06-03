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
description: El elemento FlaggedForAction especifica la marca para el valor de la acción que debe aparecer en los mensajes entrantes para que se aplique la condición o excepción.
ms.openlocfilehash: f996dc4bcf30db32e1d73fb302ab137f0a6ad4d4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466244"
---
# <a name="flaggedforaction"></a><span data-ttu-id="c7f12-103">FlaggedForAction</span><span class="sxs-lookup"><span data-stu-id="c7f12-103">FlaggedForAction</span></span>

<span data-ttu-id="c7f12-104">El elemento **FlaggedForAction** especifica la marca para el valor de la acción que debe aparecer en los mensajes entrantes para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="c7f12-104">The **FlaggedForAction** element specifies the flag for action value that must appear on incoming messages in order for the condition or exception to apply.</span></span> 
  
```XML
<FlaggedForAction/>
```

 <span data-ttu-id="c7f12-105">**FlaggedForActionType**</span><span class="sxs-lookup"><span data-stu-id="c7f12-105">**FlaggedForActionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c7f12-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c7f12-106">Attributes and elements</span></span>

<span data-ttu-id="c7f12-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c7f12-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c7f12-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c7f12-108">Attributes</span></span>

<span data-ttu-id="c7f12-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c7f12-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c7f12-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c7f12-110">Child elements</span></span>

<span data-ttu-id="c7f12-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c7f12-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c7f12-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c7f12-112">Parent elements</span></span>

|<span data-ttu-id="c7f12-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c7f12-113">**Element**</span></span>|<span data-ttu-id="c7f12-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c7f12-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c7f12-115">Condiciones</span><span class="sxs-lookup"><span data-stu-id="c7f12-115">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="c7f12-116">Representa las condiciones que, cuando se cumplan, desencadenarán las acciones de regla de una regla.</span><span class="sxs-lookup"><span data-stu-id="c7f12-116">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="c7f12-117">Excepciones</span><span class="sxs-lookup"><span data-stu-id="c7f12-117">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="c7f12-118">Representa las excepciones que representan todas las condiciones de excepción de regla disponibles para una regla de bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="c7f12-118">Represents the exceptions that represent all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c7f12-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="c7f12-119">Text value</span></span>

<span data-ttu-id="c7f12-120">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="c7f12-120">A text value is required.</span></span> <span data-ttu-id="c7f12-121">A continuación se muestran los valores de texto posibles para este elemento:</span><span class="sxs-lookup"><span data-stu-id="c7f12-121">The following are the possible text values for this element:</span></span>
  
- <span data-ttu-id="c7f12-122">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="c7f12-122">Any</span></span>
    
- <span data-ttu-id="c7f12-123">Llamar</span><span class="sxs-lookup"><span data-stu-id="c7f12-123">Call</span></span>
    
- <span data-ttu-id="c7f12-124">DoNotForward</span><span class="sxs-lookup"><span data-stu-id="c7f12-124">DoNotForward</span></span>
    
- <span data-ttu-id="c7f12-125">Realizar</span><span class="sxs-lookup"><span data-stu-id="c7f12-125">FollowUp</span></span>
    
- <span data-ttu-id="c7f12-126">FYI</span><span class="sxs-lookup"><span data-stu-id="c7f12-126">FYI</span></span>
    
- <span data-ttu-id="c7f12-127">Reenviar</span><span class="sxs-lookup"><span data-stu-id="c7f12-127">Forward</span></span>
    
- <span data-ttu-id="c7f12-128">NoResponseNecessary</span><span class="sxs-lookup"><span data-stu-id="c7f12-128">NoResponseNecessary</span></span>
    
- <span data-ttu-id="c7f12-129">Read</span><span class="sxs-lookup"><span data-stu-id="c7f12-129">Read</span></span>
    
- <span data-ttu-id="c7f12-130">Responder</span><span class="sxs-lookup"><span data-stu-id="c7f12-130">Reply</span></span>
    
- <span data-ttu-id="c7f12-131">ReplyToAll</span><span class="sxs-lookup"><span data-stu-id="c7f12-131">ReplyToAll</span></span>
    
- <span data-ttu-id="c7f12-132">Revisar</span><span class="sxs-lookup"><span data-stu-id="c7f12-132">Review</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c7f12-133">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c7f12-133">Remarks</span></span>

<span data-ttu-id="c7f12-134">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="c7f12-134">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c7f12-135">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c7f12-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c7f12-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="c7f12-136">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c7f12-137">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c7f12-137">Schema Name</span></span>  <br/> |<span data-ttu-id="c7f12-138">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="c7f12-138">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c7f12-139">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c7f12-139">Validation File</span></span>  <br/> |<span data-ttu-id="c7f12-140">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="c7f12-140">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c7f12-141">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c7f12-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="c7f12-142">Verdadero</span><span class="sxs-lookup"><span data-stu-id="c7f12-142">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c7f12-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="c7f12-143">See also</span></span>



- [<span data-ttu-id="c7f12-144">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="c7f12-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

