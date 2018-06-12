---
title: SetOofStatus (servicio web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- SetOofStatus
api_type:
- schema
ms.assetid: 9fc0ea9c-7a98-4fd7-a90c-cf5639c63a3a
description: El elemento SetOofStatus define una solicitud para establecer el estado de Unified Messaging fuera de oficina (OOF) del usuario que realiza la solicitud.
ms.openlocfilehash: df28c98013e1d5c00ea120ce1aa342e9fc2c6f31
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837447"
---
# <a name="setoofstatus-um-web-service"></a><span data-ttu-id="31609-103">SetOofStatus (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="31609-103">SetOofStatus (UM web service)</span></span>

<span data-ttu-id="31609-104">El elemento **SetOofStatus** define una solicitud para establecer el estado de Unified Messaging fuera de oficina (OOF) del usuario que realiza la solicitud.</span><span class="sxs-lookup"><span data-stu-id="31609-104">The **SetOofStatus** element defines a request to set the Unified Messaging Out of Office (OOF) status for the user who makes the request.</span></span> 
  
[<span data-ttu-id="31609-105">SetOofStatus (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="31609-105">SetOofStatus (UM web service)</span></span>](setoofstatus-um-web-service.md)
  
```xml
<SetOofStatus>
  <status/>
</SetOofStatus>
```

 <span data-ttu-id="31609-106">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="31609-106">**Type**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="31609-107">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="31609-107">Attributes and elements</span></span>

<span data-ttu-id="31609-108">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="31609-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="31609-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="31609-109">Attributes</span></span>

<span data-ttu-id="31609-110">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="31609-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="31609-111">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="31609-111">Child elements</span></span>

|<span data-ttu-id="31609-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="31609-112">**Element**</span></span>|<span data-ttu-id="31609-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="31609-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="31609-114">Estado (servicio web de mensajería unificada - SetOofStatus)</span><span class="sxs-lookup"><span data-stu-id="31609-114">Status (UM web service - SetOofStatus)</span></span>](status-um-web-servicesetoofstatus.md) <br/> |<span data-ttu-id="31609-115">Define un valor para usar en una solicitud de [operación SetOofStatus (servicio web de mensajería unificada)](setoofstatus-operation-um-web-service.md) .</span><span class="sxs-lookup"><span data-stu-id="31609-115">Defines a value to use in a [SetOofStatus operation (UM web service)](setoofstatus-operation-um-web-service.md) request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="31609-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="31609-116">Parent elements</span></span>

<span data-ttu-id="31609-117">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="31609-117">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="31609-118">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="31609-118">Text value</span></span>

<span data-ttu-id="31609-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="31609-119">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="31609-120">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="31609-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="31609-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="31609-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="31609-122">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="31609-122">Schema Name</span></span>  <br/> |<span data-ttu-id="31609-123">Mensajes</span><span class="sxs-lookup"><span data-stu-id="31609-123">Messages</span></span>  <br/> |
|<span data-ttu-id="31609-124">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="31609-124">Validation File</span></span>  <br/> |<span data-ttu-id="31609-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="31609-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="31609-126">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="31609-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="31609-127">False</span><span class="sxs-lookup"><span data-stu-id="31609-127">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="31609-128">Ver también</span><span class="sxs-lookup"><span data-stu-id="31609-128">See also</span></span>



[<span data-ttu-id="31609-129">Operación SetOofStatus (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="31609-129">SetOofStatus operation (UM web service)</span></span>](setoofstatus-operation-um-web-service.md)
  
[<span data-ttu-id="31609-130">Estado (servicio web de mensajería unificada - SetOofStatus)</span><span class="sxs-lookup"><span data-stu-id="31609-130">Status (UM web service - SetOofStatus)</span></span>](status-um-web-servicesetoofstatus.md)

