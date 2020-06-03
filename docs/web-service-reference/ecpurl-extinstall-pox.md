---
title: EcpUrl-extinstall (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f81807e6-93de-4e47-afee-1e1ae6a85054
description: El elemento EcpUrl-extinstall especifica una dirección URL parcial que se puede combinar con el valor del elemento EcpUrl (POX) para generar una dirección URL que se puede usar para ver o cambiar las aplicaciones de correo actualmente instaladas en el buzón del usuario.
ms.openlocfilehash: 889e0ca3bdcdce4b557fe066db2918fde4abaa9b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461306"
---
# <a name="ecpurl-extinstall-pox"></a><span data-ttu-id="65897-103">EcpUrl-extinstall (POX)</span><span class="sxs-lookup"><span data-stu-id="65897-103">EcpUrl-extinstall (POX)</span></span>

<span data-ttu-id="65897-104">El elemento **EcpUrl-extinstall** especifica una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para ver o cambiar las aplicaciones de correo actualmente instaladas en el buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="65897-104">The **EcpUrl-extinstall** element specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to view or change the mail apps currently installed in the user's mailbox.</span></span> 
  
[<span data-ttu-id="65897-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="65897-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="65897-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="65897-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="65897-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="65897-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="65897-108">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="65897-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="65897-109">EcpUrl-extinstall (POX)</span><span class="sxs-lookup"><span data-stu-id="65897-109">EcpUrl-extinstall (POX)</span></span>](ecpurl-extinstall-pox.md)
  
```XML
<EcpUrl-extinstall/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="65897-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="65897-110">Attributes and elements</span></span>

<span data-ttu-id="65897-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="65897-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="65897-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="65897-112">Attributes</span></span>

<span data-ttu-id="65897-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="65897-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="65897-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="65897-114">Child elements</span></span>

<span data-ttu-id="65897-115">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="65897-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="65897-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="65897-116">Parent elements</span></span>

|<span data-ttu-id="65897-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="65897-117">**Element**</span></span>|<span data-ttu-id="65897-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="65897-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="65897-119">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="65897-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="65897-120">Contiene las especificaciones para conectar un cliente al equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="65897-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="65897-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="65897-121">Text value</span></span>

<span data-ttu-id="65897-122">El valor de texto representa una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para ver o cambiar las aplicaciones de correo actualmente instaladas en el buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="65897-122">The text value represents a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to view or change the mail apps currently installed in the user's mailbox.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="65897-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="65897-123">Remarks</span></span>

<span data-ttu-id="65897-124">El elemento **EcpUrl-extinstall** es un elemento secundario opcional del elemento **Protocol** .</span><span class="sxs-lookup"><span data-stu-id="65897-124">The **EcpUrl-extinstall** element is an optional child element of the **Protocol** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="65897-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="65897-125">See also</span></span>



[<span data-ttu-id="65897-126">Elementos XML de detección automática de POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="65897-126">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

