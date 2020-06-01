---
title: AppointmentSequenceNumber
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AppointmentSequenceNumber
api_type:
- schema
ms.assetid: eb4c48bd-f905-48dc-ae16-53a080b9b025
description: El elemento AppointmentSequenceNumber especifica el número de secuencia de una versión de una cita.
ms.openlocfilehash: daeea7a656c59923bcb6f2850539c7869d6eb181
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461663"
---
# <a name="appointmentsequencenumber"></a><span data-ttu-id="edf32-103">AppointmentSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="edf32-103">AppointmentSequenceNumber</span></span>

<span data-ttu-id="edf32-104">El elemento **AppointmentSequenceNumber** especifica el número de secuencia de una versión de una cita.</span><span class="sxs-lookup"><span data-stu-id="edf32-104">The **AppointmentSequenceNumber** element specifies the sequence number of a version of an appointment.</span></span> 
  
```xml
<AppointmentSequenceNumber/>
```

 <span data-ttu-id="edf32-105">**int**</span><span class="sxs-lookup"><span data-stu-id="edf32-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="edf32-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="edf32-106">Attributes and elements</span></span>

<span data-ttu-id="edf32-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="edf32-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="edf32-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="edf32-108">Attributes</span></span>

<span data-ttu-id="edf32-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="edf32-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="edf32-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="edf32-110">Child elements</span></span>

<span data-ttu-id="edf32-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="edf32-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="edf32-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="edf32-112">Parent elements</span></span>

|<span data-ttu-id="edf32-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="edf32-113">**Element**</span></span>|<span data-ttu-id="edf32-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="edf32-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="edf32-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="edf32-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="edf32-116">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="edf32-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="edf32-117">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="edf32-117">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="edf32-118">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="edf32-118">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="edf32-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="edf32-119">Text value</span></span>

<span data-ttu-id="edf32-120">El valor de texto representa un número de versión.</span><span class="sxs-lookup"><span data-stu-id="edf32-120">The text value represents a version number.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="edf32-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="edf32-121">Remarks</span></span>

<span data-ttu-id="edf32-122">Este valor se actualiza cuando la cita se actualiza con nueva información.</span><span class="sxs-lookup"><span data-stu-id="edf32-122">This value is updated when the appointment is updated with new information.</span></span> 
  
<span data-ttu-id="edf32-123">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="edf32-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="edf32-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="edf32-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="edf32-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="edf32-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="edf32-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="edf32-126">Schema Name</span></span>  <br/> |<span data-ttu-id="edf32-127">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="edf32-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="edf32-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="edf32-128">Validation File</span></span>  <br/> |<span data-ttu-id="edf32-129">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="edf32-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="edf32-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="edf32-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="edf32-131">Falso</span><span class="sxs-lookup"><span data-stu-id="edf32-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="edf32-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="edf32-132">See also</span></span>

- [<span data-ttu-id="edf32-133">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="edf32-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

