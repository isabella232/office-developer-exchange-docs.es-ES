---
title: Acciones
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Actions
api_type:
- schema
ms.assetid: c5aa96b1-2d8b-422f-8c2f-f118572ab23f
description: El elemento Actions representa el conjunto de acciones que están disponibles para su realización en un mensaje cuando se cumplan las condiciones.
ms.openlocfilehash: 2ac53778b583595fa8be07f2c5110a9e2df16eca
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465068"
---
# <a name="actions"></a><span data-ttu-id="62ad9-103">Acciones</span><span class="sxs-lookup"><span data-stu-id="62ad9-103">Actions</span></span>

<span data-ttu-id="62ad9-104">El elemento **Actions** representa el conjunto de acciones que están disponibles para su realización en un mensaje cuando se cumplan las condiciones.</span><span class="sxs-lookup"><span data-stu-id="62ad9-104">The **Actions** element represents the set of actions that are available to be taken on a message when the conditions are fulfilled.</span></span> 
  
[<span data-ttu-id="62ad9-105">Regla (RuleType)</span><span class="sxs-lookup"><span data-stu-id="62ad9-105">Rule (RuleType)</span></span>](rule-ruletype.md)
  
```XML
<Actions>
    <AssignCategories>
    <CopyToFolder>
    <Delete>
    <ForwardAsAttachmentToRecipients>
    <ForwardToRecipients>
    <MarkImportance>
    <MarkAsRead>
    <MoveToFolder>
    <PermanentDelete>
    <RedirectToRecipients>
    <SendSMSAlertToRecipients>
    <ServerReplyWithMessage>
    <StopProcessingRules>
</Actions>
```

 <span data-ttu-id="62ad9-106">**RuleActionsType**</span><span class="sxs-lookup"><span data-stu-id="62ad9-106">**RuleActionsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="62ad9-107">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="62ad9-107">Attributes and elements</span></span>

<span data-ttu-id="62ad9-108">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="62ad9-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="62ad9-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="62ad9-109">Attributes</span></span>

<span data-ttu-id="62ad9-110">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="62ad9-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="62ad9-111">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="62ad9-111">Child elements</span></span>

