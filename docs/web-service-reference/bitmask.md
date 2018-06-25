---
title: Máscara de bits
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Bitmask
api_type:
- schema
ms.assetid: fc7eeac2-555f-4cbc-8b48-26d9ed67748a
description: El elemento de máscara de bits representa una máscara de hexadecimal o decimal que se utilizará durante una operación de restricción excluye.
ms.openlocfilehash: 86c8c61f22d8d620a9139280b2a43ed7fec4727d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763633"
---
# <a name="bitmask"></a><span data-ttu-id="95714-103">Máscara de bits</span><span class="sxs-lookup"><span data-stu-id="95714-103">Bitmask</span></span>

<span data-ttu-id="95714-104">El elemento de **máscara de bits** representa una máscara de hexadecimal o decimal que se utilizará durante una operación de restricción [excluye](excludes.md) .</span><span class="sxs-lookup"><span data-stu-id="95714-104">The **Bitmask** element represents a hexadecimal or decimal mask to be used during an [Excludes](excludes.md) restriction operation.</span></span> 
  
```xml
<Bitmask Value="" />
```

<span data-ttu-id="95714-105">**ExcludesValueType**</span><span class="sxs-lookup"><span data-stu-id="95714-105">**ExcludesValueType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="95714-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="95714-106">Attributes and elements</span></span>

<span data-ttu-id="95714-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="95714-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="95714-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="95714-108">Attributes</span></span>

|<span data-ttu-id="95714-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="95714-109">**Attribute**</span></span>|<span data-ttu-id="95714-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="95714-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="95714-111">**Value**</span><span class="sxs-lookup"><span data-stu-id="95714-111">**Value**</span></span> | <span data-ttu-id="95714-112">Representa una máscara de bits hexadecimal o decimal.</span><span class="sxs-lookup"><span data-stu-id="95714-112">Represents a decimal or hexadecimal bitmask.</span></span> <span data-ttu-id="95714-113">El valor se representa mediante la siguiente expresión regular:</span><span class="sxs-lookup"><span data-stu-id="95714-113">The value is represented by the following regular expression:</span></span><br/><span data-ttu-id="95714-114">' ((0 x</span><span class="sxs-lookup"><span data-stu-id="95714-114">\`((0x</span></span>|<span data-ttu-id="95714-115">0x)[0-9a-fA-f]\*)</span><span class="sxs-lookup"><span data-stu-id="95714-115">0X)[0-9A-Fa-f]\*)</span></span>|<span data-ttu-id="95714-116">([0-9] \*)'.</span><span class="sxs-lookup"><span data-stu-id="95714-116">([0-9]\*)\`.</span></span><br/><br/><span data-ttu-id="95714-117">Los siguientes son ejemplos de valores hexadecimales para este atributo:</span><span class="sxs-lookup"><span data-stu-id="95714-117">The following are examples of hexadecimal values for this attribute:</span></span><br/><span data-ttu-id="95714-118">-0x12AF</span><span class="sxs-lookup"><span data-stu-id="95714-118">- 0x12AF</span></span><br/><span data-ttu-id="95714-119">-0X334AE</span><span class="sxs-lookup"><span data-stu-id="95714-119">- 0X334AE</span></span><br/><br/><span data-ttu-id="95714-120">Los siguientes son ejemplos de valores decimales para este atributo:</span><span class="sxs-lookup"><span data-stu-id="95714-120">The following are examples of decimal values for this attribute:</span></span><br/><span data-ttu-id="95714-121">-10</span><span class="sxs-lookup"><span data-stu-id="95714-121">- 10</span></span><br/><span data-ttu-id="95714-122">-255</span><span class="sxs-lookup"><span data-stu-id="95714-122">- 255</span></span><br/><span data-ttu-id="95714-123">-4562</span><span class="sxs-lookup"><span data-stu-id="95714-123">- 4562</span></span> |
   
### <a name="child-elements"></a><span data-ttu-id="95714-124">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="95714-124">Child elements</span></span>

<span data-ttu-id="95714-125">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="95714-125">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="95714-126">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="95714-126">Parent elements</span></span>

|<span data-ttu-id="95714-127">**Element**</span><span class="sxs-lookup"><span data-stu-id="95714-127">**Element**</span></span>|<span data-ttu-id="95714-128">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="95714-128">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="95714-129">Excluye</span><span class="sxs-lookup"><span data-stu-id="95714-129">Excludes</span></span>](excludes.md) <br/> |<span data-ttu-id="95714-130">Realiza una máscara de bit a bit de las propiedades.</span><span class="sxs-lookup"><span data-stu-id="95714-130">Performs a bitwise mask of the properties.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="95714-131">Comentarios</span><span class="sxs-lookup"><span data-stu-id="95714-131">Remarks</span></span>

<span data-ttu-id="95714-132">Valores hexadecimales deben tener un prefijo de 0 x o 0 X.</span><span class="sxs-lookup"><span data-stu-id="95714-132">Hexadecimal values must have a prefix of either 0x or 0X.</span></span> <span data-ttu-id="95714-133">Si este prefijo no existe, el valor se supone que para ser un número decimal.</span><span class="sxs-lookup"><span data-stu-id="95714-133">If this prefix does not exist, the value is assumed to be a decimal number.</span></span>
  
<span data-ttu-id="95714-134">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="95714-134">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="95714-135">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="95714-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="95714-136">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="95714-136">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="95714-137">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="95714-137">Schema name</span></span>  <br/> |<span data-ttu-id="95714-138">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="95714-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="95714-139">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="95714-139">Validation file</span></span>  <br/> |<span data-ttu-id="95714-140">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="95714-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="95714-141">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="95714-141">Can be empty</span></span>  <br/> |<span data-ttu-id="95714-142">False</span><span class="sxs-lookup"><span data-stu-id="95714-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="95714-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="95714-143">See also</span></span>

- [<span data-ttu-id="95714-144">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="95714-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

