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
description: El elemento GlobalItemIds contiene la colección de identificadores de elemento para todos los elementos de la conversación en un buzón de correo.
ms.openlocfilehash: 064ebc4c612aaf569eafa56e57a27cf7153f2130
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835737"
---
# <a name="globalitemids"></a><span data-ttu-id="20e3e-103">GlobalItemIds</span><span class="sxs-lookup"><span data-stu-id="20e3e-103">GlobalItemIds</span></span>

<span data-ttu-id="20e3e-104">El elemento **GlobalItemIds** contiene la colección de identificadores de elemento para todos los elementos de la conversación en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="20e3e-104">The **GlobalItemIds** element contains the collection of item identifiers for all conversation items in a mailbox.</span></span> 
  
[<span data-ttu-id="20e3e-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="20e3e-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="20e3e-106">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="20e3e-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="20e3e-107">Conversación (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="20e3e-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="20e3e-108">GlobalItemIds</span><span class="sxs-lookup"><span data-stu-id="20e3e-108">GlobalItemIds</span></span>](globalitemids.md)
  
```XML
<ItemIds>
   <ItemId/>
   <OccurrenceItemId/>
   <RecurringMasterItemId/>
</ItemIds>
```

 <span data-ttu-id="20e3e-109">**NonEmptyArrayOfBaseItemIdsType**</span><span class="sxs-lookup"><span data-stu-id="20e3e-109">**NonEmptyArrayOfBaseItemIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="20e3e-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="20e3e-110">Attributes and elements</span></span>

<span data-ttu-id="20e3e-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="20e3e-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="20e3e-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="20e3e-112">Attributes</span></span>

<span data-ttu-id="20e3e-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="20e3e-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="20e3e-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="20e3e-114">Child elements</span></span>

|<span data-ttu-id="20e3e-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="20e3e-115">**Element**</span></span>|<span data-ttu-id="20e3e-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="20e3e-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="20e3e-117">ItemId</span><span class="sxs-lookup"><span data-stu-id="20e3e-117">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="20e3e-118">Contiene el único identificador y cambiar la clave de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="20e3e-118">Contains the unique identifier and change key of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="20e3e-119">OccurrenceItemId</span><span class="sxs-lookup"><span data-stu-id="20e3e-119">OccurrenceItemId</span></span>](occurrenceitemid.md) <br/> |<span data-ttu-id="20e3e-120">Identifica una sola aparición de un elemento periódico.</span><span class="sxs-lookup"><span data-stu-id="20e3e-120">Identifies a single occurrence of a recurring item.</span></span>  <br/> |
|[<span data-ttu-id="20e3e-121">RecurringMasterItemId</span><span class="sxs-lookup"><span data-stu-id="20e3e-121">RecurringMasterItemId</span></span>](recurringmasteritemid.md) <br/> |<span data-ttu-id="20e3e-122">Identifica un elemento de patrón de periodicidad mediante la identificación de uno de los identificadores de los elementos de su aparición relacionados.</span><span class="sxs-lookup"><span data-stu-id="20e3e-122">Identifies a recurrence master item by identifying one of its related occurrence items' identifiers.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="20e3e-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="20e3e-123">Parent elements</span></span>

|<span data-ttu-id="20e3e-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="20e3e-124">**Element**</span></span>|<span data-ttu-id="20e3e-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="20e3e-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="20e3e-126">Conversación (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="20e3e-126">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="20e3e-127">Representa una sola conversación.</span><span class="sxs-lookup"><span data-stu-id="20e3e-127">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="20e3e-128">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="20e3e-128">Text value</span></span>

<span data-ttu-id="20e3e-129">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="20e3e-129">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="20e3e-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="20e3e-130">Remarks</span></span>

<span data-ttu-id="20e3e-131">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda Exchange Web Services.This elemento fue introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="20e3e-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="20e3e-132">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="20e3e-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="20e3e-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="20e3e-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="20e3e-134">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="20e3e-134">Schema name</span></span>  <br/> |<span data-ttu-id="20e3e-135">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="20e3e-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="20e3e-136">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="20e3e-136">Validation file</span></span>  <br/> |<span data-ttu-id="20e3e-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="20e3e-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="20e3e-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="20e3e-138">Can be empty</span></span>  <br/> |<span data-ttu-id="20e3e-139">False</span><span class="sxs-lookup"><span data-stu-id="20e3e-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="20e3e-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="20e3e-140">See also</span></span>



[<span data-ttu-id="20e3e-141">Operación de FindConversation</span><span class="sxs-lookup"><span data-stu-id="20e3e-141">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="20e3e-142">Operación ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="20e3e-142">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="20e3e-143">Conversaciones de EWS</span><span class="sxs-lookup"><span data-stu-id="20e3e-143">Conversations in EWS</span></span>](http://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

