---
title: Operación InstallApp
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 596eae95-3e78-489a-8bb2-d2dd4a026405
description: Buscar información sobre la operación de EWS de InstallApp.
ms.openlocfilehash: ae6aab7f7176aa827bafa9abf1aa67d458d309d2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465691"
---
# <a name="installapp-operation"></a><span data-ttu-id="4e3e1-103">Operación InstallApp</span><span class="sxs-lookup"><span data-stu-id="4e3e1-103">InstallApp operation</span></span>

<span data-ttu-id="4e3e1-104">Buscar información sobre la operación de EWS de **InstallApp** .</span><span class="sxs-lookup"><span data-stu-id="4e3e1-104">Find information about the **InstallApp** EWS operation.</span></span> 
  
<span data-ttu-id="4e3e1-105">La operación **InstallApp** instala una aplicación de correo para Outlook en un buzón.</span><span class="sxs-lookup"><span data-stu-id="4e3e1-105">The **InstallApp** operation installs a mail app for Outlook in a mailbox.</span></span> 
  
<span data-ttu-id="4e3e1-106">Esta operación se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="4e3e1-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-installapp-operation"></a><span data-ttu-id="4e3e1-107">Uso de la operación InstallApp</span><span class="sxs-lookup"><span data-stu-id="4e3e1-107">Using the InstallApp operation</span></span>

<span data-ttu-id="4e3e1-108">La operación **InstallApp** toma un argumento único que identifica una aplicación de correo que se va a instalar.</span><span class="sxs-lookup"><span data-stu-id="4e3e1-108">The **InstallApp** operation takes a single argument that identifies a mail app to install.</span></span> <span data-ttu-id="4e3e1-109">El argumento contiene el manifiesto codificado en base64 para una aplicación de correo.</span><span class="sxs-lookup"><span data-stu-id="4e3e1-109">The argument contains the base64-encoded manifest for a mail app.</span></span> 
  
### <a name="installapp-operation-soap-headers"></a><span data-ttu-id="4e3e1-110">Encabezados SOAP de operación InstallApp</span><span class="sxs-lookup"><span data-stu-id="4e3e1-110">InstallApp operation SOAP headers</span></span>

<span data-ttu-id="4e3e1-111">La operación **InstallApp** puede usar los encabezados SOAP que se enumeran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="4e3e1-111">The **InstallApp** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="4e3e1-112">**Nombre de encabezado**</span><span class="sxs-lookup"><span data-stu-id="4e3e1-112">**Header name**</span></span>|<span data-ttu-id="4e3e1-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="4e3e1-113">**Element**</span></span>|<span data-ttu-id="4e3e1-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4e3e1-114">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4e3e1-115">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="4e3e1-115">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="4e3e1-116">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="4e3e1-116">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="4e3e1-117">Identifica la versión del esquema para la solicitud de operación.</span><span class="sxs-lookup"><span data-stu-id="4e3e1-117">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="4e3e1-118">Este encabezado se aplica a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="4e3e1-118">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="4e3e1-119">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="4e3e1-119">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="4e3e1-120">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="4e3e1-120">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="4e3e1-121">Identifica la versión del servidor que respondió a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4e3e1-121">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="4e3e1-122">Este encabezado se aplica a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="4e3e1-122">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="installapp-operation-request-example-install-a-mail-app-in-a-mailbox"></a><span data-ttu-id="4e3e1-123">Ejemplo de solicitud de operación InstallApp: instalar una aplicación de correo en un buzón</span><span class="sxs-lookup"><span data-stu-id="4e3e1-123">InstallApp operation request example: Install a mail app in a mailbox</span></span>

<span data-ttu-id="4e3e1-124">El siguiente ejemplo de una solicitud de operación de **InstallApp** muestra cómo instalar una aplicación de correo para Outlook.</span><span class="sxs-lookup"><span data-stu-id="4e3e1-124">The following example of an **InstallApp** operation request shows how to install a mail app for Outlook.</span></span> <span data-ttu-id="4e3e1-125">El manifiesto de la aplicación puede encontrarse mediante la [operación GetAppManifests](getappmanifests-operation.md).</span><span class="sxs-lookup"><span data-stu-id="4e3e1-125">The app manifest can be found by using the [GetAppManifests operation](getappmanifests-operation.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="4e3e1-126">El manifiesto de la aplicación codificado en Base64 se ha truncado arbitrariamente para preservar la legibilidad y no representa un manifiesto válido.</span><span class="sxs-lookup"><span data-stu-id="4e3e1-126">The base64-encoded app manifest has been arbitrarily truncated to preserve readability and does not represent a valid manifest.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:InstallApp>
         <m:Manifest>TUwiIC8+CiAgPC9SdWxlPgo8L09mZmljZUFwcD4=</m:Manifest>
      </m:InstallApp>
   </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="4e3e1-127">El cuerpo SOAP de la solicitud contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="4e3e1-127">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="4e3e1-128">InstallApp</span><span class="sxs-lookup"><span data-stu-id="4e3e1-128">InstallApp</span></span>](installapp.md)
    
