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
description: El elemento ServerVersionInfo contiene la versión del servidor que ha procesado la solicitud.
ms.openlocfilehash: b54b4833361ec78c7f8213473af4638965c7ddae
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467651"
---
# <a name="serverversioninfo-soap"></a><span data-ttu-id="bb659-103">ServerVersionInfo (SOAP)</span><span class="sxs-lookup"><span data-stu-id="bb659-103">ServerVersionInfo (SOAP)</span></span>

<span data-ttu-id="bb659-104">El elemento **ServerVersionInfo** contiene la versión del servidor que ha procesado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bb659-104">The **ServerVersionInfo** element contains the version of the server that processed the request.</span></span> 
  
```XML
<ServerVersionInfo>
   <MajorVersion/>
   <MinorVersion/>
   <MajorBuildNumber/>
   <MinorBuildNumber/>
   <Version/>
</ServerVersionInfo>
```

 <span data-ttu-id="bb659-105">**ServerVersionInfo**</span><span class="sxs-lookup"><span data-stu-id="bb659-105">**ServerVersionInfo**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bb659-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="bb659-106">Attributes and elements</span></span>

<span data-ttu-id="bb659-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="bb659-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bb659-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="bb659-108">Attributes</span></span>

<span data-ttu-id="bb659-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="bb659-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bb659-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="bb659-110">Child elements</span></span>

|<span data-ttu-id="bb659-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="bb659-111">**Element**</span></span>|<span data-ttu-id="bb659-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bb659-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bb659-113">MajorVersion (SOAP)</span><span class="sxs-lookup"><span data-stu-id="bb659-113">MajorVersion (SOAP)</span></span>](majorversion-soap.md) <br/> |<span data-ttu-id="bb659-114">Número de versión principal del servidor.</span><span class="sxs-lookup"><span data-stu-id="bb659-114">The major version number for the server.</span></span>  <br/> |
|[<span data-ttu-id="bb659-115">MinorVersion (SOAP)</span><span class="sxs-lookup"><span data-stu-id="bb659-115">MinorVersion (SOAP)</span></span>](minorversion-soap.md) <br/> |<span data-ttu-id="bb659-116">Número de versión secundaria del servidor.</span><span class="sxs-lookup"><span data-stu-id="bb659-116">The minor version number for the server.</span></span>  <br/> |
|[<span data-ttu-id="bb659-117">MajorBuildNumber (SOAP)</span><span class="sxs-lookup"><span data-stu-id="bb659-117">MajorBuildNumber (SOAP)</span></span>](majorbuildnumber-soap.md) <br/> |<span data-ttu-id="bb659-118">El número de compilación principal del servidor.</span><span class="sxs-lookup"><span data-stu-id="bb659-118">The major build number for the server.</span></span>  <br/> |
|[<span data-ttu-id="bb659-119">MinorBuildNumber (SOAP)</span><span class="sxs-lookup"><span data-stu-id="bb659-119">MinorBuildNumber (SOAP)</span></span>](minorbuildnumber-soap.md) <br/> |<span data-ttu-id="bb659-120">Número de compilación secundaria del servidor.</span><span class="sxs-lookup"><span data-stu-id="bb659-120">The minor build number for the server.</span></span>  <br/> |
|[<span data-ttu-id="bb659-121">Versión (SOAP)</span><span class="sxs-lookup"><span data-stu-id="bb659-121">Version (SOAP)</span></span>](version-soap.md) <br/> |<span data-ttu-id="bb659-122">Una descripción de la versión del producto del servidor.</span><span class="sxs-lookup"><span data-stu-id="bb659-122">A description of the server product version.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="bb659-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="bb659-123">Parent elements</span></span>

<span data-ttu-id="bb659-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="bb659-124">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bb659-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bb659-125">Remarks</span></span>

<span data-ttu-id="bb659-126">Este elemento se devuelve en el encabezado SOAP.</span><span class="sxs-lookup"><span data-stu-id="bb659-126">This element is returned in the SOAP header.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bb659-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="bb659-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bb659-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="bb659-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="bb659-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="bb659-129">Schema Name</span></span>  <br/> |<span data-ttu-id="bb659-130">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="bb659-130">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="bb659-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="bb659-131">Validation File</span></span>  <br/> |<span data-ttu-id="bb659-132">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="bb659-132">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="bb659-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="bb659-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="bb659-134">Verdadero</span><span class="sxs-lookup"><span data-stu-id="bb659-134">True</span></span>  <br/> |
   

