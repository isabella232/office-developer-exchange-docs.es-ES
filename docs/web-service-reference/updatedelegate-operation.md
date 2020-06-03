---
title: Operación UpdateDelegate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateDelegate
api_type:
- schema
ms.assetid: 03f618ac-ad1a-4772-9b81-c5bb0f12d6ab
description: La operación UpdateDelegate actualiza los permisos de delegado en el buzón de una entidad de identidad.
ms.openlocfilehash: b7cf5325d925f8d6588115a8657a2077e940f9d2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468561"
---
# <a name="updatedelegate-operation"></a><span data-ttu-id="c526f-103">Operación UpdateDelegate</span><span class="sxs-lookup"><span data-stu-id="c526f-103">UpdateDelegate operation</span></span>

<span data-ttu-id="c526f-104">La operación **UpdateDelegate** actualiza los permisos de delegado en el buzón de una entidad de identidad.</span><span class="sxs-lookup"><span data-stu-id="c526f-104">The **UpdateDelegate** operation updates delegate permissions on a principal's mailbox.</span></span> 
  
## <a name="soap-headers"></a><span data-ttu-id="c526f-105">Encabezados SOAP</span><span class="sxs-lookup"><span data-stu-id="c526f-105">SOAP Headers</span></span>

<span data-ttu-id="c526f-106">La operación **UpdateDelegate** puede usar los encabezados SOAP que se enumeran y describen en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="c526f-106">The **UpdateDelegate** operation can use the SOAP headers that are listed and described in the following table.</span></span> 
  
