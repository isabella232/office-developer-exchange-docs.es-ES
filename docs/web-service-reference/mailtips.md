---
title: Sugerencias de correo electrónico
manager: sethgros
ms.date: 09/17/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MailTips
api_type:
- schema
ms.assetid: c1cba493-bccc-4b8e-be8e-bfa8a8b10882
description: El elemento de sugerencias de correo electrónico representa los valores de distintos tipos de sugerencias de correo.
ms.openlocfilehash: 3a2e95225b09fd2d81db32f821ea3069ab7e7852
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836311"
---
# <a name="mailtips"></a><span data-ttu-id="fd768-103">Sugerencias de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="fd768-103">MailTips</span></span>

<span data-ttu-id="fd768-104">El elemento de **sugerencias de correo electrónico** representa los valores de distintos tipos de sugerencias de correo.</span><span class="sxs-lookup"><span data-stu-id="fd768-104">The **MailTips** element represents values for various types of mail tips.</span></span> 
  
```XML
<MailTips>
   <RecipientAddress/>
   <PendingMailTips/>
   <OutOfOffice/>
   <MailboxFull/>
   <CustomMailTip/>
   <TotalMemberCount/>
   <ExternalMemberCount/>
   <MaxMessageSize/>
   <DeliveryRestricted/>
   <IsModerated/>
   <InvalidRecipient/>
</MailTips>
```

 <span data-ttu-id="fd768-105">**Sugerencias de correo electrónico**</span><span class="sxs-lookup"><span data-stu-id="fd768-105">**MailTips**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fd768-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="fd768-106">Attributes and elements</span></span>

<span data-ttu-id="fd768-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="fd768-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fd768-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="fd768-108">Attributes</span></span>

<span data-ttu-id="fd768-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="fd768-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fd768-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="fd768-110">Child elements</span></span>

