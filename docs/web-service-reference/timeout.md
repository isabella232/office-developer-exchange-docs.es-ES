---
title: Timeout
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Timeout
api_type:
- schema
ms.assetid: c2e1ca5a-6667-4f6f-aac4-89de33bddc54
description: El elemento de tiempo de espera representa la duración, en minutos, que puede permanecer inactiva sin una solicitud GetEvents desde el cliente de la suscripción.
ms.openlocfilehash: 0a26002689e131959f09318b01d97ffb73b605f9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840674"
---
# <a name="timeout"></a><span data-ttu-id="23602-103">Timeout</span><span class="sxs-lookup"><span data-stu-id="23602-103">Timeout</span></span>

<span data-ttu-id="23602-104">El elemento de **tiempo de espera** representa la duración, en minutos, que puede permanecer inactiva sin una solicitud GetEvents desde el cliente de la suscripción.</span><span class="sxs-lookup"><span data-stu-id="23602-104">The **Timeout** element represents the duration, in minutes, that the subscription can remain idle without a GetEvents request from the client.</span></span> 
  
```xml
<Timeout/>
```

 <span data-ttu-id="23602-105">**int**</span><span class="sxs-lookup"><span data-stu-id="23602-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="23602-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="23602-106">Attributes and elements</span></span>

<span data-ttu-id="23602-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="23602-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="23602-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="23602-108">Attributes</span></span>

<span data-ttu-id="23602-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="23602-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="23602-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="23602-110">Child elements</span></span>

<span data-ttu-id="23602-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="23602-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="23602-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="23602-112">Parent elements</span></span>

|<span data-ttu-id="23602-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="23602-113">**Element**</span></span>|<span data-ttu-id="23602-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="23602-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="23602-115">PullSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="23602-115">PullSubscriptionRequest</span></span>](pullsubscriptionrequest.md) <br/> |<span data-ttu-id="23602-116">Representa una suscripción a una suscripción de notificación de eventos basado en la extracción.</span><span class="sxs-lookup"><span data-stu-id="23602-116">Represents a subscription to a pull-based event notification subscription.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="23602-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="23602-117">Text value</span></span>

<span data-ttu-id="23602-118">Si se usa este elemento, es necesario un valor de texto que representa un número entero.</span><span class="sxs-lookup"><span data-stu-id="23602-118">A text value that represents an integer is required if this element is used.</span></span> <span data-ttu-id="23602-119">Los valores posibles para este elemento son 1 y 1440, ambos inclusive.</span><span class="sxs-lookup"><span data-stu-id="23602-119">The possible values for this element are 1 to 1440, inclusive.</span></span> <span data-ttu-id="23602-120">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="23602-120">This element is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="23602-121">Notas</span><span class="sxs-lookup"><span data-stu-id="23602-121">Remarks</span></span>

<span data-ttu-id="23602-122">Se restablece el temporizador de tiempo de espera de la suscripción a una solicitud de GetEvents correcta.</span><span class="sxs-lookup"><span data-stu-id="23602-122">The timeout timer for the subscription is reset by a successful GetEvents request.</span></span>
  
<span data-ttu-id="23602-123">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="23602-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="23602-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="23602-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="23602-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="23602-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="23602-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="23602-126">Schema name</span></span>  <br/> |<span data-ttu-id="23602-127">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="23602-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="23602-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="23602-128">Validation file</span></span>  <br/> |<span data-ttu-id="23602-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="23602-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="23602-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="23602-130">Can be empty</span></span>  <br/> |<span data-ttu-id="23602-131">False</span><span class="sxs-lookup"><span data-stu-id="23602-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="23602-132">Ver también</span><span class="sxs-lookup"><span data-stu-id="23602-132">See also</span></span>



[<span data-ttu-id="23602-133">Operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="23602-133">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="23602-134">Operación GetEvents</span><span class="sxs-lookup"><span data-stu-id="23602-134">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="23602-135">Cancelar la operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="23602-135">Unsubscribe operation</span></span>](unsubscribe-operation.md)

