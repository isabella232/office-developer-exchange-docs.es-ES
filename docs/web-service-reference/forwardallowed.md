---
title: ForwardAllowed
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bc32e0f4-61e9-4c9f-9a03-90a07eb51c53
description: El elemento ForwardAllowed especifica si está habilitado el reenvío de mensajes de correo electrónico.
ms.openlocfilehash: 4baa170a531cc9021102ff2255afc113f40e2348
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764702"
---
# <a name="forwardallowed"></a><span data-ttu-id="539fa-103">ForwardAllowed</span><span class="sxs-lookup"><span data-stu-id="539fa-103">ForwardAllowed</span></span>

<span data-ttu-id="539fa-104">El elemento **ForwardAllowed** especifica si está habilitado el reenvío de mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="539fa-104">The **ForwardAllowed** element specifies whether forwarding emails is enabled.</span></span> 
  
```XML
<ForwardAllowed>true | false</ForwardAllowed>
```

 <span data-ttu-id="539fa-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="539fa-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="539fa-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="539fa-106">Attributes and elements</span></span>

<span data-ttu-id="539fa-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="539fa-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="539fa-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="539fa-108">Attributes</span></span>

<span data-ttu-id="539fa-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="539fa-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="539fa-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="539fa-110">Child elements</span></span>

<span data-ttu-id="539fa-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="539fa-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="539fa-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="539fa-112">Parent elements</span></span>

|<span data-ttu-id="539fa-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="539fa-113">**Element**</span></span>|<span data-ttu-id="539fa-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="539fa-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="539fa-115">RightsManagementLicenseData</span><span class="sxs-lookup"><span data-stu-id="539fa-115">RightsManagementLicenseData</span></span>](rightsmanagementlicensedata.md) <br/> |<span data-ttu-id="539fa-116">Especifica información sobre la licencia de administración de derechos.</span><span class="sxs-lookup"><span data-stu-id="539fa-116">Specifies information about the rights management license.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="539fa-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="539fa-117">Text value</span></span>

<span data-ttu-id="539fa-118">Un valor de texto de **true** para el elemento **ForwardAllowed** indica que se permite el reenvío de mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="539fa-118">A text value of **true** for the **ForwardAllowed** element indicates that forwarding emails is allowed.</span></span> <span data-ttu-id="539fa-119">Un valor de **false** indica que no se permite el reenvío.</span><span class="sxs-lookup"><span data-stu-id="539fa-119">A value of **false** indicates that forwarding is not allowed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="539fa-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="539fa-120">Remarks</span></span>

<span data-ttu-id="539fa-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="539fa-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="539fa-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="539fa-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="539fa-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="539fa-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="539fa-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="539fa-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="539fa-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="539fa-125">Schema Name</span></span>  <br/> |<span data-ttu-id="539fa-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="539fa-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="539fa-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="539fa-127">Validation File</span></span>  <br/> |<span data-ttu-id="539fa-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="539fa-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="539fa-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="539fa-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="539fa-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="539fa-130">See also</span></span>



- [<span data-ttu-id="539fa-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="539fa-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

