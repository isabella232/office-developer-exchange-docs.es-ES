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
description: El elemento ConflictingMeetingCount representa el número de reuniones que entran en conflicto con el elemento de calendario.
ms.openlocfilehash: d53245e1b5d1f0182b28b15bf55ba9742bbb2a07
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463863"
---
# <a name="conflictingmeetingcount"></a><span data-ttu-id="c542a-103">ConflictingMeetingCount</span><span class="sxs-lookup"><span data-stu-id="c542a-103">ConflictingMeetingCount</span></span>

<span data-ttu-id="c542a-104">El elemento **ConflictingMeetingCount** representa el número de reuniones que entran en conflicto con el elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="c542a-104">The **ConflictingMeetingCount** element represents the number of meetings that conflict with the calendar item.</span></span> 
  
```xml
<ConflictingMeetingCount/>
```

 <span data-ttu-id="c542a-105">**int**</span><span class="sxs-lookup"><span data-stu-id="c542a-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c542a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c542a-106">Attributes and elements</span></span>

<span data-ttu-id="c542a-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c542a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c542a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c542a-108">Attributes</span></span>

<span data-ttu-id="c542a-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c542a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c542a-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c542a-110">Child elements</span></span>

<span data-ttu-id="c542a-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c542a-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c542a-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c542a-112">Parent elements</span></span>

|<span data-ttu-id="c542a-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c542a-113">**Element**</span></span>|<span data-ttu-id="c542a-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c542a-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c542a-115">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="c542a-115">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="c542a-116">Representa una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c542a-116">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="c542a-117">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="c542a-117">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="c542a-118">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c542a-118">Represents an Exchange calendar item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c542a-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="c542a-119">Text value</span></span>

<span data-ttu-id="c542a-120">El valor de texto representa un número entero.</span><span class="sxs-lookup"><span data-stu-id="c542a-120">The text value represents an integer.</span></span> <span data-ttu-id="c542a-121">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="c542a-121">This property is read-only.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c542a-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c542a-122">Remarks</span></span>

<span data-ttu-id="c542a-123">Un elemento de calendario se considera conflictivo si se produce, al menos en parte, al mismo tiempo que otro elemento de calendario en la misma carpeta calendario.</span><span class="sxs-lookup"><span data-stu-id="c542a-123">A calendar item is considered conflicting if it occurs, at least in part, at the same time as another calendar item in the same calendar folder.</span></span> <span data-ttu-id="c542a-124">Si un elemento de calendario está en una carpeta que no es un calendario, se compara con los elementos del calendario de la carpeta calendario predeterminada.</span><span class="sxs-lookup"><span data-stu-id="c542a-124">If a calendar item is in a noncalendar folder, it is compared with calendar items in the default calendar folder.</span></span> <span data-ttu-id="c542a-125">Las convocatorias de reunión se comparan con los elementos del calendario de la carpeta calendario predeterminada.</span><span class="sxs-lookup"><span data-stu-id="c542a-125">Meeting requests are compared with calendar items in the default calendar folder.</span></span>
  
<span data-ttu-id="c542a-126">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="c542a-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c542a-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c542a-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c542a-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="c542a-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c542a-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c542a-129">Schema name</span></span>  <br/> |<span data-ttu-id="c542a-130">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="c542a-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="c542a-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c542a-131">Validation file</span></span>  <br/> |<span data-ttu-id="c542a-132">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="c542a-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c542a-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c542a-133">Can be empty</span></span>  <br/> |<span data-ttu-id="c542a-134">Falso</span><span class="sxs-lookup"><span data-stu-id="c542a-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c542a-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="c542a-135">See also</span></span>



- [<span data-ttu-id="c542a-136">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="c542a-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

