---
title: GlobalHasAttachments
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GlobalHasAttachments
api_type:
- schema
ms.assetid: 3d075e93-14bc-479d-957f-9b7873d1db39
description: El elemento GlobalHasAttachments contiene un valor que indica si el elemento de al menos una conversación en un buzón tiene datos adjuntos.
ms.openlocfilehash: 85443c45f611a2f4bff392ffecb26029564d7558
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835715"
---
# <a name="globalhasattachments"></a><span data-ttu-id="622cf-103">GlobalHasAttachments</span><span class="sxs-lookup"><span data-stu-id="622cf-103">GlobalHasAttachments</span></span>

<span data-ttu-id="622cf-104">El elemento **GlobalHasAttachments** contiene un valor que indica si el elemento de al menos una conversación en un buzón tiene datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="622cf-104">The **GlobalHasAttachments** element contains a value that indicates whether at least one conversation item in a mailbox has an attachment.</span></span> 
  
[<span data-ttu-id="622cf-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="622cf-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="622cf-106">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="622cf-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="622cf-107">Conversación (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="622cf-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="622cf-108">GlobalHasAttachments</span><span class="sxs-lookup"><span data-stu-id="622cf-108">GlobalHasAttachments</span></span>](globalhasattachments.md)
  
```XML
<GlobalHasAttachments/>
```

 <span data-ttu-id="622cf-109">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="622cf-109">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="622cf-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="622cf-110">Attributes and elements</span></span>

<span data-ttu-id="622cf-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="622cf-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="622cf-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="622cf-112">Attributes</span></span>

<span data-ttu-id="622cf-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="622cf-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="622cf-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="622cf-114">Child elements</span></span>

<span data-ttu-id="622cf-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="622cf-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="622cf-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="622cf-116">Parent elements</span></span>

|<span data-ttu-id="622cf-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="622cf-117">**Element**</span></span>|<span data-ttu-id="622cf-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="622cf-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="622cf-119">Conversación (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="622cf-119">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="622cf-120">Representa una sola conversación.</span><span class="sxs-lookup"><span data-stu-id="622cf-120">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="622cf-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="622cf-121">Text value</span></span>

<span data-ttu-id="622cf-122">El valor del elemento **GlobalHasAttachments** indica si el elemento de al menos una conversación en un buzón de correo tiene datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="622cf-122">The value of the **GlobalHasAttachments** element indicates whether at least one conversation item in a mailbox has an attachment.</span></span> <span data-ttu-id="622cf-123">Se requiere un valor de texto que representa un valor de tipo Boolean.</span><span class="sxs-lookup"><span data-stu-id="622cf-123">A text value that represents a Boolean value is required.</span></span> <span data-ttu-id="622cf-124">Un valor de **true** significa que la conversación tiene al menos un dato adjunto visible.</span><span class="sxs-lookup"><span data-stu-id="622cf-124">A value of **true** means that the conversation has at least one visible attachment.</span></span> <span data-ttu-id="622cf-125">Un valor de **false** significa que la conversación no tiene datos adjuntos o sólo oculta los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="622cf-125">A value of **false** means that the conversation either has no attachments or has only hidden attachments.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="622cf-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="622cf-126">Remarks</span></span>

<span data-ttu-id="622cf-127">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda Exchange Web Services.This elemento fue introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="622cf-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="622cf-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="622cf-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="622cf-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="622cf-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="622cf-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="622cf-130">Schema name</span></span>  <br/> |<span data-ttu-id="622cf-131">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="622cf-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="622cf-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="622cf-132">Validation file</span></span>  <br/> |<span data-ttu-id="622cf-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="622cf-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="622cf-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="622cf-134">Can be empty</span></span>  <br/> |<span data-ttu-id="622cf-135">False</span><span class="sxs-lookup"><span data-stu-id="622cf-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="622cf-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="622cf-136">See also</span></span>



[<span data-ttu-id="622cf-137">Operación de FindConversation</span><span class="sxs-lookup"><span data-stu-id="622cf-137">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="622cf-138">Operación ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="622cf-138">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="622cf-139">Conversaciones de EWS</span><span class="sxs-lookup"><span data-stu-id="622cf-139">Conversations in EWS</span></span>](http://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)
