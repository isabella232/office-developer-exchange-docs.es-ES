---
title: IsException
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsException
api_type:
- schema
ms.assetid: e7bd8ae2-2643-411e-ae08-358bac445800
description: El elemento IsException indica si se cambia una instancia de un elemento periódico del calendario desde el maestro.
ms.openlocfilehash: bb884110fd3642bebbc03504aef369f9e0412714
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836009"
---
# <a name="isexception"></a><span data-ttu-id="36cc4-103">IsException</span><span class="sxs-lookup"><span data-stu-id="36cc4-103">IsException</span></span>

<span data-ttu-id="36cc4-104">El elemento **IsException** indica si se cambia una instancia de un elemento periódico del calendario desde el maestro.</span><span class="sxs-lookup"><span data-stu-id="36cc4-104">The **IsException** element indicates whether an instance of a recurring calendar item is changed from the master.</span></span> 
  
[<span data-ttu-id="36cc4-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="36cc4-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="36cc4-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="36cc4-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="36cc4-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="36cc4-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="36cc4-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="36cc4-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="36cc4-109">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="36cc4-109">CalendarEventArray</span></span>](calendareventarray.md)
  
[<span data-ttu-id="36cc4-110">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="36cc4-110">CalendarEvent</span></span>](calendarevent.md)
  
[<span data-ttu-id="36cc4-111">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="36cc4-111">CalendarEventDetails</span></span>](calendareventdetails.md)
  
[<span data-ttu-id="36cc4-112">IsException</span><span class="sxs-lookup"><span data-stu-id="36cc4-112">IsException</span></span>](isexception.md)
  
```xml
<IsException/>
```

 <span data-ttu-id="36cc4-113">**boolean**</span><span class="sxs-lookup"><span data-stu-id="36cc4-113">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="36cc4-114">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="36cc4-114">Attributes and elements</span></span>

<span data-ttu-id="36cc4-115">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="36cc4-115">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="36cc4-116">Atributos</span><span class="sxs-lookup"><span data-stu-id="36cc4-116">Attributes</span></span>

<span data-ttu-id="36cc4-117">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="36cc4-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="36cc4-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="36cc4-118">Child elements</span></span>

<span data-ttu-id="36cc4-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="36cc4-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="36cc4-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="36cc4-120">Parent elements</span></span>

|<span data-ttu-id="36cc4-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="36cc4-121">**Element**</span></span>|<span data-ttu-id="36cc4-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="36cc4-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="36cc4-123">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="36cc4-123">CalendarEventDetails</span></span>](calendareventdetails.md) <br/> |<span data-ttu-id="36cc4-124">Proporciona información adicional acerca de un evento de calendario.</span><span class="sxs-lookup"><span data-stu-id="36cc4-124">Provides additional information about a calendar event.</span></span>  <br/> <span data-ttu-id="36cc4-125">La siguiente es la expresión de XPath 2.0 para este elemento:</span><span class="sxs-lookup"><span data-stu-id="36cc4-125">The following is the XPath 2.0 expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]/CalendarEventDetails` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="36cc4-126">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="36cc4-126">Text value</span></span>

<span data-ttu-id="36cc4-127">Si este elemento se devuelve en la respuesta, es necesario un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="36cc4-127">A text value is required if this element is returned in the response.</span></span> <span data-ttu-id="36cc4-128">Este elemento es necesario si se usa el elemento [CalendarEventDetails](calendareventdetails.md) .</span><span class="sxs-lookup"><span data-stu-id="36cc4-128">This element is required if the [CalendarEventDetails](calendareventdetails.md) element is used.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="36cc4-129">Notas</span><span class="sxs-lookup"><span data-stu-id="36cc4-129">Remarks</span></span>

<span data-ttu-id="36cc4-130">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="36cc4-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="36cc4-131">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="36cc4-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="36cc4-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="36cc4-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="36cc4-133">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="36cc4-133">Schema Name</span></span>  <br/> |<span data-ttu-id="36cc4-134">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="36cc4-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="36cc4-135">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="36cc4-135">Validation File</span></span>  <br/> |<span data-ttu-id="36cc4-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="36cc4-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="36cc4-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="36cc4-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="36cc4-138">False</span><span class="sxs-lookup"><span data-stu-id="36cc4-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="36cc4-139">Ver también</span><span class="sxs-lookup"><span data-stu-id="36cc4-139">See also</span></span>



[<span data-ttu-id="36cc4-140">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="36cc4-140">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="36cc4-141">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="36cc4-141">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="36cc4-142">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="36cc4-142">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

