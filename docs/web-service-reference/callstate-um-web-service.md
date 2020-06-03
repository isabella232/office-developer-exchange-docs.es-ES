---
title: CallState (servicio Web de mensajería unificada)
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
ms.openlocfilehash: 44614c460286ff49ebc2373263c1827c6be5cc08
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44454613"
---
# <a name="callstate-um-web-service"></a><span data-ttu-id="17d86-103">CallState (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="17d86-103">CallState (UM web service)</span></span>

<span data-ttu-id="17d86-104">El elemento **CallState** contiene un valor que indica el estado de una llamada.</span><span class="sxs-lookup"><span data-stu-id="17d86-104">The **CallState** element contains a value that indicates the status of a call.</span></span> 
  
[<span data-ttu-id="17d86-105">GetCallInfoResponse (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="17d86-105">GetCallInfoResponse (UM web service)</span></span>](getcallinforesponse-um-web-service.md)
  
[<span data-ttu-id="17d86-106">CallState (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="17d86-106">CallState (UM web service)</span></span>](callstate-um-web-service.md)
  
```xml
<CallState/>
```

 <span data-ttu-id="17d86-107">**UMCallState**</span><span class="sxs-lookup"><span data-stu-id="17d86-107">**UMCallState**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="17d86-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="17d86-108">Attributes and elements</span></span>

<span data-ttu-id="17d86-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="17d86-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="17d86-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="17d86-110">Attributes</span></span>

<span data-ttu-id="17d86-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="17d86-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="17d86-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="17d86-112">Child elements</span></span>

<span data-ttu-id="17d86-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="17d86-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="17d86-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="17d86-114">Parent elements</span></span>

|<span data-ttu-id="17d86-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="17d86-115">**Element**</span></span>|<span data-ttu-id="17d86-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="17d86-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="17d86-117">GetCallInfoResponse (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="17d86-117">GetCallInfoResponse (UM web service)</span></span>](getcallinforesponse-um-web-service.md) <br/> |<span data-ttu-id="17d86-118">Define una respuesta a una [operación de GetCallInfo (servicio Web de mensajería unificada)](getcallinfo-operation-um-web-service.md).</span><span class="sxs-lookup"><span data-stu-id="17d86-118">Defines a response to a [GetCallInfo operation (UM web service)](getcallinfo-operation-um-web-service.md).</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="17d86-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="17d86-119">Text value</span></span>

<span data-ttu-id="17d86-120">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="17d86-120">A text value is required.</span></span> <span data-ttu-id="17d86-121">Los valores posibles son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="17d86-121">The following are the possible values:</span></span>
  
- <span data-ttu-id="17d86-122">Usado</span><span class="sxs-lookup"><span data-stu-id="17d86-122">Idle</span></span>
    
- <span data-ttu-id="17d86-123">Conectando</span><span class="sxs-lookup"><span data-stu-id="17d86-123">Connecting</span></span>
    
- <span data-ttu-id="17d86-124">Alertas</span><span class="sxs-lookup"><span data-stu-id="17d86-124">Alerted</span></span>
    
- <span data-ttu-id="17d86-125">Conectado</span><span class="sxs-lookup"><span data-stu-id="17d86-125">Connected</span></span>
    
- <span data-ttu-id="17d86-126">Desconectado</span><span class="sxs-lookup"><span data-stu-id="17d86-126">Disconnected</span></span>
    
- <span data-ttu-id="17d86-127">Entra</span><span class="sxs-lookup"><span data-stu-id="17d86-127">Incoming</span></span>
    
- <span data-ttu-id="17d86-128">Transferencia</span><span class="sxs-lookup"><span data-stu-id="17d86-128">Transferring</span></span>
    
- <span data-ttu-id="17d86-129">Reenvío</span><span class="sxs-lookup"><span data-stu-id="17d86-129">Forwarding</span></span>
    
## <a name="element-information"></a><span data-ttu-id="17d86-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="17d86-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="17d86-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="17d86-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/message  <br/> |
|<span data-ttu-id="17d86-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="17d86-132">Schema Name</span></span>  <br/> |<span data-ttu-id="17d86-133">Mensajes</span><span class="sxs-lookup"><span data-stu-id="17d86-133">Messages</span></span>  <br/> |
|<span data-ttu-id="17d86-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="17d86-134">Validation File</span></span>  <br/> |<span data-ttu-id="17d86-135">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="17d86-135">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="17d86-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="17d86-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="17d86-137">Falso</span><span class="sxs-lookup"><span data-stu-id="17d86-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="17d86-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="17d86-138">See also</span></span>



[<span data-ttu-id="17d86-139">Operación GetCallInfo (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="17d86-139">GetCallInfo operation (UM web service)</span></span>](getcallinfo-operation-um-web-service.md)
  
[<span data-ttu-id="17d86-140">GetCallInfoResponse (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="17d86-140">GetCallInfoResponse (UM web service)</span></span>](getcallinforesponse-um-web-service.md)

