---
title: TokenIssuer (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2d7be675-626c-4173-89e9-e32beef81ad5
description: El elemento TokenIssuer especifica el URI (SOAP) y el extremo (SOAP) para el servicio de token de seguridad.
ms.openlocfilehash: e9c0b4140de26c7ff05daf4e863b3e8a17fedc62
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526329"
---
# <a name="tokenissuer-soap"></a><span data-ttu-id="bf8eb-103">TokenIssuer (SOAP)</span><span class="sxs-lookup"><span data-stu-id="bf8eb-103">TokenIssuer (SOAP)</span></span>

<span data-ttu-id="bf8eb-104">El elemento **TokenIssuer** especifica el [URI (SOAP)](uri-soap.md) y el [extremo (SOAP)](endpoint-soap.md) para el servicio de token de seguridad.</span><span class="sxs-lookup"><span data-stu-id="bf8eb-104">The **TokenIssuer** element specifies the [Uri (SOAP)](uri-soap.md) and [Endpoint (SOAP)](endpoint-soap.md) for the security token service.</span></span> 
  
```XML
<TokenIssuer>
   <Uri/>
   <Endpoint/>
</TokenIssuer>
```

 <span data-ttu-id="bf8eb-105">**TokenIssuer**</span><span class="sxs-lookup"><span data-stu-id="bf8eb-105">**TokenIssuer**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bf8eb-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="bf8eb-106">Attributes and elements</span></span>

<span data-ttu-id="bf8eb-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="bf8eb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bf8eb-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="bf8eb-108">Attributes</span></span>

<span data-ttu-id="bf8eb-109">Ninguno</span><span class="sxs-lookup"><span data-stu-id="bf8eb-109">None</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bf8eb-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="bf8eb-110">Child elements</span></span>

|<span data-ttu-id="bf8eb-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="bf8eb-111">**Element**</span></span>|<span data-ttu-id="bf8eb-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bf8eb-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bf8eb-113">URI (SOAP)</span><span class="sxs-lookup"><span data-stu-id="bf8eb-113">Uri (SOAP)</span></span>](uri-soap.md) <br/> |<span data-ttu-id="bf8eb-114">URI del servicio de token de seguridad que emitió el token de seguridad.</span><span class="sxs-lookup"><span data-stu-id="bf8eb-114">The URI of the security token service that issued the security token.</span></span>  <br/> |
|[<span data-ttu-id="bf8eb-115">Extremo (SOAP)</span><span class="sxs-lookup"><span data-stu-id="bf8eb-115">Endpoint (SOAP)</span></span>](endpoint-soap.md) <br/> |<span data-ttu-id="bf8eb-116">URI del extremo del servicio Web.</span><span class="sxs-lookup"><span data-stu-id="bf8eb-116">The web service Endpoint URI.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="bf8eb-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="bf8eb-117">Parent elements</span></span>

|<span data-ttu-id="bf8eb-118">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="bf8eb-118">**Element**</span></span>|<span data-ttu-id="bf8eb-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bf8eb-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bf8eb-120">TokenIssuers (SOAP)</span><span class="sxs-lookup"><span data-stu-id="bf8eb-120">TokenIssuers (SOAP)</span></span>](tokenissuers-soap.md) <br/> |<span data-ttu-id="bf8eb-121">Representa una colección de URI de servicio de token de seguridad [(SOAP)](uri-soap.md) y de [extremo (SOAP)](endpoint-soap.md).</span><span class="sxs-lookup"><span data-stu-id="bf8eb-121">Represents a collection of security token service [Uri (SOAP)](uri-soap.md) and [Endpoint (SOAP)](endpoint-soap.md).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bf8eb-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bf8eb-122">Remarks</span></span>

<span data-ttu-id="bf8eb-123">Use el elemento **TokenIssuer** para especificar el servicio de token de seguridad al usar tokens de seguridad.</span><span class="sxs-lookup"><span data-stu-id="bf8eb-123">Use the **TokenIssuer** element to specify the security token service when using security tokens.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="bf8eb-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="bf8eb-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bf8eb-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="bf8eb-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="bf8eb-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="bf8eb-126">Schema Name</span></span>  <br/> |<span data-ttu-id="bf8eb-127">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="bf8eb-127">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="bf8eb-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="bf8eb-128">Validation File</span></span>  <br/> |<span data-ttu-id="bf8eb-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="bf8eb-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="bf8eb-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="bf8eb-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="bf8eb-131">Verdadero</span><span class="sxs-lookup"><span data-stu-id="bf8eb-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bf8eb-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="bf8eb-132">See also</span></span>



[<span data-ttu-id="bf8eb-133">Referencia del servicio web de Detección automática para Exchange</span><span class="sxs-lookup"><span data-stu-id="bf8eb-133">Autodiscover web service reference for Exchange</span></span>](autodiscover-web-service-reference-for-exchange.md)
  
[<span data-ttu-id="bf8eb-134">Elementos XML de detección automática de SOAP para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="bf8eb-134">SOAP Autodiscover XML elements for Exchange 2013</span></span>](soap-autodiscover-xml-elements-for-exchange-2013.md)

