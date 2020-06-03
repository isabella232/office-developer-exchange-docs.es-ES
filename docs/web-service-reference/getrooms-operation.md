---
title: Operación GetRooms
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetRooms
api_type:
- schema
ms.assetid: 5501ddc0-3bfa-4da6-8e15-4223ca5499a3
description: La operación GetRooms obtiene las salas dentro de la lista de salas especificada.
ms.openlocfilehash: 4cb124b96637b9fcdca15595faebb2ce4d304de0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460550"
---
# <a name="getrooms-operation"></a><span data-ttu-id="d11e2-103">Operación GetRooms</span><span class="sxs-lookup"><span data-stu-id="d11e2-103">GetRooms operation</span></span>

<span data-ttu-id="d11e2-104">La operación **GetRooms** obtiene las salas dentro de la lista de salas especificada.</span><span class="sxs-lookup"><span data-stu-id="d11e2-104">The **GetRooms** operation gets the rooms within the specified room list.</span></span> 
  
## <a name="soap-headers"></a><span data-ttu-id="d11e2-105">Encabezados SOAP</span><span class="sxs-lookup"><span data-stu-id="d11e2-105">SOAP Headers</span></span>

<span data-ttu-id="d11e2-106">La operación **GetRooms** puede usar los encabezados SOAP que se enumeran y describen en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="d11e2-106">The **GetRooms** operation can use the SOAP headers that are listed and described in the following table.</span></span> 
  
