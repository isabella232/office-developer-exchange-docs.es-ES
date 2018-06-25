---
title: Operación UpdateInboxRules
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateInboxRules
api_type:
- schema
ms.assetid: f982a237-471e-45c5-a2b5-468cfc53150b
description: La operación UpdateInboxRules actualiza las reglas de bandeja de entrada del usuario autenticado mediante la aplicación de las operaciones especificadas. UpdateInboxRules se usa para crear una regla de bandeja de entrada, para establecer una regla de bandeja de entrada, o para eliminar una regla de bandeja de entrada.
ms.openlocfilehash: 6e979421d619fed6625fe05db86c1f8c6a7418c9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840831"
---
# <a name="updateinboxrules-operation"></a><span data-ttu-id="e3ce6-104">Operación UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="e3ce6-104">UpdateInboxRules operation</span></span>

<span data-ttu-id="e3ce6-105">La operación UpdateInboxRules actualiza las reglas de bandeja de entrada del usuario autenticado mediante la aplicación de las operaciones especificadas.</span><span class="sxs-lookup"><span data-stu-id="e3ce6-105">The UpdateInboxRules operation updates the authenticated user's Inbox rules by applying the specified operations.</span></span> <span data-ttu-id="e3ce6-106">**UpdateInboxRules** se usa para crear una regla de bandeja de entrada, para establecer una regla de bandeja de entrada, o para eliminar una regla de bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="e3ce6-106">**UpdateInboxRules** is used to create an Inbox rule, to set an Inbox rule, or to delete an Inbox rule.</span></span> 
  
<span data-ttu-id="e3ce6-107">Cuando se usa la operación **UpdateInboxRules** , servicios Web de Exchange elimina las reglas de envío del cliente.</span><span class="sxs-lookup"><span data-stu-id="e3ce6-107">When you use the **UpdateInboxRules** operation, Exchange Web Services deletes client-side send rules.</span></span> <span data-ttu-id="e3ce6-108">Reglas de envío del cliente se almacenan en el cliente en la regla de mensaje de la carpeta asociada información (FAI) y en ningún otro lugar.</span><span class="sxs-lookup"><span data-stu-id="e3ce6-108">Client-side send rules are stored on the client in the rule Folder Associated Information (FAI) Message and nowhere else.</span></span> <span data-ttu-id="e3ce6-109">EWS elimina esta regla mensaje FAI de forma predeterminada, basándose en la expectativa que Outlook volverá a crearlo.</span><span class="sxs-lookup"><span data-stu-id="e3ce6-109">EWS deletes this rule FAI message by default, based on the expectation that Outlook will recreate it.</span></span> <span data-ttu-id="e3ce6-110">Sin embargo, Outlook no puede volver a crear las reglas que no existen también como una regla extendida, y no existen reglas de envío del cliente como reglas extendidas.</span><span class="sxs-lookup"><span data-stu-id="e3ce6-110">However, Outlook can't recreate rules that don't also exist as an extended rule, and client-side send rules don't exist as extended rules.</span></span> <span data-ttu-id="e3ce6-111">Como resultado, estas reglas se pierden.</span><span class="sxs-lookup"><span data-stu-id="e3ce6-111">As a result, these rules are lost.</span></span> <span data-ttu-id="e3ce6-112">Es recomendable que considere la posibilidad de esto al diseñar la solución.</span><span class="sxs-lookup"><span data-stu-id="e3ce6-112">We suggest you consider this when designing your solution.</span></span> 
  
## <a name="updateinboxrules-create-rule-request-example"></a><span data-ttu-id="e3ce6-113">Ejemplo de solicitud de UpdateInboxRules (Crear regla)</span><span class="sxs-lookup"><span data-stu-id="e3ce6-113">UpdateInboxRules (Create Rule) request example</span></span>

<span data-ttu-id="e3ce6-114">Puede usar servicios Web de Exchange para crear una regla de bandeja de entrada en el buzón de un usuario en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e3ce6-114">You can use Exchange Web Services to create an Inbox rule in a user's mailbox in the Exchange store.</span></span> <span data-ttu-id="e3ce6-115">Use el elemento [UpdateInboxRules](updateinboxrules.md) junto con el elemento [CreateRuleOperation](createruleoperation.md) para crear una regla.</span><span class="sxs-lookup"><span data-stu-id="e3ce6-115">Use the [UpdateInboxRules](updateinboxrules.md) element in conjunction with the [CreateRuleOperation](createruleoperation.md) element to create a rule.</span></span> 
  
### <a name="description"></a><span data-ttu-id="e3ce6-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="e3ce6-116">Description</span></span>

