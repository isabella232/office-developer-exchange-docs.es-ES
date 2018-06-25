---
title: Operación GetPasswordExpirationDate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b0297458-58fb-4e5d-bb47-0cd17155e106
description: La operación GetPasswordExpirationDate proporciona la fecha de caducidad de contraseña de cuenta de correo electrónico para el usuario actual.
ms.openlocfilehash: c57942c88b09a910e2d529a12ea279bb2da5d693
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764932"
---
# <a name="getpasswordexpirationdate-operation"></a><span data-ttu-id="ce4dc-103">Operación GetPasswordExpirationDate</span><span class="sxs-lookup"><span data-stu-id="ce4dc-103">GetPasswordExpirationDate operation</span></span>

<span data-ttu-id="ce4dc-104">La operación **GetPasswordExpirationDate** proporciona la fecha de caducidad de contraseña de cuenta de correo electrónico para el usuario actual.</span><span class="sxs-lookup"><span data-stu-id="ce4dc-104">The **GetPasswordExpirationDate** operation provides the email account password expiration date for the current user.</span></span> 
  
<span data-ttu-id="ce4dc-105">Esta operación se introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="ce4dc-105">This operation was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="getpasswordexpirationdate-operation-soap-headers"></a><span data-ttu-id="ce4dc-106">Encabezados SOAP de operación de GetPasswordExpirationDate</span><span class="sxs-lookup"><span data-stu-id="ce4dc-106">GetPasswordExpirationDate operation SOAP headers</span></span>

<span data-ttu-id="ce4dc-107">La operación de **GetPasswordExpirationDate** puede utilizar los encabezados SOAP que se enumeran en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="ce4dc-107">The **GetPasswordExpirationDate** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="ce4dc-108">**Header**</span><span class="sxs-lookup"><span data-stu-id="ce4dc-108">**Header**</span></span>|<span data-ttu-id="ce4dc-109">**Element**</span><span class="sxs-lookup"><span data-stu-id="ce4dc-109">**Element**</span></span>|<span data-ttu-id="ce4dc-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ce4dc-110">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ce4dc-111">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="ce4dc-111">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="ce4dc-112">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="ce4dc-112">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="ce4dc-113">Identifica la referencia cultural, como se define en RFC 3066, "Etiquetas para la identificación de idiomas," que se utilizará para acceder al buzón.</span><span class="sxs-lookup"><span data-stu-id="ce4dc-113">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="ce4dc-114">Esto es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="ce4dc-114">This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="ce4dc-115">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="ce4dc-115">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="ce4dc-116">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="ce4dc-116">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="ce4dc-117">Identifica el esquema de la solicitud de la operación.</span><span class="sxs-lookup"><span data-stu-id="ce4dc-117">Identifies the schema for the operation request.</span></span> <span data-ttu-id="ce4dc-118">Esto es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="ce4dc-118">This is applicable to a request.</span></span> <span data-ttu-id="ce4dc-119">Esto es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="ce4dc-119">This is applicable to a request.</span></span>  <br/> |
   
## <a name="getpasswordexpirationdate-operation-request-example"></a><span data-ttu-id="ce4dc-120">Ejemplo de solicitud de operación de GetPasswordExpirationDate</span><span class="sxs-lookup"><span data-stu-id="ce4dc-120">GetPasswordExpirationDate operation request example</span></span>

### <a name="description"></a><span data-ttu-id="ce4dc-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="ce4dc-121">Description</span></span>

<span data-ttu-id="ce4dc-122">El siguiente ejemplo de una solicitud de operación **GetPasswordExpirationDate** muestra cómo obtener la fecha de caducidad de contraseña para una cuenta de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="ce4dc-122">The following example of a **GetPasswordExpirationDate** operation request shows how to get the password expiration date for an email account.</span></span> 
  
### <a name="code"></a><span data-ttu-id="ce4dc-123">Código</span><span class="sxs-lookup"><span data-stu-id="ce4dc-123">Code</span></span>

```XML
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
  </soap:Header>
  <soap:Body>
    <tns:GetPasswordExpirationDate>
      <tns:MailboxSmtpAddress>user1@DTZMZX-dom.extest.microsoft.com</tns:MailboxSmtpAddress>
    </tns:GetPasswordExpirationDate>
  </soap:Body>
</soap:Envelope>

```

### <a name="request-elements"></a><span data-ttu-id="ce4dc-124">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="ce4dc-124">Request elements</span></span>

<span data-ttu-id="ce4dc-125">En la solicitud se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="ce4dc-125">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="ce4dc-126">GetPasswordExpirationDate</span><span class="sxs-lookup"><span data-stu-id="ce4dc-126">GetPasswordExpirationDate</span></span>](getpasswordexpirationdate.md)
    
- [<span data-ttu-id="ce4dc-127">MailboxSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="ce4dc-127">MailboxSmtpAddress</span></span>](mailboxsmtpaddress.md)
    
## <a name="successful-getpasswordexpirationdate-operation-response"></a><span data-ttu-id="ce4dc-128">Respuesta es correcta de operación GetPasswordExpirationDate</span><span class="sxs-lookup"><span data-stu-id="ce4dc-128">Successful GetPasswordExpirationDate operation response</span></span>

<span data-ttu-id="ce4dc-129">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="ce4dc-129">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="ce4dc-130">GetPasswordExpirationDateResponse</span><span class="sxs-lookup"><span data-stu-id="ce4dc-130">GetPasswordExpirationDateResponse</span></span>](getpasswordexpirationdateresponse.md)
    
- [<span data-ttu-id="ce4dc-131">PasswordExpirationDate</span><span class="sxs-lookup"><span data-stu-id="ce4dc-131">PasswordExpirationDate</span></span>](passwordexpirationdate.md)
    

