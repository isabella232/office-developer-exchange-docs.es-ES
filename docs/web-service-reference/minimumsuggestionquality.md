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
description: El elemento MinimumSuggestionQuality define la calidad de las sugerencias de reunión que se devolverán en la respuesta.
ms.openlocfilehash: c85cbf65a63ac0b09408c14e01889f97a05b27b0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467483"
---
# <a name="minimumsuggestionquality"></a><span data-ttu-id="c6558-103">MinimumSuggestionQuality</span><span class="sxs-lookup"><span data-stu-id="c6558-103">MinimumSuggestionQuality</span></span>

<span data-ttu-id="c6558-104">El elemento **MinimumSuggestionQuality** define la calidad de las sugerencias de reunión que se devolverán en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c6558-104">The **MinimumSuggestionQuality** element defines the quality of meeting suggestions to be returned in the response.</span></span> 
  
[<span data-ttu-id="c6558-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="c6558-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
[<span data-ttu-id="c6558-106">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="c6558-106">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md)
  
[<span data-ttu-id="c6558-107">MinimumSuggestionQuality</span><span class="sxs-lookup"><span data-stu-id="c6558-107">MinimumSuggestionQuality</span></span>](minimumsuggestionquality.md)
  
```xml
<MinimumSuggestionQuality>...</MinimumSuggestionQuality>
```

 <span data-ttu-id="c6558-108">**SuggestionQuality**</span><span class="sxs-lookup"><span data-stu-id="c6558-108">**SuggestionQuality**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c6558-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c6558-109">Attributes and elements</span></span>

<span data-ttu-id="c6558-110">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c6558-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c6558-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="c6558-111">Attributes</span></span>

<span data-ttu-id="c6558-112">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c6558-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c6558-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c6558-113">Child elements</span></span>

<span data-ttu-id="c6558-114">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c6558-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c6558-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c6558-115">Parent elements</span></span>

|<span data-ttu-id="c6558-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c6558-116">**Element**</span></span>|<span data-ttu-id="c6558-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c6558-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c6558-118">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="c6558-118">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md) <br/> |<span data-ttu-id="c6558-119">Contiene las opciones para obtener información sobre las sugerencias de la reunión.</span><span class="sxs-lookup"><span data-stu-id="c6558-119">Contains the options for obtaining meeting suggestion information.</span></span>  <br/> <span data-ttu-id="c6558-120">A continuación se encuentra la expresión XPath de este elemento:</span><span class="sxs-lookup"><span data-stu-id="c6558-120">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/SuggestionViewOptions` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c6558-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="c6558-121">Text value</span></span>

<span data-ttu-id="c6558-122">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="c6558-122">A text value is required.</span></span> <span data-ttu-id="c6558-123">En la siguiente tabla se enumeran los valores posibles para este elemento:</span><span class="sxs-lookup"><span data-stu-id="c6558-123">The following table lists the possible values for this element:</span></span>
  
|<span data-ttu-id="c6558-124">**Valor**</span><span class="sxs-lookup"><span data-stu-id="c6558-124">**Value**</span></span>|<span data-ttu-id="c6558-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c6558-125">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c6558-126">**Excelente**</span><span class="sxs-lookup"><span data-stu-id="c6558-126">**Excellent**</span></span> <br/> |<span data-ttu-id="c6558-127">el 0% de los asistentes tiene un conflicto con la hora de reunión sugerida.</span><span class="sxs-lookup"><span data-stu-id="c6558-127">0% of the attendees have a conflict with the suggested meeting time.</span></span>  <br/> |
|<span data-ttu-id="c6558-128">**Good**</span><span class="sxs-lookup"><span data-stu-id="c6558-128">**Good**</span></span> <br/> |<span data-ttu-id="c6558-129">El porcentaje que se considera correcto se establece mediante el elemento [GoodThreshold](goodthreshold.md) .</span><span class="sxs-lookup"><span data-stu-id="c6558-129">The percentage that is considered good is set by using the [GoodThreshold](goodthreshold.md) element.</span></span>  <br/> |
|<span data-ttu-id="c6558-130">**Imparcial**</span><span class="sxs-lookup"><span data-stu-id="c6558-130">**Fair**</span></span> <br/> |<span data-ttu-id="c6558-131">El porcentaje que se considera justo se establece mediante el elemento [GoodThreshold](goodthreshold.md) .</span><span class="sxs-lookup"><span data-stu-id="c6558-131">The percentage that is considered fair is set by using the [GoodThreshold](goodthreshold.md) element.</span></span>  <br/> |
|<span data-ttu-id="c6558-132">**Deficiente**</span><span class="sxs-lookup"><span data-stu-id="c6558-132">**Poor**</span></span> <br/> |<span data-ttu-id="c6558-133">el 50% o más de los asistentes tienen un conflicto con la hora de reunión sugerida.</span><span class="sxs-lookup"><span data-stu-id="c6558-133">50% or more of the attendees have a conflict with the suggested meeting time.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c6558-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c6558-134">Remarks</span></span>

<span data-ttu-id="c6558-135">Este elemento es obligatorio si se usa el elemento [SuggestionsViewOptions](suggestionsviewoptions.md) .</span><span class="sxs-lookup"><span data-stu-id="c6558-135">This element is required if the [SuggestionsViewOptions](suggestionsviewoptions.md) element is used.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c6558-136">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="c6558-136">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="c6558-137">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c6558-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c6558-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="c6558-138">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c6558-139">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c6558-139">Schema Name</span></span>  <br/> |<span data-ttu-id="c6558-140">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="c6558-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="c6558-141">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c6558-141">Validation File</span></span>  <br/> |<span data-ttu-id="c6558-142">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="c6558-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c6558-143">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c6558-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="c6558-144">Falso</span><span class="sxs-lookup"><span data-stu-id="c6558-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c6558-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="c6558-145">See also</span></span>



[<span data-ttu-id="c6558-146">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="c6558-146">GetUserAvailability operation</span></span>](getuseravailability-operation.md)


[<span data-ttu-id="c6558-147">Obtener disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="c6558-147">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

