---
title: Operación GetAppMarketplaceUrl
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2c016fc3-0e13-4624-9a5b-d3e84577a860
description: Buscar información sobre la operación de EWS de GetAppMarketplaceUrl.
ms.openlocfilehash: 6797af44c3aaa6653c440b3d53a282d8c90a4381
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459528"
---
# <a name="getappmarketplaceurl-operation"></a><span data-ttu-id="fbc57-103">Operación GetAppMarketplaceUrl</span><span class="sxs-lookup"><span data-stu-id="fbc57-103">GetAppMarketplaceUrl operation</span></span>

<span data-ttu-id="fbc57-104">Buscar información sobre la operación de EWS de **GetAppMarketplaceUrl** .</span><span class="sxs-lookup"><span data-stu-id="fbc57-104">Find information about the **GetAppMarketplaceUrl** EWS operation.</span></span> 
  
<span data-ttu-id="fbc57-105">La operación **GetAppMarketplaceUrl** recupera la dirección URL del Marketplace de aplicaciones que un cliente puede visitar para adquirir aplicaciones que se van a instalar en un buzón.</span><span class="sxs-lookup"><span data-stu-id="fbc57-105">The **GetAppMarketplaceUrl** operation retrieves the URL for the app marketplace that a client can visit to acquire apps to install in a mailbox.</span></span> 
  
<span data-ttu-id="fbc57-106">Esta operación se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="fbc57-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getappmarketplaceurl-operation"></a><span data-ttu-id="fbc57-107">Uso de la operación GetAppMarketplaceUrl</span><span class="sxs-lookup"><span data-stu-id="fbc57-107">Using the GetAppMarketplaceUrl operation</span></span>

<span data-ttu-id="fbc57-108">La operación **GetAppMarketplaceUrl** no toma ningún argumento para solicitar la dirección URL del mercado desde el que un cliente puede instalar aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="fbc57-108">The **GetAppMarketplaceUrl** operation does not take any arguments to request the URL for the marketplace from which a client can install apps.</span></span> <span data-ttu-id="fbc57-109">La respuesta contendrá una dirección URL para el Marketplace de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="fbc57-109">The response will contain a URL to the app marketplace.</span></span> 
  
### <a name="getappmarketplaceurl-operation-soap-headers"></a><span data-ttu-id="fbc57-110">Encabezados SOAP de operación GetAppMarketplaceUrl</span><span class="sxs-lookup"><span data-stu-id="fbc57-110">GetAppMarketplaceUrl operation SOAP headers</span></span>

<span data-ttu-id="fbc57-111">La operación **GetAppMarketplaceUrl** puede usar los encabezados SOAP que se enumeran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="fbc57-111">The **GetAppMarketplaceUrl** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="fbc57-112">**Nombre de encabezado**</span><span class="sxs-lookup"><span data-stu-id="fbc57-112">**Header name**</span></span>|<span data-ttu-id="fbc57-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="fbc57-113">**Element**</span></span>|<span data-ttu-id="fbc57-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fbc57-114">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fbc57-115">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="fbc57-115">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="fbc57-116">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="fbc57-116">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="fbc57-117">Identifica la versión del esquema para la solicitud de operación.</span><span class="sxs-lookup"><span data-stu-id="fbc57-117">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="fbc57-118">Este encabezado se aplica a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="fbc57-118">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="fbc57-119">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="fbc57-119">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="fbc57-120">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="fbc57-120">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="fbc57-121">Identifica la versión del servidor que respondió a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fbc57-121">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="fbc57-122">Este encabezado se aplica a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="fbc57-122">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getappmarketplaceurl-operation-request-example-get-the-app-marketplace-url-for-a-mailbox"></a><span data-ttu-id="fbc57-123">Ejemplo de solicitud de operación GetAppMarketplaceUrl: obtener la dirección URL del catálogo de soluciones de la aplicación para un buzón</span><span class="sxs-lookup"><span data-stu-id="fbc57-123">GetAppMarketplaceUrl operation request example: Get the app marketplace URL for a mailbox</span></span>

<span data-ttu-id="fbc57-124">El siguiente ejemplo de una solicitud de operación de **GetAppMarketplaceUrl** muestra cómo obtener la dirección URL del catálogo de soluciones de la aplicación de un buzón.</span><span class="sxs-lookup"><span data-stu-id="fbc57-124">The following example of a **GetAppMarketplaceUrl** operation request shows how to get the app marketplace URL for a mailbox.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013_SP1" />
      <t:MailboxCulture>en-US</t:MailboxCulture>
      <t:TimeZoneContext>
         <t:TimeZoneDefinition Id="GMT Standard Time"/>
      </t:TimeZoneContext>
   </soap:Header>
   <soap:Body >
      <m:GetAppMarketplaceUrl>
        <m:ApiVersionSupported>1.0</m:ApiVersionSupported>
        <m:SchemaVersionSupported>1.0</m:SchemaVersionSupported>
      </m:GetAppMarketplaceUrl>
   </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="fbc57-125">El cuerpo SOAP de la solicitud contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="fbc57-125">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="fbc57-126">GetAppMarketplaceUrl</span><span class="sxs-lookup"><span data-stu-id="fbc57-126">GetAppMarketplaceUrl</span></span>](getappmarketplaceurl.md)
    
