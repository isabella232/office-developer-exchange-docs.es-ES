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
description: El elemento Resources representa un recurso programado para una reunión.
ms.openlocfilehash: 67b4ed93a67a48945845887aa2d08b5bfe0102d4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455593"
---
# <a name="resources"></a><span data-ttu-id="b63e8-103">Recursos</span><span class="sxs-lookup"><span data-stu-id="b63e8-103">Resources</span></span>

<span data-ttu-id="b63e8-104">El elemento **Resources** representa un recurso programado para una reunión.</span><span class="sxs-lookup"><span data-stu-id="b63e8-104">The **Resources** element represents a scheduled resource for a meeting.</span></span> 
  
```xml
<Resources>
   <Attendee/>
</Resources>
```

 <span data-ttu-id="b63e8-105">**NonEmptyArrayOfAttendeesType**</span><span class="sxs-lookup"><span data-stu-id="b63e8-105">**NonEmptyArrayOfAttendeesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b63e8-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b63e8-106">Attributes and elements</span></span>

<span data-ttu-id="b63e8-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b63e8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b63e8-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="b63e8-108">Attributes</span></span>

<span data-ttu-id="b63e8-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="b63e8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b63e8-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b63e8-110">Child elements</span></span>

|<span data-ttu-id="b63e8-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b63e8-111">**Element**</span></span>|<span data-ttu-id="b63e8-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b63e8-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b63e8-113">Asistente</span><span class="sxs-lookup"><span data-stu-id="b63e8-113">Attendee</span></span>](attendee.md) <br/> |<span data-ttu-id="b63e8-114">Representa los asistentes y los recursos de una reunión.</span><span class="sxs-lookup"><span data-stu-id="b63e8-114">Represents attendees and resources for a meeting.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b63e8-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b63e8-115">Parent elements</span></span>

|<span data-ttu-id="b63e8-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b63e8-116">**Element**</span></span>|<span data-ttu-id="b63e8-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b63e8-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b63e8-118">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="b63e8-118">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="b63e8-119">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="b63e8-119">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="b63e8-120">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="b63e8-120">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="b63e8-121">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="b63e8-121">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b63e8-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b63e8-122">Remarks</span></span>

<span data-ttu-id="b63e8-123">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="b63e8-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b63e8-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b63e8-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b63e8-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="b63e8-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b63e8-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b63e8-126">Schema name</span></span>  <br/> |<span data-ttu-id="b63e8-127">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="b63e8-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="b63e8-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b63e8-128">Validation file</span></span>  <br/> |<span data-ttu-id="b63e8-129">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="b63e8-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b63e8-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b63e8-130">Can be empty</span></span>  <br/> |<span data-ttu-id="b63e8-131">Falso</span><span class="sxs-lookup"><span data-stu-id="b63e8-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b63e8-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="b63e8-132">See also</span></span>



- [<span data-ttu-id="b63e8-133">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="b63e8-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

