---
title: GetFederationInformationResponse (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 2033c14f-dcc8-43c2-9fd9-a51946ec7055
description: El elemento GetFederationInformationResponse contiene la respuesta de la operación (SOAP) GetFederationInformation.
ms.openlocfilehash: 28b002b45968278ad4c7160b4eed29721422646d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764846"
---
# <a name="getfederationinformationresponse-soap"></a><span data-ttu-id="b6077-103">GetFederationInformationResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b6077-103">GetFederationInformationResponse (SOAP)</span></span>

<span data-ttu-id="b6077-104">El elemento **GetFederationInformationResponse** contiene la respuesta de la [operación de GetFederationInformation (SOAP)](getfederationinformation-operation-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="b6077-104">The **GetFederationInformationResponse** element contains the [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md) response.</span></span> 
  
```XML
<GetFederationInformationResponse>
   <ErrorCode/>
   <ErrorMessage/>
   <TokenIssuers/>
   <ApplicationUri/>
   <Domains/>
</GetFederationInformationResponse>
```

 <span data-ttu-id="b6077-105">**GetFederationInformationResponse**</span><span class="sxs-lookup"><span data-stu-id="b6077-105">**GetFederationInformationResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b6077-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b6077-106">Attributes and elements</span></span>

<span data-ttu-id="b6077-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b6077-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b6077-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="b6077-108">Attributes</span></span>

<span data-ttu-id="b6077-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b6077-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b6077-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b6077-110">Child elements</span></span>

|<span data-ttu-id="b6077-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="b6077-111">**Element**</span></span>|<span data-ttu-id="b6077-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b6077-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b6077-113">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b6077-113">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="b6077-114">Representa un código de error devuelto por el servicio Detección automática.</span><span class="sxs-lookup"><span data-stu-id="b6077-114">Represents an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="b6077-115">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b6077-115">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="b6077-116">Representa un mensaje en el que está asociado con un código de error devuelto por el servicio Detección automática.</span><span class="sxs-lookup"><span data-stu-id="b6077-116">Represents a message that is associated with an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="b6077-117">ApplicationUri (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b6077-117">ApplicationUri (SOAP)</span></span>](applicationuri-soap.md) <br/> |<span data-ttu-id="b6077-118">Define la ubicación de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="b6077-118">Defines the location of an application.</span></span>  <br/> |
|[<span data-ttu-id="b6077-119">TokenIssuers (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b6077-119">TokenIssuers (SOAP)</span></span>](tokenissuers-soap.md) <br/> |<span data-ttu-id="b6077-120">Representa una colección de tokens de seguridad, que contienen los extremos y los identificadores del servicio de token de seguridad.</span><span class="sxs-lookup"><span data-stu-id="b6077-120">Represents a collection of security tokens, which contain security token service identifiers and endpoints.</span></span>  <br/> |
|[<span data-ttu-id="b6077-121">Dominios (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b6077-121">Domains (SOAP)</span></span>](domains-soap.md) <br/> |<span data-ttu-id="b6077-122">Representa los dominios de las configuraciones para la que se devuelven en una operación de la [operación de GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md) **GetDomainSettings** o los dominios de que la organización ha federados en una [operación de GetFederationInformation (SOAP)](getfederationinformation-operation-soap.md) Operación **GetFederationInformation** .</span><span class="sxs-lookup"><span data-stu-id="b6077-122">Represents the domains the configurations for which are returned in a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) **GetDomainSettings** operation or the domains the organization has federated in a [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md) **GetFederationInformation** operation.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b6077-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b6077-123">Parent elements</span></span>

<span data-ttu-id="b6077-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b6077-124">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="b6077-125">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="b6077-125">Text value</span></span>

<span data-ttu-id="b6077-126">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b6077-126">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b6077-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b6077-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b6077-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b6077-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="b6077-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b6077-129">Schema Name</span></span>  <br/> |<span data-ttu-id="b6077-130">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="b6077-130">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="b6077-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b6077-131">Validation File</span></span>  <br/> |<span data-ttu-id="b6077-132">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b6077-132">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b6077-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b6077-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="b6077-134">Verdadero</span><span class="sxs-lookup"><span data-stu-id="b6077-134">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b6077-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="b6077-135">See also</span></span>



[<span data-ttu-id="b6077-136">Operación GetFederationInformation (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b6077-136">GetFederationInformation operation (SOAP)</span></span>](getfederationinformation-operation-soap.md)

