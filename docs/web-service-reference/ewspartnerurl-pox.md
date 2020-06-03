---
title: EwsPartnerUrl (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2ebae21c-3efa-4239-9b49-4a3a8871449b
description: El elemento EwsPartnerUrl especifica la dirección URL de la mejor instancia de punto de conexión para los servicios web Exchange (EWS) para un usuario habilitado para correo.
ms.openlocfilehash: a67eb17bb3db67a922c53ba5e37900ee0a9b956b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526112"
---
# <a name="ewspartnerurl-pox"></a><span data-ttu-id="3aab1-103">EwsPartnerUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="3aab1-103">EwsPartnerUrl (POX)</span></span>

<span data-ttu-id="3aab1-104">El elemento **EwsPartnerUrl** especifica la dirección URL de la mejor instancia de punto de conexión para los servicios web Exchange (EWS) para un usuario habilitado para correo.</span><span class="sxs-lookup"><span data-stu-id="3aab1-104">The **EwsPartnerUrl** element specifies the URL of the best endpoint instance for Exchange Web Services (EWS) for a mail-enabled user.</span></span> 
  
[<span data-ttu-id="3aab1-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="3aab1-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="3aab1-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="3aab1-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="3aab1-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="3aab1-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="3aab1-108">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="3aab1-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="3aab1-109">EwsPartnerUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="3aab1-109">EwsPartnerUrl (POX)</span></span>](ewspartnerurl-pox.md)
  
```XML
<EwsPartnerUrl/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="3aab1-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3aab1-110">Attributes and elements</span></span>

<span data-ttu-id="3aab1-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3aab1-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3aab1-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="3aab1-112">Attributes</span></span>

<span data-ttu-id="3aab1-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="3aab1-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3aab1-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3aab1-114">Child elements</span></span>

<span data-ttu-id="3aab1-115">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="3aab1-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3aab1-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3aab1-116">Parent elements</span></span>

|<span data-ttu-id="3aab1-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="3aab1-117">**Element**</span></span>|<span data-ttu-id="3aab1-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3aab1-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3aab1-119">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="3aab1-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="3aab1-120">Contiene las especificaciones para conectar un cliente al equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="3aab1-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3aab1-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="3aab1-121">Text value</span></span>

<span data-ttu-id="3aab1-122">El valor de texto representa la dirección URL del extremo de EWS para el usuario.</span><span class="sxs-lookup"><span data-stu-id="3aab1-122">The text value represents the URL of the EWS endpoint for the user.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3aab1-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3aab1-123">Remarks</span></span>

<span data-ttu-id="3aab1-124">El elemento **EwsPartnerUrl** es un elemento secundario opcional del elemento **Protocol** .</span><span class="sxs-lookup"><span data-stu-id="3aab1-124">The **EwsPartnerUrl** element is an optional child element of the **Protocol** element.</span></span> <span data-ttu-id="3aab1-125">Es equivalente al elemento [EwsUrl (POX)](ewsurl-pox.md) .</span><span class="sxs-lookup"><span data-stu-id="3aab1-125">It is equivalent to the [EwsUrl (POX)](ewsurl-pox.md) element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3aab1-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="3aab1-126">See also</span></span>



[<span data-ttu-id="3aab1-127">Elementos XML de detección automática de POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="3aab1-127">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

