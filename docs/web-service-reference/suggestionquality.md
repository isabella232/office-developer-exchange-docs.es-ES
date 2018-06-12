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
description: El elemento SuggestionQuality representa la calidad de la hora de la reunión sugerida.
ms.openlocfilehash: e67e0149226b36c22cdd00acd78f6582f826dd3e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840600"
---
# <a name="suggestionquality"></a><span data-ttu-id="e05bc-103">SuggestionQuality</span><span class="sxs-lookup"><span data-stu-id="e05bc-103">SuggestionQuality</span></span>

<span data-ttu-id="e05bc-104">El elemento **SuggestionQuality** representa la calidad de la hora de la reunión sugerida.</span><span class="sxs-lookup"><span data-stu-id="e05bc-104">The **SuggestionQuality** element represents the quality of the suggested meeting time.</span></span> 
  
[<span data-ttu-id="e05bc-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="e05bc-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="e05bc-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="e05bc-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="e05bc-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="e05bc-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
[<span data-ttu-id="e05bc-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="e05bc-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
[<span data-ttu-id="e05bc-109">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="e05bc-109">SuggestionArray</span></span>](suggestionarray.md)
  
[<span data-ttu-id="e05bc-110">Sugerencia</span><span class="sxs-lookup"><span data-stu-id="e05bc-110">Suggestion</span></span>](suggestion.md)
  
[<span data-ttu-id="e05bc-111">SuggestionQuality</span><span class="sxs-lookup"><span data-stu-id="e05bc-111">SuggestionQuality</span></span>](suggestionquality.md)
  
```xml
<SuggestionQuality>Excellent or Good or Fair or Poor</SuggestionQuality>
```

 <span data-ttu-id="e05bc-112">**SuggestionQuality**</span><span class="sxs-lookup"><span data-stu-id="e05bc-112">**SuggestionQuality**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e05bc-113">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e05bc-113">Attributes and elements</span></span>

<span data-ttu-id="e05bc-114">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e05bc-114">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e05bc-115">Atributos</span><span class="sxs-lookup"><span data-stu-id="e05bc-115">Attributes</span></span>

<span data-ttu-id="e05bc-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e05bc-116">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e05bc-117">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e05bc-117">Child elements</span></span>

<span data-ttu-id="e05bc-118">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e05bc-118">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e05bc-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e05bc-119">Parent elements</span></span>

|<span data-ttu-id="e05bc-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="e05bc-120">**Element**</span></span>|<span data-ttu-id="e05bc-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e05bc-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e05bc-122">Sugerencia</span><span class="sxs-lookup"><span data-stu-id="e05bc-122">Suggestion</span></span>](suggestion.md) <br/> |<span data-ttu-id="e05bc-123">Representa una sola sugerencia de tiempo de la reunión.</span><span class="sxs-lookup"><span data-stu-id="e05bc-123">Represents a single meeting time suggestion.</span></span>  <br/> <span data-ttu-id="e05bc-124">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="e05bc-124">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e05bc-125">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="e05bc-125">Text value</span></span>

<span data-ttu-id="e05bc-126">Se requiere un valor de texto que representa un valor de **SuggestionQuality** .</span><span class="sxs-lookup"><span data-stu-id="e05bc-126">A text value that represents a **SuggestionQuality** value is required.</span></span> <span data-ttu-id="e05bc-127">Los valores posibles son:</span><span class="sxs-lookup"><span data-stu-id="e05bc-127">The following are the possible values:</span></span> 
  
- <span data-ttu-id="e05bc-128">**Excelente** 100 por ciento de los usuarios y los recursos están disponibles para el tiempo de la reunión sugerida.</span><span class="sxs-lookup"><span data-stu-id="e05bc-128">**Excellent** 100 percent of users and resources are available for the suggested meeting time.</span></span> 
    
- <span data-ttu-id="e05bc-129">**Buena** El porcentaje mínimo de usuarios y recursos disponibles es igual o mayor que el valor del elemento [GoodThreshold](goodthreshold.md) más de 50.</span><span class="sxs-lookup"><span data-stu-id="e05bc-129">**Good** The minimum percentage of users and resources available is equal to or greater than the [GoodThreshold](goodthreshold.md) element value plus 50.</span></span> 
    
- <span data-ttu-id="e05bc-130">**Razonable** El porcentaje máximo de usuarios y recursos disponibles para una hora de reunión sugerida es igual que el valor del elemento [GoodThreshold](goodthreshold.md) más de 50.</span><span class="sxs-lookup"><span data-stu-id="e05bc-130">**Fair** The maximum percentage of users and resources available for a suggested meeting time is equal to the [GoodThreshold](goodthreshold.md) element value plus 50.</span></span> <span data-ttu-id="e05bc-131">El valor mínimo de una hora de reunión calidad **razonable** es 50 por ciento.</span><span class="sxs-lookup"><span data-stu-id="e05bc-131">The minimum value for a **Fair** quality meeting time is 50 percent.</span></span> 
    
- <span data-ttu-id="e05bc-132">**Deficiente** Menor que el 50 por ciento de los usuarios y los recursos están disponible para el tiempo de la reunión sugerida.</span><span class="sxs-lookup"><span data-stu-id="e05bc-132">**Poor** Less than 50 percent of the users and resources are available for the suggested meeting time.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e05bc-133">Notas</span><span class="sxs-lookup"><span data-stu-id="e05bc-133">Remarks</span></span>

<span data-ttu-id="e05bc-134">El tipo de **SuggestionQuality** también es el tipo para el [DayQuality](dayquality.md) y los elementos de [MinimumSuggestionQuality](minimumsuggestionquality.md) .</span><span class="sxs-lookup"><span data-stu-id="e05bc-134">The **SuggestionQuality** type is also the type for the [DayQuality](dayquality.md) and the [MinimumSuggestionQuality](minimumsuggestionquality.md) elements.</span></span> 
  
<span data-ttu-id="e05bc-135">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="e05bc-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e05bc-136">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e05bc-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e05bc-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e05bc-137">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e05bc-138">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e05bc-138">Schema Name</span></span>  <br/> |<span data-ttu-id="e05bc-139">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="e05bc-139">Types schema</span></span>  <br/> |
|<span data-ttu-id="e05bc-140">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e05bc-140">Validation File</span></span>  <br/> |<span data-ttu-id="e05bc-141">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e05bc-141">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e05bc-142">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e05bc-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="e05bc-143">False</span><span class="sxs-lookup"><span data-stu-id="e05bc-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e05bc-144">Ver también</span><span class="sxs-lookup"><span data-stu-id="e05bc-144">See also</span></span>



[<span data-ttu-id="e05bc-145">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="e05bc-145">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="e05bc-146">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="e05bc-146">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="e05bc-147">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="e05bc-147">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

