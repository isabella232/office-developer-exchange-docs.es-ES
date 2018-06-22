---
title: Operación GetDelegate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetDelegate
api_type:
- schema
ms.assetid: 849b2c9e-4685-4bd1-9adb-aba0fcc52650
description: La operación GetDelegate recupera la configuración de delegado para un buzón especificado.
ms.openlocfilehash: bd1a0add54ee5fd1c23b4ba09a921a9061afa394
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764800"
---
# <a name="getdelegate-operation"></a><span data-ttu-id="feb68-103">Operación GetDelegate</span><span class="sxs-lookup"><span data-stu-id="feb68-103">GetDelegate operation</span></span>

<span data-ttu-id="feb68-104">La operación **GetDelegate** recupera la configuración de delegado para un buzón especificado.</span><span class="sxs-lookup"><span data-stu-id="feb68-104">The **GetDelegate** operation retrieves the delegate settings for a specified mailbox.</span></span> 
  
## <a name="soap-headers"></a><span data-ttu-id="feb68-105">Encabezados SOAP</span><span class="sxs-lookup"><span data-stu-id="feb68-105">SOAP Headers</span></span>

<span data-ttu-id="feb68-106">La operación de **GetDelegate** puede utilizar los encabezados SOAP que se enumeran y describen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="feb68-106">The **GetDelegate** operation can use the SOAP headers that are listed and described in the following table.</span></span> 
  
