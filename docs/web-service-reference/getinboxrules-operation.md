---
title: Operación de GetInboxRules
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetInboxRules
api_type:
- schema
ms.assetid: b4b2701a-4a23-4acc-8c75-19f7955ad7ae
description: La operación GetInboxRules usa los servicios web Exchange para recuperar las reglas de la bandeja de entrada en el buzón del usuario identificado.
ms.openlocfilehash: f4c4c03f55c9f32be4a067024f4387888edd5fe9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457938"
---
# <a name="getinboxrules-operation"></a><span data-ttu-id="14fba-103">Operación de GetInboxRules</span><span class="sxs-lookup"><span data-stu-id="14fba-103">GetInboxRules operation</span></span>

<span data-ttu-id="14fba-104">La operación **GetInboxRules** usa los servicios web Exchange para recuperar las reglas de la bandeja de entrada en el buzón del usuario identificado.</span><span class="sxs-lookup"><span data-stu-id="14fba-104">The **GetInboxRules** operation uses Exchange Web Services to retrieve Inbox rules in the identified user's mailbox.</span></span> 
  
## <a name="getinboxrules-request-example"></a><span data-ttu-id="14fba-105">Ejemplo de solicitud GetInboxRules</span><span class="sxs-lookup"><span data-stu-id="14fba-105">GetInboxRules request example</span></span>

### <a name="description"></a><span data-ttu-id="14fba-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="14fba-106">Description</span></span>

<span data-ttu-id="14fba-107">En el ejemplo siguiente se muestra el XML de la solicitud que el cliente envía al servidor.</span><span class="sxs-lookup"><span data-stu-id="14fba-107">The following example shows the request XML that the client sends to the server.</span></span> <span data-ttu-id="14fba-108">La solicitud identifica al usuario en el elemento [MailboxSmtpAddress](mailboxsmtpaddress.md) .</span><span class="sxs-lookup"><span data-stu-id="14fba-108">The request identifies the user in the [MailboxSmtpAddress](mailboxsmtpaddress.md) element.</span></span> <span data-ttu-id="14fba-109">Todas las reglas de la bandeja de entrada para el usuario identificado deben devolverse en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="14fba-109">All Inbox rules for the identified user are to be returned in the response.</span></span> 
  
### <a name="code"></a><span data-ttu-id="14fba-110">Código</span><span class="sxs-lookup"><span data-stu-id="14fba-110">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
        xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
        xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010_SP1" />
  </soap:Header>
  <soap:Body>
    <m:GetInboxRules>
      <m:MailboxSmtpAddress>User1@Contoso.com</m:MailboxSmtpAddress>
    </m:GetInboxRules>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a><span data-ttu-id="14fba-111">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="14fba-111">Request elements</span></span>

<span data-ttu-id="14fba-112">La solicitud incluye el siguiente elemento opcional:</span><span class="sxs-lookup"><span data-stu-id="14fba-112">The request includes the following optional element:</span></span>
  
- [<span data-ttu-id="14fba-113">MailboxSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="14fba-113">MailboxSmtpAddress</span></span>](mailboxsmtpaddress.md)
    
## <a name="successful-getinboxrules-response-example"></a><span data-ttu-id="14fba-114">Ejemplo de respuesta GetInboxRules correcta</span><span class="sxs-lookup"><span data-stu-id="14fba-114">Successful GetInboxRules response example</span></span>

### <a name="description"></a><span data-ttu-id="14fba-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="14fba-115">Description</span></span>

<span data-ttu-id="14fba-116">El siguiente ejemplo del cuerpo del Protocolo simple de acceso a objetos (SOAP) muestra una respuesta correcta a la solicitud **GetInboxRules** .</span><span class="sxs-lookup"><span data-stu-id="14fba-116">The following Simple Object Access Protocol (SOAP) body example shows a successful response to the **GetInboxRules** request.</span></span> <span data-ttu-id="14fba-117">En este ejemplo, la respuesta incluye una regla.</span><span class="sxs-lookup"><span data-stu-id="14fba-117">In this example, the response includes one rule.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="14fba-118">Los valores de los atributos **ID** y **changekey** del elemento [FolderId](folderid.md) se han abreviado para preservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="14fba-118">The values of the **Id** and the **ChangeKey** attributes of the [FolderId](folderid.md) element have been shortened to preserve readability.</span></span> 
  
### <a name="code"></a><span data-ttu-id="14fba-119">Código</span><span class="sxs-lookup"><span data-stu-id="14fba-119">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14"
        MinorVersion="1" MajorBuildNumber="139"
        MinorBuildNumber="0"
        Version="Exchange2010_SP1"
        xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
        xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
        xmlns:xsd="http://www.w3.org/2001/XMLSchema" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
        xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetInboxRulesResponse ResponseClass="Success"
        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <OutlookRuleBlobExists>true</OutlookRuleBlobExists>
      <InboxRules>
        <Rule xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <RuleId>dCsAAABjzvA=</RuleId>
          <DisplayName>MoveInterestingToJunk</DisplayName>
          <Priority>1</Priority>
          <IsEnabled>true</IsEnabled>
          <Conditions>
            <ContainsSubjectStrings>
              <String>Interesting</String>
            </ContainsSubjectStrings>
          </Conditions>
          <Actions>
            <MoveToFolder>
              <FolderId ChangeKey="AQAAAA==" Id="AAMkAGYzZjZm" />
            </MoveToFolder>
          </Actions>
        </Rule>
      </InboxRules>
    </GetInboxRulesResponse>
  </s:Body>
</s:Envelope>
```

### <a name="response-elements"></a><span data-ttu-id="14fba-120">Elementos de respuesta</span><span class="sxs-lookup"><span data-stu-id="14fba-120">Response elements</span></span>

<span data-ttu-id="14fba-121">En la respuesta se incluyen los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="14fba-121">The following elements are included in the response:</span></span>
  
- [<span data-ttu-id="14fba-122">GetInboxRulesResponse</span><span class="sxs-lookup"><span data-stu-id="14fba-122">GetInboxRulesResponse</span></span>](getinboxrulesresponse.md)
    
- [<span data-ttu-id="14fba-123">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="14fba-123">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="14fba-124">OutlookRuleBlobExists</span><span class="sxs-lookup"><span data-stu-id="14fba-124">OutlookRuleBlobExists</span></span>](outlookruleblobexists.md)
    
- [<span data-ttu-id="14fba-125">InboxRules</span><span class="sxs-lookup"><span data-stu-id="14fba-125">InboxRules</span></span>](inboxrules.md)
    
## <a name="see-also"></a><span data-ttu-id="14fba-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="14fba-126">See also</span></span>



[<span data-ttu-id="14fba-127">Operación de UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="14fba-127">UpdateInboxRules operation</span></span>](updateinboxrules-operation.md)

