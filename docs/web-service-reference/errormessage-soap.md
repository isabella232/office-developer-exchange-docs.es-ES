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
description: El elemento ErrorMessage representa un mensaje que está asociado con un código de error devuelto por el servicio de detección automática.
ms.openlocfilehash: 4ebaf91fe26083cf241826e1fc16ac184fddf57c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530645"
---
# <a name="errormessage-soap"></a><span data-ttu-id="19564-103">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="19564-103">ErrorMessage (SOAP)</span></span>

<span data-ttu-id="19564-104">El elemento **errorMessage** representa un mensaje que está asociado con un código de error devuelto por el servicio de detección automática.</span><span class="sxs-lookup"><span data-stu-id="19564-104">The **ErrorMessage** element represents a message that is associated with an error code that is returned by the Autodiscover service.</span></span> 
  
```XML
<ErrorMessage/>
```

 <span data-ttu-id="19564-105">**string**</span><span class="sxs-lookup"><span data-stu-id="19564-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="19564-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="19564-106">Attributes and elements</span></span>

<span data-ttu-id="19564-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="19564-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="19564-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="19564-108">Attributes</span></span>

<span data-ttu-id="19564-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="19564-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="19564-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="19564-110">Child elements</span></span>

<span data-ttu-id="19564-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="19564-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="19564-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="19564-112">Parent elements</span></span>

|<span data-ttu-id="19564-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="19564-113">**Element**</span></span>|<span data-ttu-id="19564-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="19564-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="19564-115">AutodiscoverResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="19564-115">AutodiscoverResponse (SOAP)</span></span>](autodiscoverresponse-soap.md) <br/> |<span data-ttu-id="19564-116">Representa el tipo base para todas las respuestas que devuelve el servicio de detección automática.</span><span class="sxs-lookup"><span data-stu-id="19564-116">Represents the base type for all responses that are returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="19564-117">DomainResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="19564-117">DomainResponse (SOAP)</span></span>](domainresponse-soap.md) <br/> |<span data-ttu-id="19564-118">Contiene la configuración solicitada para el dominio especificado.</span><span class="sxs-lookup"><span data-stu-id="19564-118">Contains the requested settings for the specified domain.</span></span>  <br/> |
|[<span data-ttu-id="19564-119">GetDomainSettingsResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="19564-119">GetDomainSettingsResponse (SOAP)</span></span>](getdomainsettingsresponse-soap.md) <br/> |<span data-ttu-id="19564-120">Contiene la respuesta a una llamada de [operación de GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md) para un dominio individual.</span><span class="sxs-lookup"><span data-stu-id="19564-120">Contains the response to a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) call for an individual domain.</span></span>  <br/> |
|[<span data-ttu-id="19564-121">GetFederationInformationResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="19564-121">GetFederationInformationResponse (SOAP)</span></span>](getfederationinformationresponse-soap.md) <br/> |<span data-ttu-id="19564-122">Contiene la respuesta a una solicitud de [operación de GetFederationInformation (SOAP)](getfederationinformation-operation-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="19564-122">Contains the response to a [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md) request.</span></span>  <br/> |
|[<span data-ttu-id="19564-123">Respuesta (SOAP)</span><span class="sxs-lookup"><span data-stu-id="19564-123">Response (SOAP)</span></span>](response-soap.md) <br/> |<span data-ttu-id="19564-124">Contiene la respuesta a una solicitud de [operación de GetUserSettings (SOAP)](getusersettings-operation-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="19564-124">Contains the response to a [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md) request.</span></span>  <br/> |
|[<span data-ttu-id="19564-125">UserSettingError (SOAP)</span><span class="sxs-lookup"><span data-stu-id="19564-125">UserSettingError (SOAP)</span></span>](usersettingerror-soap.md) <br/> |<span data-ttu-id="19564-126">Representa un error que se devuelve al recuperar una configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="19564-126">Represents an error that is returned while retrieving a user setting.</span></span>  <br/> |
|[<span data-ttu-id="19564-127">UserResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="19564-127">UserResponse (SOAP)</span></span>](userresponse-soap.md) <br/> |<span data-ttu-id="19564-128">Representa una respuesta a una solicitud de [operación de GetUserSettings (SOAP)](getusersettings-operation-soap.md) para un usuario individual.</span><span class="sxs-lookup"><span data-stu-id="19564-128">Represents a response to a [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md) request for an individual user.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="19564-129">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="19564-129">Text value</span></span>

<span data-ttu-id="19564-130">El valor de texto representa el mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="19564-130">The text value represents the error message.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="19564-131">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="19564-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="19564-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="19564-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="19564-133">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="19564-133">Schema Name</span></span>  <br/> |<span data-ttu-id="19564-134">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="19564-134">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="19564-135">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="19564-135">Validation File</span></span>  <br/> |<span data-ttu-id="19564-136">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="19564-136">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="19564-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="19564-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="19564-138">Verdadero</span><span class="sxs-lookup"><span data-stu-id="19564-138">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="19564-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="19564-139">See also</span></span>



[<span data-ttu-id="19564-140">Operación GetUserSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="19564-140">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
  
[<span data-ttu-id="19564-141">Operación GetDomainSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="19564-141">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)
  
[<span data-ttu-id="19564-142">Operación GetFederationInformation (SOAP)</span><span class="sxs-lookup"><span data-stu-id="19564-142">GetFederationInformation operation (SOAP)</span></span>](getfederationinformation-operation-soap.md)

