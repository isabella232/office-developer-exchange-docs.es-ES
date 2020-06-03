---
title: ExceptionFieldURI
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ExceptionFieldURI
api_type:
- schema
ms.assetid: 7afda93a-0f8c-4c9e-8e09-f1b0bfc928bf
description: El elemento ExceptionFieldURI identifica errores concretos en una solicitud. Este elemento solo se usa como parte de una respuesta de error en el nodo MessageXml.
ms.openlocfilehash: a47d44098f85d8bacb1e7a2c48a33e478e56c7ac
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44454347"
---
# <a name="exceptionfielduri"></a><span data-ttu-id="1d18b-104">ExceptionFieldURI</span><span class="sxs-lookup"><span data-stu-id="1d18b-104">ExceptionFieldURI</span></span>

<span data-ttu-id="1d18b-105">El elemento **ExceptionFieldURI** identifica errores concretos en una solicitud.</span><span class="sxs-lookup"><span data-stu-id="1d18b-105">The **ExceptionFieldURI** element identifies particular errors in a request.</span></span> <span data-ttu-id="1d18b-106">Este elemento solo se usa como parte de una respuesta de error en el nodo [MessageXml](messagexml.md) .</span><span class="sxs-lookup"><span data-stu-id="1d18b-106">This element is only used as part of an error response in the [MessageXml](messagexml.md) node.</span></span> 
  
```xml
<ExceptionFieldURI FieldURI="" />
```

 <span data-ttu-id="1d18b-107">**ExceptionPropertyURIType**</span><span class="sxs-lookup"><span data-stu-id="1d18b-107">**ExceptionPropertyURIType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1d18b-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="1d18b-108">Attributes and elements</span></span>

<span data-ttu-id="1d18b-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="1d18b-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1d18b-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="1d18b-110">Attributes</span></span>

|<span data-ttu-id="1d18b-111">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="1d18b-111">**Attribute**</span></span>|<span data-ttu-id="1d18b-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1d18b-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1d18b-113">**FieldURI**</span><span class="sxs-lookup"><span data-stu-id="1d18b-113">**FieldURI**</span></span> <br/> |<span data-ttu-id="1d18b-114">Identifica una propiedad de una ocurrencia de un elemento periódico.</span><span class="sxs-lookup"><span data-stu-id="1d18b-114">Identifies a property of an occurrence of a recurring item.</span></span> <span data-ttu-id="1d18b-115">Este atributo es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1d18b-115">This attribute is required.</span></span>  <br/> |
   
#### <a name="fielduri-attribute"></a><span data-ttu-id="1d18b-116">Atributo FieldURI</span><span class="sxs-lookup"><span data-stu-id="1d18b-116">FieldURI Attribute</span></span>

