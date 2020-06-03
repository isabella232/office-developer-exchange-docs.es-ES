---
title: GetConversationItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4f7bcd0f-140c-4cbc-a5ed-daeffded1df1
description: El elemento GetConversationItems define una solicitud para obtener un conjunto de elementos que están relacionados por estar en la misma conversación.
ms.openlocfilehash: cde4bc2c39ccbc51b7436c87c4bc06e3b8d7e52c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457749"
---
# <a name="getconversationitems"></a><span data-ttu-id="a0814-103">GetConversationItems</span><span class="sxs-lookup"><span data-stu-id="a0814-103">GetConversationItems</span></span>

<span data-ttu-id="a0814-104">El elemento **GetConversationItems** define una solicitud para obtener un conjunto de elementos que están relacionados por estar en la misma conversación.</span><span class="sxs-lookup"><span data-stu-id="a0814-104">The **GetConversationItems** element defines a request to get a set of items that are related by being in the same conversation.</span></span> 
  
```XML
<GetConversationItems>
   <ItemShape/>
   <FoldersToIgnore/>
   <MaxItemsToReturn/>
   <SortOrder/>
   <MailboxScope/>
   <Conversations/>
</GetConversationItems>
```

 <span data-ttu-id="a0814-105">**GetConversationItemsType**</span><span class="sxs-lookup"><span data-stu-id="a0814-105">**GetConversationItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a0814-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a0814-106">Attributes and elements</span></span>

<span data-ttu-id="a0814-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a0814-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a0814-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="a0814-108">Attributes</span></span>

<span data-ttu-id="a0814-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="a0814-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a0814-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a0814-110">Child elements</span></span>

<span data-ttu-id="a0814-111">[ItemShape](itemshape.md)  |  [FoldersToIgnore](folderstoignore.md)  |  [MaxItemsToReturn](maxitemstoreturn.md)  |  [SortOrder (ConversationNodeSortOrder)](sortorder-conversationnodesortorder.md)  |  [MailboxScope](mailboxscope.md)  |  [Conversaciones](conversations-ex15websvcsotherref.md)</span><span class="sxs-lookup"><span data-stu-id="a0814-111">[ItemShape](itemshape.md) | [FoldersToIgnore](folderstoignore.md) | [MaxItemsToReturn](maxitemstoreturn.md) | [SortOrder (ConversationNodeSortOrder)](sortorder-conversationnodesortorder.md) | [MailboxScope](mailboxscope.md) | [Conversations](conversations-ex15websvcsotherref.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a0814-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a0814-112">Parent elements</span></span>

<span data-ttu-id="a0814-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a0814-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a0814-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a0814-114">Remarks</span></span>

<span data-ttu-id="a0814-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a0814-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="a0814-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="a0814-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a0814-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a0814-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a0814-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="a0814-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a0814-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a0814-119">Schema name</span></span>  <br/> |<span data-ttu-id="a0814-120">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="a0814-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a0814-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a0814-121">Validation file</span></span>  <br/> |<span data-ttu-id="a0814-122">messages. xsd</span><span class="sxs-lookup"><span data-stu-id="a0814-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a0814-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a0814-123">Can be empty</span></span>  <br/> |<span data-ttu-id="a0814-124">false</span><span class="sxs-lookup"><span data-stu-id="a0814-124">false</span></span>  <br/> |
   

