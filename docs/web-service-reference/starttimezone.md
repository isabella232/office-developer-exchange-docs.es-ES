---
title: StartTimeZone
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- StartTimeZone
api_type:
- schema
ms.assetid: d38c4dc1-4ecb-42a1-8d57-a451b16a2de2
description: El elemento StartTimeZone define la zona horaria para la hora de inicio de CalendarItem o MeetingRequest.
ms.openlocfilehash: fa88f676c0f6a7a2e934f51274942ed3bccbc789
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458526"
---
# <a name="starttimezone"></a><span data-ttu-id="c7b5b-103">StartTimeZone</span><span class="sxs-lookup"><span data-stu-id="c7b5b-103">StartTimeZone</span></span>

<span data-ttu-id="c7b5b-104">El elemento **StartTimeZone** define la zona horaria para la hora de inicio de [CalendarItem](calendaritem.md) o [MeetingRequest](meetingrequest.md).</span><span class="sxs-lookup"><span data-stu-id="c7b5b-104">The **StartTimeZone** element defines the time zone for the start time of a [CalendarItem](calendaritem.md) or [MeetingRequest](meetingrequest.md).</span></span>
  
```xml
<StartTimeZone Id="" Name="">
   <Periods/>
   <TransitionsGroups/>
   <Transitions/>
</StartTimeZone>
```

<span data-ttu-id="c7b5b-105">**TimeZoneDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="c7b5b-105">**TimeZoneDefinitionType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="c7b5b-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c7b5b-106">Attributes and elements</span></span>

<span data-ttu-id="c7b5b-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c7b5b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c7b5b-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c7b5b-108">Attributes</span></span>

|<span data-ttu-id="c7b5b-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="c7b5b-109">**Attribute**</span></span>|<span data-ttu-id="c7b5b-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c7b5b-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c7b5b-111">Id</span><span class="sxs-lookup"><span data-stu-id="c7b5b-111">Id</span></span>  <br/> |<span data-ttu-id="c7b5b-112">Representa el identificador único de la definición de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="c7b5b-112">Represents the unique identifier of the time zone definition.</span></span>  <br/> |
|<span data-ttu-id="c7b5b-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="c7b5b-113">Name</span></span>  <br/> |<span data-ttu-id="c7b5b-114">Representa el nombre descriptivo de la definición de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="c7b5b-114">Represents the descriptive name of the time zone definition.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c7b5b-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c7b5b-115">Child elements</span></span>

|<span data-ttu-id="c7b5b-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c7b5b-116">**Element**</span></span>|<span data-ttu-id="c7b5b-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c7b5b-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c7b5b-118">Períodos</span><span class="sxs-lookup"><span data-stu-id="c7b5b-118">Periods</span></span>](periods.md) <br/> |<span data-ttu-id="c7b5b-119">Representa una matriz de elementos [period](period.md) que define el desplazamiento de tiempo en diferentes etapas de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="c7b5b-119">Represents an array of [Period](period.md) elements that define the time offset at different stages of the time zone.</span></span>  <br/> |
|[<span data-ttu-id="c7b5b-120">TransitionsGroups</span><span class="sxs-lookup"><span data-stu-id="c7b5b-120">TransitionsGroups</span></span>](transitionsgroups.md) <br/> |<span data-ttu-id="c7b5b-121">Representa una matriz de elementos [TransitionsGroup](transitionsgroup.md) que especifican las transiciones de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="c7b5b-121">Represents an array of [TransitionsGroup](transitionsgroup.md) elements that specify time zone transitions.</span></span>  <br/> |
|[<span data-ttu-id="c7b5b-122">Transiciones</span><span class="sxs-lookup"><span data-stu-id="c7b5b-122">Transitions</span></span>](transitions.md) <br/> |<span data-ttu-id="c7b5b-123">Representa una matriz de transiciones de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="c7b5b-123">Represents an array of time zone transitions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c7b5b-124">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c7b5b-124">Parent elements</span></span>

|<span data-ttu-id="c7b5b-125">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c7b5b-125">**Element**</span></span>|<span data-ttu-id="c7b5b-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c7b5b-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c7b5b-127">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="c7b5b-127">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="c7b5b-128">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c7b5b-128">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="c7b5b-129">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="c7b5b-129">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="c7b5b-130">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c7b5b-130">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c7b5b-131">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c7b5b-131">Remarks</span></span>

<span data-ttu-id="c7b5b-132">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="c7b5b-132">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c7b5b-133">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c7b5b-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c7b5b-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="c7b5b-134">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c7b5b-135">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c7b5b-135">Schema Name</span></span>  <br/> |<span data-ttu-id="c7b5b-136">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="c7b5b-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="c7b5b-137">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c7b5b-137">Validation File</span></span>  <br/> |<span data-ttu-id="c7b5b-138">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="c7b5b-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c7b5b-139">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c7b5b-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="c7b5b-140">Falso</span><span class="sxs-lookup"><span data-stu-id="c7b5b-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c7b5b-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="c7b5b-141">See also</span></span>

- [<span data-ttu-id="c7b5b-142">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="c7b5b-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

