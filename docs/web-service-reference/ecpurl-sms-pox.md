---
title: EcpUrl-sms (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5e5e589-ee16-42a8-9cd4-ae3909fc869b
description: El elemento EcpUrl sms especifica una dirección URL parcial que se puede combinar con el valor del elemento EcpUrl (POX) para generar una dirección URL que se puede usar para tener acceso a la configuración del servicio de mensajes cortos (SMS) para un usuario habilitado para correo.
ms.openlocfilehash: 38471db7b7e046e43425b132b1716033c1c96afd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764300"
---
# <a name="ecpurl-sms-pox"></a><span data-ttu-id="ae819-103">EcpUrl-sms (POX)</span><span class="sxs-lookup"><span data-stu-id="ae819-103">EcpUrl-sms (POX)</span></span>

<span data-ttu-id="ae819-104">El elemento **EcpUrl sms** especifica una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para tener acceso a la configuración del servicio de mensajes cortos (SMS) para un usuario habilitado para correo.</span><span class="sxs-lookup"><span data-stu-id="ae819-104">The **EcpUrl-sms** element specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access Short Message Service (SMS) settings for a mail-enabled user.</span></span> 
  
[<span data-ttu-id="ae819-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="ae819-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="ae819-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="ae819-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="ae819-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="ae819-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="ae819-108">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="ae819-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="ae819-109">EcpUrl-sms (POX)</span><span class="sxs-lookup"><span data-stu-id="ae819-109">EcpUrl-sms (POX)</span></span>](ecpurl-sms-pox.md)
  
```XML
<EcpUrl-sms/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="ae819-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ae819-110">Attributes and elements</span></span>

<span data-ttu-id="ae819-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ae819-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ae819-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="ae819-112">Attributes</span></span>

<span data-ttu-id="ae819-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ae819-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ae819-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ae819-114">Child elements</span></span>

<span data-ttu-id="ae819-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ae819-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ae819-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ae819-116">Parent elements</span></span>

|<span data-ttu-id="ae819-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="ae819-117">**Element**</span></span>|<span data-ttu-id="ae819-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ae819-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ae819-119">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="ae819-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="ae819-120">Contiene las especificaciones para conectar a un cliente en el equipo que ejecuta Microsoft Exchange Server que tiene instalada la función del servidor acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="ae819-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ae819-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="ae819-121">Text value</span></span>

<span data-ttu-id="ae819-122">El valor de texto representa una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para tener acceso a la configuración de SMS para el usuario.</span><span class="sxs-lookup"><span data-stu-id="ae819-122">The text value represents a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access SMS settings for the user.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ae819-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ae819-123">Remarks</span></span>

<span data-ttu-id="ae819-124">El elemento **EcpUrl sms** es un elemento secundario opcional del elemento **Protocol** .</span><span class="sxs-lookup"><span data-stu-id="ae819-124">The **EcpUrl-sms** element is an optional child element of the **Protocol** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ae819-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="ae819-125">See also</span></span>



[<span data-ttu-id="ae819-126">Elementos de Autodiscover XML POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="ae819-126">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

