---
title: IsMeeting
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsMeeting
api_type:
- schema
ms.assetid: 6ce22f17-7a31-46c4-b643-0894d087e852
description: El elemento IsMeeting indica si el elemento de calendario es una reunión o una cita.
ms.openlocfilehash: bb1349a8690450882e6beac0ccd84a8d03272a7d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836051"
---
# <a name="ismeeting"></a><span data-ttu-id="53b53-103">IsMeeting</span><span class="sxs-lookup"><span data-stu-id="53b53-103">IsMeeting</span></span>

<span data-ttu-id="53b53-104">El elemento **IsMeeting** indica si el elemento de calendario es una reunión o una cita.</span><span class="sxs-lookup"><span data-stu-id="53b53-104">The **IsMeeting** element indicates whether the calendar item is a meeting or an appointment.</span></span> 
  
```xml
<IsMeeting/>
```

 <span data-ttu-id="53b53-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="53b53-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="53b53-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="53b53-106">Attributes and elements</span></span>

<span data-ttu-id="53b53-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="53b53-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="53b53-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="53b53-108">Attributes</span></span>

<span data-ttu-id="53b53-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="53b53-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="53b53-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="53b53-110">Child elements</span></span>

<span data-ttu-id="53b53-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="53b53-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="53b53-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="53b53-112">Parent elements</span></span>

|<span data-ttu-id="53b53-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="53b53-113">**Element**</span></span>|<span data-ttu-id="53b53-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="53b53-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="53b53-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="53b53-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="53b53-116">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="53b53-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="53b53-117">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="53b53-117">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="53b53-118">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="53b53-118">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="53b53-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="53b53-119">Text value</span></span>

<span data-ttu-id="53b53-120">Si este elemento se incluye, se requiere un valor de texto que representa un valor de tipo Boolean.</span><span class="sxs-lookup"><span data-stu-id="53b53-120">A text value that represents a Boolean value is required if this element is included.</span></span> <span data-ttu-id="53b53-121">Un valor de **true** indica que el elemento de calendario es una reunión.</span><span class="sxs-lookup"><span data-stu-id="53b53-121">A value of **true** indicates that the calendar item is a meeting.</span></span> <span data-ttu-id="53b53-122">Un valor de **false** indica que el elemento de calendario es una cita.</span><span class="sxs-lookup"><span data-stu-id="53b53-122">A value of **false** indicates that the calendar item is an appointment.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="53b53-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="53b53-123">Remarks</span></span>

<span data-ttu-id="53b53-124">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="53b53-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="53b53-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="53b53-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="53b53-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="53b53-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="53b53-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="53b53-127">Schema name</span></span>  <br/> |<span data-ttu-id="53b53-128">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="53b53-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="53b53-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="53b53-129">Validation file</span></span>  <br/> |<span data-ttu-id="53b53-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="53b53-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="53b53-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="53b53-131">Can be empty</span></span>  <br/> |<span data-ttu-id="53b53-132">False</span><span class="sxs-lookup"><span data-stu-id="53b53-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="53b53-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="53b53-133">See also</span></span>



- [<span data-ttu-id="53b53-134">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="53b53-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

