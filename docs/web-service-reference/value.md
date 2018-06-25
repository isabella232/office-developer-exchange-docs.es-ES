---
title: Valor
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
ms.assetid: 9a30cadd-909e-41b1-b4e9-291643dd89c6
description: El elemento de valor contiene el valor de una propiedad extendida.
ms.openlocfilehash: 4b8674d267b78f0384f9457e794e88ace8234826
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840960"
---
# <a name="value"></a><span data-ttu-id="e1253-103">Value</span><span class="sxs-lookup"><span data-stu-id="e1253-103">Value</span></span>

<span data-ttu-id="e1253-104">El elemento de **valor** contiene el valor de una propiedad extendida.</span><span class="sxs-lookup"><span data-stu-id="e1253-104">The **Value** element contains the value of an extended property.</span></span> 
  
```xml
<Value/>
```

<span data-ttu-id="e1253-105">**String**</span><span class="sxs-lookup"><span data-stu-id="e1253-105">**String**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="e1253-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e1253-106">Attributes and elements</span></span>

<span data-ttu-id="e1253-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e1253-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e1253-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="e1253-108">Attributes</span></span>

<span data-ttu-id="e1253-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e1253-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e1253-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e1253-110">Child elements</span></span>

<span data-ttu-id="e1253-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e1253-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e1253-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e1253-112">Parent elements</span></span>

|<span data-ttu-id="e1253-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="e1253-113">**Element**</span></span>|<span data-ttu-id="e1253-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e1253-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e1253-115">Values</span><span class="sxs-lookup"><span data-stu-id="e1253-115">Values</span></span>](values.md) <br/> |<span data-ttu-id="e1253-116">Contiene una colección de valores para una propiedad extendida.</span><span class="sxs-lookup"><span data-stu-id="e1253-116">Contains a collection of values for an extended property.</span></span>  <br/> |
|[<span data-ttu-id="e1253-117">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="e1253-117">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="e1253-118">Identifica las propiedades extendidas en carpetas y elementos.</span><span class="sxs-lookup"><span data-stu-id="e1253-118">Identifies extended properties on folders and items.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e1253-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="e1253-119">Text value</span></span>

<span data-ttu-id="e1253-120">El valor de texto debe ser compatible con el tipo que se indica mediante el atributo PropertyType de la ExtendedFieldURI.</span><span class="sxs-lookup"><span data-stu-id="e1253-120">The text value must be compatible with the type that is indicated by the PropertyType attribute of the ExtendedFieldURI.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e1253-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e1253-121">Remarks</span></span>

<span data-ttu-id="e1253-122">Un elemento de **valor** puede producirse en ambas instancias de la propiedad extendida único y de varios valores.</span><span class="sxs-lookup"><span data-stu-id="e1253-122">A **Value** element can occur in both single and multivalued extended property instances.</span></span> <span data-ttu-id="e1253-123">Para las instancias de un solo valor, existe como un elemento secundario directo del elemento [ExtendedProperty](extendedproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="e1253-123">For single-valued instances, it exists as a direct child of the [ExtendedProperty](extendedproperty.md) element.</span></span> <span data-ttu-id="e1253-124">Para la instancia multivalor, existe como un elemento secundario directo de la colección de **valores** .</span><span class="sxs-lookup"><span data-stu-id="e1253-124">For multivalued instance, it exists as a direct child of the **Values** collection.</span></span> 
  
<span data-ttu-id="e1253-125">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="e1253-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e1253-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e1253-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e1253-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e1253-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e1253-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e1253-128">Schema Name</span></span>  <br/> |<span data-ttu-id="e1253-129">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="e1253-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="e1253-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e1253-130">Validation File</span></span>  <br/> |<span data-ttu-id="e1253-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e1253-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e1253-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e1253-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="e1253-133">False</span><span class="sxs-lookup"><span data-stu-id="e1253-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e1253-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="e1253-134">See also</span></span>

- [<span data-ttu-id="e1253-135">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="e1253-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

