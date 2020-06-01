---
title: SetOofStatus (servicio Web de mensajería unificada)
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
description: El elemento SetOofStatus define una solicitud para establecer el estado fuera de la oficina de la mensajería unificada (OOF) del usuario que realiza la solicitud.
ms.openlocfilehash: 86e056a440e282cd444cfd405e452720b26b7456
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467070"
---
# <a name="setoofstatus-um-web-service"></a><span data-ttu-id="fc9e2-103">SetOofStatus (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="fc9e2-103">SetOofStatus (UM web service)</span></span>

<span data-ttu-id="fc9e2-104">El elemento **SetOofStatus** define una solicitud para establecer el estado fuera de la oficina de la mensajería unificada (OOF) del usuario que realiza la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fc9e2-104">The **SetOofStatus** element defines a request to set the Unified Messaging Out of Office (OOF) status for the user who makes the request.</span></span> 
  
[<span data-ttu-id="fc9e2-105">SetOofStatus (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="fc9e2-105">SetOofStatus (UM web service)</span></span>](setoofstatus-um-web-service.md)
  
```xml
<SetOofStatus>
  <status/>
</SetOofStatus>
```

 <span data-ttu-id="fc9e2-106">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="fc9e2-106">**Type**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fc9e2-107">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="fc9e2-107">Attributes and elements</span></span>

<span data-ttu-id="fc9e2-108">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="fc9e2-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fc9e2-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="fc9e2-109">Attributes</span></span>

<span data-ttu-id="fc9e2-110">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="fc9e2-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fc9e2-111">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="fc9e2-111">Child elements</span></span>

|<span data-ttu-id="fc9e2-112">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="fc9e2-112">**Element**</span></span>|<span data-ttu-id="fc9e2-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fc9e2-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fc9e2-114">Estado (servicio Web de mensajería unificada-SetOofStatus)</span><span class="sxs-lookup"><span data-stu-id="fc9e2-114">Status (UM web service - SetOofStatus)</span></span>](status-um-web-servicesetoofstatus.md) <br/> |<span data-ttu-id="fc9e2-115">Define un valor para usar en una solicitud de [operación de SetOofStatus (servicio Web de mensajería unificada)](setoofstatus-operation-um-web-service.md) .</span><span class="sxs-lookup"><span data-stu-id="fc9e2-115">Defines a value to use in a [SetOofStatus operation (UM web service)](setoofstatus-operation-um-web-service.md) request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="fc9e2-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="fc9e2-116">Parent elements</span></span>

<span data-ttu-id="fc9e2-117">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="fc9e2-117">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="fc9e2-118">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="fc9e2-118">Text value</span></span>

<span data-ttu-id="fc9e2-119">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="fc9e2-119">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fc9e2-120">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="fc9e2-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fc9e2-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="fc9e2-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="fc9e2-122">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="fc9e2-122">Schema Name</span></span>  <br/> |<span data-ttu-id="fc9e2-123">Mensajes</span><span class="sxs-lookup"><span data-stu-id="fc9e2-123">Messages</span></span>  <br/> |
|<span data-ttu-id="fc9e2-124">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="fc9e2-124">Validation File</span></span>  <br/> |<span data-ttu-id="fc9e2-125">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="fc9e2-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="fc9e2-126">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="fc9e2-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="fc9e2-127">Falso</span><span class="sxs-lookup"><span data-stu-id="fc9e2-127">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fc9e2-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="fc9e2-128">See also</span></span>



[<span data-ttu-id="fc9e2-129">Operación SetOofStatus (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="fc9e2-129">SetOofStatus operation (UM web service)</span></span>](setoofstatus-operation-um-web-service.md)
  
[<span data-ttu-id="fc9e2-130">Estado (servicio Web de mensajería unificada-SetOofStatus)</span><span class="sxs-lookup"><span data-stu-id="fc9e2-130">Status (UM web service - SetOofStatus)</span></span>](status-um-web-servicesetoofstatus.md)

