---
title: TokenIssuers (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 26c55228-184e-4340-bd80-f86be56f3e7a
description: Los elementos TokenIssuers representan la colección TokenIssuer (SOAP).
ms.openlocfilehash: 352487ad3fd9c1ee7de756a109fb98a49d0cdcd7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457077"
---
# <a name="tokenissuers-soap"></a><span data-ttu-id="ea207-103">TokenIssuers (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ea207-103">TokenIssuers (SOAP)</span></span>

<span data-ttu-id="ea207-104">Los elementos **TokenIssuers** representan la colección [TokenIssuer (SOAP)](tokenissuer-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="ea207-104">The **TokenIssuers** elements represents the [TokenIssuer (SOAP)](tokenissuer-soap.md) collection.</span></span> 
  
```XML
<TokenIssuers>
    <TokenIssuer/>
</TokenIssuers>
```

 <span data-ttu-id="ea207-105">**TokenIssuers**</span><span class="sxs-lookup"><span data-stu-id="ea207-105">**TokenIssuers**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ea207-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ea207-106">Attributes and elements</span></span>

<span data-ttu-id="ea207-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ea207-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ea207-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="ea207-108">Attributes</span></span>

<span data-ttu-id="ea207-109">Ninguno</span><span class="sxs-lookup"><span data-stu-id="ea207-109">None</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ea207-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ea207-110">Child elements</span></span>

|<span data-ttu-id="ea207-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ea207-111">**Element**</span></span>|<span data-ttu-id="ea207-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ea207-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ea207-113">TokenIssuer (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ea207-113">TokenIssuer (SOAP)</span></span>](tokenissuer-soap.md) <br/> |<span data-ttu-id="ea207-114">Especifica el [URI (SOAP)](uri-soap.md) y el [extremo (SOAP)](endpoint-soap.md) para el servicio de token de seguridad.</span><span class="sxs-lookup"><span data-stu-id="ea207-114">Specifies the [Uri (SOAP)](uri-soap.md) and [Endpoint (SOAP)](endpoint-soap.md) for the security token service.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ea207-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ea207-115">Parent elements</span></span>

|<span data-ttu-id="ea207-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ea207-116">**Element**</span></span>|<span data-ttu-id="ea207-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ea207-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ea207-118">GetFederationInformationResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ea207-118">GetFederationInformationResponse (SOAP)</span></span>](getfederationinformationresponse-soap.md) <br/> |<span data-ttu-id="ea207-119">Contiene la respuesta de [operación GetFederationInformation (SOAP)](getfederationinformation-operation-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="ea207-119">Contains the [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md) response.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ea207-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ea207-120">Remarks</span></span>

<span data-ttu-id="ea207-121">**TokenIssuers** representa una colección de elementos [TokenIssuer (SOAP)](tokenissuer-soap.md) que se usarán en la detección automática.</span><span class="sxs-lookup"><span data-stu-id="ea207-121">The **TokenIssuers** represents a collection of [TokenIssuer (SOAP)](tokenissuer-soap.md) elements to be used in the Autodiscovery.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="ea207-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ea207-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ea207-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="ea207-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="ea207-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ea207-124">Schema Name</span></span>  <br/> |<span data-ttu-id="ea207-125">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="ea207-125">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="ea207-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ea207-126">Validation File</span></span>  <br/> |<span data-ttu-id="ea207-127">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="ea207-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ea207-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ea207-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="ea207-129">Verdadero</span><span class="sxs-lookup"><span data-stu-id="ea207-129">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ea207-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="ea207-130">See also</span></span>



[<span data-ttu-id="ea207-131">Referencia del servicio web de Detección automática para Exchange</span><span class="sxs-lookup"><span data-stu-id="ea207-131">Autodiscover web service reference for Exchange</span></span>](autodiscover-web-service-reference-for-exchange.md)
  
[<span data-ttu-id="ea207-132">Elementos XML de detección automática de SOAP para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="ea207-132">SOAP Autodiscover XML elements for Exchange 2013</span></span>](soap-autodiscover-xml-elements-for-exchange-2013.md)

