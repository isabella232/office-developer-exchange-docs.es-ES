---
title: EcpUrl-RET (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5f090fd2-b0c4-4ca0-a959-1433d73a2069
description: El elemento EcpUrl-RET especifica una dirección URL parcial que se puede combinar con el valor del elemento EcpUrl (POX) para generar una dirección URL que se puede usar para obtener acceso a la configuración de la etiqueta de retención para un usuario habilitado para correo.
ms.openlocfilehash: 1f6878dc58bb01fca6a56fdd645efd3363a3d442
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458694"
---
# <a name="ecpurl-ret-pox"></a><span data-ttu-id="fb682-103">EcpUrl-RET (POX)</span><span class="sxs-lookup"><span data-stu-id="fb682-103">EcpUrl-ret (POX)</span></span>

<span data-ttu-id="fb682-104">El elemento **EcpUrl-RET** especifica una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para obtener acceso a la configuración de la etiqueta de retención para un usuario habilitado para correo.</span><span class="sxs-lookup"><span data-stu-id="fb682-104">The **EcpUrl-ret** element specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access retention tag settings for a mail-enabled user.</span></span> 
  
[<span data-ttu-id="fb682-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="fb682-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="fb682-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="fb682-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="fb682-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="fb682-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="fb682-108">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="fb682-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="fb682-109">EcpUrl-RET (POX)</span><span class="sxs-lookup"><span data-stu-id="fb682-109">EcpUrl-ret (POX)</span></span>](ecpurl-ret-pox.md)
  
```XML
<EcpUrl-ret/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="fb682-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="fb682-110">Attributes and elements</span></span>

<span data-ttu-id="fb682-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="fb682-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fb682-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="fb682-112">Attributes</span></span>

<span data-ttu-id="fb682-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="fb682-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fb682-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="fb682-114">Child elements</span></span>

<span data-ttu-id="fb682-115">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="fb682-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="fb682-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="fb682-116">Parent elements</span></span>

|<span data-ttu-id="fb682-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="fb682-117">**Element**</span></span>|<span data-ttu-id="fb682-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fb682-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fb682-119">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="fb682-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="fb682-120">Contiene las especificaciones para conectar un cliente al equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="fb682-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="fb682-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="fb682-121">Text value</span></span>

<span data-ttu-id="fb682-122">El valor de texto representa una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para obtener acceso a la configuración de la etiqueta de retención del usuario.</span><span class="sxs-lookup"><span data-stu-id="fb682-122">The text value represents a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access retention tag settings for the user.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="fb682-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fb682-123">Remarks</span></span>

<span data-ttu-id="fb682-124">El elemento **EcpUrl-RET** es un elemento secundario opcional del elemento **Protocol** .</span><span class="sxs-lookup"><span data-stu-id="fb682-124">The **EcpUrl-ret** element is an optional child element of the **Protocol** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fb682-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="fb682-125">See also</span></span>



[<span data-ttu-id="fb682-126">Elementos XML de detección automática de POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="fb682-126">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