|<span data-ttu-id="c526f-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="c526f-107">**Header**</span></span>|<span data-ttu-id="c526f-108">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c526f-108">**Element**</span></span>|<span data-ttu-id="c526f-109">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c526f-109">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c526f-110">Suplantación</span><span class="sxs-lookup"><span data-stu-id="c526f-110">Impersonation</span></span>  <br/> |[<span data-ttu-id="c526f-111">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="c526f-111">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="c526f-112">Identifica al usuario que está suplantando la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="c526f-112">Identifies the user whom the client application is impersonating.</span></span>  <br/> |
|<span data-ttu-id="c526f-113">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="c526f-113">MailboxCulture</span></span>  <br/> |[<span data-ttu-id="c526f-114">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="c526f-114">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="c526f-115">Identifica la referencia cultural RFC3066 que se va a usar para obtener acceso al buzón.</span><span class="sxs-lookup"><span data-stu-id="c526f-115">Identifies the RFC3066 culture to be used to access the mailbox.</span></span>  <br/> |
|<span data-ttu-id="c526f-116">RequestVersion</span><span class="sxs-lookup"><span data-stu-id="c526f-116">RequestVersion</span></span>  <br/> |[<span data-ttu-id="c526f-117">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="c526f-117">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="c526f-118">Identifica la versión del esquema para la solicitud de operación.</span><span class="sxs-lookup"><span data-stu-id="c526f-118">Identifies the schema version for the operation request.</span></span>  <br/> |
|<span data-ttu-id="c526f-119">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="c526f-119">ServerVersion</span></span>  <br/> |[<span data-ttu-id="c526f-120">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="c526f-120">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="c526f-121">Identifica la versión del servidor que respondió a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c526f-121">Identifies the version of the server that responded to the request.</span></span>  <br/> |
   
## <a name="updatedelegate-request-example"></a><span data-ttu-id="c526f-122">Ejemplo de solicitud UpdateDelegate</span><span class="sxs-lookup"><span data-stu-id="c526f-122">UpdateDelegate request example</span></span>

### <a name="description"></a><span data-ttu-id="c526f-123">Description</span><span class="sxs-lookup"><span data-stu-id="c526f-123">Description</span></span>

<span data-ttu-id="c526f-124">En el siguiente ejemplo de una solicitud de **UpdateDelegate** se muestra cómo actualizar los permisos de delegado en la cuenta de Usuario1.</span><span class="sxs-lookup"><span data-stu-id="c526f-124">The following example of an **UpdateDelegate** request shows you how to update delegate permissions on user1's account.</span></span> <span data-ttu-id="c526f-125">Al usuario2 se le concede el nivel de permisos ninguno para la carpeta tareas y se le concede permiso para ver los elementos privados.</span><span class="sxs-lookup"><span data-stu-id="c526f-125">User2 is granted the None permission level for the Tasks folder and is granted permission to view private items.</span></span> <span data-ttu-id="c526f-126">Usuario3 tiene concedidos permisos de revisor para la carpeta diario.</span><span class="sxs-lookup"><span data-stu-id="c526f-126">User3 is granted Reviewer permissions for the Journal folder.</span></span> <span data-ttu-id="c526f-127">Las convocatorias de reunión se envían a los delegados y la información sobre la solicitud se envía a user1.</span><span class="sxs-lookup"><span data-stu-id="c526f-127">Meeting requests are sent to the delegates, and information about the request is sent to User1.</span></span> 
  
### <a name="code"></a><span data-ttu-id="c526f-128">Código</span><span class="sxs-lookup"><span data-stu-id="c526f-128">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1"/>
  </soap:Header>
  <soap:Body>
    <UpdateDelegate xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <Mailbox>
        <t:EmailAddress>user1@example.com</t:EmailAddress>
      </Mailbox>
      <DelegateUsers>
        <t:DelegateUser>
          <t:UserId>
            <t:PrimarySmtpAddress>user2@example.com</t:PrimarySmtpAddress>
          </t:UserId>
          <t:DelegatePermissions>
            <t:TasksFolderPermissionLevel>None</t:TasksFolderPermissionLevel>
          </t:DelegatePermissions>
          <t:ViewPrivateItems>true</t:ViewPrivateItems>
        </t:DelegateUser>
        <t:DelegateUser>
          <t:UserId>
            <t:PrimarySmtpAddress>user3@example.com</t:PrimarySmtpAddress>
          </t:UserId>
          <t:DelegatePermissions>
            <t:JournalFolderPermissionLevel>Reviewer</t:JournalFolderPermissionLevel>
          </t:DelegatePermissions>
        </t:DelegateUser>
      </DelegateUsers>
      <DeliverMeetingRequests>DelegatesAndSendInformationToMe</DeliverMeetingRequests>
    </UpdateDelegate>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="c526f-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c526f-129">Comments</span></span>

<span data-ttu-id="c526f-130">La solicitud [UpdateDelegate](updatedelegate.md) no requiere que las actualizaciones se apliquen a los delegados.</span><span class="sxs-lookup"><span data-stu-id="c526f-130">The [UpdateDelegate](updatedelegate.md) request does not require that updates be applied to delegates.</span></span> <span data-ttu-id="c526f-131">Los clientes solo pueden cambiar la configuración de **DeliverMeetingMessage** .</span><span class="sxs-lookup"><span data-stu-id="c526f-131">Clients can change only the **DeliverMeetingMessage** setting.</span></span> 
  
## <a name="updatedelegate-response-example"></a><span data-ttu-id="c526f-132">Ejemplo de respuesta UpdateDelegate</span><span class="sxs-lookup"><span data-stu-id="c526f-132">UpdateDelegate response example</span></span>

### <a name="description"></a><span data-ttu-id="c526f-133">Description</span><span class="sxs-lookup"><span data-stu-id="c526f-133">Description</span></span>

<span data-ttu-id="c526f-134">En el ejemplo siguiente se muestra una respuesta correcta a una operación **UpdateDelegate** .</span><span class="sxs-lookup"><span data-stu-id="c526f-134">The following example shows a successful response to an **UpdateDelegate** operation.</span></span> 
  
### <a name="code"></a><span data-ttu-id="c526f-135">Código</span><span class="sxs-lookup"><span data-stu-id="c526f-135">Code</span></span>

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
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <m:UpdateDelegateResponse xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                              ResponseClass="Success"
                              xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseCode>NoError</m:ResponseCode>
      <m:ResponseMessages>
        <m:DelegateUserResponseMessageType ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:DelegateUser>
            <t:UserId>
              <t:SID>S-1-5-21-1333220396-2200287332-232816053-1117</t:SID>
              <t:PrimarySmtpAddress>User2@example.com</t:PrimarySmtpAddress>
              <t:DisplayName>User2</t:DisplayName>
            </t:UserId>
            <t:ReceiveCopiesOfMeetingMessages>true</t:ReceiveCopiesOfMeetingMessages>
            <t:ViewPrivateItems>true</t:ViewPrivateItems>
          </m:DelegateUser>
        </m:DelegateUserResponseMessageType>
        <m:DelegateUserResponseMessageType ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:DelegateUser>
            <t:UserId>
              <t:SID>S-1-5-21-1333220396-2200287332-232816053-1118</t:SID>
              <t:PrimarySmtpAddress>User3@example.com</t:PrimarySmtpAddress>
              <t:DisplayName>User3</t:DisplayName>
            </t:UserId>
            <t:ReceiveCopiesOfMeetingMessages>true</t:ReceiveCopiesOfMeetingMessages>
            <t:ViewPrivateItems>false</t:ViewPrivateItems>
          </m:DelegateUser>
        </m:DelegateUserResponseMessageType>
      </m:ResponseMessages>
    </m:UpdateDelegateResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="updatedelegate-error-response-example"></a><span data-ttu-id="c526f-136">Ejemplo de respuesta de error UpdateDelegate</span><span class="sxs-lookup"><span data-stu-id="c526f-136">UpdateDelegate Error response example</span></span>

### <a name="description"></a><span data-ttu-id="c526f-137">Description</span><span class="sxs-lookup"><span data-stu-id="c526f-137">Description</span></span>

<span data-ttu-id="c526f-138">En el ejemplo siguiente se muestra una respuesta de error a una solicitud **UpdateDelegate** .</span><span class="sxs-lookup"><span data-stu-id="c526f-138">The following example shows an error response to an **UpdateDelegate** request.</span></span> <span data-ttu-id="c526f-139">El error se ha generado porque el delegado no existe en la lista de delegados de la entidad de la identidad.</span><span class="sxs-lookup"><span data-stu-id="c526f-139">The error was generated because the delegate does not exist in the principal's delegate list.</span></span> 
  
### <a name="code"></a><span data-ttu-id="c526f-140">Código</span><span class="sxs-lookup"><span data-stu-id="c526f-140">Code</span></span>

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
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <m:UpdateDelegateResponse xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                              ResponseClass="Success" 
                              xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseCode>NoError</m:ResponseCode>
      <m:ResponseMessages>
        <m:DelegateUserResponseMessageType ResponseClass="Error">
          <m:MessageText>The user is not a delegate for the mailbox.</m:MessageText>
          <m:ResponseCode>ErrorNotDelegate</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:DelegateUserResponseMessageType>
      </m:ResponseMessages>
      </m:UpdateDelegateResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="c526f-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="c526f-141">See also</span></span>



- [<span data-ttu-id="c526f-142">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="c526f-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

