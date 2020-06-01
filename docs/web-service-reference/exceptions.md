---
title: Excepciones
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Exceptions
api_type:
- schema
ms.assetid: 7cd63ac2-3441-4ed4-915b-6f90af4b28fc
description: El elemento Exceptions identifica las excepciones que representan todas las condiciones de excepción de regla disponibles para una regla de bandeja de entrada.
ms.openlocfilehash: 1afc2980391ee588f9b9b813b87c2c699de3a6df
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463359"
---
# <a name="exceptions"></a><span data-ttu-id="44385-103">Excepciones</span><span class="sxs-lookup"><span data-stu-id="44385-103">Exceptions</span></span>

<span data-ttu-id="44385-104">El elemento **Exceptions** identifica las excepciones que representan todas las condiciones de excepción de regla disponibles para una regla de bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="44385-104">The **Exceptions** element identifies the exceptions that represent all the available rule exception conditions for an Inbox rule.</span></span> 
  
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

 <span data-ttu-id="44385-105">**RulePredicatesType**</span><span class="sxs-lookup"><span data-stu-id="44385-105">**RulePredicatesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="44385-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="44385-106">Attributes and elements</span></span>

<span data-ttu-id="44385-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="44385-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="44385-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="44385-108">Attributes</span></span>

<span data-ttu-id="44385-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="44385-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="44385-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="44385-110">Child elements</span></span>

