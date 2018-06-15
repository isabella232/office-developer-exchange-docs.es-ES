---
title: Solicitud (SOAP) (GetDomainSettings)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 3ea026fc-74f1-4118-86ae-908ed4f82a4b
description: El elemento de solicitud contiene una solicitud para devolver la configuración de dominio.
ms.openlocfilehash: 71a6072d476fd665dad8b0c0fe388a40db56e059
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837135"
---
# <a name="request-getdomainsettings-soap"></a><span data-ttu-id="c3c8c-103">Solicitud (SOAP) (GetDomainSettings)</span><span class="sxs-lookup"><span data-stu-id="c3c8c-103">Request (GetDomainSettings) (SOAP)</span></span>

<span data-ttu-id="c3c8c-104">El elemento de **solicitud** contiene una solicitud para devolver la configuración de dominio.</span><span class="sxs-lookup"><span data-stu-id="c3c8c-104">The **Request** element contains a request to return domain settings.</span></span> 
  
```xml
<Request>
   <Domains/>
   <RequestedSettings/>
</Request>
```

 <span data-ttu-id="c3c8c-105">**GetDomainSettingsRequest**</span><span class="sxs-lookup"><span data-stu-id="c3c8c-105">**GetDomainSettingsRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c3c8c-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c3c8c-106">Attributes and elements</span></span>

<span data-ttu-id="c3c8c-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c3c8c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c3c8c-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c3c8c-108">Attributes</span></span>

<span data-ttu-id="c3c8c-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c3c8c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c3c8c-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c3c8c-110">Child elements</span></span>

|<span data-ttu-id="c3c8c-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="c3c8c-111">**Element**</span></span>|<span data-ttu-id="c3c8c-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c3c8c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c3c8c-113">Dominios (SOAP)</span><span class="sxs-lookup"><span data-stu-id="c3c8c-113">Domains (SOAP)</span></span>](domains-soap.md) <br/> |<span data-ttu-id="c3c8c-114">Representa los dominios de las configuraciones para la que se devuelven en una [operación de GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md) o los dominios de que la organización ha federados en una [operación de GetFederationInformation (SOAP)](getfederationinformation-operation-soap.md).</span><span class="sxs-lookup"><span data-stu-id="c3c8c-114">Represents the domains the configurations for which are returned in a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) or the domains the organization has federated in a [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md).</span></span>  <br/> |
|[<span data-ttu-id="c3c8c-115">RequestedSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="c3c8c-115">RequestedSettings (SOAP)</span></span>](requestedsettings-soap.md) <br/> |<span data-ttu-id="c3c8c-116">Contiene los nombres de las opciones de configuración solicitado.</span><span class="sxs-lookup"><span data-stu-id="c3c8c-116">Contains the names of the requested configuration settings.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c3c8c-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c3c8c-117">Parent elements</span></span>

|<span data-ttu-id="c3c8c-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="c3c8c-118">**Element**</span></span>|<span data-ttu-id="c3c8c-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c3c8c-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c3c8c-120">GetDomainSettingsRequestMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="c3c8c-120">GetDomainSettingsRequestMessage (SOAP)</span></span>](getdomainsettingsrequestmessage-soap.md) <br/> |<span data-ttu-id="c3c8c-121">Representa una solicitud de [operación GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md).</span><span class="sxs-lookup"><span data-stu-id="c3c8c-121">Represents a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md)request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c3c8c-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="c3c8c-122">Text value</span></span>

<span data-ttu-id="c3c8c-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c3c8c-123">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c3c8c-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c3c8c-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c3c8c-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c3c8c-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="c3c8c-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c3c8c-126">Schema Name</span></span>  <br/> |<span data-ttu-id="c3c8c-127">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="c3c8c-127">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="c3c8c-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c3c8c-128">Validation File</span></span>  <br/> |<span data-ttu-id="c3c8c-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="c3c8c-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c3c8c-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c3c8c-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="c3c8c-131">Verdadero</span><span class="sxs-lookup"><span data-stu-id="c3c8c-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c3c8c-132">Ver también</span><span class="sxs-lookup"><span data-stu-id="c3c8c-132">See also</span></span>



[<span data-ttu-id="c3c8c-133">Operación GetDomainSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="c3c8c-133">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)
