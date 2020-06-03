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
ms.openlocfilehash: 2c76b9691fe88657a65130ef6829e5af64380d95
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526322"
---
# <a name="domainresponses-soap"></a><span data-ttu-id="dbead-103">DomainResponses (SOAP)</span><span class="sxs-lookup"><span data-stu-id="dbead-103">DomainResponses (SOAP)</span></span>

<span data-ttu-id="dbead-104">El elemento **DomainResponses** contiene una matriz de respuestas para la configuración de cada dominio solicitado.</span><span class="sxs-lookup"><span data-stu-id="dbead-104">The **DomainResponses** element contains an array of responses for each requested domain's settings.</span></span> 
  
```XML
<DomainResponses>
   <DomainResponse/>
</DomainResponses>
```

 <span data-ttu-id="dbead-105">**ArrayOfDomainResponse**</span><span class="sxs-lookup"><span data-stu-id="dbead-105">**ArrayOfDomainResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="dbead-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="dbead-106">Attributes and elements</span></span>

<span data-ttu-id="dbead-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="dbead-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dbead-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="dbead-108">Attributes</span></span>

<span data-ttu-id="dbead-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="dbead-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dbead-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="dbead-110">Child elements</span></span>

|<span data-ttu-id="dbead-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="dbead-111">**Element**</span></span>|<span data-ttu-id="dbead-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dbead-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dbead-113">DomainResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="dbead-113">DomainResponse (SOAP)</span></span>](domainresponse-soap.md) <br/> |<span data-ttu-id="dbead-114">Contiene la configuración solicitada para el dominio especificado.</span><span class="sxs-lookup"><span data-stu-id="dbead-114">Contains the requested settings for the specified domain.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="dbead-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="dbead-115">Parent elements</span></span>

|<span data-ttu-id="dbead-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="dbead-116">**Element**</span></span>|<span data-ttu-id="dbead-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dbead-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dbead-118">GetDomainSettingsResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="dbead-118">GetDomainSettingsResponse (SOAP)</span></span>](getdomainsettingsresponse-soap.md) <br/> |<span data-ttu-id="dbead-119">Representa la respuesta a una solicitud de [operación de GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md) para un dominio y devuelve la configuración del dominio.</span><span class="sxs-lookup"><span data-stu-id="dbead-119">Represents the response to a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) request for a domain, and returns the domain settings.</span></span>  <br/> |
|[<span data-ttu-id="dbead-120">Response (GetDomainSettings) (SOAP)</span><span class="sxs-lookup"><span data-stu-id="dbead-120">Response (GetDomainSettings) (SOAP)</span></span>](response-getdomainsettingssoap.md) <br/> |<span data-ttu-id="dbead-121">Representa la respuesta a una llamada de [operación de GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md) para un dominio individual.</span><span class="sxs-lookup"><span data-stu-id="dbead-121">Represents the response to a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) call for an individual domain.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="dbead-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="dbead-122">Text value</span></span>

<span data-ttu-id="dbead-123">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="dbead-123">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dbead-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="dbead-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dbead-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="dbead-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="dbead-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="dbead-126">Schema Name</span></span>  <br/> |<span data-ttu-id="dbead-127">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="dbead-127">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="dbead-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="dbead-128">Validation File</span></span>  <br/> |<span data-ttu-id="dbead-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="dbead-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="dbead-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="dbead-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="dbead-131">Verdadero</span><span class="sxs-lookup"><span data-stu-id="dbead-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dbead-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="dbead-132">See also</span></span>

- [<span data-ttu-id="dbead-133">Operación GetDomainSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="dbead-133">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

