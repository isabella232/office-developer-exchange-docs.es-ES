---
title: ErrorCode (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 5e5ec861-0191-4ecb-a906-47ce8ed96381
description: El elemento ErrorCode representa un código de error devuelto por el servicio de detección automática.
ms.openlocfilehash: d66167e51733ffcaa3d62a985d3e03e2ac80b715
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460095"
---
# <a name="errorcode-soap"></a><span data-ttu-id="6ff44-103">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6ff44-103">ErrorCode (SOAP)</span></span>

<span data-ttu-id="6ff44-104">El elemento **ErrorCode** representa un código de error devuelto por el servicio de detección automática.</span><span class="sxs-lookup"><span data-stu-id="6ff44-104">The **ErrorCode** element represents an error code that is returned by the Autodiscover service.</span></span> 
  
```XML
<ErrorCode/>
```

 <span data-ttu-id="6ff44-105">**string**</span><span class="sxs-lookup"><span data-stu-id="6ff44-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6ff44-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="6ff44-106">Attributes and elements</span></span>

<span data-ttu-id="6ff44-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="6ff44-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6ff44-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="6ff44-108">Attributes</span></span>

<span data-ttu-id="6ff44-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="6ff44-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6ff44-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6ff44-110">Child elements</span></span>

<span data-ttu-id="6ff44-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="6ff44-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6ff44-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6ff44-112">Parent elements</span></span>

|<span data-ttu-id="6ff44-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6ff44-113">**Element**</span></span>|<span data-ttu-id="6ff44-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6ff44-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6ff44-115">AutodiscoverResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6ff44-115">AutodiscoverResponse (SOAP)</span></span>](autodiscoverresponse-soap.md) <br/> |<span data-ttu-id="6ff44-116">Representa el tipo base para todas las respuestas que devuelve el servicio de detección automática.</span><span class="sxs-lookup"><span data-stu-id="6ff44-116">Represents the base type for all responses that are returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="6ff44-117">DomainResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6ff44-117">DomainResponse (SOAP)</span></span>](domainresponse-soap.md) <br/> |<span data-ttu-id="6ff44-118">Contiene la configuración solicitada para el dominio especificado.</span><span class="sxs-lookup"><span data-stu-id="6ff44-118">Contains the requested settings for the specified domain.</span></span>  <br/> |
|[<span data-ttu-id="6ff44-119">GetDomainSettingsResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6ff44-119">GetDomainSettingsResponse (SOAP)</span></span>](getdomainsettingsresponse-soap.md) <br/> |<span data-ttu-id="6ff44-120">Contiene la respuesta a una llamada de [operación de GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md) para un dominio individual.</span><span class="sxs-lookup"><span data-stu-id="6ff44-120">Contains the response to a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) call for an individual domain.</span></span>  <br/> |
|[<span data-ttu-id="6ff44-121">GetFederationInformationResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6ff44-121">GetFederationInformationResponse (SOAP)</span></span>](getfederationinformationresponse-soap.md) <br/> |<span data-ttu-id="6ff44-122">Contiene la respuesta a una solicitud de [operación de GetFederationInformation (SOAP)](getfederationinformation-operation-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="6ff44-122">Contains the response to a [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md) request.</span></span>  <br/> |
|[<span data-ttu-id="6ff44-123">Respuesta (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6ff44-123">Response (SOAP)</span></span>](response-soap.md) <br/> |<span data-ttu-id="6ff44-124">Contiene la respuesta a una solicitud de [operación de GetUserSettings (SOAP)](getusersettings-operation-soap.md).</span><span class="sxs-lookup"><span data-stu-id="6ff44-124">Contains the response to a [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md)request.</span></span>  <br/> |
|[<span data-ttu-id="6ff44-125">UserSettingError (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6ff44-125">UserSettingError (SOAP)</span></span>](usersettingerror-soap.md) <br/> |<span data-ttu-id="6ff44-126">Representa un error que se devuelve al recuperar una configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="6ff44-126">Represents an error that is returned while retrieving a user setting.</span></span>  <br/> |
|[<span data-ttu-id="6ff44-127">UserResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6ff44-127">UserResponse (SOAP)</span></span>](userresponse-soap.md) <br/> |<span data-ttu-id="6ff44-128">Representa una respuesta a una solicitud de [operación de GetUserSettings (SOAP)](getusersettings-operation-soap.md) para un usuario individual.</span><span class="sxs-lookup"><span data-stu-id="6ff44-128">Represents a response to a [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md) request for an individual user.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6ff44-129">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="6ff44-129">Text value</span></span>

<span data-ttu-id="6ff44-130">El valor de texto representa el código de error de una respuesta de error de detección automática.</span><span class="sxs-lookup"><span data-stu-id="6ff44-130">The text value represents the error code for an Autodiscover error response.</span></span> <span data-ttu-id="6ff44-131">En la siguiente tabla se enumeran los valores de texto posibles para el elemento **ErrorCode** .</span><span class="sxs-lookup"><span data-stu-id="6ff44-131">The following table lists the possible text values for the **ErrorCode** element.</span></span> 
  
|<span data-ttu-id="6ff44-132">**Valor de texto del código de error**</span><span class="sxs-lookup"><span data-stu-id="6ff44-132">**Error code text value**</span></span>|<span data-ttu-id="6ff44-133">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6ff44-133">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6ff44-134">NoError</span><span class="sxs-lookup"><span data-stu-id="6ff44-134">NoError</span></span>  <br/> |<span data-ttu-id="6ff44-135">No hubo ningún error.</span><span class="sxs-lookup"><span data-stu-id="6ff44-135">There was no error.</span></span>  <br/> |
|<span data-ttu-id="6ff44-136">RedirectAddress</span><span class="sxs-lookup"><span data-stu-id="6ff44-136">RedirectAddress</span></span>  <br/> |<span data-ttu-id="6ff44-137">La persona que llama debe seguir la redirección de la dirección de correo electrónico que ha devuelto la detección automática.</span><span class="sxs-lookup"><span data-stu-id="6ff44-137">The caller must follow the e-mail address redirection that was returned by Autodiscover.</span></span>  <br/> |
|<span data-ttu-id="6ff44-138">RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="6ff44-138">RedirectUrl</span></span>  <br/> |<span data-ttu-id="6ff44-139">La persona que llama debe seguir la redirección URL devuelta por la detección automática.</span><span class="sxs-lookup"><span data-stu-id="6ff44-139">The caller must follow the URL redirection that was returned by Autodiscover.</span></span>  <br/> |
|<span data-ttu-id="6ff44-140">InvalidUser</span><span class="sxs-lookup"><span data-stu-id="6ff44-140">InvalidUser</span></span>  <br/> |<span data-ttu-id="6ff44-141">El usuario que se pasó en la solicitud no es válido.</span><span class="sxs-lookup"><span data-stu-id="6ff44-141">The user that was passed in the request is invalid.</span></span>  <br/> |
|<span data-ttu-id="6ff44-142">InvalidRequest</span><span class="sxs-lookup"><span data-stu-id="6ff44-142">InvalidRequest</span></span>  <br/> |<span data-ttu-id="6ff44-143">La solicitud no es válida.</span><span class="sxs-lookup"><span data-stu-id="6ff44-143">The request is invalid.</span></span>  <br/> |
|<span data-ttu-id="6ff44-144">InvalidSetting</span><span class="sxs-lookup"><span data-stu-id="6ff44-144">InvalidSetting</span></span>  <br/> |<span data-ttu-id="6ff44-145">Una configuración especificada no es válida.</span><span class="sxs-lookup"><span data-stu-id="6ff44-145">A specified setting is invalid.</span></span>  <br/> |
|<span data-ttu-id="6ff44-146">SettingIsNotAvailable</span><span class="sxs-lookup"><span data-stu-id="6ff44-146">SettingIsNotAvailable</span></span>  <br/> |<span data-ttu-id="6ff44-147">Una configuración especificada no está disponible.</span><span class="sxs-lookup"><span data-stu-id="6ff44-147">A specified setting is not available.</span></span>  <br/> |
|<span data-ttu-id="6ff44-148">ServerBusy</span><span class="sxs-lookup"><span data-stu-id="6ff44-148">ServerBusy</span></span>  <br/> |<span data-ttu-id="6ff44-149">El servidor está demasiado ocupado para procesar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6ff44-149">The server is too busy to process the request.</span></span>  <br/> |
|<span data-ttu-id="6ff44-150">InvalidDomain</span><span class="sxs-lookup"><span data-stu-id="6ff44-150">InvalidDomain</span></span>  <br/> |<span data-ttu-id="6ff44-151">El dominio solicitado no es válido.</span><span class="sxs-lookup"><span data-stu-id="6ff44-151">The requested domain is not valid.</span></span>  <br/> |
|<span data-ttu-id="6ff44-152">NotFederated</span><span class="sxs-lookup"><span data-stu-id="6ff44-152">NotFederated</span></span>  <br/> |<span data-ttu-id="6ff44-153">La organización no está federada.</span><span class="sxs-lookup"><span data-stu-id="6ff44-153">The organization is not federated.</span></span>  <br/> |
|<span data-ttu-id="6ff44-154">InternalServerError</span><span class="sxs-lookup"><span data-stu-id="6ff44-154">InternalServerError</span></span>  <br/> |<span data-ttu-id="6ff44-155">Hay un error interno del servidor.</span><span class="sxs-lookup"><span data-stu-id="6ff44-155">There is an internal server error.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="6ff44-156">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="6ff44-156">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6ff44-157">Namespace</span><span class="sxs-lookup"><span data-stu-id="6ff44-157">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="6ff44-158">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="6ff44-158">Schema Name</span></span>  <br/> |<span data-ttu-id="6ff44-159">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="6ff44-159">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="6ff44-160">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="6ff44-160">Validation File</span></span>  <br/> |<span data-ttu-id="6ff44-161">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="6ff44-161">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6ff44-162">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="6ff44-162">Can be Empty</span></span>  <br/> |<span data-ttu-id="6ff44-163">Verdadero</span><span class="sxs-lookup"><span data-stu-id="6ff44-163">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6ff44-164">Vea también</span><span class="sxs-lookup"><span data-stu-id="6ff44-164">See also</span></span>



[<span data-ttu-id="6ff44-165">Operación GetUserSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6ff44-165">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
  
[<span data-ttu-id="6ff44-166">Operación GetDomainSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6ff44-166">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)
  
[<span data-ttu-id="6ff44-167">Operación GetFederationInformation (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6ff44-167">GetFederationInformation operation (SOAP)</span></span>](getfederationinformation-operation-soap.md)

