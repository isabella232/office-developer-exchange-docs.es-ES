---
title: Nombre (seguimiento de mensajes)
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
description: El elemento Name representa el nombre de la propiedad de un informe de seguimiento de mensajes.
ms.openlocfilehash: 86f049c0a90dbeb55418a5eee58079adf17e5ded
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/01/2020
ms.locfileid: "44466902"
---
# <a name="name-message-tracking"></a><span data-ttu-id="ae40a-103">Nombre (seguimiento de mensajes)</span><span class="sxs-lookup"><span data-stu-id="ae40a-103">Name (Message Tracking)</span></span>

<span data-ttu-id="ae40a-104">El elemento **Name** representa el nombre de la propiedad de un informe de seguimiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="ae40a-104">The **Name** element represents the property name for a message tracking report.</span></span> 
  
```xml
<Name/>
```

<span data-ttu-id="ae40a-105">**String**</span><span class="sxs-lookup"><span data-stu-id="ae40a-105">**String**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="ae40a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ae40a-106">Attributes and elements</span></span>

<span data-ttu-id="ae40a-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ae40a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ae40a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="ae40a-108">Attributes</span></span>

<span data-ttu-id="ae40a-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="ae40a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ae40a-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ae40a-110">Child elements</span></span>

<span data-ttu-id="ae40a-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="ae40a-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ae40a-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ae40a-112">Parent elements</span></span>

|<span data-ttu-id="ae40a-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ae40a-113">**Element**</span></span>|<span data-ttu-id="ae40a-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ae40a-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ae40a-115">TrackingPropertyType</span><span class="sxs-lookup"><span data-stu-id="ae40a-115">TrackingPropertyType</span></span>](trackingpropertytype.md) <br/> |<span data-ttu-id="ae40a-116">Representa un par de nombre y valor de cadenas que se usa para crear propiedades para los informes de seguimiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="ae40a-116">Represents a name and value pair of strings that is used to create properties for message tracking reports.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ae40a-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="ae40a-117">Text value</span></span>

<span data-ttu-id="ae40a-118">Es necesario un valor de texto si se usa este elemento.</span><span class="sxs-lookup"><span data-stu-id="ae40a-118">A text value is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ae40a-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ae40a-119">Remarks</span></span>

<span data-ttu-id="ae40a-120">Este elemento se puede producir al menos una vez en el elemento [TrackingPropertyType](trackingpropertytype.md) .</span><span class="sxs-lookup"><span data-stu-id="ae40a-120">This element can occur at most one time in the [TrackingPropertyType](trackingpropertytype.md) element.</span></span> 
  
<span data-ttu-id="ae40a-121">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange. este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="ae40a-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ae40a-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ae40a-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ae40a-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="ae40a-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ae40a-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ae40a-124">Schema Name</span></span>  <br/> |<span data-ttu-id="ae40a-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="ae40a-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="ae40a-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ae40a-126">Validation File</span></span>  <br/> |<span data-ttu-id="ae40a-127">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="ae40a-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ae40a-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ae40a-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="ae40a-129">Falso</span><span class="sxs-lookup"><span data-stu-id="ae40a-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ae40a-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="ae40a-130">See also</span></span>

- [<span data-ttu-id="ae40a-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="ae40a-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

