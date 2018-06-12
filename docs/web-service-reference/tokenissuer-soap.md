---
title: TokenIssuer (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2d7be675-626c-4173-89e9-e32beef81ad5
description: El elemento TokenIssuer especifica el Uri (SOAP) y el extremo (SOAP) para el servicio de token de seguridad.
ms.openlocfilehash: 1c267fc6cbfdadd471c568473cc9aeeafb43ae2d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840684"
---
# <a name="tokenissuer-soap"></a><span data-ttu-id="efc3c-103">TokenIssuer (SOAP)</span><span class="sxs-lookup"><span data-stu-id="efc3c-103">TokenIssuer (SOAP)</span></span>

<span data-ttu-id="efc3c-104">El elemento **TokenIssuer** especifica el [Uri (SOAP)](uri-soap.md) y el [Extremo (SOAP)](endpoint-soap.md) para el servicio de token de seguridad.</span><span class="sxs-lookup"><span data-stu-id="efc3c-104">The **TokenIssuer** element specifies the [Uri (SOAP)](uri-soap.md) and [Endpoint (SOAP)](endpoint-soap.md) for the security token service.</span></span> 
  
```XML
<TokenIssuer>
   <Uri/>
   <Endpoint/>
</TokenIssuer>
```

 <span data-ttu-id="efc3c-105">**TokenIssuer**</span><span class="sxs-lookup"><span data-stu-id="efc3c-105">**TokenIssuer**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="efc3c-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="efc3c-106">Attributes and elements</span></span>

<span data-ttu-id="efc3c-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="efc3c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="efc3c-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="efc3c-108">Attributes</span></span>

<span data-ttu-id="efc3c-109">Ninguno</span><span class="sxs-lookup"><span data-stu-id="efc3c-109">None</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="efc3c-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="efc3c-110">Child elements</span></span>

|<span data-ttu-id="efc3c-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="efc3c-111">**Element**</span></span>|<span data-ttu-id="efc3c-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="efc3c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="efc3c-113">URI (SOAP)</span><span class="sxs-lookup"><span data-stu-id="efc3c-113">Uri (SOAP)</span></span>](uri-soap.md) <br/> |<span data-ttu-id="efc3c-114">El URI del servicio de token de seguridad que ha emitido el token de seguridad.</span><span class="sxs-lookup"><span data-stu-id="efc3c-114">The URI of the security token service that issued the security token.</span></span>  <br/> |
|[<span data-ttu-id="efc3c-115">Extremo (SOAP)</span><span class="sxs-lookup"><span data-stu-id="efc3c-115">Endpoint (SOAP)</span></span>](endpoint-soap.md) <br/> |<span data-ttu-id="efc3c-116">El URI del extremo de servicio de web.</span><span class="sxs-lookup"><span data-stu-id="efc3c-116">The web service Endpoint URI.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="efc3c-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="efc3c-117">Parent elements</span></span>

|<span data-ttu-id="efc3c-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="efc3c-118">**Element**</span></span>|<span data-ttu-id="efc3c-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="efc3c-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="efc3c-120">TokenIssuers (SOAP)</span><span class="sxs-lookup"><span data-stu-id="efc3c-120">TokenIssuers (SOAP)</span></span>](tokenissuers-soap.md) <br/> |<span data-ttu-id="efc3c-121">Representa una colección de servicio de token de seguridad [Uri (SOAP)](uri-soap.md) y el [Extremo (SOAP)](endpoint-soap.md).</span><span class="sxs-lookup"><span data-stu-id="efc3c-121">Represents a collection of security token service [Uri (SOAP)](uri-soap.md) and [Endpoint (SOAP)](endpoint-soap.md).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="efc3c-122">Notas</span><span class="sxs-lookup"><span data-stu-id="efc3c-122">Remarks</span></span>

<span data-ttu-id="efc3c-123">Use el elemento **TokenIssuer** para especificar el servicio de token de seguridad cuando se usa los tokens de seguridad.</span><span class="sxs-lookup"><span data-stu-id="efc3c-123">Use the **TokenIssuer** element to specify the security token service when using security tokens.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="efc3c-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="efc3c-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="efc3c-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="efc3c-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="efc3c-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="efc3c-126">Schema Name</span></span>  <br/> |<span data-ttu-id="efc3c-127">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="efc3c-127">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="efc3c-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="efc3c-128">Validation File</span></span>  <br/> |<span data-ttu-id="efc3c-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="efc3c-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="efc3c-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="efc3c-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="efc3c-131">Verdadero</span><span class="sxs-lookup"><span data-stu-id="efc3c-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="efc3c-132">Ver también</span><span class="sxs-lookup"><span data-stu-id="efc3c-132">See also</span></span>



[<span data-ttu-id="efc3c-133">Referencia de servicio web de detección automática para Exchange</span><span class="sxs-lookup"><span data-stu-id="efc3c-133">Autodiscover web service reference for Exchange</span></span>](autodiscover-web-service-reference-for-exchange.md)
  
[<span data-ttu-id="efc3c-134">Elementos de Autodiscover XML SOAP para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="efc3c-134">SOAP Autodiscover XML elements for Exchange 2013</span></span>](soap-autodiscover-xml-elements-for-exchange-2013.md)

