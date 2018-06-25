---
title: Hora de finalización
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
ms.openlocfilehash: 7d3d186618a7bcc05ad82532e13e03d2e67a0e40
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764428"
---
# <a name="endtime"></a><span data-ttu-id="260c7-103">Hora de finalización</span><span class="sxs-lookup"><span data-stu-id="260c7-103">EndTime</span></span>

<span data-ttu-id="260c7-104">El elemento **EndTime** representa el final de un intervalo de tiempo.</span><span class="sxs-lookup"><span data-stu-id="260c7-104">The **EndTime** element represents the end of a time span.</span></span> 
  
```xml
<EndTime>dateTime</EndTime>
```

 <span data-ttu-id="260c7-105">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="260c7-105">**dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="260c7-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="260c7-106">Attributes and elements</span></span>

<span data-ttu-id="260c7-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="260c7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="260c7-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="260c7-108">Attributes</span></span>

<span data-ttu-id="260c7-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="260c7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="260c7-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="260c7-110">Child elements</span></span>

<span data-ttu-id="260c7-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="260c7-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="260c7-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="260c7-112">Parent elements</span></span>

|<span data-ttu-id="260c7-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="260c7-113">**Element**</span></span>|<span data-ttu-id="260c7-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="260c7-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="260c7-115">Ventana de tiempo</span><span class="sxs-lookup"><span data-stu-id="260c7-115">TimeWindow</span></span>](timewindow.md) <br/> |<span data-ttu-id="260c7-116">Identifica el intervalo de tiempo de consulta para la información de disponibilidad del usuario.</span><span class="sxs-lookup"><span data-stu-id="260c7-116">Identifies the time span queried for the user availability information.</span></span><br/><br/> <span data-ttu-id="260c7-117">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="260c7-117">The following is the XPath expression to this element:</span></span><br/><br/>  `/GetUserAvailabilityRequest/FreeBusyViewOptions/TimeWindow` <br/> |
|[<span data-ttu-id="260c7-118">DetailedSuggestionsWindow</span><span class="sxs-lookup"><span data-stu-id="260c7-118">DetailedSuggestionsWindow</span></span>](detailedsuggestionswindow.md) <br/> |<span data-ttu-id="260c7-119">Identifica el intervalo de tiempo que se consulta para obtener información detallada acerca de las horas de reunión sugerida.</span><span class="sxs-lookup"><span data-stu-id="260c7-119">Identifies the time span that is queried for detailed information about suggested meeting times.</span></span><br/><br/> <span data-ttu-id="260c7-120">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="260c7-120">The following is the XPath expression to this element:</span></span><br/><br/>  <span data-ttu-id="260c7-121">`/GetUserAvailabilityRequest/SuggestionViewOptions/DetailedSuggestionsWindow`.</span><span class="sxs-lookup"><span data-stu-id="260c7-121"></span></span>  <br/> |
|[<span data-ttu-id="260c7-122">Duración (UserOofSettings)</span><span class="sxs-lookup"><span data-stu-id="260c7-122">Duration (UserOofSettings)</span></span>](duration-useroofsettings.md) <br/> | <span data-ttu-id="260c7-123">Especifica la duración para la que está habilitado el estado de fuera de oficina (OOF) si el elemento [OofState](oofstate.md) está establecido en **programado**.</span><span class="sxs-lookup"><span data-stu-id="260c7-123">Specifies the duration for which the Out of Office (OOF) status is enabled if the [OofState](oofstate.md) element is set to **Scheduled**.</span></span>  <br/><br/>  <span data-ttu-id="260c7-124">Los siguientes son las expresiones de XPath posibles para este elemento:</span><span class="sxs-lookup"><span data-stu-id="260c7-124">The following are the possible XPath expressions to this element:</span></span><br/><br/>  `/SetUserOofSettingsRequest/UserOofSettings/Duration` <br/><br/>  `/GetUserOofSettingsResponse/OofSettings/Duration` <br/> |
|[<span data-ttu-id="260c7-125">Repetición</span><span class="sxs-lookup"><span data-stu-id="260c7-125">Occurrence</span></span>](occurrence.md) <br/> |<span data-ttu-id="260c7-126">Representa una sola aparición de modificación de un elemento periódico del calendario.</span><span class="sxs-lookup"><span data-stu-id="260c7-126">Represents a single modified occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="260c7-127">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="260c7-127">CalendarEvent</span></span>](calendarevent.md) <br/> |<span data-ttu-id="260c7-128">Representa una repetición del elemento de calendario único.</span><span class="sxs-lookup"><span data-stu-id="260c7-128">Represents a unique calendar item occurrence.</span></span> <span data-ttu-id="260c7-129">Se utiliza para las consultas de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="260c7-129">This is used for Availability inquiries.</span></span> <span data-ttu-id="260c7-130">El elemento **EndTime** es necesario en el elemento **CalendarEvent** .</span><span class="sxs-lookup"><span data-stu-id="260c7-130">The **EndTime** element is required in the **CalendarEvent** element.</span></span> <span data-ttu-id="260c7-131">El elemento **EndTime** en el elemento **CalendarEvent** es único para el tipo de **CalendarEvent** .</span><span class="sxs-lookup"><span data-stu-id="260c7-131">The **EndTime** element in the **CalendarEvent** element is unique to the **CalendarEvent** type.</span></span><br/><br/> <span data-ttu-id="260c7-132">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="260c7-132">The following is the XPath expression to this element:</span></span><br/><br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="260c7-133">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="260c7-133">Text value</span></span>

<span data-ttu-id="260c7-134">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="260c7-134">A text value is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="260c7-135">Comentarios</span><span class="sxs-lookup"><span data-stu-id="260c7-135">Remarks</span></span>

<span data-ttu-id="260c7-136">El elemento [StartTime](starttime.md) representa el principio de un intervalo de tiempo.</span><span class="sxs-lookup"><span data-stu-id="260c7-136">The [StartTime](starttime.md) element represents the beginning of a time span.</span></span> 
  
<span data-ttu-id="260c7-137">La hora de finalización representa la hora del cliente.</span><span class="sxs-lookup"><span data-stu-id="260c7-137">The end time represents the client's time.</span></span>
  
<span data-ttu-id="260c7-138">El esquema incluye muchos elementos [EndTime](endtime.md) .</span><span class="sxs-lookup"><span data-stu-id="260c7-138">The schema includes many [EndTime](endtime.md) elements.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="260c7-139">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="260c7-139">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="260c7-140">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="260c7-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="260c7-141">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="260c7-141">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="260c7-142">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="260c7-142">Schema Name</span></span>  <br/> |<span data-ttu-id="260c7-143">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="260c7-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="260c7-144">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="260c7-144">Validation File</span></span>  <br/> |<span data-ttu-id="260c7-145">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="260c7-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="260c7-146">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="260c7-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="260c7-147">False</span><span class="sxs-lookup"><span data-stu-id="260c7-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="260c7-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="260c7-148">See also</span></span>

- [<span data-ttu-id="260c7-149">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="260c7-149">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="260c7-150">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="260c7-150">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

