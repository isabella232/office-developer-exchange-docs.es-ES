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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836311"
---
# <a name="mailtips"></a><span data-ttu-id="b4bb5-103">Sugerencias de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="b4bb5-103">MailTips</span></span>

<span data-ttu-id="b4bb5-104">El elemento de **sugerencias de correo electrónico** representa los valores de distintos tipos de sugerencias de correo.</span><span class="sxs-lookup"><span data-stu-id="b4bb5-104">The **MailTips** element represents values for various types of mail tips.</span></span> 
  
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

 <span data-ttu-id="b4bb5-105">**Sugerencias de correo electrónico**</span><span class="sxs-lookup"><span data-stu-id="b4bb5-105">**MailTips**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b4bb5-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b4bb5-106">Attributes and elements</span></span>

<span data-ttu-id="b4bb5-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b4bb5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b4bb5-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="b4bb5-108">Attributes</span></span>

<span data-ttu-id="b4bb5-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b4bb5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b4bb5-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b4bb5-110">Child elements</span></span>

|<span data-ttu-id="b4bb5-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="b4bb5-111">**Element**</span></span>|<span data-ttu-id="b4bb5-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b4bb5-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b4bb5-113">RecipientAddress</span><span class="sxs-lookup"><span data-stu-id="b4bb5-113">RecipientAddress</span></span>](recipientaddress.md) <br/> |<span data-ttu-id="b4bb5-114">Representa el buzón de correo del destinatario.</span><span class="sxs-lookup"><span data-stu-id="b4bb5-114">Represents the mailbox of the recipient.</span></span>  <br/> |
|[<span data-ttu-id="b4bb5-115">PendingMailTips</span><span class="sxs-lookup"><span data-stu-id="b4bb5-115">PendingMailTips</span></span>](pendingmailtips.md) <br/> |<span data-ttu-id="b4bb5-116">Indica que las sugerencias de correo en este elemento no se podrían evaluar antes de tiempo de espera de procesamiento del servidor.</span><span class="sxs-lookup"><span data-stu-id="b4bb5-116">Indicates that the mail tips in this element could not be evaluated before the server's processing timeout expired.</span></span>  <br/> |
|[<span data-ttu-id="b4bb5-117">Fuera de la oficina</span><span class="sxs-lookup"><span data-stu-id="b4bb5-117">OutOfOffice</span></span>](outofoffice.md) <br/> |<span data-ttu-id="b4bb5-118">Representa el mensaje de respuesta y un tiempo de duración para enviar el mensaje de respuesta.</span><span class="sxs-lookup"><span data-stu-id="b4bb5-118">Represents the response message and a duration time for sending the response message.</span></span>  <br/> |
|[<span data-ttu-id="b4bb5-119">MailboxFull</span><span class="sxs-lookup"><span data-stu-id="b4bb5-119">MailboxFull</span></span>](mailboxfull.md) <br/> |<span data-ttu-id="b4bb5-120">Indica si el buzón del destinatario está lleno.</span><span class="sxs-lookup"><span data-stu-id="b4bb5-120">Indicates whether the mailbox for the recipient is full.</span></span>  <br/> |
|[<span data-ttu-id="b4bb5-121">CustomMailTip</span><span class="sxs-lookup"><span data-stu-id="b4bb5-121">CustomMailTip</span></span>](custommailtip.md) <br/> |<span data-ttu-id="b4bb5-122">Representa un mensaje de sugerencia de correo personalizado.</span><span class="sxs-lookup"><span data-stu-id="b4bb5-122">Represents a customized mail tip message.</span></span>  <br/> |
|[<span data-ttu-id="b4bb5-123">TotalMemberCount</span><span class="sxs-lookup"><span data-stu-id="b4bb5-123">TotalMemberCount</span></span>](totalmembercount.md) <br/> |<span data-ttu-id="b4bb5-124">Representa el recuento de todos los miembros de un grupo.</span><span class="sxs-lookup"><span data-stu-id="b4bb5-124">Represents the count of all members in a group.</span></span>  <br/> |
|[<span data-ttu-id="b4bb5-125">ExternalMemberCount</span><span class="sxs-lookup"><span data-stu-id="b4bb5-125">ExternalMemberCount</span></span>](externalmembercount.md) <br/> |<span data-ttu-id="b4bb5-126">Representa el recuento de miembros externos en un grupo.</span><span class="sxs-lookup"><span data-stu-id="b4bb5-126">Represents the count of external members in a group.</span></span>  <br/> |
|[<span data-ttu-id="b4bb5-127">MaxMessageSize</span><span class="sxs-lookup"><span data-stu-id="b4bb5-127">MaxMessageSize</span></span>](maxmessagesize.md) <br/> |<span data-ttu-id="b4bb5-128">Representa el tamaño máximo de mensaje que puede aceptar el destinatario.</span><span class="sxs-lookup"><span data-stu-id="b4bb5-128">Represents the maximum message size the recipient can accept.</span></span>  <br/> |
|[<span data-ttu-id="b4bb5-129">DeliveryRestricted</span><span class="sxs-lookup"><span data-stu-id="b4bb5-129">DeliveryRestricted</span></span>](deliveryrestricted.md) <br/> |<span data-ttu-id="b4bb5-130">Indica si las restricciones de entrega impedirá que el mensaje del remitente llegar al destinatario.</span><span class="sxs-lookup"><span data-stu-id="b4bb5-130">Indicates whether delivery restrictions will prevent the sender's message from reaching the recipient.</span></span>  <br/> |
|[<span data-ttu-id="b4bb5-131">IsModerated</span><span class="sxs-lookup"><span data-stu-id="b4bb5-131">IsModerated</span></span>](ismoderated.md) <br/> |<span data-ttu-id="b4bb5-132">Indica si se va a modera el buzón del destinatario.</span><span class="sxs-lookup"><span data-stu-id="b4bb5-132">Indicates whether the recipient's mailbox is being moderated.</span></span>  <br/> |
|[<span data-ttu-id="b4bb5-133">InvalidRecipient (sugerencias de correo electrónico)</span><span class="sxs-lookup"><span data-stu-id="b4bb5-133">InvalidRecipient (MailTips)</span></span>](invalidrecipient-mailtips.md) <br/> |<span data-ttu-id="b4bb5-134">Indica si el destinatario no es válido.</span><span class="sxs-lookup"><span data-stu-id="b4bb5-134">Indicates whether the recipient is invalid.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b4bb5-135">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b4bb5-135">Parent elements</span></span>

