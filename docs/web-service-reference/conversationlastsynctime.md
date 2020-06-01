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
description: El elemento ConversationLastSyncTime contiene la fecha y la hora en que una conversación se sincronizó por última vez. Este elemento debe estar presente cuando se intenta eliminar todos los elementos de una conversación que se recibieron hasta la hora especificada.
ms.openlocfilehash: f7cc6e205ab9936685d7b8c1f34129b799a53021
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461432"
---
# <a name="conversationlastsynctime"></a><span data-ttu-id="04424-104">ConversationLastSyncTime</span><span class="sxs-lookup"><span data-stu-id="04424-104">ConversationLastSyncTime</span></span>

<span data-ttu-id="04424-105">El elemento **ConversationLastSyncTime** contiene la fecha y la hora en que una conversación se sincronizó por última vez.</span><span class="sxs-lookup"><span data-stu-id="04424-105">The **ConversationLastSyncTime** element contains the date and time that a conversation was last synchronized.</span></span> <span data-ttu-id="04424-106">Este elemento debe estar presente cuando se intenta eliminar todos los elementos de una conversación que se recibieron hasta la hora especificada.</span><span class="sxs-lookup"><span data-stu-id="04424-106">This element must be present when trying to delete all items in a conversation that were received up to the specified time.</span></span> 
  
[<span data-ttu-id="04424-107">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="04424-107">ApplyConversationAction</span></span>](applyconversationaction.md)
  
[<span data-ttu-id="04424-108">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="04424-108">ConversationActions</span></span>](conversationactions.md)
  
[<span data-ttu-id="04424-109">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="04424-109">ConversationAction</span></span>](conversationaction.md)
  
[<span data-ttu-id="04424-110">ConversationLastSyncTime</span><span class="sxs-lookup"><span data-stu-id="04424-110">ConversationLastSyncTime</span></span>](conversationlastsynctime.md)
  
```XML
<ConversationLastSyncTime/>
```

 <span data-ttu-id="04424-111">**XS: dateTime**</span><span class="sxs-lookup"><span data-stu-id="04424-111">**xs:dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="04424-112">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="04424-112">Attributes and elements</span></span>

<span data-ttu-id="04424-113">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="04424-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="04424-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="04424-114">Attributes</span></span>

<span data-ttu-id="04424-115">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="04424-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="04424-116">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="04424-116">Child elements</span></span>

<span data-ttu-id="04424-117">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="04424-117">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="04424-118">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="04424-118">Parent elements</span></span>

|<span data-ttu-id="04424-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="04424-119">**Element**</span></span>|<span data-ttu-id="04424-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="04424-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="04424-121">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="04424-121">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="04424-122">Contiene una sola acción que se aplicará a una única conversación.</span><span class="sxs-lookup"><span data-stu-id="04424-122">Contains a single action to be applied to a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="04424-123">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="04424-123">Text value</span></span>

<span data-ttu-id="04424-124">El valor de texto de **ConversationLastSyncTime** indica la última vez que se sincronizó la conversación.</span><span class="sxs-lookup"><span data-stu-id="04424-124">The text value of the **ConversationLastSyncTime** indicates the last time the conversation was synchronized.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="04424-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="04424-125">Remarks</span></span>

<span data-ttu-id="04424-126">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange. este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="04424-126">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="04424-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="04424-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="04424-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="04424-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="04424-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="04424-129">Schema Name</span></span>  <br/> |<span data-ttu-id="04424-130">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="04424-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="04424-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="04424-131">Validation File</span></span>  <br/> |<span data-ttu-id="04424-132">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="04424-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="04424-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="04424-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="04424-134">Falso</span><span class="sxs-lookup"><span data-stu-id="04424-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="04424-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="04424-135">See also</span></span>



[<span data-ttu-id="04424-136">Operación ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="04424-136">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


- [<span data-ttu-id="04424-137">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="04424-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

