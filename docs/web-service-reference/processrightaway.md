---
title: ProcessRightAway
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ProcessRightAway
api_type:
- schema
ms.assetid: f6bba68b-ae4f-41c1-b3e7-c8a31cdb1b0c
description: El elemento ProcessRightAway indica si la respuesta se envía en cuanto la acción comienza a procesarse en el servidor o si la respuesta se envía una vez completada la acción. Este elemento debe estar presente para que la respuesta se envíe asincrónica a la acción solicitada.
ms.openlocfilehash: 58d2b926c48db5e7395df64e1f8ee9d6a8f0e73c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44434074"
---
# <a name="processrightaway"></a><span data-ttu-id="2ed98-104">ProcessRightAway</span><span class="sxs-lookup"><span data-stu-id="2ed98-104">ProcessRightAway</span></span>

<span data-ttu-id="2ed98-105">El elemento **ProcessRightAway** indica si la respuesta se envía en cuanto la acción comienza a procesarse en el servidor o si la respuesta se envía una vez completada la acción.</span><span class="sxs-lookup"><span data-stu-id="2ed98-105">The **ProcessRightAway** element indicates whether the response is sent as soon as the action starts processing on the server or whether the response is sent after the action has completed.</span></span> <span data-ttu-id="2ed98-106">Este elemento debe estar presente para que la respuesta se envíe asincrónica a la acción solicitada.</span><span class="sxs-lookup"><span data-stu-id="2ed98-106">This element must be present for the response to be sent asynchronous to the requested action.</span></span> 
  
[<span data-ttu-id="2ed98-107">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="2ed98-107">ApplyConversationAction</span></span>](applyconversationaction.md)
  
[<span data-ttu-id="2ed98-108">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="2ed98-108">ConversationActions</span></span>](conversationactions.md)
  
[<span data-ttu-id="2ed98-109">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="2ed98-109">ConversationAction</span></span>](conversationaction.md)
  
[<span data-ttu-id="2ed98-110">ProcessRightAway</span><span class="sxs-lookup"><span data-stu-id="2ed98-110">ProcessRightAway</span></span>](processrightaway.md)
  
```XML
<ProcessRightAway/>
```

 <span data-ttu-id="2ed98-111">**XS: Boolean**</span><span class="sxs-lookup"><span data-stu-id="2ed98-111">**xs:boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2ed98-112">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="2ed98-112">Attributes and elements</span></span>

<span data-ttu-id="2ed98-113">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="2ed98-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2ed98-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="2ed98-114">Attributes</span></span>

<span data-ttu-id="2ed98-115">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="2ed98-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2ed98-116">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2ed98-116">Child elements</span></span>

<span data-ttu-id="2ed98-117">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="2ed98-117">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2ed98-118">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="2ed98-118">Parent elements</span></span>

|<span data-ttu-id="2ed98-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="2ed98-119">**Element**</span></span>|<span data-ttu-id="2ed98-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2ed98-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2ed98-121">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="2ed98-121">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="2ed98-122">Contiene una sola acción que se aplicará a una única conversación.</span><span class="sxs-lookup"><span data-stu-id="2ed98-122">Contains a single action to be applied to a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2ed98-123">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="2ed98-123">Text value</span></span>

<span data-ttu-id="2ed98-124">Un valor de texto de **true** indica que la respuesta se envía en cuanto la acción comienza el procesamiento en el servidor.</span><span class="sxs-lookup"><span data-stu-id="2ed98-124">A text value of **true** indicates that the response is sent as soon as the action starts processing on the server.</span></span> <span data-ttu-id="2ed98-125">Un valor de texto de **false** indica que la respuesta se envía una vez completada la acción.</span><span class="sxs-lookup"><span data-stu-id="2ed98-125">A text value of **false** indicates that the response is sent after the action has completed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="2ed98-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2ed98-126">Remarks</span></span>

<span data-ttu-id="2ed98-127">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange. este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="2ed98-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2ed98-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="2ed98-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2ed98-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="2ed98-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2ed98-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="2ed98-130">Schema Name</span></span>  <br/> |<span data-ttu-id="2ed98-131">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="2ed98-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="2ed98-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="2ed98-132">Validation File</span></span>  <br/> |<span data-ttu-id="2ed98-133">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="2ed98-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2ed98-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="2ed98-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="2ed98-135">Falso</span><span class="sxs-lookup"><span data-stu-id="2ed98-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2ed98-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="2ed98-136">See also</span></span>



[<span data-ttu-id="2ed98-137">Operación ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="2ed98-137">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


- [<span data-ttu-id="2ed98-138">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="2ed98-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