<span data-ttu-id="e3ce6-117">El cliente construye la solicitud XML y envía al servidor.</span><span class="sxs-lookup"><span data-stu-id="e3ce6-117">The client constructs the request XML and sends it to the server.</span></span>
  
### <a name="code"></a><span data-ttu-id="e3ce6-118">Código</span><span class="sxs-lookup"><span data-stu-id="e3ce6-118">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version ="Exchange2010_SP1"/>
  </soap:Header>
  <soap:Body>
      <m:UpdateInboxRules>
        <m:RemoveOutlookRuleBlob>true</m:RemoveOutlookRuleBlob>
        <m:Operations>
          <t:CreateRuleOperation>
            <t:Rule>
              <t:DisplayName>MoveInterestingToJunk</t:DisplayName>
              <t:Priority>1</t:Priority>
              <t:IsEnabled>true</t:IsEnabled>
              <t:Conditions>
                <t:ContainsSubjectStrings>
                  <t:String>Interesting</t:String>
                </t:ContainsSubjectStrings>
              </t:Conditions>
              <t:Exceptions />
              <t:Actions>
                <t:MoveToFolder>
                  <t:DistinguishedFolderId Id="junkemail" />
                </t:MoveToFolder>
              </t:Actions>
            </t:Rule>
          </t:CreateRuleOperation>
        </m:Operations>
      </m:UpdateInboxRules>
  </soap:Body>
</soap:Envelope>

```

### <a name="comments"></a><span data-ttu-id="e3ce6-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e3ce6-119">Comments</span></span>

<span data-ttu-id="e3ce6-120">En este ejemplo se crea una regla que se va a mover un mensaje de correo electrónico a la carpeta correo electrónico no deseado si el asunto de correo electrónico contiene una cadena que es igual a "Interesante".</span><span class="sxs-lookup"><span data-stu-id="e3ce6-120">This example builds a rule that will move an e-mail message to the Junk E-mail folder if the e-mail subject contains a string that equals "Interesting".</span></span>
  
### <a name="request-elements"></a><span data-ttu-id="e3ce6-121">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="e3ce6-121">Request elements</span></span>

<span data-ttu-id="e3ce6-122">La solicitud de **UpdateInboxRules** incluye los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="e3ce6-122">The **UpdateInboxRules** request includes the following elements:</span></span> 
  
- [<span data-ttu-id="e3ce6-123">MailboxSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="e3ce6-123">MailboxSmtpAddress</span></span>](mailboxsmtpaddress.md)
    
- [<span data-ttu-id="e3ce6-124">RemoveOutlookRuleBlob</span><span class="sxs-lookup"><span data-stu-id="e3ce6-124">RemoveOutlookRuleBlob</span></span>](removeoutlookruleblob.md)
    
- [<span data-ttu-id="e3ce6-125">Operations</span><span class="sxs-lookup"><span data-stu-id="e3ce6-125">Operations</span></span>](operations.md)
    
<span data-ttu-id="e3ce6-126">El elemento de [operaciones](operations.md) contiene el elemento [CreateRuleOperation](createruleoperation.md) para crear una regla.</span><span class="sxs-lookup"><span data-stu-id="e3ce6-126">The [Operations](operations.md) element contains the [CreateRuleOperation](createruleoperation.md) element to create a rule.</span></span> 
  
## <a name="updateinboxrules-create-rule-response-example"></a><span data-ttu-id="e3ce6-127">Ejemplo de respuesta UpdateInboxRules (Crear regla)</span><span class="sxs-lookup"><span data-stu-id="e3ce6-127">UpdateInboxRules (Create Rule) response example</span></span>

### <a name="description"></a><span data-ttu-id="e3ce6-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="e3ce6-128">Description</span></span>

<span data-ttu-id="e3ce6-129">El siguiente ejemplo de cuerpo de SOAP Simple Object Access Protocol () muestra una respuesta correcta a la solicitud de **UpdateInboxRules** que crea una regla.</span><span class="sxs-lookup"><span data-stu-id="e3ce6-129">The following Simple Object Access Protocol (SOAP) body example shows a successful response to the **UpdateInboxRules** request that creates a rule.</span></span> 
  
### <a name="code"></a><span data-ttu-id="e3ce6-130">Código</span><span class="sxs-lookup"><span data-stu-id="e3ce6-130">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
        MinorVersion="1" 
        MajorBuildNumber="139" 
        MinorBuildNumber="0" Version="Exchange2010_SP1" 
        xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <UpdateInboxRulesResponse 
         ResponseClass="Success" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
    </UpdateInboxRulesResponse>
  </s:Body>
</s:Envelope>

```

