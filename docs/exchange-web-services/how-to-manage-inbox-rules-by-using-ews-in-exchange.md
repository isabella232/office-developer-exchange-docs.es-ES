---
title: Administrar las reglas de la Bandeja de entrada mediante EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 982ddb78-5606-44b0-8aba-dbffc60d6085
description: Obtenga información sobre cómo obtener, crear, actualizar y eliminar reglas de la Bandeja de entrada mediante la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: 0f220ad74792e55bb5d1147b0d93ee66d469048b
ms.sourcegitcommit: f13a3a4a61fa23ca6414b7c96ddf087adbe3dc9e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/11/2021
ms.locfileid: "60262207"
---
# <a name="manage-inbox-rules-by-using-ews-in-exchange"></a>Administrar las reglas de la Bandeja de entrada mediante EWS en Exchange

Obtenga información sobre cómo obtener, crear, actualizar y eliminar reglas de la Bandeja de entrada mediante la API administrada de EWS o EWS en Exchange.
  
Puede obtener, crear, actualizar y eliminar reglas de la Bandeja de entrada mediante la API administrada de EWS o EWS. Independientemente de la tecnología que use, se obtienen y modifican reglas de la Bandeja de entrada como una colección y no de manera individual. Use el mismo método u operación para crear reglas nuevas, actualizar las existentes y eliminarlas.  
  
**Tabla 1. Métodos y operaciones para obtener y modificar las reglas de la Bandeja de entrada**

