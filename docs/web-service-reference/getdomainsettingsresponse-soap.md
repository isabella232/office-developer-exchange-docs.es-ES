---
title: GetDomainSettingsResponse (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 43ebd17b-3a70-4878-9254-97a4c2c87b77
description: El elemento GetDomainSettingsResponse representa la respuesta a una operación de GetDomainSettings (SOAP), que devuelve la configuración de dominio.
ms.openlocfilehash: c4984c2c6c532fcbd45c1a75733e578f6d9491fa
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764816"
---
# <a name="getdomainsettingsresponse-soap"></a><span data-ttu-id="05caa-103">GetDomainSettingsResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="05caa-103">GetDomainSettingsResponse (SOAP)</span></span>

<span data-ttu-id="05caa-104">El elemento **GetDomainSettingsResponse** representa la respuesta a una [operación de GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md), que devuelve la configuración de dominio.</span><span class="sxs-lookup"><span data-stu-id="05caa-104">The **GetDomainSettingsResponse** element represents the response to a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md), which returns the domain settings.</span></span>
  
```XML
<GetDomainSettingsResponse>
   <DomainResponses/>
   <ErrorCode/>
   <ErrorMessage/>
</GetDomainSettingsResponse>
```

 <span data-ttu-id="05caa-105">**GetDomainSettingsResponse**</span><span class="sxs-lookup"><span data-stu-id="05caa-105">**GetDomainSettingsResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="05caa-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="05caa-106">Attributes and elements</span></span>

<span data-ttu-id="05caa-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="05caa-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="05caa-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="05caa-108">Attributes</span></span>

<span data-ttu-id="05caa-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="05caa-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="05caa-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="05caa-110">Child elements</span></span>

|<span data-ttu-id="05caa-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="05caa-111">**Element**</span></span>|<span data-ttu-id="05caa-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="05caa-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="05caa-113">DomainResponses (SOAP)</span><span class="sxs-lookup"><span data-stu-id="05caa-113">DomainResponses (SOAP)</span></span>](domainresponses-soap.md) <br/> |<span data-ttu-id="05caa-114">Contiene una matriz de respuestas para la configuración de cada dominio solicitado.</span><span class="sxs-lookup"><span data-stu-id="05caa-114">Contains an array of responses for each requested domain's settings.</span></span>  <br/> |
|[<span data-ttu-id="05caa-115">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="05caa-115">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="05caa-116">Representa un código de error devuelto por el servicio Detección automática.</span><span class="sxs-lookup"><span data-stu-id="05caa-116">Represents an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="05caa-117">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="05caa-117">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="05caa-118">Representa un mensaje en el que está asociado con un código de error devuelto por el servicio Detección automática.</span><span class="sxs-lookup"><span data-stu-id="05caa-118">Represents a message that is associated with an error code that is returned by the Autodiscover service.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="05caa-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="05caa-119">Parent elements</span></span>

<span data-ttu-id="05caa-120">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="05caa-120">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="05caa-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="05caa-121">Text value</span></span>

<span data-ttu-id="05caa-122">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="05caa-122">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="05caa-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="05caa-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="05caa-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="05caa-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="05caa-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="05caa-125">Schema Name</span></span>  <br/> |<span data-ttu-id="05caa-126">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="05caa-126">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="05caa-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="05caa-127">Validation File</span></span>  <br/> |<span data-ttu-id="05caa-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="05caa-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="05caa-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="05caa-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="05caa-130">Verdadero</span><span class="sxs-lookup"><span data-stu-id="05caa-130">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="05caa-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="05caa-131">See also</span></span>



[<span data-ttu-id="05caa-132">Operación GetDomainSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="05caa-132">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