|<span data-ttu-id="feb68-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="feb68-107">**Header**</span></span>|<span data-ttu-id="feb68-108">**Element**</span><span class="sxs-lookup"><span data-stu-id="feb68-108">**Element**</span></span>|<span data-ttu-id="feb68-109">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="feb68-109">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="feb68-110">Suplantación</span><span class="sxs-lookup"><span data-stu-id="feb68-110">Impersonation</span></span>  <br/> |[<span data-ttu-id="feb68-111">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="feb68-111">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="feb68-112">Identifica el usuario que está realizando la suplantación de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="feb68-112">Identifies the user whom the client application is impersonating.</span></span>  <br/> |
|<span data-ttu-id="feb68-113">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="feb68-113">MailboxCulture</span></span>  <br/> |[<span data-ttu-id="feb68-114">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="feb68-114">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="feb68-115">Identifica la referencia cultural de RFC3066 va a usar para tener acceso al buzón.</span><span class="sxs-lookup"><span data-stu-id="feb68-115">Identifies the RFC3066 culture to be used to access the mailbox.</span></span>  <br/> |
|<span data-ttu-id="feb68-116">RequestVersion</span><span class="sxs-lookup"><span data-stu-id="feb68-116">RequestVersion</span></span>  <br/> |[<span data-ttu-id="feb68-117">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="feb68-117">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="feb68-118">Identifica la versión del esquema para la solicitud de la operación.</span><span class="sxs-lookup"><span data-stu-id="feb68-118">Identifies the schema version for the operation request.</span></span>  <br/> |
|<span data-ttu-id="feb68-119">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="feb68-119">ServerVersion</span></span>  <br/> |[<span data-ttu-id="feb68-120">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="feb68-120">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="feb68-121">Identifica la versión del servidor que ha respondido a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="feb68-121">Identifies the version of the server that responded to the request.</span></span>  <br/> |
   
## <a name="getdelegate-request-example"></a><span data-ttu-id="feb68-122">Ejemplo de solicitud de GetDelegate</span><span class="sxs-lookup"><span data-stu-id="feb68-122">GetDelegate request example</span></span>

### <a name="description"></a><span data-ttu-id="feb68-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="feb68-123">Description</span></span>

<span data-ttu-id="feb68-124">En el ejemplo de código siguiente se muestra cómo recuperar la configuración de delegado de todos los delegados que se establecen en el buzón de correo del user3.</span><span class="sxs-lookup"><span data-stu-id="feb68-124">The following code example shows how to retrieve the delegate settings for all the delegates that are set on user3's mailbox.</span></span> <span data-ttu-id="feb68-125">Todos los permisos para cada usuario se devuelven en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="feb68-125">All the permissions for each user are returned in the response.</span></span>
  
### <a name="code"></a><span data-ttu-id="feb68-126">Código</span><span class="sxs-lookup"><span data-stu-id="feb68-126">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1"/>
  </soap:Header>
  <soap:Body>
    <GetDelegate xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
                 xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
                 IncludePermissions="true">
      <Mailbox>
        <t:EmailAddress>user3@example.com</t:EmailAddress>
      </Mailbox>
    </GetDelegate>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="feb68-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="feb68-127">Comments</span></span>

<span data-ttu-id="feb68-128">Puede usar el elemento [UserId](userid.md) para especificar usuarios individuales en lugar de devolver todos los usuarios que tienen permisos de acceso delegado en el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="feb68-128">You can use the [UserId](userid.md) element to specify individual users instead of returning all users who have delegate access permissions on the mailbox.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="feb68-129">Servicios Web de Exchange (EWS) no admite a delegados de grupo de administración.</span><span class="sxs-lookup"><span data-stu-id="feb68-129">Exchange Web Services (EWS) does not support managing group delegates.</span></span> <span data-ttu-id="feb68-130">EWS devolverá un error si se llama a la operación de **GetDelegate** para una entidad de seguridad que tiene un delegado de grupo de seguridad.</span><span class="sxs-lookup"><span data-stu-id="feb68-130">EWS will return an error if the **GetDelegate** operation is called for a principal that has a security group delegate.</span></span> 
  
## <a name="getdelegate-response-example"></a><span data-ttu-id="feb68-131">Ejemplo de respuesta GetDelegate</span><span class="sxs-lookup"><span data-stu-id="feb68-131">GetDelegate response example</span></span>

### <a name="description"></a><span data-ttu-id="feb68-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="feb68-132">Description</span></span>

<span data-ttu-id="feb68-133">El siguiente ejemplo de una respuesta **GetDelegate** muestra una respuesta a una solicitud **GetDelegate** correcta.</span><span class="sxs-lookup"><span data-stu-id="feb68-133">The following example of a **GetDelegate** response shows a successful response to a **GetDelegate** request.</span></span> <span data-ttu-id="feb68-134">La respuesta contiene información acerca de los permisos de acceso delegado, si el delegado puede ver elementos privados, si el delegado recibe copia de los mensajes de la reunión y a quién la reunión se entregaron las solicitudes.</span><span class="sxs-lookup"><span data-stu-id="feb68-134">The response contains information about the delegate access permissions, whether the delegate can view private items, whether the delegate receives copies of meeting messages, and to whom meeting requests were delivered.</span></span> 
  
### <a name="code"></a><span data-ttu-id="feb68-135">Código</span><span class="sxs-lookup"><span data-stu-id="feb68-135">Code</span></span>

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
    <m:GetDelegateResponse xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                           ResponseClass="Success" 
                           xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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
              <t:DelegatePermissions>
                <t:CalendarFolderPermissionLevel>Author</t:CalendarFolderPermissionLevel>
                <t:ContactsFolderPermissionLevel>Reviewer</t:ContactsFolderPermissionLevel>
              </t:DelegatePermissions>
              <t:ReceiveCopiesOfMeetingMessages>false</t:ReceiveCopiesOfMeetingMessages>
            <t:ViewPrivateItems>false</t:ViewPrivateItems>
            </m:DelegateUser>
          </m:DelegateUserResponseMessageType>
      </m:ResponseMessages>
      <m:DeliverMeetingRequests>DelegatesAndMe</m:DeliverMeetingRequests>
      </m:GetDelegateResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="feb68-136">Ver también</span><span class="sxs-lookup"><span data-stu-id="feb68-136">See also</span></span>



- [<span data-ttu-id="feb68-137">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="feb68-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

