---
title: ProtectionRulesConfiguration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ProtectionRulesConfiguration
api_type:
- schema
ms.assetid: e5b4699a-476e-4053-bb52-873eb921c046
description: El elemento ProtectionRulesConfiguration contiene información de configuración de servicio para el servicio de protección de las reglas.
ms.openlocfilehash: 9c286fcf9752d591d53323f45a264f4bdd078c1c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836912"
---
# <a name="protectionrulesconfiguration"></a><span data-ttu-id="98f74-103">ProtectionRulesConfiguration</span><span class="sxs-lookup"><span data-stu-id="98f74-103">ProtectionRulesConfiguration</span></span>

<span data-ttu-id="98f74-104">El elemento **ProtectionRulesConfiguration** contiene información de configuración de servicio para el servicio de protección de las reglas.</span><span class="sxs-lookup"><span data-stu-id="98f74-104">The **ProtectionRulesConfiguration** element contains service configuration information for the protection rules service.</span></span> 
  
```XML
<ProtectionRulesConfiguration RefreshInterval="">
   <Rules/>
   <InternalDomains/>
</ProtectionRulesConfiguration>
```

 <span data-ttu-id="98f74-105">**ProtectionRulesServiceConfiguration**</span><span class="sxs-lookup"><span data-stu-id="98f74-105">**ProtectionRulesServiceConfiguration**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="98f74-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="98f74-106">Attributes and elements</span></span>

<span data-ttu-id="98f74-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="98f74-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="98f74-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="98f74-108">Attributes</span></span>

|<span data-ttu-id="98f74-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="98f74-109">**Attribute**</span></span>|<span data-ttu-id="98f74-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="98f74-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="98f74-111">**RefreshInterval**</span><span class="sxs-lookup"><span data-stu-id="98f74-111">**RefreshInterval**</span></span> <br/> |<span data-ttu-id="98f74-112">Especifica la frecuencia, en horas completas, el cliente debería solicitar las reglas de protección desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="98f74-112">Specifies how often, in whole hours, the client should request protection rules from the server.</span></span> <span data-ttu-id="98f74-113">Este atributo es necesario y su valor debe ser un entero que es igual o mayor que 1.</span><span class="sxs-lookup"><span data-stu-id="98f74-113">This attribute is required and its value must be an integer that is equal to or greater than 1.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="98f74-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="98f74-114">Child elements</span></span>

|<span data-ttu-id="98f74-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="98f74-115">**Element**</span></span>|<span data-ttu-id="98f74-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="98f74-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="98f74-117">Reglas</span><span class="sxs-lookup"><span data-stu-id="98f74-117">Rules </span></span>](rules-ex15websvcsotherref.md) <br/> |<span data-ttu-id="98f74-118">Una matriz de las reglas de protección.</span><span class="sxs-lookup"><span data-stu-id="98f74-118">An array of protection rules.</span></span> <span data-ttu-id="98f74-119">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="98f74-119">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="98f74-120">InternalDomains (SmtpDomainList)</span><span class="sxs-lookup"><span data-stu-id="98f74-120">InternalDomains (SmtpDomainList)</span></span>](internaldomains-smtpdomainlist.md) <br/> |<span data-ttu-id="98f74-121">Identifica la lista de dominios SMTP internos de la organización.</span><span class="sxs-lookup"><span data-stu-id="98f74-121">Identifies the list of internal SMTP domains of the organization.</span></span> <span data-ttu-id="98f74-122">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="98f74-122">This element is required.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="98f74-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="98f74-123">Parent elements</span></span>

|<span data-ttu-id="98f74-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="98f74-124">**Element**</span></span>|<span data-ttu-id="98f74-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="98f74-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="98f74-126">ServiceConfigurationResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="98f74-126">ServiceConfigurationResponseMessageType</span></span>](serviceconfigurationresponsemessagetype.md) <br/> |<span data-ttu-id="98f74-127">Contiene la configuración del servicio.</span><span class="sxs-lookup"><span data-stu-id="98f74-127">Contains service configuration settings.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="98f74-128">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="98f74-128">Text value</span></span>

<span data-ttu-id="98f74-129">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="98f74-129">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="98f74-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="98f74-130">Remarks</span></span>

<span data-ttu-id="98f74-131">La configuración del servicio de las reglas de protección está formada por una lista de reglas, dominios internos y un intervalo de actualización.</span><span class="sxs-lookup"><span data-stu-id="98f74-131">The protection rules service configuration is comprised of a list of rules, internal domains, and a refresh interval.</span></span>
  
<span data-ttu-id="98f74-132">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="98f74-132">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="98f74-133">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="98f74-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="98f74-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="98f74-134">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="98f74-135">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="98f74-135">Schema Name</span></span>  <br/> |<span data-ttu-id="98f74-136">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="98f74-136">Messages schema</span></span>  <br/> |
|<span data-ttu-id="98f74-137">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="98f74-137">Validation File</span></span>  <br/> |<span data-ttu-id="98f74-138">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="98f74-138">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="98f74-139">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="98f74-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="98f74-140">False</span><span class="sxs-lookup"><span data-stu-id="98f74-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="98f74-141">Ver también</span><span class="sxs-lookup"><span data-stu-id="98f74-141">See also</span></span>



- [<span data-ttu-id="98f74-142">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="98f74-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

