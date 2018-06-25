---
title: EcpUrl-tm (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f35d5ac-55be-4d3a-ad03-7d6e9349d923
description: El elemento EcpUrl tm especifica una dirección URL parcial que se puede combinar con el valor del elemento EcpUrl (POX) para generar una dirección URL que se puede usar para tener acceso a una lista de todos los buzones del sitio de que un usuario habilitado para correo actualmente es un miembro.
ms.openlocfilehash: 786459cab98f8c169f768b6ef850792e8111761a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764303"
---
# <a name="ecpurl-tm-pox"></a><span data-ttu-id="1ccbe-103">EcpUrl-tm (POX)</span><span class="sxs-lookup"><span data-stu-id="1ccbe-103">EcpUrl-tm (POX)</span></span>

<span data-ttu-id="1ccbe-104">El elemento **EcpUrl tm** especifica una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para tener acceso a una lista de todos los buzones del sitio de que un usuario habilitado para correo actualmente es un miembro.</span><span class="sxs-lookup"><span data-stu-id="1ccbe-104">The **EcpUrl-tm** element specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access a list of all site mailboxes of which a mail-enabled user is currently a member.</span></span> 
  
[<span data-ttu-id="1ccbe-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="1ccbe-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="1ccbe-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="1ccbe-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="1ccbe-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="1ccbe-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="1ccbe-108">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="1ccbe-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="1ccbe-109">EcpUrl-tm (POX)</span><span class="sxs-lookup"><span data-stu-id="1ccbe-109">EcpUrl-tm (POX)</span></span>](ecpurl-tm-pox.md)
  
```XML
<EcpUrl-tm/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="1ccbe-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="1ccbe-110">Attributes and elements</span></span>

<span data-ttu-id="1ccbe-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="1ccbe-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1ccbe-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="1ccbe-112">Attributes</span></span>

<span data-ttu-id="1ccbe-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1ccbe-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1ccbe-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1ccbe-114">Child elements</span></span>

<span data-ttu-id="1ccbe-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1ccbe-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1ccbe-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="1ccbe-116">Parent elements</span></span>

|<span data-ttu-id="1ccbe-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="1ccbe-117">**Element**</span></span>|<span data-ttu-id="1ccbe-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1ccbe-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1ccbe-119">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="1ccbe-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="1ccbe-120">Contiene las especificaciones para conectar a un cliente en el equipo que ejecuta Microsoft Exchange Server que tiene instalada la función del servidor acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="1ccbe-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1ccbe-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="1ccbe-121">Text value</span></span>

<span data-ttu-id="1ccbe-122">El valor de texto representa una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para tener acceso a una lista de los buzones del sitio para el usuario.</span><span class="sxs-lookup"><span data-stu-id="1ccbe-122">The text value represents a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access a list of site mailboxes for the user.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="1ccbe-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1ccbe-123">Remarks</span></span>

<span data-ttu-id="1ccbe-124">El elemento **EcpUrl tm** es un elemento secundario opcional del elemento **Protocol** .</span><span class="sxs-lookup"><span data-stu-id="1ccbe-124">The **EcpUrl-tm** element is an optional child element of the **Protocol** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1ccbe-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="1ccbe-125">See also</span></span>



[<span data-ttu-id="1ccbe-126">Elementos de Autodiscover XML POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="1ccbe-126">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

