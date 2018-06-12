---
title: Recursos
manager: sethgros
ms.date: 09/17/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Resources
api_type:
- schema
ms.assetid: a2133cf2-7c62-4f1c-b3aa-75f14d30dd74
description: El elemento de recursos representa un recurso para una reunión programado.
ms.openlocfilehash: 31f358414e53f55b983f7633fc9c67b0ce3ab645
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837166"
---
# <a name="resources"></a><span data-ttu-id="b3c83-103">Recursos</span><span class="sxs-lookup"><span data-stu-id="b3c83-103">Resources</span></span>

<span data-ttu-id="b3c83-104">El elemento de **recursos** representa un recurso para una reunión programado.</span><span class="sxs-lookup"><span data-stu-id="b3c83-104">The **Resources** element represents a scheduled resource for a meeting.</span></span> 
  
```xml
<Resources>
   <Attendee/>
</Resources>
```

 <span data-ttu-id="b3c83-105">**NonEmptyArrayOfAttendeesType**</span><span class="sxs-lookup"><span data-stu-id="b3c83-105">**NonEmptyArrayOfAttendeesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b3c83-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b3c83-106">Attributes and elements</span></span>

<span data-ttu-id="b3c83-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b3c83-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b3c83-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="b3c83-108">Attributes</span></span>

<span data-ttu-id="b3c83-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b3c83-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b3c83-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b3c83-110">Child elements</span></span>

|<span data-ttu-id="b3c83-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="b3c83-111">**Element**</span></span>|<span data-ttu-id="b3c83-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b3c83-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b3c83-113">Attendee</span><span class="sxs-lookup"><span data-stu-id="b3c83-113">Attendee</span></span>](attendee.md) <br/> |<span data-ttu-id="b3c83-114">Representa los asistentes y los recursos de una reunión.</span><span class="sxs-lookup"><span data-stu-id="b3c83-114">Represents attendees and resources for a meeting.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b3c83-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b3c83-115">Parent elements</span></span>

|<span data-ttu-id="b3c83-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="b3c83-116">**Element**</span></span>|<span data-ttu-id="b3c83-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b3c83-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b3c83-118">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="b3c83-118">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="b3c83-119">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="b3c83-119">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="b3c83-120">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="b3c83-120">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="b3c83-121">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="b3c83-121">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b3c83-122">Notas</span><span class="sxs-lookup"><span data-stu-id="b3c83-122">Remarks</span></span>

<span data-ttu-id="b3c83-123">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="b3c83-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b3c83-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b3c83-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b3c83-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b3c83-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b3c83-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b3c83-126">Schema name</span></span>  <br/> |<span data-ttu-id="b3c83-127">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="b3c83-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="b3c83-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b3c83-128">Validation file</span></span>  <br/> |<span data-ttu-id="b3c83-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b3c83-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b3c83-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b3c83-130">Can be empty</span></span>  <br/> |<span data-ttu-id="b3c83-131">False</span><span class="sxs-lookup"><span data-stu-id="b3c83-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b3c83-132">Ver también</span><span class="sxs-lookup"><span data-stu-id="b3c83-132">See also</span></span>



- [<span data-ttu-id="b3c83-133">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="b3c83-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