- [<span data-ttu-id="fbc57-127">ApiVersionSupported</span><span class="sxs-lookup"><span data-stu-id="fbc57-127">ApiVersionSupported</span></span>](apiversionsupported.md)
    
- [<span data-ttu-id="fbc57-128">SchemaVersionSupported</span><span class="sxs-lookup"><span data-stu-id="fbc57-128">SchemaVersionSupported</span></span>](schemaversionsupported.md)
    
## <a name="successful-getappmarketplaceurl-operation-response"></a><span data-ttu-id="fbc57-129">Respuesta de operación GetAppMarketplaceUrl correcta</span><span class="sxs-lookup"><span data-stu-id="fbc57-129">Successful GetAppMarketplaceUrl operation response</span></span>

<span data-ttu-id="fbc57-130">En el siguiente ejemplo se muestra una respuesta correcta a una solicitud de operación de **GetAppMarketplaceUrl** para obtener la dirección URL del catálogo de soluciones de la aplicación de un buzón.</span><span class="sxs-lookup"><span data-stu-id="fbc57-130">The following example shows a successful response to a **GetAppMarketplaceUrl** operation request to get the app marketplace URL for a mailbox.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="fbc57-131">La dirección URL del catálogo de soluciones de la aplicación se ha modificado para preservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="fbc57-131">The app marketplace URL has been altered to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="918" 
                           MinorBuildNumber="7" 
                           Version="V2_10" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetAppMarketplaceUrlResponse ResponseClass="Success" 
                                    xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <AppMarketplaceUrl>http://marketplace.contoso.com</AppMarketplaceUrl>
      </GetAppMarketplaceUrlResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="fbc57-132">El cuerpo SOAP de respuesta contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="fbc57-132">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="fbc57-133">GetAppMarketplaceUrlResponse</span><span class="sxs-lookup"><span data-stu-id="fbc57-133">GetAppMarketplaceUrlResponse</span></span>](getappmarketplaceurlresponse.md)
    
- [<span data-ttu-id="fbc57-134">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="fbc57-134">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="fbc57-135">AppMarketplaceUrl</span><span class="sxs-lookup"><span data-stu-id="fbc57-135">AppMarketplaceUrl</span></span>](appmarketplaceurl.md)
    
## <a name="getappmarketplaceurl-operation-error-response"></a><span data-ttu-id="fbc57-136">Respuesta de error de operación de GetAppMarketPlaceUrl</span><span class="sxs-lookup"><span data-stu-id="fbc57-136">GetAppMarketPlaceUrl operation error response</span></span>

<span data-ttu-id="fbc57-137">Los errores devueltos para esta operación están relacionados con una configuración de servicio incorrecta o son errores genéricos de EWS.</span><span class="sxs-lookup"><span data-stu-id="fbc57-137">Errors returned for this operation are either related to an incorrect service configuration or are generic EWS errors.</span></span> <span data-ttu-id="fbc57-138">Para los códigos de error que son genéricos para EWS y específicos de esta operación, vea [ResponseCode](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="fbc57-138">For error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span> 
  
<span data-ttu-id="fbc57-139">En el ejemplo siguiente se muestra una respuesta de error que se devuelve cuando el panel de control de Exchange externo (ECP) no está configurado.</span><span class="sxs-lookup"><span data-stu-id="fbc57-139">The following example shows an error response that is returned when external Exchange Control Panel (ECP) is not configured.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="918" 
                           MinorBuildNumber="7" 
                           Version="V2_10" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetAppMarketplaceUrlResponse ResponseClass="Error" 
                                    xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>Cannot get external ECP URL. This might happen if external ECP URL isn't configured.</MessageText>
         <ResponseCode>ErrorCannotGetExternalEcpUrl</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </GetAppMarketplaceUrlResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="fbc57-140">El cuerpo SOAP de respuesta de error contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="fbc57-140">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="fbc57-141">GetAppMarketplaceUrlResponse</span><span class="sxs-lookup"><span data-stu-id="fbc57-141">GetAppMarketplaceUrlResponse</span></span>](getappmarketplaceurlresponse.md)
    
- [<span data-ttu-id="fbc57-142">MessageText</span><span class="sxs-lookup"><span data-stu-id="fbc57-142">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="fbc57-143">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="fbc57-143">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="fbc57-144">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="fbc57-144">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="fbc57-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="fbc57-145">See also</span></span>

- [<span data-ttu-id="fbc57-146">Operaciones de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="fbc57-146">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="fbc57-147">Operación DisableApp</span><span class="sxs-lookup"><span data-stu-id="fbc57-147">DisableApp operation</span></span>](disableapp-operation.md)
    
- [<span data-ttu-id="fbc57-148">Operación InstallApp</span><span class="sxs-lookup"><span data-stu-id="fbc57-148">InstallApp operation</span></span>](installapp-operation.md)
    
- [<span data-ttu-id="fbc57-149">Operación UninstallApp</span><span class="sxs-lookup"><span data-stu-id="fbc57-149">UninstallApp operation</span></span>](uninstallapp-operation.md)
    
- [<span data-ttu-id="fbc57-150">Operación GetAppManifests</span><span class="sxs-lookup"><span data-stu-id="fbc57-150">GetAppManifests operation</span></span>](getappmanifests-operation.md)
    