|<span data-ttu-id="62ad9-112">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="62ad9-112">**Element**</span></span>|<span data-ttu-id="62ad9-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="62ad9-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="62ad9-114">AssignCategories</span><span class="sxs-lookup"><span data-stu-id="62ad9-114">AssignCategories</span></span>](assigncategories.md) <br/> |<span data-ttu-id="62ad9-115">Representa las categorías que se marcan en los mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="62ad9-115">Represents the categories that are stamped on e-mail messages.</span></span>  <br/> |
|[<span data-ttu-id="62ad9-116">CopyToFolder</span><span class="sxs-lookup"><span data-stu-id="62ad9-116">CopyToFolder</span></span>](copytofolder.md) <br/> |<span data-ttu-id="62ad9-117">Identifica el identificador de la carpeta en la que se copiarán los elementos de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="62ad9-117">Identifies the ID of the folder that e-mail items will be copied to.</span></span>  <br/> |
|[<span data-ttu-id="62ad9-118">Eliminar</span><span class="sxs-lookup"><span data-stu-id="62ad9-118">Delete</span></span>](delete.md) <br/> |<span data-ttu-id="62ad9-119">Indica si los mensajes se moverán a la carpeta elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="62ad9-119">Indicates whether messages are to be moved to the Deleted Items folder.</span></span>  <br/> |
|[<span data-ttu-id="62ad9-120">ForwardAsAttachmentToRecipients</span><span class="sxs-lookup"><span data-stu-id="62ad9-120">ForwardAsAttachmentToRecipients</span></span>](forwardasattachmenttorecipients.md) <br/> |<span data-ttu-id="62ad9-121">Indica las direcciones de correo electrónico a las que se deben reenviar los mensajes como datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="62ad9-121">Indicates the e-mail addresses to which messages are to be forwarded as attachments.</span></span>  <br/> |
|[<span data-ttu-id="62ad9-122">ForwardToRecipients</span><span class="sxs-lookup"><span data-stu-id="62ad9-122">ForwardToRecipients</span></span>](forwardtorecipients.md) <br/> |<span data-ttu-id="62ad9-123">Indica las direcciones de correo electrónico a las que se van a reenviar los mensajes.</span><span class="sxs-lookup"><span data-stu-id="62ad9-123">Indicates the e-mail addresses to which messages are to be forwarded.</span></span>  <br/> |
|[<span data-ttu-id="62ad9-124">MarkImportance</span><span class="sxs-lookup"><span data-stu-id="62ad9-124">MarkImportance</span></span>](markimportance.md) <br/> |<span data-ttu-id="62ad9-125">Especifica la importancia que se va a estampar en los mensajes.</span><span class="sxs-lookup"><span data-stu-id="62ad9-125">Specifies the importance that is to be stamped on messages.</span></span>  <br/> |
|[<span data-ttu-id="62ad9-126">MarkAsRead</span><span class="sxs-lookup"><span data-stu-id="62ad9-126">MarkAsRead</span></span>](markasread.md) <br/> |<span data-ttu-id="62ad9-127">Indica si los mensajes se deben marcar como leídos.</span><span class="sxs-lookup"><span data-stu-id="62ad9-127">Indicates whether messages are to be marked as read.</span></span>  <br/> |
|[<span data-ttu-id="62ad9-128">MoveToFolder</span><span class="sxs-lookup"><span data-stu-id="62ad9-128">MoveToFolder</span></span>](movetofolder.md) <br/> |<span data-ttu-id="62ad9-129">Identifica el identificador de la carpeta a la que se moverán los elementos de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="62ad9-129">Identifies the ID of the folder that e-mail items will be moved to.</span></span>  <br/> |
|[<span data-ttu-id="62ad9-130">PermanentDelete</span><span class="sxs-lookup"><span data-stu-id="62ad9-130">PermanentDelete</span></span>](permanentdelete.md) <br/> |<span data-ttu-id="62ad9-131">Indica si los mensajes se eliminan permanentemente y no se guardan en la carpeta elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="62ad9-131">Indicates whether messages are to be permanently deleted and not saved to the Deleted Items folder.</span></span>  <br/> |
|[<span data-ttu-id="62ad9-132">RedirectToRecipients</span><span class="sxs-lookup"><span data-stu-id="62ad9-132">RedirectToRecipients</span></span>](redirecttorecipients.md) <br/> |<span data-ttu-id="62ad9-133">Indica las direcciones de correo electrónico a las que se van a redirigir los mensajes.</span><span class="sxs-lookup"><span data-stu-id="62ad9-133">Indicates the e-mail addresses to which messages are to be redirected.</span></span>  <br/> |
|[<span data-ttu-id="62ad9-134">SendSMSAlertToRecipients</span><span class="sxs-lookup"><span data-stu-id="62ad9-134">SendSMSAlertToRecipients</span></span>](sendsmsalerttorecipients.md) <br/> |<span data-ttu-id="62ad9-135">Indica los números de teléfono móvil a los que se enviará una alerta de servicio de mensajes cortos (SMS).</span><span class="sxs-lookup"><span data-stu-id="62ad9-135">Indicates the mobile phone numbers to which a Short Message Service (SMS) alert is to be sent.</span></span>  <br/> |
|[<span data-ttu-id="62ad9-136">ServerReplyWithMessage</span><span class="sxs-lookup"><span data-stu-id="62ad9-136">ServerReplyWithMessage</span></span>](serverreplywithmessage.md) <br/> |<span data-ttu-id="62ad9-137">Indicar.</span><span class="sxs-lookup"><span data-stu-id="62ad9-137">Indicates.</span></span> <span data-ttu-id="62ad9-138">IDENTIFICADOR del mensaje de plantilla que se va a enviar como respuesta a los mensajes entrantes.</span><span class="sxs-lookup"><span data-stu-id="62ad9-138">the ID of the template message that is to be sent as a reply to incoming messages.</span></span>  <br/> |
|[<span data-ttu-id="62ad9-139">StopProcessingRules</span><span class="sxs-lookup"><span data-stu-id="62ad9-139">StopProcessingRules</span></span>](stopprocessingrules.md) <br/> |<span data-ttu-id="62ad9-140">Indica si las reglas posteriores se deben evaluar.</span><span class="sxs-lookup"><span data-stu-id="62ad9-140">Indicates whether subsequent rules are to be evaluated.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="62ad9-141">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="62ad9-141">Parent elements</span></span>

|<span data-ttu-id="62ad9-142">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="62ad9-142">**Element**</span></span>|<span data-ttu-id="62ad9-143">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="62ad9-143">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="62ad9-144">Regla (RuleType)</span><span class="sxs-lookup"><span data-stu-id="62ad9-144">Rule (RuleType)</span></span>](rule-ruletype.md) <br/> |<span data-ttu-id="62ad9-145">Representa una sola regla en el buzón de un usuario.</span><span class="sxs-lookup"><span data-stu-id="62ad9-145">Represents a single rule in a user's mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="62ad9-146">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="62ad9-146">Text value</span></span>

<span data-ttu-id="62ad9-147">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="62ad9-147">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="62ad9-148">Comentarios</span><span class="sxs-lookup"><span data-stu-id="62ad9-148">Remarks</span></span>

<span data-ttu-id="62ad9-149">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="62ad9-149">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="62ad9-150">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="62ad9-150">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="62ad9-151">Namespace</span><span class="sxs-lookup"><span data-stu-id="62ad9-151">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="62ad9-152">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="62ad9-152">Schema Name</span></span>  <br/> |<span data-ttu-id="62ad9-153">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="62ad9-153">Types schema</span></span>  <br/> |
|<span data-ttu-id="62ad9-154">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="62ad9-154">Validation File</span></span>  <br/> |<span data-ttu-id="62ad9-155">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="62ad9-155">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="62ad9-156">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="62ad9-156">Can be Empty</span></span>  <br/> |<span data-ttu-id="62ad9-157">Verdadero</span><span class="sxs-lookup"><span data-stu-id="62ad9-157">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="62ad9-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="62ad9-158">See also</span></span>

- [<span data-ttu-id="62ad9-159">Condiciones</span><span class="sxs-lookup"><span data-stu-id="62ad9-159">Conditions</span></span>](conditions.md)
- [<span data-ttu-id="62ad9-160">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="62ad9-160">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

