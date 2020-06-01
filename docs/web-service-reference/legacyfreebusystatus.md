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
ms.openlocfilehash: ecbcae0862c9c02c0a4a61012816e4c2c6ea07b7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463233"
---
# <a name="legacyfreebusystatus"></a><span data-ttu-id="26410-103">LegacyFreeBusyStatus</span><span class="sxs-lookup"><span data-stu-id="26410-103">LegacyFreeBusyStatus</span></span>

<span data-ttu-id="26410-104">El elemento **LegacyFreeBusyStatus** representa el estado de disponibilidad del elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="26410-104">The **LegacyFreeBusyStatus** element represents the free/busy status of the calendar item.</span></span> 
  
```xml
<LegacyFreeBusyStatus/>
```

<span data-ttu-id="26410-105">**LegacyFreeBusyType**</span><span class="sxs-lookup"><span data-stu-id="26410-105">**LegacyFreeBusyType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="26410-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="26410-106">Attributes and elements</span></span>

<span data-ttu-id="26410-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="26410-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="26410-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="26410-108">Attributes</span></span>

<span data-ttu-id="26410-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="26410-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="26410-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="26410-110">Child elements</span></span>

<span data-ttu-id="26410-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="26410-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="26410-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="26410-112">Parent elements</span></span>

|<span data-ttu-id="26410-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="26410-113">**Element**</span></span>|<span data-ttu-id="26410-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="26410-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="26410-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="26410-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="26410-116">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="26410-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="26410-117">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="26410-117">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="26410-118">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="26410-118">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="26410-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="26410-119">Text value</span></span>

<span data-ttu-id="26410-120">Se requiere un valor de texto para este elemento.</span><span class="sxs-lookup"><span data-stu-id="26410-120">A text value is required for this element.</span></span> <span data-ttu-id="26410-121">A continuación se muestran los valores de texto posibles para este elemento:</span><span class="sxs-lookup"><span data-stu-id="26410-121">The following are the possible text values for this element:</span></span>
  
- <span data-ttu-id="26410-122">Libre</span><span class="sxs-lookup"><span data-stu-id="26410-122">Free</span></span> 
- <span data-ttu-id="26410-123">Provisional</span><span class="sxs-lookup"><span data-stu-id="26410-123">Tentative</span></span>
- <span data-ttu-id="26410-124">Ocupado</span><span class="sxs-lookup"><span data-stu-id="26410-124">Busy</span></span>
- <span data-ttu-id="26410-125">Oficina</span><span class="sxs-lookup"><span data-stu-id="26410-125">OOF</span></span>
- <span data-ttu-id="26410-126">WorkingElsewhere</span><span class="sxs-lookup"><span data-stu-id="26410-126">WorkingElsewhere</span></span>
- <span data-ttu-id="26410-127">NoData</span><span class="sxs-lookup"><span data-stu-id="26410-127">NoData</span></span>
    
## <a name="remarks"></a><span data-ttu-id="26410-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="26410-128">Remarks</span></span>

<span data-ttu-id="26410-129">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="26410-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="26410-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="26410-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="26410-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="26410-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="26410-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="26410-132">Schema name</span></span>  <br/> |<span data-ttu-id="26410-133">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="26410-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="26410-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="26410-134">Validation file</span></span>  <br/> |<span data-ttu-id="26410-135">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="26410-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="26410-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="26410-136">Can be empty</span></span>  <br/> |<span data-ttu-id="26410-137">Falso</span><span class="sxs-lookup"><span data-stu-id="26410-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="26410-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="26410-138">See also</span></span>

- [<span data-ttu-id="26410-139">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="26410-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

