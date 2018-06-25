---
title: SuggestionsViewOptions
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SuggestionsViewOptions
api_type:
- schema
ms.assetid: bb04ae38-e62d-4a69-a479-8ff326ca726e
description: El elemento SuggestionsViewOptions contiene las opciones para obtener información de la sugerencia de reunión.
ms.openlocfilehash: 09ff317ae0b2ebf1eadc89dc3bb1cf5b3ae19dcb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840603"
---
# <a name="suggestionsviewoptions"></a><span data-ttu-id="d5e20-103">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="d5e20-103">SuggestionsViewOptions</span></span>

<span data-ttu-id="d5e20-104">El elemento **SuggestionsViewOptions** contiene las opciones para obtener información de la sugerencia de reunión.</span><span class="sxs-lookup"><span data-stu-id="d5e20-104">The **SuggestionsViewOptions** element contains the options for obtaining meeting suggestion information.</span></span> 
  
[<span data-ttu-id="d5e20-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="d5e20-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
[<span data-ttu-id="d5e20-106">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="d5e20-106">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md)
  
```xml
<SuggestionsViewOptions>
   <GoodThreshold>...</GoodThreshold>
   <MaximumResultsByDay>...</MaximumResultsByDay>
   <MaximumNonWorkingHourResultsByDay>...</MaximumNonWorkingHourResultsByDay>
   <MeetingDurationInMinutes>...</MeetingDurationInMinutes>
   <MinimumSuggestionQuality>...</MinimumSuggestionQuality>
   <SuggestionIntervalInMinutes>...</SuggestionIntervalInMinutes>
   <DetailedSuggestionsWindow>...</DetailedSuggestionsWindow>
   <CurrentMeetingTime>...</CurrentMeetingTime>
   <GlobalObjectId>...</GlobalObjectId>
</SuggestionsViewOptions>
```

 <span data-ttu-id="d5e20-107">**SuggestionsViewOptionsType**</span><span class="sxs-lookup"><span data-stu-id="d5e20-107">**SuggestionsViewOptionsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d5e20-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d5e20-108">Attributes and elements</span></span>

<span data-ttu-id="d5e20-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d5e20-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d5e20-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="d5e20-110">Attributes</span></span>

<span data-ttu-id="d5e20-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d5e20-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d5e20-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d5e20-112">Child elements</span></span>

|<span data-ttu-id="d5e20-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="d5e20-113">**Element**</span></span>|<span data-ttu-id="d5e20-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d5e20-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d5e20-115">GoodThreshold</span><span class="sxs-lookup"><span data-stu-id="d5e20-115">GoodThreshold</span></span>](goodthreshold.md) <br/> |<span data-ttu-id="d5e20-116">Especifica el porcentaje de los asistentes que debe tener el período de tiempo abierto para que el período de tiempo calificar como una hora de reunión sugerida buena.</span><span class="sxs-lookup"><span data-stu-id="d5e20-116">Specifies the percentage of attendees that must have the time period open for the time period to qualify as a good suggested meeting time.</span></span>  <br/> |
|[<span data-ttu-id="d5e20-117">MaximumResultsByDay</span><span class="sxs-lookup"><span data-stu-id="d5e20-117">MaximumResultsByDay</span></span>](maximumresultsbyday.md) <br/> |<span data-ttu-id="d5e20-118">Especifica el número de veces que la reunión sugerida por día devuelto en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d5e20-118">Specifies the number of suggested meeting times per day returned in the response.</span></span>  <br/> |
|[<span data-ttu-id="d5e20-119">MaximumNonWorkHourResultsByDay</span><span class="sxs-lookup"><span data-stu-id="d5e20-119">MaximumNonWorkHourResultsByDay</span></span>](maximumnonworkhourresultsbyday.md) <br/> |<span data-ttu-id="d5e20-120">Especifica el número de resultados sugeridos para horas fuera del horario normal de trabajo por día de la reunión.</span><span class="sxs-lookup"><span data-stu-id="d5e20-120">Specifies the number of suggested results for meeting times outside regular working hours per day.</span></span>  <br/> |
|[<span data-ttu-id="d5e20-121">MeetingDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="d5e20-121">MeetingDurationInMinutes</span></span>](meetingdurationinminutes.md) <br/> |<span data-ttu-id="d5e20-122">Especifica la longitud de la reunión que sugerir.</span><span class="sxs-lookup"><span data-stu-id="d5e20-122">Specifies the length of the meeting to be suggested.</span></span>  <br/> |
|[<span data-ttu-id="d5e20-123">MinimumSuggestionQuality</span><span class="sxs-lookup"><span data-stu-id="d5e20-123">MinimumSuggestionQuality</span></span>](minimumsuggestionquality.md) <br/> |<span data-ttu-id="d5e20-124">Especifica la calidad de sugerencias de reunión que se devuelve en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d5e20-124">Specifies the quality of meeting suggestions to be returned in the response.</span></span>  <br/> |
|[<span data-ttu-id="d5e20-125">DetailedSuggestionsWindow</span><span class="sxs-lookup"><span data-stu-id="d5e20-125">DetailedSuggestionsWindow</span></span>](detailedsuggestionswindow.md) <br/> |<span data-ttu-id="d5e20-126">Identifica el intervalo de tiempo que se consulta para obtener información detallada acerca de las horas de reunión sugerida.</span><span class="sxs-lookup"><span data-stu-id="d5e20-126">Identifies the time span that is queried for detailed information about suggested meeting times.</span></span>  <br/> |
|[<span data-ttu-id="d5e20-127">CurrentMeetingTime</span><span class="sxs-lookup"><span data-stu-id="d5e20-127">CurrentMeetingTime</span></span>](currentmeetingtime.md) <br/> |<span data-ttu-id="d5e20-128">Los resultados de tiempo representa la hora de inicio de una reunión que desee actualizar con la reunión sugerida.</span><span class="sxs-lookup"><span data-stu-id="d5e20-128">Represents the start time of a meeting that you want to update with the suggested meeting time results.</span></span>  <br/> |
|[<span data-ttu-id="d5e20-129">GlobalObjectId</span><span class="sxs-lookup"><span data-stu-id="d5e20-129">GlobalObjectId</span></span>](globalobjectid.md) <br/> |<span data-ttu-id="d5e20-130">No se usa este elemento.</span><span class="sxs-lookup"><span data-stu-id="d5e20-130">This element is not used.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d5e20-131">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d5e20-131">Parent elements</span></span>

|<span data-ttu-id="d5e20-132">**Element**</span><span class="sxs-lookup"><span data-stu-id="d5e20-132">**Element**</span></span>|<span data-ttu-id="d5e20-133">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d5e20-133">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d5e20-134">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="d5e20-134">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md) <br/> |<span data-ttu-id="d5e20-135">Contiene los argumentos utilizados para obtener información de disponibilidad del usuario.</span><span class="sxs-lookup"><span data-stu-id="d5e20-135">Contains the arguments used to obtain user availability information.</span></span> <span data-ttu-id="d5e20-136">Esto es un elemento raíz.</span><span class="sxs-lookup"><span data-stu-id="d5e20-136">This is a root element.</span></span>  <br/> <span data-ttu-id="d5e20-137">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="d5e20-137">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d5e20-138">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d5e20-138">Remarks</span></span>

