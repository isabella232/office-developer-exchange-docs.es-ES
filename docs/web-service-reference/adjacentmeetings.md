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
description: El elemento AdjacentMeetings identifica todos los elementos de calendario adyacentes a una hora de reunión.
ms.openlocfilehash: 7c89095e24af799df22a848be06a0fd65d53be7f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463583"
---
# <a name="adjacentmeetings"></a><span data-ttu-id="5d74a-103">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="5d74a-103">AdjacentMeetings</span></span>

<span data-ttu-id="5d74a-104">El elemento **AdjacentMeetings** identifica todos los elementos de calendario adyacentes a una hora de reunión.</span><span class="sxs-lookup"><span data-stu-id="5d74a-104">The **AdjacentMeetings** element identifies all calendar items that are adjacent to a meeting time.</span></span> 
  
```xml
<AdjacentMeetings>
   <CalendarItem/>
</AdjacentMeetings>
```

 <span data-ttu-id="5d74a-105">**NonEmptyArrayOfAllItemsType**</span><span class="sxs-lookup"><span data-stu-id="5d74a-105">**NonEmptyArrayOfAllItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5d74a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="5d74a-106">Attributes and elements</span></span>

<span data-ttu-id="5d74a-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="5d74a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5d74a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="5d74a-108">Attributes</span></span>

<span data-ttu-id="5d74a-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="5d74a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5d74a-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5d74a-110">Child elements</span></span>

|<span data-ttu-id="5d74a-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="5d74a-111">**Element**</span></span>|<span data-ttu-id="5d74a-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5d74a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5d74a-113">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="5d74a-113">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="5d74a-114">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5d74a-114">Represents an Exchange calendar item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5d74a-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5d74a-115">Parent elements</span></span>

|<span data-ttu-id="5d74a-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="5d74a-116">**Element**</span></span>|<span data-ttu-id="5d74a-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5d74a-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5d74a-118">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="5d74a-118">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="5d74a-119">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5d74a-119">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="5d74a-120">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="5d74a-120">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="5d74a-121">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5d74a-121">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5d74a-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5d74a-122">Remarks</span></span>

<span data-ttu-id="5d74a-123">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="5d74a-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
> [!NOTE]
> <span data-ttu-id="5d74a-124">Aunque los elementos secundarios adicionales son válidos para cada esquema, el elemento [CalendarItem](calendaritem.md) es el único elemento secundario que los servicios web Exchange (EWS) devolverán dentro del elemento **AdjacentMeetings** .</span><span class="sxs-lookup"><span data-stu-id="5d74a-124">Although additional child elements are valid per the schema, the [CalendarItem](calendaritem.md) element is the only child element that Exchange Web Services (EWS) will return within the **AdjacentMeetings** element.</span></span> <span data-ttu-id="5d74a-125">En este tema no se enumeran los elementos secundarios que son válidos para cada esquema, pero que no se devolverán con EWS.</span><span class="sxs-lookup"><span data-stu-id="5d74a-125">This topic does not list child elements that are valid per the schema but will not be returned by EWS.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="5d74a-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="5d74a-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5d74a-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="5d74a-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5d74a-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="5d74a-128">Schema Name</span></span>  <br/> |<span data-ttu-id="5d74a-129">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="5d74a-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="5d74a-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="5d74a-130">Validation File</span></span>  <br/> |<span data-ttu-id="5d74a-131">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="5d74a-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5d74a-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="5d74a-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="5d74a-133">Falso</span><span class="sxs-lookup"><span data-stu-id="5d74a-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5d74a-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="5d74a-134">See also</span></span>

- [<span data-ttu-id="5d74a-135">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="5d74a-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

