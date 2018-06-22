---
title: ConversationLastSyncTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConversationLastSyncTime
api_type:
- schema
ms.assetid: 90f8f9e3-5fc6-4a6a-bdfb-fc91fa51f8a2
description: El elemento ConversationLastSyncTime contiene la fecha y hora en que se sincronizaron por última vez una conversación. Este elemento debe estar presente al intentar eliminar todos los elementos de una conversación que se han recibido hasta el momento especificado.
ms.openlocfilehash: 3b086d69ac0ef307059df4902e65f796c63733d1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763877"
---
# <a name="conversationlastsynctime"></a><span data-ttu-id="c1f23-104">ConversationLastSyncTime</span><span class="sxs-lookup"><span data-stu-id="c1f23-104">ConversationLastSyncTime</span></span>

<span data-ttu-id="c1f23-105">El elemento **ConversationLastSyncTime** contiene la fecha y hora en que se sincronizaron por última vez una conversación.</span><span class="sxs-lookup"><span data-stu-id="c1f23-105">The **ConversationLastSyncTime** element contains the date and time that a conversation was last synchronized.</span></span> <span data-ttu-id="c1f23-106">Este elemento debe estar presente al intentar eliminar todos los elementos de una conversación que se han recibido hasta el momento especificado.</span><span class="sxs-lookup"><span data-stu-id="c1f23-106">This element must be present when trying to delete all items in a conversation that were received up to the specified time.</span></span> 
  
[<span data-ttu-id="c1f23-107">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="c1f23-107">ApplyConversationAction</span></span>](applyconversationaction.md)
  
[<span data-ttu-id="c1f23-108">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="c1f23-108">ConversationActions</span></span>](conversationactions.md)
  
[<span data-ttu-id="c1f23-109">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="c1f23-109">ConversationAction</span></span>](conversationaction.md)
  
[<span data-ttu-id="c1f23-110">ConversationLastSyncTime</span><span class="sxs-lookup"><span data-stu-id="c1f23-110">ConversationLastSyncTime</span></span>](conversationlastsynctime.md)
  
```XML
<ConversationLastSyncTime/>
```

 <span data-ttu-id="c1f23-111">**xs: DateTime**</span><span class="sxs-lookup"><span data-stu-id="c1f23-111">**xs:dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c1f23-112">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c1f23-112">Attributes and elements</span></span>

<span data-ttu-id="c1f23-113">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c1f23-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c1f23-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="c1f23-114">Attributes</span></span>

<span data-ttu-id="c1f23-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c1f23-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c1f23-116">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c1f23-116">Child elements</span></span>

<span data-ttu-id="c1f23-117">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c1f23-117">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c1f23-118">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c1f23-118">Parent elements</span></span>

|<span data-ttu-id="c1f23-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="c1f23-119">**Element**</span></span>|<span data-ttu-id="c1f23-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c1f23-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c1f23-121">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="c1f23-121">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="c1f23-122">Contiene una única acción que se aplicará a una conversación único.</span><span class="sxs-lookup"><span data-stu-id="c1f23-122">Contains a single action to be applied to a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c1f23-123">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="c1f23-123">Text value</span></span>

<span data-ttu-id="c1f23-124">El valor de texto de la **ConversationLastSyncTime** indica la última vez que se ha sincronizado la conversación.</span><span class="sxs-lookup"><span data-stu-id="c1f23-124">The text value of the **ConversationLastSyncTime** indicates the last time the conversation was synchronized.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c1f23-125">Notas</span><span class="sxs-lookup"><span data-stu-id="c1f23-125">Remarks</span></span>

<span data-ttu-id="c1f23-126">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda Exchange Web Services.This elemento fue introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="c1f23-126">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c1f23-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c1f23-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c1f23-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c1f23-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c1f23-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c1f23-129">Schema Name</span></span>  <br/> |<span data-ttu-id="c1f23-130">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="c1f23-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="c1f23-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c1f23-131">Validation File</span></span>  <br/> |<span data-ttu-id="c1f23-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c1f23-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c1f23-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c1f23-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="c1f23-134">False</span><span class="sxs-lookup"><span data-stu-id="c1f23-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c1f23-135">Ver también</span><span class="sxs-lookup"><span data-stu-id="c1f23-135">See also</span></span>



[<span data-ttu-id="c1f23-136">Operación ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="c1f23-136">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


- [<span data-ttu-id="c1f23-137">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="c1f23-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

