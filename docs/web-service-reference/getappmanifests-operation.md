---
title: Operación GetAppManifests
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 21a4987c-c24d-4a6e-ace4-e81edcda6303
description: Busque información sobre la EWS GetAppManifests operación.
ms.openlocfilehash: 9c919bac9ac0042890d1c439454b37e6b7c60876
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764741"
---
# <a name="getappmanifests-operation"></a><span data-ttu-id="6d5b5-103">Operación GetAppManifests</span><span class="sxs-lookup"><span data-stu-id="6d5b5-103">GetAppManifests operation</span></span>

<span data-ttu-id="6d5b5-104">Obtenga información acerca de la operación de EWS **GetAppManifests** .</span><span class="sxs-lookup"><span data-stu-id="6d5b5-104">Find information about the **GetAppManifests** EWS operation.</span></span> 
  
<span data-ttu-id="6d5b5-105">La operación **GetAppManifests** recupera manifiestos de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-105">The **GetAppManifests** operation retrieves app manifests.</span></span> 
  
<span data-ttu-id="6d5b5-106">Esta operación se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getappmanifests-operation"></a><span data-ttu-id="6d5b5-107">Mediante la operación GetAppManifests</span><span class="sxs-lookup"><span data-stu-id="6d5b5-107">Using the GetAppManifests operation</span></span>

<span data-ttu-id="6d5b5-108">La operación **GetAppManifests** no toma ningún argumento para solicitar los manifiestos de aplicación para un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-108">The **GetAppManifests** operation does not take any arguments to request the app manifests for a mailbox.</span></span> <span data-ttu-id="6d5b5-109">La respuesta contendrá con codificación base64 archivos de manifiesto XML para cada aplicación que se instala en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-109">The response will contain base64-encoded XML manifest files for each app that is installed in a mailbox.</span></span> 
  
### <a name="getappmanifests-operation-soap-headers"></a><span data-ttu-id="6d5b5-110">Encabezados SOAP de operación de GetAppManifests</span><span class="sxs-lookup"><span data-stu-id="6d5b5-110">GetAppManifests operation SOAP headers</span></span>

<span data-ttu-id="6d5b5-111">La operación de **GetAppManifests** puede utilizar los encabezados SOAP que se enumeran en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-111">The **GetAppManifests** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="6d5b5-112">**Nombre de encabezado**</span><span class="sxs-lookup"><span data-stu-id="6d5b5-112">**Header name**</span></span>|<span data-ttu-id="6d5b5-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="6d5b5-113">**Element**</span></span>|<span data-ttu-id="6d5b5-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6d5b5-114">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6d5b5-115">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="6d5b5-115">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="6d5b5-116">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="6d5b5-116">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="6d5b5-117">Identifica la versión del esquema para la solicitud de la operación.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-117">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="6d5b5-118">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-118">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="6d5b5-119">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="6d5b5-119">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="6d5b5-120">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="6d5b5-120">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="6d5b5-121">Identifica la versión del servidor que ha respondido a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-121">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="6d5b5-122">Este encabezado es aplicable a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-122">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getappmanifests-operation-request-example-get-the-app-manifests-for-a-mailbox"></a><span data-ttu-id="6d5b5-123">Ejemplo de solicitud de operación de GetAppManifests: obtener los manifiestos de aplicación para un buzón de correo</span><span class="sxs-lookup"><span data-stu-id="6d5b5-123">GetAppManifests operation request example: Get the app manifests for a mailbox</span></span>

<span data-ttu-id="6d5b5-124">El siguiente ejemplo de una solicitud de operación **GetAppManifests** muestra cómo obtener los manifiestos de aplicación para un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-124">The following example of a **GetAppManifests** operation request shows how to get the app manifests for a mailbox.</span></span> <span data-ttu-id="6d5b5-125">El elemento [ApiVersionSupported](apiversionsupported.md) y el elemento de [SchemaVersionSupported](schemaversionsupported.md) son opcionales.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-125">The [ApiVersionSupported](apiversionsupported.md) element and the [SchemaVersionSupported](schemaversionsupported.md) element are optional.</span></span> 
  
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
      <m:GetAppManifests>
        <m:ApiVersionSupported>1.1</m:ApiVersionSupported>
        <m:SchemaVersionSupported>1.1</m:SchemaVersionSupported>
      </m:GetAppManifests>
   </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="6d5b5-126">La solicitud SOAP body contiene el elemento siguiente:</span><span class="sxs-lookup"><span data-stu-id="6d5b5-126">The request SOAP body contains the following element:</span></span>
  
- [<span data-ttu-id="6d5b5-127">GetAppManifests</span><span class="sxs-lookup"><span data-stu-id="6d5b5-127">GetAppManifests</span></span>](getappmanifests.md)
    
- [<span data-ttu-id="6d5b5-128">ApiVersionSupported</span><span class="sxs-lookup"><span data-stu-id="6d5b5-128">ApiVersionSupported</span></span>](apiversionsupported.md)
    
