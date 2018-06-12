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
description: El elemento ProcessRightAway indica si la respuesta se envía tan pronto como la acción inicia el procesamiento en el servidor o si la respuesta se ha enviado una vez completada la acción. Este elemento debe estar presente para la respuesta que se envíen asincrónica a la acción solicitada.
ms.openlocfilehash: 940f8e8fa0a53801ce1c3a45c3aecf1bdb6f519d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836898"
---
# <a name="processrightaway"></a><span data-ttu-id="169bb-104">ProcessRightAway</span><span class="sxs-lookup"><span data-stu-id="169bb-104">ProcessRightAway</span></span>

<span data-ttu-id="169bb-105">El elemento **ProcessRightAway** indica si la respuesta se envía tan pronto como la acción inicia el procesamiento en el servidor o si la respuesta se ha enviado una vez completada la acción.</span><span class="sxs-lookup"><span data-stu-id="169bb-105">The **ProcessRightAway** element indicates whether the response is sent as soon as the action starts processing on the server or whether the response is sent after the action has completed.</span></span> <span data-ttu-id="169bb-106">Este elemento debe estar presente para la respuesta que se envíen asincrónica a la acción solicitada.</span><span class="sxs-lookup"><span data-stu-id="169bb-106">This element must be present for the response to be sent asynchronous to the requested action.</span></span> 
  
[<span data-ttu-id="169bb-107">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="169bb-107">ApplyConversationAction</span></span>](applyconversationaction.md)
  
[<span data-ttu-id="169bb-108">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="169bb-108">ConversationActions</span></span>](conversationactions.md)
  
[<span data-ttu-id="169bb-109">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="169bb-109">ConversationAction</span></span>](conversationaction.md)
  
[<span data-ttu-id="169bb-110">ProcessRightAway</span><span class="sxs-lookup"><span data-stu-id="169bb-110">ProcessRightAway</span></span>](processrightaway.md)
  
```XML
<ProcessRightAway/>
```

 <span data-ttu-id="169bb-111">**xs: Boolean**</span><span class="sxs-lookup"><span data-stu-id="169bb-111">**xs:boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="169bb-112">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="169bb-112">Attributes and elements</span></span>

<span data-ttu-id="169bb-113">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="169bb-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="169bb-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="169bb-114">Attributes</span></span>

<span data-ttu-id="169bb-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="169bb-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="169bb-116">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="169bb-116">Child elements</span></span>

<span data-ttu-id="169bb-117">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="169bb-117">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="169bb-118">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="169bb-118">Parent elements</span></span>

|<span data-ttu-id="169bb-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="169bb-119">**Element**</span></span>|<span data-ttu-id="169bb-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="169bb-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="169bb-121">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="169bb-121">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="169bb-122">Contiene una única acción que se aplicará a una conversación único.</span><span class="sxs-lookup"><span data-stu-id="169bb-122">Contains a single action to be applied to a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="169bb-123">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="169bb-123">Text value</span></span>

<span data-ttu-id="169bb-124">Un valor de texto de **true** indica que la respuesta se envía tan pronto como la acción inicia el procesamiento en el servidor.</span><span class="sxs-lookup"><span data-stu-id="169bb-124">A text value of **true** indicates that the response is sent as soon as the action starts processing on the server.</span></span> <span data-ttu-id="169bb-125">Un valor de texto de **false** indica que la respuesta se ha enviado una vez completada la acción.</span><span class="sxs-lookup"><span data-stu-id="169bb-125">A text value of **false** indicates that the response is sent after the action has completed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="169bb-126">Notas</span><span class="sxs-lookup"><span data-stu-id="169bb-126">Remarks</span></span>

<span data-ttu-id="169bb-127">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda Exchange Web Services.This elemento fue introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="169bb-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="169bb-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="169bb-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="169bb-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="169bb-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="169bb-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="169bb-130">Schema Name</span></span>  <br/> |<span data-ttu-id="169bb-131">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="169bb-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="169bb-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="169bb-132">Validation File</span></span>  <br/> |<span data-ttu-id="169bb-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="169bb-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="169bb-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="169bb-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="169bb-135">False</span><span class="sxs-lookup"><span data-stu-id="169bb-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="169bb-136">Ver también</span><span class="sxs-lookup"><span data-stu-id="169bb-136">See also</span></span>



[<span data-ttu-id="169bb-137">Operación ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="169bb-137">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


- [<span data-ttu-id="169bb-138">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="169bb-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

