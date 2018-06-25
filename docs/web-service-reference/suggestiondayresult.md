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
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840599"
---
# <a name="suggestiondayresult"></a><span data-ttu-id="76f12-103">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="76f12-103">SuggestionDayResult</span></span>

<span data-ttu-id="76f12-104">El elemento **SuggestionDayResult** representa un solo día que contiene las horas de reunión sugerida.</span><span class="sxs-lookup"><span data-stu-id="76f12-104">The **SuggestionDayResult** element represents a single day that contains suggested meeting times.</span></span> 
  
[<span data-ttu-id="76f12-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="76f12-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="76f12-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="76f12-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="76f12-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="76f12-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
[<span data-ttu-id="76f12-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="76f12-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
```xml
<SuggestionDayResult>
   <Date>...</Date>
   <DayQuality>...</DayQuality>
   <SuggestionArray>...</SuggestionArray>
</SuggestionDayResult>
```

 <span data-ttu-id="76f12-109">**SuggestionDayResult**</span><span class="sxs-lookup"><span data-stu-id="76f12-109">**SuggestionDayResult**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="76f12-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="76f12-110">Attributes and elements</span></span>

<span data-ttu-id="76f12-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="76f12-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="76f12-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="76f12-112">Attributes</span></span>

<span data-ttu-id="76f12-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="76f12-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="76f12-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="76f12-114">Child elements</span></span>

|<span data-ttu-id="76f12-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="76f12-115">**Element**</span></span>|<span data-ttu-id="76f12-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="76f12-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="76f12-117">Date</span><span class="sxs-lookup"><span data-stu-id="76f12-117">Date</span></span>](date.md) <br/> |<span data-ttu-id="76f12-118">Representa la fecha que contiene las horas de reunión sugerida.</span><span class="sxs-lookup"><span data-stu-id="76f12-118">Represents the date that contains the suggested meeting times.</span></span>  <br/> |
|[<span data-ttu-id="76f12-119">DayQuality</span><span class="sxs-lookup"><span data-stu-id="76f12-119">DayQuality</span></span>](dayquality.md) <br/> |<span data-ttu-id="76f12-120">Representa la calidad del día para que contiene las horas de reunión sugerida de calidad.</span><span class="sxs-lookup"><span data-stu-id="76f12-120">Represents the quality of the day for containing quality suggested meeting times.</span></span>  <br/> |
|[<span data-ttu-id="76f12-121">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="76f12-121">SuggestionArray</span></span>](suggestionarray.md) <br/> |<span data-ttu-id="76f12-122">Contiene una matriz de sugerencias de reunión.</span><span class="sxs-lookup"><span data-stu-id="76f12-122">Contains an array of meeting suggestions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="76f12-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="76f12-123">Parent elements</span></span>

|<span data-ttu-id="76f12-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="76f12-124">**Element**</span></span>|<span data-ttu-id="76f12-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="76f12-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="76f12-126">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="76f12-126">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md) <br/> |<span data-ttu-id="76f12-127">Contiene una matriz de sugerencias organizadas por fecha de reunión.</span><span class="sxs-lookup"><span data-stu-id="76f12-127">Contains an array of meeting suggestions organized by date.</span></span>  <br/> <span data-ttu-id="76f12-128">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="76f12-128">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="76f12-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="76f12-129">Remarks</span></span>

<span data-ttu-id="76f12-130">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="76f12-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="76f12-131">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="76f12-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="76f12-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="76f12-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="76f12-133">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="76f12-133">Schema Name</span></span>  <br/> |<span data-ttu-id="76f12-134">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="76f12-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="76f12-135">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="76f12-135">Validation File</span></span>  <br/> |<span data-ttu-id="76f12-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="76f12-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="76f12-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="76f12-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="76f12-138">False</span><span class="sxs-lookup"><span data-stu-id="76f12-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="76f12-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="76f12-139">See also</span></span>



[<span data-ttu-id="76f12-140">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="76f12-140">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="76f12-141">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="76f12-141">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="76f12-142">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="76f12-142">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

