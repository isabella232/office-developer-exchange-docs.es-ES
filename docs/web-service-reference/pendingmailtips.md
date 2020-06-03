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
description: El elemento PendingMailTips indica que las sugerencias de correo de este elemento no se pudieron evaluar antes de que se agote el tiempo de espera de procesamiento del servidor.
ms.openlocfilehash: 715d68b367c3b7251c7406c10c1ec52dcd992a59
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529969"
---
# <a name="pendingmailtips"></a><span data-ttu-id="1bda8-103">PendingMailTips</span><span class="sxs-lookup"><span data-stu-id="1bda8-103">PendingMailTips</span></span>

<span data-ttu-id="1bda8-104">El elemento **PendingMailTips** indica que las sugerencias de correo de este elemento no se pudieron evaluar antes de que se agote el tiempo de espera de procesamiento del servidor.</span><span class="sxs-lookup"><span data-stu-id="1bda8-104">The **PendingMailTips** element indicates that the mail tips in this element could not be evaluated before the server's processing timeout expired.</span></span> 
  
```XML
<PendingMailTips>All | OutOfOfficeMessage | MailboxFullStatus | CustomMailTip | ExternalMemberCount | TotalMemberCount | MaxMessageSize | DeliveryRestriction | ModerateStatus | InvalidRecipient</PendingMailTips>
```

 <span data-ttu-id="1bda8-105">**MailTipTypes**</span><span class="sxs-lookup"><span data-stu-id="1bda8-105">**MailTipTypes**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1bda8-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="1bda8-106">Attributes and elements</span></span>

<span data-ttu-id="1bda8-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="1bda8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1bda8-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="1bda8-108">Attributes</span></span>

<span data-ttu-id="1bda8-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1bda8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1bda8-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1bda8-110">Child elements</span></span>

<span data-ttu-id="1bda8-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1bda8-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1bda8-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="1bda8-112">Parent elements</span></span>

|<span data-ttu-id="1bda8-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="1bda8-113">**Element**</span></span>|<span data-ttu-id="1bda8-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1bda8-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1bda8-115">Sugerencias de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="1bda8-115">MailTips</span></span>](mailtips.md) <br/> |<span data-ttu-id="1bda8-116">Representa los valores de distintos tipos de sugerencias de correo.</span><span class="sxs-lookup"><span data-stu-id="1bda8-116">Represents values for various types of mail tips.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1bda8-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="1bda8-117">Text value</span></span>

<span data-ttu-id="1bda8-118">En la siguiente tabla se enumeran los valores posibles para el elemento **PendingMailTips** .</span><span class="sxs-lookup"><span data-stu-id="1bda8-118">The following table lists the possible values for the **PendingMailTips** element.</span></span> 
  
