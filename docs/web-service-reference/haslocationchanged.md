---
title: HasLocationChanged
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5fd465b4-6070-4cd0-9ac3-ed9d2bfd5951
description: El elemento HasLocationChanged especifica si se ha cambiado la propiedad de ubicación de una reunión.
ms.openlocfilehash: dbb811b93149be0bb43fbb2f579a5086a396e401
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835804"
---
# <a name="haslocationchanged"></a><span data-ttu-id="26d35-103">HasLocationChanged</span><span class="sxs-lookup"><span data-stu-id="26d35-103">HasLocationChanged</span></span>

<span data-ttu-id="26d35-104">El elemento **HasLocationChanged** especifica si se ha cambiado la propiedad de ubicación de una reunión.</span><span class="sxs-lookup"><span data-stu-id="26d35-104">The **HasLocationChanged** element specifies whether the location property of a meeting has changed.</span></span> 
  
```XML
<HasLocationChanged> true | false </HasLocationChanged>
```

 <span data-ttu-id="26d35-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="26d35-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="26d35-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="26d35-106">Attributes and elements</span></span>

<span data-ttu-id="26d35-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="26d35-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="26d35-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="26d35-108">Attributes</span></span>

<span data-ttu-id="26d35-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="26d35-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="26d35-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="26d35-110">Child elements</span></span>

<span data-ttu-id="26d35-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="26d35-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="26d35-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="26d35-112">Parent elements</span></span>

|<span data-ttu-id="26d35-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="26d35-113">**Element**</span></span>|<span data-ttu-id="26d35-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="26d35-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="26d35-115">ChangeHighlights</span><span class="sxs-lookup"><span data-stu-id="26d35-115">ChangeHighlights</span></span>](changehighlights.md) <br/> |<span data-ttu-id="26d35-116">Especifica qué ha cambiado entre dos versiones de una reunión de mensaje de solicitud.</span><span class="sxs-lookup"><span data-stu-id="26d35-116">Specifies what has changed between two versions of a meeting request message.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="26d35-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="26d35-117">Text value</span></span>

<span data-ttu-id="26d35-118">Un valor de texto de **true** para el elemento **HasLocationChanged** indica que ha cambiado la propiedad de ubicación de una reunión.</span><span class="sxs-lookup"><span data-stu-id="26d35-118">A text value of **true** for the **HasLocationChanged** element indicates that the location property of a meeting has changed.</span></span> <span data-ttu-id="26d35-119">Un valor **false** indica que no ha cambiado la propiedad de ubicación de una reunión.</span><span class="sxs-lookup"><span data-stu-id="26d35-119">A value **false** indicates that the location property of a meeting has not changed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="26d35-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="26d35-120">Remarks</span></span>

<span data-ttu-id="26d35-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="26d35-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="26d35-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="26d35-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="26d35-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="26d35-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="26d35-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="26d35-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="26d35-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="26d35-125">Schema Name</span></span>  <br/> |<span data-ttu-id="26d35-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="26d35-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="26d35-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="26d35-127">Validation File</span></span>  <br/> |<span data-ttu-id="26d35-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="26d35-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="26d35-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="26d35-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="26d35-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="26d35-130">See also</span></span>



- [<span data-ttu-id="26d35-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="26d35-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

