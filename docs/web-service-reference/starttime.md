---
title: StartTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- StartTime
api_type:
- schema
ms.assetid: 1fac7937-7a06-4d66-9d2a-14423bcb3b37
description: El elemento StartTime representa el inicio de un intervalo de tiempo.
ms.openlocfilehash: 4346797d755bb6e577e1cacb8bec656a7562bf1f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837560"
---
# <a name="starttime"></a><span data-ttu-id="0e2dc-103">StartTime</span><span class="sxs-lookup"><span data-stu-id="0e2dc-103">StartTime</span></span>

<span data-ttu-id="0e2dc-104">El elemento **StartTime** representa el inicio de un intervalo de tiempo.</span><span class="sxs-lookup"><span data-stu-id="0e2dc-104">The **StartTime** element represents the start of a time span.</span></span> 
  
```xml
<StartTime/
```

<span data-ttu-id="0e2dc-105">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="0e2dc-105">**dateTime**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="0e2dc-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="0e2dc-106">Attributes and elements</span></span>

<span data-ttu-id="0e2dc-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="0e2dc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0e2dc-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="0e2dc-108">Attributes</span></span>

<span data-ttu-id="0e2dc-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0e2dc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0e2dc-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0e2dc-110">Child elements</span></span>

<span data-ttu-id="0e2dc-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0e2dc-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0e2dc-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0e2dc-112">Parent elements</span></span>

|<span data-ttu-id="0e2dc-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="0e2dc-113">**Element**</span></span>|<span data-ttu-id="0e2dc-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0e2dc-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0e2dc-115">Ventana de tiempo</span><span class="sxs-lookup"><span data-stu-id="0e2dc-115">TimeWindow</span></span>](timewindow.md) <br/> |<span data-ttu-id="0e2dc-116">Identifica el intervalo de tiempo de consulta para la información de disponibilidad del usuario.</span><span class="sxs-lookup"><span data-stu-id="0e2dc-116">Identifies the time span queried for the user availability information.</span></span>  <br/><br/> <span data-ttu-id="0e2dc-117">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="0e2dc-117">The following is the XPath expression to this element:</span></span>  <br/><br/>  `/GetUserAvailabilityRequest/FreeBusyViewOptions/TimeWindow` <br/> |
|[<span data-ttu-id="0e2dc-118">DetailedSuggestionsWindow</span><span class="sxs-lookup"><span data-stu-id="0e2dc-118">DetailedSuggestionsWindow</span></span>](detailedsuggestionswindow.md) <br/> |<span data-ttu-id="0e2dc-119">Identifica el intervalo de tiempo que se consulta para obtener información detallada acerca de las horas de reunión sugerida.</span><span class="sxs-lookup"><span data-stu-id="0e2dc-119">Identifies the time span that is queried for detailed information about suggested meeting times.</span></span>  <br/><br/> <span data-ttu-id="0e2dc-120">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="0e2dc-120">The following is the XPath expression to this element:</span></span> <br/> <br/>  `/GetUserAvailabilityRequest/SuggestionViewOptions/DetailedSuggestionsWindow` <br/> |
|[<span data-ttu-id="0e2dc-121">Duración (UserOofSettings)</span><span class="sxs-lookup"><span data-stu-id="0e2dc-121">Duration (UserOofSettings)</span></span>](duration-useroofsettings.md) <br/> | <span data-ttu-id="0e2dc-122">Especifica la duración para la que está habilitado el estado de fuera de oficina (OOF) si el elemento [OofState](oofstate.md) está establecido en **programado**.</span><span class="sxs-lookup"><span data-stu-id="0e2dc-122">Specifies the duration for which the Out of Office (OOF) status is enabled if the [OofState](oofstate.md) element is set to **Scheduled**.</span></span>  <br/><br/>  <span data-ttu-id="0e2dc-123">Los siguientes son las expresiones de XPath posibles para este elemento:</span><span class="sxs-lookup"><span data-stu-id="0e2dc-123">The following are the possible XPath expressions to this element:</span></span> <br/> <br/>  `/SetUserOofSettingsRequest/UserOofSettings/Duration` <br/><br/>  `/GetUserOofSettingsResponse/OofSettings/Duration` <br/> |
|[<span data-ttu-id="0e2dc-124">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="0e2dc-124">CalendarEvent</span></span>](calendarevent.md) <br/> |<span data-ttu-id="0e2dc-125">Representa una repetición del elemento de calendario único.</span><span class="sxs-lookup"><span data-stu-id="0e2dc-125">Represents a unique calendar item occurrence.</span></span> <span data-ttu-id="0e2dc-126">Se utiliza para las consultas de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="0e2dc-126">This is used for Availability inquiries.</span></span> <span data-ttu-id="0e2dc-127">El elemento **StartTime** es necesario en el elemento **CalendarEvent** .</span><span class="sxs-lookup"><span data-stu-id="0e2dc-127">The **StartTime** element is required in the **CalendarEvent** element.</span></span> <span data-ttu-id="0e2dc-128">El elemento **StartTime** en el elemento **CalendarEvent** es único para el tipo de **CalendarEvent** aunque contiene los mismos valores de faceta que contienen los elementos **StartTime** en el tipo de **duración** .</span><span class="sxs-lookup"><span data-stu-id="0e2dc-128">The **StartTime** element in the **CalendarEvent** element is unique to the **CalendarEvent** type although it contains the same facet values that the **StartTime** elements in the **Duration** type contain.</span></span>  <br/><br/> <span data-ttu-id="0e2dc-129">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="0e2dc-129">The following is the XPath expression to this element:</span></span>  <br/> <br/> `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0e2dc-130">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="0e2dc-130">Text value</span></span>

<span data-ttu-id="0e2dc-131">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="0e2dc-131">A text value is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0e2dc-132">Notas</span><span class="sxs-lookup"><span data-stu-id="0e2dc-132">Remarks</span></span>

<span data-ttu-id="0e2dc-133">El elemento [EndTime](endtime.md) representa el final de un período de tiempo.</span><span class="sxs-lookup"><span data-stu-id="0e2dc-133">The [EndTime](endtime.md) element represents the end of the time span.</span></span> 
  
<span data-ttu-id="0e2dc-134">El esquema incluye muchos elementos [StartTime](starttime.md) .</span><span class="sxs-lookup"><span data-stu-id="0e2dc-134">The schema includes many [StartTime](starttime.md) elements.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="0e2dc-135">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="0e2dc-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="0e2dc-136">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0e2dc-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0e2dc-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0e2dc-137">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0e2dc-138">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="0e2dc-138">Schema Name</span></span>  <br/> |<span data-ttu-id="0e2dc-139">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="0e2dc-139">Types schema</span></span>  <br/> |
|<span data-ttu-id="0e2dc-140">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="0e2dc-140">Validation File</span></span>  <br/> |<span data-ttu-id="0e2dc-141">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0e2dc-141">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0e2dc-142">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="0e2dc-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="0e2dc-143">False</span><span class="sxs-lookup"><span data-stu-id="0e2dc-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0e2dc-144">Ver también</span><span class="sxs-lookup"><span data-stu-id="0e2dc-144">See also</span></span>

- [<span data-ttu-id="0e2dc-145">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="0e2dc-145">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="0e2dc-146">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="0e2dc-146">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

