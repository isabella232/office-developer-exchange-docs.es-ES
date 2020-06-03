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
ms.openlocfilehash: f794d9970590417d916925f7258b28d4f0920d0e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467021"
---
# <a name="indexedfielduri"></a><span data-ttu-id="9e492-103">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="9e492-103">IndexedFieldURI</span></span>

<span data-ttu-id="9e492-104">El elemento **IndexedFieldURI** identifica a los miembros individuales de un diccionario.</span><span class="sxs-lookup"><span data-stu-id="9e492-104">The **IndexedFieldURI** element identifies individual members of a dictionary.</span></span> 
  
```xml
<IndexedFieldURI FieldURI="" FieldIndex="" />
```

 <span data-ttu-id="9e492-105">**PathToIndexedFieldType**</span><span class="sxs-lookup"><span data-stu-id="9e492-105">**PathToIndexedFieldType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9e492-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="9e492-106">Attributes and elements</span></span>

<span data-ttu-id="9e492-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="9e492-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9e492-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="9e492-108">Attributes</span></span>

|<span data-ttu-id="9e492-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="9e492-109">**Attribute**</span></span>|<span data-ttu-id="9e492-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9e492-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9e492-111">**FieldURI**</span><span class="sxs-lookup"><span data-stu-id="9e492-111">**FieldURI**</span></span> <br/> |<span data-ttu-id="9e492-112">Identifica el diccionario que contiene el miembro que se va a devolver.</span><span class="sxs-lookup"><span data-stu-id="9e492-112">Identifies the dictionary that contains the member to return.</span></span> <span data-ttu-id="9e492-113">Este atributo es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9e492-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="9e492-114">**FieldIndex**</span><span class="sxs-lookup"><span data-stu-id="9e492-114">**FieldIndex**</span></span> <br/> |<span data-ttu-id="9e492-115">Identifica al miembro del diccionario que se debe devolver.</span><span class="sxs-lookup"><span data-stu-id="9e492-115">Identifies the member of the dictionary to return.</span></span> <span data-ttu-id="9e492-116">Este atributo es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9e492-116">This attribute is required.</span></span>  <br/> |
   
#### <a name="fielduri-attribute"></a><span data-ttu-id="9e492-117">Atributo FieldURI</span><span class="sxs-lookup"><span data-stu-id="9e492-117">FieldURI Attribute</span></span>

|<span data-ttu-id="9e492-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="9e492-118">**Value**</span></span>|<span data-ttu-id="9e492-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9e492-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9e492-120">elemento: InternetMessageHeader</span><span class="sxs-lookup"><span data-stu-id="9e492-120">item:InternetMessageHeader</span></span>  <br/> |<span data-ttu-id="9e492-121">Representa el encabezado del mensaje de un elemento.</span><span class="sxs-lookup"><span data-stu-id="9e492-121">Represents the message header of an item.</span></span>  <br/> |
|<span data-ttu-id="9e492-122">contactos: direcciones</span><span class="sxs-lookup"><span data-stu-id="9e492-122">contacts:ImAddress</span></span>  <br/> |<span data-ttu-id="9e492-123">Representa la dirección de mensajería instantánea de un contacto.</span><span class="sxs-lookup"><span data-stu-id="9e492-123">Represents the instant messaging address of a contact.</span></span>  <br/> |
|<span data-ttu-id="9e492-124">contactos: PhysicalAddress: calle</span><span class="sxs-lookup"><span data-stu-id="9e492-124">contacts:PhysicalAddress:Street</span></span>  <br/> |<span data-ttu-id="9e492-125">Representa la dirección postal de un contacto.</span><span class="sxs-lookup"><span data-stu-id="9e492-125">Represents the street address of a contact.</span></span>  <br/> |
|<span data-ttu-id="9e492-126">contactos: PhysicalAddress: ciudad</span><span class="sxs-lookup"><span data-stu-id="9e492-126">contacts:PhysicalAddress:City</span></span>  <br/> |<span data-ttu-id="9e492-127">Representa la ciudad de un contacto.</span><span class="sxs-lookup"><span data-stu-id="9e492-127">Represents the city of a contact.</span></span>  <br/> |
|<span data-ttu-id="9e492-128">contactos: PhysicalAddress: estado</span><span class="sxs-lookup"><span data-stu-id="9e492-128">contacts:PhysicalAddress:State</span></span>  <br/> |<span data-ttu-id="9e492-129">Representa el estado de un contacto.</span><span class="sxs-lookup"><span data-stu-id="9e492-129">Represents the state of a contact.</span></span>  <br/> |
|<span data-ttu-id="9e492-130">contactos: PhysicalAddress: país</span><span class="sxs-lookup"><span data-stu-id="9e492-130">contacts:PhysicalAddress:Country</span></span>  <br/> |<span data-ttu-id="9e492-131">Representa el país o la región de un contacto.</span><span class="sxs-lookup"><span data-stu-id="9e492-131">Represents the country/region of a contact.</span></span>  <br/> |
|<span data-ttu-id="9e492-132">contactos: PhysicalAddress: CódigoPostal</span><span class="sxs-lookup"><span data-stu-id="9e492-132">contacts:PhysicalAddress:PostalCode</span></span>  <br/> |<span data-ttu-id="9e492-133">Representa el código postal de un contacto.</span><span class="sxs-lookup"><span data-stu-id="9e492-133">Represents the postal code of a contact.</span></span>  <br/> |
|<span data-ttu-id="9e492-134">contactos: PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="9e492-134">contacts:PhoneNumber</span></span>  <br/> |<span data-ttu-id="9e492-135">Representa el número de teléfono de un contacto.</span><span class="sxs-lookup"><span data-stu-id="9e492-135">Represents the phone number of a contact.</span></span>  <br/> |
|<span data-ttu-id="9e492-136">contactos: EmailAddress</span><span class="sxs-lookup"><span data-stu-id="9e492-136">contacts:EmailAddress</span></span>  <br/> |<span data-ttu-id="9e492-137">Representa la dirección de correo electrónico de un contacto.</span><span class="sxs-lookup"><span data-stu-id="9e492-137">Represents the e-mail address of a contact.</span></span>  <br/> |
|<span data-ttu-id="9e492-138">DistributionList: miembros: miembro</span><span class="sxs-lookup"><span data-stu-id="9e492-138">distributionlist:Members:Member</span></span>  <br/> |<span data-ttu-id="9e492-139">Representa un miembro de una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="9e492-139">Represents a member of a distribution list.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9e492-140">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9e492-140">Child elements</span></span>

