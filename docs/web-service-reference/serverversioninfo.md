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
ms.openlocfilehash: 5bd1fbd8fdee584a9d272fa8ab82f2a31c1357fe
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466832"
---
# <a name="serverversioninfo"></a><span data-ttu-id="1d44a-103">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="1d44a-103">ServerVersionInfo</span></span>

<span data-ttu-id="1d44a-104">El elemento **ServerVersionInfo** representa el número de versión de Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="1d44a-104">The **ServerVersionInfo** element represents the Microsoft Exchange Server version number.</span></span> 
  
```xml
<ServerVersionInfo MajorVersion="" MinorVersion="" MajorBuildNumber="" MinorBuildNumber="" Version="" />
```

## <a name="attributes-and-elements"></a><span data-ttu-id="1d44a-105">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="1d44a-105">Attributes and elements</span></span>

<span data-ttu-id="1d44a-106">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="1d44a-106">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1d44a-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="1d44a-107">Attributes</span></span>

|<span data-ttu-id="1d44a-108">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="1d44a-108">**Attribute**</span></span>|<span data-ttu-id="1d44a-109">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1d44a-109">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1d44a-110">MajorVersion</span><span class="sxs-lookup"><span data-stu-id="1d44a-110">MajorVersion</span></span>  <br/> |<span data-ttu-id="1d44a-111">Describe el número de versión principal.</span><span class="sxs-lookup"><span data-stu-id="1d44a-111">Describes the major version number.</span></span>  <br/> |
|<span data-ttu-id="1d44a-112">MinorVersion</span><span class="sxs-lookup"><span data-stu-id="1d44a-112">MinorVersion</span></span>  <br/> |<span data-ttu-id="1d44a-113">Describe el número de versión secundaria.</span><span class="sxs-lookup"><span data-stu-id="1d44a-113">Describes the minor version number.</span></span>  <br/> |
|<span data-ttu-id="1d44a-114">MajorBuildNumber</span><span class="sxs-lookup"><span data-stu-id="1d44a-114">MajorBuildNumber</span></span>  <br/> |<span data-ttu-id="1d44a-115">Describe el número de compilación principal.</span><span class="sxs-lookup"><span data-stu-id="1d44a-115">Describes the major build number.</span></span>  <br/> |
|<span data-ttu-id="1d44a-116">MinorBuildNumber</span><span class="sxs-lookup"><span data-stu-id="1d44a-116">MinorBuildNumber</span></span>  <br/> |<span data-ttu-id="1d44a-117">Describe el número de compilación secundaria.</span><span class="sxs-lookup"><span data-stu-id="1d44a-117">Describes the minor build number.</span></span>  <br/> |
|<span data-ttu-id="1d44a-118">Versión</span><span class="sxs-lookup"><span data-stu-id="1d44a-118">Version</span></span>  <br/> |<span data-ttu-id="1d44a-119">Describe la versión del esquema de los servicios Web de Exchange (EWS).</span><span class="sxs-lookup"><span data-stu-id="1d44a-119">Describes the Exchange Web Services (EWS) schema version.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1d44a-120">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1d44a-120">Child elements</span></span>

<span data-ttu-id="1d44a-121">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1d44a-121">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1d44a-122">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="1d44a-122">Parent elements</span></span>

<span data-ttu-id="1d44a-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1d44a-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1d44a-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1d44a-124">Remarks</span></span>

<span data-ttu-id="1d44a-125">Este elemento se devuelve en el encabezado SOAP de un mensaje de respuesta de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="1d44a-125">This element is returned in the SOAP header of an Exchange Web Services response message.</span></span>
  
<span data-ttu-id="1d44a-126">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="1d44a-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="1d44a-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="1d44a-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1d44a-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="1d44a-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1d44a-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="1d44a-129">Schema Name</span></span>  <br/> |<span data-ttu-id="1d44a-130">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="1d44a-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="1d44a-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="1d44a-131">Validation File</span></span>  <br/> |<span data-ttu-id="1d44a-132">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="1d44a-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1d44a-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="1d44a-133">Can Be Empty</span></span>  <br/> |<span data-ttu-id="1d44a-134">Falso</span><span class="sxs-lookup"><span data-stu-id="1d44a-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1d44a-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="1d44a-135">See also</span></span>



- [<span data-ttu-id="1d44a-136">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="1d44a-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

