---
title: SentToOrCcMe
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SentToOrCcMe
api_type:
- schema
ms.assetid: ca43e05d-df37-485b-9276-34678025f2b7
description: El elemento SentToOrCcMe indica si el propietario del buzón tiene que estar en un ToRecipients o CcRecipients propiedad de los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.
ms.openlocfilehash: baed8f71349c9ec06173d0b494ece688f6fc2c5a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837361"
---
# <a name="senttoorccme"></a><span data-ttu-id="7dc54-103">SentToOrCcMe</span><span class="sxs-lookup"><span data-stu-id="7dc54-103">SentToOrCcMe</span></span>

<span data-ttu-id="7dc54-104">El elemento **SentToOrCcMe** indica si el propietario del buzón tiene que estar en un **ToRecipients** o **CcRecipients** propiedad de los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="7dc54-104">The **SentToOrCcMe** element indicates whether the owner of the mailbox has to be in either a **ToRecipients** or **CcRecipients** property of incoming messages in order for the condition or exception to apply.</span></span> 
  
```XML
<SentToOrCcMe>true | false</SentToOrCcMe>
```

 <span data-ttu-id="7dc54-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="7dc54-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7dc54-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="7dc54-106">Attributes and elements</span></span>

<span data-ttu-id="7dc54-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="7dc54-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7dc54-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="7dc54-108">Attributes</span></span>

<span data-ttu-id="7dc54-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7dc54-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7dc54-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7dc54-110">Child elements</span></span>

<span data-ttu-id="7dc54-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7dc54-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7dc54-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7dc54-112">Parent elements</span></span>

|<span data-ttu-id="7dc54-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="7dc54-113">**Element**</span></span>|<span data-ttu-id="7dc54-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7dc54-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7dc54-115">Condiciones</span><span class="sxs-lookup"><span data-stu-id="7dc54-115">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="7dc54-116">Representa las condiciones que, cuando se cumplen los requisitos, se activará las acciones de regla para una regla.</span><span class="sxs-lookup"><span data-stu-id="7dc54-116">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="7dc54-117">Excepciones</span><span class="sxs-lookup"><span data-stu-id="7dc54-117">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="7dc54-118">Representa todas las condiciones de excepción de regla disponibles para una regla de bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="7dc54-118">Represents all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7dc54-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="7dc54-119">Text value</span></span>

<span data-ttu-id="7dc54-120">Un valor de texto de **true** indica que debe ser el propietario del buzón en la propiedad **ToRecipients** o **CcRecipients** de los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="7dc54-120">A text value of **true** indicates that the owner of the mailbox must be in the **ToRecipients** or **CcRecipients** property of the incoming messages in order for the condition or exception to apply.</span></span> <span data-ttu-id="7dc54-121">Un valor de **false** indica que no debe ser el propietario del buzón en la propiedad **ToRecipients** o **CcRecipients** de los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="7dc54-121">A value of **false** indicates that the owner of the mailbox must not be in the **ToRecipients** or **CcRecipients** property of the incoming messages in order for the condition or exception to apply.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7dc54-122">Notas</span><span class="sxs-lookup"><span data-stu-id="7dc54-122">Remarks</span></span>

<span data-ttu-id="7dc54-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="7dc54-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7dc54-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7dc54-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7dc54-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7dc54-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="7dc54-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="7dc54-126">Schema Name</span></span>  <br/> |<span data-ttu-id="7dc54-127">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="7dc54-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="7dc54-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="7dc54-128">Validation File</span></span>  <br/> |<span data-ttu-id="7dc54-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="7dc54-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7dc54-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="7dc54-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="7dc54-131">Verdadero</span><span class="sxs-lookup"><span data-stu-id="7dc54-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7dc54-132">Ver también</span><span class="sxs-lookup"><span data-stu-id="7dc54-132">See also</span></span>



- [<span data-ttu-id="7dc54-133">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="7dc54-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

