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
description: El elemento Value contiene el valor de una propiedad extendida.
ms.openlocfilehash: 5de1528dda6d58ea772d050e709c0720e389fae6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465215"
---
# <a name="value"></a><span data-ttu-id="1ae75-103">Valor</span><span class="sxs-lookup"><span data-stu-id="1ae75-103">Value</span></span>

<span data-ttu-id="1ae75-104">El elemento **Value** contiene el valor de una propiedad extendida.</span><span class="sxs-lookup"><span data-stu-id="1ae75-104">The **Value** element contains the value of an extended property.</span></span> 
  
```xml
<Value/>
```

<span data-ttu-id="1ae75-105">**String**</span><span class="sxs-lookup"><span data-stu-id="1ae75-105">**String**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="1ae75-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="1ae75-106">Attributes and elements</span></span>

<span data-ttu-id="1ae75-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="1ae75-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1ae75-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="1ae75-108">Attributes</span></span>

<span data-ttu-id="1ae75-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1ae75-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1ae75-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1ae75-110">Child elements</span></span>

<span data-ttu-id="1ae75-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1ae75-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1ae75-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="1ae75-112">Parent elements</span></span>

|<span data-ttu-id="1ae75-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="1ae75-113">**Element**</span></span>|<span data-ttu-id="1ae75-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1ae75-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1ae75-115">Valores</span><span class="sxs-lookup"><span data-stu-id="1ae75-115">Values</span></span>](values.md) <br/> |<span data-ttu-id="1ae75-116">Contiene una colección de valores para una propiedad extendida.</span><span class="sxs-lookup"><span data-stu-id="1ae75-116">Contains a collection of values for an extended property.</span></span>  <br/> |
|[<span data-ttu-id="1ae75-117">Las extendedproperty</span><span class="sxs-lookup"><span data-stu-id="1ae75-117">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="1ae75-118">Identifica las propiedades extendidas de las carpetas y los elementos.</span><span class="sxs-lookup"><span data-stu-id="1ae75-118">Identifies extended properties on folders and items.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1ae75-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="1ae75-119">Text value</span></span>

<span data-ttu-id="1ae75-120">El valor de texto debe ser compatible con el tipo que indica el atributo PropertyType de ExtendedFieldURI.</span><span class="sxs-lookup"><span data-stu-id="1ae75-120">The text value must be compatible with the type that is indicated by the PropertyType attribute of the ExtendedFieldURI.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1ae75-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1ae75-121">Remarks</span></span>

<span data-ttu-id="1ae75-122">Un elemento **Value** puede producirse en instancias de propiedades extendidas simples y con varios valores.</span><span class="sxs-lookup"><span data-stu-id="1ae75-122">A **Value** element can occur in both single and multivalued extended property instances.</span></span> <span data-ttu-id="1ae75-123">Para instancias de valor único, existe como un elemento secundario directo del elemento [las extendedproperty](extendedproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="1ae75-123">For single-valued instances, it exists as a direct child of the [ExtendedProperty](extendedproperty.md) element.</span></span> <span data-ttu-id="1ae75-124">Para una instancia multivalor, existe como elemento secundario directo de la colección de **valores** .</span><span class="sxs-lookup"><span data-stu-id="1ae75-124">For multivalued instance, it exists as a direct child of the **Values** collection.</span></span> 
  
<span data-ttu-id="1ae75-125">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="1ae75-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1ae75-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="1ae75-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1ae75-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="1ae75-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1ae75-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="1ae75-128">Schema Name</span></span>  <br/> |<span data-ttu-id="1ae75-129">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="1ae75-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="1ae75-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="1ae75-130">Validation File</span></span>  <br/> |<span data-ttu-id="1ae75-131">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="1ae75-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1ae75-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="1ae75-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="1ae75-133">Falso</span><span class="sxs-lookup"><span data-stu-id="1ae75-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1ae75-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="1ae75-134">See also</span></span>

- [<span data-ttu-id="1ae75-135">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="1ae75-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

