---
title: Operación GetMailTips
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetMailTips
api_type:
- schema
ms.assetid: 025483ec-a9f3-4735-8a95-d26e30ea7974
description: La operación GetMailTips obtiene la información de sugerencias de correo para el buzón especificado.
ms.openlocfilehash: 41a4bb99ee7ae4e416ec8a106968bb7869e60345
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458659"
---
# <a name="getmailtips-operation"></a><span data-ttu-id="15f95-103">Operación GetMailTips</span><span class="sxs-lookup"><span data-stu-id="15f95-103">GetMailTips operation</span></span>

<span data-ttu-id="15f95-104">La operación **GetMailTips** obtiene la información de sugerencias de correo para el buzón especificado.</span><span class="sxs-lookup"><span data-stu-id="15f95-104">The **GetMailTips** operation gets the mail tips information for the specified mailbox.</span></span> 
  
## <a name="getmailtips-request-example"></a><span data-ttu-id="15f95-105">Ejemplo de solicitud GetMailTips</span><span class="sxs-lookup"><span data-stu-id="15f95-105">GetMailTips request example</span></span>

### <a name="description"></a><span data-ttu-id="15f95-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="15f95-106">Description</span></span>

<span data-ttu-id="15f95-107">El cliente crea el XML de la solicitud y lo envía al servidor.</span><span class="sxs-lookup"><span data-stu-id="15f95-107">The client constructs the request XML and sends it to the server.</span></span> <span data-ttu-id="15f95-108">La solicitud identifica quién envía el cliente como, el buzón para el que se recuperan las sugerencias de correo y qué sugerencias de correo se solicitan.</span><span class="sxs-lookup"><span data-stu-id="15f95-108">The request identifies who the client is sending as, the mailbox to retrieve the mail tips for, and what mail tips are requested.</span></span> <span data-ttu-id="15f95-109">En este ejemplo, el cliente solicita que se devuelvan todas las sugerencias de correo para el buzón seleccionado.</span><span class="sxs-lookup"><span data-stu-id="15f95-109">In this example, the client requests that all mail tips be returned for the selected mailbox.</span></span>
  
### <a name="code"></a><span data-ttu-id="15f95-110">Código</span><span class="sxs-lookup"><span data-stu-id="15f95-110">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
        xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"> 
  <soap:Header> 
    <t:RequestServerVersion Version="Exchange2010" /> 
  </soap:Header> 
  <soap:Body> 
    <GetMailTips xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"> 
      <SendingAs> 
        <t:EmailAddress> user1@contoso.com </t:EmailAddress> 
        <t:RoutingType>SMTP</t:RoutingType> 
      </SendingAs> 
      <Recipients> 
        <t:Mailbox> 
          <t:EmailAddress> user2@contoso.com </t:EmailAddress> 
          <t:RoutingType>SMTP</t:RoutingType> 
        </t:Mailbox> 
      </Recipients> 
      <MailTipsRequested>All</MailTipsRequested> 
    </GetMailTips> 
  </soap:Body> 
