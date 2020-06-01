---
title: Nombredominio (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 2b4af2b2-58b5-4f28-9cb3-c07a11377747
description: El elemento DomainName especifica el dominio del usuario.
ms.openlocfilehash: ff38d6a876e396317dedece0a81a9f9f0db0f587
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458428"
---
# <a name="domainname-pox"></a><span data-ttu-id="b680f-103">Nombredominio (POX)</span><span class="sxs-lookup"><span data-stu-id="b680f-103">DomainName (POX)</span></span>

<span data-ttu-id="b680f-104">El elemento **domainname** especifica el dominio del usuario.</span><span class="sxs-lookup"><span data-stu-id="b680f-104">The **DomainName** element specifies the user's domain.</span></span> 
  
- [<span data-ttu-id="b680f-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="b680f-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)  
- [<span data-ttu-id="b680f-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="b680f-106">Response (POX)</span></span>](response-pox.md)  
- [<span data-ttu-id="b680f-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="b680f-107">Account (POX)</span></span>](account-pox.md) 
- [<span data-ttu-id="b680f-108">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="b680f-108">Protocol (POX)</span></span>](protocol-pox.md) 
- [<span data-ttu-id="b680f-109">Nombredominio (POX)</span><span class="sxs-lookup"><span data-stu-id="b680f-109">DomainName (POX)</span></span>](domainname-pox.md)
  
```xml
<DomainName/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="b680f-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b680f-110">Attributes and elements</span></span>

<span data-ttu-id="b680f-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b680f-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b680f-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="b680f-112">Attributes</span></span>

<span data-ttu-id="b680f-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="b680f-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b680f-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b680f-114">Child elements</span></span>

<span data-ttu-id="b680f-115">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="b680f-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b680f-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b680f-116">Parent elements</span></span>

|<span data-ttu-id="b680f-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b680f-117">**Element**</span></span>|<span data-ttu-id="b680f-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b680f-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b680f-119">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="b680f-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="b680f-120">Contiene las especificaciones para conectar un cliente al equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="b680f-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b680f-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="b680f-121">Text value</span></span>

<span data-ttu-id="b680f-122">El valor de texto especifica el dominio del usuario.</span><span class="sxs-lookup"><span data-stu-id="b680f-122">The text value specifies the user's domain.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b680f-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b680f-123">Remarks</span></span>

<span data-ttu-id="b680f-124">Si no se especifica ningún valor, la autenticación predeterminada es usar la dirección de correo electrónico como un formato de nombre principal de usuario (UPN).</span><span class="sxs-lookup"><span data-stu-id="b680f-124">If no value is specified, the default authentication is to use the e-mail address as a user principal name (UPN) format.</span></span> <span data-ttu-id="b680f-125">Por ejemplo: \<Username\> @ \<Domain\> .</span><span class="sxs-lookup"><span data-stu-id="b680f-125">For example: \<Username\>@\<Domain\>.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b680f-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="b680f-126">See also</span></span>

- [<span data-ttu-id="b680f-127">Elementos XML de detección automática de POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="b680f-127">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

