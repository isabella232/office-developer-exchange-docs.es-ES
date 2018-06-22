---
title: CallState (servicio web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- CallState
api_type:
- schema
ms.assetid: 88670707-12f7-41c5-ac81-dda0c354a2cb
description: El elemento CallState contiene un valor que indica el estado de una llamada.
ms.openlocfilehash: e751c2e38783c6634a44d8e1b830a9224cdf300a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763721"
---
# <a name="callstate-um-web-service"></a><span data-ttu-id="3b728-103">CallState (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="3b728-103">CallState (UM web service)</span></span>

<span data-ttu-id="3b728-104">El elemento **CallState** contiene un valor que indica el estado de una llamada.</span><span class="sxs-lookup"><span data-stu-id="3b728-104">The **CallState** element contains a value that indicates the status of a call.</span></span> 
  
[<span data-ttu-id="3b728-105">GetCallInfoResponse (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="3b728-105">GetCallInfoResponse (UM web service)</span></span>](getcallinforesponse-um-web-service.md)
  
[<span data-ttu-id="3b728-106">CallState (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="3b728-106">CallState (UM web service)</span></span>](callstate-um-web-service.md)
  
```xml
<CallState/>
```

 <span data-ttu-id="3b728-107">**UMCallState**</span><span class="sxs-lookup"><span data-stu-id="3b728-107">**UMCallState**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3b728-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3b728-108">Attributes and elements</span></span>

<span data-ttu-id="3b728-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3b728-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3b728-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="3b728-110">Attributes</span></span>

<span data-ttu-id="3b728-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3b728-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3b728-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3b728-112">Child elements</span></span>

<span data-ttu-id="3b728-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3b728-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3b728-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3b728-114">Parent elements</span></span>

|<span data-ttu-id="3b728-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="3b728-115">**Element**</span></span>|<span data-ttu-id="3b728-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3b728-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3b728-117">GetCallInfoResponse (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="3b728-117">GetCallInfoResponse (UM web service)</span></span>](getcallinforesponse-um-web-service.md) <br/> |<span data-ttu-id="3b728-118">Define una respuesta a una [operación de GetCallInfo (servicio web de mensajería unificada)](getcallinfo-operation-um-web-service.md).</span><span class="sxs-lookup"><span data-stu-id="3b728-118">Defines a response to a [GetCallInfo operation (UM web service)](getcallinfo-operation-um-web-service.md).</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3b728-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="3b728-119">Text value</span></span>

<span data-ttu-id="3b728-120">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="3b728-120">A text value is required.</span></span> <span data-ttu-id="3b728-121">Los valores posibles son:</span><span class="sxs-lookup"><span data-stu-id="3b728-121">The following are the possible values:</span></span>
  
- <span data-ttu-id="3b728-122">Inactividad</span><span class="sxs-lookup"><span data-stu-id="3b728-122">Idle</span></span>
    
- <span data-ttu-id="3b728-123">Conectando</span><span class="sxs-lookup"><span data-stu-id="3b728-123">Connecting</span></span>
    
- <span data-ttu-id="3b728-124">Una alerta</span><span class="sxs-lookup"><span data-stu-id="3b728-124">Alerted</span></span>
    
- <span data-ttu-id="3b728-125">Conectado</span><span class="sxs-lookup"><span data-stu-id="3b728-125">Connected</span></span>
    
- <span data-ttu-id="3b728-126">Desconectado</span><span class="sxs-lookup"><span data-stu-id="3b728-126">Disconnected</span></span>
    
- <span data-ttu-id="3b728-127">Entrante</span><span class="sxs-lookup"><span data-stu-id="3b728-127">Incoming</span></span>
    
- <span data-ttu-id="3b728-128">Transferir</span><span class="sxs-lookup"><span data-stu-id="3b728-128">Transferring</span></span>
    
- <span data-ttu-id="3b728-129">Desvío de llamadas</span><span class="sxs-lookup"><span data-stu-id="3b728-129">Forwarding</span></span>
    
## <a name="element-information"></a><span data-ttu-id="3b728-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3b728-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3b728-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3b728-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/message  <br/> |
|<span data-ttu-id="3b728-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3b728-132">Schema Name</span></span>  <br/> |<span data-ttu-id="3b728-133">Mensajes</span><span class="sxs-lookup"><span data-stu-id="3b728-133">Messages</span></span>  <br/> |
|<span data-ttu-id="3b728-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3b728-134">Validation File</span></span>  <br/> |<span data-ttu-id="3b728-135">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="3b728-135">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3b728-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3b728-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="3b728-137">False</span><span class="sxs-lookup"><span data-stu-id="3b728-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3b728-138">Ver también</span><span class="sxs-lookup"><span data-stu-id="3b728-138">See also</span></span>



[<span data-ttu-id="3b728-139">Operación GetCallInfo (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="3b728-139">GetCallInfo operation (UM web service)</span></span>](getcallinfo-operation-um-web-service.md)
  
[<span data-ttu-id="3b728-140">GetCallInfoResponse (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="3b728-140">GetCallInfoResponse (UM web service)</span></span>](getcallinforesponse-um-web-service.md)