|<span data-ttu-id="1bda8-119">**Valor**</span><span class="sxs-lookup"><span data-stu-id="1bda8-119">**Value**</span></span>|<span data-ttu-id="1bda8-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1bda8-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1bda8-121">Todo</span><span class="sxs-lookup"><span data-stu-id="1bda8-121">All</span></span>  <br/> |<span data-ttu-id="1bda8-122">Representa todas las sugerencias de correo disponibles.</span><span class="sxs-lookup"><span data-stu-id="1bda8-122">Represents all available mail tips.</span></span>  <br/> |
|<span data-ttu-id="1bda8-123">OutOfOfficeMessage</span><span class="sxs-lookup"><span data-stu-id="1bda8-123">OutOfOfficeMessage</span></span>  <br/> |<span data-ttu-id="1bda8-124">Representa el mensaje de fuera de la oficina (OOF).</span><span class="sxs-lookup"><span data-stu-id="1bda8-124">Represents the Out of Office (OOF) message.</span></span>  <br/> |
|<span data-ttu-id="1bda8-125">MailboxFullStatus</span><span class="sxs-lookup"><span data-stu-id="1bda8-125">MailboxFullStatus</span></span>  <br/> |<span data-ttu-id="1bda8-126">Representa el estado de un buzón de correo lleno.</span><span class="sxs-lookup"><span data-stu-id="1bda8-126">Represents the status for a mailbox being full.</span></span>  <br/> |
|<span data-ttu-id="1bda8-127">CustomMailTip</span><span class="sxs-lookup"><span data-stu-id="1bda8-127">CustomMailTip</span></span>  <br/> |<span data-ttu-id="1bda8-128">Representa una sugerencia de correo personalizada.</span><span class="sxs-lookup"><span data-stu-id="1bda8-128">Represents a custom mail tip.</span></span>  <br/> |
|<span data-ttu-id="1bda8-129">ExternalMemberCount</span><span class="sxs-lookup"><span data-stu-id="1bda8-129">ExternalMemberCount</span></span>  <br/> |<span data-ttu-id="1bda8-130">Representa el número de miembros externos.</span><span class="sxs-lookup"><span data-stu-id="1bda8-130">Represents the count of external members.</span></span>  <br/> |
|<span data-ttu-id="1bda8-131">TotalMemberCount</span><span class="sxs-lookup"><span data-stu-id="1bda8-131">TotalMemberCount</span></span>  <br/> |<span data-ttu-id="1bda8-132">Representa el número de todos los miembros.</span><span class="sxs-lookup"><span data-stu-id="1bda8-132">Represents the count of all members.</span></span>  <br/> |
|<span data-ttu-id="1bda8-133">MaxMessageSize</span><span class="sxs-lookup"><span data-stu-id="1bda8-133">MaxMessageSize</span></span>  <br/> |<span data-ttu-id="1bda8-134">Representa el tamaño máximo de mensaje que puede aceptar un destinatario.</span><span class="sxs-lookup"><span data-stu-id="1bda8-134">Represents the maximum message size a recipient can accept.</span></span>  <br/> |
|<span data-ttu-id="1bda8-135">DeliveryRestriction</span><span class="sxs-lookup"><span data-stu-id="1bda8-135">DeliveryRestriction</span></span>  <br/> |<span data-ttu-id="1bda8-136">Indica si las restricciones de entrega impedirán que el mensaje del remitente llegue al destinatario.</span><span class="sxs-lookup"><span data-stu-id="1bda8-136">Indicates whether delivery restrictions will prevent the sender's message from reaching the recipient.</span></span>  <br/> |
|<span data-ttu-id="1bda8-137">ModerationStatus</span><span class="sxs-lookup"><span data-stu-id="1bda8-137">ModerationStatus</span></span>  <br/> |<span data-ttu-id="1bda8-138">Indica si el mensaje del remitente será revisado por un moderador.</span><span class="sxs-lookup"><span data-stu-id="1bda8-138">Indicates whether the sender's message will be reviewed by a moderator.</span></span>  <br/> |
|<span data-ttu-id="1bda8-139">InvalidRecipient</span><span class="sxs-lookup"><span data-stu-id="1bda8-139">InvalidRecipient</span></span>  <br/> |<span data-ttu-id="1bda8-140">Indica si el destinatario no es válido.</span><span class="sxs-lookup"><span data-stu-id="1bda8-140">Indicates whether the recipient is invalid.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1bda8-141">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1bda8-141">Remarks</span></span>

<span data-ttu-id="1bda8-142">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="1bda8-142">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1bda8-143">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="1bda8-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1bda8-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="1bda8-144">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1bda8-145">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="1bda8-145">Schema Name</span></span>  <br/> |<span data-ttu-id="1bda8-146">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="1bda8-146">Types schema</span></span>  <br/> |
|<span data-ttu-id="1bda8-147">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="1bda8-147">Validation File</span></span>  <br/> |<span data-ttu-id="1bda8-148">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="1bda8-148">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1bda8-149">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="1bda8-149">Can be Empty</span></span>  <br/> |<span data-ttu-id="1bda8-150">Falso</span><span class="sxs-lookup"><span data-stu-id="1bda8-150">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1bda8-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="1bda8-151">See also</span></span>



- [<span data-ttu-id="1bda8-152">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="1bda8-152">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