|<span data-ttu-id="fd768-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="fd768-111">**Element**</span></span>|<span data-ttu-id="fd768-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fd768-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fd768-113">RecipientAddress</span><span class="sxs-lookup"><span data-stu-id="fd768-113">RecipientAddress</span></span>](recipientaddress.md) <br/> |<span data-ttu-id="fd768-114">Representa el buzón de correo del destinatario.</span><span class="sxs-lookup"><span data-stu-id="fd768-114">Represents the mailbox of the recipient.</span></span>  <br/> |
|[<span data-ttu-id="fd768-115">PendingMailTips</span><span class="sxs-lookup"><span data-stu-id="fd768-115">PendingMailTips</span></span>](pendingmailtips.md) <br/> |<span data-ttu-id="fd768-116">Indica que las sugerencias de correo en este elemento no se podrían evaluar antes de tiempo de espera de procesamiento del servidor.</span><span class="sxs-lookup"><span data-stu-id="fd768-116">Indicates that the mail tips in this element could not be evaluated before the server's processing timeout expired.</span></span>  <br/> |
|[<span data-ttu-id="fd768-117">Fuera de la oficina</span><span class="sxs-lookup"><span data-stu-id="fd768-117">OutOfOffice</span></span>](outofoffice.md) <br/> |<span data-ttu-id="fd768-118">Representa el mensaje de respuesta y un tiempo de duración para enviar el mensaje de respuesta.</span><span class="sxs-lookup"><span data-stu-id="fd768-118">Represents the response message and a duration time for sending the response message.</span></span>  <br/> |
|[<span data-ttu-id="fd768-119">MailboxFull</span><span class="sxs-lookup"><span data-stu-id="fd768-119">MailboxFull</span></span>](mailboxfull.md) <br/> |<span data-ttu-id="fd768-120">Indica si el buzón del destinatario está lleno.</span><span class="sxs-lookup"><span data-stu-id="fd768-120">Indicates whether the mailbox for the recipient is full.</span></span>  <br/> |
|[<span data-ttu-id="fd768-121">CustomMailTip</span><span class="sxs-lookup"><span data-stu-id="fd768-121">CustomMailTip</span></span>](custommailtip.md) <br/> |<span data-ttu-id="fd768-122">Representa un mensaje de sugerencia de correo personalizado.</span><span class="sxs-lookup"><span data-stu-id="fd768-122">Represents a customized mail tip message.</span></span>  <br/> |
|[<span data-ttu-id="fd768-123">TotalMemberCount</span><span class="sxs-lookup"><span data-stu-id="fd768-123">TotalMemberCount</span></span>](totalmembercount.md) <br/> |<span data-ttu-id="fd768-124">Representa el recuento de todos los miembros de un grupo.</span><span class="sxs-lookup"><span data-stu-id="fd768-124">Represents the count of all members in a group.</span></span>  <br/> |
|[<span data-ttu-id="fd768-125">ExternalMemberCount</span><span class="sxs-lookup"><span data-stu-id="fd768-125">ExternalMemberCount</span></span>](externalmembercount.md) <br/> |<span data-ttu-id="fd768-126">Representa el recuento de miembros externos en un grupo.</span><span class="sxs-lookup"><span data-stu-id="fd768-126">Represents the count of external members in a group.</span></span>  <br/> |
|[<span data-ttu-id="fd768-127">MaxMessageSize</span><span class="sxs-lookup"><span data-stu-id="fd768-127">MaxMessageSize</span></span>](maxmessagesize.md) <br/> |<span data-ttu-id="fd768-128">Representa el tamaño máximo de mensaje que puede aceptar el destinatario.</span><span class="sxs-lookup"><span data-stu-id="fd768-128">Represents the maximum message size the recipient can accept.</span></span>  <br/> |
|[<span data-ttu-id="fd768-129">DeliveryRestricted</span><span class="sxs-lookup"><span data-stu-id="fd768-129">DeliveryRestricted</span></span>](deliveryrestricted.md) <br/> |<span data-ttu-id="fd768-130">Indica si las restricciones de entrega impedirá que el mensaje del remitente llegar al destinatario.</span><span class="sxs-lookup"><span data-stu-id="fd768-130">Indicates whether delivery restrictions will prevent the sender's message from reaching the recipient.</span></span>  <br/> |
|[<span data-ttu-id="fd768-131">IsModerated</span><span class="sxs-lookup"><span data-stu-id="fd768-131">IsModerated</span></span>](ismoderated.md) <br/> |<span data-ttu-id="fd768-132">Indica si se va a modera el buzón del destinatario.</span><span class="sxs-lookup"><span data-stu-id="fd768-132">Indicates whether the recipient's mailbox is being moderated.</span></span>  <br/> |
|[<span data-ttu-id="fd768-133">InvalidRecipient (sugerencias de correo electrónico)</span><span class="sxs-lookup"><span data-stu-id="fd768-133">InvalidRecipient (MailTips)</span></span>](invalidrecipient-mailtips.md) <br/> |<span data-ttu-id="fd768-134">Indica si el destinatario no es válido.</span><span class="sxs-lookup"><span data-stu-id="fd768-134">Indicates whether the recipient is invalid.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="fd768-135">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="fd768-135">Parent elements</span></span>

|<span data-ttu-id="fd768-136">**Element**</span><span class="sxs-lookup"><span data-stu-id="fd768-136">**Element**</span></span>|<span data-ttu-id="fd768-137">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fd768-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fd768-138">MailTipsResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="fd768-138">MailTipsResponseMessageType</span></span>](mailtipsresponsemessagetype.md) <br/> |<span data-ttu-id="fd768-139">Representa la configuración de sugerencias de correo.</span><span class="sxs-lookup"><span data-stu-id="fd768-139">Represents mail tips settings.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="fd768-140">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="fd768-140">Text value</span></span>

<span data-ttu-id="fd768-141">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="fd768-141">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fd768-142">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fd768-142">Remarks</span></span>

<span data-ttu-id="fd768-143">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="fd768-143">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fd768-144">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="fd768-144">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fd768-145">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="fd768-145">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="fd768-146">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="fd768-146">Schema Name</span></span>  <br/> |<span data-ttu-id="fd768-147">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="fd768-147">Messages schema</span></span>  <br/> |
|<span data-ttu-id="fd768-148">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="fd768-148">Validation File</span></span>  <br/> |<span data-ttu-id="fd768-149">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="fd768-149">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="fd768-150">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="fd768-150">Can be Empty</span></span>  <br/> |<span data-ttu-id="fd768-151">False</span><span class="sxs-lookup"><span data-stu-id="fd768-151">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fd768-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="fd768-152">See also</span></span>



- [<span data-ttu-id="fd768-153">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="fd768-153">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

