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
description: El elemento IsException indica si una instancia de un elemento de calendario periódico se cambia desde el patrón.
ms.openlocfilehash: f2e45e0f1010449d4a494f5e15ecd0b22dc598e4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457588"
---
# <a name="isexception"></a><span data-ttu-id="899e1-103">IsException</span><span class="sxs-lookup"><span data-stu-id="899e1-103">IsException</span></span>

<span data-ttu-id="899e1-104">El elemento **IsException** indica si una instancia de un elemento de calendario periódico se cambia desde el patrón.</span><span class="sxs-lookup"><span data-stu-id="899e1-104">The **IsException** element indicates whether an instance of a recurring calendar item is changed from the master.</span></span> 
  
[<span data-ttu-id="899e1-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="899e1-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="899e1-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="899e1-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="899e1-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="899e1-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="899e1-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="899e1-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="899e1-109">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="899e1-109">CalendarEventArray</span></span>](calendareventarray.md)
  
[<span data-ttu-id="899e1-110">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="899e1-110">CalendarEvent</span></span>](calendarevent.md)
  
[<span data-ttu-id="899e1-111">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="899e1-111">CalendarEventDetails</span></span>](calendareventdetails.md)
  
[<span data-ttu-id="899e1-112">IsException</span><span class="sxs-lookup"><span data-stu-id="899e1-112">IsException</span></span>](isexception.md)
  
```xml
<IsException/>
```

 <span data-ttu-id="899e1-113">**boolean**</span><span class="sxs-lookup"><span data-stu-id="899e1-113">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="899e1-114">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="899e1-114">Attributes and elements</span></span>

<span data-ttu-id="899e1-115">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="899e1-115">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="899e1-116">Atributos</span><span class="sxs-lookup"><span data-stu-id="899e1-116">Attributes</span></span>

<span data-ttu-id="899e1-117">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="899e1-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="899e1-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="899e1-118">Child elements</span></span>

<span data-ttu-id="899e1-119">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="899e1-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="899e1-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="899e1-120">Parent elements</span></span>

|<span data-ttu-id="899e1-121">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="899e1-121">**Element**</span></span>|<span data-ttu-id="899e1-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="899e1-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="899e1-123">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="899e1-123">CalendarEventDetails</span></span>](calendareventdetails.md) <br/> |<span data-ttu-id="899e1-124">Proporciona información adicional acerca de un evento de calendario.</span><span class="sxs-lookup"><span data-stu-id="899e1-124">Provides additional information about a calendar event.</span></span>  <br/> <span data-ttu-id="899e1-125">La siguiente es la expresión XPath 2,0 a este elemento:</span><span class="sxs-lookup"><span data-stu-id="899e1-125">The following is the XPath 2.0 expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]/CalendarEventDetails` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="899e1-126">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="899e1-126">Text value</span></span>

<span data-ttu-id="899e1-127">Es necesario un valor de texto si este elemento se devuelve en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="899e1-127">A text value is required if this element is returned in the response.</span></span> <span data-ttu-id="899e1-128">Este elemento es obligatorio si se usa el elemento [CalendarEventDetails](calendareventdetails.md) .</span><span class="sxs-lookup"><span data-stu-id="899e1-128">This element is required if the [CalendarEventDetails](calendareventdetails.md) element is used.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="899e1-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="899e1-129">Remarks</span></span>

<span data-ttu-id="899e1-130">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="899e1-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="899e1-131">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="899e1-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="899e1-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="899e1-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="899e1-133">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="899e1-133">Schema Name</span></span>  <br/> |<span data-ttu-id="899e1-134">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="899e1-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="899e1-135">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="899e1-135">Validation File</span></span>  <br/> |<span data-ttu-id="899e1-136">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="899e1-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="899e1-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="899e1-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="899e1-138">Falso</span><span class="sxs-lookup"><span data-stu-id="899e1-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="899e1-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="899e1-139">See also</span></span>



[<span data-ttu-id="899e1-140">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="899e1-140">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="899e1-141">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="899e1-141">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="899e1-142">Obtener disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="899e1-142">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

