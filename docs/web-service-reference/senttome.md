---
title: SentToMe
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SentToMe
api_type:
- schema
ms.assetid: f18aecd1-ad33-41c3-b275-4ca648ce1da0
description: El elemento SentToMe indica si el propietario del buzón tiene que estar en la propiedad ToRecipients de los mensajes entrantes para que se aplique la condición o excepción.
ms.openlocfilehash: 830125f03ad91a3e6f2beaf11e41be5e940ed48b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44439927"
---
# <a name="senttome"></a><span data-ttu-id="5fc71-103">SentToMe</span><span class="sxs-lookup"><span data-stu-id="5fc71-103">SentToMe</span></span>

<span data-ttu-id="5fc71-104">El elemento **SentToMe** indica si el propietario del buzón tiene que estar en la propiedad **ToRecipients** de los mensajes entrantes para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="5fc71-104">The **SentToMe** element indicates whether the owner of the mailbox has to be in the **ToRecipients** property of incoming messages in order for the condition or exception to apply.</span></span> 
  
```XML
<SentToMe>true | false</SentToMe>
```

 <span data-ttu-id="5fc71-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="5fc71-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5fc71-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="5fc71-106">Attributes and elements</span></span>

<span data-ttu-id="5fc71-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="5fc71-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5fc71-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="5fc71-108">Attributes</span></span>

<span data-ttu-id="5fc71-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="5fc71-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5fc71-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5fc71-110">Child elements</span></span>

<span data-ttu-id="5fc71-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="5fc71-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5fc71-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5fc71-112">Parent elements</span></span>

|<span data-ttu-id="5fc71-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="5fc71-113">**Element**</span></span>|<span data-ttu-id="5fc71-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5fc71-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5fc71-115">Condiciones</span><span class="sxs-lookup"><span data-stu-id="5fc71-115">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="5fc71-116">Representa las condiciones que, cuando se cumplan, desencadenarán las acciones de regla de una regla.</span><span class="sxs-lookup"><span data-stu-id="5fc71-116">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="5fc71-117">Excepciones</span><span class="sxs-lookup"><span data-stu-id="5fc71-117">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="5fc71-118">Representa todas las condiciones de excepción de regla disponibles para una regla de bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="5fc71-118">Represents all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5fc71-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="5fc71-119">Text value</span></span>

<span data-ttu-id="5fc71-120">Un valor de texto de **true** indica que el propietario del buzón debe estar en la propiedad **ToRecipients** de los mensajes entrantes para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="5fc71-120">A text value of **true** indicates that the owner of the mailbox must be in the **ToRecipients** property of the incoming messages in order for the condition or exception to apply.</span></span> <span data-ttu-id="5fc71-121">Un valor de **false** indica que el propietario del buzón no debe estar en la propiedad **ToRecipients** de los mensajes entrantes para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="5fc71-121">A value of **false** indicates that the owner of the mailbox must not be in the **ToRecipients** property of the incoming messages in order for the condition or exception to apply.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5fc71-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5fc71-122">Remarks</span></span>

<span data-ttu-id="5fc71-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="5fc71-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5fc71-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="5fc71-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5fc71-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="5fc71-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="5fc71-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="5fc71-126">Schema Name</span></span>  <br/> |<span data-ttu-id="5fc71-127">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="5fc71-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="5fc71-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="5fc71-128">Validation File</span></span>  <br/> |<span data-ttu-id="5fc71-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="5fc71-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="5fc71-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="5fc71-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="5fc71-131">Verdadero</span><span class="sxs-lookup"><span data-stu-id="5fc71-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5fc71-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="5fc71-132">See also</span></span>



- [<span data-ttu-id="5fc71-133">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="5fc71-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

