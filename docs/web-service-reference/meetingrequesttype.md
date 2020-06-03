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
description: El elemento MeetingRequestType describe el tipo de convocatoria de reunión.
ms.openlocfilehash: e90c44dd4124d698ca5ef7655f6429a7167673e6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465789"
---
# <a name="meetingrequesttype"></a><span data-ttu-id="60dd3-103">MeetingRequestType</span><span class="sxs-lookup"><span data-stu-id="60dd3-103">MeetingRequestType</span></span>

<span data-ttu-id="60dd3-104">El elemento **MeetingRequestType** describe el tipo de convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="60dd3-104">The **MeetingRequestType** element describes the type of the meeting request.</span></span> 
  
```xml
<MeetingRequestType/>
```

 <span data-ttu-id="60dd3-105">**MeetingRequestTypeType**</span><span class="sxs-lookup"><span data-stu-id="60dd3-105">**MeetingRequestTypeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="60dd3-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="60dd3-106">Attributes and elements</span></span>

<span data-ttu-id="60dd3-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="60dd3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="60dd3-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="60dd3-108">Attributes</span></span>

<span data-ttu-id="60dd3-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="60dd3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="60dd3-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="60dd3-110">Child elements</span></span>

<span data-ttu-id="60dd3-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="60dd3-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="60dd3-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="60dd3-112">Parent elements</span></span>

|<span data-ttu-id="60dd3-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="60dd3-113">**Element**</span></span>|<span data-ttu-id="60dd3-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="60dd3-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="60dd3-115">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="60dd3-115">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="60dd3-116">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="60dd3-116">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="60dd3-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="60dd3-117">Text value</span></span>

<span data-ttu-id="60dd3-118">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="60dd3-118">A text value is required.</span></span> <span data-ttu-id="60dd3-119">En la siguiente tabla se enumeran los valores de texto posibles para este elemento.</span><span class="sxs-lookup"><span data-stu-id="60dd3-119">The following table lists the possible text values for this element.</span></span>
  
|<span data-ttu-id="60dd3-120">**Valor**</span><span class="sxs-lookup"><span data-stu-id="60dd3-120">**Value**</span></span>|<span data-ttu-id="60dd3-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="60dd3-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="60dd3-122">FullUpdate</span><span class="sxs-lookup"><span data-stu-id="60dd3-122">FullUpdate</span></span>  <br/> |<span data-ttu-id="60dd3-123">Identifica la convocatoria de reunión como una actualización completa de una solicitud existente.</span><span class="sxs-lookup"><span data-stu-id="60dd3-123">Identifies the meeting request as a full update to an existing request.</span></span> <span data-ttu-id="60dd3-124">Una actualización completa ha actualizado el tiempo y el contenido informativo.</span><span class="sxs-lookup"><span data-stu-id="60dd3-124">A full update has updated time and informational content.</span></span>  <br/> |
|<span data-ttu-id="60dd3-125">InformationalUpdate</span><span class="sxs-lookup"><span data-stu-id="60dd3-125">InformationalUpdate</span></span>  <br/> |<span data-ttu-id="60dd3-126">Identifica la convocatoria de reunión como que solo contiene contenido informativo actualizado.</span><span class="sxs-lookup"><span data-stu-id="60dd3-126">Identifies the meeting request as only containing updated informational content.</span></span>  <br/> |
|<span data-ttu-id="60dd3-127">NewMeetingRequest</span><span class="sxs-lookup"><span data-stu-id="60dd3-127">NewMeetingRequest</span></span>  <br/> |<span data-ttu-id="60dd3-128">Identifica la convocatoria de reunión como una convocatoria de reunión nueva.</span><span class="sxs-lookup"><span data-stu-id="60dd3-128">Identifies the meeting request as a new meeting request.</span></span>  <br/> |
|<span data-ttu-id="60dd3-129">Ninguno</span><span class="sxs-lookup"><span data-stu-id="60dd3-129">None</span></span>  <br/> |<span data-ttu-id="60dd3-130">Indica que no se ha definido el tipo de convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="60dd3-130">Indicates that the meeting request type is not defined.</span></span>  <br/> |
|<span data-ttu-id="60dd3-131">Obsoleta</span><span class="sxs-lookup"><span data-stu-id="60dd3-131">Outdated</span></span>  <br/> |<span data-ttu-id="60dd3-132">Identifica la convocatoria de reunión como no actualizada.</span><span class="sxs-lookup"><span data-stu-id="60dd3-132">Identifies the meeting request as outdated.</span></span>  <br/> |
|<span data-ttu-id="60dd3-133">PrincipalWantsCopy</span><span class="sxs-lookup"><span data-stu-id="60dd3-133">PrincipalWantsCopy</span></span>  <br/> |<span data-ttu-id="60dd3-134">Indica que la convocatoria de reunión pertenece a una entidad de identidad que ha reenviado mensajes de reunión a un delegado y tiene sus copias marcadas como informativas.</span><span class="sxs-lookup"><span data-stu-id="60dd3-134">Indicates that the meeting request belongs to a principal who has forwarded meeting messages to a delegate and has his copies marked as informational.</span></span>  <br/> |
|<span data-ttu-id="60dd3-135">SilentUpdate</span><span class="sxs-lookup"><span data-stu-id="60dd3-135">SilentUpdate</span></span>  <br/> |<span data-ttu-id="60dd3-136">Identifica la convocatoria de reunión como una actualización silenciosa de una reunión existente.</span><span class="sxs-lookup"><span data-stu-id="60dd3-136">Identifies the meeting request as a silent update to an existing meeting.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="60dd3-137">Comentarios</span><span class="sxs-lookup"><span data-stu-id="60dd3-137">Remarks</span></span>

<span data-ttu-id="60dd3-138">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="60dd3-138">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="60dd3-139">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="60dd3-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="60dd3-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="60dd3-140">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="60dd3-141">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="60dd3-141">Schema Name</span></span>  <br/> |<span data-ttu-id="60dd3-142">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="60dd3-142">Types schema</span></span>  <br/> |
|<span data-ttu-id="60dd3-143">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="60dd3-143">Validation File</span></span>  <br/> |<span data-ttu-id="60dd3-144">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="60dd3-144">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="60dd3-145">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="60dd3-145">Can be Empty</span></span>  <br/> |<span data-ttu-id="60dd3-146">Falso</span><span class="sxs-lookup"><span data-stu-id="60dd3-146">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="60dd3-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="60dd3-147">See also</span></span>



- [<span data-ttu-id="60dd3-148">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="60dd3-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

