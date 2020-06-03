---
title: Valor (seguimiento de mensajes)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Value
api_type:
- schema
ms.assetid: cb2f228f-775a-4c7d-82e7-41c7c953c808
description: El elemento Value representa el valor de la propiedad para un informe de seguimiento de mensajes.
ms.openlocfilehash: 4f6b5cb9d82a35bbe010b36e409cdc9f3a70173d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465011"
---
# <a name="value-message-tracking"></a><span data-ttu-id="a9501-103">Valor (seguimiento de mensajes)</span><span class="sxs-lookup"><span data-stu-id="a9501-103">Value (Message Tracking)</span></span>

<span data-ttu-id="a9501-104">El elemento **Value** representa el valor de la propiedad para un informe de seguimiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="a9501-104">The **Value** element represents the property value for a message tracking report.</span></span> 
  
```xml
<Value/>
```

<span data-ttu-id="a9501-105">**String**</span><span class="sxs-lookup"><span data-stu-id="a9501-105">**String**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="a9501-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a9501-106">Attributes and elements</span></span>

<span data-ttu-id="a9501-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a9501-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a9501-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="a9501-108">Attributes</span></span>

<span data-ttu-id="a9501-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="a9501-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a9501-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a9501-110">Child elements</span></span>

<span data-ttu-id="a9501-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="a9501-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a9501-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a9501-112">Parent elements</span></span>

|<span data-ttu-id="a9501-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a9501-113">**Element**</span></span>|<span data-ttu-id="a9501-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a9501-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a9501-115">TrackingPropertyType</span><span class="sxs-lookup"><span data-stu-id="a9501-115">TrackingPropertyType</span></span>](trackingpropertytype.md) <br/> |<span data-ttu-id="a9501-116">Representa un par de nombre y valor de cadenas que se usa para crear propiedades para los informes de seguimiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="a9501-116">Represents a name and value pair of strings that is used to create properties for message tracking reports.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a9501-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="a9501-117">Text value</span></span>

<span data-ttu-id="a9501-118">El valor de texto es opcional.</span><span class="sxs-lookup"><span data-stu-id="a9501-118">The text value is optional.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a9501-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a9501-119">Remarks</span></span>

<span data-ttu-id="a9501-120">Este elemento se puede producir al menos una vez en el elemento [TrackingPropertyType](trackingpropertytype.md) .</span><span class="sxs-lookup"><span data-stu-id="a9501-120">This element can occur at most one time in the [TrackingPropertyType](trackingpropertytype.md) element.</span></span> 
  
<span data-ttu-id="a9501-121">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange. este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="a9501-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a9501-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a9501-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a9501-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="a9501-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a9501-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a9501-124">Schema Name</span></span>  <br/> |<span data-ttu-id="a9501-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="a9501-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="a9501-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a9501-126">Validation File</span></span>  <br/> |<span data-ttu-id="a9501-127">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="a9501-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a9501-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a9501-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="a9501-129">Falso</span><span class="sxs-lookup"><span data-stu-id="a9501-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a9501-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="a9501-130">See also</span></span>

- [<span data-ttu-id="a9501-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="a9501-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

