---
title: PendingMailTips
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PendingMailTips
api_type:
- schema
ms.assetid: 0cd70eea-8d36-4b1b-bf80-5edf359e7ba7
description: El elemento PendingMailTips indica que no se podrían evaluar las sugerencias de correo en este elemento antes de tiempo de espera de procesamiento del servidor.
ms.openlocfilehash: 73d597f6534ea29f7d26d6526c48631251521ae5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836704"
---
# <a name="pendingmailtips"></a><span data-ttu-id="e036e-103">PendingMailTips</span><span class="sxs-lookup"><span data-stu-id="e036e-103">PendingMailTips</span></span>

<span data-ttu-id="e036e-104">El elemento **PendingMailTips** indica que no se podrían evaluar las sugerencias de correo en este elemento antes de tiempo de espera de procesamiento del servidor.</span><span class="sxs-lookup"><span data-stu-id="e036e-104">The **PendingMailTips** element indicates that the mail tips in this element could not be evaluated before the server's processing timeout expired.</span></span> 
  
```XML
<PendingMailTips>All | OutOfOfficeMessage | MailboxFullStatus | CustomMailTip | ExternalMemberCount | TotalMemberCount | MaxMessageSize | DeliveryRestriction | ModerateStatus | InvalidRecipient</PendingMailTips>
```

 <span data-ttu-id="e036e-105">**MailTipTypes**</span><span class="sxs-lookup"><span data-stu-id="e036e-105">**MailTipTypes**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e036e-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e036e-106">Attributes and elements</span></span>

<span data-ttu-id="e036e-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e036e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e036e-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="e036e-108">Attributes</span></span>

<span data-ttu-id="e036e-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e036e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e036e-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e036e-110">Child elements</span></span>

<span data-ttu-id="e036e-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e036e-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e036e-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e036e-112">Parent elements</span></span>

|<span data-ttu-id="e036e-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="e036e-113">**Element**</span></span>|<span data-ttu-id="e036e-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e036e-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e036e-115">Sugerencias de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="e036e-115">MailTips</span></span>](mailtips.md) <br/> |<span data-ttu-id="e036e-116">Representa los valores de distintos tipos de sugerencias de correo.</span><span class="sxs-lookup"><span data-stu-id="e036e-116">Represents values for various types of mail tips.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e036e-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="e036e-117">Text value</span></span>

<span data-ttu-id="e036e-118">En la siguiente tabla se enumera los valores posibles para el elemento **PendingMailTips** .</span><span class="sxs-lookup"><span data-stu-id="e036e-118">The following table lists the possible values for the **PendingMailTips** element.</span></span> 
  
