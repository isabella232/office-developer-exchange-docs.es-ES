---
title: FreeBusyView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FreeBusyView
api_type:
- schema
ms.assetid: cb18434f-5f41-4e05-a5ce-d921b2721a8c
description: El elemento FreeBusyView contiene información de disponibilidad de un usuario específico.
ms.openlocfilehash: e5cc3bea6b57d5c400dd9be44bf9f9aaf9e43eb9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456104"
---
# <a name="freebusyview"></a><span data-ttu-id="ff594-103">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="ff594-103">FreeBusyView</span></span>

<span data-ttu-id="ff594-104">El elemento **FreeBusyView** contiene información de disponibilidad de un usuario específico.</span><span class="sxs-lookup"><span data-stu-id="ff594-104">The **FreeBusyView** element contains availability information for a specific user.</span></span> 
  
[<span data-ttu-id="ff594-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="ff594-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="ff594-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="ff594-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="ff594-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="ff594-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="ff594-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="ff594-108">FreeBusyView</span></span>](freebusyview.md)
  
```xml
<FreeBusyView>
   <FreeBusyViewType>...</FreeBusyViewType>
   <MergedFreeBusy>...</MergedFreeBusy>
   <CalendarEventArray>...</CalendarEventArray>
   <WorkingHours>...</WorkingHours>
</FreeBusyView>
```

 <span data-ttu-id="ff594-109">**FreeBusyView**</span><span class="sxs-lookup"><span data-stu-id="ff594-109">**FreeBusyView**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ff594-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ff594-110">Attributes and elements</span></span>

<span data-ttu-id="ff594-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ff594-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ff594-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="ff594-112">Attributes</span></span>

<span data-ttu-id="ff594-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="ff594-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ff594-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ff594-114">Child elements</span></span>

|<span data-ttu-id="ff594-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ff594-115">**Element**</span></span>|<span data-ttu-id="ff594-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ff594-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ff594-117">FreeBusyViewType</span><span class="sxs-lookup"><span data-stu-id="ff594-117">FreeBusyViewType</span></span>](freebusyviewtype.md) <br/> |<span data-ttu-id="ff594-118">Representa el tipo de información de disponibilidad solicitada devuelta en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ff594-118">Represents the type of requested free/busy information returned in the response.</span></span>  <br/> |
|[<span data-ttu-id="ff594-119">MergedFreeBusy</span><span class="sxs-lookup"><span data-stu-id="ff594-119">MergedFreeBusy</span></span>](mergedfreebusy.md) <br/> |<span data-ttu-id="ff594-120">Contiene la secuencia de datos de disponibilidad combinada.</span><span class="sxs-lookup"><span data-stu-id="ff594-120">Contains the merged free/busy stream of data.</span></span>  <br/> |
|[<span data-ttu-id="ff594-121">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="ff594-121">CalendarEventArray</span></span>](calendareventarray.md) <br/> |<span data-ttu-id="ff594-122">Contiene un conjunto de ocurrencias de elemento de calendario únicas que representan la disponibilidad del usuario solicitado.</span><span class="sxs-lookup"><span data-stu-id="ff594-122">Contains a set of unique calendar item occurrences that represent the requested user's availability.</span></span>  <br/> |
|[<span data-ttu-id="ff594-123">WorkingHours</span><span class="sxs-lookup"><span data-stu-id="ff594-123">WorkingHours</span></span>](workinghours-ex15websvcsotherref.md) <br/> |<span data-ttu-id="ff594-124">Representa la configuración de la zona horaria y el horario laboral del usuario del buzón solicitado.</span><span class="sxs-lookup"><span data-stu-id="ff594-124">Represents the time zone settings and working hours for the requested mailbox user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ff594-125">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ff594-125">Parent elements</span></span>

|<span data-ttu-id="ff594-126">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ff594-126">**Element**</span></span>|<span data-ttu-id="ff594-127">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ff594-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ff594-128">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="ff594-128">FreeBusyResponse</span></span>](freebusyresponse.md) <br/> |<span data-ttu-id="ff594-129">Contiene la información de disponibilidad de un único usuario de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="ff594-129">Contains the free/busy information for a single mailbox user.</span></span>  <br/> <span data-ttu-id="ff594-130">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="ff594-130">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ff594-131">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ff594-131">Remarks</span></span>

<span data-ttu-id="ff594-132">Todos los elementos secundarios se enumeran en la secuencia en que se producen.</span><span class="sxs-lookup"><span data-stu-id="ff594-132">All the child elements are listed in the sequence in which they occur.</span></span> <span data-ttu-id="ff594-133">El nivel de detalle proporcionado por este elemento depende de los permisos concedidos al solicitante.</span><span class="sxs-lookup"><span data-stu-id="ff594-133">The level of detail provided by this element depends on the permissions granted to the requestor.</span></span>
  
<span data-ttu-id="ff594-134">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="ff594-134">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ff594-135">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ff594-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ff594-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="ff594-136">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ff594-137">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ff594-137">Schema Name</span></span>  <br/> |<span data-ttu-id="ff594-138">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="ff594-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="ff594-139">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ff594-139">Validation File</span></span>  <br/> |<span data-ttu-id="ff594-140">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="ff594-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ff594-141">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ff594-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="ff594-142">Falso</span><span class="sxs-lookup"><span data-stu-id="ff594-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ff594-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="ff594-143">See also</span></span>



[<span data-ttu-id="ff594-144">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="ff594-144">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="ff594-145">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="ff594-145">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="ff594-146">Obtener disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="ff594-146">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

