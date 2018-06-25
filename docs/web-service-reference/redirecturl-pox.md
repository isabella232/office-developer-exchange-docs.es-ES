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
description: El elemento RedirectUrl contiene la dirección URL del equipo que ejecuta Microsoft Exchange Server 2007 que tiene el rol de servidor de acceso de cliente instalado que se debe usar para obtener la configuración de detección automática.
ms.openlocfilehash: 3b634f1a3a3d44b6aae1a826a005149200641dcb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837027"
---
# <a name="redirecturl-pox"></a><span data-ttu-id="f851e-103">RedirectUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="f851e-103">RedirectUrl (POX)</span></span>

<span data-ttu-id="f851e-104">El elemento **RedirectUrl** contiene la dirección URL del equipo que ejecuta Microsoft Exchange Server 2007 que tiene el rol de servidor de acceso de cliente instalado que se debe usar para obtener la configuración de detección automática.</span><span class="sxs-lookup"><span data-stu-id="f851e-104">The **RedirectUrl** element contains the URL of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed that should be used to obtain Autodiscover settings.</span></span> 
  
[<span data-ttu-id="f851e-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="f851e-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="f851e-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="f851e-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="f851e-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="f851e-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="f851e-108">RedirectUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="f851e-108">RedirectUrl (POX)</span></span>](redirecturl-pox.md)
  
```xml
<RedirectUrl/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="f851e-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f851e-109">Attributes and elements</span></span>

<span data-ttu-id="f851e-110">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f851e-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f851e-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="f851e-111">Attributes</span></span>

<span data-ttu-id="f851e-112">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f851e-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f851e-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f851e-113">Child elements</span></span>

<span data-ttu-id="f851e-114">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f851e-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f851e-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f851e-115">Parent elements</span></span>

|<span data-ttu-id="f851e-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="f851e-116">**Element**</span></span>|<span data-ttu-id="f851e-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f851e-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f851e-118">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="f851e-118">Account (POX)</span></span>](account-pox.md) <br/> |<span data-ttu-id="f851e-119">Especifica la configuración de cuenta para el usuario.</span><span class="sxs-lookup"><span data-stu-id="f851e-119">Specifies account settings for the user.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f851e-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="f851e-120">Text value</span></span>

<span data-ttu-id="f851e-121">El valor de texto representa la dirección URL del servidor de acceso de cliente que se debe usar para obtener la configuración de detección automática.</span><span class="sxs-lookup"><span data-stu-id="f851e-121">The text value represents the URL of the Client Access server that should be used to obtain Autodiscover settings.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f851e-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f851e-122">Remarks</span></span>

<span data-ttu-id="f851e-123">La aplicación cliente debe dejar de redirigir después de 10 redirecciones.</span><span class="sxs-lookup"><span data-stu-id="f851e-123">The client application should stop redirecting after 10 redirects.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f851e-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="f851e-124">See also</span></span>



[<span data-ttu-id="f851e-125">Elementos de Autodiscover XML POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="f851e-125">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

