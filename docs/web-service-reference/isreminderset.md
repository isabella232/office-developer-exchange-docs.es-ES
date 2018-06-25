---
title: IsReminderSet
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsReminderSet
api_type:
- schema
ms.assetid: 6aea4cb7-ca14-4949-8e7f-660b565f6556
description: El elemento IsReminderSet indica si se ha establecido un aviso para el evento de calendario.
ms.openlocfilehash: 589178072baca652bff2779e64a212fb90478247
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836100"
---
# <a name="isreminderset"></a><span data-ttu-id="ace26-103">IsReminderSet</span><span class="sxs-lookup"><span data-stu-id="ace26-103">IsReminderSet</span></span>

<span data-ttu-id="ace26-104">El elemento **IsReminderSet** indica si se ha establecido un aviso para el evento de calendario.</span><span class="sxs-lookup"><span data-stu-id="ace26-104">The **IsReminderSet** element indicates whether a reminder has been set for the calendar event.</span></span> 
  
[<span data-ttu-id="ace26-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="ace26-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="ace26-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="ace26-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="ace26-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="ace26-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="ace26-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="ace26-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="ace26-109">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="ace26-109">CalendarEventArray</span></span>](calendareventarray.md)
  
[<span data-ttu-id="ace26-110">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="ace26-110">CalendarEvent</span></span>](calendarevent.md)
  
[<span data-ttu-id="ace26-111">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="ace26-111">CalendarEventDetails</span></span>](calendareventdetails.md)
  
[<span data-ttu-id="ace26-112">IsReminderSet</span><span class="sxs-lookup"><span data-stu-id="ace26-112">IsReminderSet</span></span>](isreminderset.md)
  
```xml
<IsReminderSet>true or false</IsReminderSet>
```

 <span data-ttu-id="ace26-113">**boolean**</span><span class="sxs-lookup"><span data-stu-id="ace26-113">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ace26-114">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ace26-114">Attributes and elements</span></span>

<span data-ttu-id="ace26-115">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ace26-115">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ace26-116">Atributos</span><span class="sxs-lookup"><span data-stu-id="ace26-116">Attributes</span></span>

<span data-ttu-id="ace26-117">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ace26-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ace26-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ace26-118">Child elements</span></span>

<span data-ttu-id="ace26-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ace26-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ace26-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ace26-120">Parent elements</span></span>

|<span data-ttu-id="ace26-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="ace26-121">**Element**</span></span>|<span data-ttu-id="ace26-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ace26-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ace26-123">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="ace26-123">CalendarEventDetails</span></span>](calendareventdetails.md) <br/> |<span data-ttu-id="ace26-124">Proporciona información adicional acerca de un evento de calendario.</span><span class="sxs-lookup"><span data-stu-id="ace26-124">Provides additional information about a calendar event.</span></span>  <br/> <span data-ttu-id="ace26-125">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="ace26-125">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]/CalendarEventDetails` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ace26-126">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="ace26-126">Text value</span></span>

<span data-ttu-id="ace26-127">Si este elemento se devuelve en la respuesta, es necesario un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="ace26-127">A text value is required if this element is returned in the response.</span></span> <span data-ttu-id="ace26-128">Este elemento es necesario si se usa el elemento [CalendarEventDetails](calendareventdetails.md) a menos que el elemento [IsPrivate](isprivate.md) está establecido en **true**.</span><span class="sxs-lookup"><span data-stu-id="ace26-128">This element is required if the [CalendarEventDetails](calendareventdetails.md) element is used unless the [IsPrivate](isprivate.md) element is set to **true**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ace26-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ace26-129">Remarks</span></span>

<span data-ttu-id="ace26-130">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="ace26-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ace26-131">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ace26-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ace26-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ace26-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ace26-133">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ace26-133">Schema Name</span></span>  <br/> |<span data-ttu-id="ace26-134">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="ace26-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="ace26-135">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ace26-135">Validation File</span></span>  <br/> |<span data-ttu-id="ace26-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ace26-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ace26-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ace26-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="ace26-138">False</span><span class="sxs-lookup"><span data-stu-id="ace26-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ace26-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="ace26-139">See also</span></span>



[<span data-ttu-id="ace26-140">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="ace26-140">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="ace26-141">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="ace26-141">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="ace26-142">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="ace26-142">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

