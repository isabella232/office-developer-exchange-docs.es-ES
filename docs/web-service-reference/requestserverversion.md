---
title: RequestServerVersion
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RequestServerVersion
api_type:
- schema
ms.assetid: af4032d5-42b3-463e-9d0a-8236d78e5b75
description: El elemento RequestServerVersion contiene la información de control de versiones que identifica la versión del esquema de destino para una solicitud.
ms.openlocfilehash: 0092d90a5fc479363f6d774b793c7148ad29f21c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837143"
---
# <a name="requestserverversion"></a><span data-ttu-id="802d8-103">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="802d8-103">RequestServerVersion</span></span>

<span data-ttu-id="802d8-104">El elemento **RequestServerVersion** contiene la información de control de versiones que identifica la versión del esquema de destino para una solicitud.</span><span class="sxs-lookup"><span data-stu-id="802d8-104">The **RequestServerVersion** element contains the versioning information that identifies the schema version to target for a request.</span></span> 
  
```XML
<RequestServerVersion Version=""/>
```

 <span data-ttu-id="802d8-105">**ExchangeVersionType**</span><span class="sxs-lookup"><span data-stu-id="802d8-105">**ExchangeVersionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="802d8-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="802d8-106">Attributes and elements</span></span>

<span data-ttu-id="802d8-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="802d8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="802d8-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="802d8-108">Attributes</span></span>

|<span data-ttu-id="802d8-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="802d8-109">**Attribute**</span></span>|<span data-ttu-id="802d8-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="802d8-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="802d8-111">Versión</span><span class="sxs-lookup"><span data-stu-id="802d8-111">Version</span></span>  <br/> |<span data-ttu-id="802d8-112">Describe la versión de destino para la solicitud.</span><span class="sxs-lookup"><span data-stu-id="802d8-112">Describes the version to target for the request.</span></span> <span data-ttu-id="802d8-113">Este atributo es necesario cuando la versión del servidor de destino es una versión de Exchange a partir de Exchange Server 2010.</span><span class="sxs-lookup"><span data-stu-id="802d8-113">This attribute is required when the target server version is a version of Exchange starting with Exchange Server 2010.</span></span>  <br/> |
   
#### <a name="version-attribute-values"></a><span data-ttu-id="802d8-114">Valores de atributo de versión</span><span class="sxs-lookup"><span data-stu-id="802d8-114">Version attribute values</span></span>

|<span data-ttu-id="802d8-115">**Valor**</span><span class="sxs-lookup"><span data-stu-id="802d8-115">**Value**</span></span>|<span data-ttu-id="802d8-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="802d8-116">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="802d8-117">Exchange2007</span><span class="sxs-lookup"><span data-stu-id="802d8-117">Exchange2007</span></span>  <br/> |<span data-ttu-id="802d8-118">Los archivos de esquema para la versión de lanzamiento inicial de Exchange 2007 de destino.</span><span class="sxs-lookup"><span data-stu-id="802d8-118">Target the schema files for the initial release version of Exchange 2007.</span></span>  <br/> |
|<span data-ttu-id="802d8-119">Exchange2007_SP1</span><span class="sxs-lookup"><span data-stu-id="802d8-119">Exchange2007_SP1</span></span>  <br/> |<span data-ttu-id="802d8-120">Los archivos de esquema para Exchange 2007 Service Pack 1 (SP1), Service Pack 2 (SP2) de Exchange 2007 y Exchange 2007 Service Pack 3 (SP3) de destino.</span><span class="sxs-lookup"><span data-stu-id="802d8-120">Target the schema files for Exchange 2007 Service Pack 1 (SP1), Exchange 2007 Service Pack 2 (SP2), and Exchange 2007 Service Pack 3 (SP3).</span></span>  <br/> |
|<span data-ttu-id="802d8-121">Exchange2010</span><span class="sxs-lookup"><span data-stu-id="802d8-121">Exchange2010</span></span>  <br/> |<span data-ttu-id="802d8-122">Los archivos de esquema para Exchange 2010 de destino.</span><span class="sxs-lookup"><span data-stu-id="802d8-122">Target the schema files for Exchange 2010.</span></span>  <br/> |
|<span data-ttu-id="802d8-123">Exchange2010_SP1</span><span class="sxs-lookup"><span data-stu-id="802d8-123">Exchange2010_SP1</span></span>  <br/> |<span data-ttu-id="802d8-124">Los archivos de esquema para Exchange 2010 Service Pack 1 (SP1) de destino.</span><span class="sxs-lookup"><span data-stu-id="802d8-124">Target the schema files for Exchange 2010 Service Pack 1 (SP1).</span></span>  <br/> |
|<span data-ttu-id="802d8-125">Exchange2010_SP2</span><span class="sxs-lookup"><span data-stu-id="802d8-125">Exchange2010_SP2</span></span>  <br/> |<span data-ttu-id="802d8-126">Los archivos de esquema para Exchange 2010 Service Pack 2 (SP2) y Service Pack 3 (SP3) de Exchange 2010 de destino.</span><span class="sxs-lookup"><span data-stu-id="802d8-126">Target the schema files for Exchange 2010 Service Pack 2 (SP2) and Exchange 2010 Service Pack 3 (SP3).</span></span>  <br/> |
|<span data-ttu-id="802d8-127">Exchange2013</span><span class="sxs-lookup"><span data-stu-id="802d8-127">Exchange2013</span></span>  <br/> |<span data-ttu-id="802d8-128">Los archivos de esquema para Exchange 2013 de destino.</span><span class="sxs-lookup"><span data-stu-id="802d8-128">Target the schema files for Exchange 2013.</span></span>  <br/> |
|<span data-ttu-id="802d8-129">Exchange2013_SP1</span><span class="sxs-lookup"><span data-stu-id="802d8-129">Exchange2013_SP1</span></span>  <br/> |<span data-ttu-id="802d8-130">Los archivos de esquema para Exchange 2013 Service Pack 1 (SP1) de destino.</span><span class="sxs-lookup"><span data-stu-id="802d8-130">Target the schema files for Exchange 2013 Service Pack 1 (SP1).</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="802d8-131">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="802d8-131">Child elements</span></span>

<span data-ttu-id="802d8-132">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="802d8-132">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="802d8-133">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="802d8-133">Parent elements</span></span>

<span data-ttu-id="802d8-134">El elemento **RequestServerVersion** se encuentra en el encabezado SOAP.</span><span class="sxs-lookup"><span data-stu-id="802d8-134">The **RequestServerVersion** element is located in the SOAP header.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="802d8-135">Comentarios</span><span class="sxs-lookup"><span data-stu-id="802d8-135">Remarks</span></span>

<span data-ttu-id="802d8-136">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="802d8-136">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="802d8-137">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="802d8-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="802d8-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="802d8-138">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="802d8-139">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="802d8-139">Schema Name</span></span>  <br/> |<span data-ttu-id="802d8-140">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="802d8-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="802d8-141">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="802d8-141">Validation File</span></span>  <br/> |<span data-ttu-id="802d8-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="802d8-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="802d8-143">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="802d8-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="802d8-144">False</span><span class="sxs-lookup"><span data-stu-id="802d8-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="802d8-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="802d8-145">See also</span></span>



- [<span data-ttu-id="802d8-146">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="802d8-146">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="802d8-147">Solicitudes de control de versiones</span><span class="sxs-lookup"><span data-stu-id="802d8-147">Versioning Requests</span></span>](http://msdn.microsoft.com/library/76877b0a-d2e5-4c74-9295-7b445a41d46a%28Office.15%29.aspx)

