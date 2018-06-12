---
title: DeploymentId (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: b879c134-307e-4645-bb53-55d8ba4fad9c
description: El elemento DeploymentId identifica de forma única el bosque de Microsoft Exchange Server 2007.
ms.openlocfilehash: 4f2548709753d8407d02218acecd9233f0ba764f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764127"
---
# <a name="deploymentid-pox"></a><span data-ttu-id="e9ee6-103">DeploymentId (POX)</span><span class="sxs-lookup"><span data-stu-id="e9ee6-103">DeploymentId (POX)</span></span>

<span data-ttu-id="e9ee6-104">El elemento **DeploymentId** identifica de forma única el bosque de Microsoft Exchange Server 2007.</span><span class="sxs-lookup"><span data-stu-id="e9ee6-104">The **DeploymentId** element uniquely identifies the Microsoft Exchange Server 2007 forest.</span></span> 
  
- [<span data-ttu-id="e9ee6-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="e9ee6-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)  
- [<span data-ttu-id="e9ee6-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="e9ee6-106">Response (POX)</span></span>](response-pox.md) 
- [<span data-ttu-id="e9ee6-107">Usuario (POX)</span><span class="sxs-lookup"><span data-stu-id="e9ee6-107">User (POX)</span></span>](user-pox.md)  
- [<span data-ttu-id="e9ee6-108">DeploymentId (POX)</span><span class="sxs-lookup"><span data-stu-id="e9ee6-108">DeploymentId (POX)</span></span>](deploymentid-pox.md)
  
```xml
<DeploymentId/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="e9ee6-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e9ee6-109">Attributes and elements</span></span>

<span data-ttu-id="e9ee6-110">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e9ee6-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e9ee6-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="e9ee6-111">Attributes</span></span>

<span data-ttu-id="e9ee6-112">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e9ee6-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e9ee6-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e9ee6-113">Child elements</span></span>

<span data-ttu-id="e9ee6-114">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e9ee6-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e9ee6-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e9ee6-115">Parent elements</span></span>

|<span data-ttu-id="e9ee6-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="e9ee6-116">**Element**</span></span>|<span data-ttu-id="e9ee6-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e9ee6-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e9ee6-118">Usuario (POX)</span><span class="sxs-lookup"><span data-stu-id="e9ee6-118">User (POX)</span></span>](user-pox.md) <br/> |<span data-ttu-id="e9ee6-119">Proporciona información específica del usuario.</span><span class="sxs-lookup"><span data-stu-id="e9ee6-119">Provides user-specific information.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e9ee6-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="e9ee6-120">Text value</span></span>

<span data-ttu-id="e9ee6-121">El valor de texto identifica de forma única el bosque de Exchange 2007 en formato GUID.</span><span class="sxs-lookup"><span data-stu-id="e9ee6-121">The text value uniquely identifies the Exchange 2007 forest in GUID format.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e9ee6-122">Notas</span><span class="sxs-lookup"><span data-stu-id="e9ee6-122">Remarks</span></span>

<span data-ttu-id="e9ee6-123">Si desinstala y, a continuación, vuelva a instalar Exchange 2007 y usar el mismo nombre de servidor, se cambia el valor de **DeploymentId** .</span><span class="sxs-lookup"><span data-stu-id="e9ee6-123">If you uninstall and then reinstall Exchange 2007 and you use the same server name, the **DeploymentId** value changes.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e9ee6-124">Ver también</span><span class="sxs-lookup"><span data-stu-id="e9ee6-124">See also</span></span>

- [<span data-ttu-id="e9ee6-125">Elementos de Autodiscover XML POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="e9ee6-125">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

