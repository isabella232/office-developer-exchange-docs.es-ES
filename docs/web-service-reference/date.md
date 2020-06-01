---
title: Fecha
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Date
api_type:
- schema
ms.assetid: 2f6bc090-fff4-45b1-8d7e-8fd6e060cce2
description: El elemento Date representa la fecha que contiene las horas de reunión sugeridas.
ms.openlocfilehash: bcc152ed6aba94907189b5579b998815be45db16
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44443791"
---
# <a name="date"></a><span data-ttu-id="a4ea4-103">Fecha</span><span class="sxs-lookup"><span data-stu-id="a4ea4-103">Date</span></span>

<span data-ttu-id="a4ea4-104">El elemento **Date** representa la fecha que contiene las horas de reunión sugeridas.</span><span class="sxs-lookup"><span data-stu-id="a4ea4-104">The **Date** element represents the date that contains the suggested meeting times.</span></span> 
  
- [<span data-ttu-id="a4ea4-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="a4ea4-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md) 
- [<span data-ttu-id="a4ea4-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="a4ea4-106">SuggestionsResponse</span></span>](suggestionsresponse.md) 
- [<span data-ttu-id="a4ea4-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="a4ea4-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)  
- [<span data-ttu-id="a4ea4-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="a4ea4-108">SuggestionDayResult</span></span>](suggestiondayresult.md)  
- [<span data-ttu-id="a4ea4-109">Fecha</span><span class="sxs-lookup"><span data-stu-id="a4ea4-109">Date</span></span>](date.md)
  
```xml
<Date>...</Date>
```

<span data-ttu-id="a4ea4-110">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="a4ea4-110">**dateTime**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="a4ea4-111">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a4ea4-111">Attributes and elements</span></span>

<span data-ttu-id="a4ea4-112">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a4ea4-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a4ea4-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="a4ea4-113">Attributes</span></span>

<span data-ttu-id="a4ea4-114">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="a4ea4-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a4ea4-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a4ea4-115">Child elements</span></span>

<span data-ttu-id="a4ea4-116">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="a4ea4-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a4ea4-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a4ea4-117">Parent elements</span></span>

|<span data-ttu-id="a4ea4-118">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a4ea4-118">**Element**</span></span>|<span data-ttu-id="a4ea4-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a4ea4-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a4ea4-120">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="a4ea4-120">SuggestionDayResult</span></span>](suggestiondayresult.md) <br/> |<span data-ttu-id="a4ea4-121">Representa un solo día que contiene las horas de reunión sugeridas.</span><span class="sxs-lookup"><span data-stu-id="a4ea4-121">Represents a single day that contains suggested meeting times.</span></span>  <br/><br/><span data-ttu-id="a4ea4-122">La siguiente es la expresión XPath 2,0 a este elemento:</span><span class="sxs-lookup"><span data-stu-id="a4ea4-122">The following is the XPath 2.0 expression to this element:</span></span><br/><br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a4ea4-123">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="a4ea4-123">Text value</span></span>

<span data-ttu-id="a4ea4-124">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="a4ea4-124">A text value is required.</span></span> <span data-ttu-id="a4ea4-125">Revise las recomendaciones de tipos de texto del esquema del Consorcio World Wide Web (W3C) para el formato del tipo de texto primitivo dateTime.</span><span class="sxs-lookup"><span data-stu-id="a4ea4-125">Review the World Wide Web Consortium (W3C) schema datatype recommendations for the format of the dateTime primitive datatype.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a4ea4-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a4ea4-126">Remarks</span></span>

<span data-ttu-id="a4ea4-127">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="a4ea4-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a4ea4-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a4ea4-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a4ea4-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="a4ea4-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a4ea4-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a4ea4-130">Schema Name</span></span>  <br/> |<span data-ttu-id="a4ea4-131">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="a4ea4-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="a4ea4-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a4ea4-132">Validation File</span></span>  <br/> |<span data-ttu-id="a4ea4-133">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="a4ea4-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a4ea4-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a4ea4-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="a4ea4-135">Falso</span><span class="sxs-lookup"><span data-stu-id="a4ea4-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a4ea4-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="a4ea4-136">See also</span></span>

- [<span data-ttu-id="a4ea4-137">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="a4ea4-137">GetUserAvailability operation</span></span>](getuseravailability-operation.md) 
- [<span data-ttu-id="a4ea4-138">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="a4ea4-138">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
- [<span data-ttu-id="a4ea4-139">Obtener disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="a4ea4-139">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

