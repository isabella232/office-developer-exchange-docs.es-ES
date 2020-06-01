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
ms.openlocfilehash: dea6e36c51ceea53201b668cfba616c03a44df86
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456965"
---
# <a name="domainresponse-soap"></a><span data-ttu-id="f88f9-103">DomainResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="f88f9-103">DomainResponse (SOAP)</span></span>

<span data-ttu-id="f88f9-104">El elemento **DomainResponse** contiene la configuración solicitada para el dominio especificado.</span><span class="sxs-lookup"><span data-stu-id="f88f9-104">The **DomainResponse** element contains the requested settings for the specified domain.</span></span> 
  
```XML
<DomainResponse>
   <DomainSettingErrors/>
   <DomainSettings/>
   <RedirectTarget/>
   <ErrorCode/>
   <ErrorMessage/>
</DomainResponse>
```

 <span data-ttu-id="f88f9-105">**DomainResponse**</span><span class="sxs-lookup"><span data-stu-id="f88f9-105">**DomainResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f88f9-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f88f9-106">Attributes and elements</span></span>

<span data-ttu-id="f88f9-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f88f9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f88f9-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="f88f9-108">Attributes</span></span>

<span data-ttu-id="f88f9-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="f88f9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f88f9-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f88f9-110">Child elements</span></span>

|<span data-ttu-id="f88f9-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f88f9-111">**Element**</span></span>|<span data-ttu-id="f88f9-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f88f9-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f88f9-113">DomainSettingErrors (SOAP)</span><span class="sxs-lookup"><span data-stu-id="f88f9-113">DomainSettingErrors (SOAP)</span></span>](domainsettingerrors-soap.md) <br/> |<span data-ttu-id="f88f9-114">Contiene información de error de la configuración que no se pudo devolver.</span><span class="sxs-lookup"><span data-stu-id="f88f9-114">Contains error information for settings that could not be returned.</span></span>  <br/> |
|[<span data-ttu-id="f88f9-115">DomainSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="f88f9-115">DomainSettings (SOAP)</span></span>](domainsettings-soap.md) <br/> |<span data-ttu-id="f88f9-116">Representa la configuración de dominio que se ha enviado en una solicitud de detección automática o devuelta por una respuesta de detección automática.</span><span class="sxs-lookup"><span data-stu-id="f88f9-116">Represents the domain settings that were submitted in an Autodiscover request or returned by an Autodiscover response.</span></span>  <br/> |
|[<span data-ttu-id="f88f9-117">RedirectTarget (SOAP)</span><span class="sxs-lookup"><span data-stu-id="f88f9-117">RedirectTarget (SOAP)</span></span>](redirecttarget-soap.md) <br/> |<span data-ttu-id="f88f9-118">Identifica el destino del redireccionamiento.</span><span class="sxs-lookup"><span data-stu-id="f88f9-118">Identifies the target of the redirection.</span></span> <span data-ttu-id="f88f9-119">El destino puede ser una dirección URL o una dirección de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="f88f9-119">The target can be either a URL or an e-mail address.</span></span>  <br/> |
|[<span data-ttu-id="f88f9-120">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="f88f9-120">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="f88f9-121">Especifica el código de error que está asociado con la solicitud específica.</span><span class="sxs-lookup"><span data-stu-id="f88f9-121">Specifies the error code that is associated with the specific request.</span></span>  <br/> |
|[<span data-ttu-id="f88f9-122">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="f88f9-122">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="f88f9-123">Especifica el mensaje de error que está asociado con la solicitud específica.</span><span class="sxs-lookup"><span data-stu-id="f88f9-123">Specifies the error message that is associated with the specific request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f88f9-124">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f88f9-124">Parent elements</span></span>

|<span data-ttu-id="f88f9-125">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f88f9-125">**Element**</span></span>|<span data-ttu-id="f88f9-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f88f9-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f88f9-127">ArrayOfDomainResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="f88f9-127">ArrayOfDomainResponse (SOAP)</span></span>](arrayofdomainresponse-soap.md) <br/> |<span data-ttu-id="f88f9-128">Contiene una matriz de elementos **DomainResponse** .</span><span class="sxs-lookup"><span data-stu-id="f88f9-128">Contains an array of **DomainResponse** elements.</span></span> <span data-ttu-id="f88f9-129">Cada elemento **DomainResponse** contiene la configuración solicitada para el usuario especificado.</span><span class="sxs-lookup"><span data-stu-id="f88f9-129">Each **DomainResponse** element contains the requested settings for the specified user.</span></span>  <br/> |
|[<span data-ttu-id="f88f9-130">DomainResponses (SOAP)</span><span class="sxs-lookup"><span data-stu-id="f88f9-130">DomainResponses (SOAP)</span></span>](domainresponses-soap.md) <br/> |<span data-ttu-id="f88f9-131">Contiene las respuestas para cada dominio.</span><span class="sxs-lookup"><span data-stu-id="f88f9-131">Contains the responses for each domain.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f88f9-132">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="f88f9-132">Text value</span></span>

<span data-ttu-id="f88f9-133">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="f88f9-133">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f88f9-134">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f88f9-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f88f9-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="f88f9-135">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="f88f9-136">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f88f9-136">Schema Name</span></span>  <br/> |<span data-ttu-id="f88f9-137">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="f88f9-137">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="f88f9-138">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f88f9-138">Validation File</span></span>  <br/> |<span data-ttu-id="f88f9-139">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="f88f9-139">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f88f9-140">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f88f9-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="f88f9-141">Verdadero</span><span class="sxs-lookup"><span data-stu-id="f88f9-141">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f88f9-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="f88f9-142">See also</span></span>

- [<span data-ttu-id="f88f9-143">Operación GetDomainSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="f88f9-143">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

