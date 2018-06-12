---
title: IsCancelled
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsCancelled
api_type:
- schema
ms.assetid: 50c1e97f-2913-47a1-8457-60428a3c5b92
description: El elemento IsCancelled indica si se ha cancelado una reunión o cita.
ms.openlocfilehash: 594b8a9ccb535f074a8cf1da060373f640231a29
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19835993"
---
# <a name="iscancelled"></a><span data-ttu-id="fe4d7-103">IsCancelled</span><span class="sxs-lookup"><span data-stu-id="fe4d7-103">IsCancelled</span></span>

<span data-ttu-id="fe4d7-104">El elemento **IsCancelled** indica si se ha cancelado una reunión o cita.</span><span class="sxs-lookup"><span data-stu-id="fe4d7-104">The **IsCancelled** element indicates whether an appointment or meeting has been canceled.</span></span> 
  
```xml
<IsCancelled/>
```

 <span data-ttu-id="fe4d7-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="fe4d7-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fe4d7-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="fe4d7-106">Attributes and elements</span></span>

<span data-ttu-id="fe4d7-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="fe4d7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fe4d7-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="fe4d7-108">Attributes</span></span>

<span data-ttu-id="fe4d7-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="fe4d7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fe4d7-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="fe4d7-110">Child elements</span></span>

<span data-ttu-id="fe4d7-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="fe4d7-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="fe4d7-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="fe4d7-112">Parent elements</span></span>

|<span data-ttu-id="fe4d7-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="fe4d7-113">**Element**</span></span>|<span data-ttu-id="fe4d7-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fe4d7-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fe4d7-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="fe4d7-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="fe4d7-116">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="fe4d7-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="fe4d7-117">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="fe4d7-117">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="fe4d7-118">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="fe4d7-118">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="fe4d7-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="fe4d7-119">Text value</span></span>

<span data-ttu-id="fe4d7-120">Si este elemento se incluye, se requiere un valor de texto que representa un valor de tipo Boolean.</span><span class="sxs-lookup"><span data-stu-id="fe4d7-120">A text value that represents a Boolean value is required if this element is included.</span></span> <span data-ttu-id="fe4d7-121">Un valor de **true** indica que se ha cancelado el elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="fe4d7-121">A value of **true** indicates that the calendar item has been canceled.</span></span> <span data-ttu-id="fe4d7-122">Un valor de **false** indica que no se ha cancelado un elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="fe4d7-122">A value of **false** indicates that a calendar item has not been canceled.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="fe4d7-123">Notas</span><span class="sxs-lookup"><span data-stu-id="fe4d7-123">Remarks</span></span>

<span data-ttu-id="fe4d7-124">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="fe4d7-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fe4d7-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="fe4d7-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fe4d7-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="fe4d7-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fe4d7-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="fe4d7-127">Schema name</span></span>  <br/> |<span data-ttu-id="fe4d7-128">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="fe4d7-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="fe4d7-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="fe4d7-129">Validation file</span></span>  <br/> |<span data-ttu-id="fe4d7-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="fe4d7-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="fe4d7-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="fe4d7-131">Can be empty</span></span>  <br/> |<span data-ttu-id="fe4d7-132">False</span><span class="sxs-lookup"><span data-stu-id="fe4d7-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fe4d7-133">Ver también</span><span class="sxs-lookup"><span data-stu-id="fe4d7-133">See also</span></span>



- [<span data-ttu-id="fe4d7-134">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="fe4d7-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

