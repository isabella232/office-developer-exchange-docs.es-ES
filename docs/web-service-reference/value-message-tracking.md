---
title: Valor (el seguimiento de mensajes)
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
description: El elemento de valor representa el valor de la propiedad para un informe de seguimiento de mensajes.
ms.openlocfilehash: 152e4fe61a4cff8013ae02900bd84bf244ae84a9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840948"
---
# <a name="value-message-tracking"></a><span data-ttu-id="d1cb1-103">Valor (el seguimiento de mensajes)</span><span class="sxs-lookup"><span data-stu-id="d1cb1-103">Value (Message Tracking)</span></span>

<span data-ttu-id="d1cb1-104">El elemento de **valor** representa el valor de la propiedad para un informe de seguimiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="d1cb1-104">The **Value** element represents the property value for a message tracking report.</span></span> 
  
```xml
<Value/>
```

<span data-ttu-id="d1cb1-105">**String**</span><span class="sxs-lookup"><span data-stu-id="d1cb1-105">**String**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="d1cb1-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d1cb1-106">Attributes and elements</span></span>

<span data-ttu-id="d1cb1-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d1cb1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d1cb1-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="d1cb1-108">Attributes</span></span>

<span data-ttu-id="d1cb1-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d1cb1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d1cb1-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d1cb1-110">Child elements</span></span>

<span data-ttu-id="d1cb1-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d1cb1-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d1cb1-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d1cb1-112">Parent elements</span></span>

|<span data-ttu-id="d1cb1-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="d1cb1-113">**Element**</span></span>|<span data-ttu-id="d1cb1-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d1cb1-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d1cb1-115">TrackingPropertyType</span><span class="sxs-lookup"><span data-stu-id="d1cb1-115">TrackingPropertyType</span></span>](trackingpropertytype.md) <br/> |<span data-ttu-id="d1cb1-116">Representa un par de cadenas nombre y valor que se usa para crear las propiedades de los informes de seguimiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="d1cb1-116">Represents a name and value pair of strings that is used to create properties for message tracking reports.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d1cb1-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="d1cb1-117">Text value</span></span>

<span data-ttu-id="d1cb1-118">El valor de texto es opcional.</span><span class="sxs-lookup"><span data-stu-id="d1cb1-118">The text value is optional.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d1cb1-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d1cb1-119">Remarks</span></span>

<span data-ttu-id="d1cb1-120">Este elemento puede aparecer como máximo una vez en el elemento [TrackingPropertyType](trackingpropertytype.md) .</span><span class="sxs-lookup"><span data-stu-id="d1cb1-120">This element can occur at most one time in the [TrackingPropertyType](trackingpropertytype.md) element.</span></span> 
  
<span data-ttu-id="d1cb1-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda Exchange Web Services.This elemento fue introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="d1cb1-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d1cb1-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d1cb1-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d1cb1-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d1cb1-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d1cb1-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d1cb1-124">Schema Name</span></span>  <br/> |<span data-ttu-id="d1cb1-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="d1cb1-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="d1cb1-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d1cb1-126">Validation File</span></span>  <br/> |<span data-ttu-id="d1cb1-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d1cb1-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d1cb1-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d1cb1-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="d1cb1-129">False</span><span class="sxs-lookup"><span data-stu-id="d1cb1-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d1cb1-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="d1cb1-130">See also</span></span>

- [<span data-ttu-id="d1cb1-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="d1cb1-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

