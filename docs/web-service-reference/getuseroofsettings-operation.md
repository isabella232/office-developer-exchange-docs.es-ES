---
title: Operación GetUserOofSettings
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetUserOofSettings
api_type:
- schema
ms.assetid: 153e4440-495b-4972-9811-2fbea740142a
description: La operación GetUserOofSettings obtiene los mensajes y la configuración de fuera de la oficina (OOF) del usuario de un buzón.
ms.openlocfilehash: 622faa622b0ea231a6331ff62631885d4252c1f5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457700"
---
# <a name="getuseroofsettings-operation"></a><span data-ttu-id="a064e-103">Operación GetUserOofSettings</span><span class="sxs-lookup"><span data-stu-id="a064e-103">GetUserOofSettings operation</span></span>

<span data-ttu-id="a064e-104">La operación **GetUserOofSettings** obtiene los mensajes y la configuración de fuera de la oficina (OOF) del usuario de un buzón.</span><span class="sxs-lookup"><span data-stu-id="a064e-104">The **GetUserOofSettings** operation gets a mailbox user's Out of Office (OOF) settings and messages.</span></span> 
  
## <a name="soap-headers"></a><span data-ttu-id="a064e-105">Encabezados SOAP</span><span class="sxs-lookup"><span data-stu-id="a064e-105">SOAP Headers</span></span>

<span data-ttu-id="a064e-106">La operación **GetUserOofSettings** puede usar los encabezados SOAP que se enumeran y describen en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="a064e-106">The **GetUserOofSettings** operation can use the SOAP headers that are listed and described in the following table.</span></span> 
  
