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
description: El elemento GetDomainSettingsResponse representa la respuesta a una operación GetDomainSettings (SOAP), que devuelve la configuración del dominio.
ms.openlocfilehash: 94cb202948e6a0d5a34f5547132c052d1d1b6a40
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461880"
---
# <a name="getdomainsettingsresponse-soap"></a><span data-ttu-id="b9eac-103">GetDomainSettingsResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b9eac-103">GetDomainSettingsResponse (SOAP)</span></span>

<span data-ttu-id="b9eac-104">El elemento **GetDomainSettingsResponse** representa la respuesta a una [operación GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md), que devuelve la configuración del dominio.</span><span class="sxs-lookup"><span data-stu-id="b9eac-104">The **GetDomainSettingsResponse** element represents the response to a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md), which returns the domain settings.</span></span>
  
```XML
<GetDomainSettingsResponse>
   <DomainResponses/>
   <ErrorCode/>
   <ErrorMessage/>
</GetDomainSettingsResponse>
```

 <span data-ttu-id="b9eac-105">**GetDomainSettingsResponse**</span><span class="sxs-lookup"><span data-stu-id="b9eac-105">**GetDomainSettingsResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b9eac-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b9eac-106">Attributes and elements</span></span>

<span data-ttu-id="b9eac-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b9eac-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b9eac-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="b9eac-108">Attributes</span></span>

<span data-ttu-id="b9eac-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="b9eac-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b9eac-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b9eac-110">Child elements</span></span>

|<span data-ttu-id="b9eac-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b9eac-111">**Element**</span></span>|<span data-ttu-id="b9eac-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b9eac-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b9eac-113">DomainResponses (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b9eac-113">DomainResponses (SOAP)</span></span>](domainresponses-soap.md) <br/> |<span data-ttu-id="b9eac-114">Contiene una matriz de respuestas para la configuración de cada dominio solicitado.</span><span class="sxs-lookup"><span data-stu-id="b9eac-114">Contains an array of responses for each requested domain's settings.</span></span>  <br/> |
|[<span data-ttu-id="b9eac-115">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b9eac-115">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="b9eac-116">Representa un código de error devuelto por el servicio de detección automática.</span><span class="sxs-lookup"><span data-stu-id="b9eac-116">Represents an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="b9eac-117">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b9eac-117">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="b9eac-118">Representa un mensaje que está asociado con un código de error devuelto por el servicio de detección automática.</span><span class="sxs-lookup"><span data-stu-id="b9eac-118">Represents a message that is associated with an error code that is returned by the Autodiscover service.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b9eac-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b9eac-119">Parent elements</span></span>

<span data-ttu-id="b9eac-120">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="b9eac-120">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="b9eac-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="b9eac-121">Text value</span></span>

<span data-ttu-id="b9eac-122">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="b9eac-122">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b9eac-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b9eac-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b9eac-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="b9eac-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="b9eac-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b9eac-125">Schema Name</span></span>  <br/> |<span data-ttu-id="b9eac-126">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="b9eac-126">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="b9eac-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b9eac-127">Validation File</span></span>  <br/> |<span data-ttu-id="b9eac-128">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="b9eac-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b9eac-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b9eac-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="b9eac-130">Verdadero</span><span class="sxs-lookup"><span data-stu-id="b9eac-130">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b9eac-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="b9eac-131">See also</span></span>



[<span data-ttu-id="b9eac-132">Operación GetDomainSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b9eac-132">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

