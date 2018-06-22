---
title: EcpUrl-extinstall (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f81807e6-93de-4e47-afee-1e1ae6a85054
description: El elemento EcpUrl extinstall especifica una dirección URL parcial que se puede combinar con el valor del elemento EcpUrl (POX) para generar una dirección URL que puede usarse para ver o cambiar las aplicaciones de correo instaladas actualmente en el buzón del usuario.
ms.openlocfilehash: f478db53e120f108c64e415e43141761d7914f71
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764289"
---
# <a name="ecpurl-extinstall-pox"></a><span data-ttu-id="36ef8-103">EcpUrl-extinstall (POX)</span><span class="sxs-lookup"><span data-stu-id="36ef8-103">EcpUrl-extinstall (POX)</span></span>

<span data-ttu-id="36ef8-104">El elemento **EcpUrl extinstall** especifica una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que puede usarse para ver o cambiar las aplicaciones de correo instaladas actualmente en el buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="36ef8-104">The **EcpUrl-extinstall** element specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to view or change the mail apps currently installed in the user's mailbox.</span></span> 
  
[<span data-ttu-id="36ef8-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="36ef8-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="36ef8-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="36ef8-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="36ef8-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="36ef8-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="36ef8-108">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="36ef8-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="36ef8-109">EcpUrl-extinstall (POX)</span><span class="sxs-lookup"><span data-stu-id="36ef8-109">EcpUrl-extinstall (POX)</span></span>](ecpurl-extinstall-pox.md)
  
```XML
<EcpUrl-extinstall/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="36ef8-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="36ef8-110">Attributes and elements</span></span>

<span data-ttu-id="36ef8-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="36ef8-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="36ef8-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="36ef8-112">Attributes</span></span>

<span data-ttu-id="36ef8-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="36ef8-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="36ef8-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="36ef8-114">Child elements</span></span>

<span data-ttu-id="36ef8-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="36ef8-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="36ef8-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="36ef8-116">Parent elements</span></span>

|<span data-ttu-id="36ef8-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="36ef8-117">**Element**</span></span>|<span data-ttu-id="36ef8-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="36ef8-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="36ef8-119">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="36ef8-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="36ef8-120">Contiene las especificaciones para conectar a un cliente en el equipo que ejecuta Microsoft Exchange Server que tiene instalada la función del servidor acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="36ef8-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="36ef8-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="36ef8-121">Text value</span></span>

<span data-ttu-id="36ef8-122">El valor de texto representa una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que puede usarse para ver o cambiar las aplicaciones de correo instaladas actualmente en el buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="36ef8-122">The text value represents a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to view or change the mail apps currently installed in the user's mailbox.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="36ef8-123">Notas</span><span class="sxs-lookup"><span data-stu-id="36ef8-123">Remarks</span></span>

<span data-ttu-id="36ef8-124">El elemento **EcpUrl extinstall** es un elemento secundario opcional del elemento **Protocol** .</span><span class="sxs-lookup"><span data-stu-id="36ef8-124">The **EcpUrl-extinstall** element is an optional child element of the **Protocol** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="36ef8-125">Ver también</span><span class="sxs-lookup"><span data-stu-id="36ef8-125">See also</span></span>



[<span data-ttu-id="36ef8-126">Elementos de Autodiscover XML POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="36ef8-126">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

