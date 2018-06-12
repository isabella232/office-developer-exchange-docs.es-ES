---
title: IndexedFieldURI
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IndexedFieldURI
api_type:
- schema
ms.assetid: 5c9cd0b5-7eca-480a-8730-fe98b1779afa
description: El elemento IndexedFieldURI identifica a los miembros individuales de un diccionario.
ms.openlocfilehash: 6a75e8855ecabf15ca31bb1e05d569c258a43b0b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19835909"
---
# <a name="indexedfielduri"></a><span data-ttu-id="40506-103">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="40506-103">IndexedFieldURI</span></span>

<span data-ttu-id="40506-104">El elemento **IndexedFieldURI** identifica a los miembros individuales de un diccionario.</span><span class="sxs-lookup"><span data-stu-id="40506-104">The **IndexedFieldURI** element identifies individual members of a dictionary.</span></span> 
  
```xml
<IndexedFieldURI FieldURI="" FieldIndex="" />
```

 <span data-ttu-id="40506-105">**PathToIndexedFieldType**</span><span class="sxs-lookup"><span data-stu-id="40506-105">**PathToIndexedFieldType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="40506-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="40506-106">Attributes and elements</span></span>

<span data-ttu-id="40506-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="40506-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="40506-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="40506-108">Attributes</span></span>

|<span data-ttu-id="40506-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="40506-109">**Attribute**</span></span>|<span data-ttu-id="40506-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="40506-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="40506-111">**FieldURI**</span><span class="sxs-lookup"><span data-stu-id="40506-111">**FieldURI**</span></span> <br/> |<span data-ttu-id="40506-112">Identifica el diccionario que contiene el miembro para devolver.</span><span class="sxs-lookup"><span data-stu-id="40506-112">Identifies the dictionary that contains the member to return.</span></span> <span data-ttu-id="40506-113">Este atributo es necesario.</span><span class="sxs-lookup"><span data-stu-id="40506-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="40506-114">**FieldIndex**</span><span class="sxs-lookup"><span data-stu-id="40506-114">**FieldIndex**</span></span> <br/> |<span data-ttu-id="40506-115">Identifica el miembro del diccionario para devolver.</span><span class="sxs-lookup"><span data-stu-id="40506-115">Identifies the member of the dictionary to return.</span></span> <span data-ttu-id="40506-116">Este atributo es necesario.</span><span class="sxs-lookup"><span data-stu-id="40506-116">This attribute is required.</span></span>  <br/> |
   
#### <a name="fielduri-attribute"></a><span data-ttu-id="40506-117">Atributo FieldURI</span><span class="sxs-lookup"><span data-stu-id="40506-117">FieldURI Attribute</span></span>

