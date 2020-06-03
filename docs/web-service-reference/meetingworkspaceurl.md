---
title: MeetingWorkspaceUrl
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MeetingWorkspaceUrl
api_type:
- schema
ms.assetid: 0ca942fe-8f57-4065-93ad-65790f9a04c3
description: El elemento MeetingWorkspaceUrl contiene la dirección URL del área de reuniones que se incluye en el elemento de calendario. Un área de reuniones es un sitio web compartido para planear la reunión y realizar un seguimiento de los resultados.
ms.openlocfilehash: cd4396e590ab1471278bd44b9a4e0009fe326eaf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466286"
---
# <a name="meetingworkspaceurl"></a><span data-ttu-id="aab21-104">MeetingWorkspaceUrl</span><span class="sxs-lookup"><span data-stu-id="aab21-104">MeetingWorkspaceUrl</span></span>

<span data-ttu-id="aab21-105">El elemento **MeetingWorkspaceUrl** contiene la dirección URL del área de reuniones que se incluye en el elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="aab21-105">The **MeetingWorkspaceUrl** element contains the URL for the meeting workspace that is included in the calendar item.</span></span> <span data-ttu-id="aab21-106">Un área de reuniones es un sitio web compartido para planear la reunión y realizar un seguimiento de los resultados.</span><span class="sxs-lookup"><span data-stu-id="aab21-106">A meeting workspace is a shared Web site for planning the meeting and tracking the results.</span></span> 
  
```xml
<MeetingWorkspaceUrl/>
```

 <span data-ttu-id="aab21-107">**string**</span><span class="sxs-lookup"><span data-stu-id="aab21-107">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="aab21-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="aab21-108">Attributes and elements</span></span>

<span data-ttu-id="aab21-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="aab21-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="aab21-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="aab21-110">Attributes</span></span>

<span data-ttu-id="aab21-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="aab21-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="aab21-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="aab21-112">Child elements</span></span>

<span data-ttu-id="aab21-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="aab21-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="aab21-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="aab21-114">Parent elements</span></span>

|<span data-ttu-id="aab21-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="aab21-115">**Element**</span></span>|<span data-ttu-id="aab21-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="aab21-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="aab21-117">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="aab21-117">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="aab21-118">Representa una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="aab21-118">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="aab21-119">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="aab21-119">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="aab21-120">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="aab21-120">Represents an Exchange calendar item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="aab21-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="aab21-121">Text value</span></span>

<span data-ttu-id="aab21-122">Si se usa este elemento, es necesario un valor de texto que represente una dirección URL.</span><span class="sxs-lookup"><span data-stu-id="aab21-122">A text value that represents a URL is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="aab21-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="aab21-123">Remarks</span></span>

<span data-ttu-id="aab21-124">La propiedad MeetingWorkspaceUrl es de lectura y escritura para el elemento de calendario del organizador.</span><span class="sxs-lookup"><span data-stu-id="aab21-124">The MeetingWorkspaceUrl property is read-writable for the organizer's calendar item.</span></span> <span data-ttu-id="aab21-125">Es de solo lectura para las convocatorias de reunión y para los elementos de calendario de los asistentes.</span><span class="sxs-lookup"><span data-stu-id="aab21-125">It is read-only for meeting requests and for attendees' calendar items.</span></span>
  
<span data-ttu-id="aab21-126">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="aab21-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="aab21-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="aab21-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aab21-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="aab21-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="aab21-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="aab21-129">Schema name</span></span>  <br/> |<span data-ttu-id="aab21-130">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="aab21-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="aab21-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="aab21-131">Validation file</span></span>  <br/> |<span data-ttu-id="aab21-132">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="aab21-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="aab21-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="aab21-133">Can be empty</span></span>  <br/> |<span data-ttu-id="aab21-134">Falso</span><span class="sxs-lookup"><span data-stu-id="aab21-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="aab21-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="aab21-135">See also</span></span>



- [<span data-ttu-id="aab21-136">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="aab21-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

