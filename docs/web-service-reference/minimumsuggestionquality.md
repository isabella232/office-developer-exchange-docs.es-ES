---
title: MinimumSuggestionQuality
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MinimumSuggestionQuality
api_type:
- schema
ms.assetid: 3725cbd4-9bc1-4f7d-8929-b2c68cb46114
description: El elemento MinimumSuggestionQuality define la calidad de sugerencias de reunión que se devuelve en la respuesta.
ms.openlocfilehash: ac79682bd761f678f23fc2d698a50fd7704f6fab
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836468"
---
# <a name="minimumsuggestionquality"></a><span data-ttu-id="0dbaa-103">MinimumSuggestionQuality</span><span class="sxs-lookup"><span data-stu-id="0dbaa-103">MinimumSuggestionQuality</span></span>

<span data-ttu-id="0dbaa-104">El elemento **MinimumSuggestionQuality** define la calidad de sugerencias de reunión que se devuelve en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0dbaa-104">The **MinimumSuggestionQuality** element defines the quality of meeting suggestions to be returned in the response.</span></span> 
  
[<span data-ttu-id="0dbaa-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="0dbaa-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
[<span data-ttu-id="0dbaa-106">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="0dbaa-106">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md)
  
[<span data-ttu-id="0dbaa-107">MinimumSuggestionQuality</span><span class="sxs-lookup"><span data-stu-id="0dbaa-107">MinimumSuggestionQuality</span></span>](minimumsuggestionquality.md)
  
```xml
<MinimumSuggestionQuality>...</MinimumSuggestionQuality>
```

 <span data-ttu-id="0dbaa-108">**SuggestionQuality**</span><span class="sxs-lookup"><span data-stu-id="0dbaa-108">**SuggestionQuality**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0dbaa-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="0dbaa-109">Attributes and elements</span></span>

<span data-ttu-id="0dbaa-110">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="0dbaa-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0dbaa-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="0dbaa-111">Attributes</span></span>

<span data-ttu-id="0dbaa-112">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0dbaa-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0dbaa-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0dbaa-113">Child elements</span></span>

<span data-ttu-id="0dbaa-114">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0dbaa-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0dbaa-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0dbaa-115">Parent elements</span></span>

|<span data-ttu-id="0dbaa-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="0dbaa-116">**Element**</span></span>|<span data-ttu-id="0dbaa-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0dbaa-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0dbaa-118">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="0dbaa-118">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md) <br/> |<span data-ttu-id="0dbaa-119">Contiene las opciones para obtener información de la sugerencia de reunión.</span><span class="sxs-lookup"><span data-stu-id="0dbaa-119">Contains the options for obtaining meeting suggestion information.</span></span>  <br/> <span data-ttu-id="0dbaa-120">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="0dbaa-120">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/SuggestionViewOptions` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0dbaa-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="0dbaa-121">Text value</span></span>

<span data-ttu-id="0dbaa-122">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="0dbaa-122">A text value is required.</span></span> <span data-ttu-id="0dbaa-123">En la siguiente tabla se enumera los valores posibles para este elemento:</span><span class="sxs-lookup"><span data-stu-id="0dbaa-123">The following table lists the possible values for this element:</span></span>
  
|<span data-ttu-id="0dbaa-124">**Valor**</span><span class="sxs-lookup"><span data-stu-id="0dbaa-124">**Value**</span></span>|<span data-ttu-id="0dbaa-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0dbaa-125">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0dbaa-126">**Excelente**</span><span class="sxs-lookup"><span data-stu-id="0dbaa-126">**Excellent**</span></span> <br/> |<span data-ttu-id="0dbaa-127">0% de los asistentes tienen un conflicto con la hora de la reunión sugerida.</span><span class="sxs-lookup"><span data-stu-id="0dbaa-127">0% of the attendees have a conflict with the suggested meeting time.</span></span>  <br/> |
|<span data-ttu-id="0dbaa-128">**Buena**</span><span class="sxs-lookup"><span data-stu-id="0dbaa-128">**Good**</span></span> <br/> |<span data-ttu-id="0dbaa-129">El porcentaje que se considera una buena se establece mediante el elemento [GoodThreshold](goodthreshold.md) .</span><span class="sxs-lookup"><span data-stu-id="0dbaa-129">The percentage that is considered good is set by using the [GoodThreshold](goodthreshold.md) element.</span></span>  <br/> |
|<span data-ttu-id="0dbaa-130">**Razonable**</span><span class="sxs-lookup"><span data-stu-id="0dbaa-130">**Fair**</span></span> <br/> |<span data-ttu-id="0dbaa-131">El porcentaje que se considera razonable se establece mediante el elemento [GoodThreshold](goodthreshold.md) .</span><span class="sxs-lookup"><span data-stu-id="0dbaa-131">The percentage that is considered fair is set by using the [GoodThreshold](goodthreshold.md) element.</span></span>  <br/> |
|<span data-ttu-id="0dbaa-132">**Deficiente**</span><span class="sxs-lookup"><span data-stu-id="0dbaa-132">**Poor**</span></span> <br/> |<span data-ttu-id="0dbaa-133">50% o más de los asistentes tienen un conflicto con la hora de la reunión sugerida.</span><span class="sxs-lookup"><span data-stu-id="0dbaa-133">50% or more of the attendees have a conflict with the suggested meeting time.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0dbaa-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0dbaa-134">Remarks</span></span>

<span data-ttu-id="0dbaa-135">Este elemento es necesario si se usa el elemento [SuggestionsViewOptions](suggestionsviewoptions.md) .</span><span class="sxs-lookup"><span data-stu-id="0dbaa-135">This element is required if the [SuggestionsViewOptions](suggestionsviewoptions.md) element is used.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="0dbaa-136">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="0dbaa-136">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="0dbaa-137">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0dbaa-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0dbaa-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0dbaa-138">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0dbaa-139">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="0dbaa-139">Schema Name</span></span>  <br/> |<span data-ttu-id="0dbaa-140">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="0dbaa-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="0dbaa-141">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="0dbaa-141">Validation File</span></span>  <br/> |<span data-ttu-id="0dbaa-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0dbaa-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0dbaa-143">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="0dbaa-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="0dbaa-144">False</span><span class="sxs-lookup"><span data-stu-id="0dbaa-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0dbaa-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="0dbaa-145">See also</span></span>



[<span data-ttu-id="0dbaa-146">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="0dbaa-146">GetUserAvailability operation</span></span>](getuseravailability-operation.md)


[<span data-ttu-id="0dbaa-147">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="0dbaa-147">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

