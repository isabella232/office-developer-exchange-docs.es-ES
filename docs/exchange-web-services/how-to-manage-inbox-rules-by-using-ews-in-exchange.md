---
title: Administrar reglas de bandeja de entrada mediante el uso de EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 982ddb78-5606-44b0-8aba-dbffc60d6085
description: Obtenga información sobre cómo obtener, crear, actualizar y eliminar reglas de la Bandeja de entrada mediante la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: 85e166ba57d74c74382b257d01d9bff8f44bade1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763108"
---
# <a name="manage-inbox-rules-by-using-ews-in-exchange"></a><span data-ttu-id="c0dc0-103">Administrar reglas de bandeja de entrada mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="c0dc0-103">Manage Inbox rules by using EWS in Exchange</span></span>

<span data-ttu-id="c0dc0-104">Obtenga información sobre cómo obtener, crear, actualizar y eliminar reglas de la Bandeja de entrada mediante la API administrada de EWS o EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="c0dc0-104">Find out how to get, create, update, and delete Inbox rules by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="c0dc0-p101">Puede obtener, crear, actualizar y eliminar reglas de la Bandeja de entrada mediante la API administrada de EWS o EWS. Independientemente de la tecnología que use, se obtienen y modifican reglas de la Bandeja de entrada como una colección y no de manera individual. Use el mismo método u operación para crear reglas nuevas, actualizar las existentes y eliminarlas. </span><span class="sxs-lookup"><span data-stu-id="c0dc0-p101">You can get, create, update, and delete Inbox rules by using the EWS Managed API or EWS. Regardless of the technology you use, you get and modify Inbox rules as a collection, rather than individually. You use the same method or operation to create new rules, update existing rules, and delete rules.</span></span> 
  
<span data-ttu-id="c0dc0-108">**La tabla 1. Métodos y operaciones para obtener y modificar las reglas de bandeja de entrada**</span><span class="sxs-lookup"><span data-stu-id="c0dc0-108">**Table 1. Methods and operations for getting and modifying Inbox rules**</span></span>

|<span data-ttu-id="c0dc0-109">**Con el fin...**</span><span class="sxs-lookup"><span data-stu-id="c0dc0-109">**In order to…**</span></span>|<span data-ttu-id="c0dc0-110">**Método de la API administrada de EWS**</span><span class="sxs-lookup"><span data-stu-id="c0dc0-110">**EWS Managed API method**</span></span>|<span data-ttu-id="c0dc0-111">**Operación de EWS**</span><span class="sxs-lookup"><span data-stu-id="c0dc0-111">**EWS operation**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c0dc0-112">Obtener las reglas de la Bandeja de entrada</span><span class="sxs-lookup"><span data-stu-id="c0dc0-112">Get Inbox rules</span></span>  <br/> |[<span data-ttu-id="c0dc0-113">ExchangeService.GetInboxRules</span><span class="sxs-lookup"><span data-stu-id="c0dc0-113">ExchangeService.GetInboxRules</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.getinboxrules%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="c0dc0-114">GetInboxRules</span><span class="sxs-lookup"><span data-stu-id="c0dc0-114">GetInboxRules</span></span>](http://msdn.microsoft.com/library/b4b2701a-4a23-4acc-8c75-19f7955ad7ae%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="c0dc0-115">Crear, actualizar o eliminar reglas de la Bandeja de entrada</span><span class="sxs-lookup"><span data-stu-id="c0dc0-115">Create, update, or delete Inbox rules</span></span>  <br/> |[<span data-ttu-id="c0dc0-116">ExchangeService.UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="c0dc0-116">ExchangeService.UpdateInboxRules</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.updateinboxrules%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="c0dc0-117">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="c0dc0-117">UpdateInboxRules</span></span>](http://msdn.microsoft.com/library/f982a237-471e-45c5-a2b5-468cfc53150b%28Office.15%29.aspx) <br/> |
   
