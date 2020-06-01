---
title: MailboxScope
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c9778823-f290-4827-ba19-5f391ed4f877
description: El elemento MailboxScope identifica si una búsqueda o búsqueda para una conversación debe abarcar el buzón principal, el buzón de archivo o bien el buzón de archivo y el principal.
ms.openlocfilehash: 92823c06d4fe186917c3cfb532eda821bd6a95a7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455376"
---
# <a name="mailboxscope"></a><span data-ttu-id="00183-103">MailboxScope</span><span class="sxs-lookup"><span data-stu-id="00183-103">MailboxScope</span></span>

<span data-ttu-id="00183-104">El elemento **MailboxScope** identifica si una búsqueda o búsqueda para una conversación debe abarcar el buzón principal, el buzón de archivo o bien el buzón de archivo y el principal.</span><span class="sxs-lookup"><span data-stu-id="00183-104">The **MailboxScope** element identifies whether a search or fetch for a conversation should span either the primary mailbox, archive mailbox, or both the primary and archive mailbox.</span></span> 
  
```XML
<MailboxScope> PrimaryOnly | ArchiveOnly | All </MailboxScope>
```

<span data-ttu-id="00183-105">**MailboxSearchLocationType**</span><span class="sxs-lookup"><span data-stu-id="00183-105">**MailboxSearchLocationType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="00183-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="00183-106">Attributes and elements</span></span>

<span data-ttu-id="00183-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="00183-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="00183-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="00183-108">Attributes</span></span>

<span data-ttu-id="00183-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="00183-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="00183-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="00183-110">Child elements</span></span>

<span data-ttu-id="00183-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="00183-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="00183-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="00183-112">Parent elements</span></span>

<span data-ttu-id="00183-113">[FindConversation](findconversation.md)  |  [GetConversationItems](getconversationitems.md)  |  [Conversación (ConversationType)](conversation-conversationtype.md)</span><span class="sxs-lookup"><span data-stu-id="00183-113">[FindConversation](findconversation.md) | [GetConversationItems](getconversationitems.md) | [Conversation (ConversationType)](conversation-conversationtype.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="00183-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="00183-114">Text value</span></span>

<span data-ttu-id="00183-115">El valor de texto del elemento **MailboxScope** es el ámbito para buscar u obtener elementos en una conversación en buzones de correo principales, buzones de correo de archivo o tanto en buzones de correo principales como de archivo.</span><span class="sxs-lookup"><span data-stu-id="00183-115">The text value of the **MailboxScope** element is the scope for finding or getting items in a conversation across either primary mailboxes, archive mailboxes, or both primary and archive mailboxes.</span></span> <span data-ttu-id="00183-116">Un valor de texto de **PrimaryOnly** indica un ámbito que tiene como destino el buzón principal de un usuario.</span><span class="sxs-lookup"><span data-stu-id="00183-116">A text value of **PrimaryOnly** indicates a scope that targets the primary mailbox for a user.</span></span> <span data-ttu-id="00183-117">Un valor de texto de **ArchiveOnly** indica un ámbito que tiene como destino el buzón de archivo de un usuario.</span><span class="sxs-lookup"><span data-stu-id="00183-117">A text value of **ArchiveOnly** indicates a scope that targets the archive mailbox for a user.</span></span> <span data-ttu-id="00183-118">Un valor de texto de **All** indica un ámbito que tiene como destino el buzón principal y el buzón de archivo.</span><span class="sxs-lookup"><span data-stu-id="00183-118">A text value of **All** indicates a scope that targets both the primary mailbox and archive mailbox.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="00183-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="00183-119">Remarks</span></span>

<span data-ttu-id="00183-120">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="00183-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="00183-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="00183-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="00183-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="00183-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="00183-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="00183-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="00183-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="00183-124">Schema name</span></span>  <br/> |<span data-ttu-id="00183-125">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="00183-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="00183-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="00183-126">Validation file</span></span>  <br/> |<span data-ttu-id="00183-127">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="00183-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="00183-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="00183-128">Can be empty</span></span>  <br/> |<span data-ttu-id="00183-129">false</span><span class="sxs-lookup"><span data-stu-id="00183-129">false</span></span>  <br/> |
   

