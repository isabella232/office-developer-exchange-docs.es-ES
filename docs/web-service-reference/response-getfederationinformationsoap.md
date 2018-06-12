---
title: Respuesta (GetFederationInformation) (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: ca48a4b3-5006-4bb7-973e-d9137ce67e16
description: El elemento de respuesta contiene la información de respuesta GetFederationInformation operación (SOAP).
ms.openlocfilehash: 946cba56d7503a0e20ec59640f4f1258c00a844e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837171"
---
# <a name="response-getfederationinformation-soap"></a><span data-ttu-id="8f80c-103">Respuesta (GetFederationInformation) (SOAP)</span><span class="sxs-lookup"><span data-stu-id="8f80c-103">Response (GetFederationInformation) (SOAP)</span></span>

<span data-ttu-id="8f80c-104">El elemento de **respuesta** contiene la información de respuesta de la [operación de GetFederationInformation (SOAP)](getfederationinformation-operation-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="8f80c-104">The **Response** element contains the [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md) response information.</span></span> 
  
```XML
<Response>
   <ErrorCode/>
   <ErrorMessage/>
   <ApplicationUri/>
   <Domains/>
</Response>
```

 <span data-ttu-id="8f80c-105">**GetFederationInformationResponse**</span><span class="sxs-lookup"><span data-stu-id="8f80c-105">**GetFederationInformationResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8f80c-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="8f80c-106">Attributes and elements</span></span>

<span data-ttu-id="8f80c-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="8f80c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8f80c-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="8f80c-108">Attributes</span></span>

<span data-ttu-id="8f80c-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="8f80c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8f80c-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8f80c-110">Child elements</span></span>

|<span data-ttu-id="8f80c-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="8f80c-111">**Element**</span></span>|<span data-ttu-id="8f80c-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8f80c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8f80c-113">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="8f80c-113">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="8f80c-114">Representa un código de error devuelto por el servicio Detección automática.</span><span class="sxs-lookup"><span data-stu-id="8f80c-114">Represents an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="8f80c-115">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="8f80c-115">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="8f80c-116">Representa un mensaje en el que está asociado con un código de error devuelto por el servicio Detección automática.</span><span class="sxs-lookup"><span data-stu-id="8f80c-116">Represents a message that is associated with an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="8f80c-117">ApplicationUri (SOAP)</span><span class="sxs-lookup"><span data-stu-id="8f80c-117">ApplicationUri (SOAP)</span></span>](applicationuri-soap.md) <br/> |<span data-ttu-id="8f80c-118">Define la ubicación de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="8f80c-118">Defines the location of an application.</span></span>  <br/> |
|[<span data-ttu-id="8f80c-119">Dominios (SOAP)</span><span class="sxs-lookup"><span data-stu-id="8f80c-119">Domains (SOAP)</span></span>](domains-soap.md) <br/> |<span data-ttu-id="8f80c-120">Representa la colección de dominio las configuraciones para la que se devuelven en una [operación de GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md)o los dominios que la organización ha federados en una [operación de GetFederationInformation (SOAP)](getfederationinformation-operation-soap.md).</span><span class="sxs-lookup"><span data-stu-id="8f80c-120">Represents the domain collection the configurations for which are returned in a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md), or the domains that the organization has federated in a [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md).</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8f80c-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="8f80c-121">Parent elements</span></span>

|<span data-ttu-id="8f80c-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="8f80c-122">**Element**</span></span>|<span data-ttu-id="8f80c-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8f80c-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8f80c-124">GetFederationInformationResponseMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="8f80c-124">GetFederationInformationResponseMessage (SOAP)</span></span>](getfederationinformationresponsemessage-soap.md) <br/> |<span data-ttu-id="8f80c-125">Define una respuesta a una solicitud de [operación GetFederationInformation (SOAP)](getfederationinformation-operation-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="8f80c-125">Defines a response to a [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="8f80c-126">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="8f80c-126">Text value</span></span>

<span data-ttu-id="8f80c-127">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="8f80c-127">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8f80c-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="8f80c-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8f80c-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8f80c-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="8f80c-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="8f80c-130">Schema Name</span></span>  <br/> |<span data-ttu-id="8f80c-131">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="8f80c-131">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="8f80c-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="8f80c-132">Validation File</span></span>  <br/> |<span data-ttu-id="8f80c-133">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="8f80c-133">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8f80c-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="8f80c-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="8f80c-135">Verdadero</span><span class="sxs-lookup"><span data-stu-id="8f80c-135">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8f80c-136">Ver también</span><span class="sxs-lookup"><span data-stu-id="8f80c-136">See also</span></span>



[<span data-ttu-id="8f80c-137">Operación GetFederationInformation (SOAP)</span><span class="sxs-lookup"><span data-stu-id="8f80c-137">GetFederationInformation operation (SOAP)</span></span>](getfederationinformation-operation-soap.md)