|<span data-ttu-id="e036e-119">**Valor**</span><span class="sxs-lookup"><span data-stu-id="e036e-119">**Value**</span></span>|<span data-ttu-id="e036e-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e036e-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e036e-121">Todos</span><span class="sxs-lookup"><span data-stu-id="e036e-121">All</span></span>  <br/> |<span data-ttu-id="e036e-122">Representa todas las sugerencias de correo disponibles.</span><span class="sxs-lookup"><span data-stu-id="e036e-122">Represents all available mail tips.</span></span>  <br/> |
|<span data-ttu-id="e036e-123">OutOfOfficeMessage</span><span class="sxs-lookup"><span data-stu-id="e036e-123">OutOfOfficeMessage</span></span>  <br/> |<span data-ttu-id="e036e-124">Representa el mensaje de fuera de oficina (OOF).</span><span class="sxs-lookup"><span data-stu-id="e036e-124">Represents the Out of Office (OOF) message.</span></span>  <br/> |
|<span data-ttu-id="e036e-125">MailboxFullStatus</span><span class="sxs-lookup"><span data-stu-id="e036e-125">MailboxFullStatus</span></span>  <br/> |<span data-ttu-id="e036e-126">Representa el estado de un buzón que se está completa.</span><span class="sxs-lookup"><span data-stu-id="e036e-126">Represents the status for a mailbox being full.</span></span>  <br/> |
|<span data-ttu-id="e036e-127">CustomMailTip</span><span class="sxs-lookup"><span data-stu-id="e036e-127">CustomMailTip</span></span>  <br/> |<span data-ttu-id="e036e-128">Representa una sugerencia de correo personalizado.</span><span class="sxs-lookup"><span data-stu-id="e036e-128">Represents a custom mail tip.</span></span>  <br/> |
|<span data-ttu-id="e036e-129">ExternalMemberCount</span><span class="sxs-lookup"><span data-stu-id="e036e-129">ExternalMemberCount</span></span>  <br/> |<span data-ttu-id="e036e-130">Representa el recuento de miembros externos.</span><span class="sxs-lookup"><span data-stu-id="e036e-130">Represents the count of external members.</span></span>  <br/> |
|<span data-ttu-id="e036e-131">TotalMemberCount</span><span class="sxs-lookup"><span data-stu-id="e036e-131">TotalMemberCount</span></span>  <br/> |<span data-ttu-id="e036e-132">Representa el recuento de todos los miembros.</span><span class="sxs-lookup"><span data-stu-id="e036e-132">Represents the count of all members.</span></span>  <br/> |
|<span data-ttu-id="e036e-133">MaxMessageSize</span><span class="sxs-lookup"><span data-stu-id="e036e-133">MaxMessageSize</span></span>  <br/> |<span data-ttu-id="e036e-134">Representa el tamaño máximo de mensaje que puede aceptar un destinatario.</span><span class="sxs-lookup"><span data-stu-id="e036e-134">Represents the maximum message size a recipient can accept.</span></span>  <br/> |
|<span data-ttu-id="e036e-135">DeliveryRestriction</span><span class="sxs-lookup"><span data-stu-id="e036e-135">DeliveryRestriction</span></span>  <br/> |<span data-ttu-id="e036e-136">Indica si las restricciones de entrega impedirá que el mensaje del remitente llegar al destinatario.</span><span class="sxs-lookup"><span data-stu-id="e036e-136">Indicates whether delivery restrictions will prevent the sender's message from reaching the recipient.</span></span>  <br/> |
|<span data-ttu-id="e036e-137">ModerationStatus</span><span class="sxs-lookup"><span data-stu-id="e036e-137">ModerationStatus</span></span>  <br/> |<span data-ttu-id="e036e-138">Indica si el mensaje del remitente será revisado por un moderador.</span><span class="sxs-lookup"><span data-stu-id="e036e-138">Indicates whether the sender's message will be reviewed by a moderator.</span></span>  <br/> |
|<span data-ttu-id="e036e-139">InvalidRecipient</span><span class="sxs-lookup"><span data-stu-id="e036e-139">InvalidRecipient</span></span>  <br/> |<span data-ttu-id="e036e-140">Indica si el destinatario no es válido.</span><span class="sxs-lookup"><span data-stu-id="e036e-140">Indicates whether the recipient is invalid.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e036e-141">Notas</span><span class="sxs-lookup"><span data-stu-id="e036e-141">Remarks</span></span>

<span data-ttu-id="e036e-142">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="e036e-142">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e036e-143">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e036e-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e036e-144">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e036e-144">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e036e-145">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e036e-145">Schema Name</span></span>  <br/> |<span data-ttu-id="e036e-146">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="e036e-146">Types schema</span></span>  <br/> |
|<span data-ttu-id="e036e-147">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e036e-147">Validation File</span></span>  <br/> |<span data-ttu-id="e036e-148">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e036e-148">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e036e-149">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e036e-149">Can be Empty</span></span>  <br/> |<span data-ttu-id="e036e-150">False</span><span class="sxs-lookup"><span data-stu-id="e036e-150">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e036e-151">Ver también</span><span class="sxs-lookup"><span data-stu-id="e036e-151">See also</span></span>



- [<span data-ttu-id="e036e-152">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="e036e-152">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

