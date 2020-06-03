---
title: Operación de UpdateInboxRules
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
description: La operación UpdateInboxRules actualiza las reglas de la bandeja de entrada del usuario autenticado mediante la aplicación de las operaciones especificadas. UpdateInboxRules se usa para crear una regla de bandeja de entrada, para establecer una regla de bandeja de entrada o para eliminar una regla de bandeja de entrada.
ms.openlocfilehash: a6ced4be25c6fe4649ad649ba01194791548bf67
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44531003"
---
# <a name="updateinboxrules-operation"></a><span data-ttu-id="ccf9d-104">Operación de UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="ccf9d-104">UpdateInboxRules operation</span></span>

<span data-ttu-id="ccf9d-105">La operación UpdateInboxRules actualiza las reglas de la bandeja de entrada del usuario autenticado mediante la aplicación de las operaciones especificadas.</span><span class="sxs-lookup"><span data-stu-id="ccf9d-105">The UpdateInboxRules operation updates the authenticated user's Inbox rules by applying the specified operations.</span></span> <span data-ttu-id="ccf9d-106">**UpdateInboxRules** se usa para crear una regla de bandeja de entrada, para establecer una regla de bandeja de entrada o para eliminar una regla de bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="ccf9d-106">**UpdateInboxRules** is used to create an Inbox rule, to set an Inbox rule, or to delete an Inbox rule.</span></span> 
  
<span data-ttu-id="ccf9d-107">Cuando se usa la operación **UpdateInboxRules** , servicios web Exchange elimina las reglas de envío del lado cliente.</span><span class="sxs-lookup"><span data-stu-id="ccf9d-107">When you use the **UpdateInboxRules** operation, Exchange Web Services deletes client-side send rules.</span></span> <span data-ttu-id="ccf9d-108">Las reglas de envío del lado cliente se almacenan en el cliente en el Mensaje de información asociada de carpetas (FAI) de la regla y en ningún otro lugar.</span><span class="sxs-lookup"><span data-stu-id="ccf9d-108">Client-side send rules are stored on the client in the rule Folder Associated Information (FAI) Message and nowhere else.</span></span> <span data-ttu-id="ccf9d-109">EWS elimina este mensaje FAI de la regla de manera predeterminada, basándose en la expectativa de que Outlook volverá a crearlo.</span><span class="sxs-lookup"><span data-stu-id="ccf9d-109">EWS deletes this rule FAI message by default, based on the expectation that Outlook will recreate it.</span></span> <span data-ttu-id="ccf9d-110">En cambio, Outlook no puede volver a crear reglas que tampoco existen como una regla extendida, y las reglas de envío del lado cliente no existen como reglas extendidas.</span><span class="sxs-lookup"><span data-stu-id="ccf9d-110">However, Outlook can't recreate rules that don't also exist as an extended rule, and client-side send rules don't exist as extended rules.</span></span> <span data-ttu-id="ccf9d-111">Como resultado, estas reglas se pierden.</span><span class="sxs-lookup"><span data-stu-id="ccf9d-111">As a result, these rules are lost.</span></span> <span data-ttu-id="ccf9d-112">Le sugerimos que considere esta posibilidad al diseñar su solución.</span><span class="sxs-lookup"><span data-stu-id="ccf9d-112">We suggest you consider this when designing your solution.</span></span> 
  
## <a name="updateinboxrules-create-rule-request-example"></a><span data-ttu-id="ccf9d-113">Ejemplo de solicitud UpdateInboxRules (Create Rule)</span><span class="sxs-lookup"><span data-stu-id="ccf9d-113">UpdateInboxRules (Create Rule) request example</span></span>

<span data-ttu-id="ccf9d-114">Puede usar los servicios web Exchange para crear una regla de bandeja de entrada en el buzón de un usuario en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ccf9d-114">You can use Exchange Web Services to create an Inbox rule in a user's mailbox in the Exchange store.</span></span> <span data-ttu-id="ccf9d-115">Use el elemento [UpdateInboxRules](updateinboxrules.md) junto con el elemento [CreateRuleOperation](createruleoperation.md) para crear una regla.</span><span class="sxs-lookup"><span data-stu-id="ccf9d-115">Use the [UpdateInboxRules](updateinboxrules.md) element in conjunction with the [CreateRuleOperation](createruleoperation.md) element to create a rule.</span></span> 
  
