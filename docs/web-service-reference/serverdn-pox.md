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
description: El elemento ServerDN especifica el nombre distintivo del equipo que ejecuta Microsoft Exchange Server 2007.
ms.openlocfilehash: 16c6e7368e221b7e54c8d7d63532bb29464a7e54
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461999"
---
# <a name="serverdn-pox"></a><span data-ttu-id="8d924-103">ServerDN (POX)</span><span class="sxs-lookup"><span data-stu-id="8d924-103">ServerDN (POX)</span></span>

<span data-ttu-id="8d924-104">El elemento **ServerDN** especifica el nombre distintivo del equipo que ejecuta Microsoft Exchange Server 2007.</span><span class="sxs-lookup"><span data-stu-id="8d924-104">The **ServerDN** element specifies the distinguished name of the computer that is running Microsoft Exchange Server 2007.</span></span> 
  
[<span data-ttu-id="8d924-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="8d924-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="8d924-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="8d924-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="8d924-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="8d924-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="8d924-108">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="8d924-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="8d924-109">ServerDN (POX)</span><span class="sxs-lookup"><span data-stu-id="8d924-109">ServerDN (POX)</span></span>](serverdn-pox.md)
  
```xml
<ServerDN/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="8d924-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="8d924-110">Attributes and elements</span></span>

<span data-ttu-id="8d924-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="8d924-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8d924-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="8d924-112">Attributes</span></span>

<span data-ttu-id="8d924-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="8d924-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8d924-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8d924-114">Child elements</span></span>

<span data-ttu-id="8d924-115">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="8d924-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8d924-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="8d924-116">Parent elements</span></span>

|<span data-ttu-id="8d924-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="8d924-117">**Element**</span></span>|<span data-ttu-id="8d924-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8d924-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8d924-119">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="8d924-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="8d924-120">Contiene las especificaciones para conectar un cliente al equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="8d924-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="8d924-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="8d924-121">Text value</span></span>

<span data-ttu-id="8d924-122">El valor de texto representa el nombre distintivo del servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="8d924-122">The text value represents the distinguished name of the Exchange server.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8d924-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8d924-123">Remarks</span></span>

<span data-ttu-id="8d924-124">El valor **ServerDN** solo se usa cuando [Type (POX)](type-pox.md) es igual a EXCH.</span><span class="sxs-lookup"><span data-stu-id="8d924-124">The **ServerDN** value is only used when [Type (POX)](type-pox.md) is equal to EXCH.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8d924-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="8d924-125">See also</span></span>



[<span data-ttu-id="8d924-126">Elementos XML de detección automática de POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="8d924-126">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

