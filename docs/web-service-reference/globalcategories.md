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
description: El elemento GlobalCategories contiene la lista de categorías para todos los elementos de la conversación en un buzón de correo.
ms.openlocfilehash: 5cedea821b14264f15026c2d297c3017534ca354
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835711"
---
# <a name="globalcategories"></a><span data-ttu-id="abc02-103">GlobalCategories</span><span class="sxs-lookup"><span data-stu-id="abc02-103">GlobalCategories</span></span>

<span data-ttu-id="abc02-104">El elemento **GlobalCategories** contiene la lista de categorías para todos los elementos de la conversación en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="abc02-104">The **GlobalCategories** element contains the category list for all conversation items in a mailbox.</span></span> 
  
[<span data-ttu-id="abc02-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="abc02-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="abc02-106">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="abc02-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="abc02-107">Conversación (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="abc02-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="abc02-108">GlobalCategories</span><span class="sxs-lookup"><span data-stu-id="abc02-108">GlobalCategories</span></span>](globalcategories.md)
  
```XML
<GlobalCategories>
   <String/>
</GlobalCategories>
```

 <span data-ttu-id="abc02-109">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="abc02-109">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="abc02-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="abc02-110">Attributes and elements</span></span>

<span data-ttu-id="abc02-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="abc02-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="abc02-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="abc02-112">Attributes</span></span>

<span data-ttu-id="abc02-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="abc02-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="abc02-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="abc02-114">Child elements</span></span>

|<span data-ttu-id="abc02-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="abc02-115">**Element**</span></span>|<span data-ttu-id="abc02-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="abc02-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="abc02-117">String</span><span class="sxs-lookup"><span data-stu-id="abc02-117">String</span></span>](string.md) <br/> |<span data-ttu-id="abc02-118">Contiene una única categoría.</span><span class="sxs-lookup"><span data-stu-id="abc02-118">Contains a single category.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="abc02-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="abc02-119">Parent elements</span></span>

|<span data-ttu-id="abc02-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="abc02-120">**Element**</span></span>|<span data-ttu-id="abc02-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="abc02-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="abc02-122">Conversación (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="abc02-122">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="abc02-123">Representa una sola conversación.</span><span class="sxs-lookup"><span data-stu-id="abc02-123">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="abc02-124">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="abc02-124">Text value</span></span>

<span data-ttu-id="abc02-125">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="abc02-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="abc02-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="abc02-126">Remarks</span></span>

<span data-ttu-id="abc02-127">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda Exchange Web Services.This elemento fue introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="abc02-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="abc02-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="abc02-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="abc02-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="abc02-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="abc02-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="abc02-130">Schema name</span></span>  <br/> |<span data-ttu-id="abc02-131">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="abc02-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="abc02-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="abc02-132">Validation file</span></span>  <br/> |<span data-ttu-id="abc02-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="abc02-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="abc02-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="abc02-134">Can be empty</span></span>  <br/> |<span data-ttu-id="abc02-135">False</span><span class="sxs-lookup"><span data-stu-id="abc02-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="abc02-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="abc02-136">See also</span></span>



[<span data-ttu-id="abc02-137">Operación de FindConversation</span><span class="sxs-lookup"><span data-stu-id="abc02-137">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="abc02-138">Operación ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="abc02-138">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="abc02-139">Conversaciones de EWS</span><span class="sxs-lookup"><span data-stu-id="abc02-139">Conversations in EWS</span></span>](http://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

