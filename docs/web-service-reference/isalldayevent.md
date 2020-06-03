---
title: IsAllDayEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsAllDayEvent
api_type:
- schema
ms.assetid: 29140a64-9d7a-4a14-a10d-c98197c9831b
description: El elemento IsAllDayEvent indica si un elemento de calendario o una convocatoria de reunión representa un evento de todo el día.
ms.openlocfilehash: f0c975deecf96e94599a47ef2c33e54a7d1a80b9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526539"
---
# <a name="isalldayevent"></a><span data-ttu-id="ba1c9-103">IsAllDayEvent</span><span class="sxs-lookup"><span data-stu-id="ba1c9-103">IsAllDayEvent</span></span>

<span data-ttu-id="ba1c9-104">El elemento **IsAllDayEvent** indica si un elemento de calendario o una convocatoria de reunión representa un evento de todo el día.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-104">The **IsAllDayEvent** element indicates whether a calendar item or meeting request represents an all-day event.</span></span> 
  
```xml
<IsAllDayEvent/>
```

 <span data-ttu-id="ba1c9-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="ba1c9-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ba1c9-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ba1c9-106">Attributes and elements</span></span>

<span data-ttu-id="ba1c9-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ba1c9-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="ba1c9-108">Attributes</span></span>

<span data-ttu-id="ba1c9-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ba1c9-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ba1c9-110">Child elements</span></span>

<span data-ttu-id="ba1c9-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ba1c9-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ba1c9-112">Parent elements</span></span>

|<span data-ttu-id="ba1c9-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ba1c9-113">**Element**</span></span>|<span data-ttu-id="ba1c9-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ba1c9-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ba1c9-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="ba1c9-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="ba1c9-116">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="ba1c9-117">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="ba1c9-117">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="ba1c9-118">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-118">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ba1c9-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="ba1c9-119">Text value</span></span>

<span data-ttu-id="ba1c9-120">Si se incluye este elemento, es necesario un valor de texto que represente un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-120">A text value that represents a Boolean value is required if this element is included.</span></span> <span data-ttu-id="ba1c9-121">Un valor de **true** indica que el elemento representa un evento de día completo.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-121">A value of **true** indicates that the item represents an all-day event.</span></span> <span data-ttu-id="ba1c9-122">Un valor de **false** indica que el elemento abarca menos de las horas laborables de un usuario.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-122">A value of **false** indicates that the item spans less than a user's working hours.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ba1c9-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ba1c9-123">Remarks</span></span>

<span data-ttu-id="ba1c9-124">Un evento de día completo abarca la duración de las horas laborables que se define para un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-124">An all-day event spans the duration of working hours that is defined for a mailbox.</span></span>
  
<span data-ttu-id="ba1c9-125">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="ba1c9-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ba1c9-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ba1c9-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ba1c9-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="ba1c9-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ba1c9-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ba1c9-128">Schema name</span></span>  <br/> |<span data-ttu-id="ba1c9-129">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="ba1c9-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="ba1c9-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ba1c9-130">Validation file</span></span>  <br/> |<span data-ttu-id="ba1c9-131">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="ba1c9-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ba1c9-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ba1c9-132">Can be empty</span></span>  <br/> |<span data-ttu-id="ba1c9-133">Falso</span><span class="sxs-lookup"><span data-stu-id="ba1c9-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ba1c9-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="ba1c9-134">See also</span></span>



- [<span data-ttu-id="ba1c9-135">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="ba1c9-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

