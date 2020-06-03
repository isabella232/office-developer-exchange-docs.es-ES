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
ms.openlocfilehash: 8b0e827d02e9051f31d43199503dc286c50e2125
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463478"
---
# <a name="appointmentstate"></a><span data-ttu-id="eec96-103">AppointmentState</span><span class="sxs-lookup"><span data-stu-id="eec96-103">AppointmentState</span></span>

<span data-ttu-id="eec96-104">El elemento **AppointmentState** especifica el estado de la cita.</span><span class="sxs-lookup"><span data-stu-id="eec96-104">The **AppointmentState** element specifies the status of the appointment.</span></span> 
  
```XML
<AppointmentState/>
```

 <span data-ttu-id="eec96-105">**int**</span><span class="sxs-lookup"><span data-stu-id="eec96-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="eec96-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="eec96-106">Attributes and elements</span></span>

<span data-ttu-id="eec96-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="eec96-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="eec96-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="eec96-108">Attributes</span></span>

<span data-ttu-id="eec96-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="eec96-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="eec96-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="eec96-110">Child elements</span></span>

<span data-ttu-id="eec96-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="eec96-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="eec96-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="eec96-112">Parent elements</span></span>

|<span data-ttu-id="eec96-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="eec96-113">**Element**</span></span>|<span data-ttu-id="eec96-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="eec96-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="eec96-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="eec96-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="eec96-116">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="eec96-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="eec96-117">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="eec96-117">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="eec96-118">Representa una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="eec96-118">Represents a meeting in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="eec96-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="eec96-119">Text value</span></span>

<span data-ttu-id="eec96-120">Este elemento contiene un valor de texto que representa los bits establecidos.</span><span class="sxs-lookup"><span data-stu-id="eec96-120">This element contains a text value that represents set bits.</span></span> <span data-ttu-id="eec96-121">Se encuentra en un formato entero.</span><span class="sxs-lookup"><span data-stu-id="eec96-121">This is in integer form.</span></span> <span data-ttu-id="eec96-122">Este elemento es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="eec96-122">This element is read-only.</span></span> <span data-ttu-id="eec96-123">Solo se devolverá en una respuesta.</span><span class="sxs-lookup"><span data-stu-id="eec96-123">It will only be returned in a response.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="eec96-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="eec96-124">Remarks</span></span>

<span data-ttu-id="eec96-125">El valor entero que se devuelve representa la máscara de la máscara de estado de cita.</span><span class="sxs-lookup"><span data-stu-id="eec96-125">The integer value that is returned represents the appointment state bitmask.</span></span> <span data-ttu-id="eec96-126">En la tabla siguiente se describe cada bit.</span><span class="sxs-lookup"><span data-stu-id="eec96-126">The following table describes each bit.</span></span>
  
|<span data-ttu-id="eec96-127">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="eec96-127">**Name**</span></span>|<span data-ttu-id="eec96-128">**Bit**</span><span class="sxs-lookup"><span data-stu-id="eec96-128">**Bit**</span></span>|<span data-ttu-id="eec96-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="eec96-129">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="eec96-130">Ninguno</span><span class="sxs-lookup"><span data-stu-id="eec96-130">None</span></span>  <br/> |<span data-ttu-id="eec96-131">0x0000</span><span class="sxs-lookup"><span data-stu-id="eec96-131">0x0000</span></span>  <br/> |<span data-ttu-id="eec96-132">No se ha establecido ningún marcador.</span><span class="sxs-lookup"><span data-stu-id="eec96-132">No flags have been set.</span></span> <span data-ttu-id="eec96-133">Solo se usa para una cita que no incluye a los asistentes.</span><span class="sxs-lookup"><span data-stu-id="eec96-133">This is only used for an appointment that does not include attendees.</span></span>  <br/> |
|<span data-ttu-id="eec96-134">Misma</span><span class="sxs-lookup"><span data-stu-id="eec96-134">Meeting</span></span>  <br/> |<span data-ttu-id="eec96-135">0x0001</span><span class="sxs-lookup"><span data-stu-id="eec96-135">0x0001</span></span>  <br/> |<span data-ttu-id="eec96-136">Esta cita es una reunión.</span><span class="sxs-lookup"><span data-stu-id="eec96-136">This appointment is a meeting.</span></span>  <br/> |
|<span data-ttu-id="eec96-137">Cantidad.Recibida</span><span class="sxs-lookup"><span data-stu-id="eec96-137">Received</span></span>  <br/> |<span data-ttu-id="eec96-138">0x0002</span><span class="sxs-lookup"><span data-stu-id="eec96-138">0x0002</span></span>  <br/> |<span data-ttu-id="eec96-139">Esta cita se ha recibido.</span><span class="sxs-lookup"><span data-stu-id="eec96-139">This appointment has been received.</span></span>  <br/> |
|<span data-ttu-id="eec96-140">Cancelado</span><span class="sxs-lookup"><span data-stu-id="eec96-140">Canceled</span></span>  <br/> |<span data-ttu-id="eec96-141">0x0004</span><span class="sxs-lookup"><span data-stu-id="eec96-141">0x0004</span></span>  <br/> |<span data-ttu-id="eec96-142">Esta cita se ha cancelado.</span><span class="sxs-lookup"><span data-stu-id="eec96-142">This appointment has been canceled.</span></span>  <br/> |
   
<span data-ttu-id="eec96-143">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="eec96-143">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="eec96-144">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="eec96-144">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="eec96-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="eec96-145">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="eec96-146">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="eec96-146">Schema name</span></span>  <br/> |<span data-ttu-id="eec96-147">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="eec96-147">Types schema</span></span>  <br/> |
|<span data-ttu-id="eec96-148">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="eec96-148">Validation file</span></span>  <br/> |<span data-ttu-id="eec96-149">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="eec96-149">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="eec96-150">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="eec96-150">Can be empty</span></span>  <br/> |<span data-ttu-id="eec96-151">Falso</span><span class="sxs-lookup"><span data-stu-id="eec96-151">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="eec96-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="eec96-152">See also</span></span>

- [<span data-ttu-id="eec96-153">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="eec96-153">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

