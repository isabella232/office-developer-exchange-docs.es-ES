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
description: El elemento TTL especifica el tiempo de vida, en horas, durante el cual la configuración sigue siendo válida.
ms.openlocfilehash: 9a17cbe4e669d1afe9f3ef4a24f2a9a2889a7d52
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467385"
---
# <a name="ttl-pox"></a><span data-ttu-id="e88ae-103">TTL (POX)</span><span class="sxs-lookup"><span data-stu-id="e88ae-103">TTL (POX)</span></span>

<span data-ttu-id="e88ae-104">El elemento **TTL** especifica el tiempo de vida, en horas, durante el cual la configuración sigue siendo válida.</span><span class="sxs-lookup"><span data-stu-id="e88ae-104">The **TTL** element specifies the Time to Live, in hours, during which the settings remain valid.</span></span> 
  
[<span data-ttu-id="e88ae-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="e88ae-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="e88ae-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="e88ae-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="e88ae-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="e88ae-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="e88ae-108">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="e88ae-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="e88ae-109">TTL (POX)</span><span class="sxs-lookup"><span data-stu-id="e88ae-109">TTL (POX)</span></span>](ttl-pox.md)
  
```xml
<TTL/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="e88ae-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e88ae-110">Attributes and elements</span></span>

<span data-ttu-id="e88ae-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e88ae-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e88ae-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="e88ae-112">Attributes</span></span>

<span data-ttu-id="e88ae-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="e88ae-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e88ae-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e88ae-114">Child elements</span></span>

<span data-ttu-id="e88ae-115">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="e88ae-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e88ae-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e88ae-116">Parent elements</span></span>

|<span data-ttu-id="e88ae-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e88ae-117">**Element**</span></span>|<span data-ttu-id="e88ae-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e88ae-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e88ae-119">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="e88ae-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="e88ae-120">Contiene las especificaciones para conectar un cliente al equipo con Exchange Server 2007 en el que está instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="e88ae-120">Contains the specifications for connecting a client to the Exchange Server 2007 computer on which the Client Access server role is installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e88ae-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="e88ae-121">Text value</span></span>

<span data-ttu-id="e88ae-122">El valor de texto representa el período de vida, en horas, durante el cual la configuración sigue siendo válida.</span><span class="sxs-lookup"><span data-stu-id="e88ae-122">The text value represents the Time to Live, in hours, during which the settings remain valid.</span></span> <span data-ttu-id="e88ae-123">Un valor de cero indica que no se requiere rediscovery.</span><span class="sxs-lookup"><span data-stu-id="e88ae-123">A value of zero indicates that rediscovery is not required.</span></span> <span data-ttu-id="e88ae-124">Si no se especifica ningún valor, el valor predeterminado de este elemento es 1 hora.</span><span class="sxs-lookup"><span data-stu-id="e88ae-124">If no value is specified, the default value for this element is 1 hour.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e88ae-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e88ae-125">Remarks</span></span>

<span data-ttu-id="e88ae-126">Una vez transcurrida la hora que se representa en el elemento **TTL** , la configuración debe volver a detectarse mediante una solicitud de detección automática.</span><span class="sxs-lookup"><span data-stu-id="e88ae-126">After the time that is represented by the **TTL** element has elapsed, the settings should be rediscovered by using an Autodiscover request.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e88ae-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="e88ae-127">See also</span></span>



[<span data-ttu-id="e88ae-128">Elementos XML de detección automática de POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="e88ae-128">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

