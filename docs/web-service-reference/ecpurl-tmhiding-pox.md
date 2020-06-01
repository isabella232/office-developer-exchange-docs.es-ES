---
title: EcpUrl-tmHiding (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b9ae15b-3ac1-45ac-85ba-38c7231fe508
description: El elemento EcpUrl-tmHiding especifica una dirección URL parcial que se puede combinar con el valor del elemento EcpUrl (POX) para generar una dirección URL que se puede usar para cancelar la suscripción del usuario a un buzón del sitio.
ms.openlocfilehash: 68b949db8b8d98caddbac3b9f96c5d5e55b104b7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463534"
---
# <a name="ecpurl-tmhiding-pox"></a><span data-ttu-id="25117-103">EcpUrl-tmHiding (POX)</span><span class="sxs-lookup"><span data-stu-id="25117-103">EcpUrl-tmHiding (POX)</span></span>

<span data-ttu-id="25117-104">El elemento **EcpUrl-tmHiding** especifica una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para cancelar la suscripción del usuario a un buzón del sitio.</span><span class="sxs-lookup"><span data-stu-id="25117-104">The **EcpUrl-tmHiding** element specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to unsubscribe the user from a site mailbox.</span></span> 
  
[<span data-ttu-id="25117-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="25117-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="25117-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="25117-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="25117-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="25117-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="25117-108">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="25117-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="25117-109">EcpUrl-tmHiding (POX)</span><span class="sxs-lookup"><span data-stu-id="25117-109">EcpUrl-tmHiding (POX)</span></span>](ecpurl-tmhiding-pox.md)
  
```XML
<EcpUrl-tmHiding/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="25117-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="25117-110">Attributes and elements</span></span>

<span data-ttu-id="25117-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="25117-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="25117-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="25117-112">Attributes</span></span>

<span data-ttu-id="25117-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="25117-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="25117-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="25117-114">Child elements</span></span>

<span data-ttu-id="25117-115">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="25117-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="25117-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="25117-116">Parent elements</span></span>

|<span data-ttu-id="25117-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="25117-117">**Element**</span></span>|<span data-ttu-id="25117-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="25117-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="25117-119">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="25117-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="25117-120">Contiene las especificaciones para conectar un cliente al equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="25117-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="25117-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="25117-121">Text value</span></span>

<span data-ttu-id="25117-122">El valor de texto representa una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para cancelar la suscripción del usuario a un buzón del sitio.</span><span class="sxs-lookup"><span data-stu-id="25117-122">The text value represents a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to unsubscribe the user from a site mailbox.</span></span> <span data-ttu-id="25117-123">El valor del elemento **EcpUrl-tmHiding** contiene los parámetros contenidos dentro de los caracteres ' < ' y ' > ' que el cliente sustituye, tal como se muestra en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="25117-123">The value of the **EcpUrl-tmHiding** element contains parameters contained within '<' and '>' characters that are substituted by the client as shown in the following table.</span></span> 
  
|<span data-ttu-id="25117-124">**Parámetro**</span><span class="sxs-lookup"><span data-stu-id="25117-124">**Parameter**</span></span>|<span data-ttu-id="25117-125">**Sustituto con**</span><span class="sxs-lookup"><span data-stu-id="25117-125">**Substitute with**</span></span>|
|:-----|:-----|
| <span data-ttu-id="25117-126">_Id_</span><span class="sxs-lookup"><span data-stu-id="25117-126">_Id_</span></span> <br/> |<span data-ttu-id="25117-127">La dirección de correo electrónico SMTP o el nombre distintivo X500 del buzón del sitio.</span><span class="sxs-lookup"><span data-stu-id="25117-127">The SMTP email address or the X500 distinguished name of the site mailbox.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="25117-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="25117-128">Remarks</span></span>

<span data-ttu-id="25117-129">El elemento **EcpUrl-tmHiding** es un elemento secundario opcional del elemento **Protocol** .</span><span class="sxs-lookup"><span data-stu-id="25117-129">The **EcpUrl-tmHiding** element is an optional child element of the **Protocol** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="25117-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="25117-130">See also</span></span>



[<span data-ttu-id="25117-131">Elementos XML de detección automática de POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="25117-131">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

