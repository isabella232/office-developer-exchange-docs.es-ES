---
title: ErrorSubscriptionIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ErrorSubscriptionIds
api_type:
- schema
ms.assetid: e64e76ff-4d98-4082-9acc-a1114ae45f44
description: El elemento ErrorSubscriptionIds contiene una matriz de identificadores de suscripción no válida.
ms.openlocfilehash: 5cdbbeb1083754510f431bc092bb67dc0addecab
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764450"
---
# <a name="errorsubscriptionids"></a><span data-ttu-id="f8c0f-103">ErrorSubscriptionIds</span><span class="sxs-lookup"><span data-stu-id="f8c0f-103">ErrorSubscriptionIds</span></span>

<span data-ttu-id="f8c0f-104">El elemento **ErrorSubscriptionIds** contiene una matriz de identificadores de suscripción no válida.</span><span class="sxs-lookup"><span data-stu-id="f8c0f-104">The **ErrorSubscriptionIds** element contains an array of invalid subscription IDs.</span></span> 
  
```xml
<ErrorSubscriptionIds>
   <SubscriptionId/>
</ErrorSubscriptionIds>
```

 <span data-ttu-id="f8c0f-105">**NonEmptyArrayOfSubscriptionIdsType**</span><span class="sxs-lookup"><span data-stu-id="f8c0f-105">**NonEmptyArrayOfSubscriptionIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f8c0f-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f8c0f-106">Attributes and elements</span></span>

<span data-ttu-id="f8c0f-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f8c0f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f8c0f-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="f8c0f-108">Attributes</span></span>

<span data-ttu-id="f8c0f-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f8c0f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f8c0f-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f8c0f-110">Child elements</span></span>

|<span data-ttu-id="f8c0f-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="f8c0f-111">**Element**</span></span>|<span data-ttu-id="f8c0f-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f8c0f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f8c0f-113">SubscriptionId (GetEvents)</span><span class="sxs-lookup"><span data-stu-id="f8c0f-113">SubscriptionId (GetEvents)</span></span>](subscriptionid-getevents.md) <br/> |<span data-ttu-id="f8c0f-114">Representa el identificador para una suscripción a.</span><span class="sxs-lookup"><span data-stu-id="f8c0f-114">Represents the identifier for a subscription.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f8c0f-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f8c0f-115">Parent elements</span></span>

|<span data-ttu-id="f8c0f-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="f8c0f-116">**Element**</span></span>|<span data-ttu-id="f8c0f-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f8c0f-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f8c0f-118">GetStreamingEventsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="f8c0f-118">GetStreamingEventsResponseMessage</span></span>](getstreamingeventsresponsemessage.md) <br/> |<span data-ttu-id="f8c0f-119">Contiene el estado y el resultado de una única solicitud de [operación GetStreamingEvents](getstreamingevents-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="f8c0f-119">Contains the status and result of a single [GetStreamingEvents operation](getstreamingevents-operation.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f8c0f-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="f8c0f-120">Text value</span></span>

<span data-ttu-id="f8c0f-121">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f8c0f-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f8c0f-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f8c0f-122">Remarks</span></span>

<span data-ttu-id="f8c0f-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda Exchange Web Services.This elemento fue introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="f8c0f-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f8c0f-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f8c0f-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f8c0f-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f8c0f-125">Namespace</span></span>  <br/> |<span data-ttu-id="f8c0f-126">http://schemas.microsoft.com/exchange/services/2006/messages y http://schemas.microsoft.com/exchange/services/2006/types</span><span class="sxs-lookup"><span data-stu-id="f8c0f-126">http://schemas.microsoft.com/exchange/services/2006/messages and http://schemas.microsoft.com/exchange/services/2006/types</span></span>  <br/> |
|<span data-ttu-id="f8c0f-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f8c0f-127">Schema Name</span></span>  <br/> |<span data-ttu-id="f8c0f-128">Esquema de los mensajes; Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="f8c0f-128">Messages schema; Types schema</span></span>  <br/> |
|<span data-ttu-id="f8c0f-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f8c0f-129">Validation File</span></span>  <br/> |<span data-ttu-id="f8c0f-130">Messages.xsd; Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f8c0f-130">Messages.xsd; Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f8c0f-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f8c0f-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="f8c0f-132">False</span><span class="sxs-lookup"><span data-stu-id="f8c0f-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f8c0f-133">Ver también</span><span class="sxs-lookup"><span data-stu-id="f8c0f-133">See also</span></span>



[<span data-ttu-id="f8c0f-134">Operación GetStreamingEvents</span><span class="sxs-lookup"><span data-stu-id="f8c0f-134">GetStreamingEvents operation</span></span>](getstreamingevents-operation.md)


- [<span data-ttu-id="f8c0f-135">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="f8c0f-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

