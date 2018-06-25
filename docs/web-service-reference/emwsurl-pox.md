---
title: EmwsUrl (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: cad0fa91-8d75-4dde-a484-518c837ae063
description: El elemento EmwsUrl especifica la dirección URL de la instancia de extremo procedimientos de Exchange Web Services (EWS) para un usuario habilitado para correo.
ms.openlocfilehash: d8905d098c9978c3413f67e9a1b2443a52fb0d1f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764386"
---
# <a name="emwsurl-pox"></a><span data-ttu-id="bed9f-103">EmwsUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="bed9f-103">EmwsUrl (POX)</span></span>

<span data-ttu-id="bed9f-104">El elemento **EmwsUrl** especifica la dirección URL de la instancia de extremo procedimientos de Exchange Web Services (EWS) para un usuario habilitado para correo.</span><span class="sxs-lookup"><span data-stu-id="bed9f-104">The **EmwsUrl** element specifies the URL of the best endpoint instance for Exchange Web Services (EWS) for a mail-enabled user.</span></span> 
  
- [<span data-ttu-id="bed9f-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="bed9f-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md) 
- [<span data-ttu-id="bed9f-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="bed9f-106">Response (POX)</span></span>](response-pox.md) 
- [<span data-ttu-id="bed9f-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="bed9f-107">Account (POX)</span></span>](account-pox.md) 
- [<span data-ttu-id="bed9f-108">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="bed9f-108">Protocol (POX)</span></span>](protocol-pox.md) 
- [<span data-ttu-id="bed9f-109">EmwsUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="bed9f-109">EmwsUrl (POX)</span></span>](emwsurl-pox.md)
  
```XML
<EmwsUrl/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="bed9f-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="bed9f-110">Attributes and elements</span></span>

<span data-ttu-id="bed9f-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="bed9f-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bed9f-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="bed9f-112">Attributes</span></span>

<span data-ttu-id="bed9f-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="bed9f-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bed9f-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="bed9f-114">Child elements</span></span>

<span data-ttu-id="bed9f-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="bed9f-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="bed9f-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="bed9f-116">Parent elements</span></span>

|<span data-ttu-id="bed9f-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="bed9f-117">**Element**</span></span>|<span data-ttu-id="bed9f-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bed9f-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bed9f-119">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="bed9f-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="bed9f-120">Contiene las especificaciones para conectar a un cliente en el equipo que ejecuta Microsoft Exchange Server que tiene instalada la función del servidor acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="bed9f-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="bed9f-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="bed9f-121">Text value</span></span>

<span data-ttu-id="bed9f-122">El valor de texto representa la dirección URL del extremo de EWS para el usuario.</span><span class="sxs-lookup"><span data-stu-id="bed9f-122">The text value represents the URL of the EWS endpoint for the user.</span></span> <span data-ttu-id="bed9f-123">Es equivalente al elemento [EwsUrl (POX)](ewsurl-pox.md) .</span><span class="sxs-lookup"><span data-stu-id="bed9f-123">It is equivalent to the [EwsUrl (POX)](ewsurl-pox.md) element.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="bed9f-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bed9f-124">Remarks</span></span>

<span data-ttu-id="bed9f-125">El elemento **EmwsUrl** es un elemento secundario opcional del elemento **Protocol** .</span><span class="sxs-lookup"><span data-stu-id="bed9f-125">The **EmwsUrl** element is an optional child element of the **Protocol** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bed9f-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="bed9f-126">See also</span></span>

- [<span data-ttu-id="bed9f-127">Elementos de Autodiscover XML POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="bed9f-127">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

