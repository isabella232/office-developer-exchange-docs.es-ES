---
title: MailTips
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
description: El elemento de sugerencias de correo electrónico representa los valores para varios tipos de sugerencias de correo.
ms.openlocfilehash: 9bacdea7b4f3108f700ed102025445e01a73e69d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44447599"
---
# <a name="mailtips"></a><span data-ttu-id="6ef57-103">MailTips</span><span class="sxs-lookup"><span data-stu-id="6ef57-103">MailTips</span></span>

<span data-ttu-id="6ef57-104">El elemento de **sugerencias** de correo electrónico representa los valores para varios tipos de sugerencias de correo.</span><span class="sxs-lookup"><span data-stu-id="6ef57-104">The **MailTips** element represents values for various types of mail tips.</span></span> 
  
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

 <span data-ttu-id="6ef57-105">**Sugerencias de correo electrónico**</span><span class="sxs-lookup"><span data-stu-id="6ef57-105">**MailTips**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6ef57-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="6ef57-106">Attributes and elements</span></span>

<span data-ttu-id="6ef57-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="6ef57-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6ef57-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="6ef57-108">Attributes</span></span>

<span data-ttu-id="6ef57-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="6ef57-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6ef57-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6ef57-110">Child elements</span></span>

|<span data-ttu-id="6ef57-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6ef57-111">**Element**</span></span>|<span data-ttu-id="6ef57-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6ef57-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6ef57-113">RecipientAddress</span><span class="sxs-lookup"><span data-stu-id="6ef57-113">RecipientAddress</span></span>](recipientaddress.md) <br/> |<span data-ttu-id="6ef57-114">Representa el buzón del destinatario.</span><span class="sxs-lookup"><span data-stu-id="6ef57-114">Represents the mailbox of the recipient.</span></span>  <br/> |
|[<span data-ttu-id="6ef57-115">PendingMailTips</span><span class="sxs-lookup"><span data-stu-id="6ef57-115">PendingMailTips</span></span>](pendingmailtips.md) <br/> |<span data-ttu-id="6ef57-116">Indica que las sugerencias de correo de este elemento no se pudieron evaluar antes de que se agote el tiempo de espera de procesamiento del servidor.</span><span class="sxs-lookup"><span data-stu-id="6ef57-116">Indicates that the mail tips in this element could not be evaluated before the server's processing timeout expired.</span></span>  <br/> |
|[<span data-ttu-id="6ef57-117">Oficina</span><span class="sxs-lookup"><span data-stu-id="6ef57-117">OutOfOffice</span></span>](outofoffice.md) <br/> |<span data-ttu-id="6ef57-118">Representa el mensaje de respuesta y una hora de duración para el envío del mensaje de respuesta.</span><span class="sxs-lookup"><span data-stu-id="6ef57-118">Represents the response message and a duration time for sending the response message.</span></span>  <br/> |
|[<span data-ttu-id="6ef57-119">MailboxFull</span><span class="sxs-lookup"><span data-stu-id="6ef57-119">MailboxFull</span></span>](mailboxfull.md) <br/> |<span data-ttu-id="6ef57-120">Indica si el buzón del destinatario está lleno.</span><span class="sxs-lookup"><span data-stu-id="6ef57-120">Indicates whether the mailbox for the recipient is full.</span></span>  <br/> |
|[<span data-ttu-id="6ef57-121">CustomMailTip</span><span class="sxs-lookup"><span data-stu-id="6ef57-121">CustomMailTip</span></span>](custommailtip.md) <br/> |<span data-ttu-id="6ef57-122">Representa un mensaje personalizado de sugerencia de correo.</span><span class="sxs-lookup"><span data-stu-id="6ef57-122">Represents a customized mail tip message.</span></span>  <br/> |
|[<span data-ttu-id="6ef57-123">TotalMemberCount</span><span class="sxs-lookup"><span data-stu-id="6ef57-123">TotalMemberCount</span></span>](totalmembercount.md) <br/> |<span data-ttu-id="6ef57-124">Representa el número de todos los miembros de un grupo.</span><span class="sxs-lookup"><span data-stu-id="6ef57-124">Represents the count of all members in a group.</span></span>  <br/> |
|[<span data-ttu-id="6ef57-125">ExternalMemberCount</span><span class="sxs-lookup"><span data-stu-id="6ef57-125">ExternalMemberCount</span></span>](externalmembercount.md) <br/> |<span data-ttu-id="6ef57-126">Representa el número de miembros externos de un grupo.</span><span class="sxs-lookup"><span data-stu-id="6ef57-126">Represents the count of external members in a group.</span></span>  <br/> |
|[<span data-ttu-id="6ef57-127">MaxMessageSize</span><span class="sxs-lookup"><span data-stu-id="6ef57-127">MaxMessageSize</span></span>](maxmessagesize.md) <br/> |<span data-ttu-id="6ef57-128">Representa el tamaño máximo de mensaje que puede aceptar el destinatario.</span><span class="sxs-lookup"><span data-stu-id="6ef57-128">Represents the maximum message size the recipient can accept.</span></span>  <br/> |
|[<span data-ttu-id="6ef57-129">DeliveryRestricted</span><span class="sxs-lookup"><span data-stu-id="6ef57-129">DeliveryRestricted</span></span>](deliveryrestricted.md) <br/> |<span data-ttu-id="6ef57-130">Indica si las restricciones de entrega impedirán que el mensaje del remitente llegue al destinatario.</span><span class="sxs-lookup"><span data-stu-id="6ef57-130">Indicates whether delivery restrictions will prevent the sender's message from reaching the recipient.</span></span>  <br/> |
|[<span data-ttu-id="6ef57-131">IsModerated</span><span class="sxs-lookup"><span data-stu-id="6ef57-131">IsModerated</span></span>](ismoderated.md) <br/> |<span data-ttu-id="6ef57-132">Indica si el buzón del destinatario se modera.</span><span class="sxs-lookup"><span data-stu-id="6ef57-132">Indicates whether the recipient's mailbox is being moderated.</span></span>  <br/> |
|[<span data-ttu-id="6ef57-133">InvalidRecipient (sugerencias de correo)</span><span class="sxs-lookup"><span data-stu-id="6ef57-133">InvalidRecipient (MailTips)</span></span>](invalidrecipient-mailtips.md) <br/> |<span data-ttu-id="6ef57-134">Indica si el destinatario no es válido.</span><span class="sxs-lookup"><span data-stu-id="6ef57-134">Indicates whether the recipient is invalid.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6ef57-135">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6ef57-135">Parent elements</span></span>

