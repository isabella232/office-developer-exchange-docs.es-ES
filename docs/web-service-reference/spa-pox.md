---
title: SPA (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: fba018d5-0c65-4e1b-9767-d1ce8b356278
description: El elemento SPA indica si se requiere autenticación de contraseña segura (SPA).
ms.openlocfilehash: cf57b3a6046b1b9b030b7cae81381189eee92c1c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467644"
---
# <a name="spa-pox"></a><span data-ttu-id="7df6d-103">SPA (POX)</span><span class="sxs-lookup"><span data-stu-id="7df6d-103">SPA (POX)</span></span>

<span data-ttu-id="7df6d-104">El elemento **Spa** indica si se requiere autenticación de contraseña segura (Spa).</span><span class="sxs-lookup"><span data-stu-id="7df6d-104">The **SPA** element indicates whether Secure Password Authentication (SPA) is required.</span></span> 
  
[<span data-ttu-id="7df6d-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="7df6d-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="7df6d-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="7df6d-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="7df6d-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="7df6d-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="7df6d-108">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="7df6d-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="7df6d-109">SPA (POX)</span><span class="sxs-lookup"><span data-stu-id="7df6d-109">SPA (POX)</span></span>](spa-pox.md)
  
```xml
<SPA/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="7df6d-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="7df6d-110">Attributes and elements</span></span>

<span data-ttu-id="7df6d-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="7df6d-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7df6d-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="7df6d-112">Attributes</span></span>

<span data-ttu-id="7df6d-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="7df6d-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7df6d-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7df6d-114">Child elements</span></span>

<span data-ttu-id="7df6d-115">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="7df6d-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7df6d-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7df6d-116">Parent elements</span></span>

|<span data-ttu-id="7df6d-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7df6d-117">**Element**</span></span>|<span data-ttu-id="7df6d-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7df6d-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7df6d-119">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="7df6d-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="7df6d-120">Contiene las especificaciones para conectar un cliente al equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="7df6d-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7df6d-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="7df6d-121">Text value</span></span>

<span data-ttu-id="7df6d-122">El valor de texto indica si se requiere SPA.</span><span class="sxs-lookup"><span data-stu-id="7df6d-122">The text value indicates whether SPA is required.</span></span> <span data-ttu-id="7df6d-123">Si el valor de texto está **activado**, se requiere Spa.</span><span class="sxs-lookup"><span data-stu-id="7df6d-123">If the text value is **on**, SPA is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7df6d-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7df6d-124">Remarks</span></span>

<span data-ttu-id="7df6d-125">Si este elemento no está presente, el valor predeterminado se establece en **on**.</span><span class="sxs-lookup"><span data-stu-id="7df6d-125">If this element is not present, the default value is set to **on**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7df6d-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="7df6d-126">See also</span></span>



[<span data-ttu-id="7df6d-127">Elementos XML de detección automática de POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="7df6d-127">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

