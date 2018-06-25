---
title: Conversación (ConversationRequestType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0308b71c-d4ff-44a8-b9ca-d5965291ee1d
description: El elemento de conversación representa una sola conversación devuelta en una respuesta de GetConversationItems.
ms.openlocfilehash: ef56e26fda7d2bf6556069355918aa576ce14cb6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763862"
---
# <a name="conversation-conversationrequesttype"></a><span data-ttu-id="a8bc7-103">Conversación (ConversationRequestType)</span><span class="sxs-lookup"><span data-stu-id="a8bc7-103">Conversation (ConversationRequestType)</span></span>

<span data-ttu-id="a8bc7-104">El elemento de **conversación** representa una sola conversación devuelta en una respuesta de **GetConversationItems** .</span><span class="sxs-lookup"><span data-stu-id="a8bc7-104">The **Conversation** element represents a single conversation returned in a **GetConversationItems** response.</span></span> 
  
```XML
<Conversation>
   <ConversationId/>
   <SyncState/>
</Conversation>
```

 ****
## <a name="attributes-and-elements"></a><span data-ttu-id="a8bc7-105">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a8bc7-105">Attributes and elements</span></span>

<span data-ttu-id="a8bc7-106">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a8bc7-106">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a8bc7-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="a8bc7-107">Attributes</span></span>

<span data-ttu-id="a8bc7-108">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a8bc7-108">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a8bc7-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a8bc7-109">Child elements</span></span>

<span data-ttu-id="a8bc7-110">[ConversationId](conversationid.md) | [estado de sincronización (base64Binary)](syncstate-base64binary.md)</span><span class="sxs-lookup"><span data-stu-id="a8bc7-110">[ConversationId](conversationid.md) | [SyncState (base64Binary)](syncstate-base64binary.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a8bc7-111">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a8bc7-111">Parent elements</span></span>

[<span data-ttu-id="a8bc7-112">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="a8bc7-112">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
## <a name="remarks"></a><span data-ttu-id="a8bc7-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a8bc7-113">Remarks</span></span>

<span data-ttu-id="a8bc7-114">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a8bc7-114">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="a8bc7-115">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="a8bc7-115">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a8bc7-116">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a8bc7-116">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a8bc7-117">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a8bc7-117">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a8bc7-118">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a8bc7-118">Schema name</span></span>  <br/> |<span data-ttu-id="a8bc7-119">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="a8bc7-119">Types schema</span></span>  <br/> |
|<span data-ttu-id="a8bc7-120">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a8bc7-120">Validation file</span></span>  <br/> |<span data-ttu-id="a8bc7-121">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a8bc7-121">types.xsd</span></span>  <br/> |
|<span data-ttu-id="a8bc7-122">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a8bc7-122">Can be empty</span></span>  <br/> |<span data-ttu-id="a8bc7-123">falso</span><span class="sxs-lookup"><span data-stu-id="a8bc7-123">false</span></span>  <br/> |
   

