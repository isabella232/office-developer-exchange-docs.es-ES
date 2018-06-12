---
title: LegacyFreeBusyStatus
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- LegacyFreeBusyStatus
api_type:
- schema
ms.assetid: ee5f3046-b79f-4f68-9455-1a688cee2745
description: El elemento LegacyFreeBusyStatus representa el estado de disponibilidad del elemento de calendario.
ms.openlocfilehash: 681d7256dbef09c6c43d33ea1fc92b5d05e73a41
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836247"
---
# <a name="legacyfreebusystatus"></a><span data-ttu-id="a6d16-103">LegacyFreeBusyStatus</span><span class="sxs-lookup"><span data-stu-id="a6d16-103">LegacyFreeBusyStatus</span></span>

<span data-ttu-id="a6d16-104">El elemento **LegacyFreeBusyStatus** representa el estado de disponibilidad del elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="a6d16-104">The **LegacyFreeBusyStatus** element represents the free/busy status of the calendar item.</span></span> 
  
```xml
<LegacyFreeBusyStatus/>
```

<span data-ttu-id="a6d16-105">**LegacyFreeBusyType**</span><span class="sxs-lookup"><span data-stu-id="a6d16-105">**LegacyFreeBusyType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="a6d16-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a6d16-106">Attributes and elements</span></span>

<span data-ttu-id="a6d16-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a6d16-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a6d16-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="a6d16-108">Attributes</span></span>

<span data-ttu-id="a6d16-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a6d16-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a6d16-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a6d16-110">Child elements</span></span>

<span data-ttu-id="a6d16-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a6d16-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a6d16-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a6d16-112">Parent elements</span></span>

|<span data-ttu-id="a6d16-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="a6d16-113">**Element**</span></span>|<span data-ttu-id="a6d16-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a6d16-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a6d16-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="a6d16-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="a6d16-116">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="a6d16-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="a6d16-117">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="a6d16-117">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="a6d16-118">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="a6d16-118">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a6d16-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="a6d16-119">Text value</span></span>

<span data-ttu-id="a6d16-120">Un valor de texto es necesario para este elemento.</span><span class="sxs-lookup"><span data-stu-id="a6d16-120">A text value is required for this element.</span></span> <span data-ttu-id="a6d16-121">Los siguientes son los posibles valores de texto para este elemento:</span><span class="sxs-lookup"><span data-stu-id="a6d16-121">The following are the possible text values for this element:</span></span>
  
- <span data-ttu-id="a6d16-122">Gratuito</span><span class="sxs-lookup"><span data-stu-id="a6d16-122">Free</span></span> 
- <span data-ttu-id="a6d16-123">Provisional</span><span class="sxs-lookup"><span data-stu-id="a6d16-123">Tentative</span></span>
- <span data-ttu-id="a6d16-124">Ocupado</span><span class="sxs-lookup"><span data-stu-id="a6d16-124">Busy</span></span>
- <span data-ttu-id="a6d16-125">FUERA DE LA OFICINA</span><span class="sxs-lookup"><span data-stu-id="a6d16-125">OOF</span></span>
- <span data-ttu-id="a6d16-126">WorkingElsewhere</span><span class="sxs-lookup"><span data-stu-id="a6d16-126">WorkingElsewhere</span></span>
- <span data-ttu-id="a6d16-127">NoData</span><span class="sxs-lookup"><span data-stu-id="a6d16-127">NoData</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a6d16-128">Notas</span><span class="sxs-lookup"><span data-stu-id="a6d16-128">Remarks</span></span>

<span data-ttu-id="a6d16-129">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="a6d16-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a6d16-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a6d16-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a6d16-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a6d16-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a6d16-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a6d16-132">Schema name</span></span>  <br/> |<span data-ttu-id="a6d16-133">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="a6d16-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="a6d16-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a6d16-134">Validation file</span></span>  <br/> |<span data-ttu-id="a6d16-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a6d16-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a6d16-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a6d16-136">Can be empty</span></span>  <br/> |<span data-ttu-id="a6d16-137">False</span><span class="sxs-lookup"><span data-stu-id="a6d16-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a6d16-138">Ver también</span><span class="sxs-lookup"><span data-stu-id="a6d16-138">See also</span></span>

- [<span data-ttu-id="a6d16-139">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="a6d16-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

