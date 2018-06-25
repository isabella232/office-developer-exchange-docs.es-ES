---
title: HasStartTimeChanged
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 04a6968d-7fb5-47ee-b66e-dc99c35dbb63
description: El elemento HasStartTimeChanged especifica si se ha cambiado la hora de inicio para una reunión.
ms.openlocfilehash: 2096084f4ec8848a63d10e0e80fdc7a37e473cd8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835809"
---
# <a name="hasstarttimechanged"></a><span data-ttu-id="4be20-103">HasStartTimeChanged</span><span class="sxs-lookup"><span data-stu-id="4be20-103">HasStartTimeChanged</span></span>

<span data-ttu-id="4be20-104">El elemento **HasStartTimeChanged** especifica si se ha cambiado la hora de inicio para una reunión.</span><span class="sxs-lookup"><span data-stu-id="4be20-104">The **HasStartTimeChanged** element specifies whether the start time for a meeting has changed.</span></span> 
  
```XML
<HasStartTimeChanged> true | false </HasStartTimeChanged>
```

 <span data-ttu-id="4be20-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="4be20-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4be20-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="4be20-106">Attributes and elements</span></span>

<span data-ttu-id="4be20-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="4be20-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4be20-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="4be20-108">Attributes</span></span>

<span data-ttu-id="4be20-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4be20-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4be20-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4be20-110">Child elements</span></span>

<span data-ttu-id="4be20-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4be20-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4be20-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="4be20-112">Parent elements</span></span>

|<span data-ttu-id="4be20-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="4be20-113">**Element**</span></span>|<span data-ttu-id="4be20-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4be20-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4be20-115">ChangeHighlights</span><span class="sxs-lookup"><span data-stu-id="4be20-115">ChangeHighlights</span></span>](changehighlights.md) <br/> |<span data-ttu-id="4be20-116">Especifica qué ha cambiado entre dos versiones de una reunión de mensaje de solicitud.</span><span class="sxs-lookup"><span data-stu-id="4be20-116">Specifies what has changed between two versions of a meeting request message.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4be20-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="4be20-117">Text value</span></span>

<span data-ttu-id="4be20-118">Un valor de texto de **true** para el elemento **HasStartTimeChanged** indica que ha cambiado la hora de inicio para una reunión.</span><span class="sxs-lookup"><span data-stu-id="4be20-118">A text value of **true** for the **HasStartTimeChanged** element indicates that the start time for a meeting has changed.</span></span> <span data-ttu-id="4be20-119">Un valor de **false** indica que no ha cambiado la hora de inicio.</span><span class="sxs-lookup"><span data-stu-id="4be20-119">A value of **false** indicates that the start time has not changed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="4be20-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4be20-120">Remarks</span></span>

<span data-ttu-id="4be20-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="4be20-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="4be20-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="4be20-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4be20-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="4be20-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4be20-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4be20-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4be20-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="4be20-125">Schema Name</span></span>  <br/> |<span data-ttu-id="4be20-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="4be20-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="4be20-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="4be20-127">Validation File</span></span>  <br/> |<span data-ttu-id="4be20-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4be20-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="4be20-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="4be20-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="4be20-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="4be20-130">See also</span></span>



- [<span data-ttu-id="4be20-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="4be20-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

