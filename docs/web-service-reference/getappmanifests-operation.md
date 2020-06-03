---
title: Operación GetAppManifests
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 21a4987c-c24d-4a6e-ace4-e81edcda6303
description: Buscar información sobre la operación de EWS de GetAppManifests.
ms.openlocfilehash: 4d4c1d32f14cf144335ddfdf8c9cd4c88a4421d0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463009"
---
# <a name="getappmanifests-operation"></a><span data-ttu-id="4b464-103">Operación GetAppManifests</span><span class="sxs-lookup"><span data-stu-id="4b464-103">GetAppManifests operation</span></span>

<span data-ttu-id="4b464-104">Buscar información sobre la operación de EWS de **GetAppManifests** .</span><span class="sxs-lookup"><span data-stu-id="4b464-104">Find information about the **GetAppManifests** EWS operation.</span></span> 
  
<span data-ttu-id="4b464-105">La operación **GetAppManifests** recupera los manifiestos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4b464-105">The **GetAppManifests** operation retrieves app manifests.</span></span> 
  
<span data-ttu-id="4b464-106">Esta operación se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="4b464-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getappmanifests-operation"></a><span data-ttu-id="4b464-107">Uso de la operación GetAppManifests</span><span class="sxs-lookup"><span data-stu-id="4b464-107">Using the GetAppManifests operation</span></span>

<span data-ttu-id="4b464-108">La operación **GetAppManifests** no toma ningún argumento para solicitar los manifiestos de aplicación de un buzón.</span><span class="sxs-lookup"><span data-stu-id="4b464-108">The **GetAppManifests** operation does not take any arguments to request the app manifests for a mailbox.</span></span> <span data-ttu-id="4b464-109">La respuesta contendrá archivos de manifiesto XML codificados en base64 para cada aplicación que esté instalada en un buzón.</span><span class="sxs-lookup"><span data-stu-id="4b464-109">The response will contain base64-encoded XML manifest files for each app that is installed in a mailbox.</span></span> 
  
### <a name="getappmanifests-operation-soap-headers"></a><span data-ttu-id="4b464-110">Encabezados SOAP de operación GetAppManifests</span><span class="sxs-lookup"><span data-stu-id="4b464-110">GetAppManifests operation SOAP headers</span></span>

<span data-ttu-id="4b464-111">La operación **GetAppManifests** puede usar los encabezados SOAP que se enumeran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="4b464-111">The **GetAppManifests** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="4b464-112">**Nombre de encabezado**</span><span class="sxs-lookup"><span data-stu-id="4b464-112">**Header name**</span></span>|<span data-ttu-id="4b464-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="4b464-113">**Element**</span></span>|<span data-ttu-id="4b464-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4b464-114">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4b464-115">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="4b464-115">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="4b464-116">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="4b464-116">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="4b464-117">Identifica la versión del esquema para la solicitud de operación.</span><span class="sxs-lookup"><span data-stu-id="4b464-117">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="4b464-118">Este encabezado se aplica a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="4b464-118">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="4b464-119">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="4b464-119">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="4b464-120">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="4b464-120">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="4b464-121">Identifica la versión del servidor que respondió a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4b464-121">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="4b464-122">Este encabezado se aplica a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="4b464-122">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getappmanifests-operation-request-example-get-the-app-manifests-for-a-mailbox"></a><span data-ttu-id="4b464-123">Ejemplo de solicitud de operación GetAppManifests: obtener los manifiestos de aplicación de un buzón de correo</span><span class="sxs-lookup"><span data-stu-id="4b464-123">GetAppManifests operation request example: Get the app manifests for a mailbox</span></span>

<span data-ttu-id="4b464-124">El siguiente ejemplo de una solicitud de operación de **GetAppManifests** muestra cómo obtener los manifiestos de aplicación para un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="4b464-124">The following example of a **GetAppManifests** operation request shows how to get the app manifests for a mailbox.</span></span> <span data-ttu-id="4b464-125">El elemento [ApiVersionSupported](apiversionsupported.md) y el elemento [SchemaVersionSupported](schemaversionsupported.md) son opcionales.</span><span class="sxs-lookup"><span data-stu-id="4b464-125">The [ApiVersionSupported](apiversionsupported.md) element and the [SchemaVersionSupported](schemaversionsupported.md) element are optional.</span></span> 
  
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
      <m:GetAppManifests>
        <m:ApiVersionSupported>1.1</m:ApiVersionSupported>
        <m:SchemaVersionSupported>1.1</m:SchemaVersionSupported>
      </m:GetAppManifests>
   </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="4b464-126">El cuerpo SOAP de la solicitud contiene el siguiente elemento:</span><span class="sxs-lookup"><span data-stu-id="4b464-126">The request SOAP body contains the following element:</span></span>
  
- [<span data-ttu-id="4b464-127">GetAppManifests</span><span class="sxs-lookup"><span data-stu-id="4b464-127">GetAppManifests</span></span>](getappmanifests.md)
    
- [<span data-ttu-id="4b464-128">ApiVersionSupported</span><span class="sxs-lookup"><span data-stu-id="4b464-128">ApiVersionSupported</span></span>](apiversionsupported.md)
    
