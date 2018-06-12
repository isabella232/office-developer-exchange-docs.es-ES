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
description: El elemento WorkingPeriodArray contiene información del período para el usuario del buzón de trabajar.
ms.openlocfilehash: 02712f05dc3373a532d769f476341b78ad25a79c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19841019"
---
# <a name="workingperiodarray"></a><span data-ttu-id="3aae9-103">WorkingPeriodArray</span><span class="sxs-lookup"><span data-stu-id="3aae9-103">WorkingPeriodArray</span></span>

<span data-ttu-id="3aae9-104">El elemento **WorkingPeriodArray** contiene información del período para el usuario del buzón de trabajar.</span><span class="sxs-lookup"><span data-stu-id="3aae9-104">The **WorkingPeriodArray** element contains working period information for the mailbox user.</span></span> 
  
[<span data-ttu-id="3aae9-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="3aae9-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="3aae9-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="3aae9-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="3aae9-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="3aae9-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="3aae9-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="3aae9-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="3aae9-109">WorkingHours</span><span class="sxs-lookup"><span data-stu-id="3aae9-109">WorkingHours</span></span>](workinghours-ex15websvcsotherref.md)
  
[<span data-ttu-id="3aae9-110">WorkingPeriodArray</span><span class="sxs-lookup"><span data-stu-id="3aae9-110">WorkingPeriodArray</span></span>](workingperiodarray.md)
  
```xml
<WorkingPeriodArray>
   <WorkingPeriod>...</WorkingPeriod>
</WorkingPeriodArray>
```

 <span data-ttu-id="3aae9-111">**ArrayOfWorkingPeriod**</span><span class="sxs-lookup"><span data-stu-id="3aae9-111">**ArrayOfWorkingPeriod**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3aae9-112">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3aae9-112">Attributes and elements</span></span>

<span data-ttu-id="3aae9-113">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3aae9-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3aae9-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="3aae9-114">Attributes</span></span>

<span data-ttu-id="3aae9-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3aae9-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3aae9-116">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3aae9-116">Child elements</span></span>

|<span data-ttu-id="3aae9-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="3aae9-117">**Element**</span></span>|<span data-ttu-id="3aae9-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3aae9-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3aae9-119">WorkingPeriod</span><span class="sxs-lookup"><span data-stu-id="3aae9-119">WorkingPeriod</span></span>](workingperiod.md) <br/> |<span data-ttu-id="3aae9-120">Contiene la semana laboral días y las horas del usuario de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="3aae9-120">Contains the work week days and hours of the mailbox user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3aae9-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3aae9-121">Parent elements</span></span>

|<span data-ttu-id="3aae9-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="3aae9-122">**Element**</span></span>|<span data-ttu-id="3aae9-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3aae9-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3aae9-124">WorkingHours</span><span class="sxs-lookup"><span data-stu-id="3aae9-124">WorkingHours</span></span>](workinghours-ex15websvcsotherref.md) <br/> |<span data-ttu-id="3aae9-125">Representa la configuración de zona horaria y horario laboral para el usuario del buzón solicitado.</span><span class="sxs-lookup"><span data-stu-id="3aae9-125">Represents the time zone settings and working hours for the requested mailbox user.</span></span>  <br/> <span data-ttu-id="3aae9-126">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="3aae9-126">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3aae9-127">Notas</span><span class="sxs-lookup"><span data-stu-id="3aae9-127">Remarks</span></span>

<span data-ttu-id="3aae9-128">Este elemento es necesario si se usa el elemento [WorkingHours](workinghours-ex15websvcsotherref.md) .</span><span class="sxs-lookup"><span data-stu-id="3aae9-128">This element is required if the [WorkingHours](workinghours-ex15websvcsotherref.md) element is used.</span></span> <span data-ttu-id="3aae9-129">Todos los elementos secundarios se enumeran en la secuencia en la que se producen.</span><span class="sxs-lookup"><span data-stu-id="3aae9-129">All the child elements are listed in the sequence in which they occur.</span></span> 
  
<span data-ttu-id="3aae9-130">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="3aae9-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3aae9-131">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3aae9-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3aae9-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3aae9-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3aae9-133">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3aae9-133">Schema Name</span></span>  <br/> |<span data-ttu-id="3aae9-134">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="3aae9-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="3aae9-135">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3aae9-135">Validation File</span></span>  <br/> |<span data-ttu-id="3aae9-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3aae9-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3aae9-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3aae9-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="3aae9-138">False</span><span class="sxs-lookup"><span data-stu-id="3aae9-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3aae9-139">Ver también</span><span class="sxs-lookup"><span data-stu-id="3aae9-139">See also</span></span>



[<span data-ttu-id="3aae9-140">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="3aae9-140">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="3aae9-141">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="3aae9-141">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="3aae9-142">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="3aae9-142">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

