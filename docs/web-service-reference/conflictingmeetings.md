---
title: ConflictingMeetings
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConflictingMeetings
api_type:
- schema
ms.assetid: cfff7a11-7b3a-4995-9815-afedd45ebb0f
description: El elemento ConflictingMeetings identifica todos los elementos de calendario que entre en conflicto con un tiempo de la reunión.
ms.openlocfilehash: 1d2558dba41ec3e7ae2711bb2dc26f54cada827a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763770"
---
# <a name="conflictingmeetings"></a><span data-ttu-id="275a6-103">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="275a6-103">ConflictingMeetings</span></span>

<span data-ttu-id="275a6-104">El elemento **ConflictingMeetings** identifica todos los elementos de calendario que entre en conflicto con un tiempo de la reunión.</span><span class="sxs-lookup"><span data-stu-id="275a6-104">The **ConflictingMeetings** element identifies all calendar items that conflict with a meeting time.</span></span> 
  
```xml
<ConflictingMeetings>
   <CalendarItem/>
</ConflictingMeetings>
```

 <span data-ttu-id="275a6-105">**NonEmptyArrayOfAllItemsType**</span><span class="sxs-lookup"><span data-stu-id="275a6-105">**NonEmptyArrayOfAllItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="275a6-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="275a6-106">Attributes and elements</span></span>

<span data-ttu-id="275a6-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="275a6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="275a6-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="275a6-108">Attributes</span></span>

<span data-ttu-id="275a6-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="275a6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="275a6-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="275a6-110">Child elements</span></span>

|<span data-ttu-id="275a6-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="275a6-111">**Element**</span></span>|<span data-ttu-id="275a6-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="275a6-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="275a6-113">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="275a6-113">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="275a6-114">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="275a6-114">Represents an Exchange calendar item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="275a6-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="275a6-115">Parent elements</span></span>

|<span data-ttu-id="275a6-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="275a6-116">**Element**</span></span>|<span data-ttu-id="275a6-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="275a6-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="275a6-118">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="275a6-118">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="275a6-119">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="275a6-119">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="275a6-120">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="275a6-120">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="275a6-121">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="275a6-121">Represents an Exchange calendar item.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="275a6-122">Notas</span><span class="sxs-lookup"><span data-stu-id="275a6-122">Remarks</span></span>

<span data-ttu-id="275a6-123">Si se usa este elemento, debe contener uno o más elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="275a6-123">If this element is used, it must contain one or more child elements.</span></span>
  
<span data-ttu-id="275a6-124">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="275a6-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
> [!NOTE]
> <span data-ttu-id="275a6-125">Aunque los elementos secundarios adicionales son válidos según el esquema, el elemento [CalendarItem](calendaritem.md) es el elemento secundario único que Exchange Web Services (EWS) devolverá dentro del elemento **ConflictingMeetings** .</span><span class="sxs-lookup"><span data-stu-id="275a6-125">Although additional child elements are valid per the schema, the [CalendarItem](calendaritem.md) element is the only child element that Exchange Web Services (EWS) will return within the **ConflictingMeetings** element.</span></span> <span data-ttu-id="275a6-126">En este tema no mostrar los elementos secundarios que son válidos según el esquema, pero no será devuelto por EWS.</span><span class="sxs-lookup"><span data-stu-id="275a6-126">This topic does not list child elements that are valid per the schema but will not be returned by EWS.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="275a6-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="275a6-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="275a6-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="275a6-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="275a6-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="275a6-129">Schema Name</span></span>  <br/> |<span data-ttu-id="275a6-130">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="275a6-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="275a6-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="275a6-131">Validation File</span></span>  <br/> |<span data-ttu-id="275a6-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="275a6-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="275a6-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="275a6-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="275a6-134">False</span><span class="sxs-lookup"><span data-stu-id="275a6-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="275a6-135">Ver también</span><span class="sxs-lookup"><span data-stu-id="275a6-135">See also</span></span>



- [<span data-ttu-id="275a6-136">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="275a6-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

