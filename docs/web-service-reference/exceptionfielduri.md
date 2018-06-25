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
description: El elemento ExceptionFieldURI identifica errores particulares en una solicitud. Este elemento solo se usa como parte de una respuesta de error en el nodo MessageXml.
ms.openlocfilehash: 79909405179cec0d0b86ad12bf52031e1daeb790
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764466"
---
# <a name="exceptionfielduri"></a><span data-ttu-id="42617-104">ExceptionFieldURI</span><span class="sxs-lookup"><span data-stu-id="42617-104">ExceptionFieldURI</span></span>

<span data-ttu-id="42617-105">El elemento **ExceptionFieldURI** identifica errores particulares en una solicitud.</span><span class="sxs-lookup"><span data-stu-id="42617-105">The **ExceptionFieldURI** element identifies particular errors in a request.</span></span> <span data-ttu-id="42617-106">Este elemento solo se usa como parte de una respuesta de error en el nodo [MessageXml](messagexml.md) .</span><span class="sxs-lookup"><span data-stu-id="42617-106">This element is only used as part of an error response in the [MessageXml](messagexml.md) node.</span></span> 
  
```xml
<ExceptionFieldURI FieldURI="" />
```

 <span data-ttu-id="42617-107">**ExceptionPropertyURIType**</span><span class="sxs-lookup"><span data-stu-id="42617-107">**ExceptionPropertyURIType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="42617-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="42617-108">Attributes and elements</span></span>

<span data-ttu-id="42617-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="42617-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="42617-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="42617-110">Attributes</span></span>

|<span data-ttu-id="42617-111">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="42617-111">**Attribute**</span></span>|<span data-ttu-id="42617-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="42617-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="42617-113">**FieldURI**</span><span class="sxs-lookup"><span data-stu-id="42617-113">**FieldURI**</span></span> <br/> |<span data-ttu-id="42617-114">Identifica una propiedad de una ocurrencia de un elemento periódico.</span><span class="sxs-lookup"><span data-stu-id="42617-114">Identifies a property of an occurrence of a recurring item.</span></span> <span data-ttu-id="42617-115">Este atributo es necesario.</span><span class="sxs-lookup"><span data-stu-id="42617-115">This attribute is required.</span></span>  <br/> |
   
#### <a name="fielduri-attribute"></a><span data-ttu-id="42617-116">Atributo FieldURI</span><span class="sxs-lookup"><span data-stu-id="42617-116">FieldURI Attribute</span></span>

