---
title: AppointmentState
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AppointmentState
api_type:
- schema
ms.assetid: ab3f5d04-ace1-4a15-9107-cefa6c41abc7
description: El elemento AppointmentState especifica el estado de la cita.
ms.openlocfilehash: 05e92a3fea10a84518b0680c425011a91bc43d93
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763538"
---
# <a name="appointmentstate"></a><span data-ttu-id="c652e-103">AppointmentState</span><span class="sxs-lookup"><span data-stu-id="c652e-103">AppointmentState</span></span>

<span data-ttu-id="c652e-104">El elemento **AppointmentState** especifica el estado de la cita.</span><span class="sxs-lookup"><span data-stu-id="c652e-104">The **AppointmentState** element specifies the status of the appointment.</span></span> 
  
```XML
<AppointmentState/>
```

 <span data-ttu-id="c652e-105">**int**</span><span class="sxs-lookup"><span data-stu-id="c652e-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c652e-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c652e-106">Attributes and elements</span></span>

<span data-ttu-id="c652e-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c652e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c652e-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c652e-108">Attributes</span></span>

<span data-ttu-id="c652e-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c652e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c652e-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c652e-110">Child elements</span></span>

<span data-ttu-id="c652e-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c652e-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c652e-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c652e-112">Parent elements</span></span>

|<span data-ttu-id="c652e-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="c652e-113">**Element**</span></span>|<span data-ttu-id="c652e-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c652e-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c652e-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="c652e-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="c652e-116">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c652e-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="c652e-117">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="c652e-117">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="c652e-118">Representa una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c652e-118">Represents a meeting in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c652e-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="c652e-119">Text value</span></span>

<span data-ttu-id="c652e-120">Este elemento contiene un valor de texto que representa el conjunto de bits.</span><span class="sxs-lookup"><span data-stu-id="c652e-120">This element contains a text value that represents set bits.</span></span> <span data-ttu-id="c652e-121">Esto está en formato de número entero.</span><span class="sxs-lookup"><span data-stu-id="c652e-121">This is in integer form.</span></span> <span data-ttu-id="c652e-122">Este elemento es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="c652e-122">This element is read-only.</span></span> <span data-ttu-id="c652e-123">Sólo se devolverán en una respuesta.</span><span class="sxs-lookup"><span data-stu-id="c652e-123">It will only be returned in a response.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c652e-124">Notas</span><span class="sxs-lookup"><span data-stu-id="c652e-124">Remarks</span></span>

<span data-ttu-id="c652e-125">El valor de número entero que se devuelve representa la máscara de bits de estado de una cita.</span><span class="sxs-lookup"><span data-stu-id="c652e-125">The integer value that is returned represents the appointment state bitmask.</span></span> <span data-ttu-id="c652e-126">En la siguiente tabla se describe cada bit.</span><span class="sxs-lookup"><span data-stu-id="c652e-126">The following table describes each bit.</span></span>
  
|<span data-ttu-id="c652e-127">**Name**</span><span class="sxs-lookup"><span data-stu-id="c652e-127">**Name**</span></span>|<span data-ttu-id="c652e-128">**Bit**</span><span class="sxs-lookup"><span data-stu-id="c652e-128">**Bit**</span></span>|<span data-ttu-id="c652e-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c652e-129">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c652e-130">None</span><span class="sxs-lookup"><span data-stu-id="c652e-130">None</span></span>  <br/> |<span data-ttu-id="c652e-131">0x0000</span><span class="sxs-lookup"><span data-stu-id="c652e-131">0x0000</span></span>  <br/> |<span data-ttu-id="c652e-132">Se han establecido ningún indicador.</span><span class="sxs-lookup"><span data-stu-id="c652e-132">No flags have been set.</span></span> <span data-ttu-id="c652e-133">Sólo se utiliza para una cita que no incluye a los asistentes.</span><span class="sxs-lookup"><span data-stu-id="c652e-133">This is only used for an appointment that does not include attendees.</span></span>  <br/> |
|<span data-ttu-id="c652e-134">Reunión</span><span class="sxs-lookup"><span data-stu-id="c652e-134">Meeting</span></span>  <br/> |<span data-ttu-id="c652e-135">0 x 0001</span><span class="sxs-lookup"><span data-stu-id="c652e-135">0x0001</span></span>  <br/> |<span data-ttu-id="c652e-136">Esta cita es una reunión.</span><span class="sxs-lookup"><span data-stu-id="c652e-136">This appointment is a meeting.</span></span>  <br/> |
|<span data-ttu-id="c652e-137">Cantidad.Recibida</span><span class="sxs-lookup"><span data-stu-id="c652e-137">Received</span></span>  <br/> |<span data-ttu-id="c652e-138">0x0002</span><span class="sxs-lookup"><span data-stu-id="c652e-138">0x0002</span></span>  <br/> |<span data-ttu-id="c652e-139">Se ha recibido esta cita.</span><span class="sxs-lookup"><span data-stu-id="c652e-139">This appointment has been received.</span></span>  <br/> |
|<span data-ttu-id="c652e-140">Cancelado</span><span class="sxs-lookup"><span data-stu-id="c652e-140">Canceled</span></span>  <br/> |<span data-ttu-id="c652e-141">0x0004</span><span class="sxs-lookup"><span data-stu-id="c652e-141">0x0004</span></span>  <br/> |<span data-ttu-id="c652e-142">Se ha cancelado esta cita.</span><span class="sxs-lookup"><span data-stu-id="c652e-142">This appointment has been canceled.</span></span>  <br/> |
   
<span data-ttu-id="c652e-143">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="c652e-143">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c652e-144">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c652e-144">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c652e-145">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c652e-145">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c652e-146">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c652e-146">Schema name</span></span>  <br/> |<span data-ttu-id="c652e-147">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="c652e-147">Types schema</span></span>  <br/> |
|<span data-ttu-id="c652e-148">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c652e-148">Validation file</span></span>  <br/> |<span data-ttu-id="c652e-149">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c652e-149">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c652e-150">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c652e-150">Can be empty</span></span>  <br/> |<span data-ttu-id="c652e-151">False</span><span class="sxs-lookup"><span data-stu-id="c652e-151">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c652e-152">Ver también</span><span class="sxs-lookup"><span data-stu-id="c652e-152">See also</span></span>

- [<span data-ttu-id="c652e-153">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="c652e-153">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

