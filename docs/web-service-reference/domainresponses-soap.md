---
title: DomainResponses (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: d9c7fd91-22cd-4c72-a841-25cb9d415e0c
description: El elemento DomainResponses contiene una matriz de respuestas para la configuración de cada dominio solicitado.
ms.openlocfilehash: 77a3efc1605337ab436f6aea2b61a67f22e4f8ce
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764271"
---
# <a name="domainresponses-soap"></a><span data-ttu-id="afb7c-103">DomainResponses (SOAP)</span><span class="sxs-lookup"><span data-stu-id="afb7c-103">DomainResponses (SOAP)</span></span>

<span data-ttu-id="afb7c-104">El elemento **DomainResponses** contiene una matriz de respuestas para la configuración de cada dominio solicitado.</span><span class="sxs-lookup"><span data-stu-id="afb7c-104">The **DomainResponses** element contains an array of responses for each requested domain's settings.</span></span> 
  
```XML
<DomainResponses>
   <DomainResponse/>
</DomainResponses>
```

 <span data-ttu-id="afb7c-105">**ArrayOfDomainResponse**</span><span class="sxs-lookup"><span data-stu-id="afb7c-105">**ArrayOfDomainResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="afb7c-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="afb7c-106">Attributes and elements</span></span>

<span data-ttu-id="afb7c-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="afb7c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="afb7c-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="afb7c-108">Attributes</span></span>

<span data-ttu-id="afb7c-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="afb7c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="afb7c-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="afb7c-110">Child elements</span></span>

|<span data-ttu-id="afb7c-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="afb7c-111">**Element**</span></span>|<span data-ttu-id="afb7c-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="afb7c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="afb7c-113">DomainResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="afb7c-113">DomainResponse (SOAP)</span></span>](domainresponse-soap.md) <br/> |<span data-ttu-id="afb7c-114">Contiene la configuración solicitada para el dominio especificado.</span><span class="sxs-lookup"><span data-stu-id="afb7c-114">Contains the requested settings for the specified domain.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="afb7c-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="afb7c-115">Parent elements</span></span>

|<span data-ttu-id="afb7c-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="afb7c-116">**Element**</span></span>|<span data-ttu-id="afb7c-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="afb7c-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="afb7c-118">GetDomainSettingsResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="afb7c-118">GetDomainSettingsResponse (SOAP)</span></span>](getdomainsettingsresponse-soap.md) <br/> |<span data-ttu-id="afb7c-119">Representa la respuesta a una solicitud de [operación GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md) para un dominio y devuelve la configuración de dominio.</span><span class="sxs-lookup"><span data-stu-id="afb7c-119">Represents the response to a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) request for a domain, and returns the domain settings.</span></span>  <br/> |
|[<span data-ttu-id="afb7c-120">Respuesta (GetDomainSettings) (SOAP)</span><span class="sxs-lookup"><span data-stu-id="afb7c-120">Response (GetDomainSettings) (SOAP)</span></span>](response-getdomainsettingssoap.md) <br/> |<span data-ttu-id="afb7c-121">Representa la respuesta a una llamada a una [operación de GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md) para un dominio individual.</span><span class="sxs-lookup"><span data-stu-id="afb7c-121">Represents the response to a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) call for an individual domain.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="afb7c-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="afb7c-122">Text value</span></span>

<span data-ttu-id="afb7c-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="afb7c-123">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="afb7c-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="afb7c-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="afb7c-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="afb7c-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="afb7c-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="afb7c-126">Schema Name</span></span>  <br/> |<span data-ttu-id="afb7c-127">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="afb7c-127">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="afb7c-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="afb7c-128">Validation File</span></span>  <br/> |<span data-ttu-id="afb7c-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="afb7c-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="afb7c-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="afb7c-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="afb7c-131">Verdadero</span><span class="sxs-lookup"><span data-stu-id="afb7c-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="afb7c-132">Ver también</span><span class="sxs-lookup"><span data-stu-id="afb7c-132">See also</span></span>

- [<span data-ttu-id="afb7c-133">Operación GetDomainSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="afb7c-133">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

