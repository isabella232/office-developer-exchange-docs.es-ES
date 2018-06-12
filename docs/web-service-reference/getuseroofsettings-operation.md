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
description: La operación GetUserOofSettings Obtiene la configuración de fuera de oficina (OOF) y los mensajes de un usuario de buzón de correo.
ms.openlocfilehash: 75a734999842cc33c213e02dc114f23372ae51fd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19835691"
---
# <a name="getuseroofsettings-operation"></a><span data-ttu-id="04bb1-103">Operación GetUserOofSettings</span><span class="sxs-lookup"><span data-stu-id="04bb1-103">GetUserOofSettings operation</span></span>

<span data-ttu-id="04bb1-104">La operación **GetUserOofSettings** Obtiene la configuración de fuera de oficina (OOF) y los mensajes de un usuario de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="04bb1-104">The **GetUserOofSettings** operation gets a mailbox user's Out of Office (OOF) settings and messages.</span></span> 
  
## <a name="soap-headers"></a><span data-ttu-id="04bb1-105">Encabezados SOAP</span><span class="sxs-lookup"><span data-stu-id="04bb1-105">SOAP Headers</span></span>

<span data-ttu-id="04bb1-106">La operación de **GetUserOofSettings** puede utilizar los encabezados SOAP que se enumeran y describen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="04bb1-106">The **GetUserOofSettings** operation can use the SOAP headers that are listed and described in the following table.</span></span> 
  
|<span data-ttu-id="04bb1-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="04bb1-107">**Header**</span></span>|<span data-ttu-id="04bb1-108">**Element**</span><span class="sxs-lookup"><span data-stu-id="04bb1-108">**Element**</span></span>|<span data-ttu-id="04bb1-109">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="04bb1-109">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="04bb1-110">Suplantación</span><span class="sxs-lookup"><span data-stu-id="04bb1-110">Impersonation</span></span>  <br/> |[<span data-ttu-id="04bb1-111">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="04bb1-111">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="04bb1-112">Identifica el usuario que está realizando la suplantación de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="04bb1-112">Identifies the user whom the client application is impersonating.</span></span>  <br/> |
|<span data-ttu-id="04bb1-113">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="04bb1-113">ServerVersion</span></span>  <br/> |[<span data-ttu-id="04bb1-114">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="04bb1-114">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="04bb1-115">Identifica la versión del servidor que ha respondido a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="04bb1-115">Identifies the version of the server that responded to the request.</span></span>  <br/> |
   
## <a name="using-the-getuseroofsettings-operation"></a><span data-ttu-id="04bb1-116">Mediante la operación GetUserOofSettings</span><span class="sxs-lookup"><span data-stu-id="04bb1-116">Using the GetUserOofSettings Operation</span></span>

<span data-ttu-id="04bb1-117">La operación **GetUserOofSettings** proporciona acceso a la configuración de fuera de la oficina de un usuario.</span><span class="sxs-lookup"><span data-stu-id="04bb1-117">The **GetUserOofSettings** operation provides access to a user's OOF settings.</span></span> <span data-ttu-id="04bb1-118">Un usuario se identifica mediante la dirección de correo electrónico del usuario.</span><span class="sxs-lookup"><span data-stu-id="04bb1-118">A user is identified by the user's email address.</span></span> <span data-ttu-id="04bb1-119">Si el mensaje de fuera de la oficina es null y OOF está habilitado, no se envía ningún mensaje de fuera de la oficina.</span><span class="sxs-lookup"><span data-stu-id="04bb1-119">If the OOF message is null and OOF is enabled, no OOF message is sent.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="04bb1-120">Si los mensajes de fuera de la oficina se establecen por MicrosoftOfficeOutlook, esta operación devolverá los mensajes de fuera de la oficina en formato HTML.</span><span class="sxs-lookup"><span data-stu-id="04bb1-120">If the OOF messages are set by MicrosoftOfficeOutlook, this operation will return the OOF messages in HTML format.</span></span> 
  
## <a name="getuseroofsettings-request-example"></a><span data-ttu-id="04bb1-121">Ejemplo de solicitud de GetUserOofSettings</span><span class="sxs-lookup"><span data-stu-id="04bb1-121">GetUserOofSettings request example</span></span>

### <a name="description"></a><span data-ttu-id="04bb1-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="04bb1-122">Description</span></span>

<span data-ttu-id="04bb1-123">En el ejemplo siguiente se muestra una solicitud de **GetUserOofSettings** que obtiene información de fuera de la oficina de un único usuario.</span><span class="sxs-lookup"><span data-stu-id="04bb1-123">The following example shows a **GetUserOofSettings** request that gets a single user's OOF information.</span></span> 
  
### <a name="code"></a><span data-ttu-id="04bb1-124">Código</span><span class="sxs-lookup"><span data-stu-id="04bb1-124">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetUserOofSettingsRequest xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <Mailbox xmlns ="http://schemas.microsoft.com/exchange/services/2006/types">
        <Address>User1@example.com</Address>
      </Mailbox>
    </GetUserOofSettingsRequest>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a><span data-ttu-id="04bb1-125">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="04bb1-125">Request elements</span></span>

<span data-ttu-id="04bb1-126">En la solicitud se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="04bb1-126">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="04bb1-127">GetUserOofSettingsRequest</span><span class="sxs-lookup"><span data-stu-id="04bb1-127">GetUserOofSettingsRequest</span></span>](getuseroofsettingsrequest.md)
    
- [<span data-ttu-id="04bb1-128">Buzón de correo (disponibilidad)</span><span class="sxs-lookup"><span data-stu-id="04bb1-128">Mailbox (Availability)</span></span>](mailbox-availability.md)
    