### <a name="successful-response-elements"></a><span data-ttu-id="e3ce6-131">Elementos de respuesta correcta</span><span class="sxs-lookup"><span data-stu-id="e3ce6-131">Successful response elements</span></span>

<span data-ttu-id="e3ce6-132">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="e3ce6-132">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="e3ce6-133">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="e3ce6-133">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="e3ce6-134">UpdateInboxRulesResponse</span><span class="sxs-lookup"><span data-stu-id="e3ce6-134">UpdateInboxRulesResponse</span></span>](updateinboxrulesresponse.md)
    
- [<span data-ttu-id="e3ce6-135">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="e3ce6-135">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="e3ce6-136">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="e3ce6-136">ResponseCode</span></span>](responsecode.md)
    
## <a name="updateinboxrules-set-rule-request-example"></a><span data-ttu-id="e3ce6-137">Ejemplo de solicitud de UpdateInboxRules (regla de conjunto)</span><span class="sxs-lookup"><span data-stu-id="e3ce6-137">UpdateInboxRules (Set Rule) request example</span></span>

<span data-ttu-id="e3ce6-138">Puede usar los servicios Web de Exchange para modificar una regla de bandeja de entrada en el buzón del usuario en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e3ce6-138">You can use Exchange Web Services to modify an Inbox rule in a user's mailbox in the Exchange store.</span></span> <span data-ttu-id="e3ce6-139">Use el elemento [UpdateInboxRules](updateinboxrules.md) junto con el elemento [SetRuleOperation](setruleoperation.md) para modificar una regla.</span><span class="sxs-lookup"><span data-stu-id="e3ce6-139">Use the [UpdateInboxRules](updateinboxrules.md) element in conjunction with the [SetRuleOperation](setruleoperation.md) element to modify a rule.</span></span> 
  
### <a name="description"></a><span data-ttu-id="e3ce6-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="e3ce6-140">Description</span></span>

<span data-ttu-id="e3ce6-141">El cliente construye la solicitud XML y envía al servidor.</span><span class="sxs-lookup"><span data-stu-id="e3ce6-141">The client constructs the request XML and sends it to the server.</span></span>
  
### <a name="code"></a><span data-ttu-id="e3ce6-142">Código</span><span class="sxs-lookup"><span data-stu-id="e3ce6-142">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version ="Exchange2010_SP1"/>
  </soap:Header>
  <soap:Body>
      <m:UpdateInboxRules>
        <m:RemoveOutlookRuleBlob>true</m:RemoveOutlookRuleBlob>
        <Operations xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
          <SetRuleOperation xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
            <Rule>
              <RuleId>Nh8AAAAwW/w=</RuleId>
              <DisplayName>(Modified) This is Junk</DisplayName>
              <Priority>1</Priority>
              <IsEnabled>true</IsEnabled>
              <Conditions>
                <ContainsSubjectStrings>
                  <String>Interesting</String>
                </ContainsSubjectStrings>
              </Conditions>
              <Actions>
                <MoveToFolder>
                  <FolderId Id="AAMkADQ1YTE1" ChangeKey="AQAAAA==" />
                </MoveToFolder>
              </Actions>
            </Rule>
          </SetRuleOperation>
        </Operations>
      </m:UpdateInboxRules>
  </soap:Body>
</soap:Envelope>

