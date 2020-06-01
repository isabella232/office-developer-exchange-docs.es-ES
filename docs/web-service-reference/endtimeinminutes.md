---
title: EndTimeInMinutes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- EndTimeInMinutes
api_type:
- schema
ms.assetid: ef05bdda-7a66-44db-bb73-a2ce8316c257
description: El elemento EndTimeInMinutes representa el final del día laborable de un usuario de buzón de correo.
ms.openlocfilehash: cb564f9de944848734749a30c813a94d6b5c4187
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459654"
---
# <a name="endtimeinminutes"></a><span data-ttu-id="98326-103">EndTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="98326-103">EndTimeInMinutes</span></span>

<span data-ttu-id="98326-104">El elemento **EndTimeInMinutes** representa el final del día laborable de un usuario de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="98326-104">The **EndTimeInMinutes** element represents the end of the working day for a mailbox user.</span></span> 
  
[<span data-ttu-id="98326-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="98326-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="98326-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="98326-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="98326-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="98326-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="98326-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="98326-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="98326-109">WorkingHours</span><span class="sxs-lookup"><span data-stu-id="98326-109">WorkingHours</span></span>](workinghours-ex15websvcsotherref.md)
  
[<span data-ttu-id="98326-110">WorkingPeriodArray</span><span class="sxs-lookup"><span data-stu-id="98326-110">WorkingPeriodArray</span></span>](workingperiodarray.md)
  
[<span data-ttu-id="98326-111">WorkingPeriod</span><span class="sxs-lookup"><span data-stu-id="98326-111">WorkingPeriod</span></span>](workingperiod.md)
  
[<span data-ttu-id="98326-112">EndTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="98326-112">EndTimeInMinutes</span></span>](endtimeinminutes.md)
  
```xml
<StartTimeInMinutes>...</StartTimeInMinutes>
```

 <span data-ttu-id="98326-113">**int**</span><span class="sxs-lookup"><span data-stu-id="98326-113">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="98326-114">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="98326-114">Attributes and elements</span></span>

<span data-ttu-id="98326-115">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="98326-115">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="98326-116">Atributos</span><span class="sxs-lookup"><span data-stu-id="98326-116">Attributes</span></span>

<span data-ttu-id="98326-117">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="98326-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="98326-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="98326-118">Child elements</span></span>

<span data-ttu-id="98326-119">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="98326-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="98326-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="98326-120">Parent elements</span></span>

|<span data-ttu-id="98326-121">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="98326-121">**Element**</span></span>|<span data-ttu-id="98326-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="98326-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="98326-123">WorkingPeriod</span><span class="sxs-lookup"><span data-stu-id="98326-123">WorkingPeriod</span></span>](workingperiod.md) <br/> |<span data-ttu-id="98326-124">Contiene la semana laboral días y horas del usuario del buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="98326-124">Contains the work week days and hours of the mailbox user.</span></span>  <br/> <span data-ttu-id="98326-125">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="98326-125">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/WorkingPeriodArray/WorkingPeriod[i]` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="98326-126">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="98326-126">Text value</span></span>

<span data-ttu-id="98326-127">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="98326-127">A text value is required.</span></span> <span data-ttu-id="98326-128">El valor de texto representa el final del día laborable por el número de minutos que han transcurrido desde que comenzó el día.</span><span class="sxs-lookup"><span data-stu-id="98326-128">The text value represents the end of the working day by how many minutes have elapsed since the day began.</span></span> <span data-ttu-id="98326-129">Por ejemplo, una hora de finalización de 6 P.M.</span><span class="sxs-lookup"><span data-stu-id="98326-129">For example, an end time of 6 P.M.</span></span> <span data-ttu-id="98326-130">se representa por 1080 minutos.</span><span class="sxs-lookup"><span data-stu-id="98326-130">is represented by 1080 minutes.</span></span>
  
<span data-ttu-id="98326-131">El intervalo de valores posibles para este elemento es de 0 a 1440.</span><span class="sxs-lookup"><span data-stu-id="98326-131">The range of possible values for this element is 0 to 1440.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="98326-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="98326-132">Remarks</span></span>

<span data-ttu-id="98326-133">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="98326-133">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="98326-134">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="98326-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="98326-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="98326-135">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="98326-136">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="98326-136">Schema Name</span></span>  <br/> |<span data-ttu-id="98326-137">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="98326-137">Types schema</span></span>  <br/> |
|<span data-ttu-id="98326-138">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="98326-138">Validation File</span></span>  <br/> |<span data-ttu-id="98326-139">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="98326-139">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="98326-140">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="98326-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="98326-141">Falso</span><span class="sxs-lookup"><span data-stu-id="98326-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="98326-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="98326-142">See also</span></span>



[<span data-ttu-id="98326-143">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="98326-143">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="98326-144">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="98326-144">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="98326-145">Obtener disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="98326-145">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

