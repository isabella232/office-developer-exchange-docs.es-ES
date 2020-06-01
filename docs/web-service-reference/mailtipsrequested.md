---
title: MailTipsRequested
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MailTipsRequested
api_type:
- schema
ms.assetid: 8037bbe5-a37f-4f77-8209-27a94f9095ef
description: El elemento MailTipsRequested contiene los tipos de sugerencias de correo solicitados desde el servicio.
ms.openlocfilehash: bcb2ebf15e628a04e8507f938d385cf113f2f2a3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465901"
---
# <a name="mailtipsrequested"></a><span data-ttu-id="26c18-103">MailTipsRequested</span><span class="sxs-lookup"><span data-stu-id="26c18-103">MailTipsRequested</span></span>

<span data-ttu-id="26c18-104">El elemento **MailTipsRequested** contiene los tipos de sugerencias de correo solicitados desde el servicio.</span><span class="sxs-lookup"><span data-stu-id="26c18-104">The **MailTipsRequested** element contains the types of mail tips requested from the service.</span></span> 
  
```XML
<MailTipsRequested/>
```

 <span data-ttu-id="26c18-105">**MailTipTypes**</span><span class="sxs-lookup"><span data-stu-id="26c18-105">**MailTipTypes**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="26c18-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="26c18-106">Attributes and elements</span></span>

<span data-ttu-id="26c18-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="26c18-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="26c18-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="26c18-108">Attributes</span></span>

<span data-ttu-id="26c18-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="26c18-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="26c18-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="26c18-110">Child elements</span></span>

<span data-ttu-id="26c18-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="26c18-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="26c18-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="26c18-112">Parent elements</span></span>

|<span data-ttu-id="26c18-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="26c18-113">**Element**</span></span>|<span data-ttu-id="26c18-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="26c18-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="26c18-115">GetMailTips</span><span class="sxs-lookup"><span data-stu-id="26c18-115">GetMailTips</span></span>](getmailtips.md) <br/> |<span data-ttu-id="26c18-116">Contiene los destinatarios y los tipos de sugerencias de correo que se van a recuperar.</span><span class="sxs-lookup"><span data-stu-id="26c18-116">Contains the recipients and types of mail tips to retrieve.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="26c18-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="26c18-117">Text value</span></span>

<span data-ttu-id="26c18-118">En la siguiente tabla se enumeran los valores posibles para el elemento **MailTipsRequested** .</span><span class="sxs-lookup"><span data-stu-id="26c18-118">The following table lists the possible values for the **MailTipsRequested** element.</span></span> 
  
