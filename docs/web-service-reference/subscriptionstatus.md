---
title: SubscriptionStatus
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SubscriptionStatus
api_type:
- schema
ms.assetid: 2d64ebb7-f26a-4d02-b7ef-d9d7da75f0c3
description: El elemento SubscriptionStatus describe el estado de una suscripción de inserción.
ms.openlocfilehash: 195ab229380f4386b39e5c3fd48208cf66e224f0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530947"
---
# <a name="subscriptionstatus"></a><span data-ttu-id="48f53-103">SubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="48f53-103">SubscriptionStatus</span></span>

<span data-ttu-id="48f53-104">El elemento **SubscriptionStatus** describe el estado de una suscripción de inserción.</span><span class="sxs-lookup"><span data-stu-id="48f53-104">The **SubscriptionStatus** element describes the status of a push subscription.</span></span> 
  
```xml
<SubscriptionStatus>OK or Unsubscribe</SubscriptionStatus>
```

 <span data-ttu-id="48f53-105">**SubscriptionStatusType**</span><span class="sxs-lookup"><span data-stu-id="48f53-105">**SubscriptionStatusType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="48f53-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="48f53-106">Attributes and elements</span></span>

<span data-ttu-id="48f53-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="48f53-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="48f53-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="48f53-108">Attributes</span></span>

<span data-ttu-id="48f53-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="48f53-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="48f53-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="48f53-110">Child elements</span></span>

<span data-ttu-id="48f53-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="48f53-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="48f53-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="48f53-112">Parent elements</span></span>

|<span data-ttu-id="48f53-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="48f53-113">**Element**</span></span>|<span data-ttu-id="48f53-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="48f53-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="48f53-115">SendNotificationResult</span><span class="sxs-lookup"><span data-stu-id="48f53-115">SendNotificationResult</span></span>](sendnotificationresult.md) <br/> |<span data-ttu-id="48f53-116">Contiene la respuesta de la aplicación cliente ' a una notificación de inserción.</span><span class="sxs-lookup"><span data-stu-id="48f53-116">Contains the response of the client application' to a push notification.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="48f53-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="48f53-117">Text value</span></span>

<span data-ttu-id="48f53-118">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="48f53-118">A text value is required.</span></span> <span data-ttu-id="48f53-119">A continuación se muestran los valores de texto posibles para este elemento:</span><span class="sxs-lookup"><span data-stu-id="48f53-119">The following are the possible text values for this element:</span></span>
  
- <span data-ttu-id="48f53-120">Aceptar</span><span class="sxs-lookup"><span data-stu-id="48f53-120">OK</span></span>
    
- <span data-ttu-id="48f53-121">Cancelar suscripción</span><span class="sxs-lookup"><span data-stu-id="48f53-121">Unsubscribe</span></span>
    
## <a name="remarks"></a><span data-ttu-id="48f53-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="48f53-122">Remarks</span></span>

<span data-ttu-id="48f53-123">Este elemento describe el estado de la suscripción.</span><span class="sxs-lookup"><span data-stu-id="48f53-123">This element describes the status of the subscription.</span></span> <span data-ttu-id="48f53-124">La aplicación cliente de suscripción de inserción devuelve el estado al equipo que ejecuta Exchange 2007 y que tiene instalado el rol de servidor acceso de clientes después de cada notificación de inserción.</span><span class="sxs-lookup"><span data-stu-id="48f53-124">The push subscription client application sends the status back to the computer that is running Exchange 2007 that has the Client Access server role installed after each push notification.</span></span> <span data-ttu-id="48f53-125">Si el valor **SubscriptionStatus** es igual a **unsubscribe**, el servidor de acceso de cliente dejará de enviar notificaciones y finalizará la suscripción.</span><span class="sxs-lookup"><span data-stu-id="48f53-125">If the **SubscriptionStatus** value equals **Unsubscribe**, the Client Access server will stop sending notifications and end the subscription.</span></span> <span data-ttu-id="48f53-126">Si el valor de **SubscriptionStatus** es **correcto**, el servidor de acceso de cliente seguirá enviando notificaciones.</span><span class="sxs-lookup"><span data-stu-id="48f53-126">If the **SubscriptionStatus** value equals **OK**, the Client Access server will continue to send notifications.</span></span>
  
<span data-ttu-id="48f53-127">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="48f53-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="48f53-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="48f53-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="48f53-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="48f53-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="48f53-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="48f53-130">Schema Name</span></span>  <br/> |<span data-ttu-id="48f53-131">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="48f53-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="48f53-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="48f53-132">Validation File</span></span>  <br/> |<span data-ttu-id="48f53-133">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="48f53-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="48f53-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="48f53-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="48f53-135">Falso</span><span class="sxs-lookup"><span data-stu-id="48f53-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="48f53-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="48f53-136">See also</span></span>



- [<span data-ttu-id="48f53-137">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="48f53-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