- [<span data-ttu-id="6d5b5-129">SchemaVersionSupported</span><span class="sxs-lookup"><span data-stu-id="6d5b5-129">SchemaVersionSupported</span></span>](schemaversionsupported.md)
    
## <a name="successful-getappmanifests-operation-response"></a><span data-ttu-id="6d5b5-130">Respuesta es correcta de operación GetAppManifests</span><span class="sxs-lookup"><span data-stu-id="6d5b5-130">Successful GetAppManifests operation response</span></span>

<span data-ttu-id="6d5b5-131">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación **GetAppManifests** para obtener los manifiestos de aplicación para un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-131">The following example shows a successful response to a **GetAppManifests** operation request to get the app manifests for a mailbox.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="6d5b5-132">Se ha truncado arbitrariamente todos los manifiestos de aplicación de base64 para conservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-132">All base64 app manifests have been arbitrarily truncated to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="918" 
                           MinorBuildNumber="07" 
                           Version="V2_10" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetAppManifestsResponse ResponseClass="Success" 
                               xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <m:Apps xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
          <t:App xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
            <t:Manifest>WNlQXBwPg==</t:Manifest>
          </t:App>
         </m:Apps>
      </GetAppManifestsResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="6d5b5-133">La respuesta SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="6d5b5-133">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="6d5b5-134">GetAppManifestsResponse</span><span class="sxs-lookup"><span data-stu-id="6d5b5-134">GetAppManifestsResponse</span></span>](getappmanifestsresponse.md)
    
- [<span data-ttu-id="6d5b5-135">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="6d5b5-135">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="6d5b5-136">Aplicaciones</span><span class="sxs-lookup"><span data-stu-id="6d5b5-136">Apps</span></span>](apps.md)
    
- [<span data-ttu-id="6d5b5-137">App</span><span class="sxs-lookup"><span data-stu-id="6d5b5-137">App</span></span>](app.md)
    
- [<span data-ttu-id="6d5b5-138">Manifest</span><span class="sxs-lookup"><span data-stu-id="6d5b5-138">Manifest</span></span>](manifest.md)
    
<span data-ttu-id="6d5b5-139">El cuerpo del mensaje SOAP de respuesta también puede contener el elemento siguiente:</span><span class="sxs-lookup"><span data-stu-id="6d5b5-139">The response SOAP body can also contain the following element:</span></span>
  
- [<span data-ttu-id="6d5b5-140">Manifiestos</span><span class="sxs-lookup"><span data-stu-id="6d5b5-140">Manifests</span></span>](manifests.md)
    
## <a name="getappmanifests-operation-error-response"></a><span data-ttu-id="6d5b5-141">Respuesta de error de la operación de GetAppManifests</span><span class="sxs-lookup"><span data-stu-id="6d5b5-141">GetAppManifests operation error response</span></span>

<span data-ttu-id="6d5b5-142">Los errores devueltos para esta operación están relacionados con un formato no válido de los parámetros de entrada o son los errores EWS genéricos.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-142">Errors returned for this operation are related to an invalid format of the input parameters or are generic EWS errors.</span></span> <span data-ttu-id="6d5b5-143">Para códigos de error que son genéricos para EWS y específicos de esta operación, vea [ResponseCode](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="6d5b5-143">For error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
```
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <ServerVersionInfo MajorVersion="15"
                       MinorVersion="0"
                       MajorBuildNumber="918"
                       MinorBuildNumber="07"
                       Version="V2_10"
                       xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetAppManifestsResponse ResponseClass="Error"
                             xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <MessageText>The apiVersionSupported parameter is invalid. 
                   It should be in the form of major version, minor 
                   version, separated by '.', for example '2.34'.</MessageText>
      <ResponseCode>ErrorInvalidRequest</ResponseCode>
      <DescriptiveLinkKey>0</DescriptiveLinkKey>
    </GetAppManifestsResponse>
  </s:Body>
</s:Envelope>

```

## <a name="see-also"></a><span data-ttu-id="6d5b5-144">Ver también</span><span class="sxs-lookup"><span data-stu-id="6d5b5-144">See also</span></span>

- [<span data-ttu-id="6d5b5-145">Operaciones de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="6d5b5-145">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="6d5b5-146">Operación DisableApp</span><span class="sxs-lookup"><span data-stu-id="6d5b5-146">DisableApp operation</span></span>](disableapp-operation.md)
    
- [<span data-ttu-id="6d5b5-147">Operación InstallApp</span><span class="sxs-lookup"><span data-stu-id="6d5b5-147">InstallApp operation</span></span>](installapp-operation.md)
    
- [<span data-ttu-id="6d5b5-148">Operación UninstallApp</span><span class="sxs-lookup"><span data-stu-id="6d5b5-148">UninstallApp operation</span></span>](uninstallapp-operation.md)
    
- [<span data-ttu-id="6d5b5-149">Operación GetAppMarketplaceUrl</span><span class="sxs-lookup"><span data-stu-id="6d5b5-149">GetAppMarketplaceUrl operation</span></span>](getappmarketplaceurl-operation.md)
    