|<span data-ttu-id="b4bb5-136">**Element**</span><span class="sxs-lookup"><span data-stu-id="b4bb5-136">**Element**</span></span>|<span data-ttu-id="b4bb5-137">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b4bb5-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b4bb5-138">MailTipsResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="b4bb5-138">MailTipsResponseMessageType</span></span>](mailtipsresponsemessagetype.md) <br/> |<span data-ttu-id="b4bb5-139">Representa la configuración de sugerencias de correo.</span><span class="sxs-lookup"><span data-stu-id="b4bb5-139">Represents mail tips settings.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b4bb5-140">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="b4bb5-140">Text value</span></span>

<span data-ttu-id="b4bb5-141">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b4bb5-141">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b4bb5-142">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b4bb5-142">Remarks</span></span>

<span data-ttu-id="b4bb5-143">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="b4bb5-143">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b4bb5-144">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b4bb5-144">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b4bb5-145">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b4bb5-145">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b4bb5-146">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b4bb5-146">Schema Name</span></span>  <br/> |<span data-ttu-id="b4bb5-147">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="b4bb5-147">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b4bb5-148">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b4bb5-148">Validation File</span></span>  <br/> |<span data-ttu-id="b4bb5-149">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b4bb5-149">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b4bb5-150">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b4bb5-150">Can be Empty</span></span>  <br/> |<span data-ttu-id="b4bb5-151">False</span><span class="sxs-lookup"><span data-stu-id="b4bb5-151">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b4bb5-152">Ver también</span><span class="sxs-lookup"><span data-stu-id="b4bb5-152">See also</span></span>



- [<span data-ttu-id="b4bb5-153">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="b4bb5-153">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

