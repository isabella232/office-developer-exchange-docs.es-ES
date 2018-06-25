---
title: ReferenceItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ReferenceItemId
api_type:
- schema
ms.assetid: 8fd4bb12-a94b-43f5-be3b-f435684e311d
description: El elemento ReferenceItemId identifica el elemento al que hace referencia el objeto de respuesta.
ms.openlocfilehash: d29f2dfec8f2c23fe0ac8c84d2bb9029fce613d2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837032"
---
# <a name="referenceitemid"></a><span data-ttu-id="c7b20-103">ReferenceItemId</span><span class="sxs-lookup"><span data-stu-id="c7b20-103">ReferenceItemId</span></span>

<span data-ttu-id="c7b20-104">El elemento **ReferenceItemId** identifica el elemento al que hace referencia el objeto de respuesta.</span><span class="sxs-lookup"><span data-stu-id="c7b20-104">The **ReferenceItemId** element identifies the item to which the response object refers.</span></span> 
  
```xml
<ReferenceItemId Id="" ChangeKey="" />
```

 <span data-ttu-id="c7b20-105">**ItemIdType**</span><span class="sxs-lookup"><span data-stu-id="c7b20-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c7b20-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c7b20-106">Attributes and elements</span></span>

<span data-ttu-id="c7b20-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c7b20-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c7b20-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c7b20-108">Attributes</span></span>

|<span data-ttu-id="c7b20-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="c7b20-109">**Attribute**</span></span>|<span data-ttu-id="c7b20-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c7b20-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c7b20-111">**Id**</span><span class="sxs-lookup"><span data-stu-id="c7b20-111">**Id**</span></span> <br/> |<span data-ttu-id="c7b20-112">Identifica un elemento específico en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c7b20-112">Identifies a specific item in the Exchange store.</span></span>  <br/> |
|<span data-ttu-id="c7b20-113">**ChangeKey**</span><span class="sxs-lookup"><span data-stu-id="c7b20-113">**ChangeKey**</span></span> <br/> |<span data-ttu-id="c7b20-114">Identifica una versión específica de un elemento.</span><span class="sxs-lookup"><span data-stu-id="c7b20-114">Identifies a specific version of an item.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c7b20-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c7b20-115">Child elements</span></span>

<span data-ttu-id="c7b20-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c7b20-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c7b20-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c7b20-117">Parent elements</span></span>

|<span data-ttu-id="c7b20-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="c7b20-118">**Element**</span></span>|<span data-ttu-id="c7b20-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c7b20-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c7b20-120">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="c7b20-120">AcceptItem</span></span>](acceptitem.md) <br/> |<span data-ttu-id="c7b20-121">Representa una respuesta a Aceptar a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="c7b20-121">Represents an Accept reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="c7b20-122">AcceptSharingInvitation</span><span class="sxs-lookup"><span data-stu-id="c7b20-122">AcceptSharingInvitation</span></span>](acceptsharinginvitation.md) <br/> |<span data-ttu-id="c7b20-123">Representa una respuesta a Aceptar a una invitación para compartir.</span><span class="sxs-lookup"><span data-stu-id="c7b20-123">Represents an Accept reply to a sharing invitation.</span></span>  <br/> |
|[<span data-ttu-id="c7b20-124">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="c7b20-124">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="c7b20-125">Representa el objeto de respuesta que se usa para cancelar una reunión.</span><span class="sxs-lookup"><span data-stu-id="c7b20-125">Represents the response object that is used to cancel a meeting.</span></span>  <br/> |
|[<span data-ttu-id="c7b20-126">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="c7b20-126">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="c7b20-127">Representa una respuesta de rechazo a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="c7b20-127">Represents a Decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="c7b20-128">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="c7b20-128">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="c7b20-129">Contiene un elemento del almacén de Exchange reenviar a los destinatarios.</span><span class="sxs-lookup"><span data-stu-id="c7b20-129">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="c7b20-130">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="c7b20-130">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="c7b20-131">Quita un elemento desde el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c7b20-131">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="c7b20-132">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="c7b20-132">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="c7b20-133">Contiene una respuesta para todos los destinatarios identificados de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c7b20-133">Contains a reply to all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="c7b20-134">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="c7b20-134">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="c7b20-135">Contiene una respuesta para el creador de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c7b20-135">Contains a reply to the creator of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="c7b20-136">SuppressReadReceipt</span><span class="sxs-lookup"><span data-stu-id="c7b20-136">SuppressReadReceipt</span></span>](suppressreadreceipt.md) <br/> |<span data-ttu-id="c7b20-137">Se usa para responder a las solicitudes de confirmación de lectura.</span><span class="sxs-lookup"><span data-stu-id="c7b20-137">Used to respond to read receipt requests.</span></span>  <br/> |
|[<span data-ttu-id="c7b20-138">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="c7b20-138">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="c7b20-139">Representa un provisional responde a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="c7b20-139">Represents a Tentative reply to a meeting request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c7b20-140">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c7b20-140">Remarks</span></span>

<span data-ttu-id="c7b20-141">El esquema que describe este elemento se encuentra en el directorio Virtual de IIS que hospeda los servicios Web Exchange del equipo que ejecuta a Microsoft Exchange Server que tiene instalada la función del servidor acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="c7b20-141">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c7b20-142">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c7b20-142">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c7b20-143">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c7b20-143">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c7b20-144">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c7b20-144">Schema Name</span></span>  <br/> |<span data-ttu-id="c7b20-145">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="c7b20-145">Types schema</span></span>  <br/> |
|<span data-ttu-id="c7b20-146">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c7b20-146">Validation File</span></span>  <br/> |<span data-ttu-id="c7b20-147">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c7b20-147">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c7b20-148">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c7b20-148">Can be Empty</span></span>  <br/> |<span data-ttu-id="c7b20-149">False</span><span class="sxs-lookup"><span data-stu-id="c7b20-149">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c7b20-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="c7b20-150">See also</span></span>



- [<span data-ttu-id="c7b20-151">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="c7b20-151">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

