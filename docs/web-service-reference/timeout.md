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
description: El elemento timeout representa la duración, en minutos, que la suscripción puede permanecer inactiva sin una solicitud GetEvents del cliente.
ms.openlocfilehash: 6f3228cd480bf0eaf259c4f321bc74d0845b9bba
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459899"
---
# <a name="timeout"></a><span data-ttu-id="33d33-103">Timeout</span><span class="sxs-lookup"><span data-stu-id="33d33-103">Timeout</span></span>

<span data-ttu-id="33d33-104">El elemento **timeout** representa la duración, en minutos, que la suscripción puede permanecer inactiva sin una solicitud GetEvents del cliente.</span><span class="sxs-lookup"><span data-stu-id="33d33-104">The **Timeout** element represents the duration, in minutes, that the subscription can remain idle without a GetEvents request from the client.</span></span> 
  
```xml
<Timeout/>
```

 <span data-ttu-id="33d33-105">**int**</span><span class="sxs-lookup"><span data-stu-id="33d33-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="33d33-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="33d33-106">Attributes and elements</span></span>

<span data-ttu-id="33d33-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="33d33-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="33d33-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="33d33-108">Attributes</span></span>

<span data-ttu-id="33d33-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="33d33-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="33d33-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="33d33-110">Child elements</span></span>

<span data-ttu-id="33d33-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="33d33-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="33d33-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="33d33-112">Parent elements</span></span>

|<span data-ttu-id="33d33-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="33d33-113">**Element**</span></span>|<span data-ttu-id="33d33-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="33d33-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="33d33-115">PullSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="33d33-115">PullSubscriptionRequest</span></span>](pullsubscriptionrequest.md) <br/> |<span data-ttu-id="33d33-116">Representa una suscripción a una suscripción de notificación de eventos basada en extracción.</span><span class="sxs-lookup"><span data-stu-id="33d33-116">Represents a subscription to a pull-based event notification subscription.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="33d33-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="33d33-117">Text value</span></span>

<span data-ttu-id="33d33-118">Es necesario un valor de texto que representa un entero si se usa este elemento.</span><span class="sxs-lookup"><span data-stu-id="33d33-118">A text value that represents an integer is required if this element is used.</span></span> <span data-ttu-id="33d33-119">Los valores posibles para este elemento son de 1 a 1440, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="33d33-119">The possible values for this element are 1 to 1440, inclusive.</span></span> <span data-ttu-id="33d33-120">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="33d33-120">This element is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="33d33-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="33d33-121">Remarks</span></span>

<span data-ttu-id="33d33-122">Una solicitud GetEvents correcta restablece el temporizador de tiempo de espera de la suscripción.</span><span class="sxs-lookup"><span data-stu-id="33d33-122">The timeout timer for the subscription is reset by a successful GetEvents request.</span></span>
  
<span data-ttu-id="33d33-123">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="33d33-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="33d33-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="33d33-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="33d33-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="33d33-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="33d33-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="33d33-126">Schema name</span></span>  <br/> |<span data-ttu-id="33d33-127">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="33d33-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="33d33-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="33d33-128">Validation file</span></span>  <br/> |<span data-ttu-id="33d33-129">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="33d33-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="33d33-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="33d33-130">Can be empty</span></span>  <br/> |<span data-ttu-id="33d33-131">Falso</span><span class="sxs-lookup"><span data-stu-id="33d33-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="33d33-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="33d33-132">See also</span></span>



[<span data-ttu-id="33d33-133">Operación subscribe</span><span class="sxs-lookup"><span data-stu-id="33d33-133">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="33d33-134">Operación GetEvents</span><span class="sxs-lookup"><span data-stu-id="33d33-134">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="33d33-135">Operación unsubscribe</span><span class="sxs-lookup"><span data-stu-id="33d33-135">Unsubscribe operation</span></span>](unsubscribe-operation.md)

