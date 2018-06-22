---
title: EwsPartnerUrl (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2ebae21c-3efa-4239-9b49-4a3a8871449b
description: El elemento EwsPartnerUrl especifica la dirección URL de la instancia de extremo procedimientos de Exchange Web Services (EWS) para un usuario habilitado para correo.
ms.openlocfilehash: 97c33e1fed4adc8a9e8542d85e67c942118f6096
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764472"
---
# <a name="ewspartnerurl-pox"></a><span data-ttu-id="47323-103">EwsPartnerUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="47323-103">EwsPartnerUrl (POX)</span></span>

<span data-ttu-id="47323-104">El elemento **EwsPartnerUrl** especifica la dirección URL de la instancia de extremo procedimientos de Exchange Web Services (EWS) para un usuario habilitado para correo.</span><span class="sxs-lookup"><span data-stu-id="47323-104">The **EwsPartnerUrl** element specifies the URL of the best endpoint instance for Exchange Web Services (EWS) for a mail-enabled user.</span></span> 
  
[<span data-ttu-id="47323-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="47323-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="47323-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="47323-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="47323-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="47323-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="47323-108">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="47323-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="47323-109">EwsPartnerUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="47323-109">EwsPartnerUrl (POX)</span></span>](ewspartnerurl-pox.md)
  
```XML
<EwsPartnerUrl/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="47323-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="47323-110">Attributes and elements</span></span>

<span data-ttu-id="47323-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="47323-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="47323-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="47323-112">Attributes</span></span>

<span data-ttu-id="47323-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="47323-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="47323-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="47323-114">Child elements</span></span>

<span data-ttu-id="47323-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="47323-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="47323-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="47323-116">Parent elements</span></span>

|<span data-ttu-id="47323-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="47323-117">**Element**</span></span>|<span data-ttu-id="47323-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="47323-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="47323-119">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="47323-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="47323-120">Contiene las especificaciones para conectar a un cliente en el equipo que ejecuta Microsoft Exchange Server que tiene instalada la función del servidor acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="47323-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="47323-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="47323-121">Text value</span></span>

<span data-ttu-id="47323-122">El valor de texto representa la dirección URL del extremo de EWS para el usuario.</span><span class="sxs-lookup"><span data-stu-id="47323-122">The text value represents the URL of the EWS endpoint for the user.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="47323-123">Notas</span><span class="sxs-lookup"><span data-stu-id="47323-123">Remarks</span></span>

<span data-ttu-id="47323-124">El elemento **EwsPartnerUrl** es un elemento secundario opcional del elemento **Protocol** .</span><span class="sxs-lookup"><span data-stu-id="47323-124">The **EwsPartnerUrl** element is an optional child element of the **Protocol** element.</span></span> <span data-ttu-id="47323-125">Es equivalente al elemento [EwsUrl (POX)](ewsurl-pox.md) .</span><span class="sxs-lookup"><span data-stu-id="47323-125">It is equivalent to the [EwsUrl (POX)](ewsurl-pox.md) element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="47323-126">Ver también</span><span class="sxs-lookup"><span data-stu-id="47323-126">See also</span></span>



[<span data-ttu-id="47323-127">Elementos de Autodiscover XML POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="47323-127">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

