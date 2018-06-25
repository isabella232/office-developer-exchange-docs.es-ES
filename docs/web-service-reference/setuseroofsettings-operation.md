---
title: Operación SetUserOofSettings
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SetUserOofSettings
api_type:
- schema
ms.assetid: 36277ef0-18ee-4b35-9e6e-8c321d8f5433
description: El método SetUserOofSettings Web establece la configuración de fuera de oficina (OOF) y el mensaje de un usuario de buzón de correo.
ms.openlocfilehash: 51c2f9488f38a4adb0e291c11adc2ebfe3426f25
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837469"
---
# <a name="setuseroofsettings-operation"></a><span data-ttu-id="2a81e-103">Operación SetUserOofSettings</span><span class="sxs-lookup"><span data-stu-id="2a81e-103">SetUserOofSettings operation</span></span>

<span data-ttu-id="2a81e-104">El método Web **SetUserOofSettings** establece la configuración de fuera de oficina (OOF) y el mensaje de un usuario de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="2a81e-104">The **SetUserOofSettings** Web method sets a mailbox user's Out of Office (OOF) settings and message.</span></span> 
  
## <a name="soap-headers"></a><span data-ttu-id="2a81e-105">Encabezados SOAP</span><span class="sxs-lookup"><span data-stu-id="2a81e-105">SOAP Headers</span></span>

<span data-ttu-id="2a81e-106">La operación de **SetUserOofSettings** puede utilizar los encabezados SOAP que se enumeran y describen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="2a81e-106">The **SetUserOofSettings** operation can use the SOAP headers that are listed and described in the following table.</span></span> 
  
|<span data-ttu-id="2a81e-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="2a81e-107">**Header**</span></span>|<span data-ttu-id="2a81e-108">**Element**</span><span class="sxs-lookup"><span data-stu-id="2a81e-108">**Element**</span></span>|<span data-ttu-id="2a81e-109">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2a81e-109">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2a81e-110">Suplantación</span><span class="sxs-lookup"><span data-stu-id="2a81e-110">Impersonation</span></span>  <br/> |[<span data-ttu-id="2a81e-111">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="2a81e-111">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="2a81e-112">Identifica el usuario que está realizando la suplantación de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="2a81e-112">Identifies the user whom the client application is impersonating.</span></span>  <br/> |
|<span data-ttu-id="2a81e-113">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="2a81e-113">ServerVersion</span></span>  <br/> |[<span data-ttu-id="2a81e-114">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="2a81e-114">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="2a81e-115">Identifica la versión del servidor que ha respondido a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2a81e-115">Identifies the version of the server that responded to the request.</span></span>  <br/> |
   
## <a name="setuseroofsettings-request-example"></a><span data-ttu-id="2a81e-116">Ejemplo de solicitud de SetUserOofSettings</span><span class="sxs-lookup"><span data-stu-id="2a81e-116">SetUserOofSettings request example</span></span>

### <a name="description"></a><span data-ttu-id="2a81e-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="2a81e-117">Description</span></span>

<span data-ttu-id="2a81e-118">El siguiente ejemplo de una solicitud de **SetUserOofSettings** establece un valor de OOF durante 10 días.</span><span class="sxs-lookup"><span data-stu-id="2a81e-118">The following example of a **SetUserOofSettings** request sets an OOF setting for 10 days.</span></span> 
  
### <a name="code"></a><span data-ttu-id="2a81e-119">Código</span><span class="sxs-lookup"><span data-stu-id="2a81e-119">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetUserOofSettingsRequest xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <Mailbox xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
        <Name>User1</Name>
        <Address>user1@example.com</Address>
        <RoutingType>SMTP</RoutingType>
      </Mailbox>
      <UserOofSettings xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
        <OofState>Enabled</OofState>
        <ExternalAudience>All</ExternalAudience>
        <Duration>
          <StartTime>2006-10-05T00:00:00</StartTime>
          <EndTime>2006-10-25T00:00:00</EndTime>
        </Duration>
        <InternalReply>
          <Message>I am out of office.  This is my internal reply.</Message>
        </InternalReply>
        <ExternalReply>
          <Message>I am out of office. This is my external reply.</Message>
        </ExternalReply>
      </UserOofSettings>
    </SetUserOofSettingsRequest>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a><span data-ttu-id="2a81e-120">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="2a81e-120">Request elements</span></span>

<span data-ttu-id="2a81e-121">En la solicitud se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="2a81e-121">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="2a81e-122">SetUserOofSettingsRequest</span><span class="sxs-lookup"><span data-stu-id="2a81e-122">SetUserOofSettingsRequest</span></span>](setuseroofsettingsrequest.md)
    
