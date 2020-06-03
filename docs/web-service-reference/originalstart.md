---
title: OriginalStart
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OriginalStart
api_type:
- schema
ms.assetid: 4599dd34-15ee-4d57-b886-732081b50784
description: El elemento OriginalStart representa la hora de inicio original de un elemento de calendario.
ms.openlocfilehash: 5346a65c432b8e96cb95e412e3e88fbc40ce36e8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462370"
---
# <a name="originalstart"></a><span data-ttu-id="1a759-103">OriginalStart</span><span class="sxs-lookup"><span data-stu-id="1a759-103">OriginalStart</span></span>

<span data-ttu-id="1a759-104">El elemento **OriginalStart** representa la hora de inicio original de un elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="1a759-104">The **OriginalStart** element represents the original start time of a calendar item.</span></span> 
  
```xml
<OriginalStart/>
```

 <span data-ttu-id="1a759-105">**DateTime**</span><span class="sxs-lookup"><span data-stu-id="1a759-105">**DateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1a759-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="1a759-106">Attributes and elements</span></span>

<span data-ttu-id="1a759-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="1a759-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1a759-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="1a759-108">Attributes</span></span>

<span data-ttu-id="1a759-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1a759-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1a759-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1a759-110">Child elements</span></span>

<span data-ttu-id="1a759-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1a759-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1a759-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="1a759-112">Parent elements</span></span>

|<span data-ttu-id="1a759-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="1a759-113">**Element**</span></span>|<span data-ttu-id="1a759-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1a759-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1a759-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="1a759-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="1a759-116">Representa un elemento de calendario en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="1a759-116">Represents a calendar item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="1a759-117">FirstOccurrence</span><span class="sxs-lookup"><span data-stu-id="1a759-117">FirstOccurrence</span></span>](firstoccurrence.md) <br/> |<span data-ttu-id="1a759-118">Representa la primera aparición de un elemento de calendario periódico.</span><span class="sxs-lookup"><span data-stu-id="1a759-118">Represents the first occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="1a759-119">LastOccurrence</span><span class="sxs-lookup"><span data-stu-id="1a759-119">LastOccurrence</span></span>](lastoccurrence.md) <br/> |<span data-ttu-id="1a759-120">Representa la última repetición de un elemento de calendario periódico.</span><span class="sxs-lookup"><span data-stu-id="1a759-120">Represents the last occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="1a759-121">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="1a759-121">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="1a759-122">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="1a759-122">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="1a759-123">Suceda</span><span class="sxs-lookup"><span data-stu-id="1a759-123">Occurrence</span></span>](occurrence.md) <br/> |<span data-ttu-id="1a759-124">Representa una ocurrencia única modificada de un elemento de calendario periódico.</span><span class="sxs-lookup"><span data-stu-id="1a759-124">Represents a single modified occurrence of a recurring calendar item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1a759-125">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="1a759-125">Text value</span></span>

<span data-ttu-id="1a759-126">Si se usa este elemento, es necesario un valor de texto que representa una fecha y hora.</span><span class="sxs-lookup"><span data-stu-id="1a759-126">A text value that represents a date and time is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1a759-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1a759-127">Remarks</span></span>

<span data-ttu-id="1a759-128">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="1a759-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1a759-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="1a759-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1a759-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="1a759-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1a759-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="1a759-131">Schema Name</span></span>  <br/> |<span data-ttu-id="1a759-132">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="1a759-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="1a759-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="1a759-133">Validation File</span></span>  <br/> |<span data-ttu-id="1a759-134">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="1a759-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1a759-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="1a759-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="1a759-136">Falso</span><span class="sxs-lookup"><span data-stu-id="1a759-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1a759-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="1a759-137">See also</span></span>



- [<span data-ttu-id="1a759-138">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="1a759-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

