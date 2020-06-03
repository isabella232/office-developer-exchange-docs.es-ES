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
ms.openlocfilehash: 4ee9a0dda3d887f8fbfa2c2b34a9a077e7af37ba
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464892"
---
# <a name="sendnotificationresult"></a><span data-ttu-id="414e8-103">SendNotificationResult</span><span class="sxs-lookup"><span data-stu-id="414e8-103">SendNotificationResult</span></span>

<span data-ttu-id="414e8-104">El elemento **SendNotificationResult** contiene la respuesta de una aplicación cliente a una notificación de inserción.</span><span class="sxs-lookup"><span data-stu-id="414e8-104">The **SendNotificationResult** element contains the response of a client application to a push notification.</span></span> 
  
```xml
<SendNotificationResult>
   <SubscriptionStatus/>
</SendNotificationResult>
```

 <span data-ttu-id="414e8-105">**SendNotificationResultType**</span><span class="sxs-lookup"><span data-stu-id="414e8-105">**SendNotificationResultType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="414e8-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="414e8-106">Attributes and elements</span></span>

<span data-ttu-id="414e8-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="414e8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="414e8-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="414e8-108">Attributes</span></span>

<span data-ttu-id="414e8-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="414e8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="414e8-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="414e8-110">Child elements</span></span>

|<span data-ttu-id="414e8-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="414e8-111">**Element**</span></span>|<span data-ttu-id="414e8-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="414e8-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="414e8-113">SubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="414e8-113">SubscriptionStatus</span></span>](subscriptionstatus.md) <br/> |<span data-ttu-id="414e8-114">Describe el estado de una suscripción de inserción.</span><span class="sxs-lookup"><span data-stu-id="414e8-114">Describes the status of a push subscription.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="414e8-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="414e8-115">Parent elements</span></span>

<span data-ttu-id="414e8-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="414e8-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="414e8-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="414e8-117">Remarks</span></span>

<span data-ttu-id="414e8-118">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="414e8-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="414e8-119">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="414e8-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="414e8-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="414e8-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="414e8-121">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="414e8-121">Schema Name</span></span>  <br/> |<span data-ttu-id="414e8-122">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="414e8-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="414e8-123">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="414e8-123">Validation File</span></span>  <br/> |<span data-ttu-id="414e8-124">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="414e8-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="414e8-125">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="414e8-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="414e8-126">Falso</span><span class="sxs-lookup"><span data-stu-id="414e8-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="414e8-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="414e8-127">See also</span></span>



- [<span data-ttu-id="414e8-128">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="414e8-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

