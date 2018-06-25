---
title: EcpUrl-devuelve (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5f090fd2-b0c4-4ca0-a959-1433d73a2069
description: El elemento devuelve EcpUrl especifica una dirección URL parcial que se puede combinar con el valor del elemento EcpUrl (POX) para generar una dirección URL que se puede usar para tener acceso a la configuración de la etiqueta de retención para un usuario habilitado para correo.
ms.openlocfilehash: 366a7a79c0f3c19b2cfef21c01826e62b0e95793
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764307"
---
# <a name="ecpurl-ret-pox"></a><span data-ttu-id="bc2d4-103">EcpUrl-devuelve (POX)</span><span class="sxs-lookup"><span data-stu-id="bc2d4-103">EcpUrl-ret (POX)</span></span>

<span data-ttu-id="bc2d4-104">El elemento **devuelve EcpUrl** especifica una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para tener acceso a la configuración de la etiqueta de retención para un usuario habilitado para correo.</span><span class="sxs-lookup"><span data-stu-id="bc2d4-104">The **EcpUrl-ret** element specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access retention tag settings for a mail-enabled user.</span></span> 
  
[<span data-ttu-id="bc2d4-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="bc2d4-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="bc2d4-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="bc2d4-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="bc2d4-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="bc2d4-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="bc2d4-108">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="bc2d4-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="bc2d4-109">EcpUrl-devuelve (POX)</span><span class="sxs-lookup"><span data-stu-id="bc2d4-109">EcpUrl-ret (POX)</span></span>](ecpurl-ret-pox.md)
  
```XML
<EcpUrl-ret/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="bc2d4-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="bc2d4-110">Attributes and elements</span></span>

<span data-ttu-id="bc2d4-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="bc2d4-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bc2d4-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="bc2d4-112">Attributes</span></span>

<span data-ttu-id="bc2d4-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="bc2d4-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bc2d4-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="bc2d4-114">Child elements</span></span>

<span data-ttu-id="bc2d4-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="bc2d4-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="bc2d4-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="bc2d4-116">Parent elements</span></span>

|<span data-ttu-id="bc2d4-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="bc2d4-117">**Element**</span></span>|<span data-ttu-id="bc2d4-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bc2d4-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bc2d4-119">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="bc2d4-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="bc2d4-120">Contiene las especificaciones para conectar a un cliente en el equipo que ejecuta Microsoft Exchange Server que tiene instalada la función del servidor acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="bc2d4-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="bc2d4-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="bc2d4-121">Text value</span></span>

<span data-ttu-id="bc2d4-122">El valor de texto representa una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para tener acceso a la configuración de la etiqueta de retención para el usuario.</span><span class="sxs-lookup"><span data-stu-id="bc2d4-122">The text value represents a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access retention tag settings for the user.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="bc2d4-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bc2d4-123">Remarks</span></span>

<span data-ttu-id="bc2d4-124">El elemento **devuelve EcpUrl** es un elemento secundario opcional del elemento **Protocol** .</span><span class="sxs-lookup"><span data-stu-id="bc2d4-124">The **EcpUrl-ret** element is an optional child element of the **Protocol** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bc2d4-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="bc2d4-125">See also</span></span>



[<span data-ttu-id="bc2d4-126">Elementos de Autodiscover XML POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="bc2d4-126">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

