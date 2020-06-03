---
title: GetCallInfoResponse (servicio Web de mensajería unificada)
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
description: El elemento GetCallInfoResponse define una respuesta a una solicitud de GetCallInfo (servicio Web de mensajería unificada).
ms.openlocfilehash: 6e54ec61a9a5ebecd96bbd39dad68f8cc011b8a1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461208"
---
# <a name="getcallinforesponse-um-web-service"></a><span data-ttu-id="726af-103">GetCallInfoResponse (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="726af-103">GetCallInfoResponse (UM web service)</span></span>

<span data-ttu-id="726af-104">El elemento **GetCallInfoResponse** define una respuesta a una solicitud de [GetCallInfo (servicio Web de mensajería unificada)](getcallinfo-operation-um-web-service.md) .</span><span class="sxs-lookup"><span data-stu-id="726af-104">The **GetCallInfoResponse** element defines a response to a [GetCallInfo operation (UM web service)](getcallinfo-operation-um-web-service.md) request.</span></span> 
  
[<span data-ttu-id="726af-105">GetCallInfoResponse (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="726af-105">GetCallInfoResponse (UM web service)</span></span>](getcallinforesponse-um-web-service.md)
  
```xml
<GetCallInfoResponse>
  <CallState/>
  <EventCause/>
</GetCallInfoResponse>
```

 <span data-ttu-id="726af-106">**UMCallInfo**</span><span class="sxs-lookup"><span data-stu-id="726af-106">**UMCallInfo**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="726af-107">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="726af-107">Attributes and elements</span></span>

<span data-ttu-id="726af-108">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="726af-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="726af-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="726af-109">Attributes</span></span>

<span data-ttu-id="726af-110">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="726af-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="726af-111">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="726af-111">Child elements</span></span>

|<span data-ttu-id="726af-112">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="726af-112">**Element**</span></span>|<span data-ttu-id="726af-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="726af-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="726af-114">CallState</span><span class="sxs-lookup"><span data-stu-id="726af-114">CallState</span></span>  <br/> |<span data-ttu-id="726af-115">Contiene un valor que indica el estado de una llamada para la que la [operación GetCallInfo (servicio Web de mensajería unificada)](getcallinfo-operation-um-web-service.md) ha solicitado información.</span><span class="sxs-lookup"><span data-stu-id="726af-115">Contains a value that indicates the status of a call for which the [GetCallInfo operation (UM web service)](getcallinfo-operation-um-web-service.md) requested information.</span></span>  <br/> |
|<span data-ttu-id="726af-116">EventCause</span><span class="sxs-lookup"><span data-stu-id="726af-116">EventCause</span></span>  <br/> |<span data-ttu-id="726af-117">Contiene un valor que indica la causa de un evento para una llamada para la que la [operación GetCallInfo (servicio Web de mensajería unificada)](getcallinfo-operation-um-web-service.md) solicita información.</span><span class="sxs-lookup"><span data-stu-id="726af-117">Contains a value that indicates the cause of an event for a call for which the [GetCallInfo operation (UM web service)](getcallinfo-operation-um-web-service.md) requested information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="726af-118">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="726af-118">Parent elements</span></span>

<span data-ttu-id="726af-119">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="726af-119">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="726af-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="726af-120">Text value</span></span>

<span data-ttu-id="726af-121">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="726af-121">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="726af-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="726af-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="726af-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="726af-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="726af-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="726af-124">Schema Name</span></span>  <br/> |<span data-ttu-id="726af-125">Mensajes</span><span class="sxs-lookup"><span data-stu-id="726af-125">Messages</span></span>  <br/> |
|<span data-ttu-id="726af-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="726af-126">Validation File</span></span>  <br/> |<span data-ttu-id="726af-127">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="726af-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="726af-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="726af-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="726af-129">Falso</span><span class="sxs-lookup"><span data-stu-id="726af-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="726af-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="726af-130">See also</span></span>



[<span data-ttu-id="726af-131">Operación GetCallInfo (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="726af-131">GetCallInfo operation (UM web service)</span></span>](getcallinfo-operation-um-web-service.md)
  
[<span data-ttu-id="726af-132">CallState (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="726af-132">CallState (UM web service)</span></span>](callstate-um-web-service.md)
  
[<span data-ttu-id="726af-133">EventCause (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="726af-133">EventCause (UM web service)</span></span>](eventcause-um-web-service.md)

