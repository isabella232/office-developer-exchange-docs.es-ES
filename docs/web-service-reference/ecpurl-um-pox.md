---
title: EcpUrl-mensajería unificada (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 455c77c6-c03f-49a7-a8ca-aa0023b6e73b
description: El elemento EcpUrl um especifica una dirección URL parcial que se puede combinar con el valor del elemento EcpUrl (POX) para generar una dirección URL que se puede usar para tener acceso a la configuración de correo de voz para un usuario habilitado para correo.
ms.openlocfilehash: 5f9be67f02703bbdfeb114eda13c5ce59f83290d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764305"
---
# <a name="ecpurl-um-pox"></a><span data-ttu-id="a14c9-103">EcpUrl-mensajería unificada (POX)</span><span class="sxs-lookup"><span data-stu-id="a14c9-103">EcpUrl-um (POX)</span></span>

<span data-ttu-id="a14c9-104">El elemento **EcpUrl um** especifica una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para tener acceso a la configuración de correo de voz para un usuario habilitado para correo.</span><span class="sxs-lookup"><span data-stu-id="a14c9-104">The **EcpUrl-um** element specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access voice mail settings for a mail-enabled user.</span></span> 
  
[<span data-ttu-id="a14c9-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="a14c9-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="a14c9-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="a14c9-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="a14c9-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="a14c9-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="a14c9-108">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="a14c9-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="a14c9-109">EcpUrl-mensajería unificada (POX)</span><span class="sxs-lookup"><span data-stu-id="a14c9-109">EcpUrl-um (POX)</span></span>](ecpurl-um-pox.md)
  
```XML
<EcpUrl-um/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="a14c9-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a14c9-110">Attributes and elements</span></span>

<span data-ttu-id="a14c9-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a14c9-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a14c9-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="a14c9-112">Attributes</span></span>

<span data-ttu-id="a14c9-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a14c9-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a14c9-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a14c9-114">Child elements</span></span>

<span data-ttu-id="a14c9-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a14c9-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a14c9-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a14c9-116">Parent elements</span></span>

|<span data-ttu-id="a14c9-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="a14c9-117">**Element**</span></span>|<span data-ttu-id="a14c9-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a14c9-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a14c9-119">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="a14c9-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="a14c9-120">Contiene las especificaciones para conectar a un cliente en el equipo que ejecuta Microsoft Exchange Server que tiene instalada la función del servidor acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="a14c9-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a14c9-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="a14c9-121">Text value</span></span>

<span data-ttu-id="a14c9-122">El valor de texto representa una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para tener acceso a la configuración de correo de voz para el usuario.</span><span class="sxs-lookup"><span data-stu-id="a14c9-122">The text value represents a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access voice mail settings for the user.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a14c9-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a14c9-123">Remarks</span></span>

<span data-ttu-id="a14c9-124">El elemento **EcpUrl-mensajería unificada** es un elemento secundario opcional del elemento **Protocol** .</span><span class="sxs-lookup"><span data-stu-id="a14c9-124">The **EcpUrl-um** element is an optional child element of the **Protocol** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a14c9-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="a14c9-125">See also</span></span>



[<span data-ttu-id="a14c9-126">Elementos de Autodiscover XML POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="a14c9-126">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

