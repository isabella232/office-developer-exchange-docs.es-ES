---
title: Tiempo de espera (duración)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bb15f9a7-8ea5-4765-9877-762c3f98bf50
description: El elemento de tiempo de espera especifica el período de tiempo antes de una suscripción de extracción se agotó el tiempo por el servidor.
ms.openlocfilehash: 23b210dcdd87f2388aecec246068f12ec6c69a78
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840650"
---
# <a name="timeout-duration"></a><span data-ttu-id="7d76a-103">Tiempo de espera (duración)</span><span class="sxs-lookup"><span data-stu-id="7d76a-103">Timeout (duration)</span></span>

<span data-ttu-id="7d76a-104">El elemento de **tiempo de espera** especifica el período de tiempo antes de una suscripción de extracción se agotó el tiempo por el servidor.</span><span class="sxs-lookup"><span data-stu-id="7d76a-104">The **Timeout** element specifies the length of time before a pull subscription is timed out by the server.</span></span> 
  
```XML
<Timeout></Timeout>
```

 <span data-ttu-id="7d76a-105">**SubscriptionTimeoutType**</span><span class="sxs-lookup"><span data-stu-id="7d76a-105">**SubscriptionTimeoutType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7d76a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="7d76a-106">Attributes and elements</span></span>

<span data-ttu-id="7d76a-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="7d76a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7d76a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="7d76a-108">Attributes</span></span>

<span data-ttu-id="7d76a-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7d76a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7d76a-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7d76a-110">Child elements</span></span>

<span data-ttu-id="7d76a-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7d76a-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7d76a-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7d76a-112">Parent elements</span></span>

[<span data-ttu-id="7d76a-113">PullSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="7d76a-113">PullSubscriptionRequest</span></span>](pullsubscriptionrequest.md)
  
## <a name="text-value"></a><span data-ttu-id="7d76a-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="7d76a-114">Text value</span></span>

<span data-ttu-id="7d76a-115">El valor de texto del elemento de **tiempo de espera** es el período de tiempo, en minutos, antes de una suscripción de extracción se agotó el tiempo por el servidor.</span><span class="sxs-lookup"><span data-stu-id="7d76a-115">The text value of the **Timeout** element is the length of time, in minutes, before a pull subscription is timed out by the server.</span></span> <span data-ttu-id="7d76a-116">El valor mínimo es 1; el valor máximo es 1440.</span><span class="sxs-lookup"><span data-stu-id="7d76a-116">The minimum value is 1; the maximum value is 1440.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7d76a-117">Notas</span><span class="sxs-lookup"><span data-stu-id="7d76a-117">Remarks</span></span>

<span data-ttu-id="7d76a-118">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="7d76a-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="7d76a-119">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="7d76a-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7d76a-120">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7d76a-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7d76a-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7d76a-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7d76a-122">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="7d76a-122">Schema name</span></span>  <br/> |<span data-ttu-id="7d76a-123">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="7d76a-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="7d76a-124">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="7d76a-124">Validation file</span></span>  <br/> |<span data-ttu-id="7d76a-125">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7d76a-125">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7d76a-126">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="7d76a-126">Can be empty</span></span>  <br/> ||
   

