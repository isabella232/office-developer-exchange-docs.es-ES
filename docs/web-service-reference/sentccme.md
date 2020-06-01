---
title: SentCcMe
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SentCcMe
api_type:
- schema
ms.assetid: bf5044e4-cbdf-4e24-a16f-b6454a51fcd5
description: El elemento SentCcMe indica si el propietario del buzón tiene que estar en la propiedad CcRecipients de los mensajes entrantes para que se aplique la condición o excepción.
ms.openlocfilehash: 1fae56a8e7d4e56c56884e5fff051ecd9f138a6d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465481"
---
# <a name="sentccme"></a><span data-ttu-id="f81d1-103">SentCcMe</span><span class="sxs-lookup"><span data-stu-id="f81d1-103">SentCcMe</span></span>

<span data-ttu-id="f81d1-104">El elemento **SentCcMe** indica si el propietario del buzón tiene que estar en la propiedad **CcRecipients** de los mensajes entrantes para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="f81d1-104">The **SentCcMe** element indicates whether the owner of the mailbox has to be in the **CcRecipients** property of incoming messages in order for the condition or exception to apply.</span></span> 
  
```XML
<SentCcMe>true | false</SentCcMe>
```

 <span data-ttu-id="f81d1-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="f81d1-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f81d1-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f81d1-106">Attributes and elements</span></span>

<span data-ttu-id="f81d1-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f81d1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f81d1-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="f81d1-108">Attributes</span></span>

<span data-ttu-id="f81d1-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="f81d1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f81d1-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f81d1-110">Child elements</span></span>

<span data-ttu-id="f81d1-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="f81d1-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f81d1-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f81d1-112">Parent elements</span></span>

|<span data-ttu-id="f81d1-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f81d1-113">**Element**</span></span>|<span data-ttu-id="f81d1-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f81d1-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f81d1-115">Condiciones</span><span class="sxs-lookup"><span data-stu-id="f81d1-115">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="f81d1-116">Representa las condiciones que, cuando se cumplan, desencadenarán las acciones de regla de una regla.</span><span class="sxs-lookup"><span data-stu-id="f81d1-116">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="f81d1-117">Excepciones</span><span class="sxs-lookup"><span data-stu-id="f81d1-117">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="f81d1-118">Representa todas las condiciones de excepción de regla disponibles para una regla de bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="f81d1-118">Represents all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f81d1-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="f81d1-119">Text value</span></span>

<span data-ttu-id="f81d1-120">Un valor de texto de **true** indica que el propietario del buzón debe estar en la propiedad **CcRecipients** de los mensajes entrantes para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="f81d1-120">A text value of **true** indicates that the owner of the mailbox must be in the **CcRecipients** property of the incoming messages in order for the condition or exception to apply.</span></span> <span data-ttu-id="f81d1-121">Un valor de **false** indica que el propietario del buzón no debe estar en la propiedad **CcRecipients** de los mensajes entrantes para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="f81d1-121">A value of **false** indicates that the owner of the mailbox must not be in the **CcRecipients** property of the incoming messages in order for the condition or exception to apply.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f81d1-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f81d1-122">Remarks</span></span>

<span data-ttu-id="f81d1-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="f81d1-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f81d1-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f81d1-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f81d1-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="f81d1-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f81d1-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f81d1-126">Schema Name</span></span>  <br/> |<span data-ttu-id="f81d1-127">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="f81d1-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="f81d1-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f81d1-128">Validation File</span></span>  <br/> |<span data-ttu-id="f81d1-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="f81d1-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f81d1-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f81d1-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="f81d1-131">Verdadero</span><span class="sxs-lookup"><span data-stu-id="f81d1-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f81d1-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="f81d1-132">See also</span></span>



- [<span data-ttu-id="f81d1-133">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="f81d1-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