- [<span data-ttu-id="04bb1-129">Dirección (cadena)</span><span class="sxs-lookup"><span data-stu-id="04bb1-129">Address (string)</span></span>](address-string.md)
    
## <a name="successful-getuseroofsettings-response-example"></a><span data-ttu-id="04bb1-130">Ejemplo de respuesta correcta de GetUserOofSettings</span><span class="sxs-lookup"><span data-stu-id="04bb1-130">Successful GetUserOofSettings response example</span></span>

### <a name="description"></a><span data-ttu-id="04bb1-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="04bb1-131">Description</span></span>

<span data-ttu-id="04bb1-132">En el ejemplo siguiente se muestra un estado OOF deshabilitado con los mensajes de fuera de la oficina.</span><span class="sxs-lookup"><span data-stu-id="04bb1-132">The following example shows a disabled OOF state with the OOF messages.</span></span>
  
### <a name="code"></a><span data-ttu-id="04bb1-133">Código</span><span class="sxs-lookup"><span data-stu-id="04bb1-133">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetUserOofSettingsResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseMessage ResponseClass="Success">
        <ResponseCode>NoError</ResponseCode>
      </ResponseMessage>
      <OofSettings xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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

### <a name="successful-getuseroofsettings-response-elements"></a><span data-ttu-id="04bb1-134">Elementos de respuesta correctos de GetUserOofSettings</span><span class="sxs-lookup"><span data-stu-id="04bb1-134">Successful GetUserOofSettings response elements</span></span>

<span data-ttu-id="04bb1-135">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="04bb1-135">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="04bb1-136">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="04bb1-136">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="04bb1-137">GetUserOofSettingsResponse</span><span class="sxs-lookup"><span data-stu-id="04bb1-137">GetUserOofSettingsResponse</span></span>](getuseroofsettingsresponse.md)
    
- [<span data-ttu-id="04bb1-138">ResponseMessage</span><span class="sxs-lookup"><span data-stu-id="04bb1-138">ResponseMessage</span></span>](responsemessage.md)
    
- [<span data-ttu-id="04bb1-139">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="04bb1-139">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="04bb1-140">OofSettings</span><span class="sxs-lookup"><span data-stu-id="04bb1-140">OofSettings</span></span>](oofsettings.md)
    
- [<span data-ttu-id="04bb1-141">OofState</span><span class="sxs-lookup"><span data-stu-id="04bb1-141">OofState</span></span>](oofstate.md)
    
- [<span data-ttu-id="04bb1-142">ExternalAudience</span><span class="sxs-lookup"><span data-stu-id="04bb1-142">ExternalAudience</span></span>](externalaudience.md)
    
- [<span data-ttu-id="04bb1-143">Duración (UserOofSettings)</span><span class="sxs-lookup"><span data-stu-id="04bb1-143">Duration (UserOofSettings)</span></span>](duration-useroofsettings.md)
    
- [<span data-ttu-id="04bb1-144">StartTime</span><span class="sxs-lookup"><span data-stu-id="04bb1-144">StartTime</span></span>](starttime.md)
    
- [<span data-ttu-id="04bb1-145">Hora de finalización</span><span class="sxs-lookup"><span data-stu-id="04bb1-145">EndTime</span></span>](endtime.md)
    
- [<span data-ttu-id="04bb1-146">InternalReply</span><span class="sxs-lookup"><span data-stu-id="04bb1-146">InternalReply</span></span>](internalreply.md)
    
- [<span data-ttu-id="04bb1-147">ExternalReply</span><span class="sxs-lookup"><span data-stu-id="04bb1-147">ExternalReply</span></span>](externalreply.md)
    
- [<span data-ttu-id="04bb1-148">Message</span><span class="sxs-lookup"><span data-stu-id="04bb1-148">Message</span></span>](message-ex15websvcsotherref.md)
    
- [<span data-ttu-id="04bb1-149">AllowExternalOof</span><span class="sxs-lookup"><span data-stu-id="04bb1-149">AllowExternalOof</span></span>](allowexternaloof.md)
    
## <a name="getuseroofsettings-error-response-example"></a><span data-ttu-id="04bb1-150">Ejemplo de respuesta de GetUserOofSettings Error</span><span class="sxs-lookup"><span data-stu-id="04bb1-150">GetUserOofSettings Error response example</span></span>

### <a name="description"></a><span data-ttu-id="04bb1-151">Descripción</span><span class="sxs-lookup"><span data-stu-id="04bb1-151">Description</span></span>

<span data-ttu-id="04bb1-152">En el ejemplo siguiente se muestra una respuesta de error debida a un intento de acceso a la información de fuera de la oficina de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="04bb1-152">The following example shows an error response caused by an attempt to access another user's OOF information.</span></span>
  
### <a name="code"></a><span data-ttu-id="04bb1-153">Código</span><span class="sxs-lookup"><span data-stu-id="04bb1-153">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <soap:Fault>
      <faultcode>soap:Client</faultcode>
      <faultstring>Microsoft.Exchange.Data.Storage.AccessDeniedException: User is not mailbox owner. User = S-1-5-21-3642464542-282065186-3871681729-1155, MailboxGuid = S-1-5-21-3642464542-282065186-3871681729-1156 ---> User is not mailbox owner. </faultstring>
      <faultactor>https://CAS01.example.com/EWS/Exchange.asmx</faultactor>
      <detail>
        <ErrorCode xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">-2146233088</ErrorCode>
      </detail>
    </soap:Fault>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="04bb1-154">Ver también</span><span class="sxs-lookup"><span data-stu-id="04bb1-154">See also</span></span>



- [<span data-ttu-id="04bb1-155">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="04bb1-155">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

