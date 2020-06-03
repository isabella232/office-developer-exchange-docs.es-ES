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
description: El elemento ConflictingMeetings identifica todos los elementos de calendario que entran en conflicto con una hora de reunión.
ms.openlocfilehash: dc897c9dc33117d379d89bb9bb41104ca02def1f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460179"
---
# <a name="conflictingmeetings"></a><span data-ttu-id="8fe65-103">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="8fe65-103">ConflictingMeetings</span></span>

<span data-ttu-id="8fe65-104">El elemento **ConflictingMeetings** identifica todos los elementos de calendario que entran en conflicto con una hora de reunión.</span><span class="sxs-lookup"><span data-stu-id="8fe65-104">The **ConflictingMeetings** element identifies all calendar items that conflict with a meeting time.</span></span> 
  
```xml
<ConflictingMeetings>
   <CalendarItem/>
</ConflictingMeetings>
```

 <span data-ttu-id="8fe65-105">**NonEmptyArrayOfAllItemsType**</span><span class="sxs-lookup"><span data-stu-id="8fe65-105">**NonEmptyArrayOfAllItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8fe65-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="8fe65-106">Attributes and elements</span></span>

<span data-ttu-id="8fe65-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="8fe65-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8fe65-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="8fe65-108">Attributes</span></span>

<span data-ttu-id="8fe65-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="8fe65-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8fe65-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8fe65-110">Child elements</span></span>

|<span data-ttu-id="8fe65-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="8fe65-111">**Element**</span></span>|<span data-ttu-id="8fe65-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8fe65-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8fe65-113">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="8fe65-113">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="8fe65-114">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="8fe65-114">Represents an Exchange calendar item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8fe65-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="8fe65-115">Parent elements</span></span>

|<span data-ttu-id="8fe65-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="8fe65-116">**Element**</span></span>|<span data-ttu-id="8fe65-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8fe65-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8fe65-118">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="8fe65-118">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="8fe65-119">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="8fe65-119">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="8fe65-120">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="8fe65-120">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="8fe65-121">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="8fe65-121">Represents an Exchange calendar item.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8fe65-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8fe65-122">Remarks</span></span>

<span data-ttu-id="8fe65-123">Si se usa este elemento, debe contener uno o más elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="8fe65-123">If this element is used, it must contain one or more child elements.</span></span>
  
<span data-ttu-id="8fe65-124">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="8fe65-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
> [!NOTE]
> <span data-ttu-id="8fe65-125">Aunque los elementos secundarios adicionales son válidos para cada esquema, el elemento [CalendarItem](calendaritem.md) es el único elemento secundario que los servicios web Exchange (EWS) devolverán dentro del elemento **ConflictingMeetings** .</span><span class="sxs-lookup"><span data-stu-id="8fe65-125">Although additional child elements are valid per the schema, the [CalendarItem](calendaritem.md) element is the only child element that Exchange Web Services (EWS) will return within the **ConflictingMeetings** element.</span></span> <span data-ttu-id="8fe65-126">En este tema no se enumeran los elementos secundarios que son válidos para cada esquema, pero que no se devolverán con EWS.</span><span class="sxs-lookup"><span data-stu-id="8fe65-126">This topic does not list child elements that are valid per the schema but will not be returned by EWS.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="8fe65-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="8fe65-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8fe65-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="8fe65-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8fe65-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="8fe65-129">Schema Name</span></span>  <br/> |<span data-ttu-id="8fe65-130">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="8fe65-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="8fe65-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="8fe65-131">Validation File</span></span>  <br/> |<span data-ttu-id="8fe65-132">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="8fe65-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8fe65-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="8fe65-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="8fe65-134">Falso</span><span class="sxs-lookup"><span data-stu-id="8fe65-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8fe65-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="8fe65-135">See also</span></span>



- [<span data-ttu-id="8fe65-136">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="8fe65-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