<span data-ttu-id="9e492-141">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="9e492-141">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9e492-142">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="9e492-142">Parent elements</span></span>

|<span data-ttu-id="9e492-143">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9e492-143">**Element**</span></span>|<span data-ttu-id="9e492-144">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9e492-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9e492-145">AdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="9e492-145">AdditionalProperties</span></span>](additionalproperties.md) <br/> |<span data-ttu-id="9e492-146">Identifica las propiedades adicionales que se van a obtener, establecer o crear.</span><span class="sxs-lookup"><span data-stu-id="9e492-146">Identifies additional properties to get, set, or create.</span></span>  <br/> |
|[<span data-ttu-id="9e492-147">AggregateOn</span><span class="sxs-lookup"><span data-stu-id="9e492-147">AggregateOn</span></span>](aggregateon.md) <br/> |<span data-ttu-id="9e492-148">Representa la propiedad que se usa para determinar el orden de los elementos agrupados para un conjunto de resultados FindItem agrupados.</span><span class="sxs-lookup"><span data-stu-id="9e492-148">Represents the property that is used to determine the order of grouped items for a grouped FindItem result set.</span></span>  <br/> |
|[<span data-ttu-id="9e492-149">GroupBy</span><span class="sxs-lookup"><span data-stu-id="9e492-149">GroupBy</span></span>](groupby.md) <br/> |<span data-ttu-id="9e492-150">Especifica una agrupación arbitraria para consultas FindItem.</span><span class="sxs-lookup"><span data-stu-id="9e492-150">Specifies an arbitrary grouping for FindItem queries.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9e492-151">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9e492-151">Remarks</span></span>

<span data-ttu-id="9e492-152">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="9e492-152">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9e492-153">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="9e492-153">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9e492-154">Namespace</span><span class="sxs-lookup"><span data-stu-id="9e492-154">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9e492-155">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="9e492-155">Schema Name</span></span>  <br/> |<span data-ttu-id="9e492-156">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="9e492-156">Types schema</span></span>  <br/> |
|<span data-ttu-id="9e492-157">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="9e492-157">Validation File</span></span>  <br/> |<span data-ttu-id="9e492-158">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="9e492-158">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9e492-159">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="9e492-159">Can be Empty</span></span>  <br/> |<span data-ttu-id="9e492-160">Falso</span><span class="sxs-lookup"><span data-stu-id="9e492-160">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9e492-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="9e492-161">See also</span></span>



- [<span data-ttu-id="9e492-162">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="9e492-162">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

