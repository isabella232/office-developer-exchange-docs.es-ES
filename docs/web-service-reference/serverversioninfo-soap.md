---
title: ServerVersionInfo (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 8662647b-e50a-4774-9ba3-a951ae6df781
description: El elemento ServerVersionInfo contiene la versión del servidor que procesa la solicitud.
ms.openlocfilehash: b02071e4997aba91fb538d52df2612fe6fd32800
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837385"
---
# <a name="serverversioninfo-soap"></a><span data-ttu-id="53fb6-103">ServerVersionInfo (SOAP)</span><span class="sxs-lookup"><span data-stu-id="53fb6-103">ServerVersionInfo (SOAP)</span></span>

<span data-ttu-id="53fb6-104">El elemento **ServerVersionInfo** contiene la versión del servidor que procesa la solicitud.</span><span class="sxs-lookup"><span data-stu-id="53fb6-104">The **ServerVersionInfo** element contains the version of the server that processed the request.</span></span> 
  
```XML
<ServerVersionInfo>
   <MajorVersion/>
   <MinorVersion/>
   <MajorBuildNumber/>
   <MinorBuildNumber/>
   <Version/>
</ServerVersionInfo>
```

 <span data-ttu-id="53fb6-105">**ServerVersionInfo**</span><span class="sxs-lookup"><span data-stu-id="53fb6-105">**ServerVersionInfo**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="53fb6-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="53fb6-106">Attributes and elements</span></span>

<span data-ttu-id="53fb6-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="53fb6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="53fb6-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="53fb6-108">Attributes</span></span>

<span data-ttu-id="53fb6-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="53fb6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="53fb6-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="53fb6-110">Child elements</span></span>

|<span data-ttu-id="53fb6-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="53fb6-111">**Element**</span></span>|<span data-ttu-id="53fb6-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="53fb6-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="53fb6-113">MajorVersion (SOAP)</span><span class="sxs-lookup"><span data-stu-id="53fb6-113">MajorVersion (SOAP)</span></span>](majorversion-soap.md) <br/> |<span data-ttu-id="53fb6-114">El número de versión principal para el servidor.</span><span class="sxs-lookup"><span data-stu-id="53fb6-114">The major version number for the server.</span></span>  <br/> |
|[<span data-ttu-id="53fb6-115">MinorVersion (SOAP)</span><span class="sxs-lookup"><span data-stu-id="53fb6-115">MinorVersion (SOAP)</span></span>](minorversion-soap.md) <br/> |<span data-ttu-id="53fb6-116">El número de versión secundaria para el servidor.</span><span class="sxs-lookup"><span data-stu-id="53fb6-116">The minor version number for the server.</span></span>  <br/> |
|[<span data-ttu-id="53fb6-117">MajorBuildNumber (SOAP)</span><span class="sxs-lookup"><span data-stu-id="53fb6-117">MajorBuildNumber (SOAP)</span></span>](majorbuildnumber-soap.md) <br/> |<span data-ttu-id="53fb6-118">El número de versión de compilación principal para el servidor.</span><span class="sxs-lookup"><span data-stu-id="53fb6-118">The major build number for the server.</span></span>  <br/> |
|[<span data-ttu-id="53fb6-119">MinorBuildNumber (SOAP)</span><span class="sxs-lookup"><span data-stu-id="53fb6-119">MinorBuildNumber (SOAP)</span></span>](minorbuildnumber-soap.md) <br/> |<span data-ttu-id="53fb6-120">El número de compilación secundaria para el servidor.</span><span class="sxs-lookup"><span data-stu-id="53fb6-120">The minor build number for the server.</span></span>  <br/> |
|[<span data-ttu-id="53fb6-121">Versión (SOAP)</span><span class="sxs-lookup"><span data-stu-id="53fb6-121">Version (SOAP)</span></span>](version-soap.md) <br/> |<span data-ttu-id="53fb6-122">Una descripción de la versión del producto de servidor.</span><span class="sxs-lookup"><span data-stu-id="53fb6-122">A description of the server product version.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="53fb6-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="53fb6-123">Parent elements</span></span>

<span data-ttu-id="53fb6-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="53fb6-124">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="53fb6-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="53fb6-125">Remarks</span></span>

<span data-ttu-id="53fb6-126">Este elemento se devuelve en el encabezado SOAP.</span><span class="sxs-lookup"><span data-stu-id="53fb6-126">This element is returned in the SOAP header.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="53fb6-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="53fb6-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="53fb6-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="53fb6-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="53fb6-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="53fb6-129">Schema Name</span></span>  <br/> |<span data-ttu-id="53fb6-130">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="53fb6-130">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="53fb6-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="53fb6-131">Validation File</span></span>  <br/> |<span data-ttu-id="53fb6-132">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="53fb6-132">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="53fb6-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="53fb6-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="53fb6-134">True</span><span class="sxs-lookup"><span data-stu-id="53fb6-134">True</span></span>  <br/> |
   

