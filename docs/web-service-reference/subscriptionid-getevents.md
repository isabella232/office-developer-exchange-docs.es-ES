---
title: SubscriptionId (GetEvents)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SubscriptionId
api_type:
- schema
ms.assetid: 77c0abab-69e8-428e-8c20-22258e4ef71b
description: El elemento SubscriptionId representa el identificador para una suscripción a.
ms.openlocfilehash: 8867b7da7c75cfd9d41f708c0481627d5186cc14
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837622"
---
# <a name="subscriptionid-getevents"></a><span data-ttu-id="de65a-103">SubscriptionId (GetEvents)</span><span class="sxs-lookup"><span data-stu-id="de65a-103">SubscriptionId (GetEvents)</span></span>

<span data-ttu-id="de65a-104">El elemento **SubscriptionId** representa el identificador para una suscripción a.</span><span class="sxs-lookup"><span data-stu-id="de65a-104">The **SubscriptionId** element represents the identifier for a subscription.</span></span> 
  
```xml
<SubscriptionId/>
```

 <span data-ttu-id="de65a-105">**SubscriptionIdType**</span><span class="sxs-lookup"><span data-stu-id="de65a-105">**SubscriptionIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="de65a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="de65a-106">Attributes and elements</span></span>

<span data-ttu-id="de65a-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="de65a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="de65a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="de65a-108">Attributes</span></span>

<span data-ttu-id="de65a-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="de65a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="de65a-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="de65a-110">Child elements</span></span>

<span data-ttu-id="de65a-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="de65a-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="de65a-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="de65a-112">Parent elements</span></span>

|<span data-ttu-id="de65a-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="de65a-113">**Element**</span></span>|<span data-ttu-id="de65a-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="de65a-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="de65a-115">GetEvents</span><span class="sxs-lookup"><span data-stu-id="de65a-115">GetEvents</span></span>](getevents.md) <br/> |<span data-ttu-id="de65a-116">Representa la operación usada por los clientes de extracción para las notificaciones de solicitud desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="de65a-116">Represents the operation used by pull clients to request notifications from the server.</span></span>  <br/> |
|[<span data-ttu-id="de65a-117">Notificación</span><span class="sxs-lookup"><span data-stu-id="de65a-117">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="de65a-118">Contiene información acerca de la suscripción y los eventos que se han producido desde la última notificación.</span><span class="sxs-lookup"><span data-stu-id="de65a-118">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
|[<span data-ttu-id="de65a-119">SubscribeResponseMessage</span><span class="sxs-lookup"><span data-stu-id="de65a-119">SubscribeResponseMessage</span></span>](subscriberesponsemessage.md) <br/> |<span data-ttu-id="de65a-120">Contiene el estado y el resultado de una solicitud Subscribe.</span><span class="sxs-lookup"><span data-stu-id="de65a-120">Contains the status and result of a Subscribe request.</span></span>  <br/> |
|[<span data-ttu-id="de65a-121">Anular la suscripción</span><span class="sxs-lookup"><span data-stu-id="de65a-121">Unsubscribe</span></span>](unsubscribe.md) <br/> |<span data-ttu-id="de65a-122">Contiene las propiedades usadas para cancelar la suscripción de una suscripción.</span><span class="sxs-lookup"><span data-stu-id="de65a-122">Contains the properties used to unsubscribe from a subscription.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="de65a-123">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="de65a-123">Text value</span></span>

<span data-ttu-id="de65a-124">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="de65a-124">A text value is required.</span></span> <span data-ttu-id="de65a-125">El valor de texto es un GUID.</span><span class="sxs-lookup"><span data-stu-id="de65a-125">The text value is a GUID.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="de65a-126">Notas</span><span class="sxs-lookup"><span data-stu-id="de65a-126">Remarks</span></span>

<span data-ttu-id="de65a-127">El GUID que representa el identificador de suscripción es generado por el servidor de acceso de cliente cuando se crea la suscripción.</span><span class="sxs-lookup"><span data-stu-id="de65a-127">The GUID that represents the subscription identifier is generated by the Client Access server when the subscription is created.</span></span>
  
<span data-ttu-id="de65a-128">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="de65a-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="de65a-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="de65a-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="de65a-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="de65a-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="de65a-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="de65a-131">Schema name</span></span>  <br/> |<span data-ttu-id="de65a-132">esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="de65a-132">messages schema</span></span>  <br/> |
|<span data-ttu-id="de65a-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="de65a-133">Validation file</span></span>  <br/> |<span data-ttu-id="de65a-134">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="de65a-134">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="de65a-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="de65a-135">Can be empty</span></span>  <br/> |<span data-ttu-id="de65a-136">False</span><span class="sxs-lookup"><span data-stu-id="de65a-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="de65a-137">Ver también</span><span class="sxs-lookup"><span data-stu-id="de65a-137">See also</span></span>



[<span data-ttu-id="de65a-138">Operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="de65a-138">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="de65a-139">Operación GetEvents</span><span class="sxs-lookup"><span data-stu-id="de65a-139">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="de65a-140">Cancelar la operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="de65a-140">Unsubscribe operation</span></span>](unsubscribe-operation.md)

