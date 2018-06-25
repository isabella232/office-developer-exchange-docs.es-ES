---
title: Operación GetRoomLists
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetRoomLists
api_type:
- schema
ms.assetid: 55d451f9-547f-44ac-872e-9cb220ea7b7c
description: La operación GetRoomLists Obtiene las listas de las salas disponibles dentro de la organización de Exchange.
ms.openlocfilehash: 139a669bfc6b7c4bc9bd9c07f9f9cf52954860c0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764962"
---
# <a name="getroomlists-operation"></a><span data-ttu-id="90de5-103">Operación GetRoomLists</span><span class="sxs-lookup"><span data-stu-id="90de5-103">GetRoomLists operation</span></span>

<span data-ttu-id="90de5-104">La operación **GetRoomLists** Obtiene las listas de las salas disponibles dentro de la organización de Exchange.</span><span class="sxs-lookup"><span data-stu-id="90de5-104">The **GetRoomLists** operation gets the room lists that are available within the Exchange organization.</span></span> 
  
## <a name="soap-headers"></a><span data-ttu-id="90de5-105">Encabezados SOAP</span><span class="sxs-lookup"><span data-stu-id="90de5-105">SOAP Headers</span></span>

<span data-ttu-id="90de5-106">La operación de **GetRoomLists** puede utilizar los encabezados SOAP que se enumeran y describen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="90de5-106">The **GetRoomLists** operation can use the SOAP headers that are listed and described in the following table.</span></span> 
  
