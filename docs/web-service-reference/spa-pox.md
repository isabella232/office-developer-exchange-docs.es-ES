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
description: El elemento SPA indica si se requiere la autenticación de contraseña segura (SPA).
ms.openlocfilehash: 1fb0f3bb40e64be89eae7dfc208d51387f532191
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837533"
---
# <a name="spa-pox"></a><span data-ttu-id="0ce6b-103">SPA (POX)</span><span class="sxs-lookup"><span data-stu-id="0ce6b-103">SPA (POX)</span></span>

<span data-ttu-id="0ce6b-104">El elemento **SPA** indica si se requiere la autenticación de contraseña segura (SPA).</span><span class="sxs-lookup"><span data-stu-id="0ce6b-104">The **SPA** element indicates whether Secure Password Authentication (SPA) is required.</span></span> 
  
[<span data-ttu-id="0ce6b-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="0ce6b-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="0ce6b-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="0ce6b-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="0ce6b-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="0ce6b-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="0ce6b-108">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="0ce6b-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="0ce6b-109">SPA (POX)</span><span class="sxs-lookup"><span data-stu-id="0ce6b-109">SPA (POX)</span></span>](spa-pox.md)
  
```xml
<SPA/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="0ce6b-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="0ce6b-110">Attributes and elements</span></span>

<span data-ttu-id="0ce6b-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="0ce6b-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0ce6b-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="0ce6b-112">Attributes</span></span>

<span data-ttu-id="0ce6b-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0ce6b-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0ce6b-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0ce6b-114">Child elements</span></span>

<span data-ttu-id="0ce6b-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0ce6b-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0ce6b-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0ce6b-116">Parent elements</span></span>

|<span data-ttu-id="0ce6b-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="0ce6b-117">**Element**</span></span>|<span data-ttu-id="0ce6b-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0ce6b-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0ce6b-119">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="0ce6b-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="0ce6b-120">Contiene las especificaciones para conectar a un cliente en el equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="0ce6b-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0ce6b-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="0ce6b-121">Text value</span></span>

<span data-ttu-id="0ce6b-122">El valor de texto indica si se requiere la SPA.</span><span class="sxs-lookup"><span data-stu-id="0ce6b-122">The text value indicates whether SPA is required.</span></span> <span data-ttu-id="0ce6b-123">Si el valor de texto está **activado**, se requiere SPA.</span><span class="sxs-lookup"><span data-stu-id="0ce6b-123">If the text value is **on**, SPA is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0ce6b-124">Notas</span><span class="sxs-lookup"><span data-stu-id="0ce6b-124">Remarks</span></span>

<span data-ttu-id="0ce6b-125">Si este elemento no está presente, el valor predeterminado se establece en **on**.</span><span class="sxs-lookup"><span data-stu-id="0ce6b-125">If this element is not present, the default value is set to **on**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0ce6b-126">Ver también</span><span class="sxs-lookup"><span data-stu-id="0ce6b-126">See also</span></span>



[<span data-ttu-id="0ce6b-127">Elementos de Autodiscover XML POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="0ce6b-127">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

