---
title: EcpUrl-TM (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f35d5ac-55be-4d3a-ad03-7d6e9349d923
description: El elemento EcpUrl-TM especifica una dirección URL parcial que se puede combinar con el valor del elemento EcpUrl (POX) para generar una dirección URL que se puede usar para tener acceso a una lista de todos los buzones de sitio de los que un usuario habilitado para correo es actualmente miembro.
ms.openlocfilehash: 8d4c787e2eeae5300cd0496f199ea71baace98ba
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463548"
---
# <a name="ecpurl-tm-pox"></a><span data-ttu-id="7fda9-103">EcpUrl-TM (POX)</span><span class="sxs-lookup"><span data-stu-id="7fda9-103">EcpUrl-tm (POX)</span></span>

<span data-ttu-id="7fda9-104">El elemento **EcpUrl-TM** especifica una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para tener acceso a una lista de todos los buzones de sitio de los que un usuario habilitado para correo es actualmente miembro.</span><span class="sxs-lookup"><span data-stu-id="7fda9-104">The **EcpUrl-tm** element specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access a list of all site mailboxes of which a mail-enabled user is currently a member.</span></span> 
  
[<span data-ttu-id="7fda9-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="7fda9-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="7fda9-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="7fda9-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="7fda9-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="7fda9-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="7fda9-108">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="7fda9-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="7fda9-109">EcpUrl-TM (POX)</span><span class="sxs-lookup"><span data-stu-id="7fda9-109">EcpUrl-tm (POX)</span></span>](ecpurl-tm-pox.md)
  
```XML
<EcpUrl-tm/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="7fda9-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="7fda9-110">Attributes and elements</span></span>

<span data-ttu-id="7fda9-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="7fda9-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7fda9-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="7fda9-112">Attributes</span></span>

<span data-ttu-id="7fda9-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="7fda9-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7fda9-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7fda9-114">Child elements</span></span>

<span data-ttu-id="7fda9-115">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="7fda9-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7fda9-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7fda9-116">Parent elements</span></span>

|<span data-ttu-id="7fda9-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7fda9-117">**Element**</span></span>|<span data-ttu-id="7fda9-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7fda9-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7fda9-119">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="7fda9-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="7fda9-120">Contiene las especificaciones para conectar un cliente al equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="7fda9-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7fda9-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="7fda9-121">Text value</span></span>

<span data-ttu-id="7fda9-122">El valor de texto representa una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para tener acceso a una lista de buzones del sitio para el usuario.</span><span class="sxs-lookup"><span data-stu-id="7fda9-122">The text value represents a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access a list of site mailboxes for the user.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7fda9-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7fda9-123">Remarks</span></span>

<span data-ttu-id="7fda9-124">El elemento **EcpUrl-TM** es un elemento secundario opcional del elemento **Protocol** .</span><span class="sxs-lookup"><span data-stu-id="7fda9-124">The **EcpUrl-tm** element is an optional child element of the **Protocol** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7fda9-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="7fda9-125">See also</span></span>



[<span data-ttu-id="7fda9-126">Elementos XML de detección automática de POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="7fda9-126">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