|<span data-ttu-id="d11e2-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="d11e2-107">**Header**</span></span>|<span data-ttu-id="d11e2-108">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="d11e2-108">**Element**</span></span>|<span data-ttu-id="d11e2-109">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d11e2-109">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d11e2-110">Suplantación</span><span class="sxs-lookup"><span data-stu-id="d11e2-110">Impersonation</span></span>  <br/> |[<span data-ttu-id="d11e2-111">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="d11e2-111">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="d11e2-112">Identifica al usuario que está suplantando la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="d11e2-112">Identifies the user whom the client application is impersonating.</span></span>  <br/> |
|<span data-ttu-id="d11e2-113">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="d11e2-113">MailboxCulture</span></span>  <br/> |[<span data-ttu-id="d11e2-114">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="d11e2-114">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="d11e2-115">Identifica la referencia cultural RFC3066 que se va a usar para obtener acceso al buzón.</span><span class="sxs-lookup"><span data-stu-id="d11e2-115">Identifies the RFC3066 culture to be used to access the mailbox.</span></span>  <br/> |
|<span data-ttu-id="d11e2-116">RequestVersion</span><span class="sxs-lookup"><span data-stu-id="d11e2-116">RequestVersion</span></span>  <br/> |[<span data-ttu-id="d11e2-117">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="d11e2-117">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="d11e2-118">Identifica la versión del esquema para la solicitud de operación.</span><span class="sxs-lookup"><span data-stu-id="d11e2-118">Identifies the schema version for the operation request.</span></span>  <br/> |
|<span data-ttu-id="d11e2-119">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="d11e2-119">ServerVersion</span></span>  <br/> |[<span data-ttu-id="d11e2-120">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="d11e2-120">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="d11e2-121">Identifica la versión del servidor que respondió a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d11e2-121">Identifies the version of the server that responded to the request.</span></span>  <br/> |
   
## <a name="getrooms-request-example"></a><span data-ttu-id="d11e2-122">Ejemplo de solicitud GetRooms</span><span class="sxs-lookup"><span data-stu-id="d11e2-122">GetRooms request example</span></span>

### <a name="description"></a><span data-ttu-id="d11e2-123">Description</span><span class="sxs-lookup"><span data-stu-id="d11e2-123">Description</span></span>

<span data-ttu-id="d11e2-124">A continuación, se muestra un ejemplo de una solicitud de **GetRooms** que obtiene las salas asociadas con una lista de salas.</span><span class="sxs-lookup"><span data-stu-id="d11e2-124">The following is an example of a **GetRooms** request that gets the rooms that are associated with a room list.</span></span> 
  
### <a name="code"></a><span data-ttu-id="d11e2-125">Código</span><span class="sxs-lookup"><span data-stu-id="d11e2-125">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version ="Exchange2010_SP1"/>
  </soap:Header>
  <soap:Body>
    <m:GetRooms>
      <m:RoomList>
        <t:EmailAddress>RoomList@contoso.com</t:EmailAddress>
      </m:RoomList>
    </m:GetRooms>
  </soap:Body>

```

### <a name="request-elements"></a><span data-ttu-id="d11e2-126">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="d11e2-126">Request elements</span></span>

<span data-ttu-id="d11e2-127">Los siguientes elementos se usan en la solicitud:</span><span class="sxs-lookup"><span data-stu-id="d11e2-127">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="d11e2-128">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="d11e2-128">RequestServerVersion</span></span>](requestserverversion.md)
    
- [<span data-ttu-id="d11e2-129">GetRooms</span><span class="sxs-lookup"><span data-stu-id="d11e2-129">GetRooms</span></span>](getrooms.md)
    
- [<span data-ttu-id="d11e2-130">RoomList</span><span class="sxs-lookup"><span data-stu-id="d11e2-130">RoomList</span></span>](roomlist.md)
    
- [<span data-ttu-id="d11e2-131">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="d11e2-131">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md)
    
## <a name="successful-getrooms-response-example"></a><span data-ttu-id="d11e2-132">Ejemplo de respuesta GetRooms correcta</span><span class="sxs-lookup"><span data-stu-id="d11e2-132">Successful GetRooms response example</span></span>

### <a name="description"></a><span data-ttu-id="d11e2-133">Description</span><span class="sxs-lookup"><span data-stu-id="d11e2-133">Description</span></span>

<span data-ttu-id="d11e2-134">La siguiente respuesta muestra la información de la dirección de correo electrónico de las salas asociadas con la lista de salas.</span><span class="sxs-lookup"><span data-stu-id="d11e2-134">The following response shows the email address information for the rooms that are associated with the room list.</span></span>
  
### <a name="code"></a><span data-ttu-id="d11e2-135">Código</span><span class="sxs-lookup"><span data-stu-id="d11e2-135">Code</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" MinorVersion="1" MajorBuildNumber="164" MinorBuildNumber="0" Version="Exchange2010_SP1" xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" xmlns="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetRoomsResponse ResponseClass="Success" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <m:Rooms xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
        <t:Room xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
          <t:Id>
            <t:Name>Room01</t:Name>
            <t:EmailAddress>Room01@contoso.com</t:EmailAddress>
            <t:RoutingType>SMTP</t:RoutingType>
            <t:MailboxType>Mailbox</t:MailboxType>
          </t:Id>
        </t:Room>
        <t:Room xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
          <t:Id>
            <t:Name>Room02</t:Name>
            <t:EmailAddress>Room02@contoso.com</t:EmailAddress>
            <t:RoutingType>SMTP</t:RoutingType>
            <t:MailboxType>Mailbox</t:MailboxType>
          </t:Id>
        </t:Room>
      </m:Rooms>
    </GetRoomsResponse>
  </s:Body>
</s:Envelope>
```

### <a name="successful-getrooms-response-elements"></a><span data-ttu-id="d11e2-136">Elementos de respuesta GetRooms correctos</span><span class="sxs-lookup"><span data-stu-id="d11e2-136">Successful GetRooms response elements</span></span>

<span data-ttu-id="d11e2-137">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="d11e2-137">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="d11e2-138">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="d11e2-138">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="d11e2-139">GetRoomsResponse</span><span class="sxs-lookup"><span data-stu-id="d11e2-139">GetRoomsResponse</span></span>](getroomsresponse.md)
    
- [<span data-ttu-id="d11e2-140">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="d11e2-140">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="d11e2-141">Sala</span><span class="sxs-lookup"><span data-stu-id="d11e2-141">Rooms</span></span>](rooms.md)
    
- [<span data-ttu-id="d11e2-142">Sala</span><span class="sxs-lookup"><span data-stu-id="d11e2-142">Room</span></span>](room.md)
    
- [<span data-ttu-id="d11e2-143">Nombre (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="d11e2-143">Name (EmailAddress)</span></span>](name-emailaddress.md)
    
- [<span data-ttu-id="d11e2-144">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="d11e2-144">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md)
    
- [<span data-ttu-id="d11e2-145">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="d11e2-145">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md)
    
- [<span data-ttu-id="d11e2-146">MailboxType</span><span class="sxs-lookup"><span data-stu-id="d11e2-146">MailboxType</span></span>](mailboxtype.md)
    
## <a name="getrooms-error-response-example"></a><span data-ttu-id="d11e2-147">Ejemplo de respuesta de error GetRooms</span><span class="sxs-lookup"><span data-stu-id="d11e2-147">GetRooms Error response example</span></span>

### <a name="description"></a><span data-ttu-id="d11e2-148">Description</span><span class="sxs-lookup"><span data-stu-id="d11e2-148">Description</span></span>

<span data-ttu-id="d11e2-149">En el ejemplo siguiente se muestra una respuesta de error causada por un intento de obtener información de la sala para una lista de salas inexistente.</span><span class="sxs-lookup"><span data-stu-id="d11e2-149">The following example shows an error response caused by an attempt to get room information for a nonexistent room list.</span></span>
  
### <a name="code"></a><span data-ttu-id="d11e2-150">Código</span><span class="sxs-lookup"><span data-stu-id="d11e2-150">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" MinorVersion="1" MajorBuildNumber="164" MinorBuildNumber="0" Version="Exchange2010_SP1" xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" xmlns="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetRoomsResponse ResponseClass="Error" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <MessageText>No results were found.</MessageText>
      <ResponseCode>ErrorNameResolutionNoResults</ResponseCode>
      <DescriptiveLinkKey>0</DescriptiveLinkKey>
    </GetRoomsResponse>
  </s:Body>
</s:Envelope>
```

### <a name="getrooms-error-response-elements"></a><span data-ttu-id="d11e2-151">Elementos de respuesta de error de GetRooms</span><span class="sxs-lookup"><span data-stu-id="d11e2-151">GetRooms Error response elements</span></span>

<span data-ttu-id="d11e2-152">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="d11e2-152">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="d11e2-153">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="d11e2-153">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="d11e2-154">GetRoomsResponse</span><span class="sxs-lookup"><span data-stu-id="d11e2-154">GetRoomsResponse</span></span>](getroomsresponse.md)
    
- [<span data-ttu-id="d11e2-155">MessageText</span><span class="sxs-lookup"><span data-stu-id="d11e2-155">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="d11e2-156">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="d11e2-156">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="d11e2-157">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="d11e2-157">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="d11e2-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="d11e2-158">See also</span></span>

- [<span data-ttu-id="d11e2-159">Operaciones de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="d11e2-159">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
- [<span data-ttu-id="d11e2-160">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="d11e2-160">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

