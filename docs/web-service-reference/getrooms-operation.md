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
description: La operación GetRooms Obtiene las salas dentro de la lista de salas especificado.
ms.openlocfilehash: 3718c476881ae8aa538646464e7c61845d849562
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764966"
---
# <a name="getrooms-operation"></a><span data-ttu-id="45bce-103">Operación GetRooms</span><span class="sxs-lookup"><span data-stu-id="45bce-103">GetRooms operation</span></span>

<span data-ttu-id="45bce-104">La operación **GetRooms** Obtiene las salas dentro de la lista de salas especificado.</span><span class="sxs-lookup"><span data-stu-id="45bce-104">The **GetRooms** operation gets the rooms within the specified room list.</span></span> 
  
## <a name="soap-headers"></a><span data-ttu-id="45bce-105">Encabezados SOAP</span><span class="sxs-lookup"><span data-stu-id="45bce-105">SOAP Headers</span></span>

<span data-ttu-id="45bce-106">La operación de **GetRooms** puede utilizar los encabezados SOAP que se enumeran y describen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="45bce-106">The **GetRooms** operation can use the SOAP headers that are listed and described in the following table.</span></span> 
  
|<span data-ttu-id="45bce-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="45bce-107">**Header**</span></span>|<span data-ttu-id="45bce-108">**Element**</span><span class="sxs-lookup"><span data-stu-id="45bce-108">**Element**</span></span>|<span data-ttu-id="45bce-109">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="45bce-109">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="45bce-110">Suplantación</span><span class="sxs-lookup"><span data-stu-id="45bce-110">Impersonation</span></span>  <br/> |[<span data-ttu-id="45bce-111">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="45bce-111">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="45bce-112">Identifica el usuario que está realizando la suplantación de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="45bce-112">Identifies the user whom the client application is impersonating.</span></span>  <br/> |
|<span data-ttu-id="45bce-113">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="45bce-113">MailboxCulture</span></span>  <br/> |[<span data-ttu-id="45bce-114">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="45bce-114">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="45bce-115">Identifica la referencia cultural de RFC3066 va a usar para tener acceso al buzón.</span><span class="sxs-lookup"><span data-stu-id="45bce-115">Identifies the RFC3066 culture to be used to access the mailbox.</span></span>  <br/> |
|<span data-ttu-id="45bce-116">RequestVersion</span><span class="sxs-lookup"><span data-stu-id="45bce-116">RequestVersion</span></span>  <br/> |[<span data-ttu-id="45bce-117">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="45bce-117">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="45bce-118">Identifica la versión del esquema para la solicitud de la operación.</span><span class="sxs-lookup"><span data-stu-id="45bce-118">Identifies the schema version for the operation request.</span></span>  <br/> |
|<span data-ttu-id="45bce-119">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="45bce-119">ServerVersion</span></span>  <br/> |[<span data-ttu-id="45bce-120">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="45bce-120">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="45bce-121">Identifica la versión del servidor que ha respondido a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="45bce-121">Identifies the version of the server that responded to the request.</span></span>  <br/> |
   
## <a name="getrooms-request-example"></a><span data-ttu-id="45bce-122">Ejemplo de solicitud de GetRooms</span><span class="sxs-lookup"><span data-stu-id="45bce-122">GetRooms request example</span></span>

### <a name="description"></a><span data-ttu-id="45bce-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="45bce-123">Description</span></span>

<span data-ttu-id="45bce-124">El siguiente es un ejemplo de una solicitud de **GetRooms** que obtiene los salones que están asociados con una lista de salas.</span><span class="sxs-lookup"><span data-stu-id="45bce-124">The following is an example of a **GetRooms** request that gets the rooms that are associated with a room list.</span></span> 
  
### <a name="code"></a><span data-ttu-id="45bce-125">Código</span><span class="sxs-lookup"><span data-stu-id="45bce-125">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="request-elements"></a><span data-ttu-id="45bce-126">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="45bce-126">Request elements</span></span>

<span data-ttu-id="45bce-127">En la solicitud se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="45bce-127">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="45bce-128">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="45bce-128">RequestServerVersion</span></span>](requestserverversion.md)
    
- [<span data-ttu-id="45bce-129">GetRooms</span><span class="sxs-lookup"><span data-stu-id="45bce-129">GetRooms</span></span>](getrooms.md)
    
- [<span data-ttu-id="45bce-130">RoomList</span><span class="sxs-lookup"><span data-stu-id="45bce-130">RoomList</span></span>](roomlist.md)
    
- [<span data-ttu-id="45bce-131">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="45bce-131">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md)
    
## <a name="successful-getrooms-response-example"></a><span data-ttu-id="45bce-132">Ejemplo de respuesta correcta de GetRooms</span><span class="sxs-lookup"><span data-stu-id="45bce-132">Successful GetRooms response example</span></span>

### <a name="description"></a><span data-ttu-id="45bce-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="45bce-133">Description</span></span>

<span data-ttu-id="45bce-134">La respuesta siguiente muestra la información de dirección de correo electrónico para los salones que están asociados con la lista de salas.</span><span class="sxs-lookup"><span data-stu-id="45bce-134">The following response shows the email address information for the rooms that are associated with the room list.</span></span>
  
### <a name="code"></a><span data-ttu-id="45bce-135">Código</span><span class="sxs-lookup"><span data-stu-id="45bce-135">Code</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" MinorVersion="1" MajorBuildNumber="164" MinorBuildNumber="0" Version="Exchange2010_SP1" xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" xmlns="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetRoomsResponse ResponseClass="Success" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <m:Rooms xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
        <t:Room xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
          <t:Id>
            <t:Name>Room01</t:Name>
            <t:EmailAddress>Room01@contoso.com</t:EmailAddress>
            <t:RoutingType>SMTP</t:RoutingType>
            <t:MailboxType>Mailbox</t:MailboxType>
          </t:Id>
        </t:Room>
        <t:Room xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

### <a name="successful-getrooms-response-elements"></a><span data-ttu-id="45bce-136">Elementos de respuesta correctos de GetRooms</span><span class="sxs-lookup"><span data-stu-id="45bce-136">Successful GetRooms response elements</span></span>

<span data-ttu-id="45bce-137">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="45bce-137">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="45bce-138">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="45bce-138">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="45bce-139">GetRoomsResponse</span><span class="sxs-lookup"><span data-stu-id="45bce-139">GetRoomsResponse</span></span>](getroomsresponse.md)
    
- [<span data-ttu-id="45bce-140">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="45bce-140">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="45bce-141">Salones</span><span class="sxs-lookup"><span data-stu-id="45bce-141">Rooms</span></span>](rooms.md)
    
- [<span data-ttu-id="45bce-142">Salón</span><span class="sxs-lookup"><span data-stu-id="45bce-142">Room</span></span>](room.md)
    
- [<span data-ttu-id="45bce-143">Nombre (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="45bce-143">Name (EmailAddress)</span></span>](name-emailaddress.md)
    
- [<span data-ttu-id="45bce-144">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="45bce-144">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md)
    
- [<span data-ttu-id="45bce-145">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="45bce-145">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md)
    
- [<span data-ttu-id="45bce-146">MailboxType</span><span class="sxs-lookup"><span data-stu-id="45bce-146">MailboxType</span></span>](mailboxtype.md)
    
## <a name="getrooms-error-response-example"></a><span data-ttu-id="45bce-147">Ejemplo de respuesta de GetRooms Error</span><span class="sxs-lookup"><span data-stu-id="45bce-147">GetRooms Error response example</span></span>

### <a name="description"></a><span data-ttu-id="45bce-148">Descripción</span><span class="sxs-lookup"><span data-stu-id="45bce-148">Description</span></span>

<span data-ttu-id="45bce-149">En el ejemplo siguiente se muestra una respuesta de error debida a un intento de obtener información sobre las salas para una lista de salas que no existe.</span><span class="sxs-lookup"><span data-stu-id="45bce-149">The following example shows an error response caused by an attempt to get room information for a nonexistent room list.</span></span>
  
### <a name="code"></a><span data-ttu-id="45bce-150">Código</span><span class="sxs-lookup"><span data-stu-id="45bce-150">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" MinorVersion="1" MajorBuildNumber="164" MinorBuildNumber="0" Version="Exchange2010_SP1" xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" xmlns="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetRoomsResponse ResponseClass="Error" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <MessageText>No results were found.</MessageText>
      <ResponseCode>ErrorNameResolutionNoResults</ResponseCode>
      <DescriptiveLinkKey>0</DescriptiveLinkKey>
    </GetRoomsResponse>
  </s:Body>
</s:Envelope>
```

### <a name="getrooms-error-response-elements"></a><span data-ttu-id="45bce-151">Elementos de respuesta de GetRooms Error</span><span class="sxs-lookup"><span data-stu-id="45bce-151">GetRooms Error response elements</span></span>

<span data-ttu-id="45bce-152">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="45bce-152">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="45bce-153">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="45bce-153">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="45bce-154">GetRoomsResponse</span><span class="sxs-lookup"><span data-stu-id="45bce-154">GetRoomsResponse</span></span>](getroomsresponse.md)
    
- [<span data-ttu-id="45bce-155">MessageText</span><span class="sxs-lookup"><span data-stu-id="45bce-155">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="45bce-156">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="45bce-156">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="45bce-157">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="45bce-157">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="45bce-158">Ver también</span><span class="sxs-lookup"><span data-stu-id="45bce-158">See also</span></span>

- [<span data-ttu-id="45bce-159">Operaciones de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="45bce-159">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
- [<span data-ttu-id="45bce-160">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="45bce-160">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

