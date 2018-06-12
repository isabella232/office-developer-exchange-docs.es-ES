---
title: SuggestionDayResult
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SuggestionDayResult
api_type:
- schema
ms.assetid: 916b1cbb-f2e3-471d-84b0-e33467616652
description: El elemento SuggestionDayResult representa un solo día que contiene las horas de reunión sugerida.
ms.openlocfilehash: 7b75258a9e70f1ec6feed6a0b18beb76f356c7f4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840599"
---
# <a name="suggestiondayresult"></a><span data-ttu-id="68a66-103">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="68a66-103">SuggestionDayResult</span></span>

<span data-ttu-id="68a66-104">El elemento **SuggestionDayResult** representa un solo día que contiene las horas de reunión sugerida.</span><span class="sxs-lookup"><span data-stu-id="68a66-104">The **SuggestionDayResult** element represents a single day that contains suggested meeting times.</span></span> 
  
[<span data-ttu-id="68a66-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="68a66-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="68a66-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="68a66-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="68a66-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="68a66-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
[<span data-ttu-id="68a66-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="68a66-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
```xml
<SuggestionDayResult>
   <Date>...</Date>
   <DayQuality>...</DayQuality>
   <SuggestionArray>...</SuggestionArray>
</SuggestionDayResult>
```

 <span data-ttu-id="68a66-109">**SuggestionDayResult**</span><span class="sxs-lookup"><span data-stu-id="68a66-109">**SuggestionDayResult**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="68a66-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="68a66-110">Attributes and elements</span></span>

<span data-ttu-id="68a66-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="68a66-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="68a66-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="68a66-112">Attributes</span></span>

<span data-ttu-id="68a66-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="68a66-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="68a66-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="68a66-114">Child elements</span></span>

|<span data-ttu-id="68a66-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="68a66-115">**Element**</span></span>|<span data-ttu-id="68a66-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="68a66-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="68a66-117">Date</span><span class="sxs-lookup"><span data-stu-id="68a66-117">Date</span></span>](date.md) <br/> |<span data-ttu-id="68a66-118">Representa la fecha que contiene las horas de reunión sugerida.</span><span class="sxs-lookup"><span data-stu-id="68a66-118">Represents the date that contains the suggested meeting times.</span></span>  <br/> |
|[<span data-ttu-id="68a66-119">DayQuality</span><span class="sxs-lookup"><span data-stu-id="68a66-119">DayQuality</span></span>](dayquality.md) <br/> |<span data-ttu-id="68a66-120">Representa la calidad del día para que contiene las horas de reunión sugerida de calidad.</span><span class="sxs-lookup"><span data-stu-id="68a66-120">Represents the quality of the day for containing quality suggested meeting times.</span></span>  <br/> |
|[<span data-ttu-id="68a66-121">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="68a66-121">SuggestionArray</span></span>](suggestionarray.md) <br/> |<span data-ttu-id="68a66-122">Contiene una matriz de sugerencias de reunión.</span><span class="sxs-lookup"><span data-stu-id="68a66-122">Contains an array of meeting suggestions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="68a66-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="68a66-123">Parent elements</span></span>

|<span data-ttu-id="68a66-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="68a66-124">**Element**</span></span>|<span data-ttu-id="68a66-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="68a66-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="68a66-126">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="68a66-126">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md) <br/> |<span data-ttu-id="68a66-127">Contiene una matriz de sugerencias organizadas por fecha de reunión.</span><span class="sxs-lookup"><span data-stu-id="68a66-127">Contains an array of meeting suggestions organized by date.</span></span>  <br/> <span data-ttu-id="68a66-128">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="68a66-128">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="68a66-129">Notas</span><span class="sxs-lookup"><span data-stu-id="68a66-129">Remarks</span></span>

<span data-ttu-id="68a66-130">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="68a66-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="68a66-131">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="68a66-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="68a66-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="68a66-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="68a66-133">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="68a66-133">Schema Name</span></span>  <br/> |<span data-ttu-id="68a66-134">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="68a66-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="68a66-135">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="68a66-135">Validation File</span></span>  <br/> |<span data-ttu-id="68a66-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="68a66-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="68a66-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="68a66-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="68a66-138">False</span><span class="sxs-lookup"><span data-stu-id="68a66-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="68a66-139">Ver también</span><span class="sxs-lookup"><span data-stu-id="68a66-139">See also</span></span>



[<span data-ttu-id="68a66-140">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="68a66-140">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="68a66-141">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="68a66-141">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="68a66-142">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="68a66-142">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