- [<span data-ttu-id="4e3e1-129">Manifiesto</span><span class="sxs-lookup"><span data-stu-id="4e3e1-129">Manifest</span></span>](manifest.md)
    
## <a name="successful-installapp-operation-response"></a><span data-ttu-id="4e3e1-130">Respuesta de operación InstallApp correcta</span><span class="sxs-lookup"><span data-stu-id="4e3e1-130">Successful InstallApp operation response</span></span>

<span data-ttu-id="4e3e1-131">En el siguiente ejemplo se muestra una respuesta correcta a una solicitud de operación **InstallApp** para instalar una aplicación de correo.</span><span class="sxs-lookup"><span data-stu-id="4e3e1-131">The following example shows a successful response to an **InstallApp** operation request to install a mail app.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="14" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <InstallAppResponse ResponseClass="Success" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
      </InstallAppResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="4e3e1-132">El cuerpo SOAP de respuesta contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="4e3e1-132">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="4e3e1-133">InstallAppResponse</span><span class="sxs-lookup"><span data-stu-id="4e3e1-133">InstallAppResponse</span></span>](installappresponse.md)
    
- [<span data-ttu-id="4e3e1-134">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="4e3e1-134">ResponseCode</span></span>](responsecode.md)
    
## <a name="installapp-operation-error-response"></a><span data-ttu-id="4e3e1-135">Respuesta de error de operación de InstallApp</span><span class="sxs-lookup"><span data-stu-id="4e3e1-135">InstallApp operation error response</span></span>

<span data-ttu-id="4e3e1-136">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **InstallApp** .</span><span class="sxs-lookup"><span data-stu-id="4e3e1-136">The following example shows an error response to an **InstallApp** operation request.</span></span> <span data-ttu-id="4e3e1-137">Se trata de una respuesta a una solicitud que contiene un manifiesto no válido.</span><span class="sxs-lookup"><span data-stu-id="4e3e1-137">This is a response to a request that contains an invalid manifest.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="14" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <InstallAppResponse ResponseClass="Error" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>This app can't be installed. Missing OfficeApp element.</MessageText>
         <ResponseCode>ErrorInternalServerError</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </InstallAppResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="4e3e1-138">El cuerpo SOAP de respuesta de error contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="4e3e1-138">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="4e3e1-139">InstallAppResponse</span><span class="sxs-lookup"><span data-stu-id="4e3e1-139">InstallAppResponse</span></span>](installappresponse.md)
    
- [<span data-ttu-id="4e3e1-140">MessageText</span><span class="sxs-lookup"><span data-stu-id="4e3e1-140">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="4e3e1-141">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="4e3e1-141">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="4e3e1-142">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="4e3e1-142">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="4e3e1-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="4e3e1-143">See also</span></span>

- [<span data-ttu-id="4e3e1-144">Operaciones de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="4e3e1-144">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="4e3e1-145">Operación DisableApp</span><span class="sxs-lookup"><span data-stu-id="4e3e1-145">DisableApp operation</span></span>](disableapp-operation.md)
    
- [<span data-ttu-id="4e3e1-146">Operación UninstallApp</span><span class="sxs-lookup"><span data-stu-id="4e3e1-146">UninstallApp operation</span></span>](uninstallapp-operation.md)
    
- [<span data-ttu-id="4e3e1-147">GetAppManifests</span><span class="sxs-lookup"><span data-stu-id="4e3e1-147">GetAppManifests</span></span>](getappmanifests.md)
    
- [<span data-ttu-id="4e3e1-148">Operación GetAppMarketplaceUrl</span><span class="sxs-lookup"><span data-stu-id="4e3e1-148">GetAppMarketplaceUrl operation</span></span>](getappmarketplaceurl-operation.md)
    

