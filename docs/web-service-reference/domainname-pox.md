---
title: DomainName (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 2b4af2b2-58b5-4f28-9cb3-c07a11377747
description: El elemento DomainName especifica el dominio del usuario.
ms.openlocfilehash: c38d2e470bd174ab6dd7e5e1dd3eee23daea5e69
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764266"
---
# <a name="domainname-pox"></a><span data-ttu-id="f1883-103">DomainName (POX)</span><span class="sxs-lookup"><span data-stu-id="f1883-103">DomainName (POX)</span></span>

<span data-ttu-id="f1883-104">El elemento **DomainName** especifica el dominio del usuario.</span><span class="sxs-lookup"><span data-stu-id="f1883-104">The **DomainName** element specifies the user's domain.</span></span> 
  
- [<span data-ttu-id="f1883-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="f1883-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)  
- [<span data-ttu-id="f1883-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="f1883-106">Response (POX)</span></span>](response-pox.md)  
- [<span data-ttu-id="f1883-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="f1883-107">Account (POX)</span></span>](account-pox.md) 
- [<span data-ttu-id="f1883-108">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="f1883-108">Protocol (POX)</span></span>](protocol-pox.md) 
- [<span data-ttu-id="f1883-109">DomainName (POX)</span><span class="sxs-lookup"><span data-stu-id="f1883-109">DomainName (POX)</span></span>](domainname-pox.md)
  
```xml
<DomainName/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="f1883-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f1883-110">Attributes and elements</span></span>

<span data-ttu-id="f1883-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f1883-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f1883-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="f1883-112">Attributes</span></span>

<span data-ttu-id="f1883-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f1883-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f1883-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f1883-114">Child elements</span></span>

<span data-ttu-id="f1883-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f1883-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f1883-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f1883-116">Parent elements</span></span>

|<span data-ttu-id="f1883-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="f1883-117">**Element**</span></span>|<span data-ttu-id="f1883-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f1883-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f1883-119">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="f1883-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="f1883-120">Contiene las especificaciones para conectar a un cliente en el equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="f1883-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f1883-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="f1883-121">Text value</span></span>

<span data-ttu-id="f1883-122">El valor de texto especifica el dominio del usuario.</span><span class="sxs-lookup"><span data-stu-id="f1883-122">The text value specifies the user's domain.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f1883-123">Notas</span><span class="sxs-lookup"><span data-stu-id="f1883-123">Remarks</span></span>

<span data-ttu-id="f1883-124">Si no se especifica ningún valor, la autenticación predeterminada es utilizar la dirección de correo electrónico como un formato de nombre principal (UPN) del usuario.</span><span class="sxs-lookup"><span data-stu-id="f1883-124">If no value is specified, the default authentication is to use the e-mail address as a user principal name (UPN) format.</span></span> <span data-ttu-id="f1883-125">Por ejemplo: \<nombre de usuario\>@\<dominio\>.</span><span class="sxs-lookup"><span data-stu-id="f1883-125">For example: \<Username\>@\<Domain\>.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f1883-126">Ver también</span><span class="sxs-lookup"><span data-stu-id="f1883-126">See also</span></span>

- [<span data-ttu-id="f1883-127">Elementos de Autodiscover XML POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="f1883-127">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

