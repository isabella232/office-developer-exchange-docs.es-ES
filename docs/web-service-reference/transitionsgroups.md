---
title: TransitionsGroups
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- TransitionsGroups
api_type:
- schema
ms.assetid: ad0849f8-5158-4a23-9c36-a49f5be1d1e1
description: El elemento TransitionsGroups representa una matriz de grupos de transición de zona horaria.
ms.openlocfilehash: 546dd3c96187bf9f1ebf574b37b689e26e3af997
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840728"
---
# <a name="transitionsgroups"></a><span data-ttu-id="5db03-103">TransitionsGroups</span><span class="sxs-lookup"><span data-stu-id="5db03-103">TransitionsGroups</span></span>

<span data-ttu-id="5db03-104">El elemento **TransitionsGroups** representa una matriz de grupos de transición de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="5db03-104">The **TransitionsGroups** element represents an array of time zone transition groups.</span></span> 
  
```XML
<TransitionsGroups>
   <TransitionsGroup/>
</TransitionsGroups>
```

 <span data-ttu-id="5db03-105">**ArrayOfTransitionsGroupsType**</span><span class="sxs-lookup"><span data-stu-id="5db03-105">**ArrayOfTransitionsGroupsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5db03-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="5db03-106">Attributes and elements</span></span>

<span data-ttu-id="5db03-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="5db03-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5db03-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="5db03-108">Attributes</span></span>

<span data-ttu-id="5db03-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5db03-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5db03-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5db03-110">Child elements</span></span>

|<span data-ttu-id="5db03-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="5db03-111">**Element**</span></span>|<span data-ttu-id="5db03-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5db03-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5db03-113">TransitionsGroup</span><span class="sxs-lookup"><span data-stu-id="5db03-113">TransitionsGroup</span></span>](transitionsgroup.md) <br/> |<span data-ttu-id="5db03-114">Representa una matriz de las transiciones de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="5db03-114">Represents an array of time zone transitions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5db03-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5db03-115">Parent elements</span></span>

|<span data-ttu-id="5db03-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="5db03-116">**Element**</span></span>|<span data-ttu-id="5db03-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5db03-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5db03-118">StartTimeZone</span><span class="sxs-lookup"><span data-stu-id="5db03-118">StartTimeZone</span></span>](starttimezone.md) <br/> |<span data-ttu-id="5db03-119">Define la zona horaria de la hora de inicio de un [CalendarItem](calendaritem.md) o [MeetingRequest](meetingrequest.md).</span><span class="sxs-lookup"><span data-stu-id="5db03-119">Defines the time zone for the start time of a [CalendarItem](calendaritem.md) or [MeetingRequest](meetingrequest.md).</span></span>  <br/> |
|[<span data-ttu-id="5db03-120">EndTimeZone</span><span class="sxs-lookup"><span data-stu-id="5db03-120">EndTimeZone</span></span>](endtimezone.md) <br/> |<span data-ttu-id="5db03-121">Define la zona horaria de la hora de finalización de un [CalendarItem](calendaritem.md) o [MeetingRequest](meetingrequest.md).</span><span class="sxs-lookup"><span data-stu-id="5db03-121">Defines the time zone for the end time of a [CalendarItem](calendaritem.md) or [MeetingRequest](meetingrequest.md).</span></span>  <br/> |
|[<span data-ttu-id="5db03-122">Definición de zona horaria</span><span class="sxs-lookup"><span data-stu-id="5db03-122">TimeZoneDefinition</span></span>](timezonedefinition.md) <br/> |<span data-ttu-id="5db03-123">Define una zona horaria.</span><span class="sxs-lookup"><span data-stu-id="5db03-123">Defines a time zone.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5db03-124">Notas</span><span class="sxs-lookup"><span data-stu-id="5db03-124">Remarks</span></span>

<span data-ttu-id="5db03-125">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="5db03-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5db03-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="5db03-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5db03-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5db03-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5db03-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="5db03-128">Schema Name</span></span>  <br/> |<span data-ttu-id="5db03-129">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="5db03-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="5db03-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="5db03-130">Validation File</span></span>  <br/> |<span data-ttu-id="5db03-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5db03-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5db03-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="5db03-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="5db03-133">False</span><span class="sxs-lookup"><span data-stu-id="5db03-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5db03-134">Ver también</span><span class="sxs-lookup"><span data-stu-id="5db03-134">See also</span></span>



- [<span data-ttu-id="5db03-135">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="5db03-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