|<span data-ttu-id="a064e-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="a064e-107">**Header**</span></span>|<span data-ttu-id="a064e-108">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a064e-108">**Element**</span></span>|<span data-ttu-id="a064e-109">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a064e-109">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a064e-110">Suplantación</span><span class="sxs-lookup"><span data-stu-id="a064e-110">Impersonation</span></span>  <br/> |[<span data-ttu-id="a064e-111">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="a064e-111">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="a064e-112">Identifica al usuario que está suplantando la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="a064e-112">Identifies the user whom the client application is impersonating.</span></span>  <br/> |
|<span data-ttu-id="a064e-113">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="a064e-113">ServerVersion</span></span>  <br/> |[<span data-ttu-id="a064e-114">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="a064e-114">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="a064e-115">Identifica la versión del servidor que respondió a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a064e-115">Identifies the version of the server that responded to the request.</span></span>  <br/> |
   
## <a name="using-the-getuseroofsettings-operation"></a><span data-ttu-id="a064e-116">Uso de la operación GetUserOofSettings</span><span class="sxs-lookup"><span data-stu-id="a064e-116">Using the GetUserOofSettings Operation</span></span>

<span data-ttu-id="a064e-117">La operación **GetUserOofSettings** proporciona acceso a la configuración OOF de un usuario.</span><span class="sxs-lookup"><span data-stu-id="a064e-117">The **GetUserOofSettings** operation provides access to a user's OOF settings.</span></span> <span data-ttu-id="a064e-118">Un usuario se identifica mediante la dirección de correo electrónico del usuario.</span><span class="sxs-lookup"><span data-stu-id="a064e-118">A user is identified by the user's email address.</span></span> <span data-ttu-id="a064e-119">Si el mensaje OOF es nulo y OOF está habilitado, no se enviará ningún mensaje OOF.</span><span class="sxs-lookup"><span data-stu-id="a064e-119">If the OOF message is null and OOF is enabled, no OOF message is sent.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="a064e-120">Si los mensajes OOF están establecidos por MicrosoftOfficeOutlook, esta operación devolverá los mensajes OOF en formato HTML.</span><span class="sxs-lookup"><span data-stu-id="a064e-120">If the OOF messages are set by MicrosoftOfficeOutlook, this operation will return the OOF messages in HTML format.</span></span> 
  
## <a name="getuseroofsettings-request-example"></a><span data-ttu-id="a064e-121">Ejemplo de solicitud GetUserOofSettings</span><span class="sxs-lookup"><span data-stu-id="a064e-121">GetUserOofSettings request example</span></span>

### <a name="description"></a><span data-ttu-id="a064e-122">Description</span><span class="sxs-lookup"><span data-stu-id="a064e-122">Description</span></span>

<span data-ttu-id="a064e-123">En el ejemplo siguiente se muestra una solicitud de **GetUserOofSettings** que obtiene la información de OOF de un solo usuario.</span><span class="sxs-lookup"><span data-stu-id="a064e-123">The following example shows a **GetUserOofSettings** request that gets a single user's OOF information.</span></span> 
  
### <a name="code"></a><span data-ttu-id="a064e-124">Código</span><span class="sxs-lookup"><span data-stu-id="a064e-124">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetUserOofSettingsRequest xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <Mailbox xmlns ="https://schemas.microsoft.com/exchange/services/2006/types">
        <Address>User1@example.com</Address>
      </Mailbox>
    </GetUserOofSettingsRequest>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a><span data-ttu-id="a064e-125">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="a064e-125">Request elements</span></span>

<span data-ttu-id="a064e-126">Los siguientes elementos se usan en la solicitud:</span><span class="sxs-lookup"><span data-stu-id="a064e-126">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="a064e-127">GetUserOofSettingsRequest</span><span class="sxs-lookup"><span data-stu-id="a064e-127">GetUserOofSettingsRequest</span></span>](getuseroofsettingsrequest.md)
    
- [<span data-ttu-id="a064e-128">Buzón de correo (disponibilidad)</span><span class="sxs-lookup"><span data-stu-id="a064e-128">Mailbox (Availability)</span></span>](mailbox-availability.md)
    
- [<span data-ttu-id="a064e-129">Address (cadena)</span><span class="sxs-lookup"><span data-stu-id="a064e-129">Address (string)</span></span>](address-string.md)
    
## <a name="successful-getuseroofsettings-response-example"></a><span data-ttu-id="a064e-130">Ejemplo de respuesta GetUserOofSettings correcta</span><span class="sxs-lookup"><span data-stu-id="a064e-130">Successful GetUserOofSettings response example</span></span>

### <a name="description"></a><span data-ttu-id="a064e-131">Description</span><span class="sxs-lookup"><span data-stu-id="a064e-131">Description</span></span>

<span data-ttu-id="a064e-132">En el ejemplo siguiente se muestra un estado de OOF deshabilitado con los mensajes OOF.</span><span class="sxs-lookup"><span data-stu-id="a064e-132">The following example shows a disabled OOF state with the OOF messages.</span></span>
  
### <a name="code"></a><span data-ttu-id="a064e-133">Código</span><span class="sxs-lookup"><span data-stu-id="a064e-133">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetUserOofSettingsResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseMessage ResponseClass="Success">
        <ResponseCode>NoError</ResponseCode>
      </ResponseMessage>
      <OofSettings xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
        <OofState>Disabled</OofState>
        <ExternalAudience>All</ExternalAudience>
        <Duration>
          <StartTime>2006-11-03T23:00:00</StartTime>
          <EndTime>2006-11-04T23:00:00</EndTime>
        </Duration>
        <InternalReply>
          <Message>I am out of office. This is my internal reply.</Message>
        </InternalReply>
        <ExternalReply>
          <Message>I am out of office. This is my external reply.</Message>
        </ExternalReply>
      </OofSettings>
      <AllowExternalOof>All</AllowExternalOof>
    </GetUserOofSettingsResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-getuseroofsettings-response-elements"></a><span data-ttu-id="a064e-134">Elementos de respuesta GetUserOofSettings correctos</span><span class="sxs-lookup"><span data-stu-id="a064e-134">Successful GetUserOofSettings response elements</span></span>

<span data-ttu-id="a064e-135">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="a064e-135">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="a064e-136">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="a064e-136">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="a064e-137">GetUserOofSettingsResponse</span><span class="sxs-lookup"><span data-stu-id="a064e-137">GetUserOofSettingsResponse</span></span>](getuseroofsettingsresponse.md)
    
