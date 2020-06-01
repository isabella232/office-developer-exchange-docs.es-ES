---
title: SuggestionQuality
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SuggestionQuality
api_type:
- schema
ms.assetid: 734f1a58-adda-4830-973e-e84bf7b870d5
description: El elemento SuggestionQuality representa la calidad de la hora de reunión sugerida.
ms.openlocfilehash: 3f8c15ccabd03687dc386a0328020cbc0bc802c4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457980"
---
# <a name="suggestionquality"></a><span data-ttu-id="d482e-103">SuggestionQuality</span><span class="sxs-lookup"><span data-stu-id="d482e-103">SuggestionQuality</span></span>

<span data-ttu-id="d482e-104">El elemento **SuggestionQuality** representa la calidad de la hora de reunión sugerida.</span><span class="sxs-lookup"><span data-stu-id="d482e-104">The **SuggestionQuality** element represents the quality of the suggested meeting time.</span></span> 
  
[<span data-ttu-id="d482e-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="d482e-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="d482e-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="d482e-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="d482e-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="d482e-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
[<span data-ttu-id="d482e-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="d482e-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
[<span data-ttu-id="d482e-109">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="d482e-109">SuggestionArray</span></span>](suggestionarray.md)
  
[<span data-ttu-id="d482e-110">Alguna</span><span class="sxs-lookup"><span data-stu-id="d482e-110">Suggestion</span></span>](suggestion.md)
  
[<span data-ttu-id="d482e-111">SuggestionQuality</span><span class="sxs-lookup"><span data-stu-id="d482e-111">SuggestionQuality</span></span>](suggestionquality.md)
  
```xml
<SuggestionQuality>Excellent or Good or Fair or Poor</SuggestionQuality>
```

 <span data-ttu-id="d482e-112">**SuggestionQuality**</span><span class="sxs-lookup"><span data-stu-id="d482e-112">**SuggestionQuality**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d482e-113">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d482e-113">Attributes and elements</span></span>

<span data-ttu-id="d482e-114">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d482e-114">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d482e-115">Atributos</span><span class="sxs-lookup"><span data-stu-id="d482e-115">Attributes</span></span>

<span data-ttu-id="d482e-116">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="d482e-116">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d482e-117">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d482e-117">Child elements</span></span>

<span data-ttu-id="d482e-118">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="d482e-118">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d482e-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d482e-119">Parent elements</span></span>

|<span data-ttu-id="d482e-120">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="d482e-120">**Element**</span></span>|<span data-ttu-id="d482e-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d482e-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d482e-122">Alguna</span><span class="sxs-lookup"><span data-stu-id="d482e-122">Suggestion</span></span>](suggestion.md) <br/> |<span data-ttu-id="d482e-123">Representa una sugerencia de hora de reunión única.</span><span class="sxs-lookup"><span data-stu-id="d482e-123">Represents a single meeting time suggestion.</span></span>  <br/> <span data-ttu-id="d482e-124">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="d482e-124">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d482e-125">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="d482e-125">Text value</span></span>

<span data-ttu-id="d482e-126">Se requiere un valor de texto que represente un valor de **SuggestionQuality** .</span><span class="sxs-lookup"><span data-stu-id="d482e-126">A text value that represents a **SuggestionQuality** value is required.</span></span> <span data-ttu-id="d482e-127">Los valores posibles son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="d482e-127">The following are the possible values:</span></span> 
  
- <span data-ttu-id="d482e-128">Un **excelente** 100 por ciento de los usuarios y recursos están disponibles para la hora de reunión sugerida.</span><span class="sxs-lookup"><span data-stu-id="d482e-128">**Excellent** 100 percent of users and resources are available for the suggested meeting time.</span></span> 
    
- <span data-ttu-id="d482e-129">**Buenos** El porcentaje mínimo de usuarios y recursos disponible es igual o mayor que el valor del elemento [GoodThreshold](goodthreshold.md) más 50.</span><span class="sxs-lookup"><span data-stu-id="d482e-129">**Good** The minimum percentage of users and resources available is equal to or greater than the [GoodThreshold](goodthreshold.md) element value plus 50.</span></span> 
    
- <span data-ttu-id="d482e-130">**Fair** El porcentaje máximo de usuarios y recursos disponibles para una hora de reunión sugerida es igual al valor del elemento [GoodThreshold](goodthreshold.md) más 50.</span><span class="sxs-lookup"><span data-stu-id="d482e-130">**Fair** The maximum percentage of users and resources available for a suggested meeting time is equal to the [GoodThreshold](goodthreshold.md) element value plus 50.</span></span> <span data-ttu-id="d482e-131">El valor mínimo para una hora de reunión de calidad **razonable** es del 50 por ciento.</span><span class="sxs-lookup"><span data-stu-id="d482e-131">The minimum value for a **Fair** quality meeting time is 50 percent.</span></span> 
    
- <span data-ttu-id="d482e-132">**Mala** Menos del 50 por ciento de los usuarios y recursos están disponibles para la hora de reunión sugerida.</span><span class="sxs-lookup"><span data-stu-id="d482e-132">**Poor** Less than 50 percent of the users and resources are available for the suggested meeting time.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d482e-133">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d482e-133">Remarks</span></span>

<span data-ttu-id="d482e-134">El tipo **SuggestionQuality** también es el tipo de los elementos [DayQuality](dayquality.md) y [MinimumSuggestionQuality](minimumsuggestionquality.md) .</span><span class="sxs-lookup"><span data-stu-id="d482e-134">The **SuggestionQuality** type is also the type for the [DayQuality](dayquality.md) and the [MinimumSuggestionQuality](minimumsuggestionquality.md) elements.</span></span> 
  
<span data-ttu-id="d482e-135">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="d482e-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d482e-136">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d482e-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d482e-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="d482e-137">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d482e-138">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d482e-138">Schema Name</span></span>  <br/> |<span data-ttu-id="d482e-139">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="d482e-139">Types schema</span></span>  <br/> |
|<span data-ttu-id="d482e-140">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d482e-140">Validation File</span></span>  <br/> |<span data-ttu-id="d482e-141">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="d482e-141">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d482e-142">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d482e-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="d482e-143">Falso</span><span class="sxs-lookup"><span data-stu-id="d482e-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d482e-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="d482e-144">See also</span></span>



[<span data-ttu-id="d482e-145">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="d482e-145">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="d482e-146">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="d482e-146">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="d482e-147">Obtener disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="d482e-147">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

