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
description: El elemento Response contiene la respuesta a una operación GetUserSettings (SOAP), GetDomainSettings Operation (SOAP) o una solicitud GetFederationInformation (SOAP).
ms.openlocfilehash: 90cb29dd4ce4026211a5b592f149c8190dc81d29
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456419"
---
# <a name="response-soap"></a><span data-ttu-id="9bff3-103">Respuesta (SOAP)</span><span class="sxs-lookup"><span data-stu-id="9bff3-103">Response (SOAP)</span></span>

<span data-ttu-id="9bff3-104">El elemento **Response** contiene la respuesta a una [operación GetUserSettings (SOAP)](getusersettings-operation-soap.md), [GetDomainSettings Operation (SOAP)](getdomainsettings-operation-soap.md)o una solicitud [GetFederationInformation (SOAP)](getfederationinformation-operation-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="9bff3-104">The **Response** element contains the response to a [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md), [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md), or a [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md) request.</span></span> 
  
```XML
<Response>
   <ErrorCode/>
   <ErrorMessage/>
   <UserResponses/>
</Response>
```

 <span data-ttu-id="9bff3-105">**GetUserSettingsResponse**</span><span class="sxs-lookup"><span data-stu-id="9bff3-105">**GetUserSettingsResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9bff3-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="9bff3-106">Attributes and elements</span></span>

<span data-ttu-id="9bff3-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="9bff3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9bff3-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="9bff3-108">Attributes</span></span>

<span data-ttu-id="9bff3-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="9bff3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9bff3-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9bff3-110">Child elements</span></span>

|<span data-ttu-id="9bff3-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9bff3-111">**Element**</span></span>|<span data-ttu-id="9bff3-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9bff3-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9bff3-113">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="9bff3-113">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="9bff3-114">Representa un código de error devuelto por el servicio de detección automática.</span><span class="sxs-lookup"><span data-stu-id="9bff3-114">Represents an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="9bff3-115">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="9bff3-115">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="9bff3-116">Representa un mensaje que está asociado con un código de error devuelto por el servicio de detección automática.</span><span class="sxs-lookup"><span data-stu-id="9bff3-116">Represents a message that is associated with an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="9bff3-117">UserResponses (SOAP)</span><span class="sxs-lookup"><span data-stu-id="9bff3-117">UserResponses (SOAP)</span></span>](userresponses-soap.md) <br/> |<span data-ttu-id="9bff3-118">Contiene las opciones de configuración para cada usuario solicitado.</span><span class="sxs-lookup"><span data-stu-id="9bff3-118">Contains the configuration settings for each requested user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9bff3-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="9bff3-119">Parent elements</span></span>

|<span data-ttu-id="9bff3-120">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9bff3-120">**Element**</span></span>|<span data-ttu-id="9bff3-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9bff3-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9bff3-122">GetUserSettingsResponseMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="9bff3-122">GetUserSettingsResponseMessage (SOAP)</span></span>](getusersettingsresponsemessage-soap.md) <br/> |<span data-ttu-id="9bff3-123">Define una respuesta a un [GetUserSettingsRequest (SOAP)](getusersettingsrequest-soap.md)</span><span class="sxs-lookup"><span data-stu-id="9bff3-123">Defines a response to a [GetUserSettingsRequest (SOAP)](getusersettingsrequest-soap.md)</span></span> <br/> |
|[<span data-ttu-id="9bff3-124">GetDomainSettingsResponseMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="9bff3-124">GetDomainSettingsResponseMessage (SOAP)</span></span>](getdomainsettingsresponsemessage-soap.md) <br/> |<span data-ttu-id="9bff3-125">Define una respuesta a un [GetDomainSettingsRequest (SOAP)](getdomainsettingsrequest-soap.md).</span><span class="sxs-lookup"><span data-stu-id="9bff3-125">Defines a response to a [GetDomainSettingsRequest (SOAP)](getdomainsettingsrequest-soap.md).</span></span>  <br/> |
|[<span data-ttu-id="9bff3-126">GetFederationInformationResponseMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="9bff3-126">GetFederationInformationResponseMessage (SOAP)</span></span>](getfederationinformationresponsemessage-soap.md) <br/> |<span data-ttu-id="9bff3-127">Define una respuesta a un [GetFederationInformationRequest (SOAP)](getfederationinformationrequest-soap.md).</span><span class="sxs-lookup"><span data-stu-id="9bff3-127">Defines a response to a [GetFederationInformationRequest (SOAP)](getfederationinformationrequest-soap.md).</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="9bff3-128">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="9bff3-128">Text value</span></span>

<span data-ttu-id="9bff3-129">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="9bff3-129">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9bff3-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="9bff3-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9bff3-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="9bff3-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="9bff3-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="9bff3-132">Schema Name</span></span>  <br/> |<span data-ttu-id="9bff3-133">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="9bff3-133">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="9bff3-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="9bff3-134">Validation File</span></span>  <br/> |<span data-ttu-id="9bff3-135">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="9bff3-135">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9bff3-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="9bff3-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="9bff3-137">Verdadero</span><span class="sxs-lookup"><span data-stu-id="9bff3-137">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9bff3-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="9bff3-138">See also</span></span>



[<span data-ttu-id="9bff3-139">Operación GetUserSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="9bff3-139">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)


[<span data-ttu-id="9bff3-140">Referencia del servicio web de Detección automática para Exchange</span><span class="sxs-lookup"><span data-stu-id="9bff3-140">Autodiscover web service reference for Exchange</span></span>](autodiscover-web-service-reference-for-exchange.md)
  
[<span data-ttu-id="9bff3-141">Elementos XML de detección automática de SOAP para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="9bff3-141">SOAP Autodiscover XML elements for Exchange 2013</span></span>](soap-autodiscover-xml-elements-for-exchange-2013.md)

