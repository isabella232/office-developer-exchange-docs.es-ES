---
title: RedirectAddr (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 0e9fa6b6-7991-4dc1-a59a-48e5f8e041e4
description: El elemento RedirectAddr especifica la dirección de correo electrónico que se debe usar para una solicitud de detección automática subsiguiente.
ms.openlocfilehash: 6bff28001851f421b4c7429770185401f2f0a743
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529878"
---
# <a name="redirectaddr-pox"></a><span data-ttu-id="b8954-103">RedirectAddr (POX)</span><span class="sxs-lookup"><span data-stu-id="b8954-103">RedirectAddr (POX)</span></span>

<span data-ttu-id="b8954-104">El elemento **RedirectAddr** especifica la dirección de correo electrónico que se debe usar para una solicitud de detección automática subsiguiente.</span><span class="sxs-lookup"><span data-stu-id="b8954-104">The **RedirectAddr** element specifies the e-mail address that should be used for a subsequent Autodiscover request.</span></span> 
  
[<span data-ttu-id="b8954-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="b8954-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="b8954-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="b8954-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="b8954-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="b8954-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="b8954-108">RedirectAddr (POX)</span><span class="sxs-lookup"><span data-stu-id="b8954-108">RedirectAddr (POX)</span></span>](redirectaddr-pox.md)
  
```xml
<RedirectAddr/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="b8954-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b8954-109">Attributes and elements</span></span>

<span data-ttu-id="b8954-110">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b8954-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b8954-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="b8954-111">Attributes</span></span>

<span data-ttu-id="b8954-112">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="b8954-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b8954-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b8954-113">Child elements</span></span>

<span data-ttu-id="b8954-114">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="b8954-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b8954-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b8954-115">Parent elements</span></span>

|<span data-ttu-id="b8954-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b8954-116">**Element**</span></span>|<span data-ttu-id="b8954-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b8954-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b8954-118">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="b8954-118">Account (POX)</span></span>](account-pox.md) <br/> |<span data-ttu-id="b8954-119">Especifica la configuración de la cuenta del usuario.</span><span class="sxs-lookup"><span data-stu-id="b8954-119">Specifies account settings for the user.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b8954-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="b8954-120">Text value</span></span>

<span data-ttu-id="b8954-121">El valor de texto representa la dirección de correo electrónico que se debe usar para una solicitud de detección automática subsiguiente.</span><span class="sxs-lookup"><span data-stu-id="b8954-121">The text value represents the e-mail address that should be used for a subsequent Autodiscover request.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b8954-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b8954-122">Remarks</span></span>

<span data-ttu-id="b8954-123">Si este elemento está presente en la respuesta de detección automática, realice otra solicitud usando el valor de texto del elemento **RedirectAddr** .</span><span class="sxs-lookup"><span data-stu-id="b8954-123">If this element is present in the Autodiscover response, make another request by using the text value of the **RedirectAddr** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b8954-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="b8954-124">See also</span></span>



[<span data-ttu-id="b8954-125">Elementos XML de detección automática de POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="b8954-125">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

