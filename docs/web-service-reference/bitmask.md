---
title: Máscara
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
description: El elemento de máscara de subred representa una máscara hexadecimal o decimal que se utilizará durante una operación de restricción de exclusión.
ms.openlocfilehash: f05be466d05b13f8f362afb5fc0552653a532475
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458813"
---
# <a name="bitmask"></a><span data-ttu-id="541c1-103">Máscara</span><span class="sxs-lookup"><span data-stu-id="541c1-103">Bitmask</span></span>

<span data-ttu-id="541c1-104">El elemento de **máscara** de subred representa una máscara hexadecimal o decimal que se utilizará durante una operación de restricción de [exclusión](excludes.md) .</span><span class="sxs-lookup"><span data-stu-id="541c1-104">The **Bitmask** element represents a hexadecimal or decimal mask to be used during an [Excludes](excludes.md) restriction operation.</span></span> 
  
```xml
<Bitmask Value="" />
```

<span data-ttu-id="541c1-105">**ExcludesValueType**</span><span class="sxs-lookup"><span data-stu-id="541c1-105">**ExcludesValueType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="541c1-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="541c1-106">Attributes and elements</span></span>

<span data-ttu-id="541c1-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="541c1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="541c1-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="541c1-108">Attributes</span></span>

|<span data-ttu-id="541c1-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="541c1-109">**Attribute**</span></span>|<span data-ttu-id="541c1-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="541c1-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="541c1-111">**Valor**</span><span class="sxs-lookup"><span data-stu-id="541c1-111">**Value**</span></span> | <span data-ttu-id="541c1-112">Representa una máscara de máscara decimal o hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="541c1-112">Represents a decimal or hexadecimal bitmask.</span></span> <span data-ttu-id="541c1-113">El valor se representa mediante la siguiente expresión regular:</span><span class="sxs-lookup"><span data-stu-id="541c1-113">The value is represented by the following regular expression:</span></span><br/><span data-ttu-id="541c1-114">`((0x|0X)[0-9A-Fa-f]*)|([0-9]*)`.</span><span class="sxs-lookup"><span data-stu-id="541c1-114">`((0x|0X)[0-9A-Fa-f]*)|([0-9]*)`.</span></span><br/><br/><span data-ttu-id="541c1-115">Los siguientes son ejemplos de valores hexadecimales para este atributo:</span><span class="sxs-lookup"><span data-stu-id="541c1-115">The following are examples of hexadecimal values for this attribute:</span></span><br/><span data-ttu-id="541c1-116">- 0x12AF</span><span class="sxs-lookup"><span data-stu-id="541c1-116">- 0x12AF</span></span><br/><span data-ttu-id="541c1-117">- 0X334AE</span><span class="sxs-lookup"><span data-stu-id="541c1-117">- 0X334AE</span></span><br/><br/><span data-ttu-id="541c1-118">Los siguientes son ejemplos de valores decimales para este atributo:</span><span class="sxs-lookup"><span data-stu-id="541c1-118">The following are examples of decimal values for this attribute:</span></span><br/><span data-ttu-id="541c1-119">-10</span><span class="sxs-lookup"><span data-stu-id="541c1-119">- 10</span></span><br/><span data-ttu-id="541c1-120">-255</span><span class="sxs-lookup"><span data-stu-id="541c1-120">- 255</span></span><br/><span data-ttu-id="541c1-121">-4562</span><span class="sxs-lookup"><span data-stu-id="541c1-121">- 4562</span></span> |
   
### <a name="child-elements"></a><span data-ttu-id="541c1-122">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="541c1-122">Child elements</span></span>

<span data-ttu-id="541c1-123">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="541c1-123">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="541c1-124">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="541c1-124">Parent elements</span></span>

|<span data-ttu-id="541c1-125">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="541c1-125">**Element**</span></span>|<span data-ttu-id="541c1-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="541c1-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="541c1-127">Excluye</span><span class="sxs-lookup"><span data-stu-id="541c1-127">Excludes</span></span>](excludes.md) <br/> |<span data-ttu-id="541c1-128">Realiza una máscara bit a bit de las propiedades.</span><span class="sxs-lookup"><span data-stu-id="541c1-128">Performs a bitwise mask of the properties.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="541c1-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="541c1-129">Remarks</span></span>

<span data-ttu-id="541c1-130">Los valores hexadecimales deben tener un prefijo de 0x o 0X.</span><span class="sxs-lookup"><span data-stu-id="541c1-130">Hexadecimal values must have a prefix of either 0x or 0X.</span></span> <span data-ttu-id="541c1-131">Si este prefijo no existe, se supone que el valor es un número decimal.</span><span class="sxs-lookup"><span data-stu-id="541c1-131">If this prefix does not exist, the value is assumed to be a decimal number.</span></span>
  
<span data-ttu-id="541c1-132">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="541c1-132">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="541c1-133">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="541c1-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="541c1-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="541c1-134">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="541c1-135">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="541c1-135">Schema name</span></span>  <br/> |<span data-ttu-id="541c1-136">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="541c1-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="541c1-137">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="541c1-137">Validation file</span></span>  <br/> |<span data-ttu-id="541c1-138">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="541c1-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="541c1-139">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="541c1-139">Can be empty</span></span>  <br/> |<span data-ttu-id="541c1-140">Falso</span><span class="sxs-lookup"><span data-stu-id="541c1-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="541c1-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="541c1-141">See also</span></span>

- [<span data-ttu-id="541c1-142">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="541c1-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

