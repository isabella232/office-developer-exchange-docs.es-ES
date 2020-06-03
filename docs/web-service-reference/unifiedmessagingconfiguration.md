---
title: UnifiedMessagingConfiguration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UnifiedMessagingConfiguration
api_type:
- schema
ms.assetid: cbdb4268-077e-44ed-8ec2-9d759c84cc6d
description: El elemento UnifiedMessagingConfiguration contiene información de configuración del servicio para el servicio de mensajería unificada.
ms.openlocfilehash: 3f9f4ed65721929c552615c07e2239f48ef837f3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528695"
---
# <a name="unifiedmessagingconfiguration"></a><span data-ttu-id="25ec4-103">UnifiedMessagingConfiguration</span><span class="sxs-lookup"><span data-stu-id="25ec4-103">UnifiedMessagingConfiguration</span></span>

<span data-ttu-id="25ec4-104">El elemento **UnifiedMessagingConfiguration** contiene información de configuración del servicio para el servicio de mensajería unificada.</span><span class="sxs-lookup"><span data-stu-id="25ec4-104">The **UnifiedMessagingConfiguration** element contains service configuration information for the Unified Messaging service.</span></span> 
  
```XML
<UnifiedMessagingConfiguration>
   <UmEnabled/>
   <PlayOnPhoneDialString/>
   <PlayOnPhoneEnabled/>
</UnifiedMessagingConfiguration>
```

 <span data-ttu-id="25ec4-105">**UnifiedMessageServiceConfiguration**</span><span class="sxs-lookup"><span data-stu-id="25ec4-105">**UnifiedMessageServiceConfiguration**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="25ec4-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="25ec4-106">Attributes and elements</span></span>

<span data-ttu-id="25ec4-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="25ec4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="25ec4-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="25ec4-108">Attributes</span></span>

<span data-ttu-id="25ec4-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="25ec4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="25ec4-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="25ec4-110">Child elements</span></span>

|<span data-ttu-id="25ec4-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="25ec4-111">**Element**</span></span>|<span data-ttu-id="25ec4-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="25ec4-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="25ec4-113">UmEnabled</span><span class="sxs-lookup"><span data-stu-id="25ec4-113">UmEnabled</span></span>](umenabled.md) <br/> |<span data-ttu-id="25ec4-114">Indica si la mensajería unificada está habilitada para una cuenta.</span><span class="sxs-lookup"><span data-stu-id="25ec4-114">Indicates whether Unified Messaging is enabled for an account.</span></span> <span data-ttu-id="25ec4-115">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="25ec4-115">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="25ec4-116">PlayOnPhoneDialString (servicios web Exchange)</span><span class="sxs-lookup"><span data-stu-id="25ec4-116">PlayOnPhoneDialString (Exchange Web Services)</span></span>](playonphonedialstring-exchange-web-services.md) <br/> |<span data-ttu-id="25ec4-117">Identifica la cadena de marcado de reproducción en teléfono.</span><span class="sxs-lookup"><span data-stu-id="25ec4-117">Identifies the Play-on-Phone dial string.</span></span> <span data-ttu-id="25ec4-118">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="25ec4-118">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="25ec4-119">PlayOnPhoneEnabled</span><span class="sxs-lookup"><span data-stu-id="25ec4-119">PlayOnPhoneEnabled</span></span>](playonphoneenabled.md) <br/> |<span data-ttu-id="25ec4-120">Indica si está habilitada la característica de reproducción en teléfono.</span><span class="sxs-lookup"><span data-stu-id="25ec4-120">Indicates whether the Play-on-Phone feature is enabled.</span></span> <span data-ttu-id="25ec4-121">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="25ec4-121">This element is required.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="25ec4-122">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="25ec4-122">Parent elements</span></span>

|<span data-ttu-id="25ec4-123">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="25ec4-123">**Element**</span></span>|<span data-ttu-id="25ec4-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="25ec4-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="25ec4-125">ServiceConfigurationResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="25ec4-125">ServiceConfigurationResponseMessageType</span></span>](serviceconfigurationresponsemessagetype.md) <br/> |<span data-ttu-id="25ec4-126">Contiene las opciones de configuración del servicio.</span><span class="sxs-lookup"><span data-stu-id="25ec4-126">Contains service configuration settings.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="25ec4-127">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="25ec4-127">Text value</span></span>

<span data-ttu-id="25ec4-128">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="25ec4-128">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="25ec4-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="25ec4-129">Remarks</span></span>

<span data-ttu-id="25ec4-130">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="25ec4-130">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="25ec4-131">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="25ec4-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="25ec4-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="25ec4-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="25ec4-133">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="25ec4-133">Schema Name</span></span>  <br/> |<span data-ttu-id="25ec4-134">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="25ec4-134">Messages schema</span></span>  <br/> |
|<span data-ttu-id="25ec4-135">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="25ec4-135">Validation File</span></span>  <br/> |<span data-ttu-id="25ec4-136">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="25ec4-136">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="25ec4-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="25ec4-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="25ec4-138">Falso</span><span class="sxs-lookup"><span data-stu-id="25ec4-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="25ec4-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="25ec4-139">See also</span></span>



- [<span data-ttu-id="25ec4-140">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="25ec4-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

