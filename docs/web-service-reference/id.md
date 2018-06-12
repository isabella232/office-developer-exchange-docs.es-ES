---
title: id.
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ID
api_type:
- schema
ms.assetid: 8caf922f-56bd-466a-a68f-d6cb236f2eec
description: El elemento de identificador representa el identificador de entrada del elemento de calendario.
ms.openlocfilehash: bdfadcbe074135aca34a408e69ed4a69974eb5d5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19835855"
---
# <a name="id"></a><span data-ttu-id="89ac3-103">id.</span><span class="sxs-lookup"><span data-stu-id="89ac3-103">ID</span></span>

<span data-ttu-id="89ac3-104">El elemento de **identificador** representa el identificador de entrada del elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="89ac3-104">The **ID** element represents the entry ID of the calendar item.</span></span> 
  
[<span data-ttu-id="89ac3-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="89ac3-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="89ac3-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="89ac3-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="89ac3-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="89ac3-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="89ac3-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="89ac3-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="89ac3-109">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="89ac3-109">CalendarEventArray</span></span>](calendareventarray.md)
  
[<span data-ttu-id="89ac3-110">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="89ac3-110">CalendarEvent</span></span>](calendarevent.md)
  
[<span data-ttu-id="89ac3-111">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="89ac3-111">CalendarEventDetails</span></span>](calendareventdetails.md)
  
[<span data-ttu-id="89ac3-112">ID</span><span class="sxs-lookup"><span data-stu-id="89ac3-112">ID</span></span>](id.md)
  
```xml
<ID>...</ID>
```

 <span data-ttu-id="89ac3-113">**string**</span><span class="sxs-lookup"><span data-stu-id="89ac3-113">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="89ac3-114">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="89ac3-114">Attributes and elements</span></span>

<span data-ttu-id="89ac3-115">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="89ac3-115">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="89ac3-116">Atributos</span><span class="sxs-lookup"><span data-stu-id="89ac3-116">Attributes</span></span>

<span data-ttu-id="89ac3-117">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="89ac3-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="89ac3-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="89ac3-118">Child elements</span></span>

<span data-ttu-id="89ac3-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="89ac3-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="89ac3-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="89ac3-120">Parent elements</span></span>

|<span data-ttu-id="89ac3-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="89ac3-121">**Element**</span></span>|<span data-ttu-id="89ac3-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="89ac3-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="89ac3-123">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="89ac3-123">CalendarEventDetails</span></span>](calendareventdetails.md) <br/> |<span data-ttu-id="89ac3-124">Proporciona información adicional para un evento del calendario.</span><span class="sxs-lookup"><span data-stu-id="89ac3-124">Provides additional information for a calendar event.</span></span>  <br/> <span data-ttu-id="89ac3-125">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="89ac3-125">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]/CalendarEventDetails` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="89ac3-126">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="89ac3-126">Text value</span></span>

<span data-ttu-id="89ac3-127">Si este elemento se devuelve en la respuesta, es necesario un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="89ac3-127">A text value is required if this element is returned in the response.</span></span> <span data-ttu-id="89ac3-128">Este elemento es necesario si se usa el elemento [CalendarEventDetails](calendareventdetails.md) .</span><span class="sxs-lookup"><span data-stu-id="89ac3-128">This element is required if the [CalendarEventDetails](calendareventdetails.md) element is used.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="89ac3-129">Notas</span><span class="sxs-lookup"><span data-stu-id="89ac3-129">Remarks</span></span>

<span data-ttu-id="89ac3-130">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="89ac3-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="89ac3-131">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="89ac3-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="89ac3-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="89ac3-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="89ac3-133">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="89ac3-133">Schema Name</span></span>  <br/> |<span data-ttu-id="89ac3-134">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="89ac3-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="89ac3-135">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="89ac3-135">Validation File</span></span>  <br/> |<span data-ttu-id="89ac3-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="89ac3-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="89ac3-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="89ac3-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="89ac3-138">False</span><span class="sxs-lookup"><span data-stu-id="89ac3-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="89ac3-139">Ver también</span><span class="sxs-lookup"><span data-stu-id="89ac3-139">See also</span></span>



[<span data-ttu-id="89ac3-140">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="89ac3-140">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="89ac3-141">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="89ac3-141">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="89ac3-142">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="89ac3-142">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

