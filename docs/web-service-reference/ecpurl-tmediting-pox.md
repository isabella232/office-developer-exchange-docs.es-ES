---
title: EcpUrl-tmEditing (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1fbc2ea9-3f94-441b-ab42-647326bf0021
description: El elemento EcpUrl tmEditing especifica una dirección URL parcial que se puede combinar con el valor del elemento EcpUrl (POX) para generar una dirección URL que se puede usar para editar un buzón de sitio existente.
ms.openlocfilehash: 29b27ffe9ef3c18a3b6471ca4a42956a43a5aaa6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764304"
---
# <a name="ecpurl-tmediting-pox"></a><span data-ttu-id="c600d-103">EcpUrl-tmEditing (POX)</span><span class="sxs-lookup"><span data-stu-id="c600d-103">EcpUrl-tmEditing (POX)</span></span>

<span data-ttu-id="c600d-104">El elemento **EcpUrl tmEditing** especifica una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para editar un buzón de sitio existente.</span><span class="sxs-lookup"><span data-stu-id="c600d-104">The **EcpUrl-tmEditing** element specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to edit an existing site mailbox.</span></span> 
  
[<span data-ttu-id="c600d-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="c600d-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="c600d-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="c600d-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="c600d-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="c600d-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="c600d-108">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="c600d-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="c600d-109">EcpUrl-tmEditing (POX)</span><span class="sxs-lookup"><span data-stu-id="c600d-109">EcpUrl-tmEditing (POX)</span></span>](ecpurl-tmediting-pox.md)
  
```XML
<EcpUrl-tmEditing/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="c600d-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c600d-110">Attributes and elements</span></span>

<span data-ttu-id="c600d-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c600d-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c600d-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="c600d-112">Attributes</span></span>

<span data-ttu-id="c600d-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c600d-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c600d-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c600d-114">Child elements</span></span>

<span data-ttu-id="c600d-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c600d-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c600d-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c600d-116">Parent elements</span></span>

|<span data-ttu-id="c600d-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="c600d-117">**Element**</span></span>|<span data-ttu-id="c600d-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c600d-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c600d-119">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="c600d-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="c600d-120">Contiene las especificaciones para conectar a un cliente en el equipo que ejecuta Microsoft Exchange Server que tiene instalada la función del servidor acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="c600d-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c600d-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="c600d-121">Text value</span></span>

<span data-ttu-id="c600d-122">El valor de texto representa una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para editar un buzón de sitio existente.</span><span class="sxs-lookup"><span data-stu-id="c600d-122">The text value represents a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to edit an existing site mailbox.</span></span> <span data-ttu-id="c600d-123">El valor del elemento **EcpUrl tmEditing** contiene parámetros contenidos en ' <' y ' >' caracteres que se sustituyen por el cliente, como se muestra en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="c600d-123">The value of the **EcpUrl-tmEditing** element contains parameters contained within '<' and '>' characters that are substituted by the client as shown in the following table.</span></span> 
  
|<span data-ttu-id="c600d-124">**Parámetro**</span><span class="sxs-lookup"><span data-stu-id="c600d-124">**Parameter**</span></span>|<span data-ttu-id="c600d-125">**Sustituir con**</span><span class="sxs-lookup"><span data-stu-id="c600d-125">**Substitute with**</span></span>|
|:-----|:-----|
| <span data-ttu-id="c600d-126">_id
_</span><span class="sxs-lookup"><span data-stu-id="c600d-126">_Id_</span></span> <br/> |<span data-ttu-id="c600d-127">Nombre del buzón de sitio completo para la dirección de correo electrónico SMTP o la X500.</span><span class="sxs-lookup"><span data-stu-id="c600d-127">The SMTP email address or the X500 distinguished name of the site mailbox.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c600d-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c600d-128">Remarks</span></span>

<span data-ttu-id="c600d-129">El elemento **EcpUrl tmEditing** es un elemento secundario opcional del elemento **Protocol** .</span><span class="sxs-lookup"><span data-stu-id="c600d-129">The **EcpUrl-tmEditing** element is an optional child element of the **Protocol** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c600d-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="c600d-130">See also</span></span>



[<span data-ttu-id="c600d-131">Elementos de Autodiscover XML POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="c600d-131">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

