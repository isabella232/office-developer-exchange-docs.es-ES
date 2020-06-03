---
title: WorkingPeriodArray
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- WorkingPeriodArray
api_type:
- schema
ms.assetid: 3a3f6393-eacc-4734-b6c9-b67023fe2830
description: El elemento WorkingPeriodArray contiene la información del período de trabajo para el usuario del buzón.
ms.openlocfilehash: a9ca55866a574c5208d8561fca6daf417867fef6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465201"
---
# <a name="workingperiodarray"></a><span data-ttu-id="9bb7d-103">WorkingPeriodArray</span><span class="sxs-lookup"><span data-stu-id="9bb7d-103">WorkingPeriodArray</span></span>

<span data-ttu-id="9bb7d-104">El elemento **WorkingPeriodArray** contiene la información del período de trabajo para el usuario del buzón.</span><span class="sxs-lookup"><span data-stu-id="9bb7d-104">The **WorkingPeriodArray** element contains working period information for the mailbox user.</span></span> 
  
[<span data-ttu-id="9bb7d-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="9bb7d-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="9bb7d-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="9bb7d-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="9bb7d-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="9bb7d-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="9bb7d-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="9bb7d-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="9bb7d-109">WorkingHours</span><span class="sxs-lookup"><span data-stu-id="9bb7d-109">WorkingHours</span></span>](workinghours-ex15websvcsotherref.md)
  
[<span data-ttu-id="9bb7d-110">WorkingPeriodArray</span><span class="sxs-lookup"><span data-stu-id="9bb7d-110">WorkingPeriodArray</span></span>](workingperiodarray.md)
  
```xml
<WorkingPeriodArray>
   <WorkingPeriod>...</WorkingPeriod>
</WorkingPeriodArray>
```

 <span data-ttu-id="9bb7d-111">**ArrayOfWorkingPeriod**</span><span class="sxs-lookup"><span data-stu-id="9bb7d-111">**ArrayOfWorkingPeriod**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9bb7d-112">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="9bb7d-112">Attributes and elements</span></span>

<span data-ttu-id="9bb7d-113">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="9bb7d-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9bb7d-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="9bb7d-114">Attributes</span></span>

<span data-ttu-id="9bb7d-115">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="9bb7d-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9bb7d-116">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9bb7d-116">Child elements</span></span>

|<span data-ttu-id="9bb7d-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9bb7d-117">**Element**</span></span>|<span data-ttu-id="9bb7d-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9bb7d-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9bb7d-119">WorkingPeriod</span><span class="sxs-lookup"><span data-stu-id="9bb7d-119">WorkingPeriod</span></span>](workingperiod.md) <br/> |<span data-ttu-id="9bb7d-120">Contiene la semana laboral días y horas del usuario del buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="9bb7d-120">Contains the work week days and hours of the mailbox user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9bb7d-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="9bb7d-121">Parent elements</span></span>

|<span data-ttu-id="9bb7d-122">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9bb7d-122">**Element**</span></span>|<span data-ttu-id="9bb7d-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9bb7d-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9bb7d-124">WorkingHours</span><span class="sxs-lookup"><span data-stu-id="9bb7d-124">WorkingHours</span></span>](workinghours-ex15websvcsotherref.md) <br/> |<span data-ttu-id="9bb7d-125">Representa la configuración de la zona horaria y el horario laboral del usuario del buzón solicitado.</span><span class="sxs-lookup"><span data-stu-id="9bb7d-125">Represents the time zone settings and working hours for the requested mailbox user.</span></span>  <br/> <span data-ttu-id="9bb7d-126">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="9bb7d-126">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9bb7d-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9bb7d-127">Remarks</span></span>

<span data-ttu-id="9bb7d-128">Este elemento es obligatorio si se usa el elemento [WorkingHours](workinghours-ex15websvcsotherref.md) .</span><span class="sxs-lookup"><span data-stu-id="9bb7d-128">This element is required if the [WorkingHours](workinghours-ex15websvcsotherref.md) element is used.</span></span> <span data-ttu-id="9bb7d-129">Todos los elementos secundarios se enumeran en la secuencia en que se producen.</span><span class="sxs-lookup"><span data-stu-id="9bb7d-129">All the child elements are listed in the sequence in which they occur.</span></span> 
  
<span data-ttu-id="9bb7d-130">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="9bb7d-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9bb7d-131">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="9bb7d-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9bb7d-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="9bb7d-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9bb7d-133">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="9bb7d-133">Schema Name</span></span>  <br/> |<span data-ttu-id="9bb7d-134">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="9bb7d-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="9bb7d-135">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="9bb7d-135">Validation File</span></span>  <br/> |<span data-ttu-id="9bb7d-136">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="9bb7d-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9bb7d-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="9bb7d-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="9bb7d-138">Falso</span><span class="sxs-lookup"><span data-stu-id="9bb7d-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9bb7d-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="9bb7d-139">See also</span></span>



[<span data-ttu-id="9bb7d-140">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="9bb7d-140">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="9bb7d-141">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="9bb7d-141">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="9bb7d-142">Obtener disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="9bb7d-142">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

