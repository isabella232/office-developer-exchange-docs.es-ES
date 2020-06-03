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
ms.openlocfilehash: 16bee698b65dc512a709e2af9ddfe8629347fee3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458568"
---
# <a name="starttime"></a><span data-ttu-id="a7993-103">StartTime</span><span class="sxs-lookup"><span data-stu-id="a7993-103">StartTime</span></span>

<span data-ttu-id="a7993-104">El elemento **startTime** representa el inicio de un intervalo de tiempo.</span><span class="sxs-lookup"><span data-stu-id="a7993-104">The **StartTime** element represents the start of a time span.</span></span> 
  
```xml
<StartTime/
```

<span data-ttu-id="a7993-105">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="a7993-105">**dateTime**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="a7993-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a7993-106">Attributes and elements</span></span>

<span data-ttu-id="a7993-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a7993-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a7993-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="a7993-108">Attributes</span></span>

<span data-ttu-id="a7993-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="a7993-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a7993-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a7993-110">Child elements</span></span>

<span data-ttu-id="a7993-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="a7993-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a7993-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a7993-112">Parent elements</span></span>

|<span data-ttu-id="a7993-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a7993-113">**Element**</span></span>|<span data-ttu-id="a7993-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a7993-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a7993-115">TimeWindow</span><span class="sxs-lookup"><span data-stu-id="a7993-115">TimeWindow</span></span>](timewindow.md) <br/> |<span data-ttu-id="a7993-116">Identifica el intervalo de tiempo consultado para obtener la información de disponibilidad del usuario.</span><span class="sxs-lookup"><span data-stu-id="a7993-116">Identifies the time span queried for the user availability information.</span></span>  <br/><br/> <span data-ttu-id="a7993-117">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="a7993-117">The following is the XPath expression to this element:</span></span>  <br/><br/>  `/GetUserAvailabilityRequest/FreeBusyViewOptions/TimeWindow` <br/> |
|[<span data-ttu-id="a7993-118">DetailedSuggestionsWindow</span><span class="sxs-lookup"><span data-stu-id="a7993-118">DetailedSuggestionsWindow</span></span>](detailedsuggestionswindow.md) <br/> |<span data-ttu-id="a7993-119">Identifica el intervalo de tiempo que se consulta para obtener información detallada sobre las horas de reunión sugeridas.</span><span class="sxs-lookup"><span data-stu-id="a7993-119">Identifies the time span that is queried for detailed information about suggested meeting times.</span></span>  <br/><br/> <span data-ttu-id="a7993-120">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="a7993-120">The following is the XPath expression to this element:</span></span> <br/> <br/>  `/GetUserAvailabilityRequest/SuggestionViewOptions/DetailedSuggestionsWindow` <br/> |
|[<span data-ttu-id="a7993-121">Duración (UserOofSettings)</span><span class="sxs-lookup"><span data-stu-id="a7993-121">Duration (UserOofSettings)</span></span>](duration-useroofsettings.md) <br/> | <span data-ttu-id="a7993-122">Especifica el tiempo durante el que se habilita el estado fuera de la oficina si el elemento [OofState](oofstate.md) está establecido en **programado**.</span><span class="sxs-lookup"><span data-stu-id="a7993-122">Specifies the duration for which the Out of Office (OOF) status is enabled if the [OofState](oofstate.md) element is set to **Scheduled**.</span></span>  <br/><br/>  <span data-ttu-id="a7993-123">Las siguientes son las posibles expresiones de XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="a7993-123">The following are the possible XPath expressions to this element:</span></span> <br/> <br/>  `/SetUserOofSettingsRequest/UserOofSettings/Duration` <br/><br/>  `/GetUserOofSettingsResponse/OofSettings/Duration` <br/> |
|[<span data-ttu-id="a7993-124">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="a7993-124">CalendarEvent</span></span>](calendarevent.md) <br/> |<span data-ttu-id="a7993-125">Representa una ocurrencia única del elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="a7993-125">Represents a unique calendar item occurrence.</span></span> <span data-ttu-id="a7993-126">Se usa para las consultas de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="a7993-126">This is used for Availability inquiries.</span></span> <span data-ttu-id="a7993-127">El elemento **startTime** es obligatorio en el elemento **CalendarEvent** .</span><span class="sxs-lookup"><span data-stu-id="a7993-127">The **StartTime** element is required in the **CalendarEvent** element.</span></span> <span data-ttu-id="a7993-128">El elemento **startTime** del elemento **CalendarEvent** es único para el tipo **CalendarEvent** , aunque contiene los mismos valores de faceta que los elementos **startTime** en el tipo de **duración** .</span><span class="sxs-lookup"><span data-stu-id="a7993-128">The **StartTime** element in the **CalendarEvent** element is unique to the **CalendarEvent** type although it contains the same facet values that the **StartTime** elements in the **Duration** type contain.</span></span>  <br/><br/> <span data-ttu-id="a7993-129">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="a7993-129">The following is the XPath expression to this element:</span></span>  <br/> <br/> `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a7993-130">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="a7993-130">Text value</span></span>

<span data-ttu-id="a7993-131">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="a7993-131">A text value is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a7993-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a7993-132">Remarks</span></span>

<span data-ttu-id="a7993-133">El elemento [EndTime](endtime.md) representa el final del intervalo de tiempo.</span><span class="sxs-lookup"><span data-stu-id="a7993-133">The [EndTime](endtime.md) element represents the end of the time span.</span></span> 
  
<span data-ttu-id="a7993-134">El esquema incluye muchos elementos [startTime](starttime.md) .</span><span class="sxs-lookup"><span data-stu-id="a7993-134">The schema includes many [StartTime](starttime.md) elements.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a7993-135">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="a7993-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="a7993-136">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a7993-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a7993-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="a7993-137">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a7993-138">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a7993-138">Schema Name</span></span>  <br/> |<span data-ttu-id="a7993-139">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="a7993-139">Types schema</span></span>  <br/> |
|<span data-ttu-id="a7993-140">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a7993-140">Validation File</span></span>  <br/> |<span data-ttu-id="a7993-141">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="a7993-141">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a7993-142">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a7993-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="a7993-143">Falso</span><span class="sxs-lookup"><span data-stu-id="a7993-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a7993-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="a7993-144">See also</span></span>

- [<span data-ttu-id="a7993-145">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="a7993-145">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="a7993-146">Obtener disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="a7993-146">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