|<span data-ttu-id="42617-117">**Valor**</span><span class="sxs-lookup"><span data-stu-id="42617-117">**Value**</span></span>|<span data-ttu-id="42617-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="42617-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="42617-119">Nombre del archivo adjunto:</span><span class="sxs-lookup"><span data-stu-id="42617-119">attachment:Name</span></span>  <br/> |<span data-ttu-id="42617-120">Identifica el nombre de datos adjuntos como que contiene un error.</span><span class="sxs-lookup"><span data-stu-id="42617-120">Identifies the attachment name as containing an error.</span></span>  <br/> |
|<span data-ttu-id="42617-121">datos adjuntos: ContentType</span><span class="sxs-lookup"><span data-stu-id="42617-121">attachment:ContentType</span></span>  <br/> |<span data-ttu-id="42617-122">Identifica el tipo de contenido como que contiene un error.</span><span class="sxs-lookup"><span data-stu-id="42617-122">Identifies the content type as containing an error.</span></span>  <br/> |
|<span data-ttu-id="42617-123">datos adjuntos: contenido</span><span class="sxs-lookup"><span data-stu-id="42617-123">attachment:Content</span></span>  <br/> |<span data-ttu-id="42617-124">Identifica el contenido como que contiene un error.</span><span class="sxs-lookup"><span data-stu-id="42617-124">Identifies the content as containing an error.</span></span>  <br/> |
|<span data-ttu-id="42617-125">Mes de periodicidad:</span><span class="sxs-lookup"><span data-stu-id="42617-125">recurrence:Month</span></span>  <br/> |<span data-ttu-id="42617-126">Identifica el campo mes como que contiene un error.</span><span class="sxs-lookup"><span data-stu-id="42617-126">Identifies the month field as containing an error.</span></span>  <br/> |
|<span data-ttu-id="42617-127">Periodicidad: DayOfWeekIndex</span><span class="sxs-lookup"><span data-stu-id="42617-127">recurrence:DayOfWeekIndex</span></span>  <br/> |<span data-ttu-id="42617-128">Identifica el día de índice de la semana como que contiene un error.</span><span class="sxs-lookup"><span data-stu-id="42617-128">Identifies the day of week index as containing an error.</span></span>  <br/> |
|<span data-ttu-id="42617-129">Periodicidad: DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="42617-129">recurrence:DaysOfWeek</span></span>  <br/> |<span data-ttu-id="42617-130">Identifica la propiedad DaysOfWeek como que contiene un error.</span><span class="sxs-lookup"><span data-stu-id="42617-130">Identifies the DaysOfWeek property as containing an error.</span></span>  <br/> |
|<span data-ttu-id="42617-131">Periodicidad: DayOfMonth</span><span class="sxs-lookup"><span data-stu-id="42617-131">recurrence:DayOfMonth</span></span>  <br/> |<span data-ttu-id="42617-132">Identifica el DayOfMonth como que contiene un error.</span><span class="sxs-lookup"><span data-stu-id="42617-132">Identifies the DayOfMonth as containing an error.</span></span>  <br/> |
|<span data-ttu-id="42617-133">Intervalo de periodicidad:</span><span class="sxs-lookup"><span data-stu-id="42617-133">recurrence:Interval</span></span>  <br/> |<span data-ttu-id="42617-134">Identifica el intervalo como que contiene un error.</span><span class="sxs-lookup"><span data-stu-id="42617-134">Identifies the interval as containing an error.</span></span>  <br/> |
|<span data-ttu-id="42617-135">Periodicidad: NumberOfOccurrences</span><span class="sxs-lookup"><span data-stu-id="42617-135">recurrence:NumberOfOccurrences</span></span>  <br/> |<span data-ttu-id="42617-136">Identifica el número de repeticiones como que contiene un error.</span><span class="sxs-lookup"><span data-stu-id="42617-136">Identifies the number of occurrences as containing an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="42617-137">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="42617-137">Child elements</span></span>

<span data-ttu-id="42617-138">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="42617-138">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="42617-139">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="42617-139">Parent elements</span></span>

|<span data-ttu-id="42617-140">**Element**</span><span class="sxs-lookup"><span data-stu-id="42617-140">**Element**</span></span>|<span data-ttu-id="42617-141">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="42617-141">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="42617-142">MessageXml</span><span class="sxs-lookup"><span data-stu-id="42617-142">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="42617-143">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="42617-143">Provides additional error response information.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="42617-144">Comentarios</span><span class="sxs-lookup"><span data-stu-id="42617-144">Remarks</span></span>

<span data-ttu-id="42617-145">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="42617-145">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="42617-146">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="42617-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="42617-147">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="42617-147">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="42617-148">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="42617-148">Schema Name</span></span>  <br/> |<span data-ttu-id="42617-149">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="42617-149">Types schema</span></span>  <br/> |
|<span data-ttu-id="42617-150">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="42617-150">Validation File</span></span>  <br/> |<span data-ttu-id="42617-151">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="42617-151">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="42617-152">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="42617-152">Can be Empty</span></span>  <br/> |<span data-ttu-id="42617-153">False</span><span class="sxs-lookup"><span data-stu-id="42617-153">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="42617-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="42617-154">See also</span></span>



- [<span data-ttu-id="42617-155">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="42617-155">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