|<span data-ttu-id="44385-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="44385-111">**Element**</span></span>|<span data-ttu-id="44385-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="44385-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="44385-113">Categories</span><span class="sxs-lookup"><span data-stu-id="44385-113">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="44385-114">Contiene las categorías que deben aplicarse a un mensaje entrante para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="44385-114">Contains the categories that must be applied to an incoming message in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="44385-115">ContainsBodyStrings</span><span class="sxs-lookup"><span data-stu-id="44385-115">ContainsBodyStrings</span></span>](containsbodystrings.md) <br/> |<span data-ttu-id="44385-116">Indica las cadenas que deben aparecer en el cuerpo de los mensajes entrantes para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="44385-116">Indicates the strings that must appear in the body of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="44385-117">ContainsHeaderStrings</span><span class="sxs-lookup"><span data-stu-id="44385-117">ContainsHeaderStrings</span></span>](containsheaderstrings.md) <br/> |<span data-ttu-id="44385-118">Indicaqtes las cadenas que deben aparecer en los encabezados de los mensajes entrantes para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="44385-118">Indicaqtes the strings that must appear in the headers of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="44385-119">ContainsRecipientStrings</span><span class="sxs-lookup"><span data-stu-id="44385-119">ContainsRecipientStrings</span></span>](containsrecipientstrings.md) <br/> |<span data-ttu-id="44385-120">Indica las cadenas que deben aparecer en las propiedades **ToRecipients** o **CcRecipients** de los mensajes entrantes para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="44385-120">Indicates the strings that must appear in either the **ToRecipients** or **CcRecipients** properties of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="44385-121">ContainsSenderStrings</span><span class="sxs-lookup"><span data-stu-id="44385-121">ContainsSenderStrings</span></span>](containssenderstrings.md) <br/> |<span data-ttu-id="44385-122">Indica las cadenas que deben aparecer en la propiedad **from** de los mensajes entrantes para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="44385-122">Indicates the strings that must appear in the **From** property of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="44385-123">ContainsSubjectOrBodyStrings</span><span class="sxs-lookup"><span data-stu-id="44385-123">ContainsSubjectOrBodyStrings</span></span>](containssubjectorbodystrings.md) <br/> |<span data-ttu-id="44385-124">Indica las cadenas que deben aparecer en el cuerpo o el asunto de los mensajes entrantes para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="44385-124">Indicates the strings that must appear in either the body or the subject of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="44385-125">ContainsSubjectStrings</span><span class="sxs-lookup"><span data-stu-id="44385-125">ContainsSubjectStrings</span></span>](containssubjectstrings.md) <br/> |<span data-ttu-id="44385-126">Indica las cadenas que deben aparecer en el asunto de los mensajes entrantes para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="44385-126">Indicates the strings that must appear in the subject of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="44385-127">FlaggedForAction</span><span class="sxs-lookup"><span data-stu-id="44385-127">FlaggedForAction</span></span>](flaggedforaction.md) <br/> |<span data-ttu-id="44385-128">Especifica la marca para el valor de la acción que debe aparecer en los mensajes entrantes para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="44385-128">Specifies the flag for action value that must appear on incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="44385-129">FromAddresses</span><span class="sxs-lookup"><span data-stu-id="44385-129">FromAddresses</span></span>](fromaddresses.md) <br/> |<span data-ttu-id="44385-130">Indica las direcciones de correo electrónico desde las que se deben enviar los mensajes entrantes para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="44385-130">Indicates the e-mail addresses from which incoming messages must be sent in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="44385-131">FromConnectedAccounts</span><span class="sxs-lookup"><span data-stu-id="44385-131">FromConnectedAccounts</span></span>](fromconnectedaccounts.md) <br/> |<span data-ttu-id="44385-132">Representa los nombres de cuenta de correo electrónico desde los que se deben agregar los mensajes entrantes para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="44385-132">Represents the e-mail account names from which incoming messages have to have been aggregated in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="44385-133">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="44385-133">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="44385-134">Indica si los mensajes entrantes deben tener datos adjuntos para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="44385-134">Indicates whether incoming messages have to have attachments in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="44385-135">Importance</span><span class="sxs-lookup"><span data-stu-id="44385-135">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="44385-136">Especifica la importancia que se marca en los mensajes entrantes para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="44385-136">Specifies the importance that is stamped on incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="44385-137">IsApprovalRequest</span><span class="sxs-lookup"><span data-stu-id="44385-137">IsApprovalRequest</span></span>](isapprovalrequest.md) <br/> |<span data-ttu-id="44385-138">Indica si los mensajes entrantes deben ser solicitudes de aprobación para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="44385-138">Indicates whether incoming messages must be approval requests in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="44385-139">IsAutomaticForward</span><span class="sxs-lookup"><span data-stu-id="44385-139">IsAutomaticForward</span></span>](isautomaticforward.md) <br/> |<span data-ttu-id="44385-140">Indica si los mensajes entrantes deben ser reenviados automáticamente para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="44385-140">Indicates whether incoming messages must be automatic forwards in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="44385-141">IsAutomaticReply</span><span class="sxs-lookup"><span data-stu-id="44385-141">IsAutomaticReply</span></span>](isautomaticreply.md) <br/> |<span data-ttu-id="44385-142">Indica si los mensajes entrantes deben ser respuestas automáticas para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="44385-142">Indicates whether incoming messages must be automatic replies in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="44385-143">IsEncrypted</span><span class="sxs-lookup"><span data-stu-id="44385-143">IsEncrypted</span></span>](isencrypted.md) <br/> |<span data-ttu-id="44385-144">Indica si los mensajes entrantes deben ser cifrados con S/MIME para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="44385-144">Indicates whether incoming messages must be S/MIME encrypted in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="44385-145">IsMeetingRequest</span><span class="sxs-lookup"><span data-stu-id="44385-145">IsMeetingRequest</span></span>](ismeetingrequest.md) <br/> |<span data-ttu-id="44385-146">Indica si los mensajes entrantes deben ser convocatorias de reunión para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="44385-146">Indicates whether incoming messages must be meeting requests in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="44385-147">IsMeetingResponse</span><span class="sxs-lookup"><span data-stu-id="44385-147">IsMeetingResponse</span></span>](ismeetingresponse.md) <br/> |<span data-ttu-id="44385-148">Indica si los mensajes entrantes deben ser respuestas a la reunión para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="44385-148">Indicates whether incoming messages must be meeting responses in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="44385-149">IsNDR</span><span class="sxs-lookup"><span data-stu-id="44385-149">IsNDR</span></span>](isndr.md) <br/> |<span data-ttu-id="44385-150">Indica si los mensajes entrantes deben ser informes de no entrega (NDR) para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="44385-150">Indicates whether incoming messages must be non-delivery reports (NDRs) in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="44385-151">IsPermissionControlled</span><span class="sxs-lookup"><span data-stu-id="44385-151">IsPermissionControlled</span></span>](ispermissioncontrolled.md) <br/> |<span data-ttu-id="44385-152">Indica si los mensajes entrantes deben ser controlados por permisos (protegido por RMS) para que se aplique la condición o excepción</span><span class="sxs-lookup"><span data-stu-id="44385-152">Indicates whether incoming messages must be permission controlled (RMS protected) in order for the condition or exception to apply</span></span>  <br/> |
|[<span data-ttu-id="44385-153">IsReadReceipt</span><span class="sxs-lookup"><span data-stu-id="44385-153">IsReadReceipt</span></span>](isreadreceipt.md) <br/> |<span data-ttu-id="44385-154">Indica si los mensajes entrantes deben ser confirmaciones de lectura para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="44385-154">Indicates whether incoming messages must be read receipts in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="44385-155">IsSigned</span><span class="sxs-lookup"><span data-stu-id="44385-155">IsSigned</span></span>](issigned.md) <br/> |<span data-ttu-id="44385-156">Indica si los mensajes entrantes deben ser firmados con S/MIME para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="44385-156">Indicates whether incoming messages must be S/MIME signed in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="44385-157">IsVoicemail</span><span class="sxs-lookup"><span data-stu-id="44385-157">IsVoicemail</span></span>](isvoicemail.md) <br/> |<span data-ttu-id="44385-158">Indica si los mensajes entrantes deben ser mensajes de correo de voz en orden para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="44385-158">Indicates whether incoming messages must be voice mail messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="44385-159">ItemClasses</span><span class="sxs-lookup"><span data-stu-id="44385-159">ItemClasses</span></span>](itemclasses.md) <br/> |<span data-ttu-id="44385-160">Representa las clases de elementos que se deben estampar en los mensajes entrantes para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="44385-160">Represents the item classes that must be stamped on incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="44385-161">MessageClassifications</span><span class="sxs-lookup"><span data-stu-id="44385-161">MessageClassifications</span></span>](messageclassifications.md) <br/> |<span data-ttu-id="44385-162">Representa las clasificaciones de mensajes que se deben marcar en los mensajes entrantes para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="44385-162">Represents the message classifications that must be stamped on incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="44385-163">NotSentToMe</span><span class="sxs-lookup"><span data-stu-id="44385-163">NotSentToMe</span></span>](notsenttome.md) <br/> |<span data-ttu-id="44385-164">Indica si el propietario del buzón no debe estar en la propiedad **ToRecipients** de los mensajes entrantes para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="44385-164">Indicates whether the owner of the mailbox must not be in the **ToRecipients** property of the incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="44385-165">SentCcMe</span><span class="sxs-lookup"><span data-stu-id="44385-165">SentCcMe</span></span>](sentccme.md) <br/> |<span data-ttu-id="44385-166">Indica si el propietario del buzón tiene que estar en la propiedad **CcRecipients** de los mensajes entrantes para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="44385-166">Indicates whether the owner of the mailbox has to be in the **CcRecipients** property of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="44385-167">SentOnlyToMe</span><span class="sxs-lookup"><span data-stu-id="44385-167">SentOnlyToMe</span></span>](sentonlytome.md) <br/> |<span data-ttu-id="44385-168">Indica si el propietario del buzón tiene que ser el único de la propiedad **ToRecipients** de los mensajes entrantes para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="44385-168">Indicates whether the owner of the mailbox has to be the only one in the **ToRecipients** property of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="44385-169">SentToAddresses</span><span class="sxs-lookup"><span data-stu-id="44385-169">SentToAddresses</span></span>](senttoaddresses.md) <br/> |<span data-ttu-id="44385-170">Indica las direcciones de correo electrónico a las que se deben enviar los mensajes entrantes para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="44385-170">Indicates the e-mail addresses that incoming messages have to have been sent to in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="44385-171">SentToMe</span><span class="sxs-lookup"><span data-stu-id="44385-171">SentToMe</span></span>](senttome.md) <br/> |<span data-ttu-id="44385-172">Indica si el propietario del buzón tiene que estar en la propiedad **ToRecipients** de los mensajes entrantes para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="44385-172">Indicates whether the owner of the mailbox has to be in the **ToRecipients** property of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="44385-173">SentToOrCcMe</span><span class="sxs-lookup"><span data-stu-id="44385-173">SentToOrCcMe</span></span>](senttoorccme.md) <br/> |<span data-ttu-id="44385-174">Indica si el propietario del buzón tiene que estar en la propiedad **ToRecipients** o **CcRecipients** de los mensajes entrantes para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="44385-174">Indicates whether the owner of the mailbox has to be in either a **ToRecipients** or **CcRecipients** property of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="44385-175">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="44385-175">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="44385-176">Indica la sensibilidad que se debe estampar en los mensajes entrantes para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="44385-176">Indicates the sensitivity that must be stamped on incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="44385-177">WithinDateRange</span><span class="sxs-lookup"><span data-stu-id="44385-177">WithinDateRange</span></span>](withindaterange.md) <br/> |<span data-ttu-id="44385-178">Especifica el intervalo de fechas en el que se deben recibir los mensajes entrantes para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="44385-178">Specifies the date range within which incoming messages have to have been received in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="44385-179">WithinSizeRange</span><span class="sxs-lookup"><span data-stu-id="44385-179">WithinSizeRange</span></span>](withinsizerange.md) <br/> |<span data-ttu-id="44385-180">Especifica los tamaños máximos y mínimos que los mensajes entrantes deben tener en orden para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="44385-180">Specifies the minimum and maximum sizes that incoming messages must be in order for the condition or exception to apply.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="44385-181">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="44385-181">Parent elements</span></span>

