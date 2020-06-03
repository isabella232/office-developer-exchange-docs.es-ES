---
title: Response (GetFederationInformation) (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: ca48a4b3-5006-4bb7-973e-d9137ce67e16
description: El elemento Response contiene la información de respuesta de la operación GetFederationInformation (SOAP).
ms.openlocfilehash: 0b9a2c518b968faa6ef86b7c1f544eac40f8e5c8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530589"
---
# <a name="response-getfederationinformation-soap"></a><span data-ttu-id="72f90-103">Response (GetFederationInformation) (SOAP)</span><span class="sxs-lookup"><span data-stu-id="72f90-103">Response (GetFederationInformation) (SOAP)</span></span>

<span data-ttu-id="72f90-104">El elemento **Response** contiene la información de respuesta de la [operación GetFederationInformation (SOAP)](getfederationinformation-operation-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="72f90-104">The **Response** element contains the [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md) response information.</span></span> 
  
```XML
<Response>
   <ErrorCode/>
   <ErrorMessage/>
   <ApplicationUri/>
   <Domains/>
</Response>
```

 <span data-ttu-id="72f90-105">**GetFederationInformationResponse**</span><span class="sxs-lookup"><span data-stu-id="72f90-105">**GetFederationInformationResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="72f90-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="72f90-106">Attributes and elements</span></span>

<span data-ttu-id="72f90-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="72f90-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="72f90-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="72f90-108">Attributes</span></span>

<span data-ttu-id="72f90-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="72f90-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="72f90-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="72f90-110">Child elements</span></span>

|<span data-ttu-id="72f90-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="72f90-111">**Element**</span></span>|<span data-ttu-id="72f90-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="72f90-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="72f90-113">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="72f90-113">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="72f90-114">Representa un código de error devuelto por el servicio de detección automática.</span><span class="sxs-lookup"><span data-stu-id="72f90-114">Represents an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="72f90-115">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="72f90-115">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="72f90-116">Representa un mensaje que está asociado con un código de error devuelto por el servicio de detección automática.</span><span class="sxs-lookup"><span data-stu-id="72f90-116">Represents a message that is associated with an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="72f90-117">ApplicationUri (SOAP)</span><span class="sxs-lookup"><span data-stu-id="72f90-117">ApplicationUri (SOAP)</span></span>](applicationuri-soap.md) <br/> |<span data-ttu-id="72f90-118">Define la ubicación de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="72f90-118">Defines the location of an application.</span></span>  <br/> |
|[<span data-ttu-id="72f90-119">Dominios (SOAP)</span><span class="sxs-lookup"><span data-stu-id="72f90-119">Domains (SOAP)</span></span>](domains-soap.md) <br/> |<span data-ttu-id="72f90-120">Representa la colección de dominios cuyas configuraciones se devuelven en una [operación GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md)o los dominios que la organización ha federado en una [operación GetFederationInformation (SOAP)](getfederationinformation-operation-soap.md).</span><span class="sxs-lookup"><span data-stu-id="72f90-120">Represents the domain collection the configurations for which are returned in a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md), or the domains that the organization has federated in a [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md).</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="72f90-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="72f90-121">Parent elements</span></span>

|<span data-ttu-id="72f90-122">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="72f90-122">**Element**</span></span>|<span data-ttu-id="72f90-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="72f90-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="72f90-124">GetFederationInformationResponseMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="72f90-124">GetFederationInformationResponseMessage (SOAP)</span></span>](getfederationinformationresponsemessage-soap.md) <br/> |<span data-ttu-id="72f90-125">Define una respuesta a una solicitud de [operación de GetFederationInformation (SOAP)](getfederationinformation-operation-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="72f90-125">Defines a response to a [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="72f90-126">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="72f90-126">Text value</span></span>

<span data-ttu-id="72f90-127">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="72f90-127">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="72f90-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="72f90-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="72f90-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="72f90-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="72f90-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="72f90-130">Schema Name</span></span>  <br/> |<span data-ttu-id="72f90-131">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="72f90-131">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="72f90-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="72f90-132">Validation File</span></span>  <br/> |<span data-ttu-id="72f90-133">messages. xsd</span><span class="sxs-lookup"><span data-stu-id="72f90-133">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="72f90-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="72f90-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="72f90-135">Verdadero</span><span class="sxs-lookup"><span data-stu-id="72f90-135">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="72f90-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="72f90-136">See also</span></span>



[<span data-ttu-id="72f90-137">Operación GetFederationInformation (SOAP)</span><span class="sxs-lookup"><span data-stu-id="72f90-137">GetFederationInformation operation (SOAP)</span></span>](getfederationinformation-operation-soap.md)