|<span data-ttu-id="40506-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="40506-118">**Value**</span></span>|<span data-ttu-id="40506-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="40506-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="40506-120">elemento: InternetMessageHeader</span><span class="sxs-lookup"><span data-stu-id="40506-120">item:InternetMessageHeader</span></span>  <br/> |<span data-ttu-id="40506-121">Representa el encabezado del mensaje de un elemento.</span><span class="sxs-lookup"><span data-stu-id="40506-121">Represents the message header of an item.</span></span>  <br/> |
|<span data-ttu-id="40506-122">contactos: ImAddress</span><span class="sxs-lookup"><span data-stu-id="40506-122">contacts:ImAddress</span></span>  <br/> |<span data-ttu-id="40506-123">Representa la dirección de un contacto de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="40506-123">Represents the instant messaging address of a contact.</span></span>  <br/> |
|<span data-ttu-id="40506-124">contactos: PhysicalAddress:Street</span><span class="sxs-lookup"><span data-stu-id="40506-124">contacts:PhysicalAddress:Street</span></span>  <br/> |<span data-ttu-id="40506-125">Representa la dirección de un contacto.</span><span class="sxs-lookup"><span data-stu-id="40506-125">Represents the street address of a contact.</span></span>  <br/> |
|<span data-ttu-id="40506-126">contactos: PhysicalAddress:City</span><span class="sxs-lookup"><span data-stu-id="40506-126">contacts:PhysicalAddress:City</span></span>  <br/> |<span data-ttu-id="40506-127">Representa la ciudad de un contacto.</span><span class="sxs-lookup"><span data-stu-id="40506-127">Represents the city of a contact.</span></span>  <br/> |
|<span data-ttu-id="40506-128">contactos: PhysicalAddress:State</span><span class="sxs-lookup"><span data-stu-id="40506-128">contacts:PhysicalAddress:State</span></span>  <br/> |<span data-ttu-id="40506-129">Representa el estado de un contacto.</span><span class="sxs-lookup"><span data-stu-id="40506-129">Represents the state of a contact.</span></span>  <br/> |
|<span data-ttu-id="40506-130">contactos: PhysicalAddress:Country</span><span class="sxs-lookup"><span data-stu-id="40506-130">contacts:PhysicalAddress:Country</span></span>  <br/> |<span data-ttu-id="40506-131">Representa el país o región de un contacto.</span><span class="sxs-lookup"><span data-stu-id="40506-131">Represents the country/region of a contact.</span></span>  <br/> |
|<span data-ttu-id="40506-132">contactos: PhysicalAddress:PostalCode</span><span class="sxs-lookup"><span data-stu-id="40506-132">contacts:PhysicalAddress:PostalCode</span></span>  <br/> |<span data-ttu-id="40506-133">Representa el código postal de un contacto.</span><span class="sxs-lookup"><span data-stu-id="40506-133">Represents the postal code of a contact.</span></span>  <br/> |
|<span data-ttu-id="40506-134">contactos: PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="40506-134">contacts:PhoneNumber</span></span>  <br/> |<span data-ttu-id="40506-135">Representa el número de teléfono de un contacto.</span><span class="sxs-lookup"><span data-stu-id="40506-135">Represents the phone number of a contact.</span></span>  <br/> |
|<span data-ttu-id="40506-136">contactos: EmailAddress</span><span class="sxs-lookup"><span data-stu-id="40506-136">contacts:EmailAddress</span></span>  <br/> |<span data-ttu-id="40506-137">Representa la dirección de correo electrónico de un contacto.</span><span class="sxs-lookup"><span data-stu-id="40506-137">Represents the e-mail address of a contact.</span></span>  <br/> |
|<span data-ttu-id="40506-138">DistributionList:members:Member</span><span class="sxs-lookup"><span data-stu-id="40506-138">distributionlist:Members:Member</span></span>  <br/> |<span data-ttu-id="40506-139">Representa a un miembro de una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="40506-139">Represents a member of a distribution list.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="40506-140">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="40506-140">Child elements</span></span>

<span data-ttu-id="40506-141">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="40506-141">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="40506-142">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="40506-142">Parent elements</span></span>

|<span data-ttu-id="40506-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="40506-143">**Element**</span></span>|<span data-ttu-id="40506-144">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="40506-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="40506-145">AdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="40506-145">AdditionalProperties</span></span>](additionalproperties.md) <br/> |<span data-ttu-id="40506-146">Identifica las propiedades adicionales para obtener, establecer o crear.</span><span class="sxs-lookup"><span data-stu-id="40506-146">Identifies additional properties to get, set, or create.</span></span>  <br/> |
|[<span data-ttu-id="40506-147">AggregateOn</span><span class="sxs-lookup"><span data-stu-id="40506-147">AggregateOn</span></span>](aggregateon.md) <br/> |<span data-ttu-id="40506-148">Representa la propiedad que se utiliza para determinar el orden de elementos agrupados en un conjunto de resultados FindItem agrupado.</span><span class="sxs-lookup"><span data-stu-id="40506-148">Represents the property that is used to determine the order of grouped items for a grouped FindItem result set.</span></span>  <br/> |
|[<span data-ttu-id="40506-149">GroupBy</span><span class="sxs-lookup"><span data-stu-id="40506-149">GroupBy</span></span>](groupby.md) <br/> |<span data-ttu-id="40506-150">Especifica un agrupamiento arbitrario para consultas FindItem.</span><span class="sxs-lookup"><span data-stu-id="40506-150">Specifies an arbitrary grouping for FindItem queries.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="40506-151">Notas</span><span class="sxs-lookup"><span data-stu-id="40506-151">Remarks</span></span>

<span data-ttu-id="40506-152">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="40506-152">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="40506-153">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="40506-153">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="40506-154">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="40506-154">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="40506-155">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="40506-155">Schema Name</span></span>  <br/> |<span data-ttu-id="40506-156">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="40506-156">Types schema</span></span>  <br/> |
|<span data-ttu-id="40506-157">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="40506-157">Validation File</span></span>  <br/> |<span data-ttu-id="40506-158">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="40506-158">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="40506-159">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="40506-159">Can be Empty</span></span>  <br/> |<span data-ttu-id="40506-160">False</span><span class="sxs-lookup"><span data-stu-id="40506-160">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="40506-161">Ver también</span><span class="sxs-lookup"><span data-stu-id="40506-161">See also</span></span>



- [<span data-ttu-id="40506-162">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="40506-162">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

