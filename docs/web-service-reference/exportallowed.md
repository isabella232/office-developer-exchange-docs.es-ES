---
title: ExportAllowed
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dcff5ccc-31dc-4941-9f71-d6519133aebb
description: El elemento ExportAllowed especifica si está habilitada la exportación.
ms.openlocfilehash: 5c07941e0a79394bbdaa1a1f62b20adedfe7a9bf
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764494"
---
# <a name="exportallowed"></a><span data-ttu-id="67590-103">ExportAllowed</span><span class="sxs-lookup"><span data-stu-id="67590-103">ExportAllowed</span></span>

<span data-ttu-id="67590-104">El elemento **ExportAllowed** especifica si está habilitada la exportación.</span><span class="sxs-lookup"><span data-stu-id="67590-104">The **ExportAllowed** element specifies whether exporting is enabled.</span></span> 
  
```XML
<ExportAllowed>true | false</ExportAllowed>
```

 <span data-ttu-id="67590-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="67590-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="67590-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="67590-106">Attributes and elements</span></span>

<span data-ttu-id="67590-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="67590-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="67590-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="67590-108">Attributes</span></span>

<span data-ttu-id="67590-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="67590-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="67590-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="67590-110">Child elements</span></span>

<span data-ttu-id="67590-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="67590-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="67590-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="67590-112">Parent elements</span></span>

|<span data-ttu-id="67590-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="67590-113">**Element**</span></span>|<span data-ttu-id="67590-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="67590-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="67590-115">RightsManagementLicenseData</span><span class="sxs-lookup"><span data-stu-id="67590-115">RightsManagementLicenseData</span></span>](rightsmanagementlicensedata.md) <br/> |<span data-ttu-id="67590-116">Especifica información sobre la licencia de administración de derechos.</span><span class="sxs-lookup"><span data-stu-id="67590-116">Specifies information about the rights management license.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="67590-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="67590-117">Text value</span></span>

<span data-ttu-id="67590-118">Un valor de texto de **true** para el elemento **ExportAllowed** indica que se permite la exportación.</span><span class="sxs-lookup"><span data-stu-id="67590-118">A text value of **true** for the **ExportAllowed** element indicates that exporting is allowed.</span></span> <span data-ttu-id="67590-119">Un valor de **false** indica que no se permite la exportación.</span><span class="sxs-lookup"><span data-stu-id="67590-119">A value of **false** indicates that exporting is not allowed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="67590-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="67590-120">Remarks</span></span>

<span data-ttu-id="67590-121">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="67590-121">This element is optional.</span></span>
  
<span data-ttu-id="67590-122">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="67590-122">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="67590-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="67590-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="67590-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="67590-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="67590-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="67590-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="67590-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="67590-126">Schema Name</span></span>  <br/> |<span data-ttu-id="67590-127">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="67590-127">Type schema</span></span>  <br/> |
|<span data-ttu-id="67590-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="67590-128">Validation File</span></span>  <br/> |<span data-ttu-id="67590-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="67590-129">types.xsd</span></span>  <br/> |
|<span data-ttu-id="67590-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="67590-130">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="67590-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="67590-131">See also</span></span>



- [<span data-ttu-id="67590-132">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="67590-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

