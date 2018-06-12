---
title: ConfigurationName
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConfigurationName
api_type:
- schema
ms.assetid: 3b524a2f-9c6b-4550-9f3d-f78d176b0f7b
description: El elemento ConfigurationName especifica las configuraciones de servicio solicitado por su nombre.
ms.openlocfilehash: a03a0bc0ab7ecbc1c2aec31f864503ee0f560908
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763767"
---
# <a name="configurationname"></a><span data-ttu-id="3185d-103">ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="3185d-103">ConfigurationName</span></span>

<span data-ttu-id="3185d-104">El elemento **ConfigurationName** especifica las configuraciones de servicio solicitado por su nombre.</span><span class="sxs-lookup"><span data-stu-id="3185d-104">The **ConfigurationName** element specifies the requested service configurations by name.</span></span> 
  
```xml
<ConfigurationName>MailTips or UnifiedMessagingConfiguration or ProtectionRules</ConfigurationName>
```

 <span data-ttu-id="3185d-105">**ServiceConfigurationType**</span><span class="sxs-lookup"><span data-stu-id="3185d-105">**ServiceConfigurationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3185d-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3185d-106">Attributes and elements</span></span>

<span data-ttu-id="3185d-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3185d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3185d-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="3185d-108">Attributes</span></span>

<span data-ttu-id="3185d-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3185d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3185d-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3185d-110">Child elements</span></span>

<span data-ttu-id="3185d-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3185d-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3185d-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3185d-112">Parent elements</span></span>

|<span data-ttu-id="3185d-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="3185d-113">**Element**</span></span>|<span data-ttu-id="3185d-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3185d-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3185d-115">RequestedConfiguration</span><span class="sxs-lookup"><span data-stu-id="3185d-115">RequestedConfiguration</span></span>](requestedconfiguration.md) <br/> |<span data-ttu-id="3185d-116">Contiene las configuraciones del servicio solicitado.</span><span class="sxs-lookup"><span data-stu-id="3185d-116">Contains the requested service configurations.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3185d-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="3185d-117">Text value</span></span>

<span data-ttu-id="3185d-118">En la siguiente tabla se enumera los valores posibles para el elemento **ConfigurationName** .</span><span class="sxs-lookup"><span data-stu-id="3185d-118">The following table lists the possible values for the **ConfigurationName** element.</span></span> 
  
<span data-ttu-id="3185d-119">**Valores de elemento ConfigurationName**</span><span class="sxs-lookup"><span data-stu-id="3185d-119">**ConfigurationName element values**</span></span>

|<span data-ttu-id="3185d-120">**Valor**</span><span class="sxs-lookup"><span data-stu-id="3185d-120">**Value**</span></span>|<span data-ttu-id="3185d-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3185d-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3185d-122">Sugerencias de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="3185d-122">MailTips</span></span>  <br/> |<span data-ttu-id="3185d-123">Identifica la configuración del servicio de sugerencias de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="3185d-123">Identifies the MailTips service configuration.</span></span>  <br/> |
|<span data-ttu-id="3185d-124">UnifiedMessagingConfiguration</span><span class="sxs-lookup"><span data-stu-id="3185d-124">UnifiedMessagingConfiguration</span></span>  <br/> |<span data-ttu-id="3185d-125">Identifica la configuración del servicio de mensajería unificada.</span><span class="sxs-lookup"><span data-stu-id="3185d-125">Identifies the Unified Messaging service configuration.</span></span>  <br/> |
|<span data-ttu-id="3185d-126">ProtectionRules</span><span class="sxs-lookup"><span data-stu-id="3185d-126">ProtectionRules</span></span>  <br/> |<span data-ttu-id="3185d-127">Identifica la configuración del servicio de las reglas de protección.</span><span class="sxs-lookup"><span data-stu-id="3185d-127">Identifies the Protection Rules service configuration.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3185d-128">Notas</span><span class="sxs-lookup"><span data-stu-id="3185d-128">Remarks</span></span>

<span data-ttu-id="3185d-129">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="3185d-129">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3185d-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3185d-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3185d-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3185d-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3185d-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3185d-132">Schema Name</span></span>  <br/> |<span data-ttu-id="3185d-133">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="3185d-133">Messages schema</span></span>  <br/> |
|<span data-ttu-id="3185d-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3185d-134">Validation File</span></span>  <br/> |<span data-ttu-id="3185d-135">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="3185d-135">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3185d-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3185d-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="3185d-137">False</span><span class="sxs-lookup"><span data-stu-id="3185d-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3185d-138">Ver también</span><span class="sxs-lookup"><span data-stu-id="3185d-138">See also</span></span>



- [<span data-ttu-id="3185d-139">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="3185d-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

