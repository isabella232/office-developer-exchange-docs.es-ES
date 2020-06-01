---
title: EcpUrl-publicación (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a51189db-f6e5-428d-833d-65a209204a5b
description: El elemento EcpUrl-Publish especifica una dirección URL parcial que se puede combinar con el valor del elemento EcpUrl (POX) para generar una dirección URL que se puede usar para obtener acceso a la configuración de publicación de calendario para un usuario habilitado para correo.
ms.openlocfilehash: 98cac9132c1ba6e368be6337fbf3b522a02cb47a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458008"
---
# <a name="ecpurl-publish-pox"></a><span data-ttu-id="b102c-103">EcpUrl-publicación (POX)</span><span class="sxs-lookup"><span data-stu-id="b102c-103">EcpUrl-publish (POX)</span></span>

<span data-ttu-id="b102c-104">El elemento **EcpUrl-Publish** especifica una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para obtener acceso a la configuración de publicación de calendario para un usuario habilitado para correo.</span><span class="sxs-lookup"><span data-stu-id="b102c-104">The **EcpUrl-publish** element specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access calendar publishing settings for a mail-enabled user.</span></span> 
  
[<span data-ttu-id="b102c-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="b102c-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="b102c-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="b102c-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="b102c-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="b102c-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="b102c-108">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="b102c-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="b102c-109">EcpUrl-publicación (POX)</span><span class="sxs-lookup"><span data-stu-id="b102c-109">EcpUrl-publish (POX)</span></span>](ecpurl-publish-pox.md)
  
```XML
<EcpUrl-publish/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="b102c-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b102c-110">Attributes and elements</span></span>

<span data-ttu-id="b102c-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b102c-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b102c-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="b102c-112">Attributes</span></span>

<span data-ttu-id="b102c-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="b102c-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b102c-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b102c-114">Child elements</span></span>

<span data-ttu-id="b102c-115">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="b102c-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b102c-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b102c-116">Parent elements</span></span>

|<span data-ttu-id="b102c-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b102c-117">**Element**</span></span>|<span data-ttu-id="b102c-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b102c-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b102c-119">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="b102c-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="b102c-120">Contiene las especificaciones para conectar un cliente al equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="b102c-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b102c-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="b102c-121">Text value</span></span>

<span data-ttu-id="b102c-122">El valor de texto representa una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para obtener acceso a la configuración de publicación del calendario para el usuario.</span><span class="sxs-lookup"><span data-stu-id="b102c-122">The text value represents a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access calendar publishing settings for the user.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b102c-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b102c-123">Remarks</span></span>

<span data-ttu-id="b102c-124">El elemento **EcpUrl-Publish** es un elemento secundario opcional del elemento **Protocol** .</span><span class="sxs-lookup"><span data-stu-id="b102c-124">The **EcpUrl-publish** element is an optional child element of the **Protocol** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b102c-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="b102c-125">See also</span></span>



[<span data-ttu-id="b102c-126">Elementos XML de detección automática de POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="b102c-126">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

