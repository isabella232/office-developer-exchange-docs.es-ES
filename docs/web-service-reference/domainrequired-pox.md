---
title: Domain (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 1f26b691-7331-4c7f-a92b-dfcc66c26963
description: El elemento Domain indica si el dominio es necesario para la autenticación.
ms.openlocfilehash: f314b9d27d1b4ee472d249ec49af1a785ff9ac25
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764262"
---
# <a name="domainrequired-pox"></a><span data-ttu-id="2066d-103">Domain (POX)</span><span class="sxs-lookup"><span data-stu-id="2066d-103">DomainRequired (POX)</span></span>

<span data-ttu-id="2066d-104">El elemento **Domain** indica si el dominio es necesario para la autenticación.</span><span class="sxs-lookup"><span data-stu-id="2066d-104">The **DomainRequired** element indicates whether the domain is required for authentication.</span></span> 
  
- [<span data-ttu-id="2066d-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="2066d-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)  
- [<span data-ttu-id="2066d-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="2066d-106">Response (POX)</span></span>](response-pox.md) 
- [<span data-ttu-id="2066d-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="2066d-107">Account (POX)</span></span>](account-pox.md)  
- [<span data-ttu-id="2066d-108">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="2066d-108">Protocol (POX)</span></span>](protocol-pox.md)  
- [<span data-ttu-id="2066d-109">Domain (POX)</span><span class="sxs-lookup"><span data-stu-id="2066d-109">DomainRequired (POX)</span></span>](domainrequired-pox.md)
  
```xml
<DomainRequired>on or off</DomainRequired>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="2066d-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="2066d-110">Attributes and elements</span></span>

<span data-ttu-id="2066d-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="2066d-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2066d-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="2066d-112">Attributes</span></span>

<span data-ttu-id="2066d-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="2066d-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2066d-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2066d-114">Child elements</span></span>

<span data-ttu-id="2066d-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="2066d-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2066d-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="2066d-116">Parent elements</span></span>

|<span data-ttu-id="2066d-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="2066d-117">**Element**</span></span>|<span data-ttu-id="2066d-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2066d-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2066d-119">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="2066d-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="2066d-120">Contiene las especificaciones para conectar a un cliente en el equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="2066d-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2066d-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="2066d-121">Text value</span></span>

<span data-ttu-id="2066d-122">El valor de texto indica si el dominio es necesario para la autenticación.</span><span class="sxs-lookup"><span data-stu-id="2066d-122">The text value indicates whether the domain is required for authentication.</span></span> <span data-ttu-id="2066d-123">Los valores posibles son **encendido** y **apagado**.</span><span class="sxs-lookup"><span data-stu-id="2066d-123">The possible values are **on** and **off**.</span></span> <span data-ttu-id="2066d-124">Si **el valor está habilitado,** la siguiente solicitud debe contener el dominio de la cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="2066d-124">If the value is **on**, the subsequent request must contain the domain of the user's account.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2066d-125">Notas</span><span class="sxs-lookup"><span data-stu-id="2066d-125">Remarks</span></span>

<span data-ttu-id="2066d-126">Si el dominio no está especificado en el elemento [LoginName (POX)](loginname-pox.md) , o no se ha especificado el elemento **LoginName** , el usuario debe escribir el dominio antes de que la autenticación se realizará correctamente.</span><span class="sxs-lookup"><span data-stu-id="2066d-126">If the domain is not specified in the [LoginName (POX)](loginname-pox.md) element, or the **LoginName** element was not specified, the user must enter the domain before authentication will succeed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2066d-127">Ver también</span><span class="sxs-lookup"><span data-stu-id="2066d-127">See also</span></span>

- [<span data-ttu-id="2066d-128">Elementos de Autodiscover XML POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="2066d-128">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

