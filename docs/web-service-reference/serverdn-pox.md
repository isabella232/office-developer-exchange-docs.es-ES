---
title: ServerDN (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 2ef73d13-e8bb-43f6-96c7-3ee157fed739
description: El elemento ServerDN especifica el nombre distintivo (DN) del equipo que ejecuta Microsoft Exchange Server 2007.
ms.openlocfilehash: d2b9ce663d8245a78acd088b0622406c0dfcb4da
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837374"
---
# <a name="serverdn-pox"></a><span data-ttu-id="66933-103">ServerDN (POX)</span><span class="sxs-lookup"><span data-stu-id="66933-103">ServerDN (POX)</span></span>

<span data-ttu-id="66933-104">El elemento **ServerDN** especifica el nombre distintivo (DN) del equipo que ejecuta Microsoft Exchange Server 2007.</span><span class="sxs-lookup"><span data-stu-id="66933-104">The **ServerDN** element specifies the distinguished name of the computer that is running Microsoft Exchange Server 2007.</span></span> 
  
[<span data-ttu-id="66933-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="66933-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="66933-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="66933-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="66933-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="66933-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="66933-108">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="66933-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="66933-109">ServerDN (POX)</span><span class="sxs-lookup"><span data-stu-id="66933-109">ServerDN (POX)</span></span>](serverdn-pox.md)
  
```xml
<ServerDN/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="66933-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="66933-110">Attributes and elements</span></span>

<span data-ttu-id="66933-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="66933-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="66933-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="66933-112">Attributes</span></span>

<span data-ttu-id="66933-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="66933-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="66933-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="66933-114">Child elements</span></span>

<span data-ttu-id="66933-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="66933-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="66933-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="66933-116">Parent elements</span></span>

|<span data-ttu-id="66933-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="66933-117">**Element**</span></span>|<span data-ttu-id="66933-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="66933-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="66933-119">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="66933-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="66933-120">Contiene las especificaciones para conectar a un cliente en el equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="66933-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="66933-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="66933-121">Text value</span></span>

<span data-ttu-id="66933-122">El valor de texto representa el nombre distintivo (DN) del servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="66933-122">The text value represents the distinguished name of the Exchange server.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="66933-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="66933-123">Remarks</span></span>

<span data-ttu-id="66933-124">El valor de **ServerDN** solo se usa al [Tipo (POX)](type-pox.md) es igual a cambio</span><span class="sxs-lookup"><span data-stu-id="66933-124">The **ServerDN** value is only used when [Type (POX)](type-pox.md) is equal to EXCH.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="66933-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="66933-125">See also</span></span>



[<span data-ttu-id="66933-126">Elementos de Autodiscover XML POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="66933-126">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

