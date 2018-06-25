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
description: El elemento UnifiedMessagingConfiguration contiene información de configuración de servicio para el servicio de mensajería unificada.
ms.openlocfilehash: 3ad8f66ecdf21062c00c2a6ac6f65fac875da38c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840757"
---
# <a name="unifiedmessagingconfiguration"></a><span data-ttu-id="40def-103">UnifiedMessagingConfiguration</span><span class="sxs-lookup"><span data-stu-id="40def-103">UnifiedMessagingConfiguration</span></span>

<span data-ttu-id="40def-104">El elemento **UnifiedMessagingConfiguration** contiene información de configuración de servicio para el servicio de mensajería unificada.</span><span class="sxs-lookup"><span data-stu-id="40def-104">The **UnifiedMessagingConfiguration** element contains service configuration information for the Unified Messaging service.</span></span> 
  
```XML
<UnifiedMessagingConfiguration>
   <UmEnabled/>
   <PlayOnPhoneDialString/>
   <PlayOnPhoneEnabled/>
</UnifiedMessagingConfiguration>
```

 <span data-ttu-id="40def-105">**UnifiedMessageServiceConfiguration**</span><span class="sxs-lookup"><span data-stu-id="40def-105">**UnifiedMessageServiceConfiguration**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="40def-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="40def-106">Attributes and elements</span></span>

<span data-ttu-id="40def-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="40def-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="40def-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="40def-108">Attributes</span></span>

<span data-ttu-id="40def-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="40def-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="40def-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="40def-110">Child elements</span></span>

|<span data-ttu-id="40def-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="40def-111">**Element**</span></span>|<span data-ttu-id="40def-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="40def-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="40def-113">UmEnabled</span><span class="sxs-lookup"><span data-stu-id="40def-113">UmEnabled</span></span>](umenabled.md) <br/> |<span data-ttu-id="40def-114">Indica si está habilitada la mensajería unificada para una cuenta.</span><span class="sxs-lookup"><span data-stu-id="40def-114">Indicates whether Unified Messaging is enabled for an account.</span></span> <span data-ttu-id="40def-115">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="40def-115">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="40def-116">PlayOnPhoneDialString (servicios Web de Exchange)</span><span class="sxs-lookup"><span data-stu-id="40def-116">PlayOnPhoneDialString (Exchange Web Services)</span></span>](playonphonedialstring-exchange-web-services.md) <br/> |<span data-ttu-id="40def-117">Identifica la cadena de marcado de reproducir en teléfono.</span><span class="sxs-lookup"><span data-stu-id="40def-117">Identifies the Play-on-Phone dial string.</span></span> <span data-ttu-id="40def-118">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="40def-118">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="40def-119">PlayOnPhoneEnabled</span><span class="sxs-lookup"><span data-stu-id="40def-119">PlayOnPhoneEnabled</span></span>](playonphoneenabled.md) <br/> |<span data-ttu-id="40def-120">Indica si está habilitada la característica Reproducir en teléfono.</span><span class="sxs-lookup"><span data-stu-id="40def-120">Indicates whether the Play-on-Phone feature is enabled.</span></span> <span data-ttu-id="40def-121">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="40def-121">This element is required.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="40def-122">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="40def-122">Parent elements</span></span>

|<span data-ttu-id="40def-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="40def-123">**Element**</span></span>|<span data-ttu-id="40def-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="40def-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="40def-125">ServiceConfigurationResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="40def-125">ServiceConfigurationResponseMessageType</span></span>](serviceconfigurationresponsemessagetype.md) <br/> |<span data-ttu-id="40def-126">Contiene la configuración del servicio.</span><span class="sxs-lookup"><span data-stu-id="40def-126">Contains service configuration settings.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="40def-127">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="40def-127">Text value</span></span>

<span data-ttu-id="40def-128">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="40def-128">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="40def-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="40def-129">Remarks</span></span>

<span data-ttu-id="40def-130">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="40def-130">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="40def-131">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="40def-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="40def-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="40def-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="40def-133">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="40def-133">Schema Name</span></span>  <br/> |<span data-ttu-id="40def-134">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="40def-134">Messages schema</span></span>  <br/> |
|<span data-ttu-id="40def-135">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="40def-135">Validation File</span></span>  <br/> |<span data-ttu-id="40def-136">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="40def-136">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="40def-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="40def-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="40def-138">False</span><span class="sxs-lookup"><span data-stu-id="40def-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="40def-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="40def-139">See also</span></span>



- [<span data-ttu-id="40def-140">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="40def-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

