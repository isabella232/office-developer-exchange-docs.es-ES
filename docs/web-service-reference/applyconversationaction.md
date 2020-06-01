---
title: ApplyConversationAction
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ApplyConversationAction
api_type:
- schema
ms.assetid: e0ee8f30-529b-4d87-8bc0-b6616e75fb6b
description: El elemento ApplyConversationAction define una solicitud para aplicar acciones a los elementos de una conversación.
ms.openlocfilehash: 659b3392778bb1a318c3942a0c8e314f12110c12
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461691"
---
# <a name="applyconversationaction"></a><span data-ttu-id="6047d-103">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="6047d-103">ApplyConversationAction</span></span>

<span data-ttu-id="6047d-104">El elemento **ApplyConversationAction** define una solicitud para aplicar acciones a los elementos de una conversación.</span><span class="sxs-lookup"><span data-stu-id="6047d-104">The **ApplyConversationAction** element defines a request to apply actions to items in a conversation.</span></span> 
  
[<span data-ttu-id="6047d-105">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="6047d-105">ApplyConversationAction</span></span>](applyconversationaction.md)
  
```XML
<ApplyConversationAction>
   <ConversationActions/>
</ApplyConversationAction>
```

 <span data-ttu-id="6047d-106">**ApplyConversationActionType**</span><span class="sxs-lookup"><span data-stu-id="6047d-106">**ApplyConversationActionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6047d-107">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="6047d-107">Attributes and elements</span></span>

<span data-ttu-id="6047d-108">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="6047d-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6047d-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="6047d-109">Attributes</span></span>

<span data-ttu-id="6047d-110">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="6047d-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6047d-111">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6047d-111">Child elements</span></span>

|<span data-ttu-id="6047d-112">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6047d-112">**Element**</span></span>|<span data-ttu-id="6047d-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6047d-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6047d-114">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="6047d-114">ConversationActions</span></span>](conversationactions.md) <br/> |<span data-ttu-id="6047d-115">Contiene una colección de conversaciones y las acciones que se aplican a ellas.</span><span class="sxs-lookup"><span data-stu-id="6047d-115">Contains a collection of conversations and the actions to apply to them.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6047d-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6047d-116">Parent elements</span></span>

<span data-ttu-id="6047d-117">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="6047d-117">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="6047d-118">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="6047d-118">Text value</span></span>

<span data-ttu-id="6047d-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="6047d-119">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6047d-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6047d-120">Remarks</span></span>

<span data-ttu-id="6047d-121">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange. este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="6047d-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6047d-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="6047d-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6047d-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="6047d-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="6047d-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="6047d-124">Schema Name</span></span>  <br/> |<span data-ttu-id="6047d-125">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="6047d-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="6047d-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="6047d-126">Validation File</span></span>  <br/> |<span data-ttu-id="6047d-127">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="6047d-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6047d-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="6047d-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="6047d-129">Falso</span><span class="sxs-lookup"><span data-stu-id="6047d-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6047d-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="6047d-130">See also</span></span>

- [<span data-ttu-id="6047d-131">Operación ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="6047d-131">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)
- [<span data-ttu-id="6047d-132">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="6047d-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