### <a name="description"></a><span data-ttu-id="ccf9d-116">Description</span><span class="sxs-lookup"><span data-stu-id="ccf9d-116">Description</span></span>

<span data-ttu-id="ccf9d-117">El cliente crea el XML de la solicitud y lo envía al servidor.</span><span class="sxs-lookup"><span data-stu-id="ccf9d-117">The client constructs the request XML and sends it to the server.</span></span>
  
### <a name="code"></a><span data-ttu-id="ccf9d-118">Código</span><span class="sxs-lookup"><span data-stu-id="ccf9d-118">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a><span data-ttu-id="ccf9d-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ccf9d-119">Comments</span></span>

<span data-ttu-id="ccf9d-120">En este ejemplo se crea una regla que moverá un mensaje de correo electrónico a la carpeta correo electrónico no deseado si el asunto del correo electrónico contiene una cadena que es igual a "interesante".</span><span class="sxs-lookup"><span data-stu-id="ccf9d-120">This example builds a rule that will move an e-mail message to the Junk E-mail folder if the e-mail subject contains a string that equals "Interesting".</span></span>
  
### <a name="request-elements"></a><span data-ttu-id="ccf9d-121">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="ccf9d-121">Request elements</span></span>

<span data-ttu-id="ccf9d-122">La solicitud **UpdateInboxRules** incluye los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="ccf9d-122">The **UpdateInboxRules** request includes the following elements:</span></span> 
  
- [<span data-ttu-id="ccf9d-123">MailboxSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="ccf9d-123">MailboxSmtpAddress</span></span>](mailboxsmtpaddress.md)
    
- [<span data-ttu-id="ccf9d-124">RemoveOutlookRuleBlob</span><span class="sxs-lookup"><span data-stu-id="ccf9d-124">RemoveOutlookRuleBlob</span></span>](removeoutlookruleblob.md)
    
- [<span data-ttu-id="ccf9d-125">Operations</span><span class="sxs-lookup"><span data-stu-id="ccf9d-125">Operations</span></span>](operations.md)
    
<span data-ttu-id="ccf9d-126">El elemento [Operations](operations.md) contiene el elemento [CreateRuleOperation](createruleoperation.md) para crear una regla.</span><span class="sxs-lookup"><span data-stu-id="ccf9d-126">The [Operations](operations.md) element contains the [CreateRuleOperation](createruleoperation.md) element to create a rule.</span></span> 
  
## <a name="updateinboxrules-create-rule-response-example"></a><span data-ttu-id="ccf9d-127">Ejemplo de respuesta UpdateInboxRules (Create Rule)</span><span class="sxs-lookup"><span data-stu-id="ccf9d-127">UpdateInboxRules (Create Rule) response example</span></span>

### <a name="description"></a><span data-ttu-id="ccf9d-128">Description</span><span class="sxs-lookup"><span data-stu-id="ccf9d-128">Description</span></span>

<span data-ttu-id="ccf9d-129">El siguiente ejemplo del cuerpo del Protocolo simple de acceso a objetos (SOAP) muestra una respuesta correcta a la solicitud **UpdateInboxRules** que crea una regla.</span><span class="sxs-lookup"><span data-stu-id="ccf9d-129">The following Simple Object Access Protocol (SOAP) body example shows a successful response to the **UpdateInboxRules** request that creates a rule.</span></span> 
  
### <a name="code"></a><span data-ttu-id="ccf9d-130">Código</span><span class="sxs-lookup"><span data-stu-id="ccf9d-130">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
        MinorVersion="1" 
        MajorBuildNumber="139" 
        MinorBuildNumber="0" Version="Exchange2010_SP1" 
        xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <UpdateInboxRulesResponse 
         ResponseClass="Success" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
    </UpdateInboxRulesResponse>
  </s:Body>
</s:Envelope>