|<span data-ttu-id="26c18-119">**Valor**</span><span class="sxs-lookup"><span data-stu-id="26c18-119">**Value**</span></span>|<span data-ttu-id="26c18-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="26c18-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="26c18-121">Todo</span><span class="sxs-lookup"><span data-stu-id="26c18-121">All</span></span>  <br/> |<span data-ttu-id="26c18-122">Representa todas las sugerencias de correo disponibles.</span><span class="sxs-lookup"><span data-stu-id="26c18-122">Represents all available mail tips.</span></span>  <br/> |
|<span data-ttu-id="26c18-123">OutOfOfficeMessage</span><span class="sxs-lookup"><span data-stu-id="26c18-123">OutOfOfficeMessage</span></span>  <br/> |<span data-ttu-id="26c18-124">Representa el mensaje de fuera de la oficina (OOF).</span><span class="sxs-lookup"><span data-stu-id="26c18-124">Represents the Out of Office (OOF) message.</span></span>  <br/> |
|<span data-ttu-id="26c18-125">MailboxFullStatus</span><span class="sxs-lookup"><span data-stu-id="26c18-125">MailboxFullStatus</span></span>  <br/> |<span data-ttu-id="26c18-126">Representa el estado de un buzón de correo lleno.</span><span class="sxs-lookup"><span data-stu-id="26c18-126">Represents the status for a mailbox that is full.</span></span>  <br/> |
|<span data-ttu-id="26c18-127">CustomMailTip</span><span class="sxs-lookup"><span data-stu-id="26c18-127">CustomMailTip</span></span>  <br/> |<span data-ttu-id="26c18-128">Representa una sugerencia de correo personalizada.</span><span class="sxs-lookup"><span data-stu-id="26c18-128">Represents a custom mail tip.</span></span>  <br/> |
|<span data-ttu-id="26c18-129">ExternalMemberCount</span><span class="sxs-lookup"><span data-stu-id="26c18-129">ExternalMemberCount</span></span>  <br/> |<span data-ttu-id="26c18-130">Representa el número de miembros externos.</span><span class="sxs-lookup"><span data-stu-id="26c18-130">Represents the count of external members.</span></span>  <br/> |
|<span data-ttu-id="26c18-131">TotalMemberCount</span><span class="sxs-lookup"><span data-stu-id="26c18-131">TotalMemberCount</span></span>  <br/> |<span data-ttu-id="26c18-132">Representa el número de todos los miembros.</span><span class="sxs-lookup"><span data-stu-id="26c18-132">Represents the count of all members.</span></span>  <br/> |
|<span data-ttu-id="26c18-133">MaxMessageSize</span><span class="sxs-lookup"><span data-stu-id="26c18-133">MaxMessageSize</span></span>  <br/> |<span data-ttu-id="26c18-134">Representa el tamaño máximo de mensaje que puede aceptar un destinatario.</span><span class="sxs-lookup"><span data-stu-id="26c18-134">Represents the maximum message size a recipient can accept.</span></span>  <br/> |
|<span data-ttu-id="26c18-135">DeliveryRestriction</span><span class="sxs-lookup"><span data-stu-id="26c18-135">DeliveryRestriction</span></span>  <br/> |<span data-ttu-id="26c18-136">Indica si las restricciones de entrega impedirán que el mensaje del remitente llegue al destinatario.</span><span class="sxs-lookup"><span data-stu-id="26c18-136">Indicates whether delivery restrictions will prevent the sender's message from reaching the recipient.</span></span>  <br/> |
|<span data-ttu-id="26c18-137">ModerationStatus</span><span class="sxs-lookup"><span data-stu-id="26c18-137">ModerationStatus</span></span>  <br/> |<span data-ttu-id="26c18-138">Indica si el mensaje del remitente será revisado por un moderador.</span><span class="sxs-lookup"><span data-stu-id="26c18-138">Indicates whether the sender's message will be reviewed by a moderator.</span></span>  <br/> |
|<span data-ttu-id="26c18-139">InvalidRecipient</span><span class="sxs-lookup"><span data-stu-id="26c18-139">InvalidRecipient</span></span>  <br/> |<span data-ttu-id="26c18-140">Indica si el destinatario no es válido.</span><span class="sxs-lookup"><span data-stu-id="26c18-140">Indicates whether the recipient is invalid.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="26c18-141">Comentarios</span><span class="sxs-lookup"><span data-stu-id="26c18-141">Remarks</span></span>

<span data-ttu-id="26c18-142">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="26c18-142">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="26c18-143">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="26c18-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="26c18-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="26c18-144">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="26c18-145">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="26c18-145">Schema Name</span></span>  <br/> |<span data-ttu-id="26c18-146">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="26c18-146">Messages schema</span></span>  <br/> |
|<span data-ttu-id="26c18-147">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="26c18-147">Validation File</span></span>  <br/> |<span data-ttu-id="26c18-148">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="26c18-148">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="26c18-149">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="26c18-149">Can be Empty</span></span>  <br/> |<span data-ttu-id="26c18-150">Falso</span><span class="sxs-lookup"><span data-stu-id="26c18-150">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="26c18-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="26c18-151">See also</span></span>



- [<span data-ttu-id="26c18-152">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="26c18-152">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

