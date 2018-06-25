---
title: Operaciones de servicio de web de mensajería unificadas para Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- Unified
api_type:
- schema
ms.assetid: d92455bd-24e8-4255-9f93-2bdeff00d42d
description: Busque información de referencia para las operaciones del servicio web de mensajería unificada de Exchange.
ms.openlocfilehash: 21d3469d752ff6cdca4ed4ea9151daca52d51e9f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840751"
---
# <a name="unified-messaging-web-service-operations-for-exchange"></a><span data-ttu-id="c01a4-103">Operaciones de servicio de web de mensajería unificadas para Exchange</span><span class="sxs-lookup"><span data-stu-id="c01a4-103">Unified Messaging web service operations for Exchange</span></span>

<span data-ttu-id="c01a4-104">Busque información de referencia para las operaciones del servicio web de mensajería unificada de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c01a4-104">Find reference information for the Unified Messaging web service operations in Exchange.</span></span>
  
<span data-ttu-id="c01a4-105">El servicio web de mensajería unificada proporciona muchas operaciones que permiten a las aplicaciones de cliente leer y cambiar las propiedades de mensajería unificada, reproducir los mensajes de correo de voz, grabar saludos y determinan los elementos del buzón a través de dispositivos de telefonía.</span><span class="sxs-lookup"><span data-stu-id="c01a4-105">The Unified Messaging web service provides many operations that enable client applications to read and change Unified Messaging properties, play voice mail messages, record greetings, and dictate mailbox items over telephony devices.</span></span> <span data-ttu-id="c01a4-106">Los artículos de esta sección proporcionan información acerca de la estructura general de los mensajes de solicitud y respuesta para las operaciones.</span><span class="sxs-lookup"><span data-stu-id="c01a4-106">The articles in this section provide information about the overall structure of the request and response messages for the operations.</span></span> <span data-ttu-id="c01a4-107">Estos artículos proporcionan ejemplos que muestran las estructuras de mensaje comunes.</span><span class="sxs-lookup"><span data-stu-id="c01a4-107">These articles provide examples that show common message structures.</span></span> <span data-ttu-id="c01a4-108">Puede usar estos ejemplos para obtener más información acerca de qué puede hacer con una solicitud de servicio web de mensajería unificada.</span><span class="sxs-lookup"><span data-stu-id="c01a4-108">You can use these examples to learn about what you can do with a Unified Messaging web service request.</span></span>
  
> [!NOTE]
>  <span data-ttu-id="c01a4-109">Para las versiones de Exchange 2010 a partir de Exchange, se recomienda que use las operaciones de mensajería unificada que están disponibles en [Exchange Web Services (EWS)](http://msdn.microsoft.com/library/60285497-0c4e-4e51-84e1-34dd6d89a5d8%28Office.15%29.aspx) en lugar del servicio web de mensajería unificada, por los motivos siguientes: > basada en la dirección URL de EWS Características de mensajería unificadas tienen soporte de primera clase en la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="c01a4-109">For versions of Exchange starting with Exchange 2010, we recommend that you use the Unified Messaging operations that are available in [Exchange Web Services (EWS)](http://msdn.microsoft.com/library/60285497-0c4e-4e51-84e1-34dd6d89a5d8%28Office.15%29.aspx) instead of the Unified Messaging web service, for the following reasons: >  The EWS-based Unified Messaging features have first-class support in the EWS Managed API.</span></span> <span data-ttu-id="c01a4-110">> En las versiones de Exchange a partir de Exchange 2010, se agregan nuevas características de mensajería unificada para EWS, pero no para el servicio web de mensajería unificada.</span><span class="sxs-lookup"><span data-stu-id="c01a4-110">>  In versions of Exchange starting with Exchange 2010, new Unified Messaging features are added to EWS but not to the Unified Messaging web service.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="c01a4-111">En esta sección</span><span class="sxs-lookup"><span data-stu-id="c01a4-111">In this section</span></span>
<span data-ttu-id="c01a4-112"><a name="bk_InThisSection"> </a></span><span class="sxs-lookup"><span data-stu-id="c01a4-112"></span></span>

- [<span data-ttu-id="c01a4-113">(Servicio web de mensajería unificada) de la operación de desconexión</span><span class="sxs-lookup"><span data-stu-id="c01a4-113">Disconnect operation (UM web service)</span></span>](disconnect-operation-um-web-service.md)
    
- [<span data-ttu-id="c01a4-114">Operación GetCallInfo (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="c01a4-114">GetCallInfo operation (UM web service)</span></span>](getcallinfo-operation-um-web-service.md)
    
- [<span data-ttu-id="c01a4-115">Operación GetUMProperties (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="c01a4-115">GetUMProperties operation (UM web service)</span></span>](getumproperties-operation-um-web-service.md)
    
- [<span data-ttu-id="c01a4-116">Operación IsUMEnabled (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="c01a4-116">IsUMEnabled operation (UM web service)</span></span>](isumenabled-operation-um-web-service.md)
    
- [<span data-ttu-id="c01a4-117">Operación PlayOnPhone (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="c01a4-117">PlayOnPhone operation (UM web service)</span></span>](playonphone-operation-um-web-service.md)
    
- [<span data-ttu-id="c01a4-118">Operación PlayOnPhoneGreeting (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="c01a4-118">PlayOnPhoneGreeting operation (UM web service)</span></span>](playonphonegreeting-operation-um-web-service.md)
    
- [<span data-ttu-id="c01a4-119">Operación ResetPIN (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="c01a4-119">ResetPIN operation (UM web service)</span></span>](resetpin-operation-um-web-service.md)
    
- [<span data-ttu-id="c01a4-120">Operación SetMissedCallNotificationEnabled (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="c01a4-120">SetMissedCallNotificationEnabled operation (UM web service)</span></span>](setmissedcallnotificationenabled-operation-um-web-service.md)
    
- [<span data-ttu-id="c01a4-121">Operación SetOofStatus (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="c01a4-121">SetOofStatus operation (UM web service)</span></span>](setoofstatus-operation-um-web-service.md)
    
- [<span data-ttu-id="c01a4-122">Operación SetPlayOnPhoneDialString (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="c01a4-122">SetPlayOnPhoneDialString operation (UM web service)</span></span>](setplayonphonedialstring-operation-um-web-service.md)
    
- [<span data-ttu-id="c01a4-123">Operación SetTelephoneAccessFolderEmail (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="c01a4-123">SetTelephoneAccessFolderEmail operation (UM web service)</span></span>](settelephoneaccessfolderemail-operation-um-web-service.md)
    
## <a name="see-also"></a><span data-ttu-id="c01a4-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="c01a4-124">See also</span></span>

- [<span data-ttu-id="c01a4-125">Referencia de servicio de web de mensajería unificada de Exchange</span><span class="sxs-lookup"><span data-stu-id="c01a4-125">Unified Messaging web service reference for Exchange</span></span>](unified-messaging-web-service-reference-for-exchange.md)
- [<span data-ttu-id="c01a4-126">Detección automática de Exchange</span><span class="sxs-lookup"><span data-stu-id="c01a4-126">Autodiscover for Exchange</span></span>](../exchange-web-services/autodiscover-for-exchange.md)
- [<span data-ttu-id="c01a4-127">Empezar a utilizar servicios web de Exchange</span><span class="sxs-lookup"><span data-stu-id="c01a4-127">Start using web services in Exchange</span></span>](../exchange-web-services/start-using-web-services-in-exchange.md)
    

