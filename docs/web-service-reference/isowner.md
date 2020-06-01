---
title: IsOwner
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ea0f0afc-32fe-46cb-8530-62a6ce9490f6
description: El elemento IsOwner especifica si el usuario de correo electrónico especificado es el propietario.
ms.openlocfilehash: 2dd085aba34052d95efd1e72edca7be4aba71155
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466524"
---
# <a name="isowner"></a><span data-ttu-id="0e208-103">IsOwner</span><span class="sxs-lookup"><span data-stu-id="0e208-103">IsOwner</span></span>

<span data-ttu-id="0e208-104">El elemento **IsOwner** especifica si el usuario de correo electrónico especificado es el propietario.</span><span class="sxs-lookup"><span data-stu-id="0e208-104">The **IsOwner** element specifies whether the specified email user is the owner.</span></span> 
  
```XML
<IsOwner>true | false</IsOwner>
```

 <span data-ttu-id="0e208-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="0e208-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0e208-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="0e208-106">Attributes and elements</span></span>

<span data-ttu-id="0e208-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="0e208-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0e208-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="0e208-108">Attributes</span></span>

<span data-ttu-id="0e208-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="0e208-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0e208-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0e208-110">Child elements</span></span>

<span data-ttu-id="0e208-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="0e208-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0e208-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0e208-112">Parent elements</span></span>

|<span data-ttu-id="0e208-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="0e208-113">**Element**</span></span>|<span data-ttu-id="0e208-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0e208-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0e208-115">RightsManagementLicenseData</span><span class="sxs-lookup"><span data-stu-id="0e208-115">RightsManagementLicenseData</span></span>](rightsmanagementlicensedata.md) <br/> |<span data-ttu-id="0e208-116">Especifica información sobre la licencia de administración de derechos.</span><span class="sxs-lookup"><span data-stu-id="0e208-116">Specifies information about the rights management license.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0e208-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="0e208-117">Text value</span></span>

<span data-ttu-id="0e208-118">Un valor de texto de **true** para el elemento **IsOwner** indica que el usuario es el propietario de los derechos emitidos en un elemento.</span><span class="sxs-lookup"><span data-stu-id="0e208-118">A text value of **true** for the **IsOwner** element indicates that the user is the owner of rights issued on an item.</span></span> <span data-ttu-id="0e208-119">Un valor de **false** indica que el usuario no es el propietario de los derechos emitidos en un elemento.</span><span class="sxs-lookup"><span data-stu-id="0e208-119">A value of **false** indicates that the user is not the owner of rights issued on an item.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="0e208-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0e208-120">Remarks</span></span>

<span data-ttu-id="0e208-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0e208-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="0e208-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="0e208-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0e208-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0e208-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0e208-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="0e208-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0e208-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="0e208-125">Schema Name</span></span>  <br/> |<span data-ttu-id="0e208-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="0e208-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="0e208-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="0e208-127">Validation File</span></span>  <br/> |<span data-ttu-id="0e208-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="0e208-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="0e208-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="0e208-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="0e208-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="0e208-130">See also</span></span>



- [<span data-ttu-id="0e208-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="0e208-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

