---
title: DomainRequired (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 1f26b691-7331-4c7f-a92b-dfcc66c26963
description: El elemento DomainRequired indica si el dominio es necesario para la autenticación.
ms.openlocfilehash: 97d602c40b247f9a6650cc4440b53bf23c18482e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461327"
---
# <a name="domainrequired-pox"></a><span data-ttu-id="886a7-103">DomainRequired (POX)</span><span class="sxs-lookup"><span data-stu-id="886a7-103">DomainRequired (POX)</span></span>

<span data-ttu-id="886a7-104">El elemento **DomainRequired** indica si el dominio es necesario para la autenticación.</span><span class="sxs-lookup"><span data-stu-id="886a7-104">The **DomainRequired** element indicates whether the domain is required for authentication.</span></span> 
  
- [<span data-ttu-id="886a7-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="886a7-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)  
- [<span data-ttu-id="886a7-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="886a7-106">Response (POX)</span></span>](response-pox.md) 
- [<span data-ttu-id="886a7-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="886a7-107">Account (POX)</span></span>](account-pox.md)  
- [<span data-ttu-id="886a7-108">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="886a7-108">Protocol (POX)</span></span>](protocol-pox.md)  
- [<span data-ttu-id="886a7-109">DomainRequired (POX)</span><span class="sxs-lookup"><span data-stu-id="886a7-109">DomainRequired (POX)</span></span>](domainrequired-pox.md)
  
```xml
<DomainRequired>on or off</DomainRequired>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="886a7-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="886a7-110">Attributes and elements</span></span>

<span data-ttu-id="886a7-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="886a7-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="886a7-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="886a7-112">Attributes</span></span>

<span data-ttu-id="886a7-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="886a7-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="886a7-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="886a7-114">Child elements</span></span>

<span data-ttu-id="886a7-115">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="886a7-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="886a7-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="886a7-116">Parent elements</span></span>

|<span data-ttu-id="886a7-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="886a7-117">**Element**</span></span>|<span data-ttu-id="886a7-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="886a7-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="886a7-119">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="886a7-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="886a7-120">Contiene las especificaciones para conectar un cliente al equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="886a7-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="886a7-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="886a7-121">Text value</span></span>

<span data-ttu-id="886a7-122">El valor de texto indica si el dominio es necesario para la autenticación.</span><span class="sxs-lookup"><span data-stu-id="886a7-122">The text value indicates whether the domain is required for authentication.</span></span> <span data-ttu-id="886a7-123">Los valores posibles son **activado** y **desactivado**.</span><span class="sxs-lookup"><span data-stu-id="886a7-123">The possible values are **on** and **off**.</span></span> <span data-ttu-id="886a7-124">Si el valor es **on**, la siguiente solicitud debe contener el dominio de la cuenta del usuario.</span><span class="sxs-lookup"><span data-stu-id="886a7-124">If the value is **on**, the subsequent request must contain the domain of the user's account.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="886a7-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="886a7-125">Remarks</span></span>

<span data-ttu-id="886a7-126">Si no se especifica el dominio en el elemento [LoginName (POX)](loginname-pox.md) o no se especificó el elemento **LoginName** , el usuario debe especificar el dominio para que la autenticación se realice correctamente.</span><span class="sxs-lookup"><span data-stu-id="886a7-126">If the domain is not specified in the [LoginName (POX)](loginname-pox.md) element, or the **LoginName** element was not specified, the user must enter the domain before authentication will succeed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="886a7-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="886a7-127">See also</span></span>

- [<span data-ttu-id="886a7-128">Elementos XML de detección automática de POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="886a7-128">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

