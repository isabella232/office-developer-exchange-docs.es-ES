---
title: IsOrganizer
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a31ac268-5061-4272-a433-ffaea2fbcfa9
description: El elemento IsOrganizer especifica un valor booleano que indica si esta persona es el organizador de la reunión.
ms.openlocfilehash: 5fd775cfc0a296c08d19d0468d96aa36ba67ddd0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836063"
---
# <a name="isorganizer"></a><span data-ttu-id="7e87e-103">IsOrganizer</span><span class="sxs-lookup"><span data-stu-id="7e87e-103">IsOrganizer</span></span>

<span data-ttu-id="7e87e-104">El elemento **IsOrganizer** especifica un valor booleano que indica si esta persona es el organizador de la reunión.</span><span class="sxs-lookup"><span data-stu-id="7e87e-104">The **IsOrganizer** element specifies a Boolean value that indicates whether this person is the organizer of the meeting.</span></span> 
  
```XML
<IsOrganizer>true | false</IsOrganizer>
```

 <span data-ttu-id="7e87e-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="7e87e-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7e87e-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="7e87e-106">Attributes and elements</span></span>

<span data-ttu-id="7e87e-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="7e87e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7e87e-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="7e87e-108">Attributes</span></span>

<span data-ttu-id="7e87e-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7e87e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7e87e-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7e87e-110">Child elements</span></span>

<span data-ttu-id="7e87e-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7e87e-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7e87e-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7e87e-112">Parent elements</span></span>

|<span data-ttu-id="7e87e-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="7e87e-113">**Element**</span></span>|<span data-ttu-id="7e87e-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7e87e-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7e87e-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="7e87e-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="7e87e-116">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="7e87e-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="7e87e-117">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="7e87e-117">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="7e87e-118">Representa un mensaje de reunión.</span><span class="sxs-lookup"><span data-stu-id="7e87e-118">Represents a meeting message.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7e87e-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="7e87e-119">Text value</span></span>

<span data-ttu-id="7e87e-120">Un valor de texto de **true** para el elemento **IsOrganizer** indica que el mensaje de reunión o elemento de calendario creado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="7e87e-120">A text value of **true** for the **IsOrganizer** element indicates that the calendar item or meeting message was created by the user.</span></span> <span data-ttu-id="7e87e-121">Un valor de **false** indica que el mensaje de reunión o elemento de calendario no se ha creado el usuario bv.</span><span class="sxs-lookup"><span data-stu-id="7e87e-121">A value of **false** indicates that the calendar item or meeting message was not created bv the user.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7e87e-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7e87e-122">Remarks</span></span>

<span data-ttu-id="7e87e-123">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="7e87e-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="7e87e-124">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="7e87e-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7e87e-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7e87e-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7e87e-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7e87e-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7e87e-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="7e87e-127">Schema Name</span></span>  <br/> |<span data-ttu-id="7e87e-128">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="7e87e-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="7e87e-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="7e87e-129">Validation File</span></span>  <br/> |<span data-ttu-id="7e87e-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7e87e-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="7e87e-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="7e87e-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="7e87e-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="7e87e-132">See also</span></span>



- [<span data-ttu-id="7e87e-133">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="7e87e-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

