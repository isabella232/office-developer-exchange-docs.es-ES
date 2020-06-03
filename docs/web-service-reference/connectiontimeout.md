---
title: ConnectionTimeout
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConnectionTimeout
api_type:
- schema
ms.assetid: 14da68a0-bcca-4281-a774-47644baa4ee9
description: El elemento ConnectionTimeout especifica el número de minutos que se va a mantener abierta una conexión.
ms.openlocfilehash: 671e3cf5466ee8b3543036811708bd7f54afdcce
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463856"
---
# <a name="connectiontimeout"></a><span data-ttu-id="6a7f0-103">ConnectionTimeout</span><span class="sxs-lookup"><span data-stu-id="6a7f0-103">ConnectionTimeout</span></span>

<span data-ttu-id="6a7f0-104">El elemento **ConnectionTimeout** especifica el número de minutos que se va a mantener abierta una conexión.</span><span class="sxs-lookup"><span data-stu-id="6a7f0-104">The **ConnectionTimeout** element specifies the number of minutes to keep a connection open.</span></span> 
  
[<span data-ttu-id="6a7f0-105">Operación GetStreamingEvents</span><span class="sxs-lookup"><span data-stu-id="6a7f0-105">GetStreamingEvents operation</span></span>](getstreamingevents-operation.md)
  
[<span data-ttu-id="6a7f0-106">ConnectionTimeout</span><span class="sxs-lookup"><span data-stu-id="6a7f0-106">ConnectionTimeout</span></span>](connectiontimeout.md)
  
```xml
<ConnectionTimeout/>
```

 <span data-ttu-id="6a7f0-107">**int**</span><span class="sxs-lookup"><span data-stu-id="6a7f0-107">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6a7f0-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="6a7f0-108">Attributes and elements</span></span>

<span data-ttu-id="6a7f0-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="6a7f0-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6a7f0-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="6a7f0-110">Attributes</span></span>

<span data-ttu-id="6a7f0-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="6a7f0-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6a7f0-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6a7f0-112">Child elements</span></span>

<span data-ttu-id="6a7f0-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="6a7f0-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6a7f0-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6a7f0-114">Parent elements</span></span>

|<span data-ttu-id="6a7f0-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6a7f0-115">**Element**</span></span>|<span data-ttu-id="6a7f0-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6a7f0-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6a7f0-117">GetStreamingEvents</span><span class="sxs-lookup"><span data-stu-id="6a7f0-117">GetStreamingEvents</span></span>](getstreamingevents.md) <br/> |<span data-ttu-id="6a7f0-118">Define una solicitud para obtener notificaciones de eventos de una conexión de transmisión por secuencias.</span><span class="sxs-lookup"><span data-stu-id="6a7f0-118">Defines a request to get event notifications from a streaming connection.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6a7f0-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="6a7f0-119">Text value</span></span>

<span data-ttu-id="6a7f0-120">El valor de texto representa un número entero que describe el número máximo de minutos que se debe mantener abierta una conexión de transmisión por secuencias.</span><span class="sxs-lookup"><span data-stu-id="6a7f0-120">The text value represents an integer that describes the maximum number of minutes to keep a streaming connection open.</span></span> <span data-ttu-id="6a7f0-121">El valor debe estar comprendido entre 1 y 30, ambos inclusive.</span><span class="sxs-lookup"><span data-stu-id="6a7f0-121">The value must be between 1 and 30, inclusive.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6a7f0-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6a7f0-122">Remarks</span></span>

<span data-ttu-id="6a7f0-123">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange. este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="6a7f0-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6a7f0-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="6a7f0-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6a7f0-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="6a7f0-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6a7f0-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="6a7f0-126">Schema name</span></span>  <br/> |<span data-ttu-id="6a7f0-127">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="6a7f0-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="6a7f0-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="6a7f0-128">Validation file</span></span>  <br/> |<span data-ttu-id="6a7f0-129">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="6a7f0-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6a7f0-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="6a7f0-130">Can be empty</span></span>  <br/> |<span data-ttu-id="6a7f0-131">Falso</span><span class="sxs-lookup"><span data-stu-id="6a7f0-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6a7f0-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="6a7f0-132">See also</span></span>



[<span data-ttu-id="6a7f0-133">Operación GetStreamingEvents</span><span class="sxs-lookup"><span data-stu-id="6a7f0-133">GetStreamingEvents operation</span></span>](getstreamingevents-operation.md)


- [<span data-ttu-id="6a7f0-134">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="6a7f0-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

