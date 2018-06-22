---
title: Condiciones
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Conditions
api_type:
- schema
ms.assetid: f049a48c-9585-43f7-8549-0b8cb19a5eea
description: El elemento de condiciones identifica las condiciones que, cuando se cumplen los requisitos, se activará las acciones de regla para una regla.
ms.openlocfilehash: f66777e82892122c4c7dac45bdef3c42f5c4a577
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763766"
---
# <a name="conditions"></a><span data-ttu-id="d986d-103">Condiciones</span><span class="sxs-lookup"><span data-stu-id="d986d-103">Conditions</span></span>

<span data-ttu-id="d986d-104">El elemento de **condiciones** identifica las condiciones que, cuando se cumplen los requisitos, se activará las acciones de regla para una regla.</span><span class="sxs-lookup"><span data-stu-id="d986d-104">The **Conditions** element identifies the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span> 
  
```XML
<Conditions>
   <Categories/>
   <ContainsBodyStrings/>
   <ContainsHeaderStrings/>
   <ContainsRecipientStrings/>
   <ContainsSenderStrings/>
   <ContainsSubjectOrBodyStrings/>
   <ContainsSubjectStrings/>
   <FlaggedForAction/>
   <FromAddresses/>
   <FromConnectedAccounts/>
   <HasAttachments/>
   <Importance/>
   <IsApprovalRequest/>
   <IsAutomaticForward/>
   <IsAutomaticReply/>
   <IsEncrypted/>
   <IsMeetingRequest/>
   <IsMeetingResponse/>
   <IsNDR/>
   <IsPermissionControlled/>
   <IsReadReceipt/>
   <IsSigned/>
   <IsVoicemail/>
   <ItemClasses/>
   <MessageClassifications/>
   <NotSentToMe/>
   <SentCcMe/>
   <SentOnlyToMe/>
   <SentToAddresses/>
   <SentToMe/>
   <SentToOrCcMe/>
   <Sensitivity/>
   <WithinDateRange/>
   <WithinSizeRange/>
</Conditions>
```

 <span data-ttu-id="d986d-105">**RulePredicatesType**</span><span class="sxs-lookup"><span data-stu-id="d986d-105">**RulePredicatesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d986d-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d986d-106">Attributes and elements</span></span>

<span data-ttu-id="d986d-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d986d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d986d-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="d986d-108">Attributes</span></span>

<span data-ttu-id="d986d-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d986d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d986d-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d986d-110">Child elements</span></span>

