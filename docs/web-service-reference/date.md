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
description: El elemento de fecha representa la fecha que contiene las horas de reunión sugerida.
ms.openlocfilehash: 98dc9d6c599222c819b2c9ed1bacd05758ae1655
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764027"
---
# <a name="date"></a><span data-ttu-id="1f0b5-103">Fecha</span><span class="sxs-lookup"><span data-stu-id="1f0b5-103">Date</span></span>

<span data-ttu-id="1f0b5-104">El elemento de **fecha** representa la fecha que contiene las horas de reunión sugerida.</span><span class="sxs-lookup"><span data-stu-id="1f0b5-104">The **Date** element represents the date that contains the suggested meeting times.</span></span> 
  
- [<span data-ttu-id="1f0b5-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="1f0b5-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md) 
- [<span data-ttu-id="1f0b5-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="1f0b5-106">SuggestionsResponse</span></span>](suggestionsresponse.md) 
- [<span data-ttu-id="1f0b5-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="1f0b5-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)  
- [<span data-ttu-id="1f0b5-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="1f0b5-108">SuggestionDayResult</span></span>](suggestiondayresult.md)  
- [<span data-ttu-id="1f0b5-109">Date</span><span class="sxs-lookup"><span data-stu-id="1f0b5-109">Date</span></span>](date.md)
  
```xml
<Date>...</Date>
```

<span data-ttu-id="1f0b5-110">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="1f0b5-110">**dateTime**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="1f0b5-111">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="1f0b5-111">Attributes and elements</span></span>

<span data-ttu-id="1f0b5-112">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="1f0b5-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1f0b5-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="1f0b5-113">Attributes</span></span>

<span data-ttu-id="1f0b5-114">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1f0b5-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1f0b5-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1f0b5-115">Child elements</span></span>

<span data-ttu-id="1f0b5-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1f0b5-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1f0b5-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="1f0b5-117">Parent elements</span></span>

|<span data-ttu-id="1f0b5-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="1f0b5-118">**Element**</span></span>|<span data-ttu-id="1f0b5-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1f0b5-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1f0b5-120">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="1f0b5-120">SuggestionDayResult</span></span>](suggestiondayresult.md) <br/> |<span data-ttu-id="1f0b5-121">Representa un solo día que contiene las horas de reunión sugerida.</span><span class="sxs-lookup"><span data-stu-id="1f0b5-121">Represents a single day that contains suggested meeting times.</span></span>  <br/><br/><span data-ttu-id="1f0b5-122">La siguiente es la expresión de XPath 2.0 para este elemento:</span><span class="sxs-lookup"><span data-stu-id="1f0b5-122">The following is the XPath 2.0 expression to this element:</span></span><br/><br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1f0b5-123">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="1f0b5-123">Text value</span></span>

<span data-ttu-id="1f0b5-124">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="1f0b5-124">A text value is required.</span></span> <span data-ttu-id="1f0b5-125">Revise las recomendaciones de tipo de datos de esquema de World Wide Web Consortium (W3C) para el formato del tipo de datos dateTime primitivo.</span><span class="sxs-lookup"><span data-stu-id="1f0b5-125">Review the World Wide Web Consortium (W3C) schema datatype recommendations for the format of the dateTime primitive datatype.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1f0b5-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1f0b5-126">Remarks</span></span>

<span data-ttu-id="1f0b5-127">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="1f0b5-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1f0b5-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="1f0b5-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1f0b5-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1f0b5-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1f0b5-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="1f0b5-130">Schema Name</span></span>  <br/> |<span data-ttu-id="1f0b5-131">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="1f0b5-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="1f0b5-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="1f0b5-132">Validation File</span></span>  <br/> |<span data-ttu-id="1f0b5-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1f0b5-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1f0b5-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="1f0b5-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="1f0b5-135">False</span><span class="sxs-lookup"><span data-stu-id="1f0b5-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1f0b5-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="1f0b5-136">See also</span></span>

- [<span data-ttu-id="1f0b5-137">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="1f0b5-137">GetUserAvailability operation</span></span>](getuseravailability-operation.md) 
- [<span data-ttu-id="1f0b5-138">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="1f0b5-138">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
- [<span data-ttu-id="1f0b5-139">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="1f0b5-139">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

