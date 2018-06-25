---
title: GoodThreshold
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GoodThreshold
api_type:
- schema
ms.assetid: 68f607f5-7271-46a6-8ffc-91878185a683
description: El elemento GoodThreshold especifica el porcentaje de los asistentes que debe tener el período de tiempo para el período de tiempo calificar como una hora de reunión sugerida buena abrir.
ms.openlocfilehash: 8044cb2b52cb572fad8731253dffa34de9d097fa
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835746"
---
# <a name="goodthreshold"></a><span data-ttu-id="a14a1-103">GoodThreshold</span><span class="sxs-lookup"><span data-stu-id="a14a1-103">GoodThreshold</span></span>

<span data-ttu-id="a14a1-104">El elemento **GoodThreshold** especifica el porcentaje de los asistentes que debe tener el período de tiempo para el período de tiempo calificar como una hora de reunión sugerida buena abrir.</span><span class="sxs-lookup"><span data-stu-id="a14a1-104">The **GoodThreshold** element specifies the percentage of attendees that must have the time period open in order for the time period to qualify as a Good suggested meeting time.</span></span> 
  
[<span data-ttu-id="a14a1-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="a14a1-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
[<span data-ttu-id="a14a1-106">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="a14a1-106">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md)
  
[<span data-ttu-id="a14a1-107">GoodThreshold</span><span class="sxs-lookup"><span data-stu-id="a14a1-107">GoodThreshold</span></span>](goodthreshold.md)
  
```xml
<GoodThreshold>...</GoodThreshold>
```

 <span data-ttu-id="a14a1-108">**int**</span><span class="sxs-lookup"><span data-stu-id="a14a1-108">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a14a1-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a14a1-109">Attributes and elements</span></span>

<span data-ttu-id="a14a1-110">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a14a1-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a14a1-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="a14a1-111">Attributes</span></span>

<span data-ttu-id="a14a1-112">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a14a1-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a14a1-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a14a1-113">Child elements</span></span>

<span data-ttu-id="a14a1-114">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a14a1-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a14a1-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a14a1-115">Parent elements</span></span>

|<span data-ttu-id="a14a1-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="a14a1-116">**Element**</span></span>|<span data-ttu-id="a14a1-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a14a1-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a14a1-118">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="a14a1-118">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md) <br/> |<span data-ttu-id="a14a1-119">Contiene las opciones para obtener información de la sugerencia de reunión.</span><span class="sxs-lookup"><span data-stu-id="a14a1-119">Contains the options for obtaining meeting suggestion information.</span></span>  <br/> <span data-ttu-id="a14a1-120">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="a14a1-120">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/SuggestionViewOptions` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a14a1-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="a14a1-121">Text value</span></span>

<span data-ttu-id="a14a1-122">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="a14a1-122">A text value is required.</span></span> <span data-ttu-id="a14a1-123">Los valores enteros esperado están entre 0 y 50.</span><span class="sxs-lookup"><span data-stu-id="a14a1-123">The expected integer values are between 0 and 50.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a14a1-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a14a1-124">Remarks</span></span>

<span data-ttu-id="a14a1-125">Este elemento es necesario si se usa el elemento [SuggestionsViewOptions](suggestionsviewoptions.md) .</span><span class="sxs-lookup"><span data-stu-id="a14a1-125">This element is required if the [SuggestionsViewOptions](suggestionsviewoptions.md) element is used.</span></span> <span data-ttu-id="a14a1-126">El elemento **GoodThreshold** también determina qué reuniones se consideran justo.</span><span class="sxs-lookup"><span data-stu-id="a14a1-126">The **GoodThreshold** element also determines what meetings are considered Fair.</span></span> <span data-ttu-id="a14a1-127">Es que el porcentaje de los asistentes con conflictos es que menor que el umbral de buena y superiores al 50 por ciento, el tiempo de la reunión sugerida certifica como justo.</span><span class="sxs-lookup"><span data-stu-id="a14a1-127">It the percentage of attendees with conflicts is less than the Good Threshold and higher than 50 percent, the suggested meeting time qualifies as Fair.</span></span> <span data-ttu-id="a14a1-128">El umbral de buena más de 50 es igual al porcentaje que define el umbral bueno/justo.</span><span class="sxs-lookup"><span data-stu-id="a14a1-128">The Good Threshold plus 50 equals the percentage that defines the Good/Fair threshold.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a14a1-129">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="a14a1-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="a14a1-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a14a1-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a14a1-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a14a1-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a14a1-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a14a1-132">Schema Name</span></span>  <br/> |<span data-ttu-id="a14a1-133">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="a14a1-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="a14a1-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a14a1-134">Validation File</span></span>  <br/> |<span data-ttu-id="a14a1-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a14a1-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a14a1-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a14a1-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="a14a1-137">False</span><span class="sxs-lookup"><span data-stu-id="a14a1-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a14a1-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="a14a1-138">See also</span></span>



[<span data-ttu-id="a14a1-139">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="a14a1-139">GetUserAvailability operation</span></span>](getuseravailability-operation.md)


[<span data-ttu-id="a14a1-140">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="a14a1-140">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