</soap:Envelope>
```

### <a name="request-elements"></a><span data-ttu-id="15f95-111">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="15f95-111">Request elements</span></span>

<span data-ttu-id="15f95-112">Los siguientes elementos se incluyen en la solicitud:</span><span class="sxs-lookup"><span data-stu-id="15f95-112">The following elements are included in the request:</span></span>
  
- [<span data-ttu-id="15f95-113">GetMailTips</span><span class="sxs-lookup"><span data-stu-id="15f95-113">GetMailTips</span></span>](getmailtips.md)
    
- [<span data-ttu-id="15f95-114">Envíoas</span><span class="sxs-lookup"><span data-stu-id="15f95-114">SendingAs</span></span>](sendingas.md)
    
- [<span data-ttu-id="15f95-115">Recipients (ArrayOfRecipientsType)</span><span class="sxs-lookup"><span data-stu-id="15f95-115">Recipients (ArrayOfRecipientsType)</span></span>](recipients-arrayofrecipientstype.md)
    
- [<span data-ttu-id="15f95-116">MailTipsRequested</span><span class="sxs-lookup"><span data-stu-id="15f95-116">MailTipsRequested</span></span>](mailtipsrequested.md)
    
## <a name="successful-getmailtips-response-example"></a><span data-ttu-id="15f95-117">Ejemplo de respuesta GetMailTips correcta</span><span class="sxs-lookup"><span data-stu-id="15f95-117">Successful GetMailTips response example</span></span>

### <a name="description"></a><span data-ttu-id="15f95-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="15f95-118">Description</span></span>

<span data-ttu-id="15f95-119">El siguiente ejemplo del cuerpo del Protocolo simple de acceso a objetos (SOAP) muestra una respuesta correcta a la solicitud **GetMailTips** .</span><span class="sxs-lookup"><span data-stu-id="15f95-119">The following Simple Object Access Protocol (SOAP) body example shows a successful response to the **GetMailTips** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="15f95-120">Código</span><span class="sxs-lookup"><span data-stu-id="15f95-120">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?> 
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/"> 
  <s:Header> 
    <h:ServerVersionInfo MajorVersion="14" MinorVersion="0" MajorBuildNumber="536" MinorBuildNumber="0" Version="Exchange2010" 
xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
xmlns:xsd="http://www.w3.org/2001/XMLSchema"/> 
  </s:Header> 
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema"> 
    <GetMailTipsResponse ResponseClass="Success" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"> 
      <ResponseCode>NoError</ResponseCode> 
      <ResponseMessages> 
        <MailTipsResponseMessageType ResponseClass="Success"> 
        <ResponseCode>NoError</ResponseCode> 
        <m:MailTips xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"> 20 / 29 [MS-OXWMT] — v20100517 Mail Tips Web Service Extensions Copyright © 2010 Microsoft Corporation. Release: Monday, May 17, 2010 
          <t:RecipientAddress xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"> 
          <t:Name/> 
          <t:EmailAddress>user2@contoso.com</t:EmailAddress> 
          <t:RoutingType>SMTP</t:RoutingType> 
          </t:RecipientAddress> 
          <t:PendingMailTips xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"/> 
          <t:OutOfOffice xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"> 
            <t:ReplyBody> 
              <t:Message/> 
            </t:ReplyBody> 
          </t:OutOfOffice> 
          <t:MailboxFull xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">false</t:MailboxFull> 
          <t:CustomMailTip xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">Hello World Mailtips</t:CustomMailTip> 
          <t:TotalMemberCount xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">1</t:TotalMemberCount> 
          <t:ExternalMemberCount xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">0</t:ExternalMemberCount> 
          <t:MaxMessageSize xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">10485760</t:MaxMessageSize> 
          <t:DeliveryRestricted xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">false</t:DeliveryRestricted> 
          <t:IsModerated xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">false</t:IsModerated> 
          <t:InvalidRecipient xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">false</t:InvalidRecipient> 
        </m:MailTips> 
        </MailTipsResponseMessageType> 
      </ResponseMessages> 
    </GetMailTipsResponse> 
  </s:Body> 
</s:Envelope>
```

### <a name="response-elements"></a><span data-ttu-id="15f95-121">Elementos de respuesta</span><span class="sxs-lookup"><span data-stu-id="15f95-121">Response elements</span></span>

<span data-ttu-id="15f95-122">En la respuesta se incluyen los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="15f95-122">The following elements are included in the response:</span></span>
  
- [<span data-ttu-id="15f95-123">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="15f95-123">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="15f95-124">Sugerencias de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="15f95-124">MailTips</span></span>](mailtips.md)
    
## <a name="see-also"></a><span data-ttu-id="15f95-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="15f95-125">See also</span></span>



[<span data-ttu-id="15f95-126">Operaciones de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="15f95-126">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
  
- [<span data-ttu-id="15f95-127">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="15f95-127">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

