---
title: HasChanged
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 15ff513d-f39e-44ed-a13f-ab3f86fa37e1
description: El elemento HasChanged indica si ha cambiado la foto de un usuario.
ms.openlocfilehash: d777220f55d33cde548d8257cf249b57481a43f8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462790"
---
# <a name="haschanged"></a><span data-ttu-id="21717-103">HasChanged</span><span class="sxs-lookup"><span data-stu-id="21717-103">HasChanged</span></span>

<span data-ttu-id="21717-104">El elemento **HasChanged** indica si ha cambiado la foto de un usuario.</span><span class="sxs-lookup"><span data-stu-id="21717-104">The **HasChanged** element indicates whether a user's photo has changed.</span></span> 
  
```XML
<HasChanged> true | false </HasChanged>
```

 ****
## <a name="attributes-and-elements"></a><span data-ttu-id="21717-105">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="21717-105">Attributes and elements</span></span>

<span data-ttu-id="21717-106">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="21717-106">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="21717-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="21717-107">Attributes</span></span>

<span data-ttu-id="21717-108">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="21717-108">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="21717-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="21717-109">Child elements</span></span>

<span data-ttu-id="21717-110">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="21717-110">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="21717-111">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="21717-111">Parent elements</span></span>

[<span data-ttu-id="21717-112">GetUserPhotoResponse</span><span class="sxs-lookup"><span data-stu-id="21717-112">GetUserPhotoResponse</span></span>](getuserphotoresponse.md)
  
## <a name="text-value"></a><span data-ttu-id="21717-113">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="21717-113">Text value</span></span>

<span data-ttu-id="21717-114">Un valor de texto de **true** para el elemento **HasChanged** indica que la foto ha cambiado desde la última vez que se devolvió.</span><span class="sxs-lookup"><span data-stu-id="21717-114">A text value of **true** for the **HasChanged** element indicates that the photo has changed since the last time it was returned.</span></span> <span data-ttu-id="21717-115">Un valor de **false** indica que la foto no ha cambiado desde la última vez que se devolvió.</span><span class="sxs-lookup"><span data-stu-id="21717-115">A value of **false** indicates that the photo has not changed since the last time it was returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="21717-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="21717-116">Remarks</span></span>

<span data-ttu-id="21717-117">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="21717-117">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="21717-118">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="21717-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="21717-119">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="21717-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="21717-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="21717-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="21717-121">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="21717-121">Schema name</span></span>  <br/> |<span data-ttu-id="21717-122">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="21717-122">Types schema</span></span>  <br/> |
|<span data-ttu-id="21717-123">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="21717-123">Validation file</span></span>  <br/> |<span data-ttu-id="21717-124">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="21717-124">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="21717-125">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="21717-125">Can be empty</span></span>  <br/> ||
   

