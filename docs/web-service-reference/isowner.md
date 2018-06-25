---
title: IsOwner
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ea0f0afc-32fe-46cb-8530-62a6ce9490f6
description: El elemento IsOwner especifica si el usuario de correo electrónico especificada es el propietario.
ms.openlocfilehash: aac3c2a599093282542025468d73c55ec4569e29
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836080"
---
# <a name="isowner"></a><span data-ttu-id="5999b-103">IsOwner</span><span class="sxs-lookup"><span data-stu-id="5999b-103">IsOwner</span></span>

<span data-ttu-id="5999b-104">El elemento **IsOwner** especifica si el usuario de correo electrónico especificada es el propietario.</span><span class="sxs-lookup"><span data-stu-id="5999b-104">The **IsOwner** element specifies whether the specified email user is the owner.</span></span> 
  
```XML
<IsOwner>true | false</IsOwner>
```

 <span data-ttu-id="5999b-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="5999b-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5999b-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="5999b-106">Attributes and elements</span></span>

<span data-ttu-id="5999b-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="5999b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5999b-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="5999b-108">Attributes</span></span>

<span data-ttu-id="5999b-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5999b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5999b-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5999b-110">Child elements</span></span>

<span data-ttu-id="5999b-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5999b-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5999b-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5999b-112">Parent elements</span></span>

|<span data-ttu-id="5999b-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="5999b-113">**Element**</span></span>|<span data-ttu-id="5999b-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5999b-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5999b-115">RightsManagementLicenseData</span><span class="sxs-lookup"><span data-stu-id="5999b-115">RightsManagementLicenseData</span></span>](rightsmanagementlicensedata.md) <br/> |<span data-ttu-id="5999b-116">Especifica información sobre la licencia de administración de derechos.</span><span class="sxs-lookup"><span data-stu-id="5999b-116">Specifies information about the rights management license.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5999b-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="5999b-117">Text value</span></span>

<span data-ttu-id="5999b-118">Un valor de texto de **true** para el elemento **IsOwner** indica que el usuario es el propietario de los derechos emitido en un elemento.</span><span class="sxs-lookup"><span data-stu-id="5999b-118">A text value of **true** for the **IsOwner** element indicates that the user is the owner of rights issued on an item.</span></span> <span data-ttu-id="5999b-119">Un valor de **false** indica que el usuario no es el propietario de los derechos emitido en un elemento.</span><span class="sxs-lookup"><span data-stu-id="5999b-119">A value of **false** indicates that the user is not the owner of rights issued on an item.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5999b-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5999b-120">Remarks</span></span>

<span data-ttu-id="5999b-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="5999b-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="5999b-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="5999b-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5999b-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="5999b-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5999b-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5999b-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5999b-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="5999b-125">Schema Name</span></span>  <br/> |<span data-ttu-id="5999b-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="5999b-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="5999b-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="5999b-127">Validation File</span></span>  <br/> |<span data-ttu-id="5999b-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5999b-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="5999b-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="5999b-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="5999b-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="5999b-130">See also</span></span>



- [<span data-ttu-id="5999b-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="5999b-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

