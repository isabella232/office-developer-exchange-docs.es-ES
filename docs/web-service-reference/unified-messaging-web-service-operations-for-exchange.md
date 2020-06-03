---
title: Operaciones del servicio Web de mensajería unificada para Exchange
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
description: Busque información de referencia para las operaciones del servicio Web de mensajería unificada en Exchange.
ms.openlocfilehash: b13ca2fbc44846db0bc98b3961916ba5d0872310
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529717"
---
# <a name="unified-messaging-web-service-operations-for-exchange"></a><span data-ttu-id="954f5-103">Operaciones del servicio Web de mensajería unificada para Exchange</span><span class="sxs-lookup"><span data-stu-id="954f5-103">Unified Messaging web service operations for Exchange</span></span>

<span data-ttu-id="954f5-104">Busque información de referencia para las operaciones del servicio Web de mensajería unificada en Exchange.</span><span class="sxs-lookup"><span data-stu-id="954f5-104">Find reference information for the Unified Messaging web service operations in Exchange.</span></span>
  
<span data-ttu-id="954f5-105">El servicio Web de mensajería unificada proporciona muchas operaciones que permiten a las aplicaciones de cliente leer y cambiar las propiedades de mensajería unificada, reproducir mensajes de correo de voz, grabar saludos y dictar elementos de buzón a través de dispositivos de telefonía.</span><span class="sxs-lookup"><span data-stu-id="954f5-105">The Unified Messaging web service provides many operations that enable client applications to read and change Unified Messaging properties, play voice mail messages, record greetings, and dictate mailbox items over telephony devices.</span></span> <span data-ttu-id="954f5-106">En los artículos de esta sección se proporciona información acerca de la estructura general de los mensajes de solicitud y respuesta para las operaciones.</span><span class="sxs-lookup"><span data-stu-id="954f5-106">The articles in this section provide information about the overall structure of the request and response messages for the operations.</span></span> <span data-ttu-id="954f5-107">En estos artículos se proporcionan ejemplos que muestran estructuras de mensajes comunes.</span><span class="sxs-lookup"><span data-stu-id="954f5-107">These articles provide examples that show common message structures.</span></span> <span data-ttu-id="954f5-108">Puede usar estos ejemplos para obtener información sobre lo que puede hacer con una solicitud de servicio Web de mensajería unificada.</span><span class="sxs-lookup"><span data-stu-id="954f5-108">You can use these examples to learn about what you can do with a Unified Messaging web service request.</span></span>
  
> [!NOTE]
> <span data-ttu-id="954f5-109">Para las versiones de Exchange a partir de Exchange 2010, le recomendamos que use las operaciones de mensajería unificada que están disponibles en los [servicios web Exchange (EWS)](https://msdn.microsoft.com/library/60285497-0c4e-4e51-84e1-34dd6d89a5d8%28Office.15%29.aspx) en lugar del servicio Web de mensajería unificada, por los siguientes motivos:</span><span class="sxs-lookup"><span data-stu-id="954f5-109">For versions of Exchange starting with Exchange 2010, we recommend that you use the Unified Messaging operations that are available in [Exchange Web Services (EWS)](https://msdn.microsoft.com/library/60285497-0c4e-4e51-84e1-34dd6d89a5d8%28Office.15%29.aspx) instead of the Unified Messaging web service, for the following reasons:</span></span> 
> - <span data-ttu-id="954f5-110">Las características de mensajería unificada basadas en EWS tienen compatibilidad de primera clase en la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="954f5-110">The EWS-based Unified Messaging features have first-class support in the EWS Managed API.</span></span> 
> - <span data-ttu-id="954f5-111">En las versiones de Exchange a partir de Exchange 2010, se agregan nuevas características de mensajería unificada a EWS, pero no al servicio Web de mensajería unificada.</span><span class="sxs-lookup"><span data-stu-id="954f5-111">In versions of Exchange starting with Exchange 2010, new Unified Messaging features are added to EWS but not to the Unified Messaging web service.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="954f5-112">En esta sección</span><span class="sxs-lookup"><span data-stu-id="954f5-112">In this section</span></span>
<span data-ttu-id="954f5-113"><a name="bk_InThisSection"> </a></span><span class="sxs-lookup"><span data-stu-id="954f5-113"><a name="bk_InThisSection"> </a></span></span>

- [<span data-ttu-id="954f5-114">Operación Disconnect (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="954f5-114">Disconnect operation (UM web service)</span></span>](disconnect-operation-um-web-service.md)    
- [<span data-ttu-id="954f5-115">Operación GetCallInfo (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="954f5-115">GetCallInfo operation (UM web service)</span></span>](getcallinfo-operation-um-web-service.md)   
- [<span data-ttu-id="954f5-116">Operación GetUMProperties (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="954f5-116">GetUMProperties operation (UM web service)</span></span>](getumproperties-operation-um-web-service.md)   
- [<span data-ttu-id="954f5-117">Operación IsUMEnabled (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="954f5-117">IsUMEnabled operation (UM web service)</span></span>](isumenabled-operation-um-web-service.md)   
- [<span data-ttu-id="954f5-118">Operación reproducir (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="954f5-118">PlayOnPhone operation (UM web service)</span></span>](playonphone-operation-um-web-service.md)   
- [<span data-ttu-id="954f5-119">Operación PlayOnPhoneGreeting (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="954f5-119">PlayOnPhoneGreeting operation (UM web service)</span></span>](playonphonegreeting-operation-um-web-service.md)   
- [<span data-ttu-id="954f5-120">Operación ResetPIN (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="954f5-120">ResetPIN operation (UM web service)</span></span>](resetpin-operation-um-web-service.md)   
- [<span data-ttu-id="954f5-121">Operación SetMissedCallNotificationEnabled (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="954f5-121">SetMissedCallNotificationEnabled operation (UM web service)</span></span>](setmissedcallnotificationenabled-operation-um-web-service.md)  
- [<span data-ttu-id="954f5-122">Operación SetOofStatus (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="954f5-122">SetOofStatus operation (UM web service)</span></span>](setoofstatus-operation-um-web-service.md)    
- [<span data-ttu-id="954f5-123">Operación SetPlayOnPhoneDialString (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="954f5-123">SetPlayOnPhoneDialString operation (UM web service)</span></span>](setplayonphonedialstring-operation-um-web-service.md)   
- [<span data-ttu-id="954f5-124">Operación SetTelephoneAccessFolderEmail (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="954f5-124">SetTelephoneAccessFolderEmail operation (UM web service)</span></span>](settelephoneaccessfolderemail-operation-um-web-service.md)
    
## <a name="see-also"></a><span data-ttu-id="954f5-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="954f5-125">See also</span></span>

- [<span data-ttu-id="954f5-126">Referencia del servicio Web de mensajería unificada para Exchange</span><span class="sxs-lookup"><span data-stu-id="954f5-126">Unified Messaging web service reference for Exchange</span></span>](unified-messaging-web-service-reference-for-exchange.md)
- [<span data-ttu-id="954f5-127">Detección automática en Exchange</span><span class="sxs-lookup"><span data-stu-id="954f5-127">Autodiscover for Exchange</span></span>](../exchange-web-services/autodiscover-for-exchange.md)
- [<span data-ttu-id="954f5-128">Empezar a usar los servicios web de Exchange</span><span class="sxs-lookup"><span data-stu-id="954f5-128">Start using web services in Exchange</span></span>](../exchange-web-services/start-using-web-services-in-exchange.md)
    

