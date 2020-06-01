---
title: EventCause (servicio Web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- EventCause
api_type:
- schema
ms.assetid: 7b3c1db8-cad4-4050-a50d-b06f065db530
description: El elemento EventCause contiene un valor que indica la causa de un evento de llamada en una respuesta a una solicitud GetCallInfo (servicio Web de mensajería unificada).
ms.openlocfilehash: 9d49fd4b16236d0dd87889fbbd039f2e271a5968
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458680"
---
# <a name="eventcause-um-web-service"></a><span data-ttu-id="9eff1-103">EventCause (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="9eff1-103">EventCause (UM web service)</span></span>

<span data-ttu-id="9eff1-104">El elemento **EventCause** contiene un valor que indica la causa de un evento de llamada en una respuesta a una solicitud [GetCallInfo (servicio Web de mensajería unificada)](getcallinfo-operation-um-web-service.md) .</span><span class="sxs-lookup"><span data-stu-id="9eff1-104">The **EventCause** element contains a value that indicates the cause for a call event in a response to a [GetCallInfo operation (UM web service)](getcallinfo-operation-um-web-service.md) request.</span></span> 
  
[<span data-ttu-id="9eff1-105">GetCallInfoResponse (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="9eff1-105">GetCallInfoResponse (UM web service)</span></span>](getcallinforesponse-um-web-service.md)
  
[<span data-ttu-id="9eff1-106">EventCause (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="9eff1-106">EventCause (UM web service)</span></span>](eventcause-um-web-service.md)
  
```xml
<GetCallInfoResponse>
  <EventCause/>
</GetCallInfoResponse>
```

 <span data-ttu-id="9eff1-107">**UMEventCause**</span><span class="sxs-lookup"><span data-stu-id="9eff1-107">**UMEventCause**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9eff1-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="9eff1-108">Attributes and elements</span></span>

<span data-ttu-id="9eff1-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="9eff1-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9eff1-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="9eff1-110">Attributes</span></span>

<span data-ttu-id="9eff1-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="9eff1-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9eff1-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9eff1-112">Child elements</span></span>

<span data-ttu-id="9eff1-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="9eff1-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9eff1-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="9eff1-114">Parent elements</span></span>

|<span data-ttu-id="9eff1-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9eff1-115">**Element**</span></span>|<span data-ttu-id="9eff1-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9eff1-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9eff1-117">GetCallInfoResponse (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="9eff1-117">GetCallInfoResponse (UM web service)</span></span>](getcallinforesponse-um-web-service.md) <br/> |<span data-ttu-id="9eff1-118">Define una respuesta a una solicitud de [operación de GetCallInfo (servicio Web de mensajería unificada)](getcallinfo-operation-um-web-service.md) .</span><span class="sxs-lookup"><span data-stu-id="9eff1-118">Defines a response to a [GetCallInfo operation (UM web service)](getcallinfo-operation-um-web-service.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="9eff1-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="9eff1-119">Text value</span></span>

<span data-ttu-id="9eff1-120">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="9eff1-120">A text value is required.</span></span> <span data-ttu-id="9eff1-121">Los valores posibles son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="9eff1-121">The following are the possible values:</span></span>
  
- <span data-ttu-id="9eff1-122">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9eff1-122">None</span></span>
    
- <span data-ttu-id="9eff1-123">UserBusy</span><span class="sxs-lookup"><span data-stu-id="9eff1-123">UserBusy</span></span>
    
- <span data-ttu-id="9eff1-124">Noanswer</span><span class="sxs-lookup"><span data-stu-id="9eff1-124">NoAnswer</span></span>
    
- <span data-ttu-id="9eff1-125">Otros</span><span class="sxs-lookup"><span data-stu-id="9eff1-125">Other</span></span>
    
## <a name="element-information"></a><span data-ttu-id="9eff1-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="9eff1-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9eff1-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="9eff1-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="9eff1-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="9eff1-128">Schema Name</span></span>  <br/> |<span data-ttu-id="9eff1-129">Mensajes</span><span class="sxs-lookup"><span data-stu-id="9eff1-129">Messages</span></span>  <br/> |
|<span data-ttu-id="9eff1-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="9eff1-130">Validation File</span></span>  <br/> |<span data-ttu-id="9eff1-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="9eff1-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9eff1-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="9eff1-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="9eff1-133">Falso</span><span class="sxs-lookup"><span data-stu-id="9eff1-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9eff1-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="9eff1-134">See also</span></span>



[<span data-ttu-id="9eff1-135">Operación GetCallInfo (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="9eff1-135">GetCallInfo operation (UM web service)</span></span>](getcallinfo-operation-um-web-service.md)
  
[<span data-ttu-id="9eff1-136">GetCallInfoResponse (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="9eff1-136">GetCallInfoResponse (UM web service)</span></span>](getcallinforesponse-um-web-service.md)

