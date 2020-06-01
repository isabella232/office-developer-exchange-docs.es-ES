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
description: El elemento DeploymentId identifica de forma exclusiva el bosque de Microsoft Exchange Server 2007.
ms.openlocfilehash: 4986a3404763e88fb3e84d52a5d30d54c810f93a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467924"
---
# <a name="deploymentid-pox"></a><span data-ttu-id="62a14-103">DeploymentId (POX)</span><span class="sxs-lookup"><span data-stu-id="62a14-103">DeploymentId (POX)</span></span>

<span data-ttu-id="62a14-104">El elemento **DeploymentId** identifica de forma exclusiva el bosque de Microsoft Exchange Server 2007.</span><span class="sxs-lookup"><span data-stu-id="62a14-104">The **DeploymentId** element uniquely identifies the Microsoft Exchange Server 2007 forest.</span></span> 
  
- [<span data-ttu-id="62a14-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="62a14-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)  
- [<span data-ttu-id="62a14-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="62a14-106">Response (POX)</span></span>](response-pox.md) 
- [<span data-ttu-id="62a14-107">Usuario (POX)</span><span class="sxs-lookup"><span data-stu-id="62a14-107">User (POX)</span></span>](user-pox.md)  
- [<span data-ttu-id="62a14-108">DeploymentId (POX)</span><span class="sxs-lookup"><span data-stu-id="62a14-108">DeploymentId (POX)</span></span>](deploymentid-pox.md)
  
```xml
<DeploymentId/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="62a14-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="62a14-109">Attributes and elements</span></span>

<span data-ttu-id="62a14-110">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="62a14-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="62a14-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="62a14-111">Attributes</span></span>

<span data-ttu-id="62a14-112">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="62a14-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="62a14-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="62a14-113">Child elements</span></span>

<span data-ttu-id="62a14-114">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="62a14-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="62a14-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="62a14-115">Parent elements</span></span>

|<span data-ttu-id="62a14-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="62a14-116">**Element**</span></span>|<span data-ttu-id="62a14-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="62a14-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="62a14-118">Usuario (POX)</span><span class="sxs-lookup"><span data-stu-id="62a14-118">User (POX)</span></span>](user-pox.md) <br/> |<span data-ttu-id="62a14-119">Proporciona información específica del usuario.</span><span class="sxs-lookup"><span data-stu-id="62a14-119">Provides user-specific information.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="62a14-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="62a14-120">Text value</span></span>

<span data-ttu-id="62a14-121">El valor de texto identifica de forma exclusiva el bosque de Exchange 2007 en formato GUID.</span><span class="sxs-lookup"><span data-stu-id="62a14-121">The text value uniquely identifies the Exchange 2007 forest in GUID format.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="62a14-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="62a14-122">Remarks</span></span>

<span data-ttu-id="62a14-123">Si desinstala y, a continuación, reinstala Exchange 2007 y usa el mismo nombre de servidor, cambia el valor **DeploymentId** .</span><span class="sxs-lookup"><span data-stu-id="62a14-123">If you uninstall and then reinstall Exchange 2007 and you use the same server name, the **DeploymentId** value changes.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="62a14-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="62a14-124">See also</span></span>

- [<span data-ttu-id="62a14-125">Elementos XML de detección automática de POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="62a14-125">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

