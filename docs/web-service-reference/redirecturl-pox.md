---
title: RedirectUrl (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: c54f310f-8c99-4c37-8e73-ac87722b6229
description: El elemento RedirectUrl contiene la dirección URL del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes que se debe usar para obtener la configuración de detección automática.
ms.openlocfilehash: 5400b1e7a4bb7ebebc58b6a0f1fc9bf37f5a2e22
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468092"
---
# <a name="redirecturl-pox"></a><span data-ttu-id="01f34-103">RedirectUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="01f34-103">RedirectUrl (POX)</span></span>

<span data-ttu-id="01f34-104">El elemento **RedirectURL** contiene la dirección URL del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes que se debe usar para obtener la configuración de detección automática.</span><span class="sxs-lookup"><span data-stu-id="01f34-104">The **RedirectUrl** element contains the URL of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed that should be used to obtain Autodiscover settings.</span></span> 
  
[<span data-ttu-id="01f34-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="01f34-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="01f34-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="01f34-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="01f34-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="01f34-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="01f34-108">RedirectUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="01f34-108">RedirectUrl (POX)</span></span>](redirecturl-pox.md)
  
```xml
<RedirectUrl/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="01f34-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="01f34-109">Attributes and elements</span></span>

<span data-ttu-id="01f34-110">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="01f34-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="01f34-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="01f34-111">Attributes</span></span>

<span data-ttu-id="01f34-112">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="01f34-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="01f34-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="01f34-113">Child elements</span></span>

<span data-ttu-id="01f34-114">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="01f34-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="01f34-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="01f34-115">Parent elements</span></span>

|<span data-ttu-id="01f34-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="01f34-116">**Element**</span></span>|<span data-ttu-id="01f34-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="01f34-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="01f34-118">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="01f34-118">Account (POX)</span></span>](account-pox.md) <br/> |<span data-ttu-id="01f34-119">Especifica la configuración de la cuenta del usuario.</span><span class="sxs-lookup"><span data-stu-id="01f34-119">Specifies account settings for the user.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="01f34-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="01f34-120">Text value</span></span>

<span data-ttu-id="01f34-121">El valor de texto representa la dirección URL del servidor de acceso de cliente que se debe usar para obtener la configuración de detección automática.</span><span class="sxs-lookup"><span data-stu-id="01f34-121">The text value represents the URL of the Client Access server that should be used to obtain Autodiscover settings.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="01f34-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="01f34-122">Remarks</span></span>

<span data-ttu-id="01f34-123">La aplicación cliente debe dejar de redirigir después de 10 redirecciones.</span><span class="sxs-lookup"><span data-stu-id="01f34-123">The client application should stop redirecting after 10 redirects.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="01f34-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="01f34-124">See also</span></span>



[<span data-ttu-id="01f34-125">Elementos XML de detección automática de POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="01f34-125">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

