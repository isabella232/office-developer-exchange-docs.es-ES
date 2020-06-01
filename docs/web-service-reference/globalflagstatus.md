---
title: GlobalFlagStatus
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GlobalFlagStatus
api_type:
- schema
ms.assetid: 3ba300f3-3355-4cab-9e77-0dcc2902e712
description: El elemento GlobalFlagStatus contiene el estado de marca agregada para todos los elementos de conversación en un buzón.
ms.openlocfilehash: f9984a1bb7e8205a98dd3ef91f841b48a7ab9389
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459507"
---
# <a name="globalflagstatus"></a><span data-ttu-id="09326-103">GlobalFlagStatus</span><span class="sxs-lookup"><span data-stu-id="09326-103">GlobalFlagStatus</span></span>

<span data-ttu-id="09326-104">El elemento **GlobalFlagStatus** contiene el estado de marca agregada para todos los elementos de conversación en un buzón.</span><span class="sxs-lookup"><span data-stu-id="09326-104">The **GlobalFlagStatus** element contains the aggregated flag status for all conversation items in a mailbox.</span></span> 
  
[<span data-ttu-id="09326-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="09326-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="09326-106">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="09326-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="09326-107">Conversación (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="09326-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="09326-108">GlobalFlagStatus</span><span class="sxs-lookup"><span data-stu-id="09326-108">GlobalFlagStatus</span></span>](globalflagstatus.md)
  
```XML
<GlobalFlagStatus> NotFlagged | Flagged | Complete </GlobalFlagStatus>
```

 <span data-ttu-id="09326-109">**FlagStatusType**</span><span class="sxs-lookup"><span data-stu-id="09326-109">**FlagStatusType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="09326-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="09326-110">Attributes and elements</span></span>

<span data-ttu-id="09326-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="09326-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="09326-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="09326-112">Attributes</span></span>

<span data-ttu-id="09326-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="09326-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="09326-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="09326-114">Child elements</span></span>

<span data-ttu-id="09326-115">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="09326-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="09326-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="09326-116">Parent elements</span></span>

|<span data-ttu-id="09326-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="09326-117">**Element**</span></span>|<span data-ttu-id="09326-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="09326-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="09326-119">Conversación (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="09326-119">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="09326-120">Representa una sola conversación.</span><span class="sxs-lookup"><span data-stu-id="09326-120">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="09326-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="09326-121">Text value</span></span>

<span data-ttu-id="09326-122">El valor de texto del elemento **GlobalFlagStatus** es el estado de marca agregada para los elementos de conversación en la carpeta actual.</span><span class="sxs-lookup"><span data-stu-id="09326-122">The text value of the **GlobalFlagStatus** element is the aggregated flag status for conversation items in the current folder.</span></span> <span data-ttu-id="09326-123">A continuación se muestran los valores de texto posibles:</span><span class="sxs-lookup"><span data-stu-id="09326-123">The following are the possible text values:</span></span> 
  
- <span data-ttu-id="09326-124">**NotFlagged** : indica el estado no marcado.</span><span class="sxs-lookup"><span data-stu-id="09326-124">**NotFlagged** - Indicates the not-flagged status.</span></span> 
    
- <span data-ttu-id="09326-125">**Marcado** : indica el estado marcado.</span><span class="sxs-lookup"><span data-stu-id="09326-125">**Flagged** - Indicates the flagged status.</span></span> 
    
- <span data-ttu-id="09326-126">**Completo** : indica el estado completo de la marca.</span><span class="sxs-lookup"><span data-stu-id="09326-126">**Complete** - Indicates the complete flag status.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="09326-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="09326-127">Remarks</span></span>

<span data-ttu-id="09326-128">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange. este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="09326-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="09326-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="09326-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="09326-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="09326-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="09326-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="09326-131">Schema name</span></span>  <br/> |<span data-ttu-id="09326-132">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="09326-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="09326-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="09326-133">Validation file</span></span>  <br/> |<span data-ttu-id="09326-134">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="09326-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="09326-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="09326-135">Can be empty</span></span>  <br/> |<span data-ttu-id="09326-136">Falso</span><span class="sxs-lookup"><span data-stu-id="09326-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="09326-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="09326-137">See also</span></span>



[<span data-ttu-id="09326-138">Operación FindConversation</span><span class="sxs-lookup"><span data-stu-id="09326-138">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="09326-139">Operación ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="09326-139">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="09326-140">Conversaciones en EWS</span><span class="sxs-lookup"><span data-stu-id="09326-140">Conversations in EWS</span></span>](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

