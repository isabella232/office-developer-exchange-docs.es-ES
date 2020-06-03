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
description: El elemento SuggestionsViewOptions contiene las opciones para obtener información sobre las sugerencias de la reunión.
ms.openlocfilehash: f584b19997f98760bd4e438dcd48a5c18cc63e4b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44433997"
---
# <a name="suggestionsviewoptions"></a><span data-ttu-id="96191-103">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="96191-103">SuggestionsViewOptions</span></span>

<span data-ttu-id="96191-104">El elemento **SuggestionsViewOptions** contiene las opciones para obtener información sobre las sugerencias de la reunión.</span><span class="sxs-lookup"><span data-stu-id="96191-104">The **SuggestionsViewOptions** element contains the options for obtaining meeting suggestion information.</span></span> 
  
[<span data-ttu-id="96191-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="96191-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
[<span data-ttu-id="96191-106">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="96191-106">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md)
  
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

 <span data-ttu-id="96191-107">**SuggestionsViewOptionsType**</span><span class="sxs-lookup"><span data-stu-id="96191-107">**SuggestionsViewOptionsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="96191-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="96191-108">Attributes and elements</span></span>

<span data-ttu-id="96191-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="96191-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="96191-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="96191-110">Attributes</span></span>

<span data-ttu-id="96191-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="96191-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="96191-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="96191-112">Child elements</span></span>

|<span data-ttu-id="96191-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="96191-113">**Element**</span></span>|<span data-ttu-id="96191-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="96191-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="96191-115">GoodThreshold</span><span class="sxs-lookup"><span data-stu-id="96191-115">GoodThreshold</span></span>](goodthreshold.md) <br/> |<span data-ttu-id="96191-116">Especifica el porcentaje de asistentes que deben tener el período de tiempo abierto durante el período de tiempo para calificarse como una buena hora de reunión.</span><span class="sxs-lookup"><span data-stu-id="96191-116">Specifies the percentage of attendees that must have the time period open for the time period to qualify as a good suggested meeting time.</span></span>  <br/> |
|[<span data-ttu-id="96191-117">MaximumResultsByDay</span><span class="sxs-lookup"><span data-stu-id="96191-117">MaximumResultsByDay</span></span>](maximumresultsbyday.md) <br/> |<span data-ttu-id="96191-118">Especifica el número de horas sugeridas de reuniones por día devueltas en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="96191-118">Specifies the number of suggested meeting times per day returned in the response.</span></span>  <br/> |
|[<span data-ttu-id="96191-119">MaximumNonWorkHourResultsByDay</span><span class="sxs-lookup"><span data-stu-id="96191-119">MaximumNonWorkHourResultsByDay</span></span>](maximumnonworkhourresultsbyday.md) <br/> |<span data-ttu-id="96191-120">Especifica el número de resultados sugeridos para las horas de reunión fuera del horario laboral normal por día.</span><span class="sxs-lookup"><span data-stu-id="96191-120">Specifies the number of suggested results for meeting times outside regular working hours per day.</span></span>  <br/> |
|[<span data-ttu-id="96191-121">MeetingDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="96191-121">MeetingDurationInMinutes</span></span>](meetingdurationinminutes.md) <br/> |<span data-ttu-id="96191-122">Especifica la duración de la reunión que se va a sugerir.</span><span class="sxs-lookup"><span data-stu-id="96191-122">Specifies the length of the meeting to be suggested.</span></span>  <br/> |
|[<span data-ttu-id="96191-123">MinimumSuggestionQuality</span><span class="sxs-lookup"><span data-stu-id="96191-123">MinimumSuggestionQuality</span></span>](minimumsuggestionquality.md) <br/> |<span data-ttu-id="96191-124">Especifica la calidad de las sugerencias de reunión que se devolverán en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="96191-124">Specifies the quality of meeting suggestions to be returned in the response.</span></span>  <br/> |
|[<span data-ttu-id="96191-125">DetailedSuggestionsWindow</span><span class="sxs-lookup"><span data-stu-id="96191-125">DetailedSuggestionsWindow</span></span>](detailedsuggestionswindow.md) <br/> |<span data-ttu-id="96191-126">Identifica el intervalo de tiempo que se consulta para obtener información detallada sobre las horas de reunión sugeridas.</span><span class="sxs-lookup"><span data-stu-id="96191-126">Identifies the time span that is queried for detailed information about suggested meeting times.</span></span>  <br/> |
|[<span data-ttu-id="96191-127">CurrentMeetingTime</span><span class="sxs-lookup"><span data-stu-id="96191-127">CurrentMeetingTime</span></span>](currentmeetingtime.md) <br/> |<span data-ttu-id="96191-128">Representa la hora de inicio de una reunión que desea actualizar con los resultados de la hora de la reunión sugerida.</span><span class="sxs-lookup"><span data-stu-id="96191-128">Represents the start time of a meeting that you want to update with the suggested meeting time results.</span></span>  <br/> |
|[<span data-ttu-id="96191-129">GlobalObjectId</span><span class="sxs-lookup"><span data-stu-id="96191-129">GlobalObjectId</span></span>](globalobjectid.md) <br/> |<span data-ttu-id="96191-130">Este elemento no se usa.</span><span class="sxs-lookup"><span data-stu-id="96191-130">This element is not used.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="96191-131">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="96191-131">Parent elements</span></span>

|<span data-ttu-id="96191-132">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="96191-132">**Element**</span></span>|<span data-ttu-id="96191-133">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="96191-133">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="96191-134">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="96191-134">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md) <br/> |<span data-ttu-id="96191-135">Contiene los argumentos usados para obtener información de disponibilidad del usuario.</span><span class="sxs-lookup"><span data-stu-id="96191-135">Contains the arguments used to obtain user availability information.</span></span> <span data-ttu-id="96191-136">Se trata de un elemento raíz.</span><span class="sxs-lookup"><span data-stu-id="96191-136">This is a root element.</span></span>  <br/> <span data-ttu-id="96191-137">A continuación se encuentra la expresión XPath de este elemento:</span><span class="sxs-lookup"><span data-stu-id="96191-137">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="96191-138">Comentarios</span><span class="sxs-lookup"><span data-stu-id="96191-138">Remarks</span></span>

<span data-ttu-id="96191-139">Este elemento no es necesario y solo se puede producir una vez si se usa.</span><span class="sxs-lookup"><span data-stu-id="96191-139">This element is not required and can only occur once if used.</span></span> <span data-ttu-id="96191-140">Este valor puede ser null si el valor del elemento [FreeBusyViewOptions](freebusyviewoptions.md) no es NULL.</span><span class="sxs-lookup"><span data-stu-id="96191-140">This value can be null if the value of the [FreeBusyViewOptions](freebusyviewoptions.md) element is not null.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="96191-141">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="96191-141">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="96191-142">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="96191-142">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="96191-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="96191-143">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="96191-144">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="96191-144">Schema Name</span></span>  <br/> |<span data-ttu-id="96191-145">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="96191-145">Types schema</span></span>  <br/> |
|<span data-ttu-id="96191-146">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="96191-146">Validation File</span></span>  <br/> |<span data-ttu-id="96191-147">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="96191-147">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="96191-148">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="96191-148">Can be Empty</span></span>  <br/> |<span data-ttu-id="96191-149">Falso</span><span class="sxs-lookup"><span data-stu-id="96191-149">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="96191-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="96191-150">See also</span></span>



[<span data-ttu-id="96191-151">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="96191-151">GetUserAvailability operation</span></span>](getuseravailability-operation.md)


[<span data-ttu-id="96191-152">Obtener disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="96191-152">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

