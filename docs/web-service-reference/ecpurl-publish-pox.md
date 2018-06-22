---
title: EcpUrl-publicar (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a51189db-f6e5-428d-833d-65a209204a5b
description: El elemento publicar EcpUrl especifica una dirección URL parcial que se puede combinar con el valor del elemento EcpUrl (POX) para generar una dirección URL que se puede usar para tener acceso a la configuración de un usuario habilitado para correo de publicación del calendario.
ms.openlocfilehash: 82f55be3ce529f6e57db5ffe18bbdea609b13595
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764301"
---
# <a name="ecpurl-publish-pox"></a><span data-ttu-id="e47dc-103">EcpUrl-publicar (POX)</span><span class="sxs-lookup"><span data-stu-id="e47dc-103">EcpUrl-publish (POX)</span></span>

<span data-ttu-id="e47dc-104">El elemento **Publicar EcpUrl** especifica una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para tener acceso a la configuración de un usuario habilitado para correo de publicación del calendario.</span><span class="sxs-lookup"><span data-stu-id="e47dc-104">The **EcpUrl-publish** element specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access calendar publishing settings for a mail-enabled user.</span></span> 
  
[<span data-ttu-id="e47dc-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="e47dc-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="e47dc-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="e47dc-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="e47dc-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="e47dc-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="e47dc-108">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="e47dc-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="e47dc-109">EcpUrl-publicar (POX)</span><span class="sxs-lookup"><span data-stu-id="e47dc-109">EcpUrl-publish (POX)</span></span>](ecpurl-publish-pox.md)
  
```XML
<EcpUrl-publish/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="e47dc-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e47dc-110">Attributes and elements</span></span>

<span data-ttu-id="e47dc-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e47dc-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e47dc-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="e47dc-112">Attributes</span></span>

<span data-ttu-id="e47dc-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e47dc-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e47dc-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e47dc-114">Child elements</span></span>

<span data-ttu-id="e47dc-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e47dc-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e47dc-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e47dc-116">Parent elements</span></span>

|<span data-ttu-id="e47dc-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="e47dc-117">**Element**</span></span>|<span data-ttu-id="e47dc-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e47dc-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e47dc-119">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="e47dc-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="e47dc-120">Contiene las especificaciones para conectar a un cliente en el equipo que ejecuta Microsoft Exchange Server que tiene instalada la función del servidor acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="e47dc-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e47dc-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="e47dc-121">Text value</span></span>

<span data-ttu-id="e47dc-122">El valor de texto representa una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para tener acceso a la configuración de publicación de calendario para el usuario.</span><span class="sxs-lookup"><span data-stu-id="e47dc-122">The text value represents a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access calendar publishing settings for the user.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e47dc-123">Notas</span><span class="sxs-lookup"><span data-stu-id="e47dc-123">Remarks</span></span>

<span data-ttu-id="e47dc-124">El elemento **Publicar EcpUrl** es un elemento secundario opcional del elemento **Protocol** .</span><span class="sxs-lookup"><span data-stu-id="e47dc-124">The **EcpUrl-publish** element is an optional child element of the **Protocol** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e47dc-125">Ver también</span><span class="sxs-lookup"><span data-stu-id="e47dc-125">See also</span></span>



[<span data-ttu-id="e47dc-126">Elementos de Autodiscover XML POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="e47dc-126">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