|<span data-ttu-id="90de5-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="90de5-107">**Header**</span></span>|<span data-ttu-id="90de5-108">**Element**</span><span class="sxs-lookup"><span data-stu-id="90de5-108">**Element**</span></span>|<span data-ttu-id="90de5-109">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="90de5-109">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="90de5-110">Suplantación</span><span class="sxs-lookup"><span data-stu-id="90de5-110">Impersonation</span></span>  <br/> |[<span data-ttu-id="90de5-111">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="90de5-111">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="90de5-112">Identifica el usuario que está realizando la suplantación de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="90de5-112">Identifies the user whom the client application is impersonating.</span></span>  <br/> |
|<span data-ttu-id="90de5-113">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="90de5-113">MailboxCulture</span></span>  <br/> |[<span data-ttu-id="90de5-114">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="90de5-114">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="90de5-115">Identifica la referencia cultural de RFC3066 va a usar para tener acceso al buzón.</span><span class="sxs-lookup"><span data-stu-id="90de5-115">Identifies the RFC3066 culture to be used to access the mailbox.</span></span>  <br/> |
|<span data-ttu-id="90de5-116">RequestVersion</span><span class="sxs-lookup"><span data-stu-id="90de5-116">RequestVersion</span></span>  <br/> |[<span data-ttu-id="90de5-117">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="90de5-117">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="90de5-118">Identifica la versión del esquema para la solicitud de la operación.</span><span class="sxs-lookup"><span data-stu-id="90de5-118">Identifies the schema version for the operation request.</span></span>  <br/> |
|<span data-ttu-id="90de5-119">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="90de5-119">ServerVersion</span></span>  <br/> |[<span data-ttu-id="90de5-120">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="90de5-120">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="90de5-121">Identifica la versión del servidor que ha respondido a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="90de5-121">Identifies the version of the server that responded to the request.</span></span>  <br/> |
   
## <a name="getroomlists-request-example"></a><span data-ttu-id="90de5-122">Ejemplo de solicitud de GetRoomLists</span><span class="sxs-lookup"><span data-stu-id="90de5-122">GetRoomLists request example</span></span>

### <a name="description"></a><span data-ttu-id="90de5-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="90de5-123">Description</span></span>

<span data-ttu-id="90de5-124">El siguiente es un ejemplo de una solicitud de **GetRoomLists** que devuelve las listas de las salas que están disponibles en el servidor.</span><span class="sxs-lookup"><span data-stu-id="90de5-124">The following is an example of a **GetRoomLists** request that returns the room lists that are available on the server.</span></span> 
  
### <a name="code"></a><span data-ttu-id="90de5-125">Código</span><span class="sxs-lookup"><span data-stu-id="90de5-125">Code</span></span>

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
    <m:GetRoomLists />
  </soap:Body>
</soap:Envelope>

```

### <a name="request-elements"></a><span data-ttu-id="90de5-126">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="90de5-126">Request elements</span></span>

<span data-ttu-id="90de5-127">El siguiente elemento se usa en la solicitud:</span><span class="sxs-lookup"><span data-stu-id="90de5-127">The following element is used in the request:</span></span>
  
- [<span data-ttu-id="90de5-128">GetRoomLists</span><span class="sxs-lookup"><span data-stu-id="90de5-128">GetRoomLists</span></span>](getroomlists.md)
    
## <a name="successful-getroomlists-response-example"></a><span data-ttu-id="90de5-129">Ejemplo de respuesta correcta de GetRoomLists</span><span class="sxs-lookup"><span data-stu-id="90de5-129">Successful GetRoomLists response example</span></span>

### <a name="description"></a><span data-ttu-id="90de5-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="90de5-130">Description</span></span>

<span data-ttu-id="90de5-131">El siguiente es un ejemplo de una respuesta a una solicitud de **GetRoomLists** .</span><span class="sxs-lookup"><span data-stu-id="90de5-131">The following is an example of a response to a **GetRoomLists** request.</span></span> <span data-ttu-id="90de5-132">Esta respuesta muestra una lista de salas en el servidor.</span><span class="sxs-lookup"><span data-stu-id="90de5-132">This response shows one room list on the server.</span></span> 
  
### <a name="code"></a><span data-ttu-id="90de5-133">Código</span><span class="sxs-lookup"><span data-stu-id="90de5-133">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" MinorVersion="1" MajorBuildNumber="164" MinorBuildNumber="0" Version="Exchange2010_SP1" xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" xmlns="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetRoomListsResponse ResponseClass="Success" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <m:RoomLists xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
        <t:Address xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
          <t:Name>Room List</t:Name>
          <t:EmailAddress>RoomList@contoso.com</t:EmailAddress>
          <t:RoutingType>SMTP</t:RoutingType>
          <t:MailboxType>PublicDL</t:MailboxType>
        </t:Address>
      </m:RoomLists>
    </GetRoomListsResponse>
  </s:Body>
</s:Envelope>

```

### <a name="successful-getroomlists-response-elements"></a><span data-ttu-id="90de5-134">Elementos de respuesta correctos de GetRoomLists</span><span class="sxs-lookup"><span data-stu-id="90de5-134">Successful GetRoomLists response elements</span></span>

<span data-ttu-id="90de5-135">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="90de5-135">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="90de5-136">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="90de5-136">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="90de5-137">GetRoomListsResponse</span><span class="sxs-lookup"><span data-stu-id="90de5-137">GetRoomListsResponse</span></span>](getroomlistsresponse.md)
    
- [<span data-ttu-id="90de5-138">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="90de5-138">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="90de5-139">RoomLists</span><span class="sxs-lookup"><span data-stu-id="90de5-139">RoomLists</span></span>](roomlists.md)
    
- [<span data-ttu-id="90de5-140">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="90de5-140">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md)
    
- [<span data-ttu-id="90de5-141">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="90de5-141">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md)
    
- [<span data-ttu-id="90de5-142">MailboxType</span><span class="sxs-lookup"><span data-stu-id="90de5-142">MailboxType</span></span>](mailboxtype.md)
    
### <a name="getroomlists-error-response-example"></a><span data-ttu-id="90de5-143">Ejemplo de respuesta de GetRoomLists Error</span><span class="sxs-lookup"><span data-stu-id="90de5-143">GetRoomLists Error response example</span></span>

#### <a name="description"></a><span data-ttu-id="90de5-144">Descripción</span><span class="sxs-lookup"><span data-stu-id="90de5-144">Description</span></span>

<span data-ttu-id="90de5-145">En el ejemplo siguiente se muestra la respuesta a un intento para obtener listas de las salas de un servidor que no tiene las listas de las salas definidas.</span><span class="sxs-lookup"><span data-stu-id="90de5-145">The following example shows the response to an attempt to get room lists from a server that does not have any room lists defined.</span></span>
  
#### <a name="code"></a><span data-ttu-id="90de5-146">Código</span><span class="sxs-lookup"><span data-stu-id="90de5-146">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" MinorVersion="1" MajorBuildNumber="164" MinorBuildNumber="0" Version="Exchange2010_SP1" xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" xmlns="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetRoomListsResponse ResponseClass="Success" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <m:RoomLists xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"/>
    </GetRoomListsResponse>
  </s:Body>
</s:Envelope>

```

#### <a name="getroomlists-error-response-elements"></a><span data-ttu-id="90de5-147">Elementos de respuesta de GetRoomLists Error</span><span class="sxs-lookup"><span data-stu-id="90de5-147">GetRoomLists Error response elements</span></span>

<span data-ttu-id="90de5-148">En la respuesta de error, se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="90de5-148">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="90de5-149">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="90de5-149">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="90de5-150">GetRoomListsResponse</span><span class="sxs-lookup"><span data-stu-id="90de5-150">GetRoomListsResponse</span></span>](getroomlistsresponse.md)
    
- [<span data-ttu-id="90de5-151">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="90de5-151">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="90de5-152">RoomLists</span><span class="sxs-lookup"><span data-stu-id="90de5-152">RoomLists</span></span>](roomlists.md)
    
## <a name="see-also"></a><span data-ttu-id="90de5-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="90de5-153">See also</span></span>



[<span data-ttu-id="90de5-154">Operaciones de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="90de5-154">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
  
- [<span data-ttu-id="90de5-155">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="90de5-155">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

