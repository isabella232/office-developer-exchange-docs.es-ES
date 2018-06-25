---
title: EditAllowed
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e63c4f7e-77c0-4826-b4e2-43b795d03914
description: El elemento EditAllowed especifica si se pueden editar Information Rights Management.
ms.openlocfilehash: 48c7d751c018bf5702b05b41eeaa7ad350189e3a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764308"
---
# <a name="editallowed"></a><span data-ttu-id="73206-103">EditAllowed</span><span class="sxs-lookup"><span data-stu-id="73206-103">EditAllowed</span></span>

<span data-ttu-id="73206-104">El elemento **EditAllowed** especifica si se pueden editar Information Rights Management.</span><span class="sxs-lookup"><span data-stu-id="73206-104">The **EditAllowed** element specifies whether Information Rights Management can be edited.</span></span> 
  
```XML
<EditAllowed> true | false </EditAllowed>
```

 <span data-ttu-id="73206-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="73206-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="73206-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="73206-106">Attributes and elements</span></span>

<span data-ttu-id="73206-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="73206-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="73206-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="73206-108">Attributes</span></span>

<span data-ttu-id="73206-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="73206-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="73206-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="73206-110">Child elements</span></span>

<span data-ttu-id="73206-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="73206-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="73206-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="73206-112">Parent elements</span></span>

|<span data-ttu-id="73206-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="73206-113">**Element**</span></span>|<span data-ttu-id="73206-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="73206-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="73206-115">RightsManagementLicenseData</span><span class="sxs-lookup"><span data-stu-id="73206-115">RightsManagementLicenseData</span></span>](rightsmanagementlicensedata.md) <br/> |<span data-ttu-id="73206-116">Especifica información sobre la licencia de administración de derechos.</span><span class="sxs-lookup"><span data-stu-id="73206-116">Specifies information about the rights management license.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="73206-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="73206-117">Text value</span></span>

<span data-ttu-id="73206-118">Un valor de texto de **true** para el elemento **EditAllowed** indica que se pueden editar Information Rights Management (IRM).</span><span class="sxs-lookup"><span data-stu-id="73206-118">A text value of **true** for the **EditAllowed** element indicates that Information Rights Management (IRM) can be edited.</span></span> <span data-ttu-id="73206-119">Un valor de **false** indica que no se pueden editar IRM.</span><span class="sxs-lookup"><span data-stu-id="73206-119">A value of **false** indicates that IRM cannot be edited.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="73206-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="73206-120">Remarks</span></span>

<span data-ttu-id="73206-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="73206-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="73206-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="73206-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="73206-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="73206-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="73206-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="73206-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="73206-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="73206-125">Schema Name</span></span>  <br/> |<span data-ttu-id="73206-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="73206-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="73206-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="73206-127">Validation File</span></span>  <br/> |<span data-ttu-id="73206-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="73206-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="73206-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="73206-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="73206-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="73206-130">See also</span></span>



- [<span data-ttu-id="73206-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="73206-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

