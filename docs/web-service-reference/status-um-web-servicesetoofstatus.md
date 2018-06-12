---
title: Estado (servicio web de mensajería unificada - SetOofStatus)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- Status
api_type:
- schema
ms.assetid: 893bcff1-ccdc-493f-b366-ce8a68c813bd
description: El elemento Status define el valor que se utilizará en una solicitud de SetOofStatus operación (servicio web de mensajería unificada).
ms.openlocfilehash: 57b4f8fe1a64341b1c2ae0a06bc98f1c9cfd28c4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837583"
---
# <a name="status-um-web-service---setoofstatus"></a><span data-ttu-id="d16aa-103">Estado (servicio web de mensajería unificada - SetOofStatus)</span><span class="sxs-lookup"><span data-stu-id="d16aa-103">Status (UM web service - SetOofStatus)</span></span>

<span data-ttu-id="d16aa-104">El elemento **Status** define el valor que se utilizará en una solicitud de [operación SetOofStatus (servicio web de mensajería unificada)](setoofstatus-operation-um-web-service.md) .</span><span class="sxs-lookup"><span data-stu-id="d16aa-104">The **Status** element defines the value to use in a [SetOofStatus operation (UM web service)](setoofstatus-operation-um-web-service.md) request.</span></span> 
  
[<span data-ttu-id="d16aa-105">SetOofStatus (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="d16aa-105">SetOofStatus (UM web service)</span></span>](setoofstatus-um-web-service.md)
  
[<span data-ttu-id="d16aa-106">Estado (servicio web de mensajería unificada - SetOofStatus)</span><span class="sxs-lookup"><span data-stu-id="d16aa-106">Status (UM web service - SetOofStatus)</span></span>](status-um-web-servicesetoofstatus.md)
  
```xml
<SetOofStatus>
  <status/>
</SetOofStatus>
```

 <span data-ttu-id="d16aa-107">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="d16aa-107">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d16aa-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d16aa-108">Attributes and elements</span></span>

<span data-ttu-id="d16aa-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d16aa-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d16aa-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="d16aa-110">Attributes</span></span>

<span data-ttu-id="d16aa-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d16aa-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d16aa-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d16aa-112">Child elements</span></span>

<span data-ttu-id="d16aa-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d16aa-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d16aa-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d16aa-114">Parent elements</span></span>

|<span data-ttu-id="d16aa-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="d16aa-115">**Element**</span></span>|<span data-ttu-id="d16aa-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d16aa-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d16aa-117">SetOofStatus (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="d16aa-117">SetOofStatus (UM web service)</span></span>](setoofstatus-um-web-service.md) <br/> |<span data-ttu-id="d16aa-118">Define una solicitud para establecer el estado de Unified Messaging fuera de oficina (OOF) del usuario que realiza la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d16aa-118">Defines a request to set the Unified Messaging Out of Office (OOF) status for the user who makes the request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d16aa-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="d16aa-119">Text value</span></span>

<span data-ttu-id="d16aa-120">Es necesario un valor Boolean.</span><span class="sxs-lookup"><span data-stu-id="d16aa-120">A Boolean value is required.</span></span> <span data-ttu-id="d16aa-121">Los valores posibles son:</span><span class="sxs-lookup"><span data-stu-id="d16aa-121">The following are the possible values:</span></span>
  
- <span data-ttu-id="d16aa-122">Verdadero</span><span class="sxs-lookup"><span data-stu-id="d16aa-122">True</span></span>
    
- <span data-ttu-id="d16aa-123">False</span><span class="sxs-lookup"><span data-stu-id="d16aa-123">False</span></span>
    
## <a name="element-information"></a><span data-ttu-id="d16aa-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d16aa-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d16aa-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d16aa-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d16aa-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d16aa-126">Schema Name</span></span>  <br/> |<span data-ttu-id="d16aa-127">Mensajes</span><span class="sxs-lookup"><span data-stu-id="d16aa-127">Messages</span></span>  <br/> |
|<span data-ttu-id="d16aa-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d16aa-128">Validation File</span></span>  <br/> |<span data-ttu-id="d16aa-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="d16aa-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d16aa-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d16aa-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="d16aa-131">False</span><span class="sxs-lookup"><span data-stu-id="d16aa-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d16aa-132">Ver también</span><span class="sxs-lookup"><span data-stu-id="d16aa-132">See also</span></span>



[<span data-ttu-id="d16aa-133">Operación SetOofStatus (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="d16aa-133">SetOofStatus operation (UM web service)</span></span>](setoofstatus-operation-um-web-service.md)

