---
title: NetShowUrl
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- NetShowUrl
api_type:
- schema
ms.assetid: a5d48fc1-b141-422c-bcb0-05d0f9ba90dd
description: El elemento NetShowUrl especifica la dirección URL de una reunión en línea de Microsoft NetShow.
ms.openlocfilehash: 2440e6c1501331d715d0e5ceb31b3b928122f927
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836519"
---
# <a name="netshowurl"></a><span data-ttu-id="46c17-103">NetShowUrl</span><span class="sxs-lookup"><span data-stu-id="46c17-103">NetShowUrl</span></span>

<span data-ttu-id="46c17-104">El elemento **NetShowUrl** especifica la dirección URL de una reunión en línea de Microsoft NetShow.</span><span class="sxs-lookup"><span data-stu-id="46c17-104">The **NetShowUrl** element specifies the URL for a Microsoft NetShow online meeting.</span></span> 
  
```xml
<NetShowUrl/>
```

 <span data-ttu-id="46c17-105">**string**</span><span class="sxs-lookup"><span data-stu-id="46c17-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="46c17-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="46c17-106">Attributes and elements</span></span>

<span data-ttu-id="46c17-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="46c17-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="46c17-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="46c17-108">Attributes</span></span>

<span data-ttu-id="46c17-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="46c17-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="46c17-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="46c17-110">Child elements</span></span>

<span data-ttu-id="46c17-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="46c17-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="46c17-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="46c17-112">Parent elements</span></span>

|<span data-ttu-id="46c17-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="46c17-113">**Element**</span></span>|<span data-ttu-id="46c17-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="46c17-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="46c17-115">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="46c17-115">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="46c17-116">Representa una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="46c17-116">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="46c17-117">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="46c17-117">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="46c17-118">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="46c17-118">Represents an Exchange calendar item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="46c17-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="46c17-119">Text value</span></span>

<span data-ttu-id="46c17-120">Si se usa este elemento, es necesario un valor de texto que representa una dirección URL.</span><span class="sxs-lookup"><span data-stu-id="46c17-120">A text value that represents a URL is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="46c17-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="46c17-121">Remarks</span></span>

<span data-ttu-id="46c17-122">Esta propiedad NetShowUrl es de lectura escritura para el elemento de calendario del organizador.</span><span class="sxs-lookup"><span data-stu-id="46c17-122">This NetShowUrl property is read-writable for the organizer's calendar item.</span></span> <span data-ttu-id="46c17-123">Es de sólo lectura para las convocatorias de reunión y de los asistentes.</span><span class="sxs-lookup"><span data-stu-id="46c17-123">It is read-only for meeting requests and for attendees.</span></span>
  
<span data-ttu-id="46c17-124">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="46c17-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="46c17-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="46c17-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="46c17-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="46c17-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="46c17-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="46c17-127">Schema name</span></span>  <br/> |<span data-ttu-id="46c17-128">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="46c17-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="46c17-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="46c17-129">Validation file</span></span>  <br/> |<span data-ttu-id="46c17-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="46c17-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="46c17-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="46c17-131">Can be empty</span></span>  <br/> |<span data-ttu-id="46c17-132">False</span><span class="sxs-lookup"><span data-stu-id="46c17-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="46c17-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="46c17-133">See also</span></span>



- [<span data-ttu-id="46c17-134">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="46c17-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

