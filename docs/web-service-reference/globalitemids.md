---
title: GlobalItemIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GlobalItemIds
api_type:
- schema
ms.assetid: b0f03ce0-a4c3-47de-9360-a880a3606e42
description: El elemento GlobalItemIds contiene la colección de identificadores de elemento para todos los elementos de conversación en un buzón.
ms.openlocfilehash: aa656e7f2fb78dafe5bf6013c1f7ad14e2372ba1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459429"
---
# <a name="globalitemids"></a><span data-ttu-id="86845-103">GlobalItemIds</span><span class="sxs-lookup"><span data-stu-id="86845-103">GlobalItemIds</span></span>

<span data-ttu-id="86845-104">El elemento **GlobalItemIds** contiene la colección de identificadores de elemento para todos los elementos de conversación en un buzón.</span><span class="sxs-lookup"><span data-stu-id="86845-104">The **GlobalItemIds** element contains the collection of item identifiers for all conversation items in a mailbox.</span></span> 
  
[<span data-ttu-id="86845-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="86845-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="86845-106">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="86845-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="86845-107">Conversación (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="86845-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="86845-108">GlobalItemIds</span><span class="sxs-lookup"><span data-stu-id="86845-108">GlobalItemIds</span></span>](globalitemids.md)
  
```XML
<ItemIds>
   <ItemId/>
   <OccurrenceItemId/>
   <RecurringMasterItemId/>
</ItemIds>
```

 <span data-ttu-id="86845-109">**NonEmptyArrayOfBaseItemIdsType**</span><span class="sxs-lookup"><span data-stu-id="86845-109">**NonEmptyArrayOfBaseItemIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="86845-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="86845-110">Attributes and elements</span></span>

<span data-ttu-id="86845-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="86845-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="86845-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="86845-112">Attributes</span></span>

<span data-ttu-id="86845-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="86845-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="86845-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="86845-114">Child elements</span></span>

|<span data-ttu-id="86845-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="86845-115">**Element**</span></span>|<span data-ttu-id="86845-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="86845-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="86845-117">ItemId</span><span class="sxs-lookup"><span data-stu-id="86845-117">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="86845-118">Contiene el identificador único y la clave de cambio de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="86845-118">Contains the unique identifier and change key of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="86845-119">OccurrenceItemId</span><span class="sxs-lookup"><span data-stu-id="86845-119">OccurrenceItemId</span></span>](occurrenceitemid.md) <br/> |<span data-ttu-id="86845-120">Identifica una única ocurrencia de un elemento periódico.</span><span class="sxs-lookup"><span data-stu-id="86845-120">Identifies a single occurrence of a recurring item.</span></span>  <br/> |
|[<span data-ttu-id="86845-121">RecurringMasterItemId</span><span class="sxs-lookup"><span data-stu-id="86845-121">RecurringMasterItemId</span></span>](recurringmasteritemid.md) <br/> |<span data-ttu-id="86845-122">Identifica un elemento principal de periodicidad mediante la identificación de uno de los identificadores de elementos de ocurrencia relacionados.</span><span class="sxs-lookup"><span data-stu-id="86845-122">Identifies a recurrence master item by identifying one of its related occurrence items' identifiers.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="86845-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="86845-123">Parent elements</span></span>

|<span data-ttu-id="86845-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="86845-124">**Element**</span></span>|<span data-ttu-id="86845-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="86845-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="86845-126">Conversación (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="86845-126">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="86845-127">Representa una sola conversación.</span><span class="sxs-lookup"><span data-stu-id="86845-127">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="86845-128">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="86845-128">Text value</span></span>

<span data-ttu-id="86845-129">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="86845-129">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="86845-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="86845-130">Remarks</span></span>

<span data-ttu-id="86845-131">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange. este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="86845-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="86845-132">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="86845-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="86845-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="86845-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="86845-134">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="86845-134">Schema name</span></span>  <br/> |<span data-ttu-id="86845-135">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="86845-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="86845-136">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="86845-136">Validation file</span></span>  <br/> |<span data-ttu-id="86845-137">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="86845-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="86845-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="86845-138">Can be empty</span></span>  <br/> |<span data-ttu-id="86845-139">Falso</span><span class="sxs-lookup"><span data-stu-id="86845-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="86845-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="86845-140">See also</span></span>



[<span data-ttu-id="86845-141">Operación FindConversation</span><span class="sxs-lookup"><span data-stu-id="86845-141">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="86845-142">Operación ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="86845-142">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="86845-143">Conversaciones en EWS</span><span class="sxs-lookup"><span data-stu-id="86845-143">Conversations in EWS</span></span>](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

