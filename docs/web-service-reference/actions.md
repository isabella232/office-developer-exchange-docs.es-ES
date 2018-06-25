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
description: El elemento Actions representa el conjunto de acciones que están disponibles para ser tomadas en un mensaje cuando se cumplen las condiciones.
ms.openlocfilehash: 093d2f28135c6077b6cea488591573af0182934b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763388"
---
# <a name="actions"></a><span data-ttu-id="f6975-103">Acciones</span><span class="sxs-lookup"><span data-stu-id="f6975-103">Actions</span></span>

<span data-ttu-id="f6975-104">El elemento **Actions** representa el conjunto de acciones que están disponibles para ser tomadas en un mensaje cuando se cumplen las condiciones.</span><span class="sxs-lookup"><span data-stu-id="f6975-104">The **Actions** element represents the set of actions that are available to be taken on a message when the conditions are fulfilled.</span></span> 
  
[<span data-ttu-id="f6975-105">Regla (RuleType)</span><span class="sxs-lookup"><span data-stu-id="f6975-105">Rule (RuleType)</span></span>](rule-ruletype.md)
  
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

 <span data-ttu-id="f6975-106">**RuleActionsType**</span><span class="sxs-lookup"><span data-stu-id="f6975-106">**RuleActionsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f6975-107">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f6975-107">Attributes and elements</span></span>

<span data-ttu-id="f6975-108">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f6975-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f6975-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="f6975-109">Attributes</span></span>

<span data-ttu-id="f6975-110">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f6975-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f6975-111">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f6975-111">Child elements</span></span>

|<span data-ttu-id="f6975-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="f6975-112">**Element**</span></span>|<span data-ttu-id="f6975-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f6975-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f6975-114">AssignCategories</span><span class="sxs-lookup"><span data-stu-id="f6975-114">AssignCategories</span></span>](assigncategories.md) <br/> |<span data-ttu-id="f6975-115">Representa las categorías que están marcadas en mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="f6975-115">Represents the categories that are stamped on e-mail messages.</span></span>  <br/> |
|[<span data-ttu-id="f6975-116">CopyToFolder</span><span class="sxs-lookup"><span data-stu-id="f6975-116">CopyToFolder</span></span>](copytofolder.md) <br/> |<span data-ttu-id="f6975-117">Identifica el identificador de la carpeta que se copiarán los elementos de correo electrónico a.</span><span class="sxs-lookup"><span data-stu-id="f6975-117">Identifies the ID of the folder that e-mail items will be copied to.</span></span>  <br/> |
|[<span data-ttu-id="f6975-118">Eliminar</span><span class="sxs-lookup"><span data-stu-id="f6975-118">Delete</span></span>](delete.md) <br/> |<span data-ttu-id="f6975-119">Indica si los mensajes se mueven a la carpeta Elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="f6975-119">Indicates whether messages are to be moved to the Deleted Items folder.</span></span>  <br/> |
|[<span data-ttu-id="f6975-120">ForwardAsAttachmentToRecipients</span><span class="sxs-lookup"><span data-stu-id="f6975-120">ForwardAsAttachmentToRecipients</span></span>](forwardasattachmenttorecipients.md) <br/> |<span data-ttu-id="f6975-121">Indica las direcciones de correo electrónico a la que los mensajes deben ser reenviado como datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="f6975-121">Indicates the e-mail addresses to which messages are to be forwarded as attachments.</span></span>  <br/> |
|[<span data-ttu-id="f6975-122">ForwardToRecipients</span><span class="sxs-lookup"><span data-stu-id="f6975-122">ForwardToRecipients</span></span>](forwardtorecipients.md) <br/> |<span data-ttu-id="f6975-123">Indica las direcciones de correo electrónico a la que los mensajes se se transfieran.</span><span class="sxs-lookup"><span data-stu-id="f6975-123">Indicates the e-mail addresses to which messages are to be forwarded.</span></span>  <br/> |
|[<span data-ttu-id="f6975-124">MarkImportance</span><span class="sxs-lookup"><span data-stu-id="f6975-124">MarkImportance</span></span>](markimportance.md) <br/> |<span data-ttu-id="f6975-125">Especifica la importancia que se mostrará en los mensajes.</span><span class="sxs-lookup"><span data-stu-id="f6975-125">Specifies the importance that is to be stamped on messages.</span></span>  <br/> |
|[<span data-ttu-id="f6975-126">MarkAsRead</span><span class="sxs-lookup"><span data-stu-id="f6975-126">MarkAsRead</span></span>](markasread.md) <br/> |<span data-ttu-id="f6975-127">Indica si los mensajes se marcan como leídos.</span><span class="sxs-lookup"><span data-stu-id="f6975-127">Indicates whether messages are to be marked as read.</span></span>  <br/> |
|[<span data-ttu-id="f6975-128">MoveToFolder</span><span class="sxs-lookup"><span data-stu-id="f6975-128">MoveToFolder</span></span>](movetofolder.md) <br/> |<span data-ttu-id="f6975-129">Identifica el identificador de la carpeta que se moverán los elementos de correo electrónico a.</span><span class="sxs-lookup"><span data-stu-id="f6975-129">Identifies the ID of the folder that e-mail items will be moved to.</span></span>  <br/> |
|[<span data-ttu-id="f6975-130">PermanentDelete</span><span class="sxs-lookup"><span data-stu-id="f6975-130">PermanentDelete</span></span>](permanentdelete.md) <br/> |<span data-ttu-id="f6975-131">Indica si los mensajes se eliminan permanentemente y no se ha guardado en la carpeta Elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="f6975-131">Indicates whether messages are to be permanently deleted and not saved to the Deleted Items folder.</span></span>  <br/> |
|[<span data-ttu-id="f6975-132">RedirectToRecipients</span><span class="sxs-lookup"><span data-stu-id="f6975-132">RedirectToRecipients</span></span>](redirecttorecipients.md) <br/> |<span data-ttu-id="f6975-133">Indica las direcciones de correo electrónico a la que los mensajes se que se redirija.</span><span class="sxs-lookup"><span data-stu-id="f6975-133">Indicates the e-mail addresses to which messages are to be redirected.</span></span>  <br/> |
|[<span data-ttu-id="f6975-134">SendSMSAlertToRecipients</span><span class="sxs-lookup"><span data-stu-id="f6975-134">SendSMSAlertToRecipients</span></span>](sendsmsalerttorecipients.md) <br/> |<span data-ttu-id="f6975-135">Indica el número de teléfono móvil a los que es una alerta de servicio de mensajes cortos (SMS) que se envíen.</span><span class="sxs-lookup"><span data-stu-id="f6975-135">Indicates the mobile phone numbers to which a Short Message Service (SMS) alert is to be sent.</span></span>  <br/> |
|[<span data-ttu-id="f6975-136">ServerReplyWithMessage</span><span class="sxs-lookup"><span data-stu-id="f6975-136">ServerReplyWithMessage</span></span>](serverreplywithmessage.md) <br/> |<span data-ttu-id="f6975-137">Indica.</span><span class="sxs-lookup"><span data-stu-id="f6975-137">Indicates.</span></span> <span data-ttu-id="f6975-138">el identificador del mensaje de plantilla que se envía como una respuesta a los mensajes entrantes.</span><span class="sxs-lookup"><span data-stu-id="f6975-138">the ID of the template message that is to be sent as a reply to incoming messages.</span></span>  <br/> |
|[<span data-ttu-id="f6975-139">StopProcessingRules</span><span class="sxs-lookup"><span data-stu-id="f6975-139">StopProcessingRules</span></span>](stopprocessingrules.md) <br/> |<span data-ttu-id="f6975-140">Indica si las reglas que siguen son que se deben evaluar.</span><span class="sxs-lookup"><span data-stu-id="f6975-140">Indicates whether subsequent rules are to be evaluated.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f6975-141">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f6975-141">Parent elements</span></span>

