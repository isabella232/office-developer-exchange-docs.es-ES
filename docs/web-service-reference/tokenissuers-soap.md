---
title: TokenIssuers (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 26c55228-184e-4340-bd80-f86be56f3e7a
description: Los elementos de TokenIssuers representa la colección de TokenIssuer (SOAP).
ms.openlocfilehash: b070d85b32d5bce8461ac4e930329f237885bad7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840696"
---
# <a name="tokenissuers-soap"></a><span data-ttu-id="0e71b-103">TokenIssuers (SOAP)</span><span class="sxs-lookup"><span data-stu-id="0e71b-103">TokenIssuers (SOAP)</span></span>

<span data-ttu-id="0e71b-104">Los elementos de **TokenIssuers** representa la colección de [TokenIssuer (SOAP)](tokenissuer-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="0e71b-104">The **TokenIssuers** elements represents the [TokenIssuer (SOAP)](tokenissuer-soap.md) collection.</span></span> 
  
```XML
<TokenIssuers>
    <TokenIssuer/>
</TokenIssuers>
```

 <span data-ttu-id="0e71b-105">**TokenIssuers**</span><span class="sxs-lookup"><span data-stu-id="0e71b-105">**TokenIssuers**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0e71b-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="0e71b-106">Attributes and elements</span></span>

<span data-ttu-id="0e71b-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="0e71b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0e71b-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="0e71b-108">Attributes</span></span>

<span data-ttu-id="0e71b-109">Ninguno</span><span class="sxs-lookup"><span data-stu-id="0e71b-109">None</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0e71b-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0e71b-110">Child elements</span></span>

|<span data-ttu-id="0e71b-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="0e71b-111">**Element**</span></span>|<span data-ttu-id="0e71b-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0e71b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0e71b-113">TokenIssuer (SOAP)</span><span class="sxs-lookup"><span data-stu-id="0e71b-113">TokenIssuer (SOAP)</span></span>](tokenissuer-soap.md) <br/> |<span data-ttu-id="0e71b-114">Especifica el [Uri (SOAP)](uri-soap.md) y el [Extremo (SOAP)](endpoint-soap.md) para el servicio de token de seguridad.</span><span class="sxs-lookup"><span data-stu-id="0e71b-114">Specifies the [Uri (SOAP)](uri-soap.md) and [Endpoint (SOAP)](endpoint-soap.md) for the security token service.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0e71b-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0e71b-115">Parent elements</span></span>

|<span data-ttu-id="0e71b-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="0e71b-116">**Element**</span></span>|<span data-ttu-id="0e71b-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0e71b-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0e71b-118">GetFederationInformationResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="0e71b-118">GetFederationInformationResponse (SOAP)</span></span>](getfederationinformationresponse-soap.md) <br/> |<span data-ttu-id="0e71b-119">Contiene la respuesta de la [operación de GetFederationInformation (SOAP)](getfederationinformation-operation-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="0e71b-119">Contains the [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md) response.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0e71b-120">Notas</span><span class="sxs-lookup"><span data-stu-id="0e71b-120">Remarks</span></span>

<span data-ttu-id="0e71b-121">El **TokenIssuers** representa una colección de elementos de [TokenIssuer (SOAP)](tokenissuer-soap.md) que se usará en la detección automática.</span><span class="sxs-lookup"><span data-stu-id="0e71b-121">The **TokenIssuers** represents a collection of [TokenIssuer (SOAP)](tokenissuer-soap.md) elements to be used in the Autodiscovery.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="0e71b-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0e71b-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0e71b-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0e71b-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="0e71b-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="0e71b-124">Schema Name</span></span>  <br/> |<span data-ttu-id="0e71b-125">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="0e71b-125">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="0e71b-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="0e71b-126">Validation File</span></span>  <br/> |<span data-ttu-id="0e71b-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="0e71b-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0e71b-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="0e71b-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="0e71b-129">Verdadero</span><span class="sxs-lookup"><span data-stu-id="0e71b-129">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0e71b-130">Ver también</span><span class="sxs-lookup"><span data-stu-id="0e71b-130">See also</span></span>



[<span data-ttu-id="0e71b-131">Referencia de servicio web de detección automática para Exchange</span><span class="sxs-lookup"><span data-stu-id="0e71b-131">Autodiscover web service reference for Exchange</span></span>](autodiscover-web-service-reference-for-exchange.md)
  
[<span data-ttu-id="0e71b-132">Elementos de Autodiscover XML SOAP para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="0e71b-132">SOAP Autodiscover XML elements for Exchange 2013</span></span>](soap-autodiscover-xml-elements-for-exchange-2013.md)