```

### <a name="successful-response-elements"></a><span data-ttu-id="ccf9d-131">Elementos Response correcto</span><span class="sxs-lookup"><span data-stu-id="ccf9d-131">Successful response elements</span></span>

<span data-ttu-id="ccf9d-132">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="ccf9d-132">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="ccf9d-133">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="ccf9d-133">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="ccf9d-134">UpdateInboxRulesResponse</span><span class="sxs-lookup"><span data-stu-id="ccf9d-134">UpdateInboxRulesResponse</span></span>](updateinboxrulesresponse.md)
    
- [<span data-ttu-id="ccf9d-135">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="ccf9d-135">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="ccf9d-136">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="ccf9d-136">ResponseCode</span></span>](responsecode.md)
    
## <a name="updateinboxrules-set-rule-request-example"></a><span data-ttu-id="ccf9d-137">Ejemplo de solicitud de UpdateInboxRules (Set Rule)</span><span class="sxs-lookup"><span data-stu-id="ccf9d-137">UpdateInboxRules (Set Rule) request example</span></span>

<span data-ttu-id="ccf9d-138">Puede usar los servicios web Exchange para modificar una regla de bandeja de entrada en el buzón de un usuario en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ccf9d-138">You can use Exchange Web Services to modify an Inbox rule in a user's mailbox in the Exchange store.</span></span> <span data-ttu-id="ccf9d-139">Use el elemento [UpdateInboxRules](updateinboxrules.md) junto con el elemento [SetRuleOperation](setruleoperation.md) para modificar una regla.</span><span class="sxs-lookup"><span data-stu-id="ccf9d-139">Use the [UpdateInboxRules](updateinboxrules.md) element in conjunction with the [SetRuleOperation](setruleoperation.md) element to modify a rule.</span></span> 
  
### <a name="description"></a><span data-ttu-id="ccf9d-140">Description</span><span class="sxs-lookup"><span data-stu-id="ccf9d-140">Description</span></span>

<span data-ttu-id="ccf9d-141">El cliente crea el XML de la solicitud y lo envía al servidor.</span><span class="sxs-lookup"><span data-stu-id="ccf9d-141">The client constructs the request XML and sends it to the server.</span></span>
  
### <a name="code"></a><span data-ttu-id="ccf9d-142">Código</span><span class="sxs-lookup"><span data-stu-id="ccf9d-142">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version ="Exchange2010_SP1"/>
  </soap:Header>
  <soap:Body>
      <m:UpdateInboxRules>
        <m:RemoveOutlookRuleBlob>true</m:RemoveOutlookRuleBlob>
        <Operations xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
          <SetRuleOperation xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
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

### <a name="comments"></a><span data-ttu-id="ccf9d-143">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ccf9d-143">Comments</span></span>

<span data-ttu-id="ccf9d-144">En este ejemplo se cambia el nombre para mostrar por "(modificado) se trata de correo no deseado".</span><span class="sxs-lookup"><span data-stu-id="ccf9d-144">This example changes the display name to "(Modified) This is Junk".</span></span>
  
> [!NOTE]
> <span data-ttu-id="ccf9d-145">Los valores de los atributos **ID** y **changekey** del elemento [FolderId](folderid.md) se han abreviado para facilitar su lectura.</span><span class="sxs-lookup"><span data-stu-id="ccf9d-145">The values of the **Id** and **ChangeKey** attributes of the [FolderId](folderid.md) element have been shortened for readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="ccf9d-146">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="ccf9d-146">Request elements</span></span>

<span data-ttu-id="ccf9d-147">La solicitud **UpdateInboxRules** incluye los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="ccf9d-147">The **UpdateInboxRules** request includes the following elements:</span></span> 
  
- [<span data-ttu-id="ccf9d-148">MailboxSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="ccf9d-148">MailboxSmtpAddress</span></span>](mailboxsmtpaddress.md)
    
- [<span data-ttu-id="ccf9d-149">RemoveOutlookRuleBlob</span><span class="sxs-lookup"><span data-stu-id="ccf9d-149">RemoveOutlookRuleBlob</span></span>](removeoutlookruleblob.md)
    
- [<span data-ttu-id="ccf9d-150">Operations</span><span class="sxs-lookup"><span data-stu-id="ccf9d-150">Operations</span></span>](operations.md)
    
<span data-ttu-id="ccf9d-151">El elemento [Operations](operations.md) contiene el elemento [SetRuleOperation](setruleoperation.md) para modificar una regla.</span><span class="sxs-lookup"><span data-stu-id="ccf9d-151">The [Operations](operations.md) element contains the [SetRuleOperation](setruleoperation.md) element to modify a rule.</span></span> 
  
## <a name="updateinboxrules-set-rule-response-example"></a><span data-ttu-id="ccf9d-152">Ejemplo de respuesta UpdateInboxRules (Set Rule)</span><span class="sxs-lookup"><span data-stu-id="ccf9d-152">UpdateInboxRules (Set Rule) response example</span></span>

### <a name="description"></a><span data-ttu-id="ccf9d-153">Description</span><span class="sxs-lookup"><span data-stu-id="ccf9d-153">Description</span></span>

<span data-ttu-id="ccf9d-154">El siguiente ejemplo del cuerpo del Protocolo simple de acceso a objetos (SOAP) muestra una respuesta correcta a la solicitud **UpdateInboxRules** que modifica una regla.</span><span class="sxs-lookup"><span data-stu-id="ccf9d-154">The following Simple Object Access Protocol (SOAP) body example shows a successful response to the **UpdateInboxRules** request that modifies a rule.</span></span> 
  
### <a name="code"></a><span data-ttu-id="ccf9d-155">Código</span><span class="sxs-lookup"><span data-stu-id="ccf9d-155">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
        MinorVersion="1" 
        MajorBuildNumber="139" 
        MinorBuildNumber="0" 
        Version="Exchange2010_SP1" 
        xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <UpdateInboxRulesResponse 
          ResponseClass="Success" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
    </UpdateInboxRulesResponse>
  </s:Body>
</s:Envelope>

```