|<span data-ttu-id="1d18b-117">**Valor**</span><span class="sxs-lookup"><span data-stu-id="1d18b-117">**Value**</span></span>|<span data-ttu-id="1d18b-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1d18b-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1d18b-119">datos adjuntos: nombre</span><span class="sxs-lookup"><span data-stu-id="1d18b-119">attachment:Name</span></span>  <br/> |<span data-ttu-id="1d18b-120">Identifica el nombre de datos adjuntos que contiene un error.</span><span class="sxs-lookup"><span data-stu-id="1d18b-120">Identifies the attachment name as containing an error.</span></span>  <br/> |
|<span data-ttu-id="1d18b-121">datos adjuntos: ContentType</span><span class="sxs-lookup"><span data-stu-id="1d18b-121">attachment:ContentType</span></span>  <br/> |<span data-ttu-id="1d18b-122">Identifica el tipo de contenido que contiene un error.</span><span class="sxs-lookup"><span data-stu-id="1d18b-122">Identifies the content type as containing an error.</span></span>  <br/> |
|<span data-ttu-id="1d18b-123">datos adjuntos: contenido</span><span class="sxs-lookup"><span data-stu-id="1d18b-123">attachment:Content</span></span>  <br/> |<span data-ttu-id="1d18b-124">Identifica el contenido como que contiene un error.</span><span class="sxs-lookup"><span data-stu-id="1d18b-124">Identifies the content as containing an error.</span></span>  <br/> |
|<span data-ttu-id="1d18b-125">periodicidad: mes</span><span class="sxs-lookup"><span data-stu-id="1d18b-125">recurrence:Month</span></span>  <br/> |<span data-ttu-id="1d18b-126">Identifica el campo month con un error.</span><span class="sxs-lookup"><span data-stu-id="1d18b-126">Identifies the month field as containing an error.</span></span>  <br/> |
|<span data-ttu-id="1d18b-127">periodicidad: DayOfWeekIndex</span><span class="sxs-lookup"><span data-stu-id="1d18b-127">recurrence:DayOfWeekIndex</span></span>  <br/> |<span data-ttu-id="1d18b-128">Identifica el índice del día de la semana que contiene un error.</span><span class="sxs-lookup"><span data-stu-id="1d18b-128">Identifies the day of week index as containing an error.</span></span>  <br/> |
|<span data-ttu-id="1d18b-129">periodicidad: DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="1d18b-129">recurrence:DaysOfWeek</span></span>  <br/> |<span data-ttu-id="1d18b-130">Identifica la propiedad DaysOfWeek que contiene un error.</span><span class="sxs-lookup"><span data-stu-id="1d18b-130">Identifies the DaysOfWeek property as containing an error.</span></span>  <br/> |
|<span data-ttu-id="1d18b-131">periodicidad: DayOfMonth</span><span class="sxs-lookup"><span data-stu-id="1d18b-131">recurrence:DayOfMonth</span></span>  <br/> |<span data-ttu-id="1d18b-132">Identifica el DayOfMonth que contiene un error.</span><span class="sxs-lookup"><span data-stu-id="1d18b-132">Identifies the DayOfMonth as containing an error.</span></span>  <br/> |
|<span data-ttu-id="1d18b-133">periodicidad: intervalo</span><span class="sxs-lookup"><span data-stu-id="1d18b-133">recurrence:Interval</span></span>  <br/> |<span data-ttu-id="1d18b-134">Identifica el intervalo como que contiene un error.</span><span class="sxs-lookup"><span data-stu-id="1d18b-134">Identifies the interval as containing an error.</span></span>  <br/> |
|<span data-ttu-id="1d18b-135">periodicidad: NumberOfOccurrences</span><span class="sxs-lookup"><span data-stu-id="1d18b-135">recurrence:NumberOfOccurrences</span></span>  <br/> |<span data-ttu-id="1d18b-136">Identifica el número de repeticiones que contienen un error.</span><span class="sxs-lookup"><span data-stu-id="1d18b-136">Identifies the number of occurrences as containing an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1d18b-137">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1d18b-137">Child elements</span></span>

<span data-ttu-id="1d18b-138">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1d18b-138">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1d18b-139">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="1d18b-139">Parent elements</span></span>

|<span data-ttu-id="1d18b-140">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="1d18b-140">**Element**</span></span>|<span data-ttu-id="1d18b-141">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1d18b-141">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1d18b-142">MessageXml</span><span class="sxs-lookup"><span data-stu-id="1d18b-142">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="1d18b-143">Proporciona información de respuesta de error adicional.</span><span class="sxs-lookup"><span data-stu-id="1d18b-143">Provides additional error response information.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1d18b-144">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1d18b-144">Remarks</span></span>

<span data-ttu-id="1d18b-145">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="1d18b-145">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1d18b-146">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="1d18b-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1d18b-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="1d18b-147">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1d18b-148">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="1d18b-148">Schema Name</span></span>  <br/> |<span data-ttu-id="1d18b-149">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="1d18b-149">Types schema</span></span>  <br/> |
|<span data-ttu-id="1d18b-150">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="1d18b-150">Validation File</span></span>  <br/> |<span data-ttu-id="1d18b-151">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="1d18b-151">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1d18b-152">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="1d18b-152">Can be Empty</span></span>  <br/> |<span data-ttu-id="1d18b-153">Falso</span><span class="sxs-lookup"><span data-stu-id="1d18b-153">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1d18b-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="1d18b-154">See also</span></span>



- [<span data-ttu-id="1d18b-155">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="1d18b-155">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

