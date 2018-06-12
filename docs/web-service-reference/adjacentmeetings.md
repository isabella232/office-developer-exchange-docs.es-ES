---
title: AdjacentMeetings
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AdjacentMeetings
api_type:
- schema
ms.assetid: 50a9c381-9166-476e-8421-29e51b94499b
description: El elemento AdjacentMeetings identifica todos los elementos de calendario que están junto a una hora de reunión.
ms.openlocfilehash: 9ab818f4f67c32c01101cc595ccb92424a872ef0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763418"
---
# <a name="adjacentmeetings"></a><span data-ttu-id="e0544-103">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="e0544-103">AdjacentMeetings</span></span>

<span data-ttu-id="e0544-104">El elemento **AdjacentMeetings** identifica todos los elementos de calendario que están junto a una hora de reunión.</span><span class="sxs-lookup"><span data-stu-id="e0544-104">The **AdjacentMeetings** element identifies all calendar items that are adjacent to a meeting time.</span></span> 
  
```xml
<AdjacentMeetings>
   <CalendarItem/>
</AdjacentMeetings>
```

 <span data-ttu-id="e0544-105">**NonEmptyArrayOfAllItemsType**</span><span class="sxs-lookup"><span data-stu-id="e0544-105">**NonEmptyArrayOfAllItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e0544-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e0544-106">Attributes and elements</span></span>

<span data-ttu-id="e0544-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e0544-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e0544-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="e0544-108">Attributes</span></span>

<span data-ttu-id="e0544-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e0544-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e0544-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e0544-110">Child elements</span></span>

|<span data-ttu-id="e0544-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="e0544-111">**Element**</span></span>|<span data-ttu-id="e0544-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e0544-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e0544-113">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="e0544-113">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="e0544-114">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e0544-114">Represents an Exchange calendar item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e0544-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e0544-115">Parent elements</span></span>

|<span data-ttu-id="e0544-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="e0544-116">**Element**</span></span>|<span data-ttu-id="e0544-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e0544-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e0544-118">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="e0544-118">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="e0544-119">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e0544-119">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="e0544-120">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="e0544-120">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="e0544-121">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e0544-121">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e0544-122">Notas</span><span class="sxs-lookup"><span data-stu-id="e0544-122">Remarks</span></span>

<span data-ttu-id="e0544-123">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="e0544-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
> [!NOTE]
> <span data-ttu-id="e0544-124">Aunque los elementos secundarios adicionales son válidos según el esquema, el elemento [CalendarItem](calendaritem.md) es el elemento secundario único que Exchange Web Services (EWS) devolverá dentro del elemento **AdjacentMeetings** .</span><span class="sxs-lookup"><span data-stu-id="e0544-124">Although additional child elements are valid per the schema, the [CalendarItem](calendaritem.md) element is the only child element that Exchange Web Services (EWS) will return within the **AdjacentMeetings** element.</span></span> <span data-ttu-id="e0544-125">En este tema no mostrar los elementos secundarios que son válidos según el esquema, pero no será devuelto por EWS.</span><span class="sxs-lookup"><span data-stu-id="e0544-125">This topic does not list child elements that are valid per the schema but will not be returned by EWS.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="e0544-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e0544-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e0544-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e0544-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e0544-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e0544-128">Schema Name</span></span>  <br/> |<span data-ttu-id="e0544-129">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="e0544-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="e0544-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e0544-130">Validation File</span></span>  <br/> |<span data-ttu-id="e0544-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e0544-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e0544-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e0544-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="e0544-133">False</span><span class="sxs-lookup"><span data-stu-id="e0544-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e0544-134">Ver también</span><span class="sxs-lookup"><span data-stu-id="e0544-134">See also</span></span>

- [<span data-ttu-id="e0544-135">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="e0544-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

