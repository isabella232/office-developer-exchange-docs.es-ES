---
title: DomainResponse (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 6aa319be-3a01-4044-8dfc-8fa1318524c3
description: El elemento DomainResponse contiene la configuración solicitada para el dominio especificado.
ms.openlocfilehash: c40f33a278b5032913329a7cd64346b572f5df2f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764265"
---
# <a name="domainresponse-soap"></a><span data-ttu-id="7c8e2-103">DomainResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7c8e2-103">DomainResponse (SOAP)</span></span>

<span data-ttu-id="7c8e2-104">El elemento **DomainResponse** contiene la configuración solicitada para el dominio especificado.</span><span class="sxs-lookup"><span data-stu-id="7c8e2-104">The **DomainResponse** element contains the requested settings for the specified domain.</span></span> 
  
```XML
<DomainResponse>
   <DomainSettingErrors/>
   <DomainSettings/>
   <RedirectTarget/>
   <ErrorCode/>
   <ErrorMessage/>
</DomainResponse>
```

 <span data-ttu-id="7c8e2-105">**DomainResponse**</span><span class="sxs-lookup"><span data-stu-id="7c8e2-105">**DomainResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7c8e2-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="7c8e2-106">Attributes and elements</span></span>

<span data-ttu-id="7c8e2-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="7c8e2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7c8e2-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="7c8e2-108">Attributes</span></span>

<span data-ttu-id="7c8e2-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7c8e2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7c8e2-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7c8e2-110">Child elements</span></span>

|<span data-ttu-id="7c8e2-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="7c8e2-111">**Element**</span></span>|<span data-ttu-id="7c8e2-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7c8e2-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7c8e2-113">DomainSettingErrors (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7c8e2-113">DomainSettingErrors (SOAP)</span></span>](domainsettingerrors-soap.md) <br/> |<span data-ttu-id="7c8e2-114">Contiene información de error de configuración que no se pudo devolver.</span><span class="sxs-lookup"><span data-stu-id="7c8e2-114">Contains error information for settings that could not be returned.</span></span>  <br/> |
|[<span data-ttu-id="7c8e2-115">DomainSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7c8e2-115">DomainSettings (SOAP)</span></span>](domainsettings-soap.md) <br/> |<span data-ttu-id="7c8e2-116">Representa la configuración de dominio que se ha enviado en una solicitud de detección automática o devueltas por una respuesta de detección automática.</span><span class="sxs-lookup"><span data-stu-id="7c8e2-116">Represents the domain settings that were submitted in an Autodiscover request or returned by an Autodiscover response.</span></span>  <br/> |
|[<span data-ttu-id="7c8e2-117">RedirectTarget (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7c8e2-117">RedirectTarget (SOAP)</span></span>](redirecttarget-soap.md) <br/> |<span data-ttu-id="7c8e2-118">Identifica el destino de la redirección.</span><span class="sxs-lookup"><span data-stu-id="7c8e2-118">Identifies the target of the redirection.</span></span> <span data-ttu-id="7c8e2-119">El destino puede ser una dirección URL o una dirección de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="7c8e2-119">The target can be either a URL or an e-mail address.</span></span>  <br/> |
|[<span data-ttu-id="7c8e2-120">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7c8e2-120">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="7c8e2-121">Especifica el código de error que está asociado a la solicitud específico.</span><span class="sxs-lookup"><span data-stu-id="7c8e2-121">Specifies the error code that is associated with the specific request.</span></span>  <br/> |
|[<span data-ttu-id="7c8e2-122">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7c8e2-122">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="7c8e2-123">Especifica el mensaje de error que está asociado a la solicitud específico.</span><span class="sxs-lookup"><span data-stu-id="7c8e2-123">Specifies the error message that is associated with the specific request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7c8e2-124">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7c8e2-124">Parent elements</span></span>

|<span data-ttu-id="7c8e2-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="7c8e2-125">**Element**</span></span>|<span data-ttu-id="7c8e2-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7c8e2-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7c8e2-127">ArrayOfDomainResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7c8e2-127">ArrayOfDomainResponse (SOAP)</span></span>](arrayofdomainresponse-soap.md) <br/> |<span data-ttu-id="7c8e2-128">Contiene una matriz de elementos de **DomainResponse** .</span><span class="sxs-lookup"><span data-stu-id="7c8e2-128">Contains an array of **DomainResponse** elements.</span></span> <span data-ttu-id="7c8e2-129">Cada elemento **DomainResponse** contiene la configuración solicitada para el usuario especificado.</span><span class="sxs-lookup"><span data-stu-id="7c8e2-129">Each **DomainResponse** element contains the requested settings for the specified user.</span></span>  <br/> |
|[<span data-ttu-id="7c8e2-130">DomainResponses (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7c8e2-130">DomainResponses (SOAP)</span></span>](domainresponses-soap.md) <br/> |<span data-ttu-id="7c8e2-131">Contiene las respuestas para cada dominio.</span><span class="sxs-lookup"><span data-stu-id="7c8e2-131">Contains the responses for each domain.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7c8e2-132">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="7c8e2-132">Text value</span></span>

<span data-ttu-id="7c8e2-133">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7c8e2-133">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7c8e2-134">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7c8e2-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7c8e2-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7c8e2-135">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="7c8e2-136">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="7c8e2-136">Schema Name</span></span>  <br/> |<span data-ttu-id="7c8e2-137">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="7c8e2-137">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="7c8e2-138">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="7c8e2-138">Validation File</span></span>  <br/> |<span data-ttu-id="7c8e2-139">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="7c8e2-139">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7c8e2-140">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="7c8e2-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="7c8e2-141">Verdadero</span><span class="sxs-lookup"><span data-stu-id="7c8e2-141">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7c8e2-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="7c8e2-142">See also</span></span>

- [<span data-ttu-id="7c8e2-143">Operación GetDomainSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7c8e2-143">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

