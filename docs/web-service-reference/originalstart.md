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
ms.openlocfilehash: 9e5facb3df87ab08e05f23258abdf1767fae64e4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836668"
---
# <a name="originalstart"></a><span data-ttu-id="54468-103">OriginalStart</span><span class="sxs-lookup"><span data-stu-id="54468-103">OriginalStart</span></span>

<span data-ttu-id="54468-104">El elemento **OriginalStart** representa la hora de inicio original de un elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="54468-104">The **OriginalStart** element represents the original start time of a calendar item.</span></span> 
  
```xml
<OriginalStart/>
```

 <span data-ttu-id="54468-105">**DateTime**</span><span class="sxs-lookup"><span data-stu-id="54468-105">**DateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="54468-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="54468-106">Attributes and elements</span></span>

<span data-ttu-id="54468-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="54468-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="54468-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="54468-108">Attributes</span></span>

<span data-ttu-id="54468-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="54468-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="54468-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="54468-110">Child elements</span></span>

<span data-ttu-id="54468-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="54468-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="54468-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="54468-112">Parent elements</span></span>

|<span data-ttu-id="54468-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="54468-113">**Element**</span></span>|<span data-ttu-id="54468-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="54468-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="54468-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="54468-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="54468-116">Representa un elemento de calendario en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="54468-116">Represents a calendar item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="54468-117">FirstOccurrence</span><span class="sxs-lookup"><span data-stu-id="54468-117">FirstOccurrence</span></span>](firstoccurrence.md) <br/> |<span data-ttu-id="54468-118">Representa la primera aparición de un elemento periódico del calendario.</span><span class="sxs-lookup"><span data-stu-id="54468-118">Represents the first occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="54468-119">LastOccurrence</span><span class="sxs-lookup"><span data-stu-id="54468-119">LastOccurrence</span></span>](lastoccurrence.md) <br/> |<span data-ttu-id="54468-120">Representa la última aparición de un elemento periódico del calendario.</span><span class="sxs-lookup"><span data-stu-id="54468-120">Represents the last occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="54468-121">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="54468-121">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="54468-122">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="54468-122">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="54468-123">Repetición</span><span class="sxs-lookup"><span data-stu-id="54468-123">Occurrence</span></span>](occurrence.md) <br/> |<span data-ttu-id="54468-124">Representa una sola aparición de modificación de un elemento periódico del calendario.</span><span class="sxs-lookup"><span data-stu-id="54468-124">Represents a single modified occurrence of a recurring calendar item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="54468-125">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="54468-125">Text value</span></span>

<span data-ttu-id="54468-126">Si se usa este elemento, es necesario un valor de texto que representa una fecha y hora.</span><span class="sxs-lookup"><span data-stu-id="54468-126">A text value that represents a date and time is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="54468-127">Notas</span><span class="sxs-lookup"><span data-stu-id="54468-127">Remarks</span></span>

<span data-ttu-id="54468-128">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="54468-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="54468-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="54468-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="54468-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="54468-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="54468-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="54468-131">Schema Name</span></span>  <br/> |<span data-ttu-id="54468-132">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="54468-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="54468-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="54468-133">Validation File</span></span>  <br/> |<span data-ttu-id="54468-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="54468-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="54468-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="54468-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="54468-136">False</span><span class="sxs-lookup"><span data-stu-id="54468-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="54468-137">Ver también</span><span class="sxs-lookup"><span data-stu-id="54468-137">See also</span></span>



- [<span data-ttu-id="54468-138">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="54468-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