|<span data-ttu-id="44385-182">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="44385-182">**Element**</span></span>|<span data-ttu-id="44385-183">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="44385-183">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="44385-184">Regla (RuleType)</span><span class="sxs-lookup"><span data-stu-id="44385-184">Rule (RuleType)</span></span>](rule-ruletype.md) <br/> |<span data-ttu-id="44385-185">Contiene una sola regla y representa una regla en el buzón de un usuario.</span><span class="sxs-lookup"><span data-stu-id="44385-185">Contains a single rule and represents a rule in a user's mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="44385-186">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="44385-186">Text value</span></span>

<span data-ttu-id="44385-187">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="44385-187">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="44385-188">Comentarios</span><span class="sxs-lookup"><span data-stu-id="44385-188">Remarks</span></span>

<span data-ttu-id="44385-189">Los predicados de regla se usan como excepciones o condiciones de regla.</span><span class="sxs-lookup"><span data-stu-id="44385-189">The rule predicates are used as rule conditions or exceptions.</span></span>
  
<span data-ttu-id="44385-190">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="44385-190">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="44385-191">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="44385-191">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="44385-192">Namespace</span><span class="sxs-lookup"><span data-stu-id="44385-192">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="44385-193">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="44385-193">Schema Name</span></span>  <br/> |<span data-ttu-id="44385-194">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="44385-194">Types schema</span></span>  <br/> |
|<span data-ttu-id="44385-195">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="44385-195">Validation File</span></span>  <br/> |<span data-ttu-id="44385-196">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="44385-196">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="44385-197">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="44385-197">Can be Empty</span></span>  <br/> |<span data-ttu-id="44385-198">Verdadero</span><span class="sxs-lookup"><span data-stu-id="44385-198">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="44385-199">Vea también</span><span class="sxs-lookup"><span data-stu-id="44385-199">See also</span></span>



[<span data-ttu-id="44385-200">Condiciones</span><span class="sxs-lookup"><span data-stu-id="44385-200">Conditions</span></span>](conditions.md)


- [<span data-ttu-id="44385-201">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="44385-201">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

