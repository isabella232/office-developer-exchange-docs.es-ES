---
title: Dominios (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 5f81d1b7-c6a4-456f-9935-13d04a3d92d7
description: El elemento de dominios representa la colección de dominio que se devuelve en una operación de GetDomainSettings (SOAP), los dominios que la organización ha federados en una operación de GetFederationInformation (SOAP) o los dominios con una relación de organización como devuelto por la operación de GetOrganizationRelationshipSettings (SOAP).
ms.openlocfilehash: 7a21a3a09516de2d1c38021ca3ccd2161d9cdd1e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764272"
---
# <a name="domains-soap"></a><span data-ttu-id="51898-103">Dominios (SOAP)</span><span class="sxs-lookup"><span data-stu-id="51898-103">Domains (SOAP)</span></span>

<span data-ttu-id="51898-104">El elemento de **dominios** representa la colección de dominio que se devuelve en una [operación de GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md), los dominios que la organización ha federados en una [operación de GetFederationInformation (SOAP)](getfederationinformation-operation-soap.md)o los dominios con una relación de la organización como devuelto por la [operación de GetOrganizationRelationshipSettings (SOAP)](getorganizationrelationshipsettings-operation-soap.md).</span><span class="sxs-lookup"><span data-stu-id="51898-104">The **Domains** element represents the domain collection that is returned in a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md), the domains that the organization has federated in a [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md), or the domains with an organization relationship as returned by [GetOrganizationRelationshipSettings operation (SOAP)](getorganizationrelationshipsettings-operation-soap.md).</span></span>
  
```XML
<Domains>
   <Domain/>
</Domains>
```

 <span data-ttu-id="51898-105">**Dominios**</span><span class="sxs-lookup"><span data-stu-id="51898-105">**Domains**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="51898-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="51898-106">Attributes and elements</span></span>

<span data-ttu-id="51898-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="51898-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="51898-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="51898-108">Attributes</span></span>

<span data-ttu-id="51898-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="51898-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="51898-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="51898-110">Child elements</span></span>

|<span data-ttu-id="51898-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="51898-111">**Element**</span></span>|<span data-ttu-id="51898-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="51898-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="51898-113">Dominio (SOAP)</span><span class="sxs-lookup"><span data-stu-id="51898-113">Domain (SOAP)</span></span>](domain-soap.md) <br/> |<span data-ttu-id="51898-114">Representa un solo dominio.</span><span class="sxs-lookup"><span data-stu-id="51898-114">Represents a single domain.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="51898-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="51898-115">Parent elements</span></span>

|<span data-ttu-id="51898-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="51898-116">**Element**</span></span>|<span data-ttu-id="51898-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="51898-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="51898-118">GetDomainSettingsRequest (SOAP)</span><span class="sxs-lookup"><span data-stu-id="51898-118">GetDomainSettingsRequest (SOAP)</span></span>](getdomainsettingsrequest-soap.md) <br/> |<span data-ttu-id="51898-119">Representa una solicitud de [operación GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="51898-119">Represents a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) request.</span></span>  <br/> |
|[<span data-ttu-id="51898-120">Respuesta (GetFederationInformation) (SOAP)</span><span class="sxs-lookup"><span data-stu-id="51898-120">Response (GetFederationInformation) (SOAP)</span></span>](response-getfederationinformationsoap.md) <br/> |<span data-ttu-id="51898-121">Contiene la información de respuesta de la [operación de GetFederationInformation (SOAP)](getfederationinformation-operation-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="51898-121">Contains the [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md) response information.</span></span>  <br/> |
|[<span data-ttu-id="51898-122">GetOrganizationRelationshipSettingsRequest (SOAP)</span><span class="sxs-lookup"><span data-stu-id="51898-122">GetOrganizationRelationshipSettingsRequest (SOAP)</span></span>](getorganizationrelationshipsettingsrequest-soap.md) <br/> |<span data-ttu-id="51898-123">Representa una solicitud de [operación GetOrganizationRelationshipSettings (SOAP)](getorganizationrelationshipsettings-operation-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="51898-123">Represents a [GetOrganizationRelationshipSettings operation (SOAP)](getorganizationrelationshipsettings-operation-soap.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="51898-124">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="51898-124">Text value</span></span>

<span data-ttu-id="51898-125">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="51898-125">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="51898-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="51898-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="51898-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="51898-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="51898-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="51898-128">Schema Name</span></span>  <br/> |<span data-ttu-id="51898-129">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="51898-129">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="51898-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="51898-130">Validation File</span></span>  <br/> |<span data-ttu-id="51898-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="51898-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="51898-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="51898-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="51898-133">Verdadero</span><span class="sxs-lookup"><span data-stu-id="51898-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="51898-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="51898-134">See also</span></span>

- [<span data-ttu-id="51898-135">GetDomainSettingsRequest (SOAP)</span><span class="sxs-lookup"><span data-stu-id="51898-135">GetDomainSettingsRequest (SOAP)</span></span>](getdomainsettingsrequest-soap.md)  
- [<span data-ttu-id="51898-136">GetFederationInformationResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="51898-136">GetFederationInformationResponse (SOAP)</span></span>](getfederationinformationresponse-soap.md)

