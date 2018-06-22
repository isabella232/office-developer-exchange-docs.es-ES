---
title: ConflictingMeetingCount
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConflictingMeetingCount
api_type:
- schema
ms.assetid: 11f4d93a-b514-4a27-8d19-f4f0a35a185e
description: El elemento ConflictingMeetingCount representa el número de las reuniones que entre en conflicto con el elemento de calendario.
ms.openlocfilehash: ace800982c284cf65ff22d92c711197ee5ee1d06
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763768"
---
# <a name="conflictingmeetingcount"></a><span data-ttu-id="95645-103">ConflictingMeetingCount</span><span class="sxs-lookup"><span data-stu-id="95645-103">ConflictingMeetingCount</span></span>

<span data-ttu-id="95645-104">El elemento **ConflictingMeetingCount** representa el número de las reuniones que entre en conflicto con el elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="95645-104">The **ConflictingMeetingCount** element represents the number of meetings that conflict with the calendar item.</span></span> 
  
```xml
<ConflictingMeetingCount/>
```

 <span data-ttu-id="95645-105">**int**</span><span class="sxs-lookup"><span data-stu-id="95645-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="95645-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="95645-106">Attributes and elements</span></span>

<span data-ttu-id="95645-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="95645-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="95645-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="95645-108">Attributes</span></span>

<span data-ttu-id="95645-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="95645-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="95645-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="95645-110">Child elements</span></span>

<span data-ttu-id="95645-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="95645-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="95645-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="95645-112">Parent elements</span></span>

|<span data-ttu-id="95645-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="95645-113">**Element**</span></span>|<span data-ttu-id="95645-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="95645-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="95645-115">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="95645-115">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="95645-116">Representa una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="95645-116">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="95645-117">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="95645-117">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="95645-118">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="95645-118">Represents an Exchange calendar item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="95645-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="95645-119">Text value</span></span>

<span data-ttu-id="95645-120">El valor de texto representa un número entero.</span><span class="sxs-lookup"><span data-stu-id="95645-120">The text value represents an integer.</span></span> <span data-ttu-id="95645-121">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="95645-121">This property is read-only.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="95645-122">Notas</span><span class="sxs-lookup"><span data-stu-id="95645-122">Remarks</span></span>

<span data-ttu-id="95645-123">Se considera que un elemento de calendario en conflicto si se produce, al menos en parte, al mismo tiempo que otro elemento de calendario en la misma carpeta de calendario.</span><span class="sxs-lookup"><span data-stu-id="95645-123">A calendar item is considered conflicting if it occurs, at least in part, at the same time as another calendar item in the same calendar folder.</span></span> <span data-ttu-id="95645-124">Si un elemento de calendario se encuentra en una carpeta de noncalendar, se compara con elementos de calendario en la carpeta Calendario predeterminada.</span><span class="sxs-lookup"><span data-stu-id="95645-124">If a calendar item is in a noncalendar folder, it is compared with calendar items in the default calendar folder.</span></span> <span data-ttu-id="95645-125">Las convocatorias de reunión se comparan con elementos de calendario en la carpeta Calendario predeterminada.</span><span class="sxs-lookup"><span data-stu-id="95645-125">Meeting requests are compared with calendar items in the default calendar folder.</span></span>
  
<span data-ttu-id="95645-126">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="95645-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="95645-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="95645-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="95645-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="95645-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="95645-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="95645-129">Schema name</span></span>  <br/> |<span data-ttu-id="95645-130">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="95645-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="95645-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="95645-131">Validation file</span></span>  <br/> |<span data-ttu-id="95645-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="95645-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="95645-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="95645-133">Can be empty</span></span>  <br/> |<span data-ttu-id="95645-134">False</span><span class="sxs-lookup"><span data-stu-id="95645-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="95645-135">Ver también</span><span class="sxs-lookup"><span data-stu-id="95645-135">See also</span></span>



- [<span data-ttu-id="95645-136">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="95645-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

