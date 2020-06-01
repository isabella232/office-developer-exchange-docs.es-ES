---
title: FirstOccurrence
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FirstOccurrence
api_type:
- schema
ms.assetid: d6748860-ce0d-4d2e-b7e4-9ed834f1e45a
description: El elemento FirstOccurrence representa la primera aparición de un elemento de calendario periódico.
ms.openlocfilehash: 22ee9018df1e89a3783c4dfb56aaf065b2c8ea6c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466300"
---
# <a name="firstoccurrence"></a><span data-ttu-id="f8aec-103">FirstOccurrence</span><span class="sxs-lookup"><span data-stu-id="f8aec-103">FirstOccurrence</span></span>

<span data-ttu-id="f8aec-104">El elemento **FirstOccurrence** representa la primera aparición de un elemento de calendario periódico.</span><span class="sxs-lookup"><span data-stu-id="f8aec-104">The **FirstOccurrence** element represents the first occurrence of a recurring calendar item.</span></span> 
  
```xml
<FirstOccurrence>
   <ItemId/>
   <Start/>
   <End/>
   <OriginalStart/>
</FirstOccurrence>
```

 <span data-ttu-id="f8aec-105">**OccurrenceInfoType**</span><span class="sxs-lookup"><span data-stu-id="f8aec-105">**OccurrenceInfoType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f8aec-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f8aec-106">Attributes and elements</span></span>

<span data-ttu-id="f8aec-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f8aec-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f8aec-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="f8aec-108">Attributes</span></span>

<span data-ttu-id="f8aec-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="f8aec-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f8aec-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f8aec-110">Child elements</span></span>

|<span data-ttu-id="f8aec-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f8aec-111">**Element**</span></span>|<span data-ttu-id="f8aec-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f8aec-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f8aec-113">ItemId</span><span class="sxs-lookup"><span data-stu-id="f8aec-113">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="f8aec-114">Contiene el identificador único y la clave de cambio de la primera aparición de un elemento de calendario periódico.</span><span class="sxs-lookup"><span data-stu-id="f8aec-114">Contains the unique identifier and change key of the first occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="f8aec-115">Start</span><span class="sxs-lookup"><span data-stu-id="f8aec-115">Start</span></span>](start.md) <br/> |<span data-ttu-id="f8aec-116">Representa la hora de inicio de la primera aparición de un elemento de calendario periódico.</span><span class="sxs-lookup"><span data-stu-id="f8aec-116">Represents the start time of the first occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="f8aec-117">Centraliza</span><span class="sxs-lookup"><span data-stu-id="f8aec-117">End </span></span>](end-ex15websvcsotherref.md) <br/> |<span data-ttu-id="f8aec-118">Representa la hora de finalización de la primera aparición de un elemento de calendario periódico.</span><span class="sxs-lookup"><span data-stu-id="f8aec-118">Represents the end time of the first occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="f8aec-119">OriginalStart</span><span class="sxs-lookup"><span data-stu-id="f8aec-119">OriginalStart</span></span>](originalstart.md) <br/> |<span data-ttu-id="f8aec-120">Representa la hora de inicio original de la primera aparición de un elemento de calendario periódico.</span><span class="sxs-lookup"><span data-stu-id="f8aec-120">Represents the original start time of the first occurrence of a recurring calendar item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f8aec-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f8aec-121">Parent elements</span></span>

|<span data-ttu-id="f8aec-122">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f8aec-122">**Element**</span></span>|<span data-ttu-id="f8aec-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f8aec-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f8aec-124">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="f8aec-124">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="f8aec-125">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="f8aec-125">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="f8aec-126">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="f8aec-126">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="f8aec-127">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="f8aec-127">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f8aec-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f8aec-128">Remarks</span></span>

<span data-ttu-id="f8aec-129">Este elemento es válido si [CalendarItemType](calendaritemtype.md) tiene el valor RecurringMaster.</span><span class="sxs-lookup"><span data-stu-id="f8aec-129">This element is valid if [CalendarItemType](calendaritemtype.md) has the RecurringMaster value.</span></span> 
  
<span data-ttu-id="f8aec-130">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="f8aec-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f8aec-131">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f8aec-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f8aec-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="f8aec-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f8aec-133">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f8aec-133">Schema name</span></span>  <br/> |<span data-ttu-id="f8aec-134">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="f8aec-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="f8aec-135">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f8aec-135">Validation file</span></span>  <br/> |<span data-ttu-id="f8aec-136">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="f8aec-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f8aec-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f8aec-137">Can be empty</span></span>  <br/> |<span data-ttu-id="f8aec-138">Falso</span><span class="sxs-lookup"><span data-stu-id="f8aec-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f8aec-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="f8aec-139">See also</span></span>



- [<span data-ttu-id="f8aec-140">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="f8aec-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
  
[<span data-ttu-id="f8aec-141">Referencia EWS para Exchange</span><span class="sxs-lookup"><span data-stu-id="f8aec-141">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)

