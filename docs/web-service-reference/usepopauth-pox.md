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
description: El elemento UsePOPAuth indica si la información de autenticación que se proporciona para un tipo de POP3 de cuenta también se usa para el protocolo Simple de transferencia de correo (SMTP).
ms.openlocfilehash: be03568d697b1f5461d49dba388a1d3f1008a67e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840892"
---
# <a name="usepopauth-pox"></a><span data-ttu-id="a1bc3-103">UsePOPAuth (POX)</span><span class="sxs-lookup"><span data-stu-id="a1bc3-103">UsePOPAuth (POX)</span></span>

<span data-ttu-id="a1bc3-104">El elemento **UsePOPAuth** indica si la información de autenticación que se proporciona para un tipo de POP3 de cuenta también se usa para el protocolo Simple de transferencia de correo (SMTP).</span><span class="sxs-lookup"><span data-stu-id="a1bc3-104">The **UsePOPAuth** element indicates whether the authentication information that is provided for a POP3 type of account is also used for Simple Mail Transfer Protocol (SMTP).</span></span> 
  
[<span data-ttu-id="a1bc3-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="a1bc3-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="a1bc3-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="a1bc3-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="a1bc3-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="a1bc3-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="a1bc3-108">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="a1bc3-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="a1bc3-109">UsePOPAuth (POX)</span><span class="sxs-lookup"><span data-stu-id="a1bc3-109">UsePOPAuth (POX)</span></span>](usepopauth-pox.md)
  
```xml
<UsePOPAuth>on or off</UsePOPAuth>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="a1bc3-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a1bc3-110">Attributes and elements</span></span>

<span data-ttu-id="a1bc3-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a1bc3-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a1bc3-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="a1bc3-112">Attributes</span></span>

<span data-ttu-id="a1bc3-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a1bc3-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a1bc3-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a1bc3-114">Child elements</span></span>

<span data-ttu-id="a1bc3-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a1bc3-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a1bc3-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a1bc3-116">Parent elements</span></span>

|<span data-ttu-id="a1bc3-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="a1bc3-117">**Element**</span></span>|<span data-ttu-id="a1bc3-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a1bc3-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a1bc3-119">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="a1bc3-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="a1bc3-120">Contiene las especificaciones para conectar a un cliente en el equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="a1bc3-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a1bc3-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="a1bc3-121">Text value</span></span>

<span data-ttu-id="a1bc3-122">El valor de texto indica si la información de autenticación que se proporciona para un tipo de POP3 de cuenta también se utiliza para SMTP.</span><span class="sxs-lookup"><span data-stu-id="a1bc3-122">The text value indicates whether the authentication information that is provided for a POP3 type of account is also used for SMTP.</span></span> <span data-ttu-id="a1bc3-123">Los valores posibles son **encendido** y **apagado**.</span><span class="sxs-lookup"><span data-stu-id="a1bc3-123">The possible values are **on** and **off**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a1bc3-124">Notas</span><span class="sxs-lookup"><span data-stu-id="a1bc3-124">Remarks</span></span>

<span data-ttu-id="a1bc3-125">El elemento **UsePOPAuth** solo se usa al [Tipo (POX)](type-pox.md) es SMTP.</span><span class="sxs-lookup"><span data-stu-id="a1bc3-125">The **UsePOPAuth** element is only used when [Type (POX)](type-pox.md) is SMTP.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a1bc3-126">Ver también</span><span class="sxs-lookup"><span data-stu-id="a1bc3-126">See also</span></span>



[<span data-ttu-id="a1bc3-127">Elementos de Autodiscover XML POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="a1bc3-127">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

