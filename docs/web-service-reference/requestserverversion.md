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
description: El elemento RequestServerVersion contiene la información de versión que identifica la versión del esquema que se va a usar como destino de una solicitud.
ms.openlocfilehash: c4ae59a03c812d21153e4338734185d933d914ec
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468323"
---
# <a name="requestserverversion"></a><span data-ttu-id="b36f6-103">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="b36f6-103">RequestServerVersion</span></span>

<span data-ttu-id="b36f6-104">El elemento **RequestServerVersion** contiene la información de versión que identifica la versión del esquema que se va a usar como destino de una solicitud.</span><span class="sxs-lookup"><span data-stu-id="b36f6-104">The **RequestServerVersion** element contains the versioning information that identifies the schema version to target for a request.</span></span> 
  
```XML
<RequestServerVersion Version=""/>
```

 <span data-ttu-id="b36f6-105">**ExchangeVersionType**</span><span class="sxs-lookup"><span data-stu-id="b36f6-105">**ExchangeVersionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b36f6-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b36f6-106">Attributes and elements</span></span>

<span data-ttu-id="b36f6-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b36f6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b36f6-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="b36f6-108">Attributes</span></span>

|<span data-ttu-id="b36f6-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="b36f6-109">**Attribute**</span></span>|<span data-ttu-id="b36f6-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b36f6-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b36f6-111">Versión</span><span class="sxs-lookup"><span data-stu-id="b36f6-111">Version</span></span>  <br/> |<span data-ttu-id="b36f6-112">Describe la versión de destino de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b36f6-112">Describes the version to target for the request.</span></span> <span data-ttu-id="b36f6-113">Este atributo es necesario cuando la versión del servidor de destino es una versión de Exchange que comienza con Exchange Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b36f6-113">This attribute is required when the target server version is a version of Exchange starting with Exchange Server 2010.</span></span>  <br/> |
   
#### <a name="version-attribute-values"></a><span data-ttu-id="b36f6-114">Valores del atributo version</span><span class="sxs-lookup"><span data-stu-id="b36f6-114">Version attribute values</span></span>

|<span data-ttu-id="b36f6-115">**Valor**</span><span class="sxs-lookup"><span data-stu-id="b36f6-115">**Value**</span></span>|<span data-ttu-id="b36f6-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b36f6-116">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b36f6-117">Exchange2007</span><span class="sxs-lookup"><span data-stu-id="b36f6-117">Exchange2007</span></span>  <br/> |<span data-ttu-id="b36f6-118">Destino los archivos de esquema de la versión de lanzamiento inicial de Exchange 2007.</span><span class="sxs-lookup"><span data-stu-id="b36f6-118">Target the schema files for the initial release version of Exchange 2007.</span></span>  <br/> |
|<span data-ttu-id="b36f6-119">Exchange2007_SP1</span><span class="sxs-lookup"><span data-stu-id="b36f6-119">Exchange2007_SP1</span></span>  <br/> |<span data-ttu-id="b36f6-120">Destino los archivos de esquema de Exchange 2007 Service Pack 1 (SP1), Exchange 2007 Service Pack 2 (SP2) y Exchange 2007 Service Pack 3 (SP3).</span><span class="sxs-lookup"><span data-stu-id="b36f6-120">Target the schema files for Exchange 2007 Service Pack 1 (SP1), Exchange 2007 Service Pack 2 (SP2), and Exchange 2007 Service Pack 3 (SP3).</span></span>  <br/> |
|<span data-ttu-id="b36f6-121">Exchange2010</span><span class="sxs-lookup"><span data-stu-id="b36f6-121">Exchange2010</span></span>  <br/> |<span data-ttu-id="b36f6-122">Target los archivos de esquema de Exchange 2010.</span><span class="sxs-lookup"><span data-stu-id="b36f6-122">Target the schema files for Exchange 2010.</span></span>  <br/> |
|<span data-ttu-id="b36f6-123">Exchange2010_SP1</span><span class="sxs-lookup"><span data-stu-id="b36f6-123">Exchange2010_SP1</span></span>  <br/> |<span data-ttu-id="b36f6-124">Target los archivos de esquema de Exchange 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="b36f6-124">Target the schema files for Exchange 2010 Service Pack 1 (SP1).</span></span>  <br/> |
|<span data-ttu-id="b36f6-125">Exchange2010_SP2</span><span class="sxs-lookup"><span data-stu-id="b36f6-125">Exchange2010_SP2</span></span>  <br/> |<span data-ttu-id="b36f6-126">Destino los archivos de esquema de Exchange 2010 Service Pack 2 (SP2) y Exchange 2010 Service Pack 3 (SP3).</span><span class="sxs-lookup"><span data-stu-id="b36f6-126">Target the schema files for Exchange 2010 Service Pack 2 (SP2) and Exchange 2010 Service Pack 3 (SP3).</span></span>  <br/> |
|<span data-ttu-id="b36f6-127">Exchange2013</span><span class="sxs-lookup"><span data-stu-id="b36f6-127">Exchange2013</span></span>  <br/> |<span data-ttu-id="b36f6-128">Target los archivos de esquema de Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="b36f6-128">Target the schema files for Exchange 2013.</span></span>  <br/> |
|<span data-ttu-id="b36f6-129">Exchange2013_SP1</span><span class="sxs-lookup"><span data-stu-id="b36f6-129">Exchange2013_SP1</span></span>  <br/> |<span data-ttu-id="b36f6-130">Target los archivos de esquema de Exchange 2013 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="b36f6-130">Target the schema files for Exchange 2013 Service Pack 1 (SP1).</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b36f6-131">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b36f6-131">Child elements</span></span>

<span data-ttu-id="b36f6-132">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="b36f6-132">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b36f6-133">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b36f6-133">Parent elements</span></span>

<span data-ttu-id="b36f6-134">El elemento **RequestServerVersion** se encuentra en el encabezado SOAP.</span><span class="sxs-lookup"><span data-stu-id="b36f6-134">The **RequestServerVersion** element is located in the SOAP header.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b36f6-135">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b36f6-135">Remarks</span></span>

<span data-ttu-id="b36f6-136">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="b36f6-136">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b36f6-137">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b36f6-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b36f6-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="b36f6-138">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b36f6-139">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b36f6-139">Schema Name</span></span>  <br/> |<span data-ttu-id="b36f6-140">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="b36f6-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="b36f6-141">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b36f6-141">Validation File</span></span>  <br/> |<span data-ttu-id="b36f6-142">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="b36f6-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b36f6-143">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b36f6-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="b36f6-144">Falso</span><span class="sxs-lookup"><span data-stu-id="b36f6-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b36f6-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="b36f6-145">See also</span></span>



- [<span data-ttu-id="b36f6-146">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="b36f6-146">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="b36f6-147">Solicitudes de control de versiones</span><span class="sxs-lookup"><span data-stu-id="b36f6-147">Versioning Requests</span></span>](https://msdn.microsoft.com/library/76877b0a-d2e5-4c74-9295-7b445a41d46a%28Office.15%29.aspx)

