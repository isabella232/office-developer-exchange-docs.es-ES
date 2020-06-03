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
ms.openlocfilehash: 35244e122ee31045359afd0833459bbb94fd0aa1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467413"
---
# <a name="transitionsgroups"></a><span data-ttu-id="22dca-103">TransitionsGroups</span><span class="sxs-lookup"><span data-stu-id="22dca-103">TransitionsGroups</span></span>

<span data-ttu-id="22dca-104">El elemento **TransitionsGroups** representa una matriz de grupos de transición de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="22dca-104">The **TransitionsGroups** element represents an array of time zone transition groups.</span></span> 
  
```XML
<TransitionsGroups>
   <TransitionsGroup/>
</TransitionsGroups>
```

 <span data-ttu-id="22dca-105">**ArrayOfTransitionsGroupsType**</span><span class="sxs-lookup"><span data-stu-id="22dca-105">**ArrayOfTransitionsGroupsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="22dca-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="22dca-106">Attributes and elements</span></span>

<span data-ttu-id="22dca-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="22dca-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="22dca-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="22dca-108">Attributes</span></span>

<span data-ttu-id="22dca-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="22dca-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="22dca-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="22dca-110">Child elements</span></span>

|<span data-ttu-id="22dca-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="22dca-111">**Element**</span></span>|<span data-ttu-id="22dca-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="22dca-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="22dca-113">TransitionsGroup</span><span class="sxs-lookup"><span data-stu-id="22dca-113">TransitionsGroup</span></span>](transitionsgroup.md) <br/> |<span data-ttu-id="22dca-114">Representa una matriz de transiciones de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="22dca-114">Represents an array of time zone transitions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="22dca-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="22dca-115">Parent elements</span></span>

|<span data-ttu-id="22dca-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="22dca-116">**Element**</span></span>|<span data-ttu-id="22dca-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="22dca-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="22dca-118">StartTimeZone</span><span class="sxs-lookup"><span data-stu-id="22dca-118">StartTimeZone</span></span>](starttimezone.md) <br/> |<span data-ttu-id="22dca-119">Define la zona horaria de la hora de inicio de un [CalendarItem](calendaritem.md) o [MeetingRequest](meetingrequest.md).</span><span class="sxs-lookup"><span data-stu-id="22dca-119">Defines the time zone for the start time of a [CalendarItem](calendaritem.md) or [MeetingRequest](meetingrequest.md).</span></span>  <br/> |
|[<span data-ttu-id="22dca-120">EndTimeZone</span><span class="sxs-lookup"><span data-stu-id="22dca-120">EndTimeZone</span></span>](endtimezone.md) <br/> |<span data-ttu-id="22dca-121">Define la zona horaria de la hora de finalización de [CalendarItem](calendaritem.md) o [MeetingRequest](meetingrequest.md).</span><span class="sxs-lookup"><span data-stu-id="22dca-121">Defines the time zone for the end time of a [CalendarItem](calendaritem.md) or [MeetingRequest](meetingrequest.md).</span></span>  <br/> |
|[<span data-ttu-id="22dca-122">TimeZoneDefinition</span><span class="sxs-lookup"><span data-stu-id="22dca-122">TimeZoneDefinition</span></span>](timezonedefinition.md) <br/> |<span data-ttu-id="22dca-123">Define una zona horaria.</span><span class="sxs-lookup"><span data-stu-id="22dca-123">Defines a time zone.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="22dca-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="22dca-124">Remarks</span></span>

<span data-ttu-id="22dca-125">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="22dca-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="22dca-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="22dca-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="22dca-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="22dca-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="22dca-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="22dca-128">Schema Name</span></span>  <br/> |<span data-ttu-id="22dca-129">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="22dca-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="22dca-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="22dca-130">Validation File</span></span>  <br/> |<span data-ttu-id="22dca-131">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="22dca-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="22dca-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="22dca-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="22dca-133">Falso</span><span class="sxs-lookup"><span data-stu-id="22dca-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="22dca-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="22dca-134">See also</span></span>



- [<span data-ttu-id="22dca-135">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="22dca-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

