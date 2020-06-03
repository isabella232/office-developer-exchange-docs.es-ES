---
title: GlobalCategories
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GlobalCategories
api_type:
- schema
ms.assetid: 7a1d3f04-4ada-4a31-845e-f1f1ff6e136f
description: El elemento GlobalCategories contiene la lista de categorías para todos los elementos de conversación en un buzón.
ms.openlocfilehash: d608328f8adae56e140affdb36b38605d6f89486
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530123"
---
# <a name="globalcategories"></a><span data-ttu-id="f2d1d-103">GlobalCategories</span><span class="sxs-lookup"><span data-stu-id="f2d1d-103">GlobalCategories</span></span>

<span data-ttu-id="f2d1d-104">El elemento **GlobalCategories** contiene la lista de categorías para todos los elementos de conversación en un buzón.</span><span class="sxs-lookup"><span data-stu-id="f2d1d-104">The **GlobalCategories** element contains the category list for all conversation items in a mailbox.</span></span> 
  
[<span data-ttu-id="f2d1d-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="f2d1d-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="f2d1d-106">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="f2d1d-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="f2d1d-107">Conversación (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="f2d1d-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="f2d1d-108">GlobalCategories</span><span class="sxs-lookup"><span data-stu-id="f2d1d-108">GlobalCategories</span></span>](globalcategories.md)
  
```XML
<GlobalCategories>
   <String/>
</GlobalCategories>
```

 <span data-ttu-id="f2d1d-109">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="f2d1d-109">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f2d1d-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f2d1d-110">Attributes and elements</span></span>

<span data-ttu-id="f2d1d-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f2d1d-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f2d1d-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="f2d1d-112">Attributes</span></span>

<span data-ttu-id="f2d1d-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="f2d1d-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f2d1d-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f2d1d-114">Child elements</span></span>

|<span data-ttu-id="f2d1d-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f2d1d-115">**Element**</span></span>|<span data-ttu-id="f2d1d-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f2d1d-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f2d1d-117">String</span><span class="sxs-lookup"><span data-stu-id="f2d1d-117">String</span></span>](string.md) <br/> |<span data-ttu-id="f2d1d-118">Contiene una única categoría.</span><span class="sxs-lookup"><span data-stu-id="f2d1d-118">Contains a single category.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f2d1d-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f2d1d-119">Parent elements</span></span>

|<span data-ttu-id="f2d1d-120">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f2d1d-120">**Element**</span></span>|<span data-ttu-id="f2d1d-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f2d1d-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f2d1d-122">Conversación (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="f2d1d-122">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="f2d1d-123">Representa una sola conversación.</span><span class="sxs-lookup"><span data-stu-id="f2d1d-123">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f2d1d-124">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="f2d1d-124">Text value</span></span>

<span data-ttu-id="f2d1d-125">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f2d1d-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f2d1d-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f2d1d-126">Remarks</span></span>

<span data-ttu-id="f2d1d-127">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange. este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="f2d1d-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f2d1d-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f2d1d-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f2d1d-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="f2d1d-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f2d1d-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f2d1d-130">Schema name</span></span>  <br/> |<span data-ttu-id="f2d1d-131">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="f2d1d-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="f2d1d-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f2d1d-132">Validation file</span></span>  <br/> |<span data-ttu-id="f2d1d-133">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="f2d1d-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f2d1d-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f2d1d-134">Can be empty</span></span>  <br/> |<span data-ttu-id="f2d1d-135">Falso</span><span class="sxs-lookup"><span data-stu-id="f2d1d-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f2d1d-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="f2d1d-136">See also</span></span>



[<span data-ttu-id="f2d1d-137">Operación FindConversation</span><span class="sxs-lookup"><span data-stu-id="f2d1d-137">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="f2d1d-138">Operación ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="f2d1d-138">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="f2d1d-139">Conversaciones en EWS</span><span class="sxs-lookup"><span data-stu-id="f2d1d-139">Conversations in EWS</span></span>](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

