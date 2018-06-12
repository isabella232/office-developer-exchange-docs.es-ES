---
title: ErrorMessage (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: b84dd664-4c49-42c9-a49f-2ec4a9f7588b
description: El elemento ErrorMessage representa un mensaje en el que está asociado con un código de error devuelto por el servicio Detección automática.
ms.openlocfilehash: 888eedc9c7cbbd1aad5cba21e76d999699c7ed02
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764446"
---
# <a name="errormessage-soap"></a><span data-ttu-id="71a6e-103">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="71a6e-103">ErrorMessage (SOAP)</span></span>

<span data-ttu-id="71a6e-104">El elemento **ErrorMessage** representa un mensaje en el que está asociado con un código de error devuelto por el servicio Detección automática.</span><span class="sxs-lookup"><span data-stu-id="71a6e-104">The **ErrorMessage** element represents a message that is associated with an error code that is returned by the Autodiscover service.</span></span> 
  
```XML
<ErrorMessage/>
```

 <span data-ttu-id="71a6e-105">**string**</span><span class="sxs-lookup"><span data-stu-id="71a6e-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="71a6e-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="71a6e-106">Attributes and elements</span></span>

<span data-ttu-id="71a6e-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="71a6e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="71a6e-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="71a6e-108">Attributes</span></span>

<span data-ttu-id="71a6e-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="71a6e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="71a6e-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="71a6e-110">Child elements</span></span>

<span data-ttu-id="71a6e-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="71a6e-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="71a6e-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="71a6e-112">Parent elements</span></span>

|<span data-ttu-id="71a6e-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="71a6e-113">**Element**</span></span>|<span data-ttu-id="71a6e-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="71a6e-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="71a6e-115">AutodiscoverResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="71a6e-115">AutodiscoverResponse (SOAP)</span></span>](autodiscoverresponse-soap.md) <br/> |<span data-ttu-id="71a6e-116">Representa el tipo base para todas las respuestas que son devueltos por el servicio de detección automática.</span><span class="sxs-lookup"><span data-stu-id="71a6e-116">Represents the base type for all responses that are returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="71a6e-117">DomainResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="71a6e-117">DomainResponse (SOAP)</span></span>](domainresponse-soap.md) <br/> |<span data-ttu-id="71a6e-118">Contiene la configuración solicitada para el dominio especificado.</span><span class="sxs-lookup"><span data-stu-id="71a6e-118">Contains the requested settings for the specified domain.</span></span>  <br/> |
|[<span data-ttu-id="71a6e-119">GetDomainSettingsResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="71a6e-119">GetDomainSettingsResponse (SOAP)</span></span>](getdomainsettingsresponse-soap.md) <br/> |<span data-ttu-id="71a6e-120">Contiene la respuesta a una llamada de la [operación de GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md) para un dominio individual.</span><span class="sxs-lookup"><span data-stu-id="71a6e-120">Contains the response to a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) call for an individual domain.</span></span>  <br/> |
|[<span data-ttu-id="71a6e-121">GetFederationInformationResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="71a6e-121">GetFederationInformationResponse (SOAP)</span></span>](getfederationinformationresponse-soap.md) <br/> |<span data-ttu-id="71a6e-122">Contiene la respuesta a una solicitud de [operación GetFederationInformation (SOAP)](getfederationinformation-operation-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="71a6e-122">Contains the response to a [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md) request.</span></span>  <br/> |
|[<span data-ttu-id="71a6e-123">Respuesta (SOAP)</span><span class="sxs-lookup"><span data-stu-id="71a6e-123">Response (SOAP)</span></span>](response-soap.md) <br/> |<span data-ttu-id="71a6e-124">Contiene la respuesta a una solicitud de [operación GetUserSettings (SOAP)](getusersettings-operation-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="71a6e-124">Contains the response to a [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md) request.</span></span>  <br/> |
|[<span data-ttu-id="71a6e-125">UserSettingError (SOAP)</span><span class="sxs-lookup"><span data-stu-id="71a6e-125">UserSettingError (SOAP)</span></span>](usersettingerror-soap.md) <br/> |<span data-ttu-id="71a6e-126">Representa un error que se devuelve al recuperar una configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="71a6e-126">Represents an error that is returned while retrieving a user setting.</span></span>  <br/> |
|[<span data-ttu-id="71a6e-127">UserResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="71a6e-127">UserResponse (SOAP)</span></span>](userresponse-soap.md) <br/> |<span data-ttu-id="71a6e-128">Representa una respuesta a una solicitud de [operación GetUserSettings (SOAP)](getusersettings-operation-soap.md) para un usuario individual.</span><span class="sxs-lookup"><span data-stu-id="71a6e-128">Represents a response to a [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md) request for an individual user.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="71a6e-129">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="71a6e-129">Text value</span></span>

<span data-ttu-id="71a6e-130">El valor de texto representa el mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="71a6e-130">The text value represents the error message.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="71a6e-131">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="71a6e-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="71a6e-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="71a6e-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="71a6e-133">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="71a6e-133">Schema Name</span></span>  <br/> |<span data-ttu-id="71a6e-134">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="71a6e-134">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="71a6e-135">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="71a6e-135">Validation File</span></span>  <br/> |<span data-ttu-id="71a6e-136">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="71a6e-136">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="71a6e-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="71a6e-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="71a6e-138">Verdadero</span><span class="sxs-lookup"><span data-stu-id="71a6e-138">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="71a6e-139">Ver también</span><span class="sxs-lookup"><span data-stu-id="71a6e-139">See also</span></span>



[<span data-ttu-id="71a6e-140">Operación GetUserSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="71a6e-140">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
  
[<span data-ttu-id="71a6e-141">Operación GetDomainSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="71a6e-141">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)
  
[<span data-ttu-id="71a6e-142">Operación GetFederationInformation (SOAP)</span><span class="sxs-lookup"><span data-stu-id="71a6e-142">GetFederationInformation operation (SOAP)</span></span>](getfederationinformation-operation-soap.md)

