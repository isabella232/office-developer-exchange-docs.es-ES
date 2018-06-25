---
title: MailboxScope
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c9778823-f290-4827-ba19-5f391ed4f877
description: El elemento MailboxScope identifica si una búsqueda u obtención de una conversación debe abarcar el buzón principal, buzón de archivo o ambos la principal y archivar el buzón de correo.
ms.openlocfilehash: 89c9776079d686b114d6b744150f1c6df3711eab
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836293"
---
# <a name="mailboxscope"></a><span data-ttu-id="6774d-103">MailboxScope</span><span class="sxs-lookup"><span data-stu-id="6774d-103">MailboxScope</span></span>

<span data-ttu-id="6774d-104">El elemento **MailboxScope** identifica si una búsqueda u obtención de una conversación debe abarcar el buzón principal, buzón de archivo o ambos la principal y archivar el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="6774d-104">The **MailboxScope** element identifies whether a search or fetch for a conversation should span either the primary mailbox, archive mailbox, or both the primary and archive mailbox.</span></span> 
  
```XML
<MailboxScope> PrimaryOnly | ArchiveOnly | All </MailboxScope>
```

<span data-ttu-id="6774d-105">**MailboxSearchLocationType**</span><span class="sxs-lookup"><span data-stu-id="6774d-105">**MailboxSearchLocationType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="6774d-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="6774d-106">Attributes and elements</span></span>

<span data-ttu-id="6774d-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="6774d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6774d-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="6774d-108">Attributes</span></span>

<span data-ttu-id="6774d-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="6774d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6774d-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6774d-110">Child elements</span></span>

<span data-ttu-id="6774d-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="6774d-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6774d-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6774d-112">Parent elements</span></span>

<span data-ttu-id="6774d-113">[FindConversation](findconversation.md) | [GetConversationItems](getconversationitems.md) | [conversación (ConversationType)](conversation-conversationtype.md)</span><span class="sxs-lookup"><span data-stu-id="6774d-113">[FindConversation](findconversation.md) | [GetConversationItems](getconversationitems.md) | [Conversation (ConversationType)](conversation-conversationtype.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="6774d-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="6774d-114">Text value</span></span>

<span data-ttu-id="6774d-115">El valor de texto del elemento **MailboxScope** es el ámbito de búsqueda u obtener elementos en una conversación entre ambos buzones de correo principales, archivar los buzones de correo, o ambos primaria y buzones de archivo.</span><span class="sxs-lookup"><span data-stu-id="6774d-115">The text value of the **MailboxScope** element is the scope for finding or getting items in a conversation across either primary mailboxes, archive mailboxes, or both primary and archive mailboxes.</span></span> <span data-ttu-id="6774d-116">Un valor de texto de **PrimaryOnly** indica un ámbito que se dirige el buzón principal para un usuario.</span><span class="sxs-lookup"><span data-stu-id="6774d-116">A text value of **PrimaryOnly** indicates a scope that targets the primary mailbox for a user.</span></span> <span data-ttu-id="6774d-117">Un valor de texto de **ArchiveOnly** indica un ámbito que se dirige el buzón de archivo para un usuario.</span><span class="sxs-lookup"><span data-stu-id="6774d-117">A text value of **ArchiveOnly** indicates a scope that targets the archive mailbox for a user.</span></span> <span data-ttu-id="6774d-118">Un valor de texto de **todos los** indica un ámbito que se dirige el buzón principal y el buzón de archivo.</span><span class="sxs-lookup"><span data-stu-id="6774d-118">A text value of **All** indicates a scope that targets both the primary mailbox and archive mailbox.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6774d-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6774d-119">Remarks</span></span>

<span data-ttu-id="6774d-120">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6774d-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="6774d-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="6774d-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6774d-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="6774d-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6774d-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6774d-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="6774d-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="6774d-124">Schema name</span></span>  <br/> |<span data-ttu-id="6774d-125">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="6774d-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="6774d-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="6774d-126">Validation file</span></span>  <br/> |<span data-ttu-id="6774d-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="6774d-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6774d-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="6774d-128">Can be empty</span></span>  <br/> |<span data-ttu-id="6774d-129">falso</span><span class="sxs-lookup"><span data-stu-id="6774d-129">false</span></span>  <br/> |
   

