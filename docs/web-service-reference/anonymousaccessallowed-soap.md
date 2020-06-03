---
title: AnonymousAccessAllowed (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bf819a65-30f2-4881-a34f-cb30a9c2b6a7
description: El elemento AnonymousAccessAllowed indica si una ubicación de uso compartido de documentos requiere un usuario autenticado.
ms.openlocfilehash: b3ff22fbba603bbd74dc08a0dbb1d8687714fe7d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466083"
---
# <a name="anonymousaccessallowed-soap"></a><span data-ttu-id="97046-103">AnonymousAccessAllowed (SOAP)</span><span class="sxs-lookup"><span data-stu-id="97046-103">AnonymousAccessAllowed (SOAP)</span></span>

<span data-ttu-id="97046-104">El elemento **AnonymousAccessAllowed** indica si una ubicación de uso compartido de documentos requiere un usuario autenticado.</span><span class="sxs-lookup"><span data-stu-id="97046-104">The **AnonymousAccessAllowed** element indicates whether a document sharing location requires an authenticated user.</span></span> 
  
```XML
<AnonymousAccessAllowed /> 
```

 <span data-ttu-id="97046-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="97046-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="97046-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="97046-106">Attributes and elements</span></span>

<span data-ttu-id="97046-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="97046-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="97046-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="97046-108">Attributes</span></span>

<span data-ttu-id="97046-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="97046-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="97046-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="97046-110">Child elements</span></span>

<span data-ttu-id="97046-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="97046-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="97046-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="97046-112">Parent elements</span></span>

|<span data-ttu-id="97046-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="97046-113">**Element**</span></span>|<span data-ttu-id="97046-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="97046-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="97046-115">DocumentSharingLocation (SOAP)</span><span class="sxs-lookup"><span data-stu-id="97046-115">DocumentSharingLocation (SOAP)</span></span>](documentsharinglocation-soap.md) <br/> |<span data-ttu-id="97046-116">Representa la información de ubicación y metadatos de una ubicación de uso compartido de documentos.</span><span class="sxs-lookup"><span data-stu-id="97046-116">Represents location and metadata information for a document sharing location.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="97046-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="97046-117">Text value</span></span>

<span data-ttu-id="97046-118">El valor booleano del elemento **AnonymousAccessAllowed** indica si la ubicación de uso compartido requiere un usuario autenticado.</span><span class="sxs-lookup"><span data-stu-id="97046-118">The Boolean value of the **AnonymousAccessAllowed** element indicates whether the sharing location requires an authenticated user.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="97046-119">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="97046-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="97046-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="97046-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="97046-121">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="97046-121">Schema Name</span></span>  <br/> |<span data-ttu-id="97046-122">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="97046-122">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="97046-123">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="97046-123">Validation File</span></span>  <br/> |<span data-ttu-id="97046-124">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="97046-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="97046-125">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="97046-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="97046-126">Verdadero</span><span class="sxs-lookup"><span data-stu-id="97046-126">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="97046-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="97046-127">See also</span></span>

- [<span data-ttu-id="97046-128">Operación GetUserSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="97046-128">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
- [<span data-ttu-id="97046-129">Referencia del servicio web de Detección automática para Exchange</span><span class="sxs-lookup"><span data-stu-id="97046-129">Autodiscover web service reference for Exchange</span></span>](autodiscover-web-service-reference-for-exchange.md)
- [<span data-ttu-id="97046-130">Elementos XML de detección automática de SOAP para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="97046-130">SOAP Autodiscover XML elements for Exchange 2013</span></span>](soap-autodiscover-xml-elements-for-exchange-2013.md)

