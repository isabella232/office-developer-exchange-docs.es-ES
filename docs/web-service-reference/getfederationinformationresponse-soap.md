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
description: El elemento GetFederationInformationResponse contiene la respuesta de operación GetFederationInformation (SOAP).
ms.openlocfilehash: c9e65a2b1759946b8493b3c730f08df6fe353fd8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460046"
---
# <a name="getfederationinformationresponse-soap"></a><span data-ttu-id="cdbce-103">GetFederationInformationResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="cdbce-103">GetFederationInformationResponse (SOAP)</span></span>

<span data-ttu-id="cdbce-104">El elemento **GetFederationInformationResponse** contiene la respuesta de [operación GetFederationInformation (SOAP)](getfederationinformation-operation-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="cdbce-104">The **GetFederationInformationResponse** element contains the [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md) response.</span></span> 
  
```XML
<GetFederationInformationResponse>
   <ErrorCode/>
   <ErrorMessage/>
   <TokenIssuers/>
   <ApplicationUri/>
   <Domains/>
</GetFederationInformationResponse>
```

 <span data-ttu-id="cdbce-105">**GetFederationInformationResponse**</span><span class="sxs-lookup"><span data-stu-id="cdbce-105">**GetFederationInformationResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cdbce-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="cdbce-106">Attributes and elements</span></span>

<span data-ttu-id="cdbce-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="cdbce-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cdbce-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="cdbce-108">Attributes</span></span>

<span data-ttu-id="cdbce-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="cdbce-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cdbce-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="cdbce-110">Child elements</span></span>

|<span data-ttu-id="cdbce-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="cdbce-111">**Element**</span></span>|<span data-ttu-id="cdbce-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cdbce-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cdbce-113">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="cdbce-113">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="cdbce-114">Representa un código de error devuelto por el servicio de detección automática.</span><span class="sxs-lookup"><span data-stu-id="cdbce-114">Represents an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="cdbce-115">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="cdbce-115">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="cdbce-116">Representa un mensaje que está asociado con un código de error devuelto por el servicio de detección automática.</span><span class="sxs-lookup"><span data-stu-id="cdbce-116">Represents a message that is associated with an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="cdbce-117">ApplicationUri (SOAP)</span><span class="sxs-lookup"><span data-stu-id="cdbce-117">ApplicationUri (SOAP)</span></span>](applicationuri-soap.md) <br/> |<span data-ttu-id="cdbce-118">Define la ubicación de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="cdbce-118">Defines the location of an application.</span></span>  <br/> |
|[<span data-ttu-id="cdbce-119">TokenIssuers (SOAP)</span><span class="sxs-lookup"><span data-stu-id="cdbce-119">TokenIssuers (SOAP)</span></span>](tokenissuers-soap.md) <br/> |<span data-ttu-id="cdbce-120">Representa una colección de tokens de seguridad, que contiene identificadores de servicio de token de seguridad y puntos de conexión.</span><span class="sxs-lookup"><span data-stu-id="cdbce-120">Represents a collection of security tokens, which contain security token service identifiers and endpoints.</span></span>  <br/> |
|[<span data-ttu-id="cdbce-121">Dominios (SOAP)</span><span class="sxs-lookup"><span data-stu-id="cdbce-121">Domains (SOAP)</span></span>](domains-soap.md) <br/> |<span data-ttu-id="cdbce-122">Representa los dominios de las configuraciones que se devuelven en una operación de [GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md) **GetDomainSettings** o los dominios que la organización ha federado en una operación de [GetFederationInformation (SOAP)](getfederationinformation-operation-soap.md) **GetFederationInformation** .</span><span class="sxs-lookup"><span data-stu-id="cdbce-122">Represents the domains the configurations for which are returned in a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) **GetDomainSettings** operation or the domains the organization has federated in a [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md) **GetFederationInformation** operation.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="cdbce-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="cdbce-123">Parent elements</span></span>

<span data-ttu-id="cdbce-124">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="cdbce-124">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="cdbce-125">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="cdbce-125">Text value</span></span>

<span data-ttu-id="cdbce-126">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="cdbce-126">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cdbce-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="cdbce-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cdbce-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="cdbce-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="cdbce-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="cdbce-129">Schema Name</span></span>  <br/> |<span data-ttu-id="cdbce-130">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="cdbce-130">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="cdbce-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="cdbce-131">Validation File</span></span>  <br/> |<span data-ttu-id="cdbce-132">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="cdbce-132">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="cdbce-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="cdbce-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="cdbce-134">Verdadero</span><span class="sxs-lookup"><span data-stu-id="cdbce-134">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cdbce-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="cdbce-135">See also</span></span>



[<span data-ttu-id="cdbce-136">Operación GetFederationInformation (SOAP)</span><span class="sxs-lookup"><span data-stu-id="cdbce-136">GetFederationInformation operation (SOAP)</span></span>](getfederationinformation-operation-soap.md)

