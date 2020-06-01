---
title: EndTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- EndTime
api_type:
- schema
ms.assetid: 82e4ef4f-a557-4044-b9b7-d91622f4ac55
description: El elemento EndTime representa el final de un intervalo de tiempo.
ms.openlocfilehash: 5a30b32ecfeafe582cd07dd662aacb0a960257c9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462995"
---
# <a name="endtime"></a><span data-ttu-id="96cc1-103">EndTime</span><span class="sxs-lookup"><span data-stu-id="96cc1-103">EndTime</span></span>

<span data-ttu-id="96cc1-104">El elemento **EndTime** representa el final de un intervalo de tiempo.</span><span class="sxs-lookup"><span data-stu-id="96cc1-104">The **EndTime** element represents the end of a time span.</span></span> 
  
```xml
<EndTime>dateTime</EndTime>
```

 <span data-ttu-id="96cc1-105">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="96cc1-105">**dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="96cc1-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="96cc1-106">Attributes and elements</span></span>

<span data-ttu-id="96cc1-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="96cc1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="96cc1-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="96cc1-108">Attributes</span></span>

<span data-ttu-id="96cc1-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="96cc1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="96cc1-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="96cc1-110">Child elements</span></span>

<span data-ttu-id="96cc1-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="96cc1-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="96cc1-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="96cc1-112">Parent elements</span></span>

|<span data-ttu-id="96cc1-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="96cc1-113">**Element**</span></span>|<span data-ttu-id="96cc1-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="96cc1-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="96cc1-115">TimeWindow</span><span class="sxs-lookup"><span data-stu-id="96cc1-115">TimeWindow</span></span>](timewindow.md) <br/> |<span data-ttu-id="96cc1-116">Identifica el intervalo de tiempo consultado para obtener la información de disponibilidad del usuario.</span><span class="sxs-lookup"><span data-stu-id="96cc1-116">Identifies the time span queried for the user availability information.</span></span><br/><br/> <span data-ttu-id="96cc1-117">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="96cc1-117">The following is the XPath expression to this element:</span></span><br/><br/>  `/GetUserAvailabilityRequest/FreeBusyViewOptions/TimeWindow` <br/> |
|[<span data-ttu-id="96cc1-118">DetailedSuggestionsWindow</span><span class="sxs-lookup"><span data-stu-id="96cc1-118">DetailedSuggestionsWindow</span></span>](detailedsuggestionswindow.md) <br/> |<span data-ttu-id="96cc1-119">Identifica el intervalo de tiempo que se consulta para obtener información detallada sobre las horas de reunión sugeridas.</span><span class="sxs-lookup"><span data-stu-id="96cc1-119">Identifies the time span that is queried for detailed information about suggested meeting times.</span></span><br/><br/> <span data-ttu-id="96cc1-120">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="96cc1-120">The following is the XPath expression to this element:</span></span><br/><br/>  <span data-ttu-id="96cc1-121">`/GetUserAvailabilityRequest/SuggestionViewOptions/DetailedSuggestionsWindow`.</span><span class="sxs-lookup"><span data-stu-id="96cc1-121">`/GetUserAvailabilityRequest/SuggestionViewOptions/DetailedSuggestionsWindow`.</span></span>  <br/> |
|[<span data-ttu-id="96cc1-122">Duración (UserOofSettings)</span><span class="sxs-lookup"><span data-stu-id="96cc1-122">Duration (UserOofSettings)</span></span>](duration-useroofsettings.md) <br/> | <span data-ttu-id="96cc1-123">Especifica el tiempo durante el que se habilita el estado fuera de la oficina si el elemento [OofState](oofstate.md) está establecido en **programado**.</span><span class="sxs-lookup"><span data-stu-id="96cc1-123">Specifies the duration for which the Out of Office (OOF) status is enabled if the [OofState](oofstate.md) element is set to **Scheduled**.</span></span>  <br/><br/>  <span data-ttu-id="96cc1-124">Las siguientes son las posibles expresiones de XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="96cc1-124">The following are the possible XPath expressions to this element:</span></span><br/><br/>  `/SetUserOofSettingsRequest/UserOofSettings/Duration` <br/><br/>  `/GetUserOofSettingsResponse/OofSettings/Duration` <br/> |
|[<span data-ttu-id="96cc1-125">Suceda</span><span class="sxs-lookup"><span data-stu-id="96cc1-125">Occurrence</span></span>](occurrence.md) <br/> |<span data-ttu-id="96cc1-126">Representa una ocurrencia única modificada de un elemento de calendario periódico.</span><span class="sxs-lookup"><span data-stu-id="96cc1-126">Represents a single modified occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="96cc1-127">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="96cc1-127">CalendarEvent</span></span>](calendarevent.md) <br/> |<span data-ttu-id="96cc1-128">Representa una ocurrencia única del elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="96cc1-128">Represents a unique calendar item occurrence.</span></span> <span data-ttu-id="96cc1-129">Se usa para las consultas de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="96cc1-129">This is used for Availability inquiries.</span></span> <span data-ttu-id="96cc1-130">El elemento **EndTime** es obligatorio en el elemento **CalendarEvent** .</span><span class="sxs-lookup"><span data-stu-id="96cc1-130">The **EndTime** element is required in the **CalendarEvent** element.</span></span> <span data-ttu-id="96cc1-131">El elemento **EndTime** del elemento **CalendarEvent** es único para el tipo **CalendarEvent** .</span><span class="sxs-lookup"><span data-stu-id="96cc1-131">The **EndTime** element in the **CalendarEvent** element is unique to the **CalendarEvent** type.</span></span><br/><br/> <span data-ttu-id="96cc1-132">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="96cc1-132">The following is the XPath expression to this element:</span></span><br/><br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="96cc1-133">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="96cc1-133">Text value</span></span>

<span data-ttu-id="96cc1-134">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="96cc1-134">A text value is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="96cc1-135">Comentarios</span><span class="sxs-lookup"><span data-stu-id="96cc1-135">Remarks</span></span>

<span data-ttu-id="96cc1-136">El elemento [startTime](starttime.md) representa el principio de un intervalo de tiempo.</span><span class="sxs-lookup"><span data-stu-id="96cc1-136">The [StartTime](starttime.md) element represents the beginning of a time span.</span></span> 
  
<span data-ttu-id="96cc1-137">La hora de finalización representa la hora del cliente.</span><span class="sxs-lookup"><span data-stu-id="96cc1-137">The end time represents the client's time.</span></span>
  
<span data-ttu-id="96cc1-138">El esquema incluye varios elementos [EndTime](endtime.md) .</span><span class="sxs-lookup"><span data-stu-id="96cc1-138">The schema includes many [EndTime](endtime.md) elements.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="96cc1-139">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="96cc1-139">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="96cc1-140">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="96cc1-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="96cc1-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="96cc1-141">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="96cc1-142">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="96cc1-142">Schema Name</span></span>  <br/> |<span data-ttu-id="96cc1-143">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="96cc1-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="96cc1-144">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="96cc1-144">Validation File</span></span>  <br/> |<span data-ttu-id="96cc1-145">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="96cc1-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="96cc1-146">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="96cc1-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="96cc1-147">Falso</span><span class="sxs-lookup"><span data-stu-id="96cc1-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="96cc1-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="96cc1-148">See also</span></span>

- [<span data-ttu-id="96cc1-149">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="96cc1-149">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="96cc1-150">Obtener disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="96cc1-150">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