```

### <a name="comments"></a><span data-ttu-id="e3ce6-143">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e3ce6-143">Comments</span></span>

<span data-ttu-id="e3ce6-144">En este ejemplo se cambia el nombre para mostrar "(modificado) es no deseado".</span><span class="sxs-lookup"><span data-stu-id="e3ce6-144">This example changes the display name to "(Modified) This is Junk".</span></span>
  
> [!NOTE]
> <span data-ttu-id="e3ce6-145">Los valores del **identificador** y **ChangeKey** atributos del elemento [FolderId](folderid.md) se han abreviado para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="e3ce6-145">The values of the **Id** and **ChangeKey** attributes of the [FolderId](folderid.md) element have been shortened for readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="e3ce6-146">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="e3ce6-146">Request elements</span></span>

<span data-ttu-id="e3ce6-147">La solicitud de **UpdateInboxRules** incluye los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="e3ce6-147">The **UpdateInboxRules** request includes the following elements:</span></span> 
  
- [<span data-ttu-id="e3ce6-148">MailboxSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="e3ce6-148">MailboxSmtpAddress</span></span>](mailboxsmtpaddress.md)
    
- [<span data-ttu-id="e3ce6-149">RemoveOutlookRuleBlob</span><span class="sxs-lookup"><span data-stu-id="e3ce6-149">RemoveOutlookRuleBlob</span></span>](removeoutlookruleblob.md)
    
- [<span data-ttu-id="e3ce6-150">Operations</span><span class="sxs-lookup"><span data-stu-id="e3ce6-150">Operations</span></span>](operations.md)
    
<span data-ttu-id="e3ce6-151">El elemento de [operaciones](operations.md) contiene el elemento [SetRuleOperation](setruleoperation.md) para modificar una regla.</span><span class="sxs-lookup"><span data-stu-id="e3ce6-151">The [Operations](operations.md) element contains the [SetRuleOperation](setruleoperation.md) element to modify a rule.</span></span> 
  
## <a name="updateinboxrules-set-rule-response-example"></a><span data-ttu-id="e3ce6-152">Ejemplo de respuesta UpdateInboxRules (regla de conjunto)</span><span class="sxs-lookup"><span data-stu-id="e3ce6-152">UpdateInboxRules (Set Rule) response example</span></span>

### <a name="description"></a><span data-ttu-id="e3ce6-153">Descripción</span><span class="sxs-lookup"><span data-stu-id="e3ce6-153">Description</span></span>

<span data-ttu-id="e3ce6-154">El siguiente ejemplo de cuerpo de SOAP Simple Object Access Protocol () muestra una respuesta correcta a la solicitud de **UpdateInboxRules** que modifica una regla.</span><span class="sxs-lookup"><span data-stu-id="e3ce6-154">The following Simple Object Access Protocol (SOAP) body example shows a successful response to the **UpdateInboxRules** request that modifies a rule.</span></span> 
  
### <a name="code"></a><span data-ttu-id="e3ce6-155">Código</span><span class="sxs-lookup"><span data-stu-id="e3ce6-155">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
        MinorVersion="1" 
        MajorBuildNumber="139" 
        MinorBuildNumber="0" 
        Version="Exchange2010_SP1" 
        xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <UpdateInboxRulesResponse 
          ResponseClass="Success" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
    </UpdateInboxRulesResponse>
  </s:Body>
</s:Envelope>

```

### <a name="successful-response-elements"></a><span data-ttu-id="e3ce6-156">Elementos de respuesta correcta</span><span class="sxs-lookup"><span data-stu-id="e3ce6-156">Successful response elements</span></span>

<span data-ttu-id="e3ce6-157">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="e3ce6-157">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="e3ce6-158">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="e3ce6-158">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="e3ce6-159">UpdateInboxRulesResponse</span><span class="sxs-lookup"><span data-stu-id="e3ce6-159">UpdateInboxRulesResponse</span></span>](updateinboxrulesresponse.md)
    
- [<span data-ttu-id="e3ce6-160">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="e3ce6-160">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="e3ce6-161">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="e3ce6-161">ResponseCode</span></span>](responsecode.md)
    
## <a name="updateinboxrules-delete-rule-request-example"></a><span data-ttu-id="e3ce6-162">Ejemplo de solicitud de UpdateInboxRules (Eliminar regla)</span><span class="sxs-lookup"><span data-stu-id="e3ce6-162">UpdateInboxRules (Delete Rule) request example</span></span>

<span data-ttu-id="e3ce6-163">Puede usar los servicios Web de Exchange para eliminar una regla de bandeja de entrada en el buzón del usuario en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e3ce6-163">You can use Exchange Web Services to delete an Inbox rule in a user's mailbox in the Exchange store.</span></span> <span data-ttu-id="e3ce6-164">Para eliminar una regla, use la [UpdateInboxRules](updateinboxrules.md) junto con el elemento [DeleteRuleOperation](deleteruleoperation.md) .</span><span class="sxs-lookup"><span data-stu-id="e3ce6-164">Use the [UpdateInboxRules](updateinboxrules.md) in conjunction with the [DeleteRuleOperation](deleteruleoperation.md) element to delete a rule.</span></span> 
  
### <a name="description"></a><span data-ttu-id="e3ce6-165">Descripción</span><span class="sxs-lookup"><span data-stu-id="e3ce6-165">Description</span></span>

<span data-ttu-id="e3ce6-166">El cliente construye la solicitud XML y envía al servidor.</span><span class="sxs-lookup"><span data-stu-id="e3ce6-166">The client constructs the request XML and sends it to the server.</span></span>
  
