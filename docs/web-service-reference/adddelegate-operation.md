---
title: Operación AddDelegate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AddDelegate
api_type:
- schema
ms.assetid: 012d8cc5-648c-4ba0-a155-15c422b1e994
description: La operación AddDelegate agrega uno o más delegados al buzón de una entidad de identidad y establece permisos de acceso específicos.
ms.openlocfilehash: 80adbe71d69be1025dc9593c6a9002bc68fdcb76
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466517"
---
# <a name="adddelegate-operation"></a><span data-ttu-id="aebb5-103">Operación AddDelegate</span><span class="sxs-lookup"><span data-stu-id="aebb5-103">AddDelegate operation</span></span>

<span data-ttu-id="aebb5-104">La operación **AddDelegate** agrega uno o más delegados al buzón de una entidad de identidad y establece permisos de acceso específicos.</span><span class="sxs-lookup"><span data-stu-id="aebb5-104">The **AddDelegate** operation adds one or more delegates to a principal's mailbox and sets specific access permissions.</span></span> 
  
## <a name="soap-headers"></a><span data-ttu-id="aebb5-105">Encabezados SOAP</span><span class="sxs-lookup"><span data-stu-id="aebb5-105">SOAP headers</span></span>

<span data-ttu-id="aebb5-106">La operación **AddDelegate** puede usar los encabezados SOAP que se enumeran y describen en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="aebb5-106">The **AddDelegate** operation can use the SOAP headers that are listed and described in the following table.</span></span> 
  
