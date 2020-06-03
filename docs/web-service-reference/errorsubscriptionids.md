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
description: El elemento ErrorSubscriptionIds contiene una matriz de identificadores de suscripción no válidos.
ms.openlocfilehash: bdc5c86560800464d677a9043607bed3f7872e32
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526189"
---
# <a name="errorsubscriptionids"></a><span data-ttu-id="09d85-103">ErrorSubscriptionIds</span><span class="sxs-lookup"><span data-stu-id="09d85-103">ErrorSubscriptionIds</span></span>

<span data-ttu-id="09d85-104">El elemento **ErrorSubscriptionIds** contiene una matriz de identificadores de suscripción no válidos.</span><span class="sxs-lookup"><span data-stu-id="09d85-104">The **ErrorSubscriptionIds** element contains an array of invalid subscription IDs.</span></span> 
  
```xml
<ErrorSubscriptionIds>
   <SubscriptionId/>
</ErrorSubscriptionIds>
```

 <span data-ttu-id="09d85-105">**NonEmptyArrayOfSubscriptionIdsType**</span><span class="sxs-lookup"><span data-stu-id="09d85-105">**NonEmptyArrayOfSubscriptionIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="09d85-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="09d85-106">Attributes and elements</span></span>

<span data-ttu-id="09d85-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="09d85-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="09d85-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="09d85-108">Attributes</span></span>

<span data-ttu-id="09d85-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="09d85-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="09d85-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="09d85-110">Child elements</span></span>

|<span data-ttu-id="09d85-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="09d85-111">**Element**</span></span>|<span data-ttu-id="09d85-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="09d85-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="09d85-113">SubscriptionId (GetEvents)</span><span class="sxs-lookup"><span data-stu-id="09d85-113">SubscriptionId (GetEvents)</span></span>](subscriptionid-getevents.md) <br/> |<span data-ttu-id="09d85-114">Representa el identificador de una suscripción.</span><span class="sxs-lookup"><span data-stu-id="09d85-114">Represents the identifier for a subscription.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="09d85-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="09d85-115">Parent elements</span></span>

|<span data-ttu-id="09d85-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="09d85-116">**Element**</span></span>|<span data-ttu-id="09d85-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="09d85-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="09d85-118">GetStreamingEventsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="09d85-118">GetStreamingEventsResponseMessage</span></span>](getstreamingeventsresponsemessage.md) <br/> |<span data-ttu-id="09d85-119">Contiene el estado y el resultado de una sola solicitud de [operación GetStreamingEvents](getstreamingevents-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="09d85-119">Contains the status and result of a single [GetStreamingEvents operation](getstreamingevents-operation.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="09d85-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="09d85-120">Text value</span></span>

<span data-ttu-id="09d85-121">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="09d85-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="09d85-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="09d85-122">Remarks</span></span>

<span data-ttu-id="09d85-123">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange. este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="09d85-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="09d85-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="09d85-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="09d85-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="09d85-125">Namespace</span></span>  <br/> |<span data-ttu-id="09d85-126">https://schemas.microsoft.com/exchange/services/2006/messages y https://schemas.microsoft.com/exchange/services/2006/types</span><span class="sxs-lookup"><span data-stu-id="09d85-126">https://schemas.microsoft.com/exchange/services/2006/messages and https://schemas.microsoft.com/exchange/services/2006/types</span></span>  <br/> |
|<span data-ttu-id="09d85-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="09d85-127">Schema Name</span></span>  <br/> |<span data-ttu-id="09d85-128">Esquema de mensajes; Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="09d85-128">Messages schema; Types schema</span></span>  <br/> |
|<span data-ttu-id="09d85-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="09d85-129">Validation File</span></span>  <br/> |<span data-ttu-id="09d85-130">Messages. xsd; Types. xsd</span><span class="sxs-lookup"><span data-stu-id="09d85-130">Messages.xsd; Types.xsd</span></span>  <br/> |
|<span data-ttu-id="09d85-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="09d85-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="09d85-132">Falso</span><span class="sxs-lookup"><span data-stu-id="09d85-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="09d85-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="09d85-133">See also</span></span>



[<span data-ttu-id="09d85-134">Operación GetStreamingEvents</span><span class="sxs-lookup"><span data-stu-id="09d85-134">GetStreamingEvents operation</span></span>](getstreamingevents-operation.md)


- [<span data-ttu-id="09d85-135">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="09d85-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

