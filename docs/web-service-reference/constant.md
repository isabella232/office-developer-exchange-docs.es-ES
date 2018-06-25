---
title: Constante
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Constant
api_type:
- schema
ms.assetid: 340af0cd-9f12-44ab-b8f1-21d107c8d0c9
description: El elemento constante identifica un valor constante en una restricción.
ms.openlocfilehash: 73912bc1981c5d54040f7c4a563ad805916fe721
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763779"
---
# <a name="constant"></a><span data-ttu-id="4e60a-103">Constante</span><span class="sxs-lookup"><span data-stu-id="4e60a-103">Constant</span></span>

<span data-ttu-id="4e60a-104">El elemento **constante** identifica un valor constante en una restricción.</span><span class="sxs-lookup"><span data-stu-id="4e60a-104">The **Constant** element identifies a constant value in a restriction.</span></span> 
  
```xml
<Constant Value="" />
```

 <span data-ttu-id="4e60a-105">**ConstantValueType**</span><span class="sxs-lookup"><span data-stu-id="4e60a-105">**ConstantValueType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4e60a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="4e60a-106">Attributes and elements</span></span>

<span data-ttu-id="4e60a-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="4e60a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4e60a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="4e60a-108">Attributes</span></span>

|<span data-ttu-id="4e60a-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="4e60a-109">**Attribute**</span></span>|<span data-ttu-id="4e60a-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4e60a-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4e60a-111">**Value**</span><span class="sxs-lookup"><span data-stu-id="4e60a-111">**Value**</span></span> <br/> |<span data-ttu-id="4e60a-112">Especifica el valor de comparación de la restricción.</span><span class="sxs-lookup"><span data-stu-id="4e60a-112">Specifies the value to compare in the restriction.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4e60a-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4e60a-113">Child elements</span></span>

<span data-ttu-id="4e60a-114">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4e60a-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4e60a-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="4e60a-115">Parent elements</span></span>

|<span data-ttu-id="4e60a-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="4e60a-116">**Element**</span></span>|<span data-ttu-id="4e60a-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4e60a-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4e60a-118">Incluye</span><span class="sxs-lookup"><span data-stu-id="4e60a-118">Contains</span></span>](contains.md) <br/> |<span data-ttu-id="4e60a-119">Representa una expresión de búsqueda que determina si una propiedad determinada contiene el valor de cadena constante proporcionada.</span><span class="sxs-lookup"><span data-stu-id="4e60a-119">Represents a search expression that determines whether a given property contains the supplied constant string value.</span></span>  <br/> |
|[<span data-ttu-id="4e60a-120">FieldURIOrConstant</span><span class="sxs-lookup"><span data-stu-id="4e60a-120">FieldURIOrConstant</span></span>](fielduriorconstant.md) <br/> |<span data-ttu-id="4e60a-121">Representa una propiedad o un valor constante que se usará cuando se comparan con otra propiedad.</span><span class="sxs-lookup"><span data-stu-id="4e60a-121">Represents either a property or a constant value to be used when comparing with another property.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4e60a-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4e60a-122">Remarks</span></span>

<span data-ttu-id="4e60a-123">El valor de cadena en el atributo de **valor** debe ser convertible en el tipo que intenta comparar.</span><span class="sxs-lookup"><span data-stu-id="4e60a-123">The string value in the **Value** attribute must be coercible into the type you are trying to compare against.</span></span> <span data-ttu-id="4e60a-124">Por ejemplo, si se está comparando una propiedad de fecha y hora con respecto a un valor constante, el valor de cadena debe representar un fecha y hora.</span><span class="sxs-lookup"><span data-stu-id="4e60a-124">For example, if you are comparing a date/time property against a constant value, the string value must represent a date/time.</span></span> 
  
<span data-ttu-id="4e60a-125">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="4e60a-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4e60a-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="4e60a-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4e60a-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4e60a-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4e60a-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="4e60a-128">Schema Name</span></span>  <br/> |<span data-ttu-id="4e60a-129">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="4e60a-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="4e60a-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="4e60a-130">Validation File</span></span>  <br/> |<span data-ttu-id="4e60a-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4e60a-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4e60a-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="4e60a-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="4e60a-133">False</span><span class="sxs-lookup"><span data-stu-id="4e60a-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4e60a-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="4e60a-134">See also</span></span>



- [<span data-ttu-id="4e60a-135">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="4e60a-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

