---
title: GlobalImportance
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GlobalImportance
api_type:
- schema
ms.assetid: 8bcec699-e771-4f38-b7d9-61f324af1b4e
description: El elemento GlobalImportance contiene la importancia agregada para todos los elementos de conversación en un buzón.
ms.openlocfilehash: c760168afa3edac20ca0ae7bc677610d8456d178
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459450"
---
# <a name="globalimportance"></a><span data-ttu-id="798a5-103">GlobalImportance</span><span class="sxs-lookup"><span data-stu-id="798a5-103">GlobalImportance</span></span>

<span data-ttu-id="798a5-104">El elemento **GlobalImportance** contiene la importancia agregada para todos los elementos de conversación en un buzón.</span><span class="sxs-lookup"><span data-stu-id="798a5-104">The **GlobalImportance** element contains the aggregated importance for all conversation items in a mailbox.</span></span> 
  
[<span data-ttu-id="798a5-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="798a5-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="798a5-106">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="798a5-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="798a5-107">Conversación (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="798a5-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="798a5-108">GlobalImportance</span><span class="sxs-lookup"><span data-stu-id="798a5-108">GlobalImportance</span></span>](globalimportance.md)
  
```XML
<GlobalImportance> Low | Normal | High </GlobalImportance>
```

 <span data-ttu-id="798a5-109">**ImportanceChoicesType**</span><span class="sxs-lookup"><span data-stu-id="798a5-109">**ImportanceChoicesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="798a5-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="798a5-110">Attributes and elements</span></span>

<span data-ttu-id="798a5-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="798a5-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="798a5-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="798a5-112">Attributes</span></span>

<span data-ttu-id="798a5-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="798a5-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="798a5-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="798a5-114">Child elements</span></span>

<span data-ttu-id="798a5-115">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="798a5-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="798a5-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="798a5-116">Parent elements</span></span>

|<span data-ttu-id="798a5-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="798a5-117">**Element**</span></span>|<span data-ttu-id="798a5-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="798a5-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="798a5-119">Conversación (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="798a5-119">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="798a5-120">Representa una sola conversación.</span><span class="sxs-lookup"><span data-stu-id="798a5-120">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="798a5-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="798a5-121">Text value</span></span>

<span data-ttu-id="798a5-122">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="798a5-122">A text value is required.</span></span> <span data-ttu-id="798a5-123">A continuación se muestran los valores posibles para este elemento:</span><span class="sxs-lookup"><span data-stu-id="798a5-123">The following are the possible values for this element:</span></span>
  
- <span data-ttu-id="798a5-124">Bajo</span><span class="sxs-lookup"><span data-stu-id="798a5-124">Low</span></span>
    
- <span data-ttu-id="798a5-125">Normal</span><span class="sxs-lookup"><span data-stu-id="798a5-125">Normal</span></span>
    
- <span data-ttu-id="798a5-126">Alta</span><span class="sxs-lookup"><span data-stu-id="798a5-126">High</span></span>
    
## <a name="remarks"></a><span data-ttu-id="798a5-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="798a5-127">Remarks</span></span>

<span data-ttu-id="798a5-128">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange. este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="798a5-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="798a5-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="798a5-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="798a5-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="798a5-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="798a5-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="798a5-131">Schema name</span></span>  <br/> |<span data-ttu-id="798a5-132">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="798a5-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="798a5-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="798a5-133">Validation file</span></span>  <br/> |<span data-ttu-id="798a5-134">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="798a5-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="798a5-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="798a5-135">Can be empty</span></span>  <br/> |<span data-ttu-id="798a5-136">Falso</span><span class="sxs-lookup"><span data-stu-id="798a5-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="798a5-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="798a5-137">See also</span></span>



[<span data-ttu-id="798a5-138">Operación FindConversation</span><span class="sxs-lookup"><span data-stu-id="798a5-138">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="798a5-139">Operación ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="798a5-139">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="798a5-140">Conversaciones en EWS</span><span class="sxs-lookup"><span data-stu-id="798a5-140">Conversations in EWS</span></span>](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

