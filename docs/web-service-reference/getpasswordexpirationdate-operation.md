---
title: Operación GetPasswordExpirationDate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b0297458-58fb-4e5d-bb47-0cd17155e106
description: La operación GetPasswordExpirationDate proporciona la fecha de expiración de la contraseña de la cuenta de correo electrónico para el usuario actual.
ms.openlocfilehash: 4184092cf98161e4c2f74446cef5439722ae71a1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457896"
---
# <a name="getpasswordexpirationdate-operation"></a><span data-ttu-id="017e5-103">Operación GetPasswordExpirationDate</span><span class="sxs-lookup"><span data-stu-id="017e5-103">GetPasswordExpirationDate operation</span></span>

<span data-ttu-id="017e5-104">La operación **GetPasswordExpirationDate** proporciona la fecha de expiración de la contraseña de la cuenta de correo electrónico para el usuario actual.</span><span class="sxs-lookup"><span data-stu-id="017e5-104">The **GetPasswordExpirationDate** operation provides the email account password expiration date for the current user.</span></span> 
  
<span data-ttu-id="017e5-105">Esta operación se introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="017e5-105">This operation was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="getpasswordexpirationdate-operation-soap-headers"></a><span data-ttu-id="017e5-106">Encabezados SOAP de operación GetPasswordExpirationDate</span><span class="sxs-lookup"><span data-stu-id="017e5-106">GetPasswordExpirationDate operation SOAP headers</span></span>

<span data-ttu-id="017e5-107">La operación **GetPasswordExpirationDate** puede usar los encabezados SOAP que se enumeran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="017e5-107">The **GetPasswordExpirationDate** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="017e5-108">**Header**</span><span class="sxs-lookup"><span data-stu-id="017e5-108">**Header**</span></span>|<span data-ttu-id="017e5-109">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="017e5-109">**Element**</span></span>|<span data-ttu-id="017e5-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="017e5-110">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="017e5-111">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="017e5-111">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="017e5-112">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="017e5-112">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="017e5-113">Identifica la referencia cultural, tal y como se define en RFC 3066, "etiquetas para la identificación de idiomas", que se va a usar para obtener acceso al buzón.</span><span class="sxs-lookup"><span data-stu-id="017e5-113">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="017e5-114">Esto es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="017e5-114">This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="017e5-115">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="017e5-115">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="017e5-116">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="017e5-116">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="017e5-117">Identifica el esquema de la solicitud de operación.</span><span class="sxs-lookup"><span data-stu-id="017e5-117">Identifies the schema for the operation request.</span></span> <span data-ttu-id="017e5-118">Esto es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="017e5-118">This is applicable to a request.</span></span> <span data-ttu-id="017e5-119">Esto es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="017e5-119">This is applicable to a request.</span></span>  <br/> |
   
## <a name="getpasswordexpirationdate-operation-request-example"></a><span data-ttu-id="017e5-120">Ejemplo de solicitud de operación GetPasswordExpirationDate</span><span class="sxs-lookup"><span data-stu-id="017e5-120">GetPasswordExpirationDate operation request example</span></span>

### <a name="description"></a><span data-ttu-id="017e5-121">Description</span><span class="sxs-lookup"><span data-stu-id="017e5-121">Description</span></span>

<span data-ttu-id="017e5-122">El siguiente ejemplo de una solicitud de operación de **GetPasswordExpirationDate** muestra cómo obtener la fecha de expiración de la contraseña de una cuenta de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="017e5-122">The following example of a **GetPasswordExpirationDate** operation request shows how to get the password expiration date for an email account.</span></span> 
  
### <a name="code"></a><span data-ttu-id="017e5-123">Código</span><span class="sxs-lookup"><span data-stu-id="017e5-123">Code</span></span>

```XML
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
  </soap:Header>
  <soap:Body>
    <tns:GetPasswordExpirationDate>
      <tns:MailboxSmtpAddress>user1@DTZMZX-dom.extest.microsoft.com</tns:MailboxSmtpAddress>
    </tns:GetPasswordExpirationDate>
  </soap:Body>
</soap:Envelope>

```

### <a name="request-elements"></a><span data-ttu-id="017e5-124">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="017e5-124">Request elements</span></span>

<span data-ttu-id="017e5-125">Los siguientes elementos se usan en la solicitud:</span><span class="sxs-lookup"><span data-stu-id="017e5-125">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="017e5-126">GetPasswordExpirationDate</span><span class="sxs-lookup"><span data-stu-id="017e5-126">GetPasswordExpirationDate</span></span>](getpasswordexpirationdate.md)
    
- [<span data-ttu-id="017e5-127">MailboxSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="017e5-127">MailboxSmtpAddress</span></span>](mailboxsmtpaddress.md)
    
## <a name="successful-getpasswordexpirationdate-operation-response"></a><span data-ttu-id="017e5-128">Respuesta de operación GetPasswordExpirationDate correcta</span><span class="sxs-lookup"><span data-stu-id="017e5-128">Successful GetPasswordExpirationDate operation response</span></span>

<span data-ttu-id="017e5-129">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="017e5-129">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="017e5-130">GetPasswordExpirationDateResponse</span><span class="sxs-lookup"><span data-stu-id="017e5-130">GetPasswordExpirationDateResponse</span></span>](getpasswordexpirationdateresponse.md)
    
- [<span data-ttu-id="017e5-131">PasswordExpirationDate</span><span class="sxs-lookup"><span data-stu-id="017e5-131">PasswordExpirationDate</span></span>](passwordexpirationdate.md)
    

