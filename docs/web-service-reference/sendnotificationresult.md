---
title: SendNotificationResult
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SendNotificationResult
api_type:
- schema
ms.assetid: fa9d6202-fa66-4f10-9858-53f4f1ce14bc
description: El elemento SendNotificationResult contiene la respuesta de una aplicación cliente a una notificación de inserción.
ms.openlocfilehash: 9acaa396430cf4e06a9c996834874d19dcab50ac
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837350"
---
# <a name="sendnotificationresult"></a><span data-ttu-id="3503f-103">SendNotificationResult</span><span class="sxs-lookup"><span data-stu-id="3503f-103">SendNotificationResult</span></span>

<span data-ttu-id="3503f-104">El elemento **SendNotificationResult** contiene la respuesta de una aplicación cliente a una notificación de inserción.</span><span class="sxs-lookup"><span data-stu-id="3503f-104">The **SendNotificationResult** element contains the response of a client application to a push notification.</span></span> 
  
```xml
<SendNotificationResult>
   <SubscriptionStatus/>
</SendNotificationResult>
```

 <span data-ttu-id="3503f-105">**SendNotificationResultType**</span><span class="sxs-lookup"><span data-stu-id="3503f-105">**SendNotificationResultType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3503f-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3503f-106">Attributes and elements</span></span>

<span data-ttu-id="3503f-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3503f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3503f-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="3503f-108">Attributes</span></span>

<span data-ttu-id="3503f-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3503f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3503f-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3503f-110">Child elements</span></span>

|<span data-ttu-id="3503f-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="3503f-111">**Element**</span></span>|<span data-ttu-id="3503f-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3503f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3503f-113">SubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="3503f-113">SubscriptionStatus</span></span>](subscriptionstatus.md) <br/> |<span data-ttu-id="3503f-114">Describe el estado de una suscripción de inserción.</span><span class="sxs-lookup"><span data-stu-id="3503f-114">Describes the status of a push subscription.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3503f-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3503f-115">Parent elements</span></span>

<span data-ttu-id="3503f-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3503f-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3503f-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3503f-117">Remarks</span></span>

<span data-ttu-id="3503f-118">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="3503f-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3503f-119">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3503f-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3503f-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3503f-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3503f-121">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3503f-121">Schema Name</span></span>  <br/> |<span data-ttu-id="3503f-122">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="3503f-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="3503f-123">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3503f-123">Validation File</span></span>  <br/> |<span data-ttu-id="3503f-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="3503f-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3503f-125">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3503f-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="3503f-126">False</span><span class="sxs-lookup"><span data-stu-id="3503f-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3503f-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="3503f-127">See also</span></span>



- [<span data-ttu-id="3503f-128">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="3503f-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

