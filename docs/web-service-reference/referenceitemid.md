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
description: El elemento ReferenceItemId identifica el elemento al que hace referencia el objeto Response.
ms.openlocfilehash: 3b77d75de91af8ec8fb7ae2d507377d1d976febf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457231"
---
# <a name="referenceitemid"></a><span data-ttu-id="7adcf-103">ReferenceItemId</span><span class="sxs-lookup"><span data-stu-id="7adcf-103">ReferenceItemId</span></span>

<span data-ttu-id="7adcf-104">El elemento **ReferenceItemId** identifica el elemento al que hace referencia el objeto Response.</span><span class="sxs-lookup"><span data-stu-id="7adcf-104">The **ReferenceItemId** element identifies the item to which the response object refers.</span></span> 
  
```xml
<ReferenceItemId Id="" ChangeKey="" />
```

 <span data-ttu-id="7adcf-105">**ItemIdType**</span><span class="sxs-lookup"><span data-stu-id="7adcf-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7adcf-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="7adcf-106">Attributes and elements</span></span>

<span data-ttu-id="7adcf-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="7adcf-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7adcf-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="7adcf-108">Attributes</span></span>

|<span data-ttu-id="7adcf-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="7adcf-109">**Attribute**</span></span>|<span data-ttu-id="7adcf-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7adcf-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7adcf-111">**Id**</span><span class="sxs-lookup"><span data-stu-id="7adcf-111">**Id**</span></span> <br/> |<span data-ttu-id="7adcf-112">Identifica un elemento específico en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="7adcf-112">Identifies a specific item in the Exchange store.</span></span>  <br/> |
|<span data-ttu-id="7adcf-113">**ChangeKey**</span><span class="sxs-lookup"><span data-stu-id="7adcf-113">**ChangeKey**</span></span> <br/> |<span data-ttu-id="7adcf-114">Identifica una versión específica de un elemento.</span><span class="sxs-lookup"><span data-stu-id="7adcf-114">Identifies a specific version of an item.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7adcf-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7adcf-115">Child elements</span></span>

<span data-ttu-id="7adcf-116">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="7adcf-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7adcf-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7adcf-117">Parent elements</span></span>

|<span data-ttu-id="7adcf-118">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7adcf-118">**Element**</span></span>|<span data-ttu-id="7adcf-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7adcf-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7adcf-120">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="7adcf-120">AcceptItem</span></span>](acceptitem.md) <br/> |<span data-ttu-id="7adcf-121">Representa una respuesta de aceptación para una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="7adcf-121">Represents an Accept reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="7adcf-122">AcceptSharingInvitation</span><span class="sxs-lookup"><span data-stu-id="7adcf-122">AcceptSharingInvitation</span></span>](acceptsharinginvitation.md) <br/> |<span data-ttu-id="7adcf-123">Representa una respuesta de aceptación para una invitación para uso compartido.</span><span class="sxs-lookup"><span data-stu-id="7adcf-123">Represents an Accept reply to a sharing invitation.</span></span>  <br/> |
|[<span data-ttu-id="7adcf-124">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="7adcf-124">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="7adcf-125">Representa el objeto de respuesta que se usa para cancelar una reunión.</span><span class="sxs-lookup"><span data-stu-id="7adcf-125">Represents the response object that is used to cancel a meeting.</span></span>  <br/> |
|[<span data-ttu-id="7adcf-126">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="7adcf-126">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="7adcf-127">Representa una respuesta de rechazo a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="7adcf-127">Represents a Decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="7adcf-128">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="7adcf-128">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="7adcf-129">Contiene un elemento de almacén de Exchange que se va a reenviar a los destinatarios.</span><span class="sxs-lookup"><span data-stu-id="7adcf-129">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="7adcf-130">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="7adcf-130">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="7adcf-131">Quita un elemento del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="7adcf-131">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="7adcf-132">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="7adcf-132">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="7adcf-133">Contiene una respuesta a todos los destinatarios identificados de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="7adcf-133">Contains a reply to all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="7adcf-134">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="7adcf-134">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="7adcf-135">Contiene una respuesta al creador de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="7adcf-135">Contains a reply to the creator of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="7adcf-136">SuppressReadReceipt</span><span class="sxs-lookup"><span data-stu-id="7adcf-136">SuppressReadReceipt</span></span>](suppressreadreceipt.md) <br/> |<span data-ttu-id="7adcf-137">Se usa para responder a solicitudes de confirmación de lectura.</span><span class="sxs-lookup"><span data-stu-id="7adcf-137">Used to respond to read receipt requests.</span></span>  <br/> |
|[<span data-ttu-id="7adcf-138">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="7adcf-138">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="7adcf-139">Representa una respuesta provisional a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="7adcf-139">Represents a Tentative reply to a meeting request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7adcf-140">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7adcf-140">Remarks</span></span>

<span data-ttu-id="7adcf-141">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange del equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="7adcf-141">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7adcf-142">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7adcf-142">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7adcf-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="7adcf-143">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7adcf-144">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="7adcf-144">Schema Name</span></span>  <br/> |<span data-ttu-id="7adcf-145">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="7adcf-145">Types schema</span></span>  <br/> |
|<span data-ttu-id="7adcf-146">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="7adcf-146">Validation File</span></span>  <br/> |<span data-ttu-id="7adcf-147">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="7adcf-147">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7adcf-148">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="7adcf-148">Can be Empty</span></span>  <br/> |<span data-ttu-id="7adcf-149">Falso</span><span class="sxs-lookup"><span data-stu-id="7adcf-149">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7adcf-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="7adcf-150">See also</span></span>



- [<span data-ttu-id="7adcf-151">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="7adcf-151">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

