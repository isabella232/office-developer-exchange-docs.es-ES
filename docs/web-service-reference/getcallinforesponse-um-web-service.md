---
title: GetCallInfoResponse (servicio web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- GetCallInfoResponse
api_type:
- schema
ms.assetid: aa5196bf-f5f3-455c-94ea-304fb7920c79
description: El elemento GetCallInfoResponse define una respuesta a una solicitud de GetCallInfo operación (servicio web de mensajería unificada).
ms.openlocfilehash: d9658dd9cb47f925e05dc21a8651c98dce1f0a2a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764769"
---
# <a name="getcallinforesponse-um-web-service"></a><span data-ttu-id="5bf1a-103">GetCallInfoResponse (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="5bf1a-103">GetCallInfoResponse (UM web service)</span></span>

<span data-ttu-id="5bf1a-104">El elemento **GetCallInfoResponse** define una respuesta a una solicitud de [operación GetCallInfo (servicio web de mensajería unificada)](getcallinfo-operation-um-web-service.md) .</span><span class="sxs-lookup"><span data-stu-id="5bf1a-104">The **GetCallInfoResponse** element defines a response to a [GetCallInfo operation (UM web service)](getcallinfo-operation-um-web-service.md) request.</span></span> 
  
[<span data-ttu-id="5bf1a-105">GetCallInfoResponse (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="5bf1a-105">GetCallInfoResponse (UM web service)</span></span>](getcallinforesponse-um-web-service.md)
  
```xml
<GetCallInfoResponse>
  <CallState/>
  <EventCause/>
</GetCallInfoResponse>
```

 <span data-ttu-id="5bf1a-106">**UMCallInfo**</span><span class="sxs-lookup"><span data-stu-id="5bf1a-106">**UMCallInfo**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5bf1a-107">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="5bf1a-107">Attributes and elements</span></span>

<span data-ttu-id="5bf1a-108">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="5bf1a-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5bf1a-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="5bf1a-109">Attributes</span></span>

<span data-ttu-id="5bf1a-110">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5bf1a-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5bf1a-111">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5bf1a-111">Child elements</span></span>

|<span data-ttu-id="5bf1a-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="5bf1a-112">**Element**</span></span>|<span data-ttu-id="5bf1a-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5bf1a-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5bf1a-114">CallState</span><span class="sxs-lookup"><span data-stu-id="5bf1a-114">CallState</span></span>  <br/> |<span data-ttu-id="5bf1a-115">Contiene un valor que indica el estado de una llamada para que la [operación de GetCallInfo (servicio web de mensajería unificada)](getcallinfo-operation-um-web-service.md) solicita información.</span><span class="sxs-lookup"><span data-stu-id="5bf1a-115">Contains a value that indicates the status of a call for which the [GetCallInfo operation (UM web service)](getcallinfo-operation-um-web-service.md) requested information.</span></span>  <br/> |
|<span data-ttu-id="5bf1a-116">EventCause</span><span class="sxs-lookup"><span data-stu-id="5bf1a-116">EventCause</span></span>  <br/> |<span data-ttu-id="5bf1a-117">Contiene un valor que indica la causa de un evento para una llamada para que la [operación de GetCallInfo (servicio web de mensajería unificada)](getcallinfo-operation-um-web-service.md) solicita información.</span><span class="sxs-lookup"><span data-stu-id="5bf1a-117">Contains a value that indicates the cause of an event for a call for which the [GetCallInfo operation (UM web service)](getcallinfo-operation-um-web-service.md) requested information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5bf1a-118">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5bf1a-118">Parent elements</span></span>

<span data-ttu-id="5bf1a-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5bf1a-119">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="5bf1a-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="5bf1a-120">Text value</span></span>

<span data-ttu-id="5bf1a-121">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5bf1a-121">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5bf1a-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="5bf1a-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5bf1a-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5bf1a-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="5bf1a-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="5bf1a-124">Schema Name</span></span>  <br/> |<span data-ttu-id="5bf1a-125">Mensajes</span><span class="sxs-lookup"><span data-stu-id="5bf1a-125">Messages</span></span>  <br/> |
|<span data-ttu-id="5bf1a-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="5bf1a-126">Validation File</span></span>  <br/> |<span data-ttu-id="5bf1a-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="5bf1a-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="5bf1a-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="5bf1a-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="5bf1a-129">False</span><span class="sxs-lookup"><span data-stu-id="5bf1a-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5bf1a-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="5bf1a-130">See also</span></span>



[<span data-ttu-id="5bf1a-131">Operación GetCallInfo (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="5bf1a-131">GetCallInfo operation (UM web service)</span></span>](getcallinfo-operation-um-web-service.md)
  
[<span data-ttu-id="5bf1a-132">CallState (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="5bf1a-132">CallState (UM web service)</span></span>](callstate-um-web-service.md)
  
[<span data-ttu-id="5bf1a-133">EventCause (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="5bf1a-133">EventCause (UM web service)</span></span>](eventcause-um-web-service.md)

