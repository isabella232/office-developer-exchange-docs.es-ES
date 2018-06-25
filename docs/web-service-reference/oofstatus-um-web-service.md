---
title: OofStatus (servicio web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- OofStatus
api_type:
- schema
ms.assetid: 0ba4225a-784e-4e6e-bd20-be45f0f7597c
description: El elemento OofStatus contiene un valor que indicaties el estado de Unified Messaging fuera de la oficina del usuario que está realizando una solicitud de GetUMProperties operación (servicio web de mensajería unificada).
ms.openlocfilehash: 1fe358a8bfea3c509220d6705a238ae832de37e8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836650"
---
# <a name="oofstatus-um-web-service"></a><span data-ttu-id="8492d-103">OofStatus (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="8492d-103">OofStatus (UM web service)</span></span>

<span data-ttu-id="8492d-104">El elemento **OofStatus** contiene un valor que indicaties el estado de Unified Messaging fuera de la oficina del usuario que está realizando una solicitud de [operación GetUMProperties (servicio web de mensajería unificada)](getumproperties-operation-um-web-service.md) .</span><span class="sxs-lookup"><span data-stu-id="8492d-104">The **OofStatus** element contains a value that indicaties the Unified Messaging Out of Office status for the user who is making a [GetUMProperties operation (UM web service)](getumproperties-operation-um-web-service.md) request.</span></span> 
  
[<span data-ttu-id="8492d-105">GetUMPropertiesResponse (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="8492d-105">GetUMPropertiesResponse (UM web service)</span></span>](getumpropertiesresponse-um-web-service.md)
  
[<span data-ttu-id="8492d-106">OofStatus (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="8492d-106">OofStatus (UM web service)</span></span>](oofstatus-um-web-service.md)
  
```xml
<GetUMPropertiesResponse>
    <OofStatus/>
  <MissedCallNotificationEnabled/>
  <PlayOnPhoneDialString/>
  <TelephoneAccessNumbers/>
  <TelephoneAccessFolderEmail/>
</GetUMPropertiesResponse>
```

 <span data-ttu-id="8492d-107">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="8492d-107">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8492d-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="8492d-108">Attributes and elements</span></span>

<span data-ttu-id="8492d-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="8492d-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8492d-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="8492d-110">Attributes</span></span>

<span data-ttu-id="8492d-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="8492d-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8492d-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8492d-112">Child elements</span></span>

<span data-ttu-id="8492d-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="8492d-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8492d-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="8492d-114">Parent elements</span></span>

|<span data-ttu-id="8492d-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="8492d-115">**Element**</span></span>|<span data-ttu-id="8492d-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8492d-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8492d-117">GetUMPropertiesResponse (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="8492d-117">GetUMPropertiesResponse (UM web service)</span></span>](getumpropertiesresponse-um-web-service.md) <br/> |<span data-ttu-id="8492d-118">Define una respuesta a una solicitud de [operación GetUMProperties (servicio web de mensajería unificada)](getumproperties-operation-um-web-service.md) .</span><span class="sxs-lookup"><span data-stu-id="8492d-118">Defines a response to a [GetUMProperties operation (UM web service)](getumproperties-operation-um-web-service.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="8492d-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="8492d-119">Text value</span></span>

<span data-ttu-id="8492d-120">Se requiere un valor de tipo Boolean de texto.</span><span class="sxs-lookup"><span data-stu-id="8492d-120">A Boolean text value is required.</span></span> <span data-ttu-id="8492d-121">Los valores posibles son:</span><span class="sxs-lookup"><span data-stu-id="8492d-121">The following are the possible values:</span></span>
  
- <span data-ttu-id="8492d-122">Verdadero</span><span class="sxs-lookup"><span data-stu-id="8492d-122">True</span></span>
    
- <span data-ttu-id="8492d-123">False</span><span class="sxs-lookup"><span data-stu-id="8492d-123">False</span></span>
    
## <a name="element-information"></a><span data-ttu-id="8492d-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="8492d-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8492d-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8492d-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="8492d-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="8492d-126">Schema Name</span></span>  <br/> |<span data-ttu-id="8492d-127">Mensajes</span><span class="sxs-lookup"><span data-stu-id="8492d-127">Messages</span></span>  <br/> |
|<span data-ttu-id="8492d-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="8492d-128">Validation File</span></span>  <br/> |<span data-ttu-id="8492d-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="8492d-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8492d-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="8492d-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="8492d-131">False</span><span class="sxs-lookup"><span data-stu-id="8492d-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8492d-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="8492d-132">See also</span></span>



[<span data-ttu-id="8492d-133">Operación GetUMProperties (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="8492d-133">GetUMProperties operation (UM web service)</span></span>](getumproperties-operation-um-web-service.md)
  
[<span data-ttu-id="8492d-134">GetUMPropertiesResponse (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="8492d-134">GetUMPropertiesResponse (UM web service)</span></span>](getumpropertiesresponse-um-web-service.md)

