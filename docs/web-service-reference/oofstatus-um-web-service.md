---
title: OofStatus (servicio Web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- OofStatus
api_type:
- schema
ms.assetid: 0ba4225a-784e-4e6e-bd20-be45f0f7597c
description: El elemento OofStatus contiene un valor que indicaties el estado fuera de la oficina de mensajería unificada para el usuario que realiza una solicitud de GetUMProperties (servicio Web de mensajería unificada).
ms.openlocfilehash: 80b1d5aa508579eec14637ed10c322b5fbb670da
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460578"
---
# <a name="oofstatus-um-web-service"></a><span data-ttu-id="c4bec-103">OofStatus (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="c4bec-103">OofStatus (UM web service)</span></span>

<span data-ttu-id="c4bec-104">El elemento **OofStatus** contiene un valor que indicaties el estado fuera de la oficina de mensajería unificada para el usuario que realiza una solicitud de [GetUMProperties (servicio Web de mensajería unificada)](getumproperties-operation-um-web-service.md) .</span><span class="sxs-lookup"><span data-stu-id="c4bec-104">The **OofStatus** element contains a value that indicaties the Unified Messaging Out of Office status for the user who is making a [GetUMProperties operation (UM web service)](getumproperties-operation-um-web-service.md) request.</span></span> 
  
[<span data-ttu-id="c4bec-105">GetUMPropertiesResponse (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="c4bec-105">GetUMPropertiesResponse (UM web service)</span></span>](getumpropertiesresponse-um-web-service.md)
  
[<span data-ttu-id="c4bec-106">OofStatus (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="c4bec-106">OofStatus (UM web service)</span></span>](oofstatus-um-web-service.md)
  
```xml
<GetUMPropertiesResponse>
    <OofStatus/>
  <MissedCallNotificationEnabled/>
  <PlayOnPhoneDialString/>
  <TelephoneAccessNumbers/>
  <TelephoneAccessFolderEmail/>
</GetUMPropertiesResponse>
```

 <span data-ttu-id="c4bec-107">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="c4bec-107">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c4bec-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c4bec-108">Attributes and elements</span></span>

<span data-ttu-id="c4bec-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c4bec-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c4bec-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="c4bec-110">Attributes</span></span>

<span data-ttu-id="c4bec-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c4bec-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c4bec-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c4bec-112">Child elements</span></span>

<span data-ttu-id="c4bec-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c4bec-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c4bec-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c4bec-114">Parent elements</span></span>

|<span data-ttu-id="c4bec-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c4bec-115">**Element**</span></span>|<span data-ttu-id="c4bec-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c4bec-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c4bec-117">GetUMPropertiesResponse (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="c4bec-117">GetUMPropertiesResponse (UM web service)</span></span>](getumpropertiesresponse-um-web-service.md) <br/> |<span data-ttu-id="c4bec-118">Define una respuesta a una solicitud de [operación de GetUMProperties (servicio Web de mensajería unificada)](getumproperties-operation-um-web-service.md) .</span><span class="sxs-lookup"><span data-stu-id="c4bec-118">Defines a response to a [GetUMProperties operation (UM web service)](getumproperties-operation-um-web-service.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c4bec-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="c4bec-119">Text value</span></span>

<span data-ttu-id="c4bec-120">Se requiere un valor de texto booleano.</span><span class="sxs-lookup"><span data-stu-id="c4bec-120">A Boolean text value is required.</span></span> <span data-ttu-id="c4bec-121">Los valores posibles son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="c4bec-121">The following are the possible values:</span></span>
  
- <span data-ttu-id="c4bec-122">Verdadero</span><span class="sxs-lookup"><span data-stu-id="c4bec-122">True</span></span>
    
- <span data-ttu-id="c4bec-123">Falso</span><span class="sxs-lookup"><span data-stu-id="c4bec-123">False</span></span>
    
## <a name="element-information"></a><span data-ttu-id="c4bec-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c4bec-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c4bec-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="c4bec-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c4bec-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c4bec-126">Schema Name</span></span>  <br/> |<span data-ttu-id="c4bec-127">Mensajes</span><span class="sxs-lookup"><span data-stu-id="c4bec-127">Messages</span></span>  <br/> |
|<span data-ttu-id="c4bec-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c4bec-128">Validation File</span></span>  <br/> |<span data-ttu-id="c4bec-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="c4bec-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c4bec-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c4bec-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="c4bec-131">Falso</span><span class="sxs-lookup"><span data-stu-id="c4bec-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c4bec-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="c4bec-132">See also</span></span>



[<span data-ttu-id="c4bec-133">Operación GetUMProperties (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="c4bec-133">GetUMProperties operation (UM web service)</span></span>](getumproperties-operation-um-web-service.md)
  
[<span data-ttu-id="c4bec-134">GetUMPropertiesResponse (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="c4bec-134">GetUMPropertiesResponse (UM web service)</span></span>](getumpropertiesresponse-um-web-service.md)

