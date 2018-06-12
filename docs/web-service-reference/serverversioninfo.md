---
title: ServerVersionInfo
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ServerVersionInfo
api_type:
- schema
ms.assetid: c04a6872-ca27-432b-aac2-36b023d0afc6
description: El elemento ServerVersionInfo representa el número de versión de Microsoft Exchange Server.
ms.openlocfilehash: aff8a6542e2ae6fb1148dd29051b7b33ad90eeff
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837389"
---
# <a name="serverversioninfo"></a><span data-ttu-id="5aa65-103">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="5aa65-103">ServerVersionInfo</span></span>

<span data-ttu-id="5aa65-104">El elemento **ServerVersionInfo** representa el número de versión de Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="5aa65-104">The **ServerVersionInfo** element represents the Microsoft Exchange Server version number.</span></span> 
  
```xml
<ServerVersionInfo MajorVersion="" MinorVersion="" MajorBuildNumber="" MinorBuildNumber="" Version="" />
```

## <a name="attributes-and-elements"></a><span data-ttu-id="5aa65-105">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="5aa65-105">Attributes and elements</span></span>

<span data-ttu-id="5aa65-106">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="5aa65-106">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5aa65-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="5aa65-107">Attributes</span></span>

|<span data-ttu-id="5aa65-108">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="5aa65-108">**Attribute**</span></span>|<span data-ttu-id="5aa65-109">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5aa65-109">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5aa65-110">MajorVersion</span><span class="sxs-lookup"><span data-stu-id="5aa65-110">MajorVersion</span></span>  <br/> |<span data-ttu-id="5aa65-111">Describe el número de versión principal.</span><span class="sxs-lookup"><span data-stu-id="5aa65-111">Describes the major version number.</span></span>  <br/> |
|<span data-ttu-id="5aa65-112">MinorVersion</span><span class="sxs-lookup"><span data-stu-id="5aa65-112">MinorVersion</span></span>  <br/> |<span data-ttu-id="5aa65-113">Describe el número de versión secundaria.</span><span class="sxs-lookup"><span data-stu-id="5aa65-113">Describes the minor version number.</span></span>  <br/> |
|<span data-ttu-id="5aa65-114">MajorBuildNumber</span><span class="sxs-lookup"><span data-stu-id="5aa65-114">MajorBuildNumber</span></span>  <br/> |<span data-ttu-id="5aa65-115">Describe el número de versión de compilación principal.</span><span class="sxs-lookup"><span data-stu-id="5aa65-115">Describes the major build number.</span></span>  <br/> |
|<span data-ttu-id="5aa65-116">MinorBuildNumber</span><span class="sxs-lookup"><span data-stu-id="5aa65-116">MinorBuildNumber</span></span>  <br/> |<span data-ttu-id="5aa65-117">Describe el número de compilación secundaria.</span><span class="sxs-lookup"><span data-stu-id="5aa65-117">Describes the minor build number.</span></span>  <br/> |
|<span data-ttu-id="5aa65-118">Versión</span><span class="sxs-lookup"><span data-stu-id="5aa65-118">Version</span></span>  <br/> |<span data-ttu-id="5aa65-119">Describe la versión de esquema de Exchange Web Services (EWS).</span><span class="sxs-lookup"><span data-stu-id="5aa65-119">Describes the Exchange Web Services (EWS) schema version.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="5aa65-120">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5aa65-120">Child elements</span></span>

<span data-ttu-id="5aa65-121">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5aa65-121">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5aa65-122">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5aa65-122">Parent elements</span></span>

<span data-ttu-id="5aa65-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5aa65-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5aa65-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5aa65-124">Remarks</span></span>

<span data-ttu-id="5aa65-125">Este elemento se devuelve en el encabezado SOAP de un mensaje de respuesta de los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="5aa65-125">This element is returned in the SOAP header of an Exchange Web Services response message.</span></span>
  
<span data-ttu-id="5aa65-126">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server que tiene instalada la función del servidor acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="5aa65-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="5aa65-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="5aa65-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5aa65-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5aa65-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5aa65-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="5aa65-129">Schema Name</span></span>  <br/> |<span data-ttu-id="5aa65-130">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="5aa65-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="5aa65-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="5aa65-131">Validation File</span></span>  <br/> |<span data-ttu-id="5aa65-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5aa65-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5aa65-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="5aa65-133">Can Be Empty</span></span>  <br/> |<span data-ttu-id="5aa65-134">False</span><span class="sxs-lookup"><span data-stu-id="5aa65-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5aa65-135">Ver también</span><span class="sxs-lookup"><span data-stu-id="5aa65-135">See also</span></span>



- [<span data-ttu-id="5aa65-136">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="5aa65-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

