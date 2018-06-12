---
title: NetworkRequirements (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 1555fd2e-05b6-4b94-907b-dae9174049d9
description: El elemento NetworkRequirements contiene los criterios que se usan para determinar si el equipo cliente está en una red que cumpla los requisitos del proveedor de servicios Internet (ISP) para conectarse al servidor.
ms.openlocfilehash: f3abcff04cd4121b8dcc7ceff7658ad389e6d0b0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836529"
---
# <a name="networkrequirements-pox"></a><span data-ttu-id="5c498-103">NetworkRequirements (POX)</span><span class="sxs-lookup"><span data-stu-id="5c498-103">NetworkRequirements (POX)</span></span>

<span data-ttu-id="5c498-104">El elemento **NetworkRequirements** contiene los criterios que se usan para determinar si el equipo cliente está en una red que cumpla los requisitos del proveedor de servicios Internet (ISP) para conectarse al servidor.</span><span class="sxs-lookup"><span data-stu-id="5c498-104">The **NetworkRequirements** element contains the criteria that are used to determine whether the client computer is on a network that meets the requirements of the Internet service provider (ISP) to connect to the server.</span></span> 
  
[<span data-ttu-id="5c498-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="5c498-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="5c498-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="5c498-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="5c498-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="5c498-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="5c498-108">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="5c498-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="5c498-109">NetworkRequirements (POX)</span><span class="sxs-lookup"><span data-stu-id="5c498-109">NetworkRequirements (POX)</span></span>](networkrequirements-pox.md)
  
```xml
<NetworkRequirements>
   <IPv4Start/>
   <IPv4End/>
   <IPv6Start/>
   <IPv6End/>
</NetworkRequirements>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="5c498-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="5c498-110">Attributes and elements</span></span>

<span data-ttu-id="5c498-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="5c498-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5c498-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="5c498-112">Attributes</span></span>

<span data-ttu-id="5c498-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5c498-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5c498-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5c498-114">Child elements</span></span>

|<span data-ttu-id="5c498-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="5c498-115">**Element**</span></span>|<span data-ttu-id="5c498-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5c498-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5c498-117">IPv4Start (POX)</span><span class="sxs-lookup"><span data-stu-id="5c498-117">IPv4Start (POX)</span></span>](ipv4start-pox.md) <br/> |<span data-ttu-id="5c498-118">Identifica el inicio de un intervalo de IP versión 4 (IPv4) las direcciones que se usan para identificar un equipo en una red.</span><span class="sxs-lookup"><span data-stu-id="5c498-118">Identifies the start of a range of IP version 4 (IPv4) addresses that are used to identify a computer on a network.</span></span>  <br/> |
|[<span data-ttu-id="5c498-119">IPv4End (POX)</span><span class="sxs-lookup"><span data-stu-id="5c498-119">IPv4End (POX)</span></span>](ipv4end-pox.md) <br/> |<span data-ttu-id="5c498-120">Identifica el final de un intervalo de IP versión 4 (IPv4) las direcciones que se usan para identificar un equipo en la red.</span><span class="sxs-lookup"><span data-stu-id="5c498-120">Identifies the end of a range of IP version 4 (IPv4) addresses that are used to identify a computer on the network.</span></span>  <br/> |
|[<span data-ttu-id="5c498-121">IPv6Start (POX)</span><span class="sxs-lookup"><span data-stu-id="5c498-121">IPv6Start (POX)</span></span>](ipv6start-pox.md) <br/> |<span data-ttu-id="5c498-122">Identifica el inicio de un intervalo de IP versión 6 (IPv6) las direcciones que se usan para identificar un equipo en una red.</span><span class="sxs-lookup"><span data-stu-id="5c498-122">Identifies the start of a range of IP version 6 (IPv6) addresses that are used to identify a computer on a network.</span></span>  <br/> |
|[<span data-ttu-id="5c498-123">IPv6End (POX)</span><span class="sxs-lookup"><span data-stu-id="5c498-123">IPv6End (POX)</span></span>](ipv6end-pox.md) <br/> |<span data-ttu-id="5c498-124">Identifica el final de un intervalo de IP versión 6 (IPv6) las direcciones que se usan para identificar un equipo en una red.</span><span class="sxs-lookup"><span data-stu-id="5c498-124">Identifies the end of a range of IP version 6 (IPv6) addresses that are used to identify a computer on a network.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5c498-125">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5c498-125">Parent elements</span></span>

|<span data-ttu-id="5c498-126">**Element**</span><span class="sxs-lookup"><span data-stu-id="5c498-126">**Element**</span></span>|<span data-ttu-id="5c498-127">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5c498-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5c498-128">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="5c498-128">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="5c498-129">Contiene las especificaciones para conectar a un cliente en el equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="5c498-129">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5c498-130">Notas</span><span class="sxs-lookup"><span data-stu-id="5c498-130">Remarks</span></span>

<span data-ttu-id="5c498-131">Si el cliente de correo electrónico no coincide con los requisitos de red, deben intentar otros tipos de protocolo.</span><span class="sxs-lookup"><span data-stu-id="5c498-131">If the e-mail client does not match the network requirements, it should try other protocol types.</span></span> <span data-ttu-id="5c498-132">ISP pueden proporcionar un conjunto de servidores con las etiquetas de [Protocolo (POX)](protocol-pox.md) que no requieren la autenticación pero que son necesarios para estar en la red de ISP.</span><span class="sxs-lookup"><span data-stu-id="5c498-132">ISPs may provide one set of servers with [Protocol (POX)](protocol-pox.md) tags that do not require authentication but are required to be on the ISP network.</span></span> <span data-ttu-id="5c498-133">ISP pueden mostrar otro conjunto de servidores que requieren la autenticación pero que no tienen que estar en una red específica.</span><span class="sxs-lookup"><span data-stu-id="5c498-133">ISPs may list another set of servers that require authentication but are not required to be on a specific network.</span></span> 
  
<span data-ttu-id="5c498-134">El elemento **NetworkRequirements** es opcional.</span><span class="sxs-lookup"><span data-stu-id="5c498-134">The **NetworkRequirements** element is optional.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5c498-135">Ver también</span><span class="sxs-lookup"><span data-stu-id="5c498-135">See also</span></span>



[<span data-ttu-id="5c498-136">Elementos de Autodiscover XML POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="5c498-136">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

