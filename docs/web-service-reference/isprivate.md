---
title: IsPrivate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsPrivate
api_type:
- schema
ms.assetid: 1712bc94-9789-4507-8521-bde1be51e331
description: El elemento IsPrivate indica si el elemento de calendario es privado.
ms.openlocfilehash: 37c0357b3eab2314ee74e1c98287b3dc05a3bf26
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836095"
---
# <a name="isprivate"></a><span data-ttu-id="45fa0-103">IsPrivate</span><span class="sxs-lookup"><span data-stu-id="45fa0-103">IsPrivate</span></span>

<span data-ttu-id="45fa0-104">El elemento **IsPrivate** indica si el elemento de calendario es privado.</span><span class="sxs-lookup"><span data-stu-id="45fa0-104">The **IsPrivate** element indicates whether the calendar item is private.</span></span> 
  
[<span data-ttu-id="45fa0-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="45fa0-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="45fa0-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="45fa0-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="45fa0-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="45fa0-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="45fa0-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="45fa0-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="45fa0-109">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="45fa0-109">CalendarEventArray</span></span>](calendareventarray.md)
  
[<span data-ttu-id="45fa0-110">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="45fa0-110">CalendarEvent</span></span>](calendarevent.md)
  
[<span data-ttu-id="45fa0-111">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="45fa0-111">CalendarEventDetails</span></span>](calendareventdetails.md)
  
[<span data-ttu-id="45fa0-112">IsPrivate</span><span class="sxs-lookup"><span data-stu-id="45fa0-112">IsPrivate</span></span>](isprivate.md)
  
```xml
<IsPrivate>true or false</IsPrivate>
```

 <span data-ttu-id="45fa0-113">**boolean**</span><span class="sxs-lookup"><span data-stu-id="45fa0-113">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="45fa0-114">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="45fa0-114">Attributes and elements</span></span>

<span data-ttu-id="45fa0-115">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="45fa0-115">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="45fa0-116">Atributos</span><span class="sxs-lookup"><span data-stu-id="45fa0-116">Attributes</span></span>

<span data-ttu-id="45fa0-117">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="45fa0-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="45fa0-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="45fa0-118">Child elements</span></span>

<span data-ttu-id="45fa0-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="45fa0-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="45fa0-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="45fa0-120">Parent elements</span></span>

|<span data-ttu-id="45fa0-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="45fa0-121">**Element**</span></span>|<span data-ttu-id="45fa0-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="45fa0-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="45fa0-123">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="45fa0-123">CalendarEventDetails</span></span>](calendareventdetails.md) <br/> |<span data-ttu-id="45fa0-124">Proporciona información adicional acerca de un evento de calendario.</span><span class="sxs-lookup"><span data-stu-id="45fa0-124">Provides additional information about a calendar event.</span></span>  <br/> <span data-ttu-id="45fa0-125">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="45fa0-125">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]/CalendarEventDetails` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="45fa0-126">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="45fa0-126">Text value</span></span>

<span data-ttu-id="45fa0-127">Se requiere un valor de texto que representa un valor de tipo Boolean.</span><span class="sxs-lookup"><span data-stu-id="45fa0-127">A text value that represents a Boolean value is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="45fa0-128">Notas</span><span class="sxs-lookup"><span data-stu-id="45fa0-128">Remarks</span></span>

<span data-ttu-id="45fa0-129">Si se usa este elemento, los demás elementos en el elemento [CalendarEventDetails](calendareventdetails.md) no se incluirá en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="45fa0-129">If this element is used, the other elements in the [CalendarEventDetails](calendareventdetails.md) element will not be included in the response.</span></span> 
  
<span data-ttu-id="45fa0-130">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="45fa0-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="45fa0-131">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="45fa0-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="45fa0-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="45fa0-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="45fa0-133">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="45fa0-133">Schema Name</span></span>  <br/> |<span data-ttu-id="45fa0-134">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="45fa0-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="45fa0-135">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="45fa0-135">Validation File</span></span>  <br/> |<span data-ttu-id="45fa0-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="45fa0-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="45fa0-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="45fa0-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="45fa0-138">False</span><span class="sxs-lookup"><span data-stu-id="45fa0-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="45fa0-139">Ver también</span><span class="sxs-lookup"><span data-stu-id="45fa0-139">See also</span></span>



[<span data-ttu-id="45fa0-140">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="45fa0-140">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="45fa0-141">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="45fa0-141">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="45fa0-142">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="45fa0-142">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

