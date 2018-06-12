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
description: El elemento de ConnectionTimeout especifica el número de minutos que desea mantener una conexión abierta.
ms.openlocfilehash: 2bb40ba502853c70ef107c4c740fdfe7073abe31
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763775"
---
# <a name="connectiontimeout"></a><span data-ttu-id="a9a46-103">ConnectionTimeout</span><span class="sxs-lookup"><span data-stu-id="a9a46-103">ConnectionTimeout</span></span>

<span data-ttu-id="a9a46-104">El elemento de **ConnectionTimeout** especifica el número de minutos que desea mantener una conexión abierta.</span><span class="sxs-lookup"><span data-stu-id="a9a46-104">The **ConnectionTimeout** element specifies the number of minutes to keep a connection open.</span></span> 
  
[<span data-ttu-id="a9a46-105">Operación GetStreamingEvents</span><span class="sxs-lookup"><span data-stu-id="a9a46-105">GetStreamingEvents operation</span></span>](getstreamingevents-operation.md)
  
[<span data-ttu-id="a9a46-106">ConnectionTimeout</span><span class="sxs-lookup"><span data-stu-id="a9a46-106">ConnectionTimeout</span></span>](connectiontimeout.md)
  
```xml
<ConnectionTimeout/>
```

 <span data-ttu-id="a9a46-107">**int**</span><span class="sxs-lookup"><span data-stu-id="a9a46-107">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a9a46-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a9a46-108">Attributes and elements</span></span>

<span data-ttu-id="a9a46-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a9a46-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a9a46-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="a9a46-110">Attributes</span></span>

<span data-ttu-id="a9a46-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a9a46-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a9a46-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a9a46-112">Child elements</span></span>

<span data-ttu-id="a9a46-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a9a46-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a9a46-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a9a46-114">Parent elements</span></span>

|<span data-ttu-id="a9a46-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="a9a46-115">**Element**</span></span>|<span data-ttu-id="a9a46-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a9a46-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a9a46-117">GetStreamingEvents</span><span class="sxs-lookup"><span data-stu-id="a9a46-117">GetStreamingEvents</span></span>](getstreamingevents.md) <br/> |<span data-ttu-id="a9a46-118">Define una solicitud para obtener las notificaciones de eventos de una conexión de transmisión por secuencias.</span><span class="sxs-lookup"><span data-stu-id="a9a46-118">Defines a request to get event notifications from a streaming connection.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a9a46-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="a9a46-119">Text value</span></span>

<span data-ttu-id="a9a46-120">El valor de texto representa un número entero que describe el número máximo de minutos que desea mantener abierta una conexión de transmisión por secuencias.</span><span class="sxs-lookup"><span data-stu-id="a9a46-120">The text value represents an integer that describes the maximum number of minutes to keep a streaming connection open.</span></span> <span data-ttu-id="a9a46-121">El valor debe ser entre 1 y 30, ambos inclusive.</span><span class="sxs-lookup"><span data-stu-id="a9a46-121">The value must be between 1 and 30, inclusive.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a9a46-122">Notas</span><span class="sxs-lookup"><span data-stu-id="a9a46-122">Remarks</span></span>

<span data-ttu-id="a9a46-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda Exchange Web Services.This elemento fue introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="a9a46-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a9a46-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a9a46-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a9a46-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a9a46-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a9a46-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a9a46-126">Schema name</span></span>  <br/> |<span data-ttu-id="a9a46-127">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="a9a46-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="a9a46-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a9a46-128">Validation file</span></span>  <br/> |<span data-ttu-id="a9a46-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a9a46-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a9a46-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a9a46-130">Can be empty</span></span>  <br/> |<span data-ttu-id="a9a46-131">False</span><span class="sxs-lookup"><span data-stu-id="a9a46-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a9a46-132">Ver también</span><span class="sxs-lookup"><span data-stu-id="a9a46-132">See also</span></span>



[<span data-ttu-id="a9a46-133">Operación GetStreamingEvents</span><span class="sxs-lookup"><span data-stu-id="a9a46-133">GetStreamingEvents operation</span></span>](getstreamingevents-operation.md)


- [<span data-ttu-id="a9a46-134">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="a9a46-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