|<span data-ttu-id="d986d-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="d986d-111">**Element**</span></span>|<span data-ttu-id="d986d-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d986d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d986d-113">Categories</span><span class="sxs-lookup"><span data-stu-id="d986d-113">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="d986d-114">Contiene las categorías que se deben aplicar a un mensaje entrante en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="d986d-114">Contains the categories that must be applied to an incoming message in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d986d-115">ContainsBodyStrings</span><span class="sxs-lookup"><span data-stu-id="d986d-115">ContainsBodyStrings</span></span>](containsbodystrings.md) <br/> |<span data-ttu-id="d986d-116">Indica las cadenas que deben aparecer en el cuerpo de los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="d986d-116">Indicates the strings that must appear in the body of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d986d-117">ContainsHeaderStrings</span><span class="sxs-lookup"><span data-stu-id="d986d-117">ContainsHeaderStrings</span></span>](containsheaderstrings.md) <br/> |<span data-ttu-id="d986d-118">Indica las cadenas que deben aparecer en los encabezados de los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="d986d-118">Indicates the strings that must appear in the headers of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d986d-119">ContainsRecipientStrings</span><span class="sxs-lookup"><span data-stu-id="d986d-119">ContainsRecipientStrings</span></span>](containsrecipientstrings.md) <br/> |<span data-ttu-id="d986d-120">Indica las cadenas que deben aparecer en la **ToRecipients** o **CcRecipients** propiedades de los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="d986d-120">Indicates the strings that must appear in either the **ToRecipients** or **CcRecipients** properties of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d986d-121">ContainsSenderStrings</span><span class="sxs-lookup"><span data-stu-id="d986d-121">ContainsSenderStrings</span></span>](containssenderstrings.md) <br/> |<span data-ttu-id="d986d-122">Indica las cadenas que deben aparecer en la propiedad **From** de los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="d986d-122">Indicates the strings that must appear in the **From** property of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d986d-123">ContainsSubjectOrBodyStrings</span><span class="sxs-lookup"><span data-stu-id="d986d-123">ContainsSubjectOrBodyStrings</span></span>](containssubjectorbodystrings.md) <br/> |<span data-ttu-id="d986d-124">Indica las cadenas que deben aparecer en el cuerpo o el asunto de los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="d986d-124">Indicates the strings that must appear in either the body or the subject of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d986d-125">ContainsSubjectStrings</span><span class="sxs-lookup"><span data-stu-id="d986d-125">ContainsSubjectStrings</span></span>](containssubjectstrings.md) <br/> |<span data-ttu-id="d986d-126">Indica las cadenas que deben aparecer en el asunto de los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="d986d-126">Indicates the strings that must appear in the subject of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d986d-127">FlaggedForAction</span><span class="sxs-lookup"><span data-stu-id="d986d-127">FlaggedForAction</span></span>](flaggedforaction.md) <br/> |<span data-ttu-id="d986d-128">Especifica la marca para el valor de la acción que debe aparecer en los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="d986d-128">Specifies the flag for action value that must appear on incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d986d-129">FromAddresses</span><span class="sxs-lookup"><span data-stu-id="d986d-129">FromAddresses</span></span>](fromaddresses.md) <br/> |<span data-ttu-id="d986d-130">Indica las direcciones de correo electrónico desde la que se deben enviar los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="d986d-130">Indicates the e-mail addresses from which incoming messages must be sent in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d986d-131">FromConnectedAccounts</span><span class="sxs-lookup"><span data-stu-id="d986d-131">FromConnectedAccounts</span></span>](fromconnectedaccounts.md) <br/> |<span data-ttu-id="d986d-132">Representa los nombres de cuenta de correo electrónico desde la que los mensajes entrantes tienen que agregadas en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="d986d-132">Represents the e-mail account names from which incoming messages have to have been aggregated in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d986d-133">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="d986d-133">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="d986d-134">Indica si los mensajes entrantes tienen que tener los datos adjuntos en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="d986d-134">Indicates whether incoming messages have to have attachments in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d986d-135">Importancia</span><span class="sxs-lookup"><span data-stu-id="d986d-135">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="d986d-136">Especifica la importancia que se mostrará en los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="d986d-136">Specifies the importance that is stamped on incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d986d-137">IsApprovalRequest</span><span class="sxs-lookup"><span data-stu-id="d986d-137">IsApprovalRequest</span></span>](isapprovalrequest.md) <br/> |<span data-ttu-id="d986d-138">Indica si los mensajes entrantes deben ser solicitudes de aprobación en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="d986d-138">Indicates whether incoming messages must be approval requests in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d986d-139">IsAutomaticForward</span><span class="sxs-lookup"><span data-stu-id="d986d-139">IsAutomaticForward</span></span>](isautomaticforward.md) <br/> |<span data-ttu-id="d986d-140">Indica si los mensajes entrantes deben ser reenvíos automáticos en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="d986d-140">Indicates whether incoming messages must be automatic forwards in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d986d-141">IsAutomaticReply</span><span class="sxs-lookup"><span data-stu-id="d986d-141">IsAutomaticReply</span></span>](isautomaticreply.md) <br/> |<span data-ttu-id="d986d-142">Indica si los mensajes entrantes deben ser las respuestas automáticas en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="d986d-142">Indicates whether incoming messages must be automatic replies in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d986d-143">IsEncrypted</span><span class="sxs-lookup"><span data-stu-id="d986d-143">IsEncrypted</span></span>](isencrypted.md) <br/> |<span data-ttu-id="d986d-144">Indica si los mensajes entrantes deben ser S/MIME cifrado en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="d986d-144">Indicates whether incoming messages must be S/MIME encrypted in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d986d-145">IsMeetingRequest</span><span class="sxs-lookup"><span data-stu-id="d986d-145">IsMeetingRequest</span></span>](ismeetingrequest.md) <br/> |<span data-ttu-id="d986d-146">Indica si los mensajes entrantes deben ser las convocatorias de reunión en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="d986d-146">Indicates whether incoming messages must be meeting requests in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d986d-147">IsMeetingResponse</span><span class="sxs-lookup"><span data-stu-id="d986d-147">IsMeetingResponse</span></span>](ismeetingresponse.md) <br/> |<span data-ttu-id="d986d-148">Indica si los mensajes entrantes deben ser respuestas de reunión en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="d986d-148">Indicates whether incoming messages must be meeting responses in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d986d-149">IsNDR</span><span class="sxs-lookup"><span data-stu-id="d986d-149">IsNDR</span></span>](isndr.md) <br/> |<span data-ttu-id="d986d-150">Indica si los mensajes entrantes deben ser informes de no entrega (NDR) en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="d986d-150">Indicates whether incoming messages must be non-delivery reports (NDRs) in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d986d-151">IsPermissionControlled</span><span class="sxs-lookup"><span data-stu-id="d986d-151">IsPermissionControlled</span></span>](ispermissioncontrolled.md) <br/> |<span data-ttu-id="d986d-152">Indica si los mensajes entrantes deben ser permiso controlado (protegido con RMS) en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="d986d-152">Indicates whether incoming messages must be permission controlled (RMS protected) in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d986d-153">IsReadReceipt</span><span class="sxs-lookup"><span data-stu-id="d986d-153">IsReadReceipt</span></span>](isreadreceipt.md) <br/> |<span data-ttu-id="d986d-154">Indica si los mensajes entrantes deben ser confirmaciones de lectura en el orden de la condición o excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="d986d-154">Indicates whether incoming messages must be read receipts in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d986d-155">IsSigned</span><span class="sxs-lookup"><span data-stu-id="d986d-155">IsSigned</span></span>](issigned.md) <br/> |<span data-ttu-id="d986d-156">Indica si los mensajes entrantes deben ser QUE S/MIME firmados para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="d986d-156">Indicates whether incoming messages must be S/MIME signed in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d986d-157">IsVoicemail</span><span class="sxs-lookup"><span data-stu-id="d986d-157">IsVoicemail</span></span>](isvoicemail.md) <br/> |<span data-ttu-id="d986d-158">Indica si los mensajes entrantes deben ser los mensajes de correo de voz en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="d986d-158">Indicates whether incoming messages must be voice mail messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d986d-159">ItemClasses</span><span class="sxs-lookup"><span data-stu-id="d986d-159">ItemClasses</span></span>](itemclasses.md) <br/> |<span data-ttu-id="d986d-160">Representa las clases de elemento deben estar marcados en los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="d986d-160">Represents the item classes that must be stamped on incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d986d-161">MessageClassifications</span><span class="sxs-lookup"><span data-stu-id="d986d-161">MessageClassifications</span></span>](messageclassifications.md) <br/> |<span data-ttu-id="d986d-162">Representa las clasificaciones de mensajes deben estar marcados en los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="d986d-162">Represents the message classifications that must be stamped on incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d986d-163">NotSentToMe</span><span class="sxs-lookup"><span data-stu-id="d986d-163">NotSentToMe</span></span>](notsenttome.md) <br/> |<span data-ttu-id="d986d-164">Indica si el propietario del buzón no debe estar en la propiedad **ToRecipients** de los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="d986d-164">Indicates whether the owner of the mailbox must not be in the **ToRecipients** property of the incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d986d-165">SentCcMe</span><span class="sxs-lookup"><span data-stu-id="d986d-165">SentCcMe</span></span>](sentccme.md) <br/> |<span data-ttu-id="d986d-166">Indica si el propietario del buzón tiene que estar en la propiedad **CcRecipients** de los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="d986d-166">Indicates whether the owner of the mailbox has to be in the **CcRecipients** property of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d986d-167">SentOnlyToMe</span><span class="sxs-lookup"><span data-stu-id="d986d-167">SentOnlyToMe</span></span>](sentonlytome.md) <br/> |<span data-ttu-id="d986d-168">Indica si el propietario del buzón tiene que ser el único existente en la propiedad **ToRecipients** de los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="d986d-168">Indicates whether the owner of the mailbox has to be the only one in the **ToRecipients** property of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d986d-169">SentToAddresses</span><span class="sxs-lookup"><span data-stu-id="d986d-169">SentToAddresses</span></span>](senttoaddresses.md) <br/> |<span data-ttu-id="d986d-170">Indica las direcciones de correo electrónico que se han enviado en orden para la condición o la excepción que se debe aplicar a los mensajes entrantes.</span><span class="sxs-lookup"><span data-stu-id="d986d-170">Indicates the e-mail addresses that incoming messages have to have been sent to in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d986d-171">SentToMe</span><span class="sxs-lookup"><span data-stu-id="d986d-171">SentToMe</span></span>](senttome.md) <br/> |<span data-ttu-id="d986d-172">Indica si el propietario del buzón tiene que estar en la propiedad **ToRecipients** de los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="d986d-172">Indicates whether the owner of the mailbox has to be in the **ToRecipients** property of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d986d-173">SentToOrCcMe</span><span class="sxs-lookup"><span data-stu-id="d986d-173">SentToOrCcMe</span></span>](senttoorccme.md) <br/> |<span data-ttu-id="d986d-174">Indica si el propietario del buzón tiene que estar en un **ToRecipients** o **CcRecipients** propiedad de los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="d986d-174">Indicates whether the owner of the mailbox has to be in either a **ToRecipients** or **CcRecipients** property of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d986d-175">Sensibilidad</span><span class="sxs-lookup"><span data-stu-id="d986d-175">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="d986d-176">Indica la confidencialidad debe estar marcados en los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="d986d-176">Indicates the sensitivity that must be stamped on incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d986d-177">WithinDateRange</span><span class="sxs-lookup"><span data-stu-id="d986d-177">WithinDateRange</span></span>](withindaterange.md) <br/> |<span data-ttu-id="d986d-178">Especifica el intervalo de fechas dentro del cual los mensajes entrantes tienen que se han recibido en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="d986d-178">Specifies the date range within which incoming messages have to have been received in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="d986d-179">WithinSizeRange</span><span class="sxs-lookup"><span data-stu-id="d986d-179">WithinSizeRange</span></span>](withinsizerange.md) <br/> |<span data-ttu-id="d986d-180">Especifica los tamaños máximos y mínimos que deben ser los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="d986d-180">Specifies the minimum and maximum sizes that incoming messages must be in order for the condition or exception to apply.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d986d-181">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d986d-181">Parent elements</span></span>