|<span data-ttu-id="aebb5-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="aebb5-107">**Header**</span></span>|<span data-ttu-id="aebb5-108">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="aebb5-108">**Element**</span></span>|<span data-ttu-id="aebb5-109">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="aebb5-109">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="aebb5-110">Suplantación</span><span class="sxs-lookup"><span data-stu-id="aebb5-110">Impersonation</span></span>  <br/> |[<span data-ttu-id="aebb5-111">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="aebb5-111">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="aebb5-112">Identifica al usuario que está suplantando la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="aebb5-112">Identifies the user whom the client application is impersonating.</span></span>  <br/> |
|<span data-ttu-id="aebb5-113">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="aebb5-113">MailboxCulture</span></span>  <br/> |[<span data-ttu-id="aebb5-114">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="aebb5-114">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="aebb5-115">Identifica la referencia cultural RFC3066 que se va a usar para obtener acceso al buzón.</span><span class="sxs-lookup"><span data-stu-id="aebb5-115">Identifies the RFC3066 culture to be used to access the mailbox.</span></span>  <br/> |
|<span data-ttu-id="aebb5-116">RequestVersion</span><span class="sxs-lookup"><span data-stu-id="aebb5-116">RequestVersion</span></span>  <br/> |[<span data-ttu-id="aebb5-117">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="aebb5-117">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="aebb5-118">Identifica la versión del esquema para la solicitud de operación.</span><span class="sxs-lookup"><span data-stu-id="aebb5-118">Identifies the schema version for the operation request.</span></span>  <br/> |
|<span data-ttu-id="aebb5-119">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="aebb5-119">ServerVersion</span></span>  <br/> |[<span data-ttu-id="aebb5-120">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="aebb5-120">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="aebb5-121">Identifica la versión del servidor que respondió a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="aebb5-121">Identifies the version of the server that responded to the request.</span></span>  <br/> |
   
## <a name="adddelegate-request-example"></a><span data-ttu-id="aebb5-122">Ejemplo de solicitud AddDelegate</span><span class="sxs-lookup"><span data-stu-id="aebb5-122">AddDelegate request example</span></span>

### <a name="description"></a><span data-ttu-id="aebb5-123">Description</span><span class="sxs-lookup"><span data-stu-id="aebb5-123">Description</span></span>

<span data-ttu-id="aebb5-124">El siguiente ejemplo de una solicitud **AddDelegate** muestra un intento de conceder a user1 permisos delegar en carpetas que son propiedad del usuario2.</span><span class="sxs-lookup"><span data-stu-id="aebb5-124">The following example of an **AddDelegate** request shows an attempt to give user1 delegate permissions on folders that are owned by user2.</span></span> <span data-ttu-id="aebb5-125">User1 tiene permisos de autor para user2's la carpeta calendario y los permisos de nivel de revisor en la carpeta contactos de user2's.</span><span class="sxs-lookup"><span data-stu-id="aebb5-125">User1 is given Author-level permissions to user2's Calendar folder and Reviewer-level permissions to user2's Contacts folder.</span></span> <span data-ttu-id="aebb5-126">User1 no recibirá copias de los mensajes de reunión y no podrá ver los elementos privados en el buzón de user2's.</span><span class="sxs-lookup"><span data-stu-id="aebb5-126">User1 will not receive copies of meeting messages and will be unable to view private items in user2's mailbox.</span></span> <span data-ttu-id="aebb5-127">Las convocatorias de reunión se enviarán tanto a user1 como a usuario2.</span><span class="sxs-lookup"><span data-stu-id="aebb5-127">Meeting requests will be sent to both user1 and user2.</span></span> 
  
### <a name="code"></a><span data-ttu-id="aebb5-128">Código</span><span class="sxs-lookup"><span data-stu-id="aebb5-128">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1"/>
  </soap:Header>
  <soap:Body xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
    <AddDelegate>
      <Mailbox>
        <t:EmailAddress>user2@example.com</t:EmailAddress>
      </Mailbox>
      <DelegateUsers>
        <t:DelegateUser>
          <t:UserId>
            <t:PrimarySmtpAddress>user1@example.com</t:PrimarySmtpAddress>
          </t:UserId>
          <t:DelegatePermissions>
            <t:CalendarFolderPermissionLevel>Author</t:CalendarFolderPermissionLevel>
            <t:ContactsFolderPermissionLevel>Reviewer</t:ContactsFolderPermissionLevel>
          </t:DelegatePermissions>
          <t:ReceiveCopiesOfMeetingMessages>false</t:ReceiveCopiesOfMeetingMessages>
          <t:ViewPrivateItems>false</t:ViewPrivateItems>
        </t:DelegateUser>
      </DelegateUsers>
      <DeliverMeetingRequests>DelegatesAndMe</DeliverMeetingRequests>
    </AddDelegate>
  </soap:Body>
</soap:Envelope>
```

## <a name="adddelegate-response-example"></a><span data-ttu-id="aebb5-129">Ejemplo de respuesta AddDelegate</span><span class="sxs-lookup"><span data-stu-id="aebb5-129">AddDelegate response example</span></span>

### <a name="description"></a><span data-ttu-id="aebb5-130">Description</span><span class="sxs-lookup"><span data-stu-id="aebb5-130">Description</span></span>

<span data-ttu-id="aebb5-131">El siguiente ejemplo de una respuesta de **AddDelegate** muestra una respuesta correcta a una solicitud de **AddDelegate** .</span><span class="sxs-lookup"><span data-stu-id="aebb5-131">The following example of an **AddDelegate** response shows a successful response to an **AddDelegate** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="aebb5-132">Código</span><span class="sxs-lookup"><span data-stu-id="aebb5-132">Code</span></span>

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
    <m:AddDelegateResponse xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                           ResponseClass="Success" 
                           xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseCode>NoError</m:ResponseCode>
      <m:ResponseMessages>
        <m:DelegateUserResponseMessageType ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:DelegateUser>
              <t:UserId>
                <t:SID>S-1-5-21-1333220396-2200287332-232816053-1116</t:SID>
                <t:PrimarySmtpAddress>User1@example.com</t:PrimarySmtpAddress>
                <t:DisplayName>User1</t:DisplayName>
              </t:UserId>
              <t:ReceiveCopiesOfMeetingMessages>false</t:ReceiveCopiesOfMeetingMessages>
            <t:ViewPrivateItems>false</t:ViewPrivateItems>
            </m:DelegateUser>
        </m:DelegateUserResponseMessageType>
      </m:ResponseMessages>
    </m:AddDelegateResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="adddelegate-error-response-example"></a><span data-ttu-id="aebb5-133">Ejemplo de respuesta de error AddDelegate</span><span class="sxs-lookup"><span data-stu-id="aebb5-133">AddDelegate error response example</span></span>

### <a name="description"></a><span data-ttu-id="aebb5-134">Description</span><span class="sxs-lookup"><span data-stu-id="aebb5-134">Description</span></span>

<span data-ttu-id="aebb5-135">En el ejemplo siguiente se muestra la respuesta a una solicitud para agregar un delegado que ya se ha agregado al buzón de la entidad de la identidad.</span><span class="sxs-lookup"><span data-stu-id="aebb5-135">The following example shows the response to a request to add a delegate who has already been added to the principal's mailbox.</span></span>
  
### <a name="code"></a><span data-ttu-id="aebb5-136">Código</span><span class="sxs-lookup"><span data-stu-id="aebb5-136">Code</span></span>

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
    <m:AddDelegateResponse xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                           ResponseClass="Success"
                           xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseCode>NoError</m:ResponseCode>
      <m:ResponseMessages>
        <m:DelegateUserResponseMessageType ResponseClass="Error">
          <m:MessageText>The user is already a delegate for the mailbox.</m:MessageText>
          <m:ResponseCode>ErrorDelegateAlreadyExists</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:DelegateUserResponseMessageType>
      </m:ResponseMessages>
      </m:AddDelegateResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="aebb5-137">Comentarios</span><span class="sxs-lookup"><span data-stu-id="aebb5-137">Comments</span></span>

<span data-ttu-id="aebb5-138">Si se devuelve el código de respuesta ErrorDelegateAlreadyExists al intentar agregar un delegado, use la [operación GetDelegate](getdelegate-operation.md) para obtener todos los permisos actuales para el delegado y, a continuación, use la [operación UpdateDelegate](updatedelegate-operation.md) para establecer los nuevos permisos.</span><span class="sxs-lookup"><span data-stu-id="aebb5-138">If the ErrorDelegateAlreadyExists response code is returned when you try to add a delegate, use the [GetDelegate operation](getdelegate-operation.md) to get all the current permissions for the delegate, and then use the [UpdateDelegate operation](updatedelegate-operation.md) to set the new permissions.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="aebb5-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="aebb5-139">See also</span></span>

- [<span data-ttu-id="aebb5-140">Adición de delegados</span><span class="sxs-lookup"><span data-stu-id="aebb5-140">Adding Delegates</span></span>](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