|**Para**|**Método de la API administrada de EWS**|**Operación de EWS**|
|:-----|:-----|:-----|
|Obtener las reglas de la Bandeja de entrada  <br/> |[ExchangeService.GetInboxRules](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.getinboxrules%28v=exchg.80%29.aspx) <br/> |[GetInboxRules](https://msdn.microsoft.com/library/b4b2701a-4a23-4acc-8c75-19f7955ad7ae%28Office.15%29.aspx) <br/> |
|Crear, actualizar o eliminar reglas de la Bandeja de entrada  <br/> |[ExchangeService.UpdateInboxRules](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.updateinboxrules%28v=exchg.80%29.aspx) <br/> |[UpdateInboxRules](https://msdn.microsoft.com/library/f982a237-471e-45c5-a2b5-468cfc53150b%28Office.15%29.aspx) <br/> |
   
Para crear, actualizar o eliminar reglas de la Bandeja de entrada mediante la API administrada de EWS o EWS, debe quitar la regla de Outlook, si existe. Si usa la API administrada de EWS, puede hacerlo estableciendo el parámetro **removeOutlookRulesBlob** en **true** en la llamada al método **ExchangeService.UpdateInboxRules**. Si usa EWS, establezca el valor del elemento [RemoveOutlookRuleBlob](https://msdn.microsoft.com/library/69614475-8bd3-4475-b988-614fe9cad8ef%28Office.15%29.aspx) en **true** en la operación **UpdateInboxRules**. Recomendamos que su aplicación compruebe la propiedad [RuleCollection.OutlookRuleBlobExists](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.rulecollection.outlookruleblobexists%28v=exchg.80%29.aspx) (si está usando la API administrada de EWS) o el elemento [OutlookRuleBlobExists](https://msdn.microsoft.com/library/ae1bc448-deb9-4b5b-ab38-4b276abcb650%28Office.15%29.aspx) (si está usando EWS) antes de actualizar las reglas de la Bandeja de entrada. Si está propiedad o elemento tiene un valor **true**, la aplicación debería avisar al usuario de que se perderá cualquier regla deshabilitada como parte de la actualización, y solo continuará con su permiso.
  
Cuando llama al método **UpdateInboxRules**, EWS elimina las reglas de envío del lado cliente. Las reglas de envío del lado cliente se almacenan en el cliente en el Mensaje de información asociada de carpetas (FAI) de la regla y en ningún otro lugar. EWS elimina este mensaje FAI de la regla de manera predeterminada, basándose en la expectativa de que Outlook volverá a crearlo. En cambio, Outlook no puede volver a crear reglas que tampoco existen como una regla extendida, y las reglas de envío del lado cliente no existen como reglas extendidas. Como resultado, estas reglas se pierden. Le sugerimos que considere esta posibilidad al diseñar su solución. 
  
> [!NOTE]
> Los ejemplos de código de la API administrada de EWS de este artículo usan un [conjunto común de métodos de utilidad](how-to-manage-inbox-rules-by-using-ews-in-exchange.md#bk_UtilitySource). Estos métodos se omiten de los ejemplos de código para mayor brevedad. 
  
## <a name="get-inbox-rules-by-using-the-ews-managed-api"></a>Obtener las reglas de la Bandeja de entrada mediante la API administrada de EWS
<a name="bk_GetRulesEWSMA"> </a>

Para obtener las reglas de bandeja de entrada actuales, utilice el método [ExchangeService.GetInboxRules](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.getinboxrules%28v=exchg.80%29.aspx). Este método devuelve un objeto [RuleCollection](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.rulecollection%28v=exchg.80%29.aspx) que contiene todas las reglas de bandeja de entrada actuales. 
  
En este ejemplo, cada regla de la bandeja de entrada actual se pasa a una función auxiliar (**ParseRuleDetails**) para mostrar los detalles de la regla. 
  
```cs
using System;
using System.Collections.Generic;
using Microsoft.Exchange.WebServices.Data;
private static void GetInboxRules(ExchangeService service, string emailAddress)
{
    RuleCollection inboxRules = null;
    Console.WriteLine("Retrieving inbox rules...");
    // Get the rules from the user's Inbox.
    try
    {
        inboxRules = service.GetInboxRules(emailAddress);
    }
    catch (ServiceResponseException ex)
    {
        Console.WriteLine("Error getting inbox rules: {0}", ex.ErrorCode.ToString());
        return;
    }
    // Loop through the rules and print out the details of each.
    foreach (Rule rule in inboxRules)
    {
        Console.WriteLine("\n***************************************************************");
        Console.WriteLine("Rule: {0}", rule.DisplayName);
        Console.WriteLine("Rule ID: {0}", rule.Id);
        Console.WriteLine("Priority: {0}", rule.Priority);
        Console.WriteLine("Enabled: {0}", rule.IsEnabled.ToString());
        Console.WriteLine("Error: {0}", rule.IsInError.ToString());
        Console.WriteLine("Supported: {0}", (!rule.IsNotSupported).ToString());
        ParseRuleDetails(service, rule);
    }
}
```

## <a name="get-inbox-rules-by-using-ews"></a>Obtener las reglas de la Bandeja de entrada mediante EWS
<a name="bk_GetRulesEWS"> </a>

La siguiente solicitud SOAP de EWS usa [GetInboxRules operation](https://msdn.microsoft.com/library/b4b2701a-4a23-4acc-8c75-19f7955ad7ae%28Office.15%29.aspx) para recuperar las reglas de la Bandeja de entrada de naiara@contoso.com. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
<soap:Header>
  <t:RequestServerVersion Version="Exchange2013" />
</soap:Header>
<soap:Body>
  <m:GetInboxRules>
    <m:MailboxSmtpAddress>sadie@contoso.com</m:MailboxSmtpAddress>
  </m:GetInboxRules>
</soap:Body>
</soap:Envelope>
```

La siguiente respuesta SOAP de EWS contiene las reglas actuales de la Bandeja de entrada de naiara@contoso.com.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
<s:Header>
  <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="712" MinorBuildNumber="22" Version="V2_3" 
      xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
      xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
      xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
      xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
</s:Header>
<s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <GetInboxRulesResponse ResponseClass="Success" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
    <ResponseCode>NoError</ResponseCode>
    <OutlookRuleBlobExists>false</OutlookRuleBlobExists>
    <InboxRules>
      <Rule xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
        <RuleId>AQAAAAAAASY=</RuleId>
        <DisplayName>Alfred</DisplayName>
        <Priority>1</Priority>
        <IsEnabled>true</IsEnabled>
        <Conditions>
          <FromAddresses>
            <Address>
              <Name>Alfred Welker</Name>
              <EmailAddress>/o=First Organization/ou=Exchange Administrative Group (FYDIBOHF23SPDLT)/cn=Recipients/cn=9a83e6380cae41918c71e7921d960b5a-Alfre</EmailAddress>
              <RoutingType>EX</RoutingType>
            </Address>
          </FromAddresses>
        </Conditions>
        <Actions>
          <MoveToFolder>
            <FolderId Id="AAMkADg1OWUwODcyLTg4M2MtNDAyMS05YjI0LTI5ZGM5OTU4Njk3YwAuAAAAAADPriAxh444TpHj2GoQxWQNAQAN+VjmVZl5Rq1ymCq5eFKOAAAAABSyAAA=" ChangeKey="AQAAAA==" />
          </MoveToFolder>
          <StopProcessingRules>true</StopProcessingRules>
        </Actions>
      </Rule>
      <Rule xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
        <RuleId>AQAAAAAAASQ=</RuleId>
        <DisplayName>Important</DisplayName>
        <Priority>2</Priority>
        <IsEnabled>true</IsEnabled>
        <Conditions>
          <ContainsSubjectStrings>
            <String>Urgent</String>
          </ContainsSubjectStrings>
          <FromAddresses>
            <Address>
              <Name>Hope Gross</Name>
              <EmailAddress>/o=First Organization/ou=Exchange Administrative Group (FYDIBOHF23SPDLT)/cn=Recipients/cn=9b55e4100c064d9d8c5f72ff36802ed3-Hope</EmailAddress>
              <RoutingType>EX</RoutingType>
            </Address>
          </FromAddresses>
        </Conditions>
        <Actions>
          <MarkImportance>High</MarkImportance>
          <StopProcessingRules>true</StopProcessingRules>
        </Actions>
      </Rule>
    </InboxRules>
  </GetInboxRulesResponse>
</s:Body>
</s:Envelope>
```

## <a name="create-inbox-rules-by-using-the-ews-managed-api"></a>Crear las reglas de la Bandeja de entrada mediante la API administrada de EWS
<a name="bk_CreateRulesEWSMA"> </a>

Para crear una regla, incluya un objeto [CreateRuleOperation](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.createruleoperation%28v=exchg.80%29.aspx) en la colección de objetos [RuleOperation](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.ruleoperation%28v=exchg.80%29.aspx) que se pasaron al método [ExchangeService.UpdateInboxRules](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.updateinboxrules%28v=exchg.80%29.aspx). 
  
En este ejemplo, se crea una regla nueva para mover el correo que se ha enviado a una lista de distribución denominada "Ventas" a una subcarpeta de la bandeja de entrada, también denominada "Ventas".
  
```cs
using System;
using System.Collections.Generic;
using Microsoft.Exchange.WebServices.Data;
private static void CreateInboxRule(ExchangeService service, string emailAddress)
{
    // Before modifying the rules on the server, determine
    // whether an Outlook rules BLOB exists. Updating rules
    // via EWS requires removal of the Outlook BLOB. This can
    // result in any rules that the user has disabled via the Outlook
    // UI to be lost.
    RuleCollection currentRules = null;
    try
    {
        currentRules = service.GetInboxRules(emailAddress);
    }
    catch (ServiceResponseException ex)
    {
        Console.WriteLine("Error getting inbox rules: {0}", ex.ErrorCode.ToString());
    }
    if (currentRules != null && currentRules.OutlookRuleBlobExists)
    {
        Console.WriteLine("WARNING: Adding a new rule will delete the Outlook rule BLOB.");
        Console.WriteLine("This can lead to a loss of any disabled rules.");
        Console.Write("Hit Y to proceed (any other key to cancel): ");
        ConsoleKeyInfo cki = Console.ReadKey();
        if (cki.KeyChar != 'Y' && cki.KeyChar != 'y')
        {
            Console.WriteLine("\nCanceling addition of new rule...");
            return;
        }
        Console.WriteLine();
    }
    Console.WriteLine("Adding \"Sales\" rule.");
    Rule newRule = new Rule();
    // Creating a rule called "Sales"
    newRule.DisplayName = "Sales";
    // Conditions
    // When messages are sent to the "Sales" address (sales@contoso.com),
    newRule.Conditions.SentToAddresses.Add("Sales", "sales@contoso.com");
    FolderId moveToFolderId = GetFolderIdByName(service, WellKnownFolderName.Inbox, "Sales");
    if (moveToFolderId == null)
    {
        throw new ArgumentException("Invalid subfolder specified");
    }
    // Actions
    // Move the message to the "Sales" folder
    newRule.Actions.MoveToFolder = moveToFolderId;
    // And stop processing more rules
    newRule.Actions.StopProcessingRules = true;
    // Exceptions
    // Except if the message is from Hope Gross (hope@contoso.com).
    newRule.Exceptions.FromAddresses.Add("Hope Gross", "hope@contoso.com");
    Console.WriteLine("Rule: {0}", newRule.DisplayName);
    ParseRuleDetails(service, newRule);
    // Add the new rule to the CreateRule operation.
    CreateRuleOperation createMoveIfFromSalesRule = new CreateRuleOperation(newRule);
    try
    {
        // Update rules. Note that this method can accept
        // an array of rule operations, enabling you to batch
        // updates.
        service.UpdateInboxRules(new RuleOperation[] { createMoveIfFromSalesRule }, true);
    }
    catch (UpdateInboxRulesException ex)
    {
        Console.WriteLine("Error updating Inbox rules: {0}", ex.ErrorCode.ToString());
        return;
    }
    Console.WriteLine("Rule added.");
}
```

## <a name="create-inbox-rules-by-using-ews"></a>Crear las reglas de la Bandeja de entrada mediante EWS
<a name="bk_CreateRulesEWS"> </a>

La siguiente solicitud SOAP de EWS crea la regla "Ventas" en la bandeja de entrada de naiara@contoso.com.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
  <soap:Body>
    <m:UpdateInboxRules>
      <m:RemoveOutlookRuleBlob>true</m:RemoveOutlookRuleBlob>
      <m:Operations>
        <t:CreateRuleOperation>
          <t:Rule>
            <t:DisplayName>Sales</t:DisplayName>
            <t:Priority>1</t:Priority>
            <t:IsEnabled>true</t:IsEnabled>
            <t:IsInError>false</t:IsInError>
            <t:Conditions>
              <t:SentToAddresses>
                <t:Address>
                  <t:Name>Sales</t:Name>
                  <t:EmailAddress>sales@contoso.com</t:EmailAddress>
                </t:Address>
              </t:SentToAddresses>
            </t:Conditions>
            <t:Exceptions>
              <t:FromAddresses>
                <t:Address>
                  <t:Name>Hope Gross</t:Name>
                  <t:EmailAddress>hope@contoso.com</t:EmailAddress>
                </t:Address>
              </t:FromAddresses>
            </t:Exceptions>
            <t:Actions>
              <t:MoveToFolder>
                <t:FolderId Id="AAMkADg1OWUwODcyLTg4M2MtNDAyMS05YjI0LTI5ZGM5OTU4Njk3YwAuAAAAAADPriAxh444TpHj2GoQxWQNAQAN+VjmVZl5Rq1ymCq5eFKOAAAAABSxAAA=" 
                    ChangeKey="AQAAABYAAAAN+VjmVZl5Rq1ymCq5eFKOAAAAABTZ" />
              </t:MoveToFolder>
              <t:StopProcessingRules>true</t:StopProcessingRules>
            </t:Actions>
          </t:Rule>
        </t:CreateRuleOperation>
      </m:Operations>
    </m:UpdateInboxRules>
  </soap:Body>
</soap:Envelope>
```

## <a name="update-inbox-rules-by-using-the-ews-managed-api"></a>Actualizar las reglas de la Bandeja de entrada mediante la API administrada de EWS
<a name="bk_UpdateRulesEWSMA"> </a>

Para actualizar una regla, incluya un objeto [SetRuleOperation](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.setruleoperation%28v=exchg.80%29.aspx) de la colección de objetos **RuleOperation** que se pasaron al método **UpdateInboxRules**. 
  
En este ejemplo, la regla "Ventas" se actualiza para agregar una excepción. Si el asunto contiene la palabra "Urgente", los mensajes no se moverán a la subcarpeta "Ventas".
  
```cs
using System;
using System.Collections.Generic;
using Microsoft.Exchange.WebServices.Data;
private static void UpdateInboxRule(ExchangeService service, string emailAddress)
{
    // Before modifying the rules on the server, determine
    // whether an Outlook rules BLOB exists. Updating rules
    // via EWS requires removal of the Outlook BLOB. This can
    // result in any rules that the user has disabled via the Outlook
    // UI to be lost.
    RuleCollection currentRules = null;
    try
    {
        currentRules = service.GetInboxRules(emailAddress);
    }
    catch (ServiceResponseException ex)
    {
        Console.WriteLine("Error getting inbox rules: {0}", ex.ErrorCode.ToString());
    }
    if (currentRules != null && currentRules.OutlookRuleBlobExists)
    {
        Console.WriteLine("WARNING: Updating an existing rule will delete the Outlook rule BLOB.");
        Console.WriteLine("This can lead to a loss of any disabled rules.");
        Console.Write("Hit Y to proceed (any other key to cancel): ");
        ConsoleKeyInfo cki = Console.ReadKey();
        if (cki.KeyChar != 'Y' && cki.KeyChar != 'y')
        {
            Console.WriteLine("\nCanceling update of rule...");
            return;
        }
        Console.WriteLine();
    }
    // Look for the rule called "Sales" and modify it
    // to add an exception if "Urgent" is in the subject.
    Console.WriteLine("Updating rule \"Sales\"...");
    Rule ruleToUpdate = null;
    foreach (Rule rule in currentRules)
    {
        if (rule.DisplayName == "Sales")
        {
            ruleToUpdate = rule;
            break;
        }
    }
    if (ruleToUpdate == null)
    {
        Console.WriteLine("Could not find a rule called \"Sales\", canceling update.");
        return;
    }
    // Add the exception.
    ruleToUpdate.Exceptions.ContainsSubjectStrings.Add("Urgent");
    SetRuleOperation setRuleOperation = new SetRuleOperation(ruleToUpdate);
    try
    {
        // Update rules. Note that this method can accept
        // an array of rule operations, enabling you to batch
        // updates.
        service.UpdateInboxRules(new RuleOperation[] { setRuleOperation }, true);
    }
    catch (UpdateInboxRulesException ex)
    {
        Console.WriteLine("Error updating Inbox rules: {0}", ex.ErrorCode.ToString());
        return;
    }
    Console.WriteLine("Rule updated.");
}
```

## <a name="update-inbox-rules-by-using-ews"></a>Actualizar las reglas de la Bandeja de entrada mediante EWS
<a name="bk_UpdateRulesEWS"> </a>

La siguiente solicitud SOAP de EWS actualiza la regla "Ventas" en la bandeja de entrada de naiara@contoso.com.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
  <soap:Body>
    <m:UpdateInboxRules>
      <m:RemoveOutlookRuleBlob>true</m:RemoveOutlookRuleBlob>
      <m:Operations>
        <t:SetRuleOperation>
          <t:Rule>
            <t:RuleId>AQAAAATnzOA=</t:RuleId>
            <t:DisplayName>Sales</t:DisplayName>
            <t:Priority>1</t:Priority>
            <t:IsEnabled>true</t:IsEnabled>
            <t:IsInError>false</t:IsInError>
            <t:Conditions>
              <t:SentToAddresses>
                <t:Address>
                  <t:Name>Sales</t:Name>
                  <t:EmailAddress>sales@contoso.com</t:EmailAddress>
                  <t:RoutingType>SMTP</t:RoutingType>
                </t:Address>
              </t:SentToAddresses>
            </t:Conditions>
            <t:Exceptions>
              <t:ContainsSubjectStrings>
                <t:String>Urgent</t:String>
              </t:ContainsSubjectStrings>
              <t:FromAddresses>
                <t:Address>
                  <t:Name>Hope Gross</t:Name>
                  <t:EmailAddress>hope@contoso.com</t:EmailAddress>
                  <t:RoutingType>SMTP</t:RoutingType>
                </t:Address>
              </t:FromAddresses>
            </t:Exceptions>
            <t:Actions>
              <t:MoveToFolder>
                <t:FolderId Id="AAMkADg1OWUwODcyLTg4M2MtNDAyMS05YjI0LTI5ZGM5OTU4Njk3YwAuAAAAAADPriAxh444TpHj2GoQxWQNAQAN+VjmVZl5Rq1ymCq5eFKOAAAAABSxAAA=" 
                    ChangeKey="AQAAAA==" />
              </t:MoveToFolder>
              <t:StopProcessingRules>true</t:StopProcessingRules>
            </t:Actions>
          </t:Rule>
        </t:SetRuleOperation>
      </m:Operations>
    </m:UpdateInboxRules>
  </soap:Body>
</soap:Envelope>
```

## <a name="delete-inbox-rules-by-using-the-ews-managed-api"></a>Eliminar las reglas de la Bandeja de entrada mediante la API administrada de EWS
<a name="bk_DeleteRulesEWSMA"> </a>

Para eliminar una regla, incluya un objeto [DeleteRuleOperation](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.deleteruleoperation%28v=exchg.80%29.aspx) en la colección de objetos **RuleOperation** que se pasaron al método **UpdateInboxRules**. 
  
En este ejemplo, la regla "Ventas" se elimina.
  
```cs
using System;
using System.Collections.Generic;
using Microsoft.Exchange.WebServices.Data;
private static void DeleteInboxRule(ExchangeService service, string emailAddress)
{
    // Before modifying the rules on the server, determine
    // whether an Outlook rules BLOB exists. Updating rules
    // via EWS requires removal of the Outlook BLOB. This can
    // result in any rules that the user has disabled via the Outlook
    // UI to be lost.
    RuleCollection currentRules = null;
    try
    {
        currentRules = service.GetInboxRules(emailAddress);
    }
    catch (ServiceResponseException ex)
    {
        Console.WriteLine("Error getting inbox rules: {0}", ex.ErrorCode.ToString());
    }
    if (currentRules != null && currentRules.OutlookRuleBlobExists)
    {
        Console.WriteLine("WARNING: Deleting a rule will delete the Outlook rule BLOB.");
        Console.WriteLine("This can lead to a loss of any disabled rules.");
        Console.Write("Hit Y to proceed (any other key to cancel): ");
        ConsoleKeyInfo cki = Console.ReadKey();
        if (cki.KeyChar != 'Y' && cki.KeyChar != 'y')
        {
            Console.WriteLine("\nCancelling deletion of new rule...");
            return;
        }
        Console.WriteLine();
    }
    // Look for the rule called "Sales" and delete it.
    Console.WriteLine("Deleting rule \"Sales\"...");
    string ruleId = string.Empty;
    foreach (Rule rule in currentRules)
    {
        if (rule.DisplayName == "Sales")
        {
            ruleId = rule.Id;
            break;
        }
    }
    if (string.IsNullOrEmpty(ruleId))
    {
        Console.WriteLine("Could not find a rule called \"Sales\", canceling delete.");
        return;
    }
    DeleteRuleOperation deleteRuleOperation = new DeleteRuleOperation(ruleId);
    try
    {
        // Update rules. Note that this method can accept
        // an array of rule operations, enabling you to batch
        // updates.
        service.UpdateInboxRules(new RuleOperation[] { deleteRuleOperation }, true);
    }
    catch (UpdateInboxRulesException ex)
    {
        Console.WriteLine("Error updating Inbox rules: {0}", ex.ErrorCode.ToString());
        return;
    }
    Console.WriteLine("Rule deleted.");
}
```

## <a name="delete-inbox-rules-by-using-ews"></a>Eliminar las reglas de la Bandeja de entrada mediante EWS
<a name="bk_DeleteRulesEWS"> </a>

La siguiente solicitud SOAP de EWS elimina la regla "Ventas" en la bandeja de entrada de naiara@contoso.com.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
  <soap:Body>
    <m:UpdateInboxRules>
      <m:RemoveOutlookRuleBlob>true</m:RemoveOutlookRuleBlob>
      <m:Operations>
        <t:DeleteRuleOperation>
          <t:RuleId>AQAAAATnzOA=</t:RuleId>
        </t:DeleteRuleOperation>
      </m:Operations>
    </m:UpdateInboxRules>
  </soap:Body>
</soap:Envelope>
```

## <a name="source-for-sample-utility-methods"></a>Origen de los métodos de utilidad de ejemplo
<a name="bk_UtilitySource"> </a>

Los ejemplos de la API administrada de EWS de este artículo usan los métodos de utilidad que están incluidos en el siguiente ejemplo.
  
```cs
private static void ParseRuleDetails(ExchangeService service, Rule rule)
{
    // Conditions
    string conditions = ParseRulePredicates(rule.Conditions, false);
    if (!string.IsNullOrEmpty(conditions))
    {
        Console.WriteLine("When a message:");
        Console.WriteLine(conditions);
    }
    // Actions
    string actions = ParseRuleActions(service, rule.Actions);
    if (!string.IsNullOrEmpty(actions))
    {
        Console.WriteLine("Take the following action(s):");
        Console.WriteLine(actions);
    }
    // Exceptions
    string exceptions = ParseRulePredicates(rule.Exceptions, true);
    if (!string.IsNullOrEmpty(exceptions))
    {
        Console.WriteLine("Except when the message:");
        Console.WriteLine(exceptions);
    }
}
private static string ParseRulePredicates(RulePredicates predicates, bool isExceptions)
{
    string humanReadablePredicates = string.Empty;
    foreach (string category in predicates.Categories)
    {
        humanReadablePredicates = AppendToHumanReadableString(humanReadablePredicates,
            "has the category \"" + category + "\"", isExceptions);
    }
    foreach (string bodyString in predicates.ContainsBodyStrings)
    {
        humanReadablePredicates = AppendToHumanReadableString(humanReadablePredicates,
            "has \"" + bodyString + "\" in the body", isExceptions);
    }
    foreach (string headerString in predicates.ContainsHeaderStrings)
    {
        humanReadablePredicates = AppendToHumanReadableString(humanReadablePredicates,
            "has \"" + headerString + "\" in the headers", isExceptions);
    }
    foreach (string recipientString in predicates.ContainsRecipientStrings)
    {
        humanReadablePredicates = AppendToHumanReadableString(humanReadablePredicates,
            "has \"" + recipientString + "\" in the recipient's address", isExceptions);
    }
    foreach (string senderString in predicates.ContainsSenderStrings)
    {
        humanReadablePredicates = AppendToHumanReadableString(humanReadablePredicates,
            "has \"" + senderString + "\" in the sender's address", isExceptions);
    }
    foreach (string subjectOrBodyString in predicates.ContainsSubjectOrBodyStrings)
    {
        humanReadablePredicates = AppendToHumanReadableString(humanReadablePredicates,
            "has \"" + subjectOrBodyString + "\" in the subject or body", isExceptions);
    }
    foreach (string subjectString in predicates.ContainsSubjectStrings)
    {
        humanReadablePredicates = AppendToHumanReadableString(humanReadablePredicates,
            "has \"" + subjectString + "\" in the subject", isExceptions);
    }
    if (predicates.FlaggedForAction != null)
    {
        humanReadablePredicates = AppendToHumanReadableString(humanReadablePredicates,
            "is flagged for \"" + predicates.FlaggedForAction.Value + "\" action", isExceptions);
    }
    foreach (EmailAddress fromAddress in predicates.FromAddresses)
    {
        humanReadablePredicates = AppendToHumanReadableString(humanReadablePredicates,
            "is from " + fromAddress.Name + " (" + fromAddress.Address + ")", isExceptions);
    }
    foreach (string fromConnectedAccount in predicates.FromConnectedAccounts)
    {
        humanReadablePredicates = AppendToHumanReadableString(humanReadablePredicates,
            "is from the \"" + fromConnectedAccount + "\" account", isExceptions);
    }
    if (predicates.HasAttachments)
    {
        humanReadablePredicates = AppendToHumanReadableString(humanReadablePredicates,
            "has an attachment", isExceptions);
    }
    if (predicates.Importance != null)
    {
        humanReadablePredicates = AppendToHumanReadableString(humanReadablePredicates,
            "is marked as " + predicates.Importance.Value + " importance", isExceptions);
    }
    if (predicates.IsApprovalRequest)
    {
        humanReadablePredicates = AppendToHumanReadableString(humanReadablePredicates,
            "is an approval request", isExceptions);
    }
    if (predicates.IsAutomaticForward)
    {
        humanReadablePredicates = AppendToHumanReadableString(humanReadablePredicates,
            "is an automatic forward", isExceptions);
    }
    if (predicates.IsAutomaticReply)
    {
        humanReadablePredicates = AppendToHumanReadableString(humanReadablePredicates,
            "is an automatic reply", isExceptions);
    }
    if (predicates.IsEncrypted)
    {
        humanReadablePredicates = AppendToHumanReadableString(humanReadablePredicates,
            "is encrypted", isExceptions);
    }
    if (predicates.IsMeetingRequest)
    {
        humanReadablePredicates = AppendToHumanReadableString(humanReadablePredicates,
            "is a meeting request", isExceptions);
    }
    if (predicates.IsMeetingResponse)
    {
        humanReadablePredicates = AppendToHumanReadableString(humanReadablePredicates,
            "is a meeting response", isExceptions);
    }
    if (predicates.IsNonDeliveryReport)
    {
        humanReadablePredicates = AppendToHumanReadableString(humanReadablePredicates,
            "is a non-delivery report", isExceptions);
    }
    if (predicates.IsPermissionControlled)
    {
        humanReadablePredicates = AppendToHumanReadableString(humanReadablePredicates,
            "is a rights-managed message", isExceptions);
    }
    if (predicates.IsReadReceipt)
    {
        humanReadablePredicates = AppendToHumanReadableString(humanReadablePredicates,
            "is a read receipt", isExceptions);
    }
    if (predicates.IsSigned)
    {
        humanReadablePredicates = AppendToHumanReadableString(humanReadablePredicates,
            "is signed", isExceptions);
    }
    if (predicates.IsVoicemail)
    {
        humanReadablePredicates = AppendToHumanReadableString(humanReadablePredicates,
            "is a voicemail", isExceptions);
    }
    foreach (string messageClass in predicates.ItemClasses)
    {
        humanReadablePredicates = AppendToHumanReadableString(humanReadablePredicates,
            "has a message class of \"" + messageClass + "\"", isExceptions);
    }
    foreach (string messageClassification in predicates.MessageClassifications)
    {
        humanReadablePredicates = AppendToHumanReadableString(humanReadablePredicates,
            "has a classification of \"" + messageClassification + "\"", isExceptions);
    }
    if (predicates.NotSentToMe)
    {
        humanReadablePredicates = AppendToHumanReadableString(humanReadablePredicates,
            "is not sent to me", isExceptions);
    }
    if (predicates.Sensitivity != null)
    {
        humanReadablePredicates = AppendToHumanReadableString(humanReadablePredicates,
            "has a sensitivity of \"" + predicates.Sensitivity.Value + "\"", isExceptions);
    }
    if (predicates.SentCcMe)
    {
        humanReadablePredicates = AppendToHumanReadableString(humanReadablePredicates,
            "has me on the CC line", isExceptions);
    }
    if (predicates.SentOnlyToMe)
    {
        humanReadablePredicates = AppendToHumanReadableString(humanReadablePredicates,
            "is sent ONLY to me", isExceptions);
    }
    foreach (EmailAddress sentToAddress in predicates.SentToAddresses)
    {
        humanReadablePredicates = AppendToHumanReadableString(humanReadablePredicates,
            "is sent to " + sentToAddress.Name + " (" + sentToAddress.Address + ")", isExceptions);
    }
    if (predicates.SentToMe)
    {
        humanReadablePredicates = AppendToHumanReadableString(humanReadablePredicates,
            "has me on the To line", isExceptions);
    }
    if (predicates.SentToOrCcMe)
    {
        humanReadablePredicates = AppendToHumanReadableString(humanReadablePredicates,
            "has me on the To or CC line", isExceptions);
    }
    if (predicates.WithinDateRange != null)
    {
        if (predicates.WithinDateRange.Start != null)
        {
            humanReadablePredicates = AppendToHumanReadableString(humanReadablePredicates,
                "was received after " + predicates.WithinDateRange.Start.ToString(), isExceptions);
        }
        if (predicates.WithinDateRange.End != null)
        {
            humanReadablePredicates = AppendToHumanReadableString(humanReadablePredicates,
                "was recieved before " + predicates.WithinDateRange.End.ToString(), isExceptions);
        }
    }
    if (predicates.WithinSizeRange != null)
    {
        if (predicates.WithinSizeRange.MinimumSize != null)
        {
            humanReadablePredicates = AppendToHumanReadableString(humanReadablePredicates,
                "is larger than " + predicates.WithinSizeRange.MinimumSize + " kb", isExceptions);
        }
        if (predicates.WithinSizeRange.MaximumSize != null)
        {
            humanReadablePredicates = AppendToHumanReadableString(humanReadablePredicates,
                "is smaller than " + predicates.WithinSizeRange.MaximumSize + " kb", isExceptions);
        }
    }
    return humanReadablePredicates;
}
private static string ParseRuleActions(ExchangeService service, RuleActions actions)
{
    string humanReadableActions = string.Empty;
    foreach (string category in actions.AssignCategories)
    {
        humanReadableActions = AppendToHumanReadableString(humanReadableActions,
            "assign the \"" + category + "\" category", false);
    }
    if (actions.CopyToFolder != null)
    {
        humanReadableActions = AppendToHumanReadableString(humanReadableActions,
            "move to the \"" + GetFolderNameFromId(service, actions.CopyToFolder) + "\" folder", false);
    }
    if (actions.Delete)
    {
        humanReadableActions = AppendToHumanReadableString(humanReadableActions,
            "delete the message", false);
    }
    foreach (EmailAddress forwardAddress in actions.ForwardAsAttachmentToRecipients)
    {
        humanReadableActions = AppendToHumanReadableString(humanReadableActions,
            "forward as an attachment to " + forwardAddress.Name + " (" +
            forwardAddress.Address + ")", false);
    }
    foreach (EmailAddress forwardAddress in actions.ForwardToRecipients)
    {
        humanReadableActions = AppendToHumanReadableString(humanReadableActions,
            "forward to " + forwardAddress.Name + " (" + forwardAddress.Address + ")", false);
    }
    if (actions.MarkAsRead)
    {
        humanReadableActions = AppendToHumanReadableString(humanReadableActions,
            "mark the message as read", false);
    }
    if (actions.MarkImportance != null)
    {
        humanReadableActions = AppendToHumanReadableString(humanReadableActions,
            "mark the message with " + actions.MarkImportance.Value + " importance", false);
    }
    if (actions.MoveToFolder != null)
    {
        humanReadableActions = AppendToHumanReadableString(humanReadableActions,
            "move the message to the \"" + GetFolderNameFromId(service, actions.MoveToFolder) + "\" folder", false);
    }
    if (actions.PermanentDelete)
    {
        humanReadableActions = AppendToHumanReadableString(humanReadableActions,
            "permanently delete the message", false);
    }
    foreach (EmailAddress redirectAddress in actions.RedirectToRecipients)
    {
        humanReadableActions = AppendToHumanReadableString(humanReadableActions,
            "redirect the message to " + redirectAddress.Name + " (" +
            redirectAddress.Address + ")", false);
    }
    foreach (MobilePhone smsRecipient in actions.SendSMSAlertToRecipients)
    {
        humanReadableActions = AppendToHumanReadableString(humanReadableActions,
            "send SMS alert to " + smsRecipient.Name + " (" +
            smsRecipient.PhoneNumber + ")", false);
    }
    if (actions.ServerReplyWithMessage != null)
    {
        humanReadableActions = AppendToHumanReadableString(humanReadableActions,
            "have the server reply with a template message, ID=" +
            actions.ServerReplyWithMessage.UniqueId, false);
    }
    if (actions.StopProcessingRules)
    {
        humanReadableActions = AppendToHumanReadableString(humanReadableActions,
            "stop processing more rules", false);
    }
    return humanReadableActions;
}
private static string AppendToHumanReadableString(string humanReadableString, string appendString, bool isExceptions)
{
    // Conditions and Actions are AND'ed together
    string logicalOperator = "AND";
    if (isExceptions)
    {
        // Exceptions are OR'ed
        logicalOperator = "OR";
    }
    if (!string.IsNullOrEmpty(humanReadableString))
    {
        // There's already an item in the list, so we need to
        // add the operator
        humanReadableString += "\n  " + logicalOperator + " ";
    }
    else
    {
        humanReadableString += "  ";
    }
    humanReadableString += appendString;
    return humanReadableString;
}
private static string GetFolderNameFromId(ExchangeService service, FolderId folderId)
{
    string folderName = string.Empty;
    Folder folder = null;
    try
    {
        folder = Folder.Bind(service, folderId);
    }
    catch (ServiceResponseException)
    {
        Console.WriteLine("Unable to bind to the folder specified.");
    }
    if (folder != null)
        folderName = folder.DisplayName;
    return folderName;
}
private static FolderId GetFolderIdByName(ExchangeService service, WellKnownFolderName parentWellKnownFolder, string subFolderName)
{
    FolderId returnId = null;
    Folder parentFolder = null;
    try
    {
        parentFolder = Folder.Bind(service, parentWellKnownFolder);
    }
    catch (ServiceResponseException)
    {
        Console.WriteLine("Unable to bind to the {} folder.", parentWellKnownFolder.ToString());
    }
    if (parentFolder == null)
        return null;
    SearchFilter searchFilter = new SearchFilter.IsEqualTo(FolderSchema.DisplayName, subFolderName);
    FolderView view = new FolderView(10);
    view.PropertySet = new PropertySet(BasePropertySet.IdOnly);
    view.PropertySet.Add(FolderSchema.DisplayName);
    view.Traversal = FolderTraversal.Shallow;
    FindFoldersResults searchResults = null;
    try
    {
        searchResults = parentFolder.FindFolders(searchFilter, view);
    }
    catch (ServiceResponseException ex)
    {
        Console.WriteLine("Error searching for {0} folder: {1}", subFolderName,
            ex.ErrorCode.ToString());
    }
    foreach (Folder subFolder in searchResults.Folders)
    {
        if (subFolder.DisplayName == subFolderName)
            returnId = subFolder.Id;
        break;
    }
    return returnId;
}
```

## <a name="see-also"></a>Vea también


- [Administración de la Bandeja de entrada y EWS en Exchange](inbox-management-and-ews-in-exchange.md)
    
- [Método ExchangeService.GetInboxRules](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.getinboxrules%28v=exchg.80%29.aspx)
    
- [Método ExchangeService.UpdateInboxRules](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.updateinboxrules%28v=exchg.80%29.aspx)
    
- [Operación de GetInboxRules](https://msdn.microsoft.com/library/b4b2701a-4a23-4acc-8c75-19f7955ad7ae%28Office.15%29.aspx)
    
- [Operación de UpdateInboxRules](https://msdn.microsoft.com/library/f982a237-471e-45c5-a2b5-468cfc53150b%28Office.15%29.aspx)
    