|<span data-ttu-id="f6975-142">**Element**</span><span class="sxs-lookup"><span data-stu-id="f6975-142">**Element**</span></span>|<span data-ttu-id="f6975-143">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f6975-143">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f6975-144">Regla (RuleType)</span><span class="sxs-lookup"><span data-stu-id="f6975-144">Rule (RuleType)</span></span>](rule-ruletype.md) <br/> |<span data-ttu-id="f6975-145">Representa una sola regla en el buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="f6975-145">Represents a single rule in a user's mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f6975-146">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="f6975-146">Text value</span></span>

<span data-ttu-id="f6975-147">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f6975-147">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f6975-148">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f6975-148">Remarks</span></span>

<span data-ttu-id="f6975-149">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="f6975-149">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f6975-150">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f6975-150">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f6975-151">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f6975-151">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f6975-152">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f6975-152">Schema Name</span></span>  <br/> |<span data-ttu-id="f6975-153">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="f6975-153">Types schema</span></span>  <br/> |
|<span data-ttu-id="f6975-154">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f6975-154">Validation File</span></span>  <br/> |<span data-ttu-id="f6975-155">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f6975-155">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f6975-156">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f6975-156">Can be Empty</span></span>  <br/> |<span data-ttu-id="f6975-157">Verdadero</span><span class="sxs-lookup"><span data-stu-id="f6975-157">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f6975-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="f6975-158">See also</span></span>

- [<span data-ttu-id="f6975-159">Condiciones</span><span class="sxs-lookup"><span data-stu-id="f6975-159">Conditions</span></span>](conditions.md)
- [<span data-ttu-id="f6975-160">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="f6975-160">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
