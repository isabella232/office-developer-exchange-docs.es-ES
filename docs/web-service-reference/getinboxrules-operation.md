---
title: Operación GetInboxRules
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
description: La operación GetInboxRules usa servicios Web de Exchange para recuperar las reglas de bandeja de entrada en el buzón del usuario identificado.
ms.openlocfilehash: f8a5068b1f189cc6fd5feef6dfec29204a0b8887
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764872"
---
# <a name="getinboxrules-operation"></a><span data-ttu-id="89abe-103">Operación GetInboxRules</span><span class="sxs-lookup"><span data-stu-id="89abe-103">GetInboxRules operation</span></span>

<span data-ttu-id="89abe-104">La operación **GetInboxRules** usa servicios Web de Exchange para recuperar las reglas de bandeja de entrada en el buzón del usuario identificado.</span><span class="sxs-lookup"><span data-stu-id="89abe-104">The **GetInboxRules** operation uses Exchange Web Services to retrieve Inbox rules in the identified user's mailbox.</span></span> 
  
## <a name="getinboxrules-request-example"></a><span data-ttu-id="89abe-105">Ejemplo de solicitud de GetInboxRules</span><span class="sxs-lookup"><span data-stu-id="89abe-105">GetInboxRules request example</span></span>

### <a name="description"></a><span data-ttu-id="89abe-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="89abe-106">Description</span></span>

<span data-ttu-id="89abe-107">En el ejemplo siguiente se muestra la solicitud XML que el cliente envía al servidor.</span><span class="sxs-lookup"><span data-stu-id="89abe-107">The following example shows the request XML that the client sends to the server.</span></span> <span data-ttu-id="89abe-108">La solicitud identifica al usuario en el elemento [MailboxSmtpAddress](mailboxsmtpaddress.md) .</span><span class="sxs-lookup"><span data-stu-id="89abe-108">The request identifies the user in the [MailboxSmtpAddress](mailboxsmtpaddress.md) element.</span></span> <span data-ttu-id="89abe-109">Todas las reglas de bandeja de entrada para el usuario identificado están que se devuelve en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="89abe-109">All Inbox rules for the identified user are to be returned in the response.</span></span> 
  
### <a name="code"></a><span data-ttu-id="89abe-110">Código</span><span class="sxs-lookup"><span data-stu-id="89abe-110">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
        xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
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

### <a name="request-elements"></a><span data-ttu-id="89abe-111">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="89abe-111">Request elements</span></span>

<span data-ttu-id="89abe-112">La solicitud incluye el elemento opcional siguiente:</span><span class="sxs-lookup"><span data-stu-id="89abe-112">The request includes the following optional element:</span></span>
  
- [<span data-ttu-id="89abe-113">MailboxSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="89abe-113">MailboxSmtpAddress</span></span>](mailboxsmtpaddress.md)
    
## <a name="successful-getinboxrules-response-example"></a><span data-ttu-id="89abe-114">Ejemplo de respuesta correcta de GetInboxRules</span><span class="sxs-lookup"><span data-stu-id="89abe-114">Successful GetInboxRules response example</span></span>

### <a name="description"></a><span data-ttu-id="89abe-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="89abe-115">Description</span></span>

<span data-ttu-id="89abe-116">El siguiente ejemplo de cuerpo de SOAP Simple Object Access Protocol () muestra una respuesta correcta a la solicitud de **GetInboxRules** .</span><span class="sxs-lookup"><span data-stu-id="89abe-116">The following Simple Object Access Protocol (SOAP) body example shows a successful response to the **GetInboxRules** request.</span></span> <span data-ttu-id="89abe-117">En este ejemplo, la respuesta incluye una regla.</span><span class="sxs-lookup"><span data-stu-id="89abe-117">In this example, the response includes one rule.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="89abe-118">Los valores del **identificador** y los atributos **ChangeKey** del elemento [FolderId](folderid.md) se han abreviado para conservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="89abe-118">The values of the **Id** and the **ChangeKey** attributes of the [FolderId](folderid.md) element have been shortened to preserve readability.</span></span> 
  
### <a name="code"></a><span data-ttu-id="89abe-119">Código</span><span class="sxs-lookup"><span data-stu-id="89abe-119">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14"
        MinorVersion="1" MajorBuildNumber="139"
        MinorBuildNumber="0"
        Version="Exchange2010_SP1"
        xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
        xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
        xmlns:xsd="http://www.w3.org/2001/XMLSchema" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
        xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetInboxRulesResponse ResponseClass="Success"
        xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <OutlookRuleBlobExists>true</OutlookRuleBlobExists>
      <InboxRules>
        <Rule xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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

### <a name="response-elements"></a><span data-ttu-id="89abe-120">Elementos de respuesta</span><span class="sxs-lookup"><span data-stu-id="89abe-120">Response elements</span></span>

<span data-ttu-id="89abe-121">En la respuesta se incluyen los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="89abe-121">The following elements are included in the response:</span></span>
  
- [<span data-ttu-id="89abe-122">GetInboxRulesResponse</span><span class="sxs-lookup"><span data-stu-id="89abe-122">GetInboxRulesResponse</span></span>](getinboxrulesresponse.md)
    
- [<span data-ttu-id="89abe-123">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="89abe-123">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="89abe-124">OutlookRuleBlobExists</span><span class="sxs-lookup"><span data-stu-id="89abe-124">OutlookRuleBlobExists</span></span>](outlookruleblobexists.md)
    
- [<span data-ttu-id="89abe-125">InboxRules</span><span class="sxs-lookup"><span data-stu-id="89abe-125">InboxRules</span></span>](inboxrules.md)
    
## <a name="see-also"></a><span data-ttu-id="89abe-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="89abe-126">See also</span></span>



[<span data-ttu-id="89abe-127">Operación de UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="89abe-127">UpdateInboxRules operation</span></span>](updateinboxrules-operation.md)