- [<span data-ttu-id="2a81e-123">Buzón de correo (disponibilidad)</span><span class="sxs-lookup"><span data-stu-id="2a81e-123">Mailbox (Availability)</span></span>](mailbox-availability.md)
    
- [<span data-ttu-id="2a81e-124">Nombre (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="2a81e-124">Name (EmailAddress)</span></span>](name-emailaddress.md)
    
- [<span data-ttu-id="2a81e-125">Dirección (cadena)</span><span class="sxs-lookup"><span data-stu-id="2a81e-125">Address (string)</span></span>](address-string.md)
    
- [<span data-ttu-id="2a81e-126">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="2a81e-126">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md)
    
- [<span data-ttu-id="2a81e-127">UserOofSettings</span><span class="sxs-lookup"><span data-stu-id="2a81e-127">UserOofSettings</span></span>](useroofsettings.md)
    
- [<span data-ttu-id="2a81e-128">OofState</span><span class="sxs-lookup"><span data-stu-id="2a81e-128">OofState</span></span>](oofstate.md)
    
- [<span data-ttu-id="2a81e-129">ExternalAudience</span><span class="sxs-lookup"><span data-stu-id="2a81e-129">ExternalAudience</span></span>](externalaudience.md)
    
- [<span data-ttu-id="2a81e-130">Duración (UserOofSettings)</span><span class="sxs-lookup"><span data-stu-id="2a81e-130">Duration (UserOofSettings)</span></span>](duration-useroofsettings.md)
    
- [<span data-ttu-id="2a81e-131">StartTime</span><span class="sxs-lookup"><span data-stu-id="2a81e-131">StartTime</span></span>](starttime.md)
    
- [<span data-ttu-id="2a81e-132">Hora de finalización</span><span class="sxs-lookup"><span data-stu-id="2a81e-132">EndTime</span></span>](endtime.md)
    
- [<span data-ttu-id="2a81e-133">InternalReply</span><span class="sxs-lookup"><span data-stu-id="2a81e-133">InternalReply</span></span>](internalreply.md)
    
- [<span data-ttu-id="2a81e-134">Mensaje (disponibilidad)</span><span class="sxs-lookup"><span data-stu-id="2a81e-134">Message (Availability)</span></span>](message-availability.md)
    
- [<span data-ttu-id="2a81e-135">ExternalReply</span><span class="sxs-lookup"><span data-stu-id="2a81e-135">ExternalReply</span></span>](externalreply.md)
    
## <a name="successful-setuseroofsettings-response-example"></a><span data-ttu-id="2a81e-136">Ejemplo de respuesta correcta de SetUserOofSettings</span><span class="sxs-lookup"><span data-stu-id="2a81e-136">Successful SetUserOofSettings response example</span></span>

### <a name="description"></a><span data-ttu-id="2a81e-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="2a81e-137">Description</span></span>

<span data-ttu-id="2a81e-138">En el ejemplo siguiente se muestra una respuesta correcta a la solicitud de **SetUserOofSettings** .</span><span class="sxs-lookup"><span data-stu-id="2a81e-138">The following example shows a successful response to the **SetUserOofSettings** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="2a81e-139">Código</span><span class="sxs-lookup"><span data-stu-id="2a81e-139">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" /> 
  </soap:Header>
  <soap:Body>
    <SetUserOofSettingsResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseMessage ResponseClass="Success">
        <ResponseCode>NoError</ResponseCode> 
      </ResponseMessage>
    </SetUserOofSettingsResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-response-elements"></a><span data-ttu-id="2a81e-140">Elementos de respuesta correcta</span><span class="sxs-lookup"><span data-stu-id="2a81e-140">Successful response elements</span></span>

<span data-ttu-id="2a81e-141">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="2a81e-141">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="2a81e-142">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="2a81e-142">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="2a81e-143">SetUserOofSettingsResponse</span><span class="sxs-lookup"><span data-stu-id="2a81e-143">SetUserOofSettingsResponse</span></span>](setuseroofsettingsresponse.md)
    
- [<span data-ttu-id="2a81e-144">ResponseMessage</span><span class="sxs-lookup"><span data-stu-id="2a81e-144">ResponseMessage</span></span>](responsemessage.md)
    
- [<span data-ttu-id="2a81e-145">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="2a81e-145">ResponseCode</span></span>](responsecode.md)
    
## <a name="see-also"></a><span data-ttu-id="2a81e-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="2a81e-146">See also</span></span>



- [<span data-ttu-id="2a81e-147">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="2a81e-147">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

