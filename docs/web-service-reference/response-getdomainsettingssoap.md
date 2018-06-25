---
title: Respuesta (GetDomainSettings) (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: a5b052df-93bd-4fe1-ac30-83de9a3dfcd7
description: El elemento de respuesta representa la respuesta a una llamada GetDomainSettings para un dominio individual.
ms.openlocfilehash: 316d77104894cf5ed9121e7dab1c38646765c948
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837169"
---
# <a name="response-getdomainsettings-soap"></a><span data-ttu-id="58f89-103">Respuesta (GetDomainSettings) (SOAP)</span><span class="sxs-lookup"><span data-stu-id="58f89-103">Response (GetDomainSettings) (SOAP)</span></span>

<span data-ttu-id="58f89-104">El elemento de **respuesta** representa la respuesta a una llamada **GetDomainSettings** para un dominio individual.</span><span class="sxs-lookup"><span data-stu-id="58f89-104">The **Response** element represents the response to a **GetDomainSettings** call for an individual domain.</span></span> 
  
```XML
<Response>
   <DomainResponses/>
   <ErrorCode/>
   <ErrorMessage/>
</Response>
```

 <span data-ttu-id="58f89-105">**GetDomainSettingsResponse**</span><span class="sxs-lookup"><span data-stu-id="58f89-105">**GetDomainSettingsResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="58f89-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="58f89-106">Attributes and elements</span></span>

<span data-ttu-id="58f89-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="58f89-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="58f89-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="58f89-108">Attributes</span></span>

<span data-ttu-id="58f89-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="58f89-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="58f89-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="58f89-110">Child elements</span></span>

|<span data-ttu-id="58f89-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="58f89-111">**Element**</span></span>|<span data-ttu-id="58f89-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="58f89-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="58f89-113">DomainResponses (SOAP)</span><span class="sxs-lookup"><span data-stu-id="58f89-113">DomainResponses (SOAP)</span></span>](domainresponses-soap.md) <br/> |<span data-ttu-id="58f89-114">Contiene la respuesta para cada dominio solicitado en una solicitud de **GetDomainSettings** .</span><span class="sxs-lookup"><span data-stu-id="58f89-114">Contains the response for each domain requested in a **GetDomainSettings** request.</span></span>  <br/> |
|[<span data-ttu-id="58f89-115">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="58f89-115">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="58f89-116">Contiene el código de error que está asociado a la respuesta, si procede.</span><span class="sxs-lookup"><span data-stu-id="58f89-116">Contains the error code that is associated with the response, if applicable.</span></span>  <br/> |
|[<span data-ttu-id="58f89-117">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="58f89-117">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="58f89-118">Contiene el mensaje de error que está asociado a la respuesta, si procede.</span><span class="sxs-lookup"><span data-stu-id="58f89-118">Contains the error message that is associated with the response, if applicable.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="58f89-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="58f89-119">Parent elements</span></span>

|<span data-ttu-id="58f89-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="58f89-120">**Element**</span></span>|<span data-ttu-id="58f89-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="58f89-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="58f89-122">GetDomainSettingsResponseMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="58f89-122">GetDomainSettingsResponseMessage (SOAP)</span></span>](getdomainsettingsresponsemessage-soap.md) <br/> |<span data-ttu-id="58f89-123">Para el autor de la llamada, devuelve el dominio de valores de configuración.</span><span class="sxs-lookup"><span data-stu-id="58f89-123">Returns to the caller the domain configuration settings.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="58f89-124">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="58f89-124">Text value</span></span>

<span data-ttu-id="58f89-125">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="58f89-125">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="58f89-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="58f89-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="58f89-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="58f89-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="58f89-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="58f89-128">Schema Name</span></span>  <br/> |<span data-ttu-id="58f89-129">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="58f89-129">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="58f89-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="58f89-130">Validation File</span></span>  <br/> |<span data-ttu-id="58f89-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="58f89-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="58f89-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="58f89-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="58f89-133">Verdadero</span><span class="sxs-lookup"><span data-stu-id="58f89-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="58f89-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="58f89-134">See also</span></span>



[<span data-ttu-id="58f89-135">Operación GetDomainSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="58f89-135">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

