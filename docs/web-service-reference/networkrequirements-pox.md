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
description: El elemento NetworkRequirements contiene los criterios que se usan para determinar si el equipo cliente está en una red que cumple con los requisitos del proveedor de servicios de Internet (ISP) para conectarse al servidor.
ms.openlocfilehash: d588f7eb12a445fba9c997c4b9db0a6842105b4e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462727"
---
# <a name="networkrequirements-pox"></a><span data-ttu-id="70568-103">NetworkRequirements (POX)</span><span class="sxs-lookup"><span data-stu-id="70568-103">NetworkRequirements (POX)</span></span>

<span data-ttu-id="70568-104">El elemento **NetworkRequirements** contiene los criterios que se usan para determinar si el equipo cliente está en una red que cumple con los requisitos del proveedor de servicios de Internet (ISP) para conectarse al servidor.</span><span class="sxs-lookup"><span data-stu-id="70568-104">The **NetworkRequirements** element contains the criteria that are used to determine whether the client computer is on a network that meets the requirements of the Internet service provider (ISP) to connect to the server.</span></span> 
  
[<span data-ttu-id="70568-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="70568-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="70568-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="70568-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="70568-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="70568-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="70568-108">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="70568-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="70568-109">NetworkRequirements (POX)</span><span class="sxs-lookup"><span data-stu-id="70568-109">NetworkRequirements (POX)</span></span>](networkrequirements-pox.md)
  
```xml
<NetworkRequirements>
   <IPv4Start/>
   <IPv4End/>
   <IPv6Start/>
   <IPv6End/>
</NetworkRequirements>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="70568-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="70568-110">Attributes and elements</span></span>

<span data-ttu-id="70568-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="70568-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="70568-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="70568-112">Attributes</span></span>

<span data-ttu-id="70568-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="70568-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="70568-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="70568-114">Child elements</span></span>

|<span data-ttu-id="70568-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="70568-115">**Element**</span></span>|<span data-ttu-id="70568-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="70568-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="70568-117">IPv4Start (POX)</span><span class="sxs-lookup"><span data-stu-id="70568-117">IPv4Start (POX)</span></span>](ipv4start-pox.md) <br/> |<span data-ttu-id="70568-118">Identifica el inicio de un intervalo de direcciones IP de la versión 4 (IPv4) que se usan para identificar un equipo en una red.</span><span class="sxs-lookup"><span data-stu-id="70568-118">Identifies the start of a range of IP version 4 (IPv4) addresses that are used to identify a computer on a network.</span></span>  <br/> |
|[<span data-ttu-id="70568-119">IPv4End (POX)</span><span class="sxs-lookup"><span data-stu-id="70568-119">IPv4End (POX)</span></span>](ipv4end-pox.md) <br/> |<span data-ttu-id="70568-120">Identifica el final de un intervalo de direcciones IP de la versión 4 (IPv4) que se usan para identificar un equipo en la red.</span><span class="sxs-lookup"><span data-stu-id="70568-120">Identifies the end of a range of IP version 4 (IPv4) addresses that are used to identify a computer on the network.</span></span>  <br/> |
|[<span data-ttu-id="70568-121">IPv6Start (POX)</span><span class="sxs-lookup"><span data-stu-id="70568-121">IPv6Start (POX)</span></span>](ipv6start-pox.md) <br/> |<span data-ttu-id="70568-122">Identifica el inicio de un intervalo de direcciones IP versión 6 (IPv6) que se usan para identificar un equipo en una red.</span><span class="sxs-lookup"><span data-stu-id="70568-122">Identifies the start of a range of IP version 6 (IPv6) addresses that are used to identify a computer on a network.</span></span>  <br/> |
|[<span data-ttu-id="70568-123">IPv6End (POX)</span><span class="sxs-lookup"><span data-stu-id="70568-123">IPv6End (POX)</span></span>](ipv6end-pox.md) <br/> |<span data-ttu-id="70568-124">Identifica el final de un intervalo de direcciones IP versión 6 (IPv6) que se usan para identificar un equipo en una red.</span><span class="sxs-lookup"><span data-stu-id="70568-124">Identifies the end of a range of IP version 6 (IPv6) addresses that are used to identify a computer on a network.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="70568-125">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="70568-125">Parent elements</span></span>

|<span data-ttu-id="70568-126">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="70568-126">**Element**</span></span>|<span data-ttu-id="70568-127">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="70568-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="70568-128">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="70568-128">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="70568-129">Contiene las especificaciones para conectar un cliente al equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="70568-129">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="70568-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="70568-130">Remarks</span></span>

<span data-ttu-id="70568-131">Si el cliente de correo electrónico no cumple los requisitos de red, debe probar otros tipos de protocolo.</span><span class="sxs-lookup"><span data-stu-id="70568-131">If the e-mail client does not match the network requirements, it should try other protocol types.</span></span> <span data-ttu-id="70568-132">Los ISP pueden proporcionar un conjunto de servidores con etiquetas de [Protocolo (POX)](protocol-pox.md) que no requieran autenticación pero que necesiten estar en la red del ISP.</span><span class="sxs-lookup"><span data-stu-id="70568-132">ISPs may provide one set of servers with [Protocol (POX)](protocol-pox.md) tags that do not require authentication but are required to be on the ISP network.</span></span> <span data-ttu-id="70568-133">Los ISP pueden enumerar otro conjunto de servidores que requieran autenticación pero que no necesiten estar en una red específica.</span><span class="sxs-lookup"><span data-stu-id="70568-133">ISPs may list another set of servers that require authentication but are not required to be on a specific network.</span></span> 
  
<span data-ttu-id="70568-134">El elemento **NetworkRequirements** es opcional.</span><span class="sxs-lookup"><span data-stu-id="70568-134">The **NetworkRequirements** element is optional.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="70568-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="70568-135">See also</span></span>



[<span data-ttu-id="70568-136">Elementos XML de detección automática de POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="70568-136">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

