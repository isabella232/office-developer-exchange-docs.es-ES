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
description: El elemento GlobalImportance contiene la importancia agregada para todos los elementos de la conversación en un buzón de correo.
ms.openlocfilehash: c9cdcf20fd3e6eca9ab501cbc747544a4d7b7ded
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835731"
---
# <a name="globalimportance"></a><span data-ttu-id="c3e41-103">GlobalImportance</span><span class="sxs-lookup"><span data-stu-id="c3e41-103">GlobalImportance</span></span>

<span data-ttu-id="c3e41-104">El elemento **GlobalImportance** contiene la importancia agregada para todos los elementos de la conversación en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="c3e41-104">The **GlobalImportance** element contains the aggregated importance for all conversation items in a mailbox.</span></span> 
  
[<span data-ttu-id="c3e41-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="c3e41-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="c3e41-106">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="c3e41-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="c3e41-107">Conversación (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="c3e41-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="c3e41-108">GlobalImportance</span><span class="sxs-lookup"><span data-stu-id="c3e41-108">GlobalImportance</span></span>](globalimportance.md)
  
```XML
<GlobalImportance> Low | Normal | High </GlobalImportance>
```

 <span data-ttu-id="c3e41-109">**ImportanceChoicesType**</span><span class="sxs-lookup"><span data-stu-id="c3e41-109">**ImportanceChoicesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c3e41-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c3e41-110">Attributes and elements</span></span>

<span data-ttu-id="c3e41-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c3e41-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c3e41-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="c3e41-112">Attributes</span></span>

<span data-ttu-id="c3e41-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c3e41-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c3e41-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c3e41-114">Child elements</span></span>

<span data-ttu-id="c3e41-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c3e41-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c3e41-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c3e41-116">Parent elements</span></span>

|<span data-ttu-id="c3e41-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="c3e41-117">**Element**</span></span>|<span data-ttu-id="c3e41-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c3e41-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c3e41-119">Conversación (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="c3e41-119">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="c3e41-120">Representa una sola conversación.</span><span class="sxs-lookup"><span data-stu-id="c3e41-120">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c3e41-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="c3e41-121">Text value</span></span>

<span data-ttu-id="c3e41-122">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="c3e41-122">A text value is required.</span></span> <span data-ttu-id="c3e41-123">Los siguientes son los valores posibles para este elemento:</span><span class="sxs-lookup"><span data-stu-id="c3e41-123">The following are the possible values for this element:</span></span>
  
- <span data-ttu-id="c3e41-124">Low</span><span class="sxs-lookup"><span data-stu-id="c3e41-124">Low</span></span>
    
- <span data-ttu-id="c3e41-125">Importance</span><span class="sxs-lookup"><span data-stu-id="c3e41-125">Normal</span></span>
    
- <span data-ttu-id="c3e41-126">High</span><span class="sxs-lookup"><span data-stu-id="c3e41-126">High</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c3e41-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c3e41-127">Remarks</span></span>

<span data-ttu-id="c3e41-128">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda Exchange Web Services.This elemento fue introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="c3e41-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c3e41-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c3e41-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c3e41-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c3e41-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c3e41-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c3e41-131">Schema name</span></span>  <br/> |<span data-ttu-id="c3e41-132">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="c3e41-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="c3e41-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c3e41-133">Validation file</span></span>  <br/> |<span data-ttu-id="c3e41-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c3e41-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c3e41-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c3e41-135">Can be empty</span></span>  <br/> |<span data-ttu-id="c3e41-136">False</span><span class="sxs-lookup"><span data-stu-id="c3e41-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c3e41-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="c3e41-137">See also</span></span>



[<span data-ttu-id="c3e41-138">Operación de FindConversation</span><span class="sxs-lookup"><span data-stu-id="c3e41-138">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="c3e41-139">Operación ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="c3e41-139">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="c3e41-140">Conversaciones de EWS</span><span class="sxs-lookup"><span data-stu-id="c3e41-140">Conversations in EWS</span></span>](http://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

