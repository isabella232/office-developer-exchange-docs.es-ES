---
title: GlobalLastDeliveryTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GlobalLastDeliveryTime
api_type:
- schema
ms.assetid: a88dada9-c527-43a7-b2d3-31aad330def9
description: El elemento GlobalLastDeliveryTime contiene la hora de entrega del mensaje que se recibió por última vez en esta conversación en todas las carpetas del buzón.
ms.openlocfilehash: b6d4d7c1d51c206e44973a717d25df4066845ada
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459415"
---
# <a name="globallastdeliverytime"></a><span data-ttu-id="c5166-103">GlobalLastDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="c5166-103">GlobalLastDeliveryTime</span></span>

<span data-ttu-id="c5166-104">El elemento **GlobalLastDeliveryTime** contiene la hora de entrega del mensaje que se recibió por última vez en esta conversación en todas las carpetas del buzón.</span><span class="sxs-lookup"><span data-stu-id="c5166-104">The **GlobalLastDeliveryTime** element contains the delivery time of the message that was last received in this conversation across all folders in the mailbox.</span></span> 
  
[<span data-ttu-id="c5166-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="c5166-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="c5166-106">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="c5166-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="c5166-107">Conversación (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="c5166-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="c5166-108">GlobalLastDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="c5166-108">GlobalLastDeliveryTime</span></span>](globallastdeliverytime.md)
  
```XML
<GlobalLastDeliveryTime/>
```

 <span data-ttu-id="c5166-109">**XS: dateTime**</span><span class="sxs-lookup"><span data-stu-id="c5166-109">**xs:dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c5166-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c5166-110">Attributes and elements</span></span>

<span data-ttu-id="c5166-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c5166-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c5166-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="c5166-112">Attributes</span></span>

<span data-ttu-id="c5166-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c5166-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c5166-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c5166-114">Child elements</span></span>

<span data-ttu-id="c5166-115">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c5166-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c5166-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c5166-116">Parent elements</span></span>

|<span data-ttu-id="c5166-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c5166-117">**Element**</span></span>|<span data-ttu-id="c5166-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c5166-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c5166-119">Conversación (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="c5166-119">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="c5166-120">Representa una sola conversación.</span><span class="sxs-lookup"><span data-stu-id="c5166-120">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c5166-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="c5166-121">Text value</span></span>

<span data-ttu-id="c5166-122">El valor de texto del elemento **GlobalLastDeliveryTime** es la fecha y la hora del mensaje que se recibió por última vez en esta conversación en todas las carpetas del buzón.</span><span class="sxs-lookup"><span data-stu-id="c5166-122">The text value of the **GlobalLastDeliveryTime** element is the date and time of the message that was last received in this conversation across all folders in the mailbox.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c5166-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c5166-123">Remarks</span></span>

<span data-ttu-id="c5166-124">Este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1). El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c5166-124">This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c5166-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c5166-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c5166-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="c5166-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c5166-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c5166-127">Schema name</span></span>  <br/> |<span data-ttu-id="c5166-128">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="c5166-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="c5166-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c5166-129">Validation file</span></span>  <br/> |<span data-ttu-id="c5166-130">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="c5166-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c5166-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c5166-131">Can be empty</span></span>  <br/> |<span data-ttu-id="c5166-132">Falso</span><span class="sxs-lookup"><span data-stu-id="c5166-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c5166-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="c5166-133">See also</span></span>



[<span data-ttu-id="c5166-134">Operación FindConversation</span><span class="sxs-lookup"><span data-stu-id="c5166-134">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="c5166-135">Operación ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="c5166-135">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="c5166-136">Conversaciones en EWS</span><span class="sxs-lookup"><span data-stu-id="c5166-136">Conversations in EWS</span></span>](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