### <a name="successful-response-elements"></a><span data-ttu-id="ccf9d-156">Elementos Response correcto</span><span class="sxs-lookup"><span data-stu-id="ccf9d-156">Successful response elements</span></span>

<span data-ttu-id="ccf9d-157">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="ccf9d-157">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="ccf9d-158">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="ccf9d-158">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="ccf9d-159">UpdateInboxRulesResponse</span><span class="sxs-lookup"><span data-stu-id="ccf9d-159">UpdateInboxRulesResponse</span></span>](updateinboxrulesresponse.md)
    
- [<span data-ttu-id="ccf9d-160">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="ccf9d-160">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="ccf9d-161">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="ccf9d-161">ResponseCode</span></span>](responsecode.md)
    
## <a name="updateinboxrules-delete-rule-request-example"></a><span data-ttu-id="ccf9d-162">Ejemplo de solicitud UpdateInboxRules (Delete Rule)</span><span class="sxs-lookup"><span data-stu-id="ccf9d-162">UpdateInboxRules (Delete Rule) request example</span></span>

<span data-ttu-id="ccf9d-163">Puede usar los servicios web Exchange para eliminar una regla de bandeja de entrada en el buzón de un usuario en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ccf9d-163">You can use Exchange Web Services to delete an Inbox rule in a user's mailbox in the Exchange store.</span></span> <span data-ttu-id="ccf9d-164">Use [UpdateInboxRules](updateinboxrules.md) junto con el elemento [DeleteRuleOperation](deleteruleoperation.md) para eliminar una regla.</span><span class="sxs-lookup"><span data-stu-id="ccf9d-164">Use the [UpdateInboxRules](updateinboxrules.md) in conjunction with the [DeleteRuleOperation](deleteruleoperation.md) element to delete a rule.</span></span> 
  
### <a name="description"></a><span data-ttu-id="ccf9d-165">Description</span><span class="sxs-lookup"><span data-stu-id="ccf9d-165">Description</span></span>

<span data-ttu-id="ccf9d-166">El cliente crea el XML de la solicitud y lo envía al servidor.</span><span class="sxs-lookup"><span data-stu-id="ccf9d-166">The client constructs the request XML and sends it to the server.</span></span>
  
### <a name="code"></a><span data-ttu-id="ccf9d-167">Código</span><span class="sxs-lookup"><span data-stu-id="ccf9d-167">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a><span data-ttu-id="ccf9d-168">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ccf9d-168">Comments</span></span>

