---
title: MeetingRequestType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MeetingRequestType
api_type:
- schema
ms.assetid: bcd5c97c-19aa-4b1d-a8e8-e8c4bd473dd9
description: El elemento MeetingRequestType describe el tipo de la convocatoria de reunión.
ms.openlocfilehash: 7269587e2fa72aeb9070a7b53ee9215829729329
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836432"
---
# <a name="meetingrequesttype"></a><span data-ttu-id="60622-103">MeetingRequestType</span><span class="sxs-lookup"><span data-stu-id="60622-103">MeetingRequestType</span></span>

<span data-ttu-id="60622-104">El elemento **MeetingRequestType** describe el tipo de la convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="60622-104">The **MeetingRequestType** element describes the type of the meeting request.</span></span> 
  
```xml
<MeetingRequestType/>
```

 <span data-ttu-id="60622-105">**MeetingRequestTypeType**</span><span class="sxs-lookup"><span data-stu-id="60622-105">**MeetingRequestTypeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="60622-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="60622-106">Attributes and elements</span></span>

<span data-ttu-id="60622-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="60622-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="60622-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="60622-108">Attributes</span></span>

<span data-ttu-id="60622-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="60622-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="60622-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="60622-110">Child elements</span></span>

<span data-ttu-id="60622-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="60622-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="60622-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="60622-112">Parent elements</span></span>

|<span data-ttu-id="60622-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="60622-113">**Element**</span></span>|<span data-ttu-id="60622-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="60622-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="60622-115">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="60622-115">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="60622-116">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="60622-116">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="60622-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="60622-117">Text value</span></span>

<span data-ttu-id="60622-118">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="60622-118">A text value is required.</span></span> <span data-ttu-id="60622-119">En la siguiente tabla se enumera los posibles valores de texto para este elemento.</span><span class="sxs-lookup"><span data-stu-id="60622-119">The following table lists the possible text values for this element.</span></span>
  
|<span data-ttu-id="60622-120">**Valor**</span><span class="sxs-lookup"><span data-stu-id="60622-120">**Value**</span></span>|<span data-ttu-id="60622-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="60622-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="60622-122">FullUpdate</span><span class="sxs-lookup"><span data-stu-id="60622-122">FullUpdate</span></span>  <br/> |<span data-ttu-id="60622-123">Identifica la convocatoria de reunión como una actualización completa a una solicitud de existente.</span><span class="sxs-lookup"><span data-stu-id="60622-123">Identifies the meeting request as a full update to an existing request.</span></span> <span data-ttu-id="60622-124">Se actualizó una actualización completa tiempo y contenido informativo.</span><span class="sxs-lookup"><span data-stu-id="60622-124">A full update has updated time and informational content.</span></span>  <br/> |
|<span data-ttu-id="60622-125">InformationalUpdate</span><span class="sxs-lookup"><span data-stu-id="60622-125">InformationalUpdate</span></span>  <br/> |<span data-ttu-id="60622-126">Identifica la convocatoria de reunión como sólo que contiene el contenido informativo actualizado.</span><span class="sxs-lookup"><span data-stu-id="60622-126">Identifies the meeting request as only containing updated informational content.</span></span>  <br/> |
|<span data-ttu-id="60622-127">NewMeetingRequest</span><span class="sxs-lookup"><span data-stu-id="60622-127">NewMeetingRequest</span></span>  <br/> |<span data-ttu-id="60622-128">Identifica la convocatoria de reunión como una nueva convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="60622-128">Identifies the meeting request as a new meeting request.</span></span>  <br/> |
|<span data-ttu-id="60622-129">None</span><span class="sxs-lookup"><span data-stu-id="60622-129">None</span></span>  <br/> |<span data-ttu-id="60622-130">Indica que el tipo de solicitud de la reunión no se ha definido.</span><span class="sxs-lookup"><span data-stu-id="60622-130">Indicates that the meeting request type is not defined.</span></span>  <br/> |
|<span data-ttu-id="60622-131">Obsoleto</span><span class="sxs-lookup"><span data-stu-id="60622-131">Outdated</span></span>  <br/> |<span data-ttu-id="60622-132">Identifica la convocatoria de reunión como obsoleto.</span><span class="sxs-lookup"><span data-stu-id="60622-132">Identifies the meeting request as outdated.</span></span>  <br/> |
|<span data-ttu-id="60622-133">PrincipalWantsCopy</span><span class="sxs-lookup"><span data-stu-id="60622-133">PrincipalWantsCopy</span></span>  <br/> |<span data-ttu-id="60622-134">Indica que la convocatoria de reunión pertenece a una entidad de seguridad que se reenvió los mensajes de reunión a un delegado y tiene sus copias marcados como informativos.</span><span class="sxs-lookup"><span data-stu-id="60622-134">Indicates that the meeting request belongs to a principal who has forwarded meeting messages to a delegate and has his copies marked as informational.</span></span>  <br/> |
|<span data-ttu-id="60622-135">SilentUpdate</span><span class="sxs-lookup"><span data-stu-id="60622-135">SilentUpdate</span></span>  <br/> |<span data-ttu-id="60622-136">Identifica la convocatoria de reunión como una actualización silenciosa a una reunión existente.</span><span class="sxs-lookup"><span data-stu-id="60622-136">Identifies the meeting request as a silent update to an existing meeting.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="60622-137">Comentarios</span><span class="sxs-lookup"><span data-stu-id="60622-137">Remarks</span></span>

<span data-ttu-id="60622-138">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="60622-138">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="60622-139">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="60622-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="60622-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="60622-140">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="60622-141">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="60622-141">Schema Name</span></span>  <br/> |<span data-ttu-id="60622-142">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="60622-142">Types schema</span></span>  <br/> |
|<span data-ttu-id="60622-143">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="60622-143">Validation File</span></span>  <br/> |<span data-ttu-id="60622-144">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="60622-144">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="60622-145">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="60622-145">Can be Empty</span></span>  <br/> |<span data-ttu-id="60622-146">False</span><span class="sxs-lookup"><span data-stu-id="60622-146">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="60622-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="60622-147">See also</span></span>



- [<span data-ttu-id="60622-148">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="60622-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

