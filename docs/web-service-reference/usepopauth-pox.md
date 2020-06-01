---
title: UsePOPAuth (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 28f552d8-6bb8-49b4-a45c-b2053670f1cc
description: El elemento UsePOPAuth indica si la información de autenticación que se proporciona para un tipo de cuenta POP3 también se usa para el Protocolo simple de transferencia de correo (SMTP).
ms.openlocfilehash: 8d5bfffaab31c382ad43915e18b8a7a2b2737c21
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466510"
---
# <a name="usepopauth-pox"></a><span data-ttu-id="746d0-103">UsePOPAuth (POX)</span><span class="sxs-lookup"><span data-stu-id="746d0-103">UsePOPAuth (POX)</span></span>

<span data-ttu-id="746d0-104">El elemento **UsePOPAuth** indica si la información de autenticación que se proporciona para un tipo de cuenta POP3 también se usa para el Protocolo simple de transferencia de correo (SMTP).</span><span class="sxs-lookup"><span data-stu-id="746d0-104">The **UsePOPAuth** element indicates whether the authentication information that is provided for a POP3 type of account is also used for Simple Mail Transfer Protocol (SMTP).</span></span> 
  
[<span data-ttu-id="746d0-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="746d0-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="746d0-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="746d0-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="746d0-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="746d0-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="746d0-108">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="746d0-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="746d0-109">UsePOPAuth (POX)</span><span class="sxs-lookup"><span data-stu-id="746d0-109">UsePOPAuth (POX)</span></span>](usepopauth-pox.md)
  
```xml
<UsePOPAuth>on or off</UsePOPAuth>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="746d0-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="746d0-110">Attributes and elements</span></span>

<span data-ttu-id="746d0-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="746d0-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="746d0-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="746d0-112">Attributes</span></span>

<span data-ttu-id="746d0-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="746d0-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="746d0-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="746d0-114">Child elements</span></span>

<span data-ttu-id="746d0-115">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="746d0-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="746d0-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="746d0-116">Parent elements</span></span>

|<span data-ttu-id="746d0-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="746d0-117">**Element**</span></span>|<span data-ttu-id="746d0-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="746d0-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="746d0-119">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="746d0-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="746d0-120">Contiene las especificaciones para conectar un cliente al equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="746d0-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="746d0-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="746d0-121">Text value</span></span>

<span data-ttu-id="746d0-122">El valor de texto indica si la información de autenticación que se proporciona para un tipo de cuenta POP3 también se usa para SMTP.</span><span class="sxs-lookup"><span data-stu-id="746d0-122">The text value indicates whether the authentication information that is provided for a POP3 type of account is also used for SMTP.</span></span> <span data-ttu-id="746d0-123">Los valores posibles son **activado** y **desactivado**.</span><span class="sxs-lookup"><span data-stu-id="746d0-123">The possible values are **on** and **off**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="746d0-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="746d0-124">Remarks</span></span>

<span data-ttu-id="746d0-125">El elemento **UsePOPAuth** solo se usa cuando el [tipo (POX)](type-pox.md) es SMTP.</span><span class="sxs-lookup"><span data-stu-id="746d0-125">The **UsePOPAuth** element is only used when [Type (POX)](type-pox.md) is SMTP.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="746d0-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="746d0-126">See also</span></span>



[<span data-ttu-id="746d0-127">Elementos XML de detección automática de POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="746d0-127">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