|<span data-ttu-id="6ef57-136">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6ef57-136">**Element**</span></span>|<span data-ttu-id="6ef57-137">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6ef57-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6ef57-138">MailTipsResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="6ef57-138">MailTipsResponseMessageType</span></span>](mailtipsresponsemessagetype.md) <br/> |<span data-ttu-id="6ef57-139">Representa la configuración de sugerencias de correo.</span><span class="sxs-lookup"><span data-stu-id="6ef57-139">Represents mail tips settings.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6ef57-140">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="6ef57-140">Text value</span></span>

<span data-ttu-id="6ef57-141">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="6ef57-141">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6ef57-142">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6ef57-142">Remarks</span></span>

<span data-ttu-id="6ef57-143">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="6ef57-143">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6ef57-144">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="6ef57-144">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6ef57-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="6ef57-145">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="6ef57-146">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="6ef57-146">Schema Name</span></span>  <br/> |<span data-ttu-id="6ef57-147">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="6ef57-147">Messages schema</span></span>  <br/> |
|<span data-ttu-id="6ef57-148">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="6ef57-148">Validation File</span></span>  <br/> |<span data-ttu-id="6ef57-149">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="6ef57-149">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6ef57-150">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="6ef57-150">Can be Empty</span></span>  <br/> |<span data-ttu-id="6ef57-151">Falso</span><span class="sxs-lookup"><span data-stu-id="6ef57-151">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6ef57-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="6ef57-152">See also</span></span>



- [<span data-ttu-id="6ef57-153">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="6ef57-153">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