<span data-ttu-id="ccf9d-169">En este ejemplo se elimina la regla identificada existente.</span><span class="sxs-lookup"><span data-stu-id="ccf9d-169">This example deletes the existing identified rule.</span></span>
  
### <a name="request-elements"></a><span data-ttu-id="ccf9d-170">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="ccf9d-170">Request elements</span></span>

<span data-ttu-id="ccf9d-171">La solicitud **UpdateInboxRules** incluye los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="ccf9d-171">The **UpdateInboxRules** request includes the following elements:</span></span> 
  
- [<span data-ttu-id="ccf9d-172">MailboxSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="ccf9d-172">MailboxSmtpAddress</span></span>](mailboxsmtpaddress.md)
    
- [<span data-ttu-id="ccf9d-173">RemoveOutlookRuleBlob</span><span class="sxs-lookup"><span data-stu-id="ccf9d-173">RemoveOutlookRuleBlob</span></span>](removeoutlookruleblob.md)
    
- [<span data-ttu-id="ccf9d-174">Operations</span><span class="sxs-lookup"><span data-stu-id="ccf9d-174">Operations</span></span>](operations.md)
    
<span data-ttu-id="ccf9d-175">El elemento [Operations](operations.md) contiene el elemento [DeleteRuleOperation](deleteruleoperation.md) para eliminar una regla.</span><span class="sxs-lookup"><span data-stu-id="ccf9d-175">The [Operations](operations.md) element contains the [DeleteRuleOperation](deleteruleoperation.md) element to delete a rule.</span></span> 
  
## <a name="updateinboxrules-delete-rule-response-example"></a><span data-ttu-id="ccf9d-176">Ejemplo de respuesta UpdateInboxRules (Delete Rule)</span><span class="sxs-lookup"><span data-stu-id="ccf9d-176">UpdateInboxRules (Delete Rule) response example</span></span>

### <a name="description"></a><span data-ttu-id="ccf9d-177">Description</span><span class="sxs-lookup"><span data-stu-id="ccf9d-177">Description</span></span>

<span data-ttu-id="ccf9d-178">El siguiente ejemplo del cuerpo del Protocolo simple de acceso a objetos (SOAP) muestra una respuesta correcta a la solicitud **UpdateInboxRules** que elimina una regla.</span><span class="sxs-lookup"><span data-stu-id="ccf9d-178">The following Simple Object Access Protocol (SOAP) body example shows a successful response to the **UpdateInboxRules** request that deletes a rule.</span></span> 
  
### <a name="code"></a><span data-ttu-id="ccf9d-179">Código</span><span class="sxs-lookup"><span data-stu-id="ccf9d-179">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
        MinorVersion="1" 
        MajorBuildNumber="139" 
        MinorBuildNumber="0" 
        Version="Exchange2010_SP1" 
        xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <UpdateInboxRulesResponse ResponseClass="Success" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
    </UpdateInboxRulesResponse>
  </s:Body>
</s:Envelope>

```

### <a name="successful-response-elements"></a><span data-ttu-id="ccf9d-180">Elementos Response correcto</span><span class="sxs-lookup"><span data-stu-id="ccf9d-180">Successful response elements</span></span>

<span data-ttu-id="ccf9d-181">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="ccf9d-181">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="ccf9d-182">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="ccf9d-182">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="ccf9d-183">UpdateInboxRulesResponse</span><span class="sxs-lookup"><span data-stu-id="ccf9d-183">UpdateInboxRulesResponse</span></span>](updateinboxrulesresponse.md)
    
- [<span data-ttu-id="ccf9d-184">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="ccf9d-184">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="ccf9d-185">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="ccf9d-185">ResponseCode</span></span>](responsecode.md)
    
## <a name="see-also"></a><span data-ttu-id="ccf9d-186">Vea también</span><span class="sxs-lookup"><span data-stu-id="ccf9d-186">See also</span></span>



[<span data-ttu-id="ccf9d-187">Operación de GetInboxRules</span><span class="sxs-lookup"><span data-stu-id="ccf9d-187">GetInboxRules operation</span></span>](getinboxrules-operation.md)

