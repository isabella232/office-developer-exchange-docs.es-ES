---
title: EcpUrl-tmEditing (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1fbc2ea9-3f94-441b-ab42-647326bf0021
description: El elemento EcpUrl-tmEditing especifica una dirección URL parcial que se puede combinar con el valor del elemento EcpUrl (POX) para generar una dirección URL que se puede usar para editar un buzón de sitio existente.
ms.openlocfilehash: 5d6c6b8e8f73d113cfde3570065435927ffbae05
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463541"
---
# <a name="ecpurl-tmediting-pox"></a><span data-ttu-id="5641c-103">EcpUrl-tmEditing (POX)</span><span class="sxs-lookup"><span data-stu-id="5641c-103">EcpUrl-tmEditing (POX)</span></span>

<span data-ttu-id="5641c-104">El elemento **EcpUrl-tmEditing** especifica una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para editar un buzón de sitio existente.</span><span class="sxs-lookup"><span data-stu-id="5641c-104">The **EcpUrl-tmEditing** element specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to edit an existing site mailbox.</span></span> 
  
[<span data-ttu-id="5641c-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="5641c-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="5641c-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="5641c-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="5641c-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="5641c-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="5641c-108">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="5641c-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="5641c-109">EcpUrl-tmEditing (POX)</span><span class="sxs-lookup"><span data-stu-id="5641c-109">EcpUrl-tmEditing (POX)</span></span>](ecpurl-tmediting-pox.md)
  
```XML
<EcpUrl-tmEditing/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="5641c-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="5641c-110">Attributes and elements</span></span>

<span data-ttu-id="5641c-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="5641c-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5641c-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="5641c-112">Attributes</span></span>

<span data-ttu-id="5641c-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="5641c-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5641c-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5641c-114">Child elements</span></span>

<span data-ttu-id="5641c-115">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="5641c-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5641c-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5641c-116">Parent elements</span></span>

|<span data-ttu-id="5641c-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="5641c-117">**Element**</span></span>|<span data-ttu-id="5641c-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5641c-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5641c-119">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="5641c-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="5641c-120">Contiene las especificaciones para conectar un cliente al equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="5641c-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5641c-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="5641c-121">Text value</span></span>

<span data-ttu-id="5641c-122">El valor de texto representa una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para editar un buzón de sitio existente.</span><span class="sxs-lookup"><span data-stu-id="5641c-122">The text value represents a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to edit an existing site mailbox.</span></span> <span data-ttu-id="5641c-123">El valor del elemento **EcpUrl-tmEditing** contiene los parámetros contenidos dentro de los caracteres ' < ' y ' > ' que el cliente sustituye, tal como se muestra en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="5641c-123">The value of the **EcpUrl-tmEditing** element contains parameters contained within '<' and '>' characters that are substituted by the client as shown in the following table.</span></span> 
  
|<span data-ttu-id="5641c-124">**Parámetro**</span><span class="sxs-lookup"><span data-stu-id="5641c-124">**Parameter**</span></span>|<span data-ttu-id="5641c-125">**Sustituto con**</span><span class="sxs-lookup"><span data-stu-id="5641c-125">**Substitute with**</span></span>|
|:-----|:-----|
| <span data-ttu-id="5641c-126">_Id_</span><span class="sxs-lookup"><span data-stu-id="5641c-126">_Id_</span></span> <br/> |<span data-ttu-id="5641c-127">La dirección de correo electrónico SMTP o el nombre distintivo X500 del buzón del sitio.</span><span class="sxs-lookup"><span data-stu-id="5641c-127">The SMTP email address or the X500 distinguished name of the site mailbox.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5641c-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5641c-128">Remarks</span></span>

<span data-ttu-id="5641c-129">El elemento **EcpUrl-tmEditing** es un elemento secundario opcional del elemento **Protocol** .</span><span class="sxs-lookup"><span data-stu-id="5641c-129">The **EcpUrl-tmEditing** element is an optional child element of the **Protocol** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5641c-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="5641c-130">See also</span></span>



[<span data-ttu-id="5641c-131">Elementos XML de detección automática de POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="5641c-131">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

