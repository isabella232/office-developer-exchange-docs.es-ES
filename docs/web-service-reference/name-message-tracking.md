---
title: Nombre (el seguimiento de mensajes)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Name
api_type:
- schema
ms.assetid: a1669f6d-53f3-4849-9b30-56909aaeac82
description: El elemento Name representa el nombre de la propiedad para un informe de seguimiento de mensajes.
ms.openlocfilehash: c905df03842de47b2bcbd62897aa9a8cf464cc6d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836501"
---
# <a name="name-message-tracking"></a><span data-ttu-id="92749-103">Nombre (el seguimiento de mensajes)</span><span class="sxs-lookup"><span data-stu-id="92749-103">Name (Message Tracking)</span></span>

<span data-ttu-id="92749-104">El elemento **Name** representa el nombre de la propiedad para un informe de seguimiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="92749-104">The **Name** element represents the property name for a message tracking report.</span></span> 
  
```xml
<Name/>
```

<span data-ttu-id="92749-105">**String**</span><span class="sxs-lookup"><span data-stu-id="92749-105">**String**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="92749-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="92749-106">Attributes and elements</span></span>

<span data-ttu-id="92749-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="92749-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="92749-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="92749-108">Attributes</span></span>

<span data-ttu-id="92749-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="92749-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="92749-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="92749-110">Child elements</span></span>

<span data-ttu-id="92749-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="92749-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="92749-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="92749-112">Parent elements</span></span>

|<span data-ttu-id="92749-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="92749-113">**Element**</span></span>|<span data-ttu-id="92749-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="92749-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="92749-115">TrackingPropertyType</span><span class="sxs-lookup"><span data-stu-id="92749-115">TrackingPropertyType</span></span>](trackingpropertytype.md) <br/> |<span data-ttu-id="92749-116">Representa un par de cadenas nombre y valor que se usa para crear las propiedades de los informes de seguimiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="92749-116">Represents a name and value pair of strings that is used to create properties for message tracking reports.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="92749-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="92749-117">Text value</span></span>

<span data-ttu-id="92749-118">Si se usa este elemento, se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="92749-118">A text value is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="92749-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="92749-119">Remarks</span></span>

<span data-ttu-id="92749-120">Este elemento puede aparecer como máximo una vez en el elemento [TrackingPropertyType](trackingpropertytype.md) .</span><span class="sxs-lookup"><span data-stu-id="92749-120">This element can occur at most one time in the [TrackingPropertyType](trackingpropertytype.md) element.</span></span> 
  
<span data-ttu-id="92749-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda Exchange Web Services.This elemento fue introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="92749-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="92749-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="92749-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="92749-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="92749-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="92749-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="92749-124">Schema Name</span></span>  <br/> |<span data-ttu-id="92749-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="92749-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="92749-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="92749-126">Validation File</span></span>  <br/> |<span data-ttu-id="92749-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="92749-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="92749-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="92749-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="92749-129">False</span><span class="sxs-lookup"><span data-stu-id="92749-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="92749-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="92749-130">See also</span></span>

- [<span data-ttu-id="92749-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="92749-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