<span data-ttu-id="c0dc0-118">Con el fin de crear, actualizar o eliminar las reglas de bandeja de entrada mediante el uso de la API administrada de EWS o EWS, debe quitar la regla de Outlook, si existe.</span><span class="sxs-lookup"><span data-stu-id="c0dc0-118">In order to create, update, or delete Inbox rules by using the EWS Managed API or EWS, you must remove the Outlook rule, if it exists.</span></span> <span data-ttu-id="c0dc0-119">Si se usa la API administrada de EWS, para ello, al establecer el parámetro **removeOutlookRulesBlob** en **true** en la llamada al método **ExchangeService.UpdateInboxRules** .</span><span class="sxs-lookup"><span data-stu-id="c0dc0-119">If you're using the EWS Managed API, you do this by setting the **removeOutlookRulesBlob** parameter to **true** in the **ExchangeService.UpdateInboxRules** method call.</span></span> <span data-ttu-id="c0dc0-120">Si está usando EWS, establezca el valor del elemento [RemoveOutlookRuleBlob](http://msdn.microsoft.com/library/69614475-8bd3-4475-b988-614fe9cad8ef%28Office.15%29.aspx) en **true** en la operación **UpdateInboxRules** .</span><span class="sxs-lookup"><span data-stu-id="c0dc0-120">If you're using EWS, you set the value of the [RemoveOutlookRuleBlob](http://msdn.microsoft.com/library/69614475-8bd3-4475-b988-614fe9cad8ef%28Office.15%29.aspx) element to **true** in the **UpdateInboxRules** operation.</span></span> <span data-ttu-id="c0dc0-121">Se recomienda que la aplicación debe comprobar la propiedad [RuleCollection.OutlookRuleBlobExists](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.rulecollection.outlookruleblobexists%28v=exchg.80%29.aspx) (si está usando la API administrada de EWS), o el elemento de [OutlookRuleBlobExists](http://msdn.microsoft.com/library/ae1bc448-deb9-4b5b-ab38-4b276abcb650%28Office.15%29.aspx) (si está utilizando EWS) antes de actualizar las reglas de bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="c0dc0-121">We recommend that your application check the [RuleCollection.OutlookRuleBlobExists](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.rulecollection.outlookruleblobexists%28v=exchg.80%29.aspx) property (if you are using the EWS Managed API), or the [OutlookRuleBlobExists](http://msdn.microsoft.com/library/ae1bc448-deb9-4b5b-ab38-4b276abcb650%28Office.15%29.aspx) element (if you're using EWS) before updating Inbox rules.</span></span> <span data-ttu-id="c0dc0-122">Si esta propiedad o este elemento tiene un valor de **true**, la aplicación debe avisar al usuario que cualquier reglas desactivadas se perderán como parte de la actualización y proceda sólo con sus permisos.</span><span class="sxs-lookup"><span data-stu-id="c0dc0-122">If this property or element has a value of **true**, your application should alert the user that any disabled rules will be lost as part of the update, and only proceed with their permission.</span></span>
  
<span data-ttu-id="c0dc0-123">Cuando se llama al método **UpdateInboxRules** , EWS elimina las reglas de envío del cliente.</span><span class="sxs-lookup"><span data-stu-id="c0dc0-123">When you call the **UpdateInboxRules** method, EWS deletes client-side send rules.</span></span> <span data-ttu-id="c0dc0-124">Reglas de envío del cliente se almacenan en el cliente en la regla de mensaje de la carpeta asociada información (FAI) y en ningún otro lugar.</span><span class="sxs-lookup"><span data-stu-id="c0dc0-124">Client-side send rules are stored on the client in the rule Folder Associated Information (FAI) Message and nowhere else.</span></span> <span data-ttu-id="c0dc0-125">EWS elimina esta regla mensaje FAI de forma predeterminada, basándose en la expectativa que Outlook volverá a crearlo.</span><span class="sxs-lookup"><span data-stu-id="c0dc0-125">EWS deletes this rule FAI message by default, based on the expectation that Outlook will recreate it.</span></span> <span data-ttu-id="c0dc0-126">Sin embargo, Outlook no puede volver a crear las reglas que no existen también como una regla extendida, y no existen reglas de envío del cliente como reglas extendidas.</span><span class="sxs-lookup"><span data-stu-id="c0dc0-126">However, Outlook can't recreate rules that don't also exist as an extended rule, and client-side send rules don't exist as extended rules.</span></span> <span data-ttu-id="c0dc0-127">Como resultado, estas reglas se pierden.</span><span class="sxs-lookup"><span data-stu-id="c0dc0-127">As a result, these rules are lost.</span></span> <span data-ttu-id="c0dc0-128">Es recomendable que considere la posibilidad de esto al diseñar la solución.</span><span class="sxs-lookup"><span data-stu-id="c0dc0-128">We suggest you consider this when designing your solution.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c0dc0-129">Los ejemplos de código de API administrada de EWS en este artículo usan un [conjunto común de métodos de utilidad](how-to-manage-inbox-rules-by-using-ews-in-exchange.md#bk_UtilitySource).</span><span class="sxs-lookup"><span data-stu-id="c0dc0-129">The EWS Managed API code examples in this article use a [common set of utility methods](how-to-manage-inbox-rules-by-using-ews-in-exchange.md#bk_UtilitySource).</span></span> <span data-ttu-id="c0dc0-130">Estos métodos se omiten de los ejemplos de código por razones de brevedad.</span><span class="sxs-lookup"><span data-stu-id="c0dc0-130">These methods are omitted from the code samples for brevity.</span></span> 
  
## <a name="get-inbox-rules-by-using-the-ews-managed-api"></a><span data-ttu-id="c0dc0-131">Obtener las reglas de la Bandeja de entrada mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="c0dc0-131">Get Inbox rules by using the EWS Managed API</span></span>
<span data-ttu-id="c0dc0-132"><a name="bk_GetRulesEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="c0dc0-132"></span></span>

<span data-ttu-id="c0dc0-133">Para obtener las reglas de bandeja de entrada actuales, use el método [ExchangeService.GetInboxRules](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.getinboxrules%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="c0dc0-133">To get the current Inbox rules, use the [ExchangeService.GetInboxRules](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.getinboxrules%28v=exchg.80%29.aspx) method.</span></span> <span data-ttu-id="c0dc0-134">Este método devuelve un objeto [RuleCollection](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.rulecollection%28v=exchg.80%29.aspx) que contiene todas las reglas de bandeja de entrada actuales.</span><span class="sxs-lookup"><span data-stu-id="c0dc0-134">This method returns a [RuleCollection](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.rulecollection%28v=exchg.80%29.aspx) object that contains all the current Inbox rules.</span></span> 
  
<span data-ttu-id="c0dc0-135">En este ejemplo, se pasa cada regla de la Bandeja de entrada actual a una función auxiliar ( **ParseRuleDetails** ) para ver los detalles de la regla.</span><span class="sxs-lookup"><span data-stu-id="c0dc0-135">In this example, each rule in the current Inbox is passed to a helper function ( **ParseRuleDetails** ) to display the details of the rule.</span></span> 
  
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

## <a name="get-inbox-rules-by-using-ews"></a><span data-ttu-id="c0dc0-136">Obtener las reglas de la Bandeja de entrada mediante EWS</span><span class="sxs-lookup"><span data-stu-id="c0dc0-136">Get Inbox rules by using EWS</span></span>
<span data-ttu-id="c0dc0-137"><a name="bk_GetRulesEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="c0dc0-137"></span></span>

<span data-ttu-id="c0dc0-138">La siguiente solicitud SOAP de EWS usa la [operación de GetInboxRules](http://msdn.microsoft.com/library/b4b2701a-4a23-4acc-8c75-19f7955ad7ae%28Office.15%29.aspx) para recuperar las reglas de bandeja de entrada para sadie@contoso.com.</span><span class="sxs-lookup"><span data-stu-id="c0dc0-138">The following EWS SOAP request uses the [GetInboxRules operation](http://msdn.microsoft.com/library/b4b2701a-4a23-4acc-8c75-19f7955ad7ae%28Office.15%29.aspx) to retrieve the Inbox rules for sadie@contoso.com.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="c0dc0-139">La siguiente respuesta SOAP de EWS contiene las reglas actuales de la Bandeja de entrada de naiara@contoso.com.</span><span class="sxs-lookup"><span data-stu-id="c0dc0-139">The following EWS SOAP response contains the current Inbox rules for sadie@contoso.com.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
<s:Header>
  <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="712" MinorBuildNumber="22" Version="V2_3" 
      xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
      xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
      xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
      xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
</s:Header>
<s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <GetInboxRulesResponse ResponseClass="Success" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
    <ResponseCode>NoError</ResponseCode>
    <OutlookRuleBlobExists>false</OutlookRuleBlobExists>
    <InboxRules>
      <Rule xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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
      <Rule xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="create-inbox-rules-by-using-the-ews-managed-api"></a><span data-ttu-id="c0dc0-140">Crear las reglas de la Bandeja de entrada mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="c0dc0-140">Create Inbox rules by using the EWS Managed API</span></span>
<span data-ttu-id="c0dc0-141"><a name="bk_CreateRulesEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="c0dc0-141"></span></span>

<span data-ttu-id="c0dc0-142">Para crear una regla, incluir un objeto [CreateRuleOperation](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.createruleoperation%28v=exchg.80%29.aspx) en la colección de objetos [RuleOperation](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.ruleoperation%28v=exchg.80%29.aspx) que se pasan al método [ExchangeService.UpdateInboxRules](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.updateinboxrules%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="c0dc0-142">To create a rule, include a [CreateRuleOperation](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.createruleoperation%28v=exchg.80%29.aspx) object in the collection of [RuleOperation](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.ruleoperation%28v=exchg.80%29.aspx) objects passed to the [ExchangeService.UpdateInboxRules](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.updateinboxrules%28v=exchg.80%29.aspx) method.</span></span> 
  
<span data-ttu-id="c0dc0-143">En este ejemplo, se crea una regla nueva para mover el correo que se ha enviado a una lista de distribución denominada "Ventas" a una subcarpeta de la bandeja de entrada, también denominada "Ventas".</span><span class="sxs-lookup"><span data-stu-id="c0dc0-143">In this example, a new rule is created to move mail sent to a distribution list called "Sales" to a subfolder of the Inbox, also called "Sales".</span></span>
  
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
    if (currentRules != null &amp;&amp; currentRules.OutlookRuleBlobExists)
    {
        Console.WriteLine("WARNING: Adding a new rule will delete the Outlook rule BLOB.");
        Console.WriteLine("This can lead to a loss of any disabled rules.");
        Console.Write("Hit Y to proceed (any other key to cancel): ");
        ConsoleKeyInfo cki = Console.ReadKey();
        if (cki.KeyChar != 'Y' &amp;&amp; cki.KeyChar != 'y')
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

## <a name="create-inbox-rules-by-using-ews"></a><span data-ttu-id="c0dc0-144">Crear las reglas de la Bandeja de entrada mediante EWS</span><span class="sxs-lookup"><span data-stu-id="c0dc0-144">Create Inbox rules by using EWS</span></span>
<span data-ttu-id="c0dc0-145"><a name="bk_CreateRulesEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="c0dc0-145"></span></span>

<span data-ttu-id="c0dc0-146">La siguiente solicitud SOAP de EWS crea la regla "Ventas" en la bandeja de entrada de naiara@contoso.com.</span><span class="sxs-lookup"><span data-stu-id="c0dc0-146">The following EWS SOAP request creates the "Sales" rule in sadie@contoso.com's Inbox.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

## <a name="update-inbox-rules-by-using-the-ews-managed-api"></a><span data-ttu-id="c0dc0-147">Actualizar las reglas de la Bandeja de entrada mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="c0dc0-147">Update Inbox rules by using the EWS Managed API</span></span>
<span data-ttu-id="c0dc0-148"><a name="bk_UpdateRulesEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="c0dc0-148"></span></span>

<span data-ttu-id="c0dc0-149">Para actualizar una regla, incluir un objeto [SetRuleOperation](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.setruleoperation%28v=exchg.80%29.aspx) en la colección de objetos **RuleOperation** que se pasan al método **UpdateInboxRules** .</span><span class="sxs-lookup"><span data-stu-id="c0dc0-149">To update a rule, include a [SetRuleOperation](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.setruleoperation%28v=exchg.80%29.aspx) object in the collection of **RuleOperation** objects passed to the **UpdateInboxRules** method.</span></span> 
  
<span data-ttu-id="c0dc0-p106">En este ejemplo, la regla "Ventas" se actualiza para agregar una excepción. Si el asunto contiene la palabra "Urgente", los mensajes no se moverán a la subcarpeta "Ventas".</span><span class="sxs-lookup"><span data-stu-id="c0dc0-p106">In this example, the "Sales" rule is updated to add an exception. If the subject contains the word "Urgent", the messages will not be moved to the "Sales" subfolder.</span></span>
  
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
    if (currentRules != null &amp;&amp; currentRules.OutlookRuleBlobExists)
    {
        Console.WriteLine("WARNING: Updating an existing rule will delete the Outlook rule BLOB.");
        Console.WriteLine("This can lead to a loss of any disabled rules.");
        Console.Write("Hit Y to proceed (any other key to cancel): ");
        ConsoleKeyInfo cki = Console.ReadKey();
        if (cki.KeyChar != 'Y' &amp;&amp; cki.KeyChar != 'y')
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

## <a name="update-inbox-rules-by-using-ews"></a><span data-ttu-id="c0dc0-152">Actualizar las reglas de la Bandeja de entrada mediante EWS</span><span class="sxs-lookup"><span data-stu-id="c0dc0-152">Update Inbox rules by using EWS</span></span>
<span data-ttu-id="c0dc0-153"><a name="bk_UpdateRulesEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="c0dc0-153"></span></span>

<span data-ttu-id="c0dc0-154">La siguiente solicitud SOAP de EWS actualiza la regla "Ventas" en la bandeja de entrada de naiara@contoso.com.</span><span class="sxs-lookup"><span data-stu-id="c0dc0-154">The following EWS SOAP request updates the "Sales" rule in sadie@contoso.com's Inbox.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

## <a name="delete-inbox-rules-by-using-the-ews-managed-api"></a><span data-ttu-id="c0dc0-155">Eliminar las reglas de la Bandeja de entrada mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="c0dc0-155">Delete Inbox rules by using the EWS Managed API</span></span>
<span data-ttu-id="c0dc0-156"><a name="bk_DeleteRulesEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="c0dc0-156"></span></span>

<span data-ttu-id="c0dc0-157">Para eliminar una regla, incluir un objeto [DeleteRuleOperation](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.deleteruleoperation%28v=exchg.80%29.aspx) en la colección de objetos **RuleOperation** que se pasan al método **UpdateInboxRules** .</span><span class="sxs-lookup"><span data-stu-id="c0dc0-157">To delete a rule, include a [DeleteRuleOperation](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.deleteruleoperation%28v=exchg.80%29.aspx) object in the collection of **RuleOperation** objects passed to the **UpdateInboxRules** method.</span></span> 
  
<span data-ttu-id="c0dc0-158">En este ejemplo, la regla "Ventas" se elimina.</span><span class="sxs-lookup"><span data-stu-id="c0dc0-158">In this example, the "Sales" rule is deleted.</span></span>
  
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
    if (currentRules != null &amp;&amp; currentRules.OutlookRuleBlobExists)
    {
        Console.WriteLine("WARNING: Deleting a rule will delete the Outlook rule BLOB.");
        Console.WriteLine("This can lead to a loss of any disabled rules.");
        Console.Write("Hit Y to proceed (any other key to cancel): ");
        ConsoleKeyInfo cki = Console.ReadKey();
        if (cki.KeyChar != 'Y' &amp;&amp; cki.KeyChar != 'y')
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

## <a name="delete-inbox-rules-by-using-ews"></a><span data-ttu-id="c0dc0-159">Eliminar las reglas de la Bandeja de entrada mediante EWS</span><span class="sxs-lookup"><span data-stu-id="c0dc0-159">Delete Inbox rules by using EWS</span></span>
<span data-ttu-id="c0dc0-160"><a name="bk_DeleteRulesEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="c0dc0-160"></span></span>

<span data-ttu-id="c0dc0-161">La siguiente solicitud SOAP de EWS elimina la regla "Ventas" en la bandeja de entrada de naiara@contoso.com.</span><span class="sxs-lookup"><span data-stu-id="c0dc0-161">The following EWS SOAP request deletes the "Sales" rules from sadie@contoso.com's inbox.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

## <a name="source-for-sample-utility-methods"></a><span data-ttu-id="c0dc0-162">Origen de los métodos de utilidad de ejemplo</span><span class="sxs-lookup"><span data-stu-id="c0dc0-162">Source for sample utility methods</span></span>
<span data-ttu-id="c0dc0-163"><a name="bk_UtilitySource"> </a></span><span class="sxs-lookup"><span data-stu-id="c0dc0-163"></span></span>

<span data-ttu-id="c0dc0-164">Los ejemplos de la API administrada de EWS de este artículo usan los métodos de utilidad que están incluidos en el siguiente ejemplo.</span><span class="sxs-lookup"><span data-stu-id="c0dc0-164">The EWS Managed API examples in this article use the utility methods included in the following example.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="c0dc0-165">Vea también</span><span class="sxs-lookup"><span data-stu-id="c0dc0-165">See also</span></span>


- [<span data-ttu-id="c0dc0-166">Administración de la Bandeja de entrada y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="c0dc0-166">Inbox management and EWS in Exchange</span></span>](inbox-management-and-ews-in-exchange.md)
    
- [<span data-ttu-id="c0dc0-167">ExchangeService.GetInboxRules (método)</span><span class="sxs-lookup"><span data-stu-id="c0dc0-167">ExchangeService.GetInboxRules method</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.getinboxrules%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="c0dc0-168">ExchangeService.UpdateInboxRules (método)</span><span class="sxs-lookup"><span data-stu-id="c0dc0-168">ExchangeService.UpdateInboxRules method</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.updateinboxrules%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="c0dc0-169">Operación de GetInboxRules</span><span class="sxs-lookup"><span data-stu-id="c0dc0-169">GetInboxRules operation</span></span>](http://msdn.microsoft.com/library/b4b2701a-4a23-4acc-8c75-19f7955ad7ae%28Office.15%29.aspx)
    
- [<span data-ttu-id="c0dc0-170">Operación de UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="c0dc0-170">UpdateInboxRules operation</span></span>](http://msdn.microsoft.com/library/f982a237-471e-45c5-a2b5-468cfc53150b%28Office.15%29.aspx)
    

