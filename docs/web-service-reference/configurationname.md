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
description: El elemento ConfigurationName especifica las configuraciones de servicio solicitadas por nombre.
ms.openlocfilehash: 5e1216253a633af643dbd276827842dbe2db5d5f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463926"
---
# <a name="configurationname"></a><span data-ttu-id="b7aec-103">ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="b7aec-103">ConfigurationName</span></span>

<span data-ttu-id="b7aec-104">El elemento **ConfigurationName** especifica las configuraciones de servicio solicitadas por nombre.</span><span class="sxs-lookup"><span data-stu-id="b7aec-104">The **ConfigurationName** element specifies the requested service configurations by name.</span></span> 
  
```xml
<ConfigurationName>MailTips or UnifiedMessagingConfiguration or ProtectionRules</ConfigurationName>
```

 <span data-ttu-id="b7aec-105">**ServiceConfigurationType**</span><span class="sxs-lookup"><span data-stu-id="b7aec-105">**ServiceConfigurationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b7aec-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b7aec-106">Attributes and elements</span></span>

<span data-ttu-id="b7aec-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b7aec-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b7aec-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="b7aec-108">Attributes</span></span>

<span data-ttu-id="b7aec-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="b7aec-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b7aec-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b7aec-110">Child elements</span></span>

<span data-ttu-id="b7aec-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="b7aec-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b7aec-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b7aec-112">Parent elements</span></span>

|<span data-ttu-id="b7aec-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b7aec-113">**Element**</span></span>|<span data-ttu-id="b7aec-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b7aec-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b7aec-115">RequestedConfiguration</span><span class="sxs-lookup"><span data-stu-id="b7aec-115">RequestedConfiguration</span></span>](requestedconfiguration.md) <br/> |<span data-ttu-id="b7aec-116">Contiene las configuraciones de servicio solicitadas.</span><span class="sxs-lookup"><span data-stu-id="b7aec-116">Contains the requested service configurations.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b7aec-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="b7aec-117">Text value</span></span>

<span data-ttu-id="b7aec-118">En la siguiente tabla se enumeran los valores posibles para el elemento **ConfigurationName** .</span><span class="sxs-lookup"><span data-stu-id="b7aec-118">The following table lists the possible values for the **ConfigurationName** element.</span></span> 
  
<span data-ttu-id="b7aec-119">**Valores del elemento ConfigurationName**</span><span class="sxs-lookup"><span data-stu-id="b7aec-119">**ConfigurationName element values**</span></span>

|<span data-ttu-id="b7aec-120">**Valor**</span><span class="sxs-lookup"><span data-stu-id="b7aec-120">**Value**</span></span>|<span data-ttu-id="b7aec-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b7aec-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b7aec-122">MailTips</span><span class="sxs-lookup"><span data-stu-id="b7aec-122">MailTips</span></span>  <br/> |<span data-ttu-id="b7aec-123">Identifica la configuración del servicio de sugerencias de correo.</span><span class="sxs-lookup"><span data-stu-id="b7aec-123">Identifies the MailTips service configuration.</span></span>  <br/> |
|<span data-ttu-id="b7aec-124">UnifiedMessagingConfiguration</span><span class="sxs-lookup"><span data-stu-id="b7aec-124">UnifiedMessagingConfiguration</span></span>  <br/> |<span data-ttu-id="b7aec-125">Identifica la configuración del servicio de mensajería unificada.</span><span class="sxs-lookup"><span data-stu-id="b7aec-125">Identifies the Unified Messaging service configuration.</span></span>  <br/> |
|<span data-ttu-id="b7aec-126">ProtectionRules</span><span class="sxs-lookup"><span data-stu-id="b7aec-126">ProtectionRules</span></span>  <br/> |<span data-ttu-id="b7aec-127">Identifica la configuración del servicio de reglas de protección.</span><span class="sxs-lookup"><span data-stu-id="b7aec-127">Identifies the Protection Rules service configuration.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b7aec-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b7aec-128">Remarks</span></span>

<span data-ttu-id="b7aec-129">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="b7aec-129">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b7aec-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b7aec-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b7aec-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="b7aec-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b7aec-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b7aec-132">Schema Name</span></span>  <br/> |<span data-ttu-id="b7aec-133">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="b7aec-133">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b7aec-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b7aec-134">Validation File</span></span>  <br/> |<span data-ttu-id="b7aec-135">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="b7aec-135">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b7aec-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b7aec-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="b7aec-137">Falso</span><span class="sxs-lookup"><span data-stu-id="b7aec-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b7aec-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="b7aec-138">See also</span></span>



- [<span data-ttu-id="b7aec-139">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="b7aec-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

