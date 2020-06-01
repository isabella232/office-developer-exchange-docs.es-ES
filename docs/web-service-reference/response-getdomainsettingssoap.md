---
title: Response (GetDomainSettings) (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: a5b052df-93bd-4fe1-ac30-83de9a3dfcd7
description: El elemento Response representa la respuesta a una llamada de GetDomainSettings para un dominio individual.
ms.openlocfilehash: 67fe7aea4533058fa0df972e49a2069749dc258b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455586"
---
# <a name="response-getdomainsettings-soap"></a><span data-ttu-id="a9b59-103">Response (GetDomainSettings) (SOAP)</span><span class="sxs-lookup"><span data-stu-id="a9b59-103">Response (GetDomainSettings) (SOAP)</span></span>

<span data-ttu-id="a9b59-104">El elemento **Response** representa la respuesta a una llamada de **GetDomainSettings** para un dominio individual.</span><span class="sxs-lookup"><span data-stu-id="a9b59-104">The **Response** element represents the response to a **GetDomainSettings** call for an individual domain.</span></span> 
  
```XML
<Response>
   <DomainResponses/>
   <ErrorCode/>
   <ErrorMessage/>
</Response>
```

 <span data-ttu-id="a9b59-105">**GetDomainSettingsResponse**</span><span class="sxs-lookup"><span data-stu-id="a9b59-105">**GetDomainSettingsResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a9b59-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a9b59-106">Attributes and elements</span></span>

<span data-ttu-id="a9b59-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a9b59-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a9b59-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="a9b59-108">Attributes</span></span>

<span data-ttu-id="a9b59-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="a9b59-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a9b59-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a9b59-110">Child elements</span></span>

|<span data-ttu-id="a9b59-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a9b59-111">**Element**</span></span>|<span data-ttu-id="a9b59-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a9b59-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a9b59-113">DomainResponses (SOAP)</span><span class="sxs-lookup"><span data-stu-id="a9b59-113">DomainResponses (SOAP)</span></span>](domainresponses-soap.md) <br/> |<span data-ttu-id="a9b59-114">Contiene la respuesta para cada dominio solicitado en una solicitud **GetDomainSettings** .</span><span class="sxs-lookup"><span data-stu-id="a9b59-114">Contains the response for each domain requested in a **GetDomainSettings** request.</span></span>  <br/> |
|[<span data-ttu-id="a9b59-115">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="a9b59-115">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="a9b59-116">Contiene el código de error asociado a la respuesta, si procede.</span><span class="sxs-lookup"><span data-stu-id="a9b59-116">Contains the error code that is associated with the response, if applicable.</span></span>  <br/> |
|[<span data-ttu-id="a9b59-117">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="a9b59-117">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="a9b59-118">Contiene el mensaje de error que está asociado a la respuesta, si procede.</span><span class="sxs-lookup"><span data-stu-id="a9b59-118">Contains the error message that is associated with the response, if applicable.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a9b59-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a9b59-119">Parent elements</span></span>

|<span data-ttu-id="a9b59-120">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a9b59-120">**Element**</span></span>|<span data-ttu-id="a9b59-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a9b59-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a9b59-122">GetDomainSettingsResponseMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="a9b59-122">GetDomainSettingsResponseMessage (SOAP)</span></span>](getdomainsettingsresponsemessage-soap.md) <br/> |<span data-ttu-id="a9b59-123">Devuelve al autor de la llamada los valores de configuración del dominio.</span><span class="sxs-lookup"><span data-stu-id="a9b59-123">Returns to the caller the domain configuration settings.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a9b59-124">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="a9b59-124">Text value</span></span>

<span data-ttu-id="a9b59-125">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="a9b59-125">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a9b59-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a9b59-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a9b59-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="a9b59-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="a9b59-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a9b59-128">Schema Name</span></span>  <br/> |<span data-ttu-id="a9b59-129">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="a9b59-129">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="a9b59-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a9b59-130">Validation File</span></span>  <br/> |<span data-ttu-id="a9b59-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="a9b59-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a9b59-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a9b59-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="a9b59-133">Verdadero</span><span class="sxs-lookup"><span data-stu-id="a9b59-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a9b59-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="a9b59-134">See also</span></span>



[<span data-ttu-id="a9b59-135">Operación GetDomainSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="a9b59-135">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

