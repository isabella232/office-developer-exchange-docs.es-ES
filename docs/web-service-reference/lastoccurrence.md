---
title: LastOccurrence
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- LastOccurrence
api_type:
- schema
ms.assetid: c9ef0fcb-4265-4e60-9986-fff0f211d00b
description: El elemento LastOccurrence representa la última repetición de un elemento de calendario periódico.
ms.openlocfilehash: 8771bbed166cfb6fdcf4d1dfe4fa0812013e2667
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459815"
---
# <a name="lastoccurrence"></a><span data-ttu-id="22883-103">LastOccurrence</span><span class="sxs-lookup"><span data-stu-id="22883-103">LastOccurrence</span></span>

<span data-ttu-id="22883-104">El elemento **LastOccurrence** representa la última repetición de un elemento de calendario periódico.</span><span class="sxs-lookup"><span data-stu-id="22883-104">The **LastOccurrence** element represents the last occurrence of a recurring calendar item.</span></span> 
  
```xml
<LastOccurrence>
   <ItemId/>
   <Start/>
   <End/>
   <OriginalStart/>
</LastOccurrence>
```

 <span data-ttu-id="22883-105">**OccurrenceInfoType**</span><span class="sxs-lookup"><span data-stu-id="22883-105">**OccurrenceInfoType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="22883-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="22883-106">Attributes and elements</span></span>

<span data-ttu-id="22883-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="22883-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="22883-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="22883-108">Attributes</span></span>

<span data-ttu-id="22883-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="22883-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="22883-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="22883-110">Child elements</span></span>

|<span data-ttu-id="22883-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="22883-111">**Element**</span></span>|<span data-ttu-id="22883-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="22883-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="22883-113">ItemId</span><span class="sxs-lookup"><span data-stu-id="22883-113">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="22883-114">Contiene el identificador único y la clave de cambio de la última repetición de un elemento de calendario periódico.</span><span class="sxs-lookup"><span data-stu-id="22883-114">Contains the unique identifier and change key of the last occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="22883-115">Start</span><span class="sxs-lookup"><span data-stu-id="22883-115">Start</span></span>](start.md) <br/> |<span data-ttu-id="22883-116">Representa la hora de inicio de la última repetición de un elemento de calendario periódico.</span><span class="sxs-lookup"><span data-stu-id="22883-116">Represents the start time of the last occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="22883-117">Centraliza</span><span class="sxs-lookup"><span data-stu-id="22883-117">End </span></span>](end-ex15websvcsotherref.md) <br/> |<span data-ttu-id="22883-118">Representa la hora de finalización de la última repetición de un elemento de calendario periódico.</span><span class="sxs-lookup"><span data-stu-id="22883-118">Represents the end time of the last occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="22883-119">OriginalStart</span><span class="sxs-lookup"><span data-stu-id="22883-119">OriginalStart</span></span>](originalstart.md) <br/> |<span data-ttu-id="22883-120">Representa la hora de inicio original de la última repetición de un elemento de calendario periódico.</span><span class="sxs-lookup"><span data-stu-id="22883-120">Represents the original start time of the last occurrence of a recurring calendar item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="22883-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="22883-121">Parent elements</span></span>

|<span data-ttu-id="22883-122">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="22883-122">**Element**</span></span>|<span data-ttu-id="22883-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="22883-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="22883-124">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="22883-124">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="22883-125">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="22883-125">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="22883-126">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="22883-126">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="22883-127">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="22883-127">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="22883-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="22883-128">Remarks</span></span>

<span data-ttu-id="22883-129">Este elemento es válido si [CalendarItemType](calendaritemtype.md) tiene el valor RecurringMaster.</span><span class="sxs-lookup"><span data-stu-id="22883-129">This element is valid if [CalendarItemType](calendaritemtype.md) has the RecurringMaster value.</span></span> 
  
<span data-ttu-id="22883-130">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="22883-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="22883-131">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="22883-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="22883-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="22883-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="22883-133">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="22883-133">Schema name</span></span>  <br/> |<span data-ttu-id="22883-134">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="22883-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="22883-135">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="22883-135">Validation file</span></span>  <br/> |<span data-ttu-id="22883-136">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="22883-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="22883-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="22883-137">Can be empty</span></span>  <br/> |<span data-ttu-id="22883-138">Falso</span><span class="sxs-lookup"><span data-stu-id="22883-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="22883-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="22883-139">See also</span></span>



- [<span data-ttu-id="22883-140">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="22883-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
  
[<span data-ttu-id="22883-141">Referencia EWS para Exchange</span><span class="sxs-lookup"><span data-stu-id="22883-141">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)

