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
ms.openlocfilehash: 1f6de15f7a3b07714899aef2ff74a8d556f8ca1d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840595"
---
# <a name="subscriptionstatus"></a><span data-ttu-id="7d671-103">SubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="7d671-103">SubscriptionStatus</span></span>

<span data-ttu-id="7d671-104">El elemento **SubscriptionStatus** describe el estado de una suscripción de inserción.</span><span class="sxs-lookup"><span data-stu-id="7d671-104">The **SubscriptionStatus** element describes the status of a push subscription.</span></span> 
  
```xml
<SubscriptionStatus>OK or Unsubscribe</SubscriptionStatus>
```

 <span data-ttu-id="7d671-105">**SubscriptionStatusType**</span><span class="sxs-lookup"><span data-stu-id="7d671-105">**SubscriptionStatusType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7d671-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="7d671-106">Attributes and elements</span></span>

<span data-ttu-id="7d671-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="7d671-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7d671-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="7d671-108">Attributes</span></span>

<span data-ttu-id="7d671-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7d671-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7d671-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7d671-110">Child elements</span></span>

<span data-ttu-id="7d671-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7d671-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7d671-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7d671-112">Parent elements</span></span>

|<span data-ttu-id="7d671-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="7d671-113">**Element**</span></span>|<span data-ttu-id="7d671-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7d671-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7d671-115">SendNotificationResult</span><span class="sxs-lookup"><span data-stu-id="7d671-115">SendNotificationResult</span></span>](sendnotificationresult.md) <br/> |<span data-ttu-id="7d671-116">Contiene la respuesta de la aplicación cliente ' a una notificación de inserción.</span><span class="sxs-lookup"><span data-stu-id="7d671-116">Contains the response of the client application' to a push notification.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7d671-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="7d671-117">Text value</span></span>

<span data-ttu-id="7d671-118">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="7d671-118">A text value is required.</span></span> <span data-ttu-id="7d671-119">Los siguientes son los posibles valores de texto para este elemento:</span><span class="sxs-lookup"><span data-stu-id="7d671-119">The following are the possible text values for this element:</span></span>
  
- <span data-ttu-id="7d671-120">Aceptar</span><span class="sxs-lookup"><span data-stu-id="7d671-120">OK</span></span>
    
- <span data-ttu-id="7d671-121">Cancelar suscripción</span><span class="sxs-lookup"><span data-stu-id="7d671-121">Unsubscribe</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7d671-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7d671-122">Remarks</span></span>

<span data-ttu-id="7d671-123">Este elemento describe el estado de la suscripción.</span><span class="sxs-lookup"><span data-stu-id="7d671-123">This element describes the status of the subscription.</span></span> <span data-ttu-id="7d671-124">La aplicación de cliente de suscripción de inserción envía el estado al equipo que ejecuta Exchange 2007 que tiene el rol de servidor de acceso de cliente instalado después de cada notificación de inserción.</span><span class="sxs-lookup"><span data-stu-id="7d671-124">The push subscription client application sends the status back to the computer that is running Exchange 2007 that has the Client Access server role installed after each push notification.</span></span> <span data-ttu-id="7d671-125">Si el valor de **SubscriptionStatus** es igual a **Cancelar la suscripción**, el servidor de acceso de cliente detendrá enviar notificaciones y finalizar la suscripción.</span><span class="sxs-lookup"><span data-stu-id="7d671-125">If the **SubscriptionStatus** value equals **Unsubscribe**, the Client Access server will stop sending notifications and end the subscription.</span></span> <span data-ttu-id="7d671-126">Si el valor de **SubscriptionStatus** es igual a **Aceptar**, el servidor de acceso de cliente continuará enviar notificaciones.</span><span class="sxs-lookup"><span data-stu-id="7d671-126">If the **SubscriptionStatus** value equals **OK**, the Client Access server will continue to send notifications.</span></span>
  
<span data-ttu-id="7d671-127">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="7d671-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7d671-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7d671-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7d671-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7d671-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="7d671-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="7d671-130">Schema Name</span></span>  <br/> |<span data-ttu-id="7d671-131">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="7d671-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="7d671-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="7d671-132">Validation File</span></span>  <br/> |<span data-ttu-id="7d671-133">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="7d671-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7d671-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="7d671-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="7d671-135">False</span><span class="sxs-lookup"><span data-stu-id="7d671-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7d671-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="7d671-136">See also</span></span>



- [<span data-ttu-id="7d671-137">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="7d671-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

