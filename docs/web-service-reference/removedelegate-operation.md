---
title: Operación RemoveDelegate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RemoveDelegate
api_type:
- schema
ms.assetid: 1d42d5ff-8fde-4f8a-b18d-57b1ef7a946a
description: La operación RemoveDelegate quita a uno o varios delegados de buzón de un usuario.
ms.openlocfilehash: 6f3371d19bd8a7fd967d4959d85037ae6b51f6aa
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837088"
---
# <a name="removedelegate-operation"></a><span data-ttu-id="2765a-103">Operación RemoveDelegate</span><span class="sxs-lookup"><span data-stu-id="2765a-103">RemoveDelegate operation</span></span>

<span data-ttu-id="2765a-104">La operación **RemoveDelegate** quita a uno o varios delegados de buzón de un usuario.</span><span class="sxs-lookup"><span data-stu-id="2765a-104">The **RemoveDelegate** operation removes one or more delegates from a user's mailbox.</span></span> 
  
## <a name="soap-headers"></a><span data-ttu-id="2765a-105">Encabezados SOAP</span><span class="sxs-lookup"><span data-stu-id="2765a-105">SOAP Headers</span></span>

<span data-ttu-id="2765a-106">La operación de **RemoveDelegate** puede utilizar los encabezados SOAP que se enumeran y describen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="2765a-106">The **RemoveDelegate** operation can use the SOAP headers that are listed and described in the following table.</span></span> 
  