- [<span data-ttu-id="a064e-138">ResponseMessage</span><span class="sxs-lookup"><span data-stu-id="a064e-138">ResponseMessage</span></span>](responsemessage.md)
    
- [<span data-ttu-id="a064e-139">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="a064e-139">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="a064e-140">OofSettings</span><span class="sxs-lookup"><span data-stu-id="a064e-140">OofSettings</span></span>](oofsettings.md)
    
- [<span data-ttu-id="a064e-141">OofState</span><span class="sxs-lookup"><span data-stu-id="a064e-141">OofState</span></span>](oofstate.md)
    
- [<span data-ttu-id="a064e-142">ExternalAudience</span><span class="sxs-lookup"><span data-stu-id="a064e-142">ExternalAudience</span></span>](externalaudience.md)
    
- [<span data-ttu-id="a064e-143">Duración (UserOofSettings)</span><span class="sxs-lookup"><span data-stu-id="a064e-143">Duration (UserOofSettings)</span></span>](duration-useroofsettings.md)
    
- [<span data-ttu-id="a064e-144">StartTime</span><span class="sxs-lookup"><span data-stu-id="a064e-144">StartTime</span></span>](starttime.md)
    
- [<span data-ttu-id="a064e-145">EndTime</span><span class="sxs-lookup"><span data-stu-id="a064e-145">EndTime</span></span>](endtime.md)
    
- [<span data-ttu-id="a064e-146">InternalReply</span><span class="sxs-lookup"><span data-stu-id="a064e-146">InternalReply</span></span>](internalreply.md)
    
- [<span data-ttu-id="a064e-147">ExternalReply</span><span class="sxs-lookup"><span data-stu-id="a064e-147">ExternalReply</span></span>](externalreply.md)
    
- [<span data-ttu-id="a064e-148">Message</span><span class="sxs-lookup"><span data-stu-id="a064e-148">Message</span></span>](message-ex15websvcsotherref.md)
    
- [<span data-ttu-id="a064e-149">AllowExternalOof</span><span class="sxs-lookup"><span data-stu-id="a064e-149">AllowExternalOof</span></span>](allowexternaloof.md)
    
## <a name="getuseroofsettings-error-response-example"></a><span data-ttu-id="a064e-150">Ejemplo de respuesta de error GetUserOofSettings</span><span class="sxs-lookup"><span data-stu-id="a064e-150">GetUserOofSettings Error response example</span></span>

### <a name="description"></a><span data-ttu-id="a064e-151">Description</span><span class="sxs-lookup"><span data-stu-id="a064e-151">Description</span></span>

<span data-ttu-id="a064e-152">En el ejemplo siguiente se muestra una respuesta de error causada por un intento de acceder a la información de OOF de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="a064e-152">The following example shows an error response caused by an attempt to access another user's OOF information.</span></span>
  
### <a name="code"></a><span data-ttu-id="a064e-153">Código</span><span class="sxs-lookup"><span data-stu-id="a064e-153">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <soap:Fault>
      <faultcode>soap:Client</faultcode>
      <faultstring>Microsoft.Exchange.Data.Storage.AccessDeniedException: User is not mailbox owner. User = S-1-5-21-3642464542-282065186-3871681729-1155, MailboxGuid = S-1-5-21-3642464542-282065186-3871681729-1156 ---> User is not mailbox owner. </faultstring>
      <faultactor>https://CAS01.example.com/EWS/Exchange.asmx</faultactor>
      <detail>
        <ErrorCode xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">-2146233088</ErrorCode>
      </detail>
    </soap:Fault>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="a064e-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="a064e-154">See also</span></span>



- [<span data-ttu-id="a064e-155">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="a064e-155">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

