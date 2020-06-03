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
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460095"
---
# <a name="errorcode-soap"></a><span data-ttu-id="274eb-103">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="274eb-103">ErrorCode (SOAP)</span></span>

<span data-ttu-id="274eb-104">El elemento **ErrorCode** representa un código de error devuelto por el servicio de detección automática.</span><span class="sxs-lookup"><span data-stu-id="274eb-104">The **ErrorCode** element represents an error code that is returned by the Autodiscover service.</span></span> 
  
```XML
<ErrorCode/>
```

 <span data-ttu-id="274eb-105">**string**</span><span class="sxs-lookup"><span data-stu-id="274eb-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="274eb-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="274eb-106">Attributes and elements</span></span>

<span data-ttu-id="274eb-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="274eb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="274eb-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="274eb-108">Attributes</span></span>

<span data-ttu-id="274eb-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="274eb-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="274eb-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="274eb-110">Child elements</span></span>

<span data-ttu-id="274eb-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="274eb-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="274eb-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="274eb-112">Parent elements</span></span>

|<span data-ttu-id="274eb-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="274eb-113">**Element**</span></span>|<span data-ttu-id="274eb-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="274eb-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="274eb-115">AutodiscoverResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="274eb-115">AutodiscoverResponse (SOAP)</span></span>](autodiscoverresponse-soap.md) <br/> |<span data-ttu-id="274eb-116">Representa el tipo base para todas las respuestas que devuelve el servicio de detección automática.</span><span class="sxs-lookup"><span data-stu-id="274eb-116">Represents the base type for all responses that are returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="274eb-117">DomainResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="274eb-117">DomainResponse (SOAP)</span></span>](domainresponse-soap.md) <br/> |<span data-ttu-id="274eb-118">Contiene la configuración solicitada para el dominio especificado.</span><span class="sxs-lookup"><span data-stu-id="274eb-118">Contains the requested settings for the specified domain.</span></span>  <br/> |
|[<span data-ttu-id="274eb-119">GetDomainSettingsResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="274eb-119">GetDomainSettingsResponse (SOAP)</span></span>](getdomainsettingsresponse-soap.md) <br/> |<span data-ttu-id="274eb-120">Contiene la respuesta a una llamada de [operación de GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md) para un dominio individual.</span><span class="sxs-lookup"><span data-stu-id="274eb-120">Contains the response to a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) call for an individual domain.</span></span>  <br/> |
|[<span data-ttu-id="274eb-121">GetFederationInformationResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="274eb-121">GetFederationInformationResponse (SOAP)</span></span>](getfederationinformationresponse-soap.md) <br/> |<span data-ttu-id="274eb-122">Contiene la respuesta a una solicitud de [operación de GetFederationInformation (SOAP)](getfederationinformation-operation-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="274eb-122">Contains the response to a [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md) request.</span></span>  <br/> |
|[<span data-ttu-id="274eb-123">Respuesta (SOAP)</span><span class="sxs-lookup"><span data-stu-id="274eb-123">Response (SOAP)</span></span>](response-soap.md) <br/> |<span data-ttu-id="274eb-124">Contiene la respuesta a una solicitud de [operación de GetUserSettings (SOAP)](getusersettings-operation-soap.md).</span><span class="sxs-lookup"><span data-stu-id="274eb-124">Contains the response to a [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md)request.</span></span>  <br/> |
|[<span data-ttu-id="274eb-125">UserSettingError (SOAP)</span><span class="sxs-lookup"><span data-stu-id="274eb-125">UserSettingError (SOAP)</span></span>](usersettingerror-soap.md) <br/> |<span data-ttu-id="274eb-126">Representa un error que se devuelve al recuperar una configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="274eb-126">Represents an error that is returned while retrieving a user setting.</span></span>  <br/> |
|[<span data-ttu-id="274eb-127">UserResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="274eb-127">UserResponse (SOAP)</span></span>](userresponse-soap.md) <br/> |<span data-ttu-id="274eb-128">Representa una respuesta a una solicitud de [operación de GetUserSettings (SOAP)](getusersettings-operation-soap.md) para un usuario individual.</span><span class="sxs-lookup"><span data-stu-id="274eb-128">Represents a response to a [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md) request for an individual user.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="274eb-129">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="274eb-129">Text value</span></span>

<span data-ttu-id="274eb-130">El valor de texto representa el código de error de una respuesta de error de detección automática.</span><span class="sxs-lookup"><span data-stu-id="274eb-130">The text value represents the error code for an Autodiscover error response.</span></span> <span data-ttu-id="274eb-131">En la siguiente tabla se enumeran los valores de texto posibles para el elemento **ErrorCode** .</span><span class="sxs-lookup"><span data-stu-id="274eb-131">The following table lists the possible text values for the **ErrorCode** element.</span></span> 
  
|<span data-ttu-id="274eb-132">**Valor de texto del código de error**</span><span class="sxs-lookup"><span data-stu-id="274eb-132">**Error code text value**</span></span>|<span data-ttu-id="274eb-133">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="274eb-133">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="274eb-134">NoError</span><span class="sxs-lookup"><span data-stu-id="274eb-134">NoError</span></span>  <br/> |<span data-ttu-id="274eb-135">No hubo ningún error.</span><span class="sxs-lookup"><span data-stu-id="274eb-135">There was no error.</span></span>  <br/> |
|<span data-ttu-id="274eb-136">RedirectAddress</span><span class="sxs-lookup"><span data-stu-id="274eb-136">RedirectAddress</span></span>  <br/> |<span data-ttu-id="274eb-137">La persona que llama debe seguir la redirección de la dirección de correo electrónico que ha devuelto la detección automática.</span><span class="sxs-lookup"><span data-stu-id="274eb-137">The caller must follow the e-mail address redirection that was returned by Autodiscover.</span></span>  <br/> |
|<span data-ttu-id="274eb-138">RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="274eb-138">RedirectUrl</span></span>  <br/> |<span data-ttu-id="274eb-139">La persona que llama debe seguir la redirección URL devuelta por la detección automática.</span><span class="sxs-lookup"><span data-stu-id="274eb-139">The caller must follow the URL redirection that was returned by Autodiscover.</span></span>  <br/> |
|<span data-ttu-id="274eb-140">InvalidUser</span><span class="sxs-lookup"><span data-stu-id="274eb-140">InvalidUser</span></span>  <br/> |<span data-ttu-id="274eb-141">El usuario que se pasó en la solicitud no es válido.</span><span class="sxs-lookup"><span data-stu-id="274eb-141">The user that was passed in the request is invalid.</span></span>  <br/> |
|<span data-ttu-id="274eb-142">InvalidRequest</span><span class="sxs-lookup"><span data-stu-id="274eb-142">InvalidRequest</span></span>  <br/> |<span data-ttu-id="274eb-143">La solicitud no es válida.</span><span class="sxs-lookup"><span data-stu-id="274eb-143">The request is invalid.</span></span>  <br/> |
|<span data-ttu-id="274eb-144">InvalidSetting</span><span class="sxs-lookup"><span data-stu-id="274eb-144">InvalidSetting</span></span>  <br/> |<span data-ttu-id="274eb-145">Una configuración especificada no es válida.</span><span class="sxs-lookup"><span data-stu-id="274eb-145">A specified setting is invalid.</span></span>  <br/> |
|<span data-ttu-id="274eb-146">SettingIsNotAvailable</span><span class="sxs-lookup"><span data-stu-id="274eb-146">SettingIsNotAvailable</span></span>  <br/> |<span data-ttu-id="274eb-147">Una configuración especificada no está disponible.</span><span class="sxs-lookup"><span data-stu-id="274eb-147">A specified setting is not available.</span></span>  <br/> |
|<span data-ttu-id="274eb-148">ServerBusy</span><span class="sxs-lookup"><span data-stu-id="274eb-148">ServerBusy</span></span>  <br/> |<span data-ttu-id="274eb-149">El servidor está demasiado ocupado para procesar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="274eb-149">The server is too busy to process the request.</span></span>  <br/> |
|<span data-ttu-id="274eb-150">InvalidDomain</span><span class="sxs-lookup"><span data-stu-id="274eb-150">InvalidDomain</span></span>  <br/> |<span data-ttu-id="274eb-151">El dominio solicitado no es válido.</span><span class="sxs-lookup"><span data-stu-id="274eb-151">The requested domain is not valid.</span></span>  <br/> |
|<span data-ttu-id="274eb-152">NotFederated</span><span class="sxs-lookup"><span data-stu-id="274eb-152">NotFederated</span></span>  <br/> |<span data-ttu-id="274eb-153">La organización no está federada.</span><span class="sxs-lookup"><span data-stu-id="274eb-153">The organization is not federated.</span></span>  <br/> |
|<span data-ttu-id="274eb-154">InternalServerError</span><span class="sxs-lookup"><span data-stu-id="274eb-154">InternalServerError</span></span>  <br/> |<span data-ttu-id="274eb-155">Hay un error interno del servidor.</span><span class="sxs-lookup"><span data-stu-id="274eb-155">There is an internal server error.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="274eb-156">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="274eb-156">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="274eb-157">Namespace</span><span class="sxs-lookup"><span data-stu-id="274eb-157">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="274eb-158">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="274eb-158">Schema Name</span></span>  <br/> |<span data-ttu-id="274eb-159">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="274eb-159">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="274eb-160">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="274eb-160">Validation File</span></span>  <br/> |<span data-ttu-id="274eb-161">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="274eb-161">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="274eb-162">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="274eb-162">Can be Empty</span></span>  <br/> |<span data-ttu-id="274eb-163">Verdadero</span><span class="sxs-lookup"><span data-stu-id="274eb-163">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="274eb-164">Vea también</span><span class="sxs-lookup"><span data-stu-id="274eb-164">See also</span></span>



[<span data-ttu-id="274eb-165">Operación GetUserSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="274eb-165">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
  
[<span data-ttu-id="274eb-166">Operación GetDomainSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="274eb-166">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)
  
[<span data-ttu-id="274eb-167">Operación GetFederationInformation (SOAP)</span><span class="sxs-lookup"><span data-stu-id="274eb-167">GetFederationInformation operation (SOAP)</span></span>](getfederationinformation-operation-soap.md)

