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
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763770"
---
# <a name="conflictingmeetings"></a><span data-ttu-id="c3442-103">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="c3442-103">ConflictingMeetings</span></span>

<span data-ttu-id="c3442-104">El elemento **ConflictingMeetings** identifica todos los elementos de calendario que entre en conflicto con un tiempo de la reunión.</span><span class="sxs-lookup"><span data-stu-id="c3442-104">The **ConflictingMeetings** element identifies all calendar items that conflict with a meeting time.</span></span> 
  
```xml
<ConflictingMeetings>
   <CalendarItem/>
</ConflictingMeetings>
```

 <span data-ttu-id="c3442-105">**NonEmptyArrayOfAllItemsType**</span><span class="sxs-lookup"><span data-stu-id="c3442-105">**NonEmptyArrayOfAllItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c3442-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c3442-106">Attributes and elements</span></span>

<span data-ttu-id="c3442-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c3442-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c3442-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c3442-108">Attributes</span></span>

<span data-ttu-id="c3442-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c3442-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c3442-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c3442-110">Child elements</span></span>

|<span data-ttu-id="c3442-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="c3442-111">**Element**</span></span>|<span data-ttu-id="c3442-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c3442-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c3442-113">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="c3442-113">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="c3442-114">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c3442-114">Represents an Exchange calendar item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c3442-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c3442-115">Parent elements</span></span>

|<span data-ttu-id="c3442-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="c3442-116">**Element**</span></span>|<span data-ttu-id="c3442-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c3442-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c3442-118">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="c3442-118">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="c3442-119">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c3442-119">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="c3442-120">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="c3442-120">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="c3442-121">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c3442-121">Represents an Exchange calendar item.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c3442-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c3442-122">Remarks</span></span>

<span data-ttu-id="c3442-123">Si se usa este elemento, debe contener uno o más elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="c3442-123">If this element is used, it must contain one or more child elements.</span></span>
  
<span data-ttu-id="c3442-124">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="c3442-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
> [!NOTE]
> <span data-ttu-id="c3442-125">Aunque los elementos secundarios adicionales son válidos según el esquema, el elemento [CalendarItem](calendaritem.md) es el elemento secundario único que Exchange Web Services (EWS) devolverá dentro del elemento **ConflictingMeetings** .</span><span class="sxs-lookup"><span data-stu-id="c3442-125">Although additional child elements are valid per the schema, the [CalendarItem](calendaritem.md) element is the only child element that Exchange Web Services (EWS) will return within the **ConflictingMeetings** element.</span></span> <span data-ttu-id="c3442-126">En este tema no mostrar los elementos secundarios que son válidos según el esquema, pero no será devuelto por EWS.</span><span class="sxs-lookup"><span data-stu-id="c3442-126">This topic does not list child elements that are valid per the schema but will not be returned by EWS.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="c3442-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c3442-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c3442-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c3442-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c3442-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c3442-129">Schema Name</span></span>  <br/> |<span data-ttu-id="c3442-130">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="c3442-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="c3442-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c3442-131">Validation File</span></span>  <br/> |<span data-ttu-id="c3442-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c3442-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c3442-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c3442-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="c3442-134">False</span><span class="sxs-lookup"><span data-stu-id="c3442-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c3442-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="c3442-135">See also</span></span>



- [<span data-ttu-id="c3442-136">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="c3442-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

