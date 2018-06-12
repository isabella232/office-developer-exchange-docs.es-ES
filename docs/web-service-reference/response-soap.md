---
title: Respuesta (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 4c2bcdeb-95ce-4ffa-bd83-118af53b534f
description: El elemento de respuesta contiene la respuesta a una solicitud de operación (SOAP) GetFederationInformation, operación GetDomainSettings (SOAP) o una operación de GetUserSettings (SOAP).
ms.openlocfilehash: 240c8e1f904ad685b51c1f657b2bc18e14fd985e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837179"
---
# <a name="response-soap"></a><span data-ttu-id="ccf9e-103">Respuesta (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ccf9e-103">Response (SOAP)</span></span>

<span data-ttu-id="ccf9e-104">El elemento de **respuesta** contiene la respuesta a una [operación de GetUserSettings (SOAP)](getusersettings-operation-soap.md), [operación GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md)o una solicitud de [operación GetFederationInformation (SOAP)](getfederationinformation-operation-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="ccf9e-104">The **Response** element contains the response to a [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md), [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md), or a [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md) request.</span></span> 
  
```XML
<Response>
   <ErrorCode/>
   <ErrorMessage/>
   <UserResponses/>
</Response>
```

 <span data-ttu-id="ccf9e-105">**GetUserSettingsResponse**</span><span class="sxs-lookup"><span data-stu-id="ccf9e-105">**GetUserSettingsResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ccf9e-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ccf9e-106">Attributes and elements</span></span>

<span data-ttu-id="ccf9e-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ccf9e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ccf9e-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="ccf9e-108">Attributes</span></span>

<span data-ttu-id="ccf9e-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ccf9e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ccf9e-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ccf9e-110">Child elements</span></span>

|<span data-ttu-id="ccf9e-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="ccf9e-111">**Element**</span></span>|<span data-ttu-id="ccf9e-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ccf9e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ccf9e-113">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ccf9e-113">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="ccf9e-114">Representa un código de error devuelto por el servicio Detección automática.</span><span class="sxs-lookup"><span data-stu-id="ccf9e-114">Represents an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="ccf9e-115">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ccf9e-115">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="ccf9e-116">Representa un mensaje en el que está asociado con un código de error devuelto por el servicio Detección automática.</span><span class="sxs-lookup"><span data-stu-id="ccf9e-116">Represents a message that is associated with an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="ccf9e-117">UserResponses (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ccf9e-117">UserResponses (SOAP)</span></span>](userresponses-soap.md) <br/> |<span data-ttu-id="ccf9e-118">Contiene las opciones de configuración para cada usuario solicitado.</span><span class="sxs-lookup"><span data-stu-id="ccf9e-118">Contains the configuration settings for each requested user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ccf9e-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ccf9e-119">Parent elements</span></span>

|<span data-ttu-id="ccf9e-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="ccf9e-120">**Element**</span></span>|<span data-ttu-id="ccf9e-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ccf9e-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ccf9e-122">GetUserSettingsResponseMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ccf9e-122">GetUserSettingsResponseMessage (SOAP)</span></span>](getusersettingsresponsemessage-soap.md) <br/> |<span data-ttu-id="ccf9e-123">Define una respuesta a un [GetUserSettingsRequest (SOAP)](getusersettingsrequest-soap.md)</span><span class="sxs-lookup"><span data-stu-id="ccf9e-123">Defines a response to a [GetUserSettingsRequest (SOAP)](getusersettingsrequest-soap.md)</span></span> <br/> |
|[<span data-ttu-id="ccf9e-124">GetDomainSettingsResponseMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ccf9e-124">GetDomainSettingsResponseMessage (SOAP)</span></span>](getdomainsettingsresponsemessage-soap.md) <br/> |<span data-ttu-id="ccf9e-125">Define una respuesta a un [GetDomainSettingsRequest (SOAP)](getdomainsettingsrequest-soap.md).</span><span class="sxs-lookup"><span data-stu-id="ccf9e-125">Defines a response to a [GetDomainSettingsRequest (SOAP)](getdomainsettingsrequest-soap.md).</span></span>  <br/> |
|[<span data-ttu-id="ccf9e-126">GetFederationInformationResponseMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ccf9e-126">GetFederationInformationResponseMessage (SOAP)</span></span>](getfederationinformationresponsemessage-soap.md) <br/> |<span data-ttu-id="ccf9e-127">Define una respuesta a un [GetFederationInformationRequest (SOAP)](getfederationinformationrequest-soap.md).</span><span class="sxs-lookup"><span data-stu-id="ccf9e-127">Defines a response to a [GetFederationInformationRequest (SOAP)](getfederationinformationrequest-soap.md).</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ccf9e-128">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="ccf9e-128">Text value</span></span>

<span data-ttu-id="ccf9e-129">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ccf9e-129">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ccf9e-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ccf9e-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ccf9e-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ccf9e-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="ccf9e-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ccf9e-132">Schema Name</span></span>  <br/> |<span data-ttu-id="ccf9e-133">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="ccf9e-133">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="ccf9e-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ccf9e-134">Validation File</span></span>  <br/> |<span data-ttu-id="ccf9e-135">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ccf9e-135">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ccf9e-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ccf9e-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="ccf9e-137">Verdadero</span><span class="sxs-lookup"><span data-stu-id="ccf9e-137">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ccf9e-138">Ver también</span><span class="sxs-lookup"><span data-stu-id="ccf9e-138">See also</span></span>



[<span data-ttu-id="ccf9e-139">Operación GetUserSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ccf9e-139">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)


[<span data-ttu-id="ccf9e-140">Referencia de servicio web de detección automática para Exchange</span><span class="sxs-lookup"><span data-stu-id="ccf9e-140">Autodiscover web service reference for Exchange</span></span>](autodiscover-web-service-reference-for-exchange.md)
  
[<span data-ttu-id="ccf9e-141">Elementos de Autodiscover XML SOAP para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="ccf9e-141">SOAP Autodiscover XML elements for Exchange 2013</span></span>](soap-autodiscover-xml-elements-for-exchange-2013.md)

