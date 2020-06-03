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
ms.openlocfilehash: c36c659414700439436cd2ca903e443164c1473b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457805"
---
# <a name="isprivate"></a><span data-ttu-id="11bb9-103">IsPrivate</span><span class="sxs-lookup"><span data-stu-id="11bb9-103">IsPrivate</span></span>

<span data-ttu-id="11bb9-104">El elemento **IsPrivate** indica si el elemento de calendario es privado.</span><span class="sxs-lookup"><span data-stu-id="11bb9-104">The **IsPrivate** element indicates whether the calendar item is private.</span></span> 
  
[<span data-ttu-id="11bb9-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="11bb9-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="11bb9-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="11bb9-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="11bb9-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="11bb9-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="11bb9-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="11bb9-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="11bb9-109">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="11bb9-109">CalendarEventArray</span></span>](calendareventarray.md)
  
[<span data-ttu-id="11bb9-110">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="11bb9-110">CalendarEvent</span></span>](calendarevent.md)
  
[<span data-ttu-id="11bb9-111">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="11bb9-111">CalendarEventDetails</span></span>](calendareventdetails.md)
  
[<span data-ttu-id="11bb9-112">IsPrivate</span><span class="sxs-lookup"><span data-stu-id="11bb9-112">IsPrivate</span></span>](isprivate.md)
  
```xml
<IsPrivate>true or false</IsPrivate>
```

 <span data-ttu-id="11bb9-113">**boolean**</span><span class="sxs-lookup"><span data-stu-id="11bb9-113">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="11bb9-114">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="11bb9-114">Attributes and elements</span></span>

<span data-ttu-id="11bb9-115">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="11bb9-115">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="11bb9-116">Atributos</span><span class="sxs-lookup"><span data-stu-id="11bb9-116">Attributes</span></span>

<span data-ttu-id="11bb9-117">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="11bb9-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="11bb9-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="11bb9-118">Child elements</span></span>

<span data-ttu-id="11bb9-119">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="11bb9-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="11bb9-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="11bb9-120">Parent elements</span></span>

|<span data-ttu-id="11bb9-121">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="11bb9-121">**Element**</span></span>|<span data-ttu-id="11bb9-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="11bb9-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="11bb9-123">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="11bb9-123">CalendarEventDetails</span></span>](calendareventdetails.md) <br/> |<span data-ttu-id="11bb9-124">Proporciona información adicional acerca de un evento de calendario.</span><span class="sxs-lookup"><span data-stu-id="11bb9-124">Provides additional information about a calendar event.</span></span>  <br/> <span data-ttu-id="11bb9-125">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="11bb9-125">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]/CalendarEventDetails` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="11bb9-126">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="11bb9-126">Text value</span></span>

<span data-ttu-id="11bb9-127">Se requiere un valor de texto que representa un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="11bb9-127">A text value that represents a Boolean value is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="11bb9-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="11bb9-128">Remarks</span></span>

<span data-ttu-id="11bb9-129">Si se usa este elemento, los demás elementos del elemento [CalendarEventDetails](calendareventdetails.md) no se incluirán en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="11bb9-129">If this element is used, the other elements in the [CalendarEventDetails](calendareventdetails.md) element will not be included in the response.</span></span> 
  
<span data-ttu-id="11bb9-130">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="11bb9-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="11bb9-131">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="11bb9-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="11bb9-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="11bb9-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="11bb9-133">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="11bb9-133">Schema Name</span></span>  <br/> |<span data-ttu-id="11bb9-134">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="11bb9-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="11bb9-135">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="11bb9-135">Validation File</span></span>  <br/> |<span data-ttu-id="11bb9-136">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="11bb9-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="11bb9-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="11bb9-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="11bb9-138">Falso</span><span class="sxs-lookup"><span data-stu-id="11bb9-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="11bb9-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="11bb9-139">See also</span></span>



[<span data-ttu-id="11bb9-140">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="11bb9-140">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="11bb9-141">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="11bb9-141">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="11bb9-142">Obtener disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="11bb9-142">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