- [<span data-ttu-id="4b464-129">SchemaVersionSupported</span><span class="sxs-lookup"><span data-stu-id="4b464-129">SchemaVersionSupported</span></span>](schemaversionsupported.md)
    
## <a name="successful-getappmanifests-operation-response"></a><span data-ttu-id="4b464-130">Respuesta de operación GetAppManifests correcta</span><span class="sxs-lookup"><span data-stu-id="4b464-130">Successful GetAppManifests operation response</span></span>

<span data-ttu-id="4b464-131">En el siguiente ejemplo se muestra una respuesta correcta a una solicitud de operación de **GetAppManifests** para obtener los manifiestos de aplicación de un buzón.</span><span class="sxs-lookup"><span data-stu-id="4b464-131">The following example shows a successful response to a **GetAppManifests** operation request to get the app manifests for a mailbox.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4b464-132">Todos los manifiestos de aplicación Base64 se han truncado arbitrariamente para preservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="4b464-132">All base64 app manifests have been arbitrarily truncated to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="918" 
                           MinorBuildNumber="07" 
                           Version="V2_10" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetAppManifestsResponse ResponseClass="Success" 
                               xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <m:Apps xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
          <t:App xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
            <t:Manifest>WNlQXBwPg==</t:Manifest>
          </t:App>
         </m:Apps>
      </GetAppManifestsResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="4b464-133">El cuerpo SOAP de respuesta contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="4b464-133">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="4b464-134">GetAppManifestsResponse</span><span class="sxs-lookup"><span data-stu-id="4b464-134">GetAppManifestsResponse</span></span>](getappmanifestsresponse.md)
    
- [<span data-ttu-id="4b464-135">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="4b464-135">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="4b464-136">Aplicaciones</span><span class="sxs-lookup"><span data-stu-id="4b464-136">Apps</span></span>](apps.md)
    
- [<span data-ttu-id="4b464-137">App</span><span class="sxs-lookup"><span data-stu-id="4b464-137">App</span></span>](app.md)
    
- [<span data-ttu-id="4b464-138">Manifiesto</span><span class="sxs-lookup"><span data-stu-id="4b464-138">Manifest</span></span>](manifest.md)
    
<span data-ttu-id="4b464-139">El cuerpo SOAP de respuesta también puede contener el siguiente elemento:</span><span class="sxs-lookup"><span data-stu-id="4b464-139">The response SOAP body can also contain the following element:</span></span>
  
- [<span data-ttu-id="4b464-140">Manifiestos</span><span class="sxs-lookup"><span data-stu-id="4b464-140">Manifests</span></span>](manifests.md)
    
## <a name="getappmanifests-operation-error-response"></a><span data-ttu-id="4b464-141">Respuesta de error de operación de GetAppManifests</span><span class="sxs-lookup"><span data-stu-id="4b464-141">GetAppManifests operation error response</span></span>

<span data-ttu-id="4b464-142">Los errores devueltos para esta operación están relacionados con un formato no válido de los parámetros de entrada o son errores genéricos de EWS.</span><span class="sxs-lookup"><span data-stu-id="4b464-142">Errors returned for this operation are related to an invalid format of the input parameters or are generic EWS errors.</span></span> <span data-ttu-id="4b464-143">Para los códigos de error que son genéricos para EWS y específicos de esta operación, vea [ResponseCode](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="4b464-143">For error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
```
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <ServerVersionInfo MajorVersion="15"
                       MinorVersion="0"
                       MajorBuildNumber="918"
                       MinorBuildNumber="07"
                       Version="V2_10"
                       xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetAppManifestsResponse ResponseClass="Error"
                             xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <MessageText>The apiVersionSupported parameter is invalid. 
                   It should be in the form of major version, minor 
                   version, separated by '.', for example '2.34'.</MessageText>
      <ResponseCode>ErrorInvalidRequest</ResponseCode>
      <DescriptiveLinkKey>0</DescriptiveLinkKey>
    </GetAppManifestsResponse>
  </s:Body>
</s:Envelope>

```

## <a name="see-also"></a><span data-ttu-id="4b464-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="4b464-144">See also</span></span>

- [<span data-ttu-id="4b464-145">Operaciones de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="4b464-145">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="4b464-146">Operación DisableApp</span><span class="sxs-lookup"><span data-stu-id="4b464-146">DisableApp operation</span></span>](disableapp-operation.md)
    
- [<span data-ttu-id="4b464-147">Operación InstallApp</span><span class="sxs-lookup"><span data-stu-id="4b464-147">InstallApp operation</span></span>](installapp-operation.md)
    
- [<span data-ttu-id="4b464-148">Operación UninstallApp</span><span class="sxs-lookup"><span data-stu-id="4b464-148">UninstallApp operation</span></span>](uninstallapp-operation.md)
    
- [<span data-ttu-id="4b464-149">Operación GetAppMarketplaceUrl</span><span class="sxs-lookup"><span data-stu-id="4b464-149">GetAppMarketplaceUrl operation</span></span>](getappmarketplaceurl-operation.md)
    