|<span data-ttu-id="d986d-182">**Element**</span><span class="sxs-lookup"><span data-stu-id="d986d-182">**Element**</span></span>|<span data-ttu-id="d986d-183">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d986d-183">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d986d-184">Regla (RuleType)</span><span class="sxs-lookup"><span data-stu-id="d986d-184">Rule (RuleType)</span></span>](rule-ruletype.md) <br/> |<span data-ttu-id="d986d-185">Contiene una sola regla y representa una regla en el buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="d986d-185">Contains a single rule and represents a rule in a user's mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d986d-186">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="d986d-186">Text value</span></span>

<span data-ttu-id="d986d-187">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d986d-187">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d986d-188">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d986d-188">Remarks</span></span>

<span data-ttu-id="d986d-189">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="d986d-189">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d986d-190">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d986d-190">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d986d-191">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d986d-191">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d986d-192">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d986d-192">Schema Name</span></span>  <br/> |<span data-ttu-id="d986d-193">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="d986d-193">Types schema</span></span>  <br/> |
|<span data-ttu-id="d986d-194">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d986d-194">Validation File</span></span>  <br/> |<span data-ttu-id="d986d-195">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d986d-195">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d986d-196">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d986d-196">Can be Empty</span></span>  <br/> |<span data-ttu-id="d986d-197">Verdadero</span><span class="sxs-lookup"><span data-stu-id="d986d-197">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d986d-198">Ver también</span><span class="sxs-lookup"><span data-stu-id="d986d-198">See also</span></span>



[<span data-ttu-id="d986d-199">Excepciones</span><span class="sxs-lookup"><span data-stu-id="d986d-199">Exceptions</span></span>](exceptions.md)


- [<span data-ttu-id="d986d-200">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="d986d-200">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