### <a name="code"></a><span data-ttu-id="e3ce6-167">Código</span><span class="sxs-lookup"><span data-stu-id="e3ce6-167">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version ="Exchange2010_SP1"/>
  </soap:Header>
  <soap:Body>
      <m:UpdateInboxRules>
        <m:RemoveOutlookRuleBlob>true</m:RemoveOutlookRuleBlob>
        <m:Operations>
          <t:DeleteRuleOperation>
            <t:RuleId>Nh8AAAAwW/U=</t:RuleId>
          </t:DeleteRuleOperation>
        </m:Operations>
      </m:UpdateInboxRules>
  </soap:Body>
</soap:Envelope>

```

### <a name="comments"></a><span data-ttu-id="e3ce6-168">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e3ce6-168">Comments</span></span>

<span data-ttu-id="e3ce6-169">En este ejemplo se elimina la regla identificada existente.</span><span class="sxs-lookup"><span data-stu-id="e3ce6-169">This example deletes the existing identified rule.</span></span>
  
### <a name="request-elements"></a><span data-ttu-id="e3ce6-170">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="e3ce6-170">Request elements</span></span>

<span data-ttu-id="e3ce6-171">La solicitud de **UpdateInboxRules** incluye los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="e3ce6-171">The **UpdateInboxRules** request includes the following elements:</span></span> 
  
- [<span data-ttu-id="e3ce6-172">MailboxSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="e3ce6-172">MailboxSmtpAddress</span></span>](mailboxsmtpaddress.md)
    
- [<span data-ttu-id="e3ce6-173">RemoveOutlookRuleBlob</span><span class="sxs-lookup"><span data-stu-id="e3ce6-173">RemoveOutlookRuleBlob</span></span>](removeoutlookruleblob.md)
    
- [<span data-ttu-id="e3ce6-174">Operations</span><span class="sxs-lookup"><span data-stu-id="e3ce6-174">Operations</span></span>](operations.md)
    
<span data-ttu-id="e3ce6-175">El elemento de [operaciones](operations.md) contiene el elemento [DeleteRuleOperation](deleteruleoperation.md) para eliminar una regla.</span><span class="sxs-lookup"><span data-stu-id="e3ce6-175">The [Operations](operations.md) element contains the [DeleteRuleOperation](deleteruleoperation.md) element to delete a rule.</span></span> 
  
## <a name="updateinboxrules-delete-rule-response-example"></a><span data-ttu-id="e3ce6-176">Ejemplo de respuesta UpdateInboxRules (Eliminar regla)</span><span class="sxs-lookup"><span data-stu-id="e3ce6-176">UpdateInboxRules (Delete Rule) response example</span></span>

### <a name="description"></a><span data-ttu-id="e3ce6-177">Descripción</span><span class="sxs-lookup"><span data-stu-id="e3ce6-177">Description</span></span>

<span data-ttu-id="e3ce6-178">El siguiente ejemplo de cuerpo de SOAP Simple Object Access Protocol () muestra una respuesta correcta a la solicitud de **UpdateInboxRules** que se elimina una regla.</span><span class="sxs-lookup"><span data-stu-id="e3ce6-178">The following Simple Object Access Protocol (SOAP) body example shows a successful response to the **UpdateInboxRules** request that deletes a rule.</span></span> 
  
### <a name="code"></a><span data-ttu-id="e3ce6-179">Código</span><span class="sxs-lookup"><span data-stu-id="e3ce6-179">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
        MinorVersion="1" 
        MajorBuildNumber="139" 
        MinorBuildNumber="0" 
        Version="Exchange2010_SP1" 
        xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <UpdateInboxRulesResponse ResponseClass="Success" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
    </UpdateInboxRulesResponse>
  </s:Body>
</s:Envelope>

```

### <a name="successful-response-elements"></a><span data-ttu-id="e3ce6-180">Elementos de respuesta correcta</span><span class="sxs-lookup"><span data-stu-id="e3ce6-180">Successful response elements</span></span>

<span data-ttu-id="e3ce6-181">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="e3ce6-181">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="e3ce6-182">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="e3ce6-182">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="e3ce6-183">UpdateInboxRulesResponse</span><span class="sxs-lookup"><span data-stu-id="e3ce6-183">UpdateInboxRulesResponse</span></span>](updateinboxrulesresponse.md)
    
- [<span data-ttu-id="e3ce6-184">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="e3ce6-184">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="e3ce6-185">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="e3ce6-185">ResponseCode</span></span>](responsecode.md)
    
## <a name="see-also"></a><span data-ttu-id="e3ce6-186">Vea también</span><span class="sxs-lookup"><span data-stu-id="e3ce6-186">See also</span></span>



[<span data-ttu-id="e3ce6-187">Operación de GetInboxRules</span><span class="sxs-lookup"><span data-stu-id="e3ce6-187">GetInboxRules operation</span></span>](getinboxrules-operation.md)

