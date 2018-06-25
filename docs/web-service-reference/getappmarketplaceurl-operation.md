---
title: Operación GetAppMarketplaceUrl
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2c016fc3-0e13-4624-9a5b-d3e84577a860
description: Busque información sobre la EWS GetAppMarketplaceUrl operación.
ms.openlocfilehash: 616e7f571ba5283a773e51d611cd18bb37b5bc8b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764747"
---
# <a name="getappmarketplaceurl-operation"></a><span data-ttu-id="2cbf2-103">Operación GetAppMarketplaceUrl</span><span class="sxs-lookup"><span data-stu-id="2cbf2-103">GetAppMarketplaceUrl operation</span></span>

<span data-ttu-id="2cbf2-104">Obtenga información acerca de la operación de EWS **GetAppMarketplaceUrl** .</span><span class="sxs-lookup"><span data-stu-id="2cbf2-104">Find information about the **GetAppMarketplaceUrl** EWS operation.</span></span> 
  
<span data-ttu-id="2cbf2-105">La operación **GetAppMarketplaceUrl** recupera la dirección URL para el catálogo de soluciones de aplicación que un cliente puede visitar para adquirir aplicaciones para instalar en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="2cbf2-105">The **GetAppMarketplaceUrl** operation retrieves the URL for the app marketplace that a client can visit to acquire apps to install in a mailbox.</span></span> 
  
<span data-ttu-id="2cbf2-106">Esta operación se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="2cbf2-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getappmarketplaceurl-operation"></a><span data-ttu-id="2cbf2-107">Mediante la operación GetAppMarketplaceUrl</span><span class="sxs-lookup"><span data-stu-id="2cbf2-107">Using the GetAppMarketplaceUrl operation</span></span>

<span data-ttu-id="2cbf2-108">La operación **GetAppMarketplaceUrl** no toma ningún argumento para solicitar la dirección URL para el catálogo de soluciones desde la que un cliente puede instalar aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="2cbf2-108">The **GetAppMarketplaceUrl** operation does not take any arguments to request the URL for the marketplace from which a client can install apps.</span></span> <span data-ttu-id="2cbf2-109">La respuesta contendrá una dirección URL para el catálogo de soluciones de aplicación.</span><span class="sxs-lookup"><span data-stu-id="2cbf2-109">The response will contain a URL to the app marketplace.</span></span> 
  
### <a name="getappmarketplaceurl-operation-soap-headers"></a><span data-ttu-id="2cbf2-110">Encabezados SOAP de operación de GetAppMarketplaceUrl</span><span class="sxs-lookup"><span data-stu-id="2cbf2-110">GetAppMarketplaceUrl operation SOAP headers</span></span>

<span data-ttu-id="2cbf2-111">La operación de **GetAppMarketplaceUrl** puede utilizar los encabezados SOAP que se enumeran en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="2cbf2-111">The **GetAppMarketplaceUrl** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="2cbf2-112">**Nombre de encabezado**</span><span class="sxs-lookup"><span data-stu-id="2cbf2-112">**Header name**</span></span>|<span data-ttu-id="2cbf2-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="2cbf2-113">**Element**</span></span>|<span data-ttu-id="2cbf2-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2cbf2-114">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2cbf2-115">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="2cbf2-115">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="2cbf2-116">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="2cbf2-116">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="2cbf2-117">Identifica la versión del esquema para la solicitud de la operación.</span><span class="sxs-lookup"><span data-stu-id="2cbf2-117">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="2cbf2-118">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="2cbf2-118">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="2cbf2-119">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="2cbf2-119">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="2cbf2-120">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="2cbf2-120">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="2cbf2-121">Identifica la versión del servidor que ha respondido a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2cbf2-121">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="2cbf2-122">Este encabezado es aplicable a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="2cbf2-122">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getappmarketplaceurl-operation-request-example-get-the-app-marketplace-url-for-a-mailbox"></a><span data-ttu-id="2cbf2-123">Ejemplo de solicitud de operación de GetAppMarketplaceUrl: obtener la dirección URL de catálogo de soluciones de aplicación para un buzón de correo</span><span class="sxs-lookup"><span data-stu-id="2cbf2-123">GetAppMarketplaceUrl operation request example: Get the app marketplace URL for a mailbox</span></span>

<span data-ttu-id="2cbf2-124">El siguiente ejemplo de una solicitud de operación **GetAppMarketplaceUrl** muestra cómo obtener la dirección URL de catálogo de soluciones de aplicación para un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="2cbf2-124">The following example of a **GetAppMarketplaceUrl** operation request shows how to get the app marketplace URL for a mailbox.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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

<span data-ttu-id="2cbf2-125">La solicitud SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="2cbf2-125">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="2cbf2-126">GetAppMarketplaceUrl</span><span class="sxs-lookup"><span data-stu-id="2cbf2-126">GetAppMarketplaceUrl</span></span>](getappmarketplaceurl.md)
    
- [<span data-ttu-id="2cbf2-127">ApiVersionSupported</span><span class="sxs-lookup"><span data-stu-id="2cbf2-127">ApiVersionSupported</span></span>](apiversionsupported.md)
    
