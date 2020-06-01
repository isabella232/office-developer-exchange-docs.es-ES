---
title: Estado (servicio Web de mensajería unificada-SetOofStatus)
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
description: El elemento status define el valor que se debe usar en una solicitud de operación SetOofStatus (servicio Web de mensajería unificada).
ms.openlocfilehash: 865152baf28c22578664e16db2dcd5f82a04af98
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459983"
---
# <a name="status-um-web-service---setoofstatus"></a><span data-ttu-id="54d2b-103">Estado (servicio Web de mensajería unificada-SetOofStatus)</span><span class="sxs-lookup"><span data-stu-id="54d2b-103">Status (UM web service - SetOofStatus)</span></span>

<span data-ttu-id="54d2b-104">El elemento **status** define el valor que se debe usar en una solicitud de [operación SetOofStatus (servicio Web de mensajería unificada)](setoofstatus-operation-um-web-service.md) .</span><span class="sxs-lookup"><span data-stu-id="54d2b-104">The **Status** element defines the value to use in a [SetOofStatus operation (UM web service)](setoofstatus-operation-um-web-service.md) request.</span></span> 
  
[<span data-ttu-id="54d2b-105">SetOofStatus (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="54d2b-105">SetOofStatus (UM web service)</span></span>](setoofstatus-um-web-service.md)
  
[<span data-ttu-id="54d2b-106">Estado (servicio Web de mensajería unificada-SetOofStatus)</span><span class="sxs-lookup"><span data-stu-id="54d2b-106">Status (UM web service - SetOofStatus)</span></span>](status-um-web-servicesetoofstatus.md)
  
```xml
<SetOofStatus>
  <status/>
</SetOofStatus>
```

 <span data-ttu-id="54d2b-107">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="54d2b-107">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="54d2b-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="54d2b-108">Attributes and elements</span></span>

<span data-ttu-id="54d2b-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="54d2b-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="54d2b-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="54d2b-110">Attributes</span></span>

<span data-ttu-id="54d2b-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="54d2b-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="54d2b-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="54d2b-112">Child elements</span></span>

<span data-ttu-id="54d2b-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="54d2b-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="54d2b-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="54d2b-114">Parent elements</span></span>

|<span data-ttu-id="54d2b-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="54d2b-115">**Element**</span></span>|<span data-ttu-id="54d2b-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="54d2b-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="54d2b-117">SetOofStatus (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="54d2b-117">SetOofStatus (UM web service)</span></span>](setoofstatus-um-web-service.md) <br/> |<span data-ttu-id="54d2b-118">Define una solicitud para establecer el estado fuera de la oficina de la mensajería unificada (OOF) del usuario que realiza la solicitud.</span><span class="sxs-lookup"><span data-stu-id="54d2b-118">Defines a request to set the Unified Messaging Out of Office (OOF) status for the user who makes the request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="54d2b-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="54d2b-119">Text value</span></span>

<span data-ttu-id="54d2b-120">Se requiere un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="54d2b-120">A Boolean value is required.</span></span> <span data-ttu-id="54d2b-121">Los valores posibles son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="54d2b-121">The following are the possible values:</span></span>
  
- <span data-ttu-id="54d2b-122">Verdadero</span><span class="sxs-lookup"><span data-stu-id="54d2b-122">True</span></span>
    
- <span data-ttu-id="54d2b-123">Falso</span><span class="sxs-lookup"><span data-stu-id="54d2b-123">False</span></span>
    
## <a name="element-information"></a><span data-ttu-id="54d2b-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="54d2b-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="54d2b-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="54d2b-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="54d2b-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="54d2b-126">Schema Name</span></span>  <br/> |<span data-ttu-id="54d2b-127">Mensajes</span><span class="sxs-lookup"><span data-stu-id="54d2b-127">Messages</span></span>  <br/> |
|<span data-ttu-id="54d2b-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="54d2b-128">Validation File</span></span>  <br/> |<span data-ttu-id="54d2b-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="54d2b-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="54d2b-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="54d2b-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="54d2b-131">Falso</span><span class="sxs-lookup"><span data-stu-id="54d2b-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="54d2b-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="54d2b-132">See also</span></span>



[<span data-ttu-id="54d2b-133">Operación SetOofStatus (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="54d2b-133">SetOofStatus operation (UM web service)</span></span>](setoofstatus-operation-um-web-service.md)

