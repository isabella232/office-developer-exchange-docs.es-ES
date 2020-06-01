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
description: El elemento ProtectionRulesConfiguration contiene información de configuración del servicio para el servicio de reglas de protección.
ms.openlocfilehash: e664fba78f170c9f4c59b49b3a08c0dd2e4ed4cd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456775"
---
# <a name="protectionrulesconfiguration"></a><span data-ttu-id="705bb-103">ProtectionRulesConfiguration</span><span class="sxs-lookup"><span data-stu-id="705bb-103">ProtectionRulesConfiguration</span></span>

<span data-ttu-id="705bb-104">El elemento **ProtectionRulesConfiguration** contiene información de configuración del servicio para el servicio de reglas de protección.</span><span class="sxs-lookup"><span data-stu-id="705bb-104">The **ProtectionRulesConfiguration** element contains service configuration information for the protection rules service.</span></span> 
  
```XML
<ProtectionRulesConfiguration RefreshInterval="">
   <Rules/>
   <InternalDomains/>
</ProtectionRulesConfiguration>
```

 <span data-ttu-id="705bb-105">**ProtectionRulesServiceConfiguration**</span><span class="sxs-lookup"><span data-stu-id="705bb-105">**ProtectionRulesServiceConfiguration**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="705bb-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="705bb-106">Attributes and elements</span></span>

<span data-ttu-id="705bb-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="705bb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="705bb-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="705bb-108">Attributes</span></span>

|<span data-ttu-id="705bb-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="705bb-109">**Attribute**</span></span>|<span data-ttu-id="705bb-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="705bb-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="705bb-111">**RefreshInterval**</span><span class="sxs-lookup"><span data-stu-id="705bb-111">**RefreshInterval**</span></span> <br/> |<span data-ttu-id="705bb-112">Especifica la frecuencia, en horas completas, que el cliente debe solicitar reglas de protección del servidor.</span><span class="sxs-lookup"><span data-stu-id="705bb-112">Specifies how often, in whole hours, the client should request protection rules from the server.</span></span> <span data-ttu-id="705bb-113">Este atributo es obligatorio y su valor debe ser un entero que sea igual o mayor que 1.</span><span class="sxs-lookup"><span data-stu-id="705bb-113">This attribute is required and its value must be an integer that is equal to or greater than 1.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="705bb-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="705bb-114">Child elements</span></span>

|<span data-ttu-id="705bb-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="705bb-115">**Element**</span></span>|<span data-ttu-id="705bb-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="705bb-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="705bb-117">Reglas</span><span class="sxs-lookup"><span data-stu-id="705bb-117">Rules </span></span>](rules-ex15websvcsotherref.md) <br/> |<span data-ttu-id="705bb-118">Una matriz de reglas de protección.</span><span class="sxs-lookup"><span data-stu-id="705bb-118">An array of protection rules.</span></span> <span data-ttu-id="705bb-119">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="705bb-119">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="705bb-120">InternalDomains (SmtpDomainList)</span><span class="sxs-lookup"><span data-stu-id="705bb-120">InternalDomains (SmtpDomainList)</span></span>](internaldomains-smtpdomainlist.md) <br/> |<span data-ttu-id="705bb-121">Identifica la lista de dominios SMTP internos de la organización.</span><span class="sxs-lookup"><span data-stu-id="705bb-121">Identifies the list of internal SMTP domains of the organization.</span></span> <span data-ttu-id="705bb-122">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="705bb-122">This element is required.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="705bb-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="705bb-123">Parent elements</span></span>

|<span data-ttu-id="705bb-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="705bb-124">**Element**</span></span>|<span data-ttu-id="705bb-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="705bb-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="705bb-126">ServiceConfigurationResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="705bb-126">ServiceConfigurationResponseMessageType</span></span>](serviceconfigurationresponsemessagetype.md) <br/> |<span data-ttu-id="705bb-127">Contiene las opciones de configuración del servicio.</span><span class="sxs-lookup"><span data-stu-id="705bb-127">Contains service configuration settings.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="705bb-128">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="705bb-128">Text value</span></span>

<span data-ttu-id="705bb-129">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="705bb-129">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="705bb-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="705bb-130">Remarks</span></span>

<span data-ttu-id="705bb-131">La configuración del servicio de reglas de protección se compone de una lista de reglas, dominios internos y un intervalo de actualización.</span><span class="sxs-lookup"><span data-stu-id="705bb-131">The protection rules service configuration is comprised of a list of rules, internal domains, and a refresh interval.</span></span>
  
<span data-ttu-id="705bb-132">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="705bb-132">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="705bb-133">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="705bb-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="705bb-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="705bb-134">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="705bb-135">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="705bb-135">Schema Name</span></span>  <br/> |<span data-ttu-id="705bb-136">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="705bb-136">Messages schema</span></span>  <br/> |
|<span data-ttu-id="705bb-137">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="705bb-137">Validation File</span></span>  <br/> |<span data-ttu-id="705bb-138">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="705bb-138">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="705bb-139">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="705bb-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="705bb-140">Falso</span><span class="sxs-lookup"><span data-stu-id="705bb-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="705bb-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="705bb-141">See also</span></span>



- [<span data-ttu-id="705bb-142">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="705bb-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

