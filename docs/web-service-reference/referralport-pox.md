---
title: ReferralPort (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: cd693f1e-fed4-4eb9-8297-178906f47050
description: El elemento ReferralPort especifica el puerto que se usa para obtener una referencia a un directorio.
ms.openlocfilehash: 6b3968d7b2f252439d2dfbc647bd8337668cf818
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456797"
---
# <a name="referralport-pox"></a><span data-ttu-id="5f7a7-103">ReferralPort (POX)</span><span class="sxs-lookup"><span data-stu-id="5f7a7-103">ReferralPort (POX)</span></span>

<span data-ttu-id="5f7a7-104">El elemento **ReferralPort** especifica el puerto que se usa para obtener una referencia a un directorio.</span><span class="sxs-lookup"><span data-stu-id="5f7a7-104">The **ReferralPort** element specifies the port that is used to get a referral to a directory.</span></span> 
  
[<span data-ttu-id="5f7a7-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="5f7a7-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="5f7a7-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="5f7a7-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="5f7a7-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="5f7a7-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="5f7a7-108">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="5f7a7-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="5f7a7-109">ReferralPort (POX)</span><span class="sxs-lookup"><span data-stu-id="5f7a7-109">ReferralPort (POX)</span></span>](referralport-pox.md)
  
```xml
<ReferralPort/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="5f7a7-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="5f7a7-110">Attributes and elements</span></span>

<span data-ttu-id="5f7a7-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="5f7a7-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5f7a7-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="5f7a7-112">Attributes</span></span>

<span data-ttu-id="5f7a7-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="5f7a7-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5f7a7-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5f7a7-114">Child elements</span></span>

<span data-ttu-id="5f7a7-115">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="5f7a7-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5f7a7-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5f7a7-116">Parent elements</span></span>

|<span data-ttu-id="5f7a7-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="5f7a7-117">**Element**</span></span>|<span data-ttu-id="5f7a7-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5f7a7-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5f7a7-119">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="5f7a7-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="5f7a7-120">Contiene las especificaciones para conectar un cliente al equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="5f7a7-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5f7a7-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="5f7a7-121">Text value</span></span>

<span data-ttu-id="5f7a7-122">El valor de texto representa el puerto que se usa para obtener acceso al servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5f7a7-122">The text value represents the port that is used to access the Exchange server.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5f7a7-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5f7a7-123">Remarks</span></span>

<span data-ttu-id="5f7a7-124">El elemento **ReferralPort** solo se usa cuando el elemento [Type (POX)](type-pox.md) es igual a EXCH o a expr.</span><span class="sxs-lookup"><span data-stu-id="5f7a7-124">The **ReferralPort** element is only used when the [Type (POX)](type-pox.md) element equals EXCH or EXPR.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5f7a7-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="5f7a7-125">See also</span></span>



[<span data-ttu-id="5f7a7-126">Elementos XML de detección automática de POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="5f7a7-126">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