<span data-ttu-id="d5e20-139">Este elemento no es necesario y sólo puede aparecer una vez si se usa.</span><span class="sxs-lookup"><span data-stu-id="d5e20-139">This element is not required and can only occur once if used.</span></span> <span data-ttu-id="d5e20-140">Este valor puede ser null si el valor del elemento [FreeBusyViewOptions](freebusyviewoptions.md) no es nulo.</span><span class="sxs-lookup"><span data-stu-id="d5e20-140">This value can be null if the value of the [FreeBusyViewOptions](freebusyviewoptions.md) element is not null.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d5e20-141">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="d5e20-141">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="d5e20-142">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d5e20-142">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d5e20-143">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d5e20-143">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d5e20-144">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d5e20-144">Schema Name</span></span>  <br/> |<span data-ttu-id="d5e20-145">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="d5e20-145">Types schema</span></span>  <br/> |
|<span data-ttu-id="d5e20-146">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d5e20-146">Validation File</span></span>  <br/> |<span data-ttu-id="d5e20-147">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d5e20-147">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d5e20-148">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d5e20-148">Can be Empty</span></span>  <br/> |<span data-ttu-id="d5e20-149">False</span><span class="sxs-lookup"><span data-stu-id="d5e20-149">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d5e20-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="d5e20-150">See also</span></span>



[<span data-ttu-id="d5e20-151">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="d5e20-151">GetUserAvailability operation</span></span>](getuseravailability-operation.md)


[<span data-ttu-id="d5e20-152">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="d5e20-152">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

