---
title: Cuando se ejecuta
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- When
api_type:
- schema
ms.assetid: c7df1333-a33d-4cc6-a08a-34b68843f47d
description: Cuando elemento proporciona información acerca de cuándo se produce un elemento de calendario o reunión.
ms.openlocfilehash: 519712ed10958cf556c8fb29372326ade3c31c90
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19841004"
---
# <a name="when"></a><span data-ttu-id="079aa-103">Cuando se ejecuta</span><span class="sxs-lookup"><span data-stu-id="079aa-103">When</span></span>

<span data-ttu-id="079aa-104">El elemento **cuando** proporciona información acerca de cuándo se produce un elemento de reunión o un calendario.</span><span class="sxs-lookup"><span data-stu-id="079aa-104">The **When** element provides information about when a calendar or meeting item occurs.</span></span> 
  
```xml
<When/>
```

 <span data-ttu-id="079aa-105">**String**</span><span class="sxs-lookup"><span data-stu-id="079aa-105">**String**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="079aa-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="079aa-106">Attributes and elements</span></span>

<span data-ttu-id="079aa-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="079aa-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="079aa-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="079aa-108">Attributes</span></span>

<span data-ttu-id="079aa-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="079aa-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="079aa-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="079aa-110">Child elements</span></span>

<span data-ttu-id="079aa-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="079aa-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="079aa-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="079aa-112">Parent elements</span></span>

|<span data-ttu-id="079aa-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="079aa-113">**Element**</span></span>|<span data-ttu-id="079aa-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="079aa-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="079aa-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="079aa-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="079aa-116">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="079aa-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="079aa-117">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="079aa-117">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="079aa-118">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="079aa-118">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="079aa-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="079aa-119">Text value</span></span>

<span data-ttu-id="079aa-120">El valor de texto es una cadena que describe cuando se produce un elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="079aa-120">The text value is a string that describes when a calendar item occurs.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="079aa-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="079aa-121">Remarks</span></span>

<span data-ttu-id="079aa-122">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="079aa-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="079aa-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="079aa-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="079aa-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="079aa-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="079aa-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="079aa-125">Schema name</span></span>  <br/> |<span data-ttu-id="079aa-126">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="079aa-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="079aa-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="079aa-127">Validation file</span></span>  <br/> |<span data-ttu-id="079aa-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="079aa-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="079aa-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="079aa-129">Can be empty</span></span>  <br/> |<span data-ttu-id="079aa-130">False</span><span class="sxs-lookup"><span data-stu-id="079aa-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="079aa-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="079aa-131">See also</span></span>



- [<span data-ttu-id="079aa-132">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="079aa-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

