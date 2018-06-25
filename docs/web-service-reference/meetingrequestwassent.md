---
title: MeetingRequestWasSent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MeetingRequestWasSent
api_type:
- schema
ms.assetid: 9192400a-8eef-4147-9f94-aa8ea91b41d8
description: El elemento MeetingRequestWasSent indica si se ha enviado una convocatoria de reunión a los asistentes solicitados.
ms.openlocfilehash: 0a87b1d773997e08ab96726375e4c8ce010faaf7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836438"
---
# <a name="meetingrequestwassent"></a><span data-ttu-id="a70ea-103">MeetingRequestWasSent</span><span class="sxs-lookup"><span data-stu-id="a70ea-103">MeetingRequestWasSent</span></span>

<span data-ttu-id="a70ea-104">El elemento **MeetingRequestWasSent** indica si se ha enviado una convocatoria de reunión a los asistentes solicitados.</span><span class="sxs-lookup"><span data-stu-id="a70ea-104">The **MeetingRequestWasSent** element indicates whether a meeting request has been sent to requested attendees.</span></span> 
  
```xml
<MeetingRequestWasSent/>
```

 <span data-ttu-id="a70ea-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="a70ea-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a70ea-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a70ea-106">Attributes and elements</span></span>

<span data-ttu-id="a70ea-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a70ea-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a70ea-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="a70ea-108">Attributes</span></span>

<span data-ttu-id="a70ea-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a70ea-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a70ea-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a70ea-110">Child elements</span></span>

<span data-ttu-id="a70ea-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a70ea-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a70ea-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a70ea-112">Parent elements</span></span>

|<span data-ttu-id="a70ea-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="a70ea-113">**Element**</span></span>|<span data-ttu-id="a70ea-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a70ea-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a70ea-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="a70ea-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="a70ea-116">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="a70ea-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="a70ea-117">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="a70ea-117">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="a70ea-118">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="a70ea-118">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a70ea-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="a70ea-119">Text value</span></span>

<span data-ttu-id="a70ea-120">Si este elemento se incluye, se requiere un valor de texto que representa un valor de tipo Boolean.</span><span class="sxs-lookup"><span data-stu-id="a70ea-120">A text value that represents a Boolean value is required if this element is included.</span></span> <span data-ttu-id="a70ea-121">Un valor de **true** indica que se ha enviado una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="a70ea-121">A value of **true** indicates that a meeting request was sent.</span></span> <span data-ttu-id="a70ea-122">Un valor de **false** indica que no se ha enviado una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="a70ea-122">A value of **false** indicates that a meeting request has not been sent.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a70ea-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a70ea-123">Remarks</span></span>

<span data-ttu-id="a70ea-124">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="a70ea-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a70ea-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a70ea-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a70ea-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a70ea-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a70ea-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a70ea-127">Schema name</span></span>  <br/> |<span data-ttu-id="a70ea-128">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="a70ea-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="a70ea-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a70ea-129">Validation file</span></span>  <br/> |<span data-ttu-id="a70ea-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a70ea-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a70ea-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a70ea-131">Can be empty</span></span>  <br/> |<span data-ttu-id="a70ea-132">False</span><span class="sxs-lookup"><span data-stu-id="a70ea-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a70ea-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="a70ea-133">See also</span></span>



- [<span data-ttu-id="a70ea-134">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="a70ea-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

