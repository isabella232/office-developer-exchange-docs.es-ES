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
description: El elemento ErrorCode representa un código de error devuelto por el servicio Detección automática.
ms.openlocfilehash: 2dd91cec4645325c02bc8588af0ee0547909b945
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764436"
---
# <a name="errorcode-soap"></a><span data-ttu-id="7462c-103">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7462c-103">ErrorCode (SOAP)</span></span>

<span data-ttu-id="7462c-104">El elemento **ErrorCode** representa un código de error devuelto por el servicio Detección automática.</span><span class="sxs-lookup"><span data-stu-id="7462c-104">The **ErrorCode** element represents an error code that is returned by the Autodiscover service.</span></span> 
  
```XML
<ErrorCode/>
```

 <span data-ttu-id="7462c-105">**string**</span><span class="sxs-lookup"><span data-stu-id="7462c-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7462c-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="7462c-106">Attributes and elements</span></span>

<span data-ttu-id="7462c-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="7462c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7462c-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="7462c-108">Attributes</span></span>

<span data-ttu-id="7462c-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7462c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7462c-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7462c-110">Child elements</span></span>

<span data-ttu-id="7462c-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7462c-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7462c-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7462c-112">Parent elements</span></span>

|<span data-ttu-id="7462c-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="7462c-113">**Element**</span></span>|<span data-ttu-id="7462c-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7462c-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7462c-115">AutodiscoverResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7462c-115">AutodiscoverResponse (SOAP)</span></span>](autodiscoverresponse-soap.md) <br/> |<span data-ttu-id="7462c-116">Representa el tipo base para todas las respuestas que son devueltos por el servicio de detección automática.</span><span class="sxs-lookup"><span data-stu-id="7462c-116">Represents the base type for all responses that are returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="7462c-117">DomainResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7462c-117">DomainResponse (SOAP)</span></span>](domainresponse-soap.md) <br/> |<span data-ttu-id="7462c-118">Contiene la configuración solicitada para el dominio especificado.</span><span class="sxs-lookup"><span data-stu-id="7462c-118">Contains the requested settings for the specified domain.</span></span>  <br/> |
|[<span data-ttu-id="7462c-119">GetDomainSettingsResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7462c-119">GetDomainSettingsResponse (SOAP)</span></span>](getdomainsettingsresponse-soap.md) <br/> |<span data-ttu-id="7462c-120">Contiene la respuesta a una llamada de la [operación de GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md) para un dominio individual.</span><span class="sxs-lookup"><span data-stu-id="7462c-120">Contains the response to a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) call for an individual domain.</span></span>  <br/> |
|[<span data-ttu-id="7462c-121">GetFederationInformationResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7462c-121">GetFederationInformationResponse (SOAP)</span></span>](getfederationinformationresponse-soap.md) <br/> |<span data-ttu-id="7462c-122">Contiene la respuesta a una solicitud de [operación GetFederationInformation (SOAP)](getfederationinformation-operation-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="7462c-122">Contains the response to a [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md) request.</span></span>  <br/> |
|[<span data-ttu-id="7462c-123">Respuesta (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7462c-123">Response (SOAP)</span></span>](response-soap.md) <br/> |<span data-ttu-id="7462c-124">Contiene la respuesta a una solicitud de [operación GetUserSettings (SOAP)](getusersettings-operation-soap.md).</span><span class="sxs-lookup"><span data-stu-id="7462c-124">Contains the response to a [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md)request.</span></span>  <br/> |
|[<span data-ttu-id="7462c-125">UserSettingError (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7462c-125">UserSettingError (SOAP)</span></span>](usersettingerror-soap.md) <br/> |<span data-ttu-id="7462c-126">Representa un error que se devuelve al recuperar una configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="7462c-126">Represents an error that is returned while retrieving a user setting.</span></span>  <br/> |
|[<span data-ttu-id="7462c-127">UserResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7462c-127">UserResponse (SOAP)</span></span>](userresponse-soap.md) <br/> |<span data-ttu-id="7462c-128">Representa una respuesta a una solicitud de [operación GetUserSettings (SOAP)](getusersettings-operation-soap.md) para un usuario individual.</span><span class="sxs-lookup"><span data-stu-id="7462c-128">Represents a response to a [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md) request for an individual user.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7462c-129">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="7462c-129">Text value</span></span>

<span data-ttu-id="7462c-130">El valor de texto representa el código de error para una respuesta de error de detección automática.</span><span class="sxs-lookup"><span data-stu-id="7462c-130">The text value represents the error code for an Autodiscover error response.</span></span> <span data-ttu-id="7462c-131">En la siguiente tabla se enumera los posibles valores de texto para el elemento de **código de error** .</span><span class="sxs-lookup"><span data-stu-id="7462c-131">The following table lists the possible text values for the **ErrorCode** element.</span></span> 
  
|<span data-ttu-id="7462c-132">**Valor de texto del código de error**</span><span class="sxs-lookup"><span data-stu-id="7462c-132">**Error code text value**</span></span>|<span data-ttu-id="7462c-133">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7462c-133">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7462c-134">NoError</span><span class="sxs-lookup"><span data-stu-id="7462c-134">NoError</span></span>  <br/> |<span data-ttu-id="7462c-135">Se ha producido ningún error.</span><span class="sxs-lookup"><span data-stu-id="7462c-135">There was no error.</span></span>  <br/> |
|<span data-ttu-id="7462c-136">RedirectAddress</span><span class="sxs-lookup"><span data-stu-id="7462c-136">RedirectAddress</span></span>  <br/> |<span data-ttu-id="7462c-137">El autor de la llamada debe seguir la redirección de dirección de correo electrónico que se ha devuelto por la detección automática.</span><span class="sxs-lookup"><span data-stu-id="7462c-137">The caller must follow the e-mail address redirection that was returned by Autodiscover.</span></span>  <br/> |
|<span data-ttu-id="7462c-138">RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="7462c-138">RedirectUrl</span></span>  <br/> |<span data-ttu-id="7462c-139">El autor de la llamada debe seguir la redirección de dirección URL que se ha devuelto por la detección automática.</span><span class="sxs-lookup"><span data-stu-id="7462c-139">The caller must follow the URL redirection that was returned by Autodiscover.</span></span>  <br/> |
|<span data-ttu-id="7462c-140">InvalidUser</span><span class="sxs-lookup"><span data-stu-id="7462c-140">InvalidUser</span></span>  <br/> |<span data-ttu-id="7462c-141">El usuario que se pasó en la solicitud no es válido.</span><span class="sxs-lookup"><span data-stu-id="7462c-141">The user that was passed in the request is invalid.</span></span>  <br/> |
|<span data-ttu-id="7462c-142">InvalidRequest</span><span class="sxs-lookup"><span data-stu-id="7462c-142">InvalidRequest</span></span>  <br/> |<span data-ttu-id="7462c-143">La solicitud no es válida.</span><span class="sxs-lookup"><span data-stu-id="7462c-143">The request is invalid.</span></span>  <br/> |
|<span data-ttu-id="7462c-144">InvalidSetting</span><span class="sxs-lookup"><span data-stu-id="7462c-144">InvalidSetting</span></span>  <br/> |<span data-ttu-id="7462c-145">Una opción de configuración especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="7462c-145">A specified setting is invalid.</span></span>  <br/> |
|<span data-ttu-id="7462c-146">SettingIsNotAvailable</span><span class="sxs-lookup"><span data-stu-id="7462c-146">SettingIsNotAvailable</span></span>  <br/> |<span data-ttu-id="7462c-147">Una opción de configuración especificado no está disponible.</span><span class="sxs-lookup"><span data-stu-id="7462c-147">A specified setting is not available.</span></span>  <br/> |
|<span data-ttu-id="7462c-148">ServerBusy</span><span class="sxs-lookup"><span data-stu-id="7462c-148">ServerBusy</span></span>  <br/> |<span data-ttu-id="7462c-149">El servidor está demasiado ocupado para procesar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7462c-149">The server is too busy to process the request.</span></span>  <br/> |
|<span data-ttu-id="7462c-150">InvalidDomain</span><span class="sxs-lookup"><span data-stu-id="7462c-150">InvalidDomain</span></span>  <br/> |<span data-ttu-id="7462c-151">El dominio solicitado no es válido.</span><span class="sxs-lookup"><span data-stu-id="7462c-151">The requested domain is not valid.</span></span>  <br/> |
|<span data-ttu-id="7462c-152">NotFederated</span><span class="sxs-lookup"><span data-stu-id="7462c-152">NotFederated</span></span>  <br/> |<span data-ttu-id="7462c-153">La organización no está federada.</span><span class="sxs-lookup"><span data-stu-id="7462c-153">The organization is not federated.</span></span>  <br/> |
|<span data-ttu-id="7462c-154">InternalServerError</span><span class="sxs-lookup"><span data-stu-id="7462c-154">InternalServerError</span></span>  <br/> |<span data-ttu-id="7462c-155">Hay un error interno del servidor.</span><span class="sxs-lookup"><span data-stu-id="7462c-155">There is an internal server error.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="7462c-156">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7462c-156">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7462c-157">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7462c-157">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="7462c-158">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="7462c-158">Schema Name</span></span>  <br/> |<span data-ttu-id="7462c-159">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="7462c-159">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="7462c-160">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="7462c-160">Validation File</span></span>  <br/> |<span data-ttu-id="7462c-161">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="7462c-161">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7462c-162">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="7462c-162">Can be Empty</span></span>  <br/> |<span data-ttu-id="7462c-163">Verdadero</span><span class="sxs-lookup"><span data-stu-id="7462c-163">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7462c-164">Vea también</span><span class="sxs-lookup"><span data-stu-id="7462c-164">See also</span></span>



[<span data-ttu-id="7462c-165">Operación GetUserSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7462c-165">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
  
[<span data-ttu-id="7462c-166">Operación GetDomainSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7462c-166">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)
  
[<span data-ttu-id="7462c-167">Operación GetFederationInformation (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7462c-167">GetFederationInformation operation (SOAP)</span></span>](getfederationinformation-operation-soap.md)

