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
description: El elemento Constant identifica un valor constante en una restricción.
ms.openlocfilehash: 6cb2eaa4227a8fd0985e8ff5a15d647c3bb1cd6a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461558"
---
# <a name="constant"></a><span data-ttu-id="ce244-103">Constante</span><span class="sxs-lookup"><span data-stu-id="ce244-103">Constant</span></span>

<span data-ttu-id="ce244-104">El elemento **Constant** identifica un valor constante en una restricción.</span><span class="sxs-lookup"><span data-stu-id="ce244-104">The **Constant** element identifies a constant value in a restriction.</span></span> 
  
```xml
<Constant Value="" />
```

 <span data-ttu-id="ce244-105">**ConstantValueType**</span><span class="sxs-lookup"><span data-stu-id="ce244-105">**ConstantValueType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ce244-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ce244-106">Attributes and elements</span></span>

<span data-ttu-id="ce244-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ce244-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ce244-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="ce244-108">Attributes</span></span>

|<span data-ttu-id="ce244-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="ce244-109">**Attribute**</span></span>|<span data-ttu-id="ce244-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ce244-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ce244-111">**Valor**</span><span class="sxs-lookup"><span data-stu-id="ce244-111">**Value**</span></span> <br/> |<span data-ttu-id="ce244-112">Especifica el valor que se va a comparar en la restricción.</span><span class="sxs-lookup"><span data-stu-id="ce244-112">Specifies the value to compare in the restriction.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ce244-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ce244-113">Child elements</span></span>

<span data-ttu-id="ce244-114">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="ce244-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ce244-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ce244-115">Parent elements</span></span>

|<span data-ttu-id="ce244-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ce244-116">**Element**</span></span>|<span data-ttu-id="ce244-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ce244-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ce244-118">Contains</span><span class="sxs-lookup"><span data-stu-id="ce244-118">Contains</span></span>](contains.md) <br/> |<span data-ttu-id="ce244-119">Representa una expresión de búsqueda que determina si una propiedad determinada contiene el valor de cadena constante proporcionado.</span><span class="sxs-lookup"><span data-stu-id="ce244-119">Represents a search expression that determines whether a given property contains the supplied constant string value.</span></span>  <br/> |
|[<span data-ttu-id="ce244-120">FieldURIOrConstant</span><span class="sxs-lookup"><span data-stu-id="ce244-120">FieldURIOrConstant</span></span>](fielduriorconstant.md) <br/> |<span data-ttu-id="ce244-121">Representa una propiedad o un valor constante que se utilizará al comparar con otra propiedad.</span><span class="sxs-lookup"><span data-stu-id="ce244-121">Represents either a property or a constant value to be used when comparing with another property.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ce244-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ce244-122">Remarks</span></span>

<span data-ttu-id="ce244-123">El valor de cadena en el atributo **Value** debe ser convertible en el tipo con el que está intentando comparar.</span><span class="sxs-lookup"><span data-stu-id="ce244-123">The string value in the **Value** attribute must be coercible into the type you are trying to compare against.</span></span> <span data-ttu-id="ce244-124">Por ejemplo, si se compara una propiedad de fecha y hora con un valor constante, el valor de cadena debe representar una fecha y hora.</span><span class="sxs-lookup"><span data-stu-id="ce244-124">For example, if you are comparing a date/time property against a constant value, the string value must represent a date/time.</span></span> 
  
<span data-ttu-id="ce244-125">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="ce244-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ce244-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ce244-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ce244-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="ce244-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ce244-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ce244-128">Schema Name</span></span>  <br/> |<span data-ttu-id="ce244-129">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="ce244-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="ce244-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ce244-130">Validation File</span></span>  <br/> |<span data-ttu-id="ce244-131">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="ce244-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ce244-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ce244-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="ce244-133">Falso</span><span class="sxs-lookup"><span data-stu-id="ce244-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ce244-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="ce244-134">See also</span></span>



- [<span data-ttu-id="ce244-135">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="ce244-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

