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
description: El elemento ApplyConversationAction define una solicitud para aplicar acciones a los elementos en una conversación.
ms.openlocfilehash: 1b672c6e6d2f60e50215417be7100e9cd77e2a58
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763529"
---
# <a name="applyconversationaction"></a><span data-ttu-id="d9ea9-103">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="d9ea9-103">ApplyConversationAction</span></span>

<span data-ttu-id="d9ea9-104">El elemento **ApplyConversationAction** define una solicitud para aplicar acciones a los elementos en una conversación.</span><span class="sxs-lookup"><span data-stu-id="d9ea9-104">The **ApplyConversationAction** element defines a request to apply actions to items in a conversation.</span></span> 
  
[<span data-ttu-id="d9ea9-105">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="d9ea9-105">ApplyConversationAction</span></span>](applyconversationaction.md)
  
```XML
<ApplyConversationAction>
   <ConversationActions/>
</ApplyConversationAction>
```

 <span data-ttu-id="d9ea9-106">**ApplyConversationActionType**</span><span class="sxs-lookup"><span data-stu-id="d9ea9-106">**ApplyConversationActionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d9ea9-107">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d9ea9-107">Attributes and elements</span></span>

<span data-ttu-id="d9ea9-108">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d9ea9-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d9ea9-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="d9ea9-109">Attributes</span></span>

<span data-ttu-id="d9ea9-110">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d9ea9-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d9ea9-111">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d9ea9-111">Child elements</span></span>

|<span data-ttu-id="d9ea9-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="d9ea9-112">**Element**</span></span>|<span data-ttu-id="d9ea9-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d9ea9-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d9ea9-114">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="d9ea9-114">ConversationActions</span></span>](conversationactions.md) <br/> |<span data-ttu-id="d9ea9-115">Contiene una colección de las conversaciones y las acciones que se debe aplicar a ellos.</span><span class="sxs-lookup"><span data-stu-id="d9ea9-115">Contains a collection of conversations and the actions to apply to them.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d9ea9-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d9ea9-116">Parent elements</span></span>

<span data-ttu-id="d9ea9-117">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d9ea9-117">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="d9ea9-118">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="d9ea9-118">Text value</span></span>

<span data-ttu-id="d9ea9-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d9ea9-119">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d9ea9-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d9ea9-120">Remarks</span></span>

<span data-ttu-id="d9ea9-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda Exchange Web Services.This elemento fue introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="d9ea9-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d9ea9-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d9ea9-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d9ea9-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d9ea9-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d9ea9-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d9ea9-124">Schema Name</span></span>  <br/> |<span data-ttu-id="d9ea9-125">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="d9ea9-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d9ea9-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d9ea9-126">Validation File</span></span>  <br/> |<span data-ttu-id="d9ea9-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="d9ea9-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d9ea9-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d9ea9-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="d9ea9-129">False</span><span class="sxs-lookup"><span data-stu-id="d9ea9-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d9ea9-130">Ver también</span><span class="sxs-lookup"><span data-stu-id="d9ea9-130">See also</span></span>

- [<span data-ttu-id="d9ea9-131">Operación ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="d9ea9-131">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)
- [<span data-ttu-id="d9ea9-132">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="d9ea9-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