- [<span data-ttu-id="2cbf2-128">SchemaVersionSupported</span><span class="sxs-lookup"><span data-stu-id="2cbf2-128">SchemaVersionSupported</span></span>](schemaversionsupported.md)
    
## <a name="successful-getappmarketplaceurl-operation-response"></a><span data-ttu-id="2cbf2-129">Respuesta es correcta de operación GetAppMarketplaceUrl</span><span class="sxs-lookup"><span data-stu-id="2cbf2-129">Successful GetAppMarketplaceUrl operation response</span></span>

<span data-ttu-id="2cbf2-130">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación **GetAppMarketplaceUrl** para obtener la dirección URL de catálogo de soluciones de aplicación para un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="2cbf2-130">The following example shows a successful response to a **GetAppMarketplaceUrl** operation request to get the app marketplace URL for a mailbox.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="2cbf2-131">La dirección URL de catálogo de soluciones de aplicación se ha modificado para conservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="2cbf2-131">The app marketplace URL has been altered to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="918" 
                           MinorBuildNumber="7" 
                           Version="V2_10" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetAppMarketplaceUrlResponse ResponseClass="Success" 
                                    xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <AppMarketplaceUrl>http://marketplace.contoso.com</AppMarketplaceUrl>
      </GetAppMarketplaceUrlResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="2cbf2-132">La respuesta SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="2cbf2-132">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="2cbf2-133">GetAppMarketplaceUrlResponse</span><span class="sxs-lookup"><span data-stu-id="2cbf2-133">GetAppMarketplaceUrlResponse</span></span>](getappmarketplaceurlresponse.md)
    
- [<span data-ttu-id="2cbf2-134">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="2cbf2-134">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="2cbf2-135">AppMarketplaceUrl</span><span class="sxs-lookup"><span data-stu-id="2cbf2-135">AppMarketplaceUrl</span></span>](appmarketplaceurl.md)
    
## <a name="getappmarketplaceurl-operation-error-response"></a><span data-ttu-id="2cbf2-136">Respuesta de error de la operación de GetAppMarketPlaceUrl</span><span class="sxs-lookup"><span data-stu-id="2cbf2-136">GetAppMarketPlaceUrl operation error response</span></span>

<span data-ttu-id="2cbf2-137">Los errores devueltos para esta operación ya sea relacionados con la configuración de un servicio incorrecto o son los errores EWS genéricos.</span><span class="sxs-lookup"><span data-stu-id="2cbf2-137">Errors returned for this operation are either related to an incorrect service configuration or are generic EWS errors.</span></span> <span data-ttu-id="2cbf2-138">Para códigos de error que son genéricos para EWS y específicos de esta operación, vea [ResponseCode](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="2cbf2-138">For error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span> 
  
<span data-ttu-id="2cbf2-139">En el ejemplo siguiente se muestra una respuesta de error que se devuelve al Panel de Control externo de Exchange (ECP) no está configurado.</span><span class="sxs-lookup"><span data-stu-id="2cbf2-139">The following example shows an error response that is returned when external Exchange Control Panel (ECP) is not configured.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="918" 
                           MinorBuildNumber="7" 
                           Version="V2_10" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetAppMarketplaceUrlResponse ResponseClass="Error" 
                                    xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>Cannot get external ECP URL. This might happen if external ECP URL isn't configured.</MessageText>
         <ResponseCode>ErrorCannotGetExternalEcpUrl</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </GetAppMarketplaceUrlResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="2cbf2-140">La respuesta de error SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="2cbf2-140">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="2cbf2-141">GetAppMarketplaceUrlResponse</span><span class="sxs-lookup"><span data-stu-id="2cbf2-141">GetAppMarketplaceUrlResponse</span></span>](getappmarketplaceurlresponse.md)
    
- [<span data-ttu-id="2cbf2-142">MessageText</span><span class="sxs-lookup"><span data-stu-id="2cbf2-142">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="2cbf2-143">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="2cbf2-143">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="2cbf2-144">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="2cbf2-144">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="2cbf2-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="2cbf2-145">See also</span></span>

- [<span data-ttu-id="2cbf2-146">Operaciones de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="2cbf2-146">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="2cbf2-147">Operación DisableApp</span><span class="sxs-lookup"><span data-stu-id="2cbf2-147">DisableApp operation</span></span>](disableapp-operation.md)
    
- [<span data-ttu-id="2cbf2-148">Operación InstallApp</span><span class="sxs-lookup"><span data-stu-id="2cbf2-148">InstallApp operation</span></span>](installapp-operation.md)
    
- [<span data-ttu-id="2cbf2-149">Operación UninstallApp</span><span class="sxs-lookup"><span data-stu-id="2cbf2-149">UninstallApp operation</span></span>](uninstallapp-operation.md)
    
- [<span data-ttu-id="2cbf2-150">Operación GetAppManifests</span><span class="sxs-lookup"><span data-stu-id="2cbf2-150">GetAppManifests operation</span></span>](getappmanifests-operation.md)
    

