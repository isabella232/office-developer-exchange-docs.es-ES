---
title: SentOnlyToMe
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SentOnlyToMe
api_type:
- schema
ms.assetid: b6d4dea5-812d-4b29-917d-071ebd7ddd92
description: El elemento SentOnlyToMe indica si el propietario del buzón tiene que ser el único de la propiedad ToRecipients de los mensajes entrantes para que se aplique la condición o excepción.
ms.openlocfilehash: 3127550b09d6f5ccf5ba87ad34557afd047f8be0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458652"
---
# <a name="sentonlytome"></a><span data-ttu-id="5b5c8-103">SentOnlyToMe</span><span class="sxs-lookup"><span data-stu-id="5b5c8-103">SentOnlyToMe</span></span>

<span data-ttu-id="5b5c8-104">El elemento **SentOnlyToMe** indica si el propietario del buzón tiene que ser el único de la propiedad **ToRecipients** de los mensajes entrantes para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="5b5c8-104">The **SentOnlyToMe** element indicates whether the owner of the mailbox has to be the only one in the **ToRecipients** property of incoming messages in order for the condition or exception to apply.</span></span> 
  
```XML
<SentOnlyToMe/>true | false</SentOnlyToMe>
```

 <span data-ttu-id="5b5c8-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="5b5c8-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5b5c8-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="5b5c8-106">Attributes and elements</span></span>

<span data-ttu-id="5b5c8-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="5b5c8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5b5c8-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="5b5c8-108">Attributes</span></span>

<span data-ttu-id="5b5c8-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="5b5c8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5b5c8-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5b5c8-110">Child elements</span></span>

<span data-ttu-id="5b5c8-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="5b5c8-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5b5c8-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5b5c8-112">Parent elements</span></span>

|<span data-ttu-id="5b5c8-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="5b5c8-113">**Element**</span></span>|<span data-ttu-id="5b5c8-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5b5c8-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5b5c8-115">Condiciones</span><span class="sxs-lookup"><span data-stu-id="5b5c8-115">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="5b5c8-116">Representa las condiciones que, cuando se cumplan, desencadenarán las acciones de regla de una regla.</span><span class="sxs-lookup"><span data-stu-id="5b5c8-116">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="5b5c8-117">Excepciones</span><span class="sxs-lookup"><span data-stu-id="5b5c8-117">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="5b5c8-118">Representa todas las condiciones de excepción de regla disponibles para una regla de bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="5b5c8-118">Represents all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5b5c8-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="5b5c8-119">Text value</span></span>

<span data-ttu-id="5b5c8-120">Un valor de texto de **true** indica que el propietario del buzón debe ser el único en la propiedad **ToRecipients** de los mensajes entrantes para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="5b5c8-120">A text value of **true** indicates that the owner of the mailbox must be the only one in the **ToRecipients** property of the incoming messages in order for the condition or exception to apply.</span></span> <span data-ttu-id="5b5c8-121">Un valor de **false** indica que el propietario del buzón no debe ser el único en la propiedad **ToRecipients** de los mensajes entrantes para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="5b5c8-121">A value of **false** indicates that the owner of the mailbox must not be the only one in the **ToRecipients** property of the incoming messages in order for the condition or exception to apply.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5b5c8-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5b5c8-122">Remarks</span></span>

<span data-ttu-id="5b5c8-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="5b5c8-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5b5c8-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="5b5c8-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5b5c8-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="5b5c8-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="5b5c8-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="5b5c8-126">Schema Name</span></span>  <br/> |<span data-ttu-id="5b5c8-127">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="5b5c8-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="5b5c8-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="5b5c8-128">Validation File</span></span>  <br/> |<span data-ttu-id="5b5c8-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="5b5c8-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="5b5c8-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="5b5c8-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="5b5c8-131">Verdadero</span><span class="sxs-lookup"><span data-stu-id="5b5c8-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5b5c8-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="5b5c8-132">See also</span></span>



- [<span data-ttu-id="5b5c8-133">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="5b5c8-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