|<span data-ttu-id="2765a-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="2765a-107">**Header**</span></span>|<span data-ttu-id="2765a-108">**Element**</span><span class="sxs-lookup"><span data-stu-id="2765a-108">**Element**</span></span>|<span data-ttu-id="2765a-109">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2765a-109">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2765a-110">Suplantación</span><span class="sxs-lookup"><span data-stu-id="2765a-110">Impersonation</span></span>  <br/> |[<span data-ttu-id="2765a-111">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="2765a-111">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="2765a-112">Identifica el usuario que está realizando la suplantación de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="2765a-112">Identifies the user whom the client application is impersonating.</span></span>  <br/> |
|<span data-ttu-id="2765a-113">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="2765a-113">MailboxCulture</span></span>  <br/> |[<span data-ttu-id="2765a-114">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="2765a-114">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="2765a-115">Identifica la referencia cultural de RFC3066 va a usar para tener acceso al buzón.</span><span class="sxs-lookup"><span data-stu-id="2765a-115">Identifies the RFC3066 culture to be used to access the mailbox.</span></span>  <br/> |
|<span data-ttu-id="2765a-116">RequestVersion</span><span class="sxs-lookup"><span data-stu-id="2765a-116">RequestVersion</span></span>  <br/> |[<span data-ttu-id="2765a-117">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="2765a-117">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="2765a-118">Identifica la versión del esquema para la solicitud de la operación.</span><span class="sxs-lookup"><span data-stu-id="2765a-118">Identifies the schema version for the operation request.</span></span>  <br/> |
|<span data-ttu-id="2765a-119">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="2765a-119">ServerVersion</span></span>  <br/> |[<span data-ttu-id="2765a-120">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="2765a-120">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="2765a-121">Identifica la versión del servidor que ha respondido a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2765a-121">Identifies the version of the server that responded to the request.</span></span>  <br/> |
   
## <a name="removedelegate-request-example"></a><span data-ttu-id="2765a-122">Ejemplo de solicitud de RemoveDelegate</span><span class="sxs-lookup"><span data-stu-id="2765a-122">RemoveDelegate request example</span></span>

### <a name="description"></a><span data-ttu-id="2765a-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="2765a-123">Description</span></span>

<span data-ttu-id="2765a-124">En el ejemplo de código siguiente se muestra cómo quitar a dos delegados de buzón de user1.</span><span class="sxs-lookup"><span data-stu-id="2765a-124">The following code example shows how to remove two delegates from user1's mailbox.</span></span> <span data-ttu-id="2765a-125">En este ejemplo, se quita un delegado mediante el uso de una dirección SMTP principal del delegado y el otro se se quita mediante el uso de identificador de seguridad del delegado (SID).</span><span class="sxs-lookup"><span data-stu-id="2765a-125">In this example, one delegate is removed by using the delegate's primary SMTP address, and the other one is removed by using the delegate's security identifier (SID).</span></span>
  
### <a name="code"></a><span data-ttu-id="2765a-126">Código</span><span class="sxs-lookup"><span data-stu-id="2765a-126">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1"/>
  </soap:Header>
  <soap:Body>
    <RemoveDelegate xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
                    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <Mailbox>
        <t:EmailAddress>user1@example.com</t:EmailAddress>
      </Mailbox>
      <UserIds>
        <t:UserId>
          <t:PrimarySmtpAddress>user2@example.com</t:PrimarySmtpAddress>
        </t:UserId>
        <t:UserId>
          <t:SID>S-1-5-21-1333220396-2200287332-232816053-1118</t:SID>
        </t:UserId>
      </UserIds>
    </RemoveDelegate>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="2765a-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2765a-127">Comments</span></span>

<span data-ttu-id="2765a-128">La operación **RemoveDelegate** no requieren que el usuario delegado especificado que tenga un buzón o que exista en el servicio de directorio de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2765a-128">The **RemoveDelegate** operation does not require the specified delegate user to have a mailbox or to exist in the Active Directory directory service.</span></span> <span data-ttu-id="2765a-129">La operación de **RemoveDelegate** se realizará correctamente si la entrada de delegado es huérfana.</span><span class="sxs-lookup"><span data-stu-id="2765a-129">The **RemoveDelegate** operation will succeed if the delegate entry is orphaned.</span></span> 
  
## <a name="removedelegate-response-example"></a><span data-ttu-id="2765a-130">Ejemplo de respuesta RemoveDelegate</span><span class="sxs-lookup"><span data-stu-id="2765a-130">RemoveDelegate response example</span></span>

### <a name="description"></a><span data-ttu-id="2765a-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="2765a-131">Description</span></span>

<span data-ttu-id="2765a-132">El siguiente ejemplo de una respuesta **RemoveDelegate** muestra una respuesta a una solicitud **RemoveDelegate** correcta.</span><span class="sxs-lookup"><span data-stu-id="2765a-132">The following example of a **RemoveDelegate** response shows a successful response to a **RemoveDelegate** request.</span></span> <span data-ttu-id="2765a-133">La respuesta contiene un elemento **DelegateUserResponseMessageType** para cada delegado que se ha quitado del buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="2765a-133">The response contains a **DelegateUserResponseMessageType** element for each delegate that is removed from the mailbox.</span></span> 
  
### <a name="code"></a><span data-ttu-id="2765a-134">Código</span><span class="sxs-lookup"><span data-stu-id="2765a-134">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" 
                         MinorVersion="1" 
                         MajorBuildNumber="206" 
                         MinorBuildNumber="0" 
                         Version="Exchange2007_SP1" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <m:RemoveDelegateResponse xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                              ResponseClass="Success" 
                              xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseCode>NoError</m:ResponseCode>
      <m:ResponseMessages>
        <m:DelegateUserResponseMessageType ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:DelegateUserResponseMessageType>
        <m:DelegateUserResponseMessageType ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:DelegateUserResponseMessageType>
      </m:ResponseMessages>
      </m:RemoveDelegateResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="removedelegate-error-response-example"></a><span data-ttu-id="2765a-135">Ejemplo de respuesta de RemoveDelegate Error</span><span class="sxs-lookup"><span data-stu-id="2765a-135">RemoveDelegate Error response example</span></span>

### <a name="description"></a><span data-ttu-id="2765a-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="2765a-136">Description</span></span>

<span data-ttu-id="2765a-137">El siguiente ejemplo de una respuesta de error **RemoveDelegate** muestra los resultados de una solicitud para quitar a un delegado que no existe.</span><span class="sxs-lookup"><span data-stu-id="2765a-137">The following example of a **RemoveDelegate** error response shows the results of a request to remove a delegate that does not exist.</span></span> 
  
### <a name="code"></a><span data-ttu-id="2765a-138">Código</span><span class="sxs-lookup"><span data-stu-id="2765a-138">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8"
                         MinorVersion="1"
                         MajorBuildNumber="206"
                         MinorBuildNumber="0"
                         Version="Exchange2007_SP1"
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <m:RemoveDelegateResponse xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
                              ResponseClass="Success"
                              xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseCode>NoError</m:ResponseCode>
      <m:ResponseMessages>
        <m:DelegateUserResponseMessageType ResponseClass="Error">
          <m:MessageText>The user is not a delegate for the mailbox.</m:MessageText>
          <m:ResponseCode>ErrorNotDelegate</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:DelegateUserResponseMessageType>
      </m:ResponseMessages>
    </m:RemoveDelegateResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="2765a-139">Ver también</span><span class="sxs-lookup"><span data-stu-id="2765a-139">See also</span></span>



- [<span data-ttu-id="2765a-140">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="2765a-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

