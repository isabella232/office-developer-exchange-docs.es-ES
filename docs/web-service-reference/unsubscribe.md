---
title: Cancelar suscripción
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Unsubscribe
api_type:
- schema
ms.assetid: 5584db5f-553a-47ce-85fb-f9902c9990ab
description: El elemento de cancelación de suscripción contiene las propiedades usadas para cancelar la suscripción de una suscripción.
ms.openlocfilehash: bab797ff74a921e3e93c993229bc6d6d289e0c5c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840795"
---
# <a name="unsubscribe"></a><span data-ttu-id="b9eff-103">Cancelar suscripción</span><span class="sxs-lookup"><span data-stu-id="b9eff-103">Unsubscribe</span></span>

<span data-ttu-id="b9eff-104">El elemento de **cancelación de suscripción** contiene las propiedades usadas para cancelar la suscripción de una suscripción.</span><span class="sxs-lookup"><span data-stu-id="b9eff-104">The **Unsubscribe** element contains the properties used to unsubscribe from a subscription.</span></span> 
  
[<span data-ttu-id="b9eff-105">Anular la suscripción</span><span class="sxs-lookup"><span data-stu-id="b9eff-105">Unsubscribe</span></span>](unsubscribe.md)
  
```xml
<Unsubscribe>
   <SubscriptionId/>
</Unsubscribe>
```

 <span data-ttu-id="b9eff-106">**UnsubscribeType**</span><span class="sxs-lookup"><span data-stu-id="b9eff-106">**UnsubscribeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b9eff-107">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b9eff-107">Attributes and elements</span></span>

<span data-ttu-id="b9eff-108">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b9eff-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b9eff-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="b9eff-109">Attributes</span></span>

<span data-ttu-id="b9eff-110">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b9eff-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b9eff-111">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b9eff-111">Child elements</span></span>

|<span data-ttu-id="b9eff-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="b9eff-112">**Element**</span></span>|<span data-ttu-id="b9eff-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b9eff-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b9eff-114">SubscriptionId (GetEvents)</span><span class="sxs-lookup"><span data-stu-id="b9eff-114">SubscriptionId (GetEvents)</span></span>](subscriptionid-getevents.md) <br/> |<span data-ttu-id="b9eff-115">Representa el identificador para una suscripción a.</span><span class="sxs-lookup"><span data-stu-id="b9eff-115">Represents the identifier for a subscription.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b9eff-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b9eff-116">Parent elements</span></span>

<span data-ttu-id="b9eff-117">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b9eff-117">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b9eff-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b9eff-118">Remarks</span></span>

<span data-ttu-id="b9eff-119">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="b9eff-119">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b9eff-120">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b9eff-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b9eff-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b9eff-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b9eff-122">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b9eff-122">Schema name</span></span>  <br/> |<span data-ttu-id="b9eff-123">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="b9eff-123">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b9eff-124">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b9eff-124">Validation file</span></span>  <br/> |<span data-ttu-id="b9eff-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b9eff-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b9eff-126">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b9eff-126">Can be empty</span></span>  <br/> |<span data-ttu-id="b9eff-127">False</span><span class="sxs-lookup"><span data-stu-id="b9eff-127">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b9eff-128">Ver también</span><span class="sxs-lookup"><span data-stu-id="b9eff-128">See also</span></span>



[<span data-ttu-id="b9eff-129">Operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="b9eff-129">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="b9eff-130">Operación GetEvents</span><span class="sxs-lookup"><span data-stu-id="b9eff-130">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="b9eff-131">Cancelar la operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="b9eff-131">Unsubscribe operation</span></span>](unsubscribe-operation.md)

