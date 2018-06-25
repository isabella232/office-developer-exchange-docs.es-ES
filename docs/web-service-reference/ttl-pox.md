---
title: TTL (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 178eefa1-995c-4bea-930b-e51293961191
description: El elemento TTL especifica el período de vida, en horas, durante el cual la configuración permanece válida.
ms.openlocfilehash: 5fecf3103553a82ed2aeeecfc1e4e1b9fe38583c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840733"
---
# <a name="ttl-pox"></a><span data-ttu-id="a7b6b-103">TTL (POX)</span><span class="sxs-lookup"><span data-stu-id="a7b6b-103">TTL (POX)</span></span>

<span data-ttu-id="a7b6b-104">El elemento **TTL** especifica el período de vida, en horas, durante el cual la configuración permanece válida.</span><span class="sxs-lookup"><span data-stu-id="a7b6b-104">The **TTL** element specifies the Time to Live, in hours, during which the settings remain valid.</span></span> 
  
[<span data-ttu-id="a7b6b-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="a7b6b-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="a7b6b-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="a7b6b-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="a7b6b-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="a7b6b-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="a7b6b-108">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="a7b6b-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="a7b6b-109">TTL (POX)</span><span class="sxs-lookup"><span data-stu-id="a7b6b-109">TTL (POX)</span></span>](ttl-pox.md)
  
```xml
<TTL/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="a7b6b-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a7b6b-110">Attributes and elements</span></span>

<span data-ttu-id="a7b6b-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a7b6b-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a7b6b-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="a7b6b-112">Attributes</span></span>

<span data-ttu-id="a7b6b-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a7b6b-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a7b6b-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a7b6b-114">Child elements</span></span>

<span data-ttu-id="a7b6b-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a7b6b-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a7b6b-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a7b6b-116">Parent elements</span></span>

|<span data-ttu-id="a7b6b-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="a7b6b-117">**Element**</span></span>|<span data-ttu-id="a7b6b-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a7b6b-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a7b6b-119">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="a7b6b-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="a7b6b-120">Contiene las especificaciones para conectar a un cliente con el equipo de Exchange Server 2007 en la que está instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="a7b6b-120">Contains the specifications for connecting a client to the Exchange Server 2007 computer on which the Client Access server role is installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a7b6b-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="a7b6b-121">Text value</span></span>

<span data-ttu-id="a7b6b-122">El valor de texto representa el período de vida, en horas, durante el cual la configuración permanece válida.</span><span class="sxs-lookup"><span data-stu-id="a7b6b-122">The text value represents the Time to Live, in hours, during which the settings remain valid.</span></span> <span data-ttu-id="a7b6b-123">Un valor de cero indica que redescubrimiento no es necesario.</span><span class="sxs-lookup"><span data-stu-id="a7b6b-123">A value of zero indicates that rediscovery is not required.</span></span> <span data-ttu-id="a7b6b-124">Si no se especifica ningún valor, el valor predeterminado para este elemento es 1 hora.</span><span class="sxs-lookup"><span data-stu-id="a7b6b-124">If no value is specified, the default value for this element is 1 hour.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a7b6b-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a7b6b-125">Remarks</span></span>

<span data-ttu-id="a7b6b-126">Una vez transcurrido el tiempo que está representado por el elemento de **período de Vida** , la configuración se debe redescubrir mediante el uso de una solicitud de detección automática.</span><span class="sxs-lookup"><span data-stu-id="a7b6b-126">After the time that is represented by the **TTL** element has elapsed, the settings should be rediscovered by using an Autodiscover request.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a7b6b-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="a7b6b-127">See also</span></span>



[<span data-ttu-id="a7b6b-128">Elementos de Autodiscover XML POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="a7b6b-128">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

