---
title: Request (GetDomainSettings) (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 3ea026fc-74f1-4118-86ae-908ed4f82a4b
description: El elemento request contiene una solicitud para devolver la configuración del dominio.
ms.openlocfilehash: c5f666102be8aaeee001a23706732e9e6c44b560
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459591"
---
# <a name="request-getdomainsettings-soap"></a><span data-ttu-id="7f35b-103">Request (GetDomainSettings) (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7f35b-103">Request (GetDomainSettings) (SOAP)</span></span>

<span data-ttu-id="7f35b-104">El elemento **request** contiene una solicitud para devolver la configuración del dominio.</span><span class="sxs-lookup"><span data-stu-id="7f35b-104">The **Request** element contains a request to return domain settings.</span></span> 
  
```xml
<Request>
   <Domains/>
   <RequestedSettings/>
</Request>
```

 <span data-ttu-id="7f35b-105">**GetDomainSettingsRequest**</span><span class="sxs-lookup"><span data-stu-id="7f35b-105">**GetDomainSettingsRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7f35b-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="7f35b-106">Attributes and elements</span></span>

<span data-ttu-id="7f35b-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="7f35b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7f35b-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="7f35b-108">Attributes</span></span>

<span data-ttu-id="7f35b-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="7f35b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7f35b-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7f35b-110">Child elements</span></span>

|<span data-ttu-id="7f35b-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7f35b-111">**Element**</span></span>|<span data-ttu-id="7f35b-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7f35b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7f35b-113">Dominios (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7f35b-113">Domains (SOAP)</span></span>](domains-soap.md) <br/> |<span data-ttu-id="7f35b-114">Representa los dominios de las configuraciones que se devuelven en una [operación GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md) o los dominios que la organización ha federado en una [operación GetFederationInformation (SOAP)](getfederationinformation-operation-soap.md).</span><span class="sxs-lookup"><span data-stu-id="7f35b-114">Represents the domains the configurations for which are returned in a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) or the domains the organization has federated in a [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md).</span></span>  <br/> |
|[<span data-ttu-id="7f35b-115">RequestedSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7f35b-115">RequestedSettings (SOAP)</span></span>](requestedsettings-soap.md) <br/> |<span data-ttu-id="7f35b-116">Contiene los nombres de las opciones de configuración solicitadas.</span><span class="sxs-lookup"><span data-stu-id="7f35b-116">Contains the names of the requested configuration settings.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7f35b-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7f35b-117">Parent elements</span></span>

|<span data-ttu-id="7f35b-118">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7f35b-118">**Element**</span></span>|<span data-ttu-id="7f35b-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7f35b-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7f35b-120">GetDomainSettingsRequestMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7f35b-120">GetDomainSettingsRequestMessage (SOAP)</span></span>](getdomainsettingsrequestmessage-soap.md) <br/> |<span data-ttu-id="7f35b-121">Representa una solicitud de [operación de GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md).</span><span class="sxs-lookup"><span data-stu-id="7f35b-121">Represents a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md)request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7f35b-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="7f35b-122">Text value</span></span>

<span data-ttu-id="7f35b-123">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="7f35b-123">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7f35b-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7f35b-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7f35b-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="7f35b-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="7f35b-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="7f35b-126">Schema Name</span></span>  <br/> |<span data-ttu-id="7f35b-127">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="7f35b-127">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="7f35b-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="7f35b-128">Validation File</span></span>  <br/> |<span data-ttu-id="7f35b-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="7f35b-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7f35b-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="7f35b-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="7f35b-131">Verdadero</span><span class="sxs-lookup"><span data-stu-id="7f35b-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7f35b-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="7f35b-132">See also</span></span>



[<span data-ttu-id="7f35b-133">Operación GetDomainSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7f35b-133">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

