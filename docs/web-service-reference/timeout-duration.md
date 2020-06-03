---
title: Tiempo de espera (duración)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bb15f9a7-8ea5-4765-9877-762c3f98bf50
description: El elemento timeout especifica el período de tiempo que debe transcurrir antes de que el servidor supere el tiempo de espera de una suscripción de extracción.
ms.openlocfilehash: b5b0e77d794080cd8e0da1e14acf4cb059b80b08
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460284"
---
# <a name="timeout-duration"></a><span data-ttu-id="b4209-103">Tiempo de espera (duración)</span><span class="sxs-lookup"><span data-stu-id="b4209-103">Timeout (duration)</span></span>

<span data-ttu-id="b4209-104">El elemento **timeout** especifica el período de tiempo que debe transcurrir antes de que el servidor supere el tiempo de espera de una suscripción de extracción.</span><span class="sxs-lookup"><span data-stu-id="b4209-104">The **Timeout** element specifies the length of time before a pull subscription is timed out by the server.</span></span> 
  
```XML
<Timeout></Timeout>
```

 <span data-ttu-id="b4209-105">**SubscriptionTimeoutType**</span><span class="sxs-lookup"><span data-stu-id="b4209-105">**SubscriptionTimeoutType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b4209-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b4209-106">Attributes and elements</span></span>

<span data-ttu-id="b4209-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b4209-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b4209-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="b4209-108">Attributes</span></span>

<span data-ttu-id="b4209-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="b4209-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b4209-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b4209-110">Child elements</span></span>

<span data-ttu-id="b4209-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="b4209-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b4209-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b4209-112">Parent elements</span></span>

[<span data-ttu-id="b4209-113">PullSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="b4209-113">PullSubscriptionRequest</span></span>](pullsubscriptionrequest.md)
  
## <a name="text-value"></a><span data-ttu-id="b4209-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="b4209-114">Text value</span></span>

<span data-ttu-id="b4209-115">El valor de texto del elemento **timeout** es el período de tiempo, en minutos, antes de que el servidor agote el tiempo de espera de una suscripción de extracción.</span><span class="sxs-lookup"><span data-stu-id="b4209-115">The text value of the **Timeout** element is the length of time, in minutes, before a pull subscription is timed out by the server.</span></span> <span data-ttu-id="b4209-116">El valor mínimo es 1; el valor máximo es 1440.</span><span class="sxs-lookup"><span data-stu-id="b4209-116">The minimum value is 1; the maximum value is 1440.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b4209-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b4209-117">Remarks</span></span>

<span data-ttu-id="b4209-118">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b4209-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="b4209-119">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="b4209-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b4209-120">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b4209-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b4209-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="b4209-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b4209-122">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b4209-122">Schema name</span></span>  <br/> |<span data-ttu-id="b4209-123">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="b4209-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="b4209-124">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b4209-124">Validation file</span></span>  <br/> |<span data-ttu-id="b4209-125">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="b4209-125">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b4209-126">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b4209-126">Can be empty</span></span>  <br/> ||
   

