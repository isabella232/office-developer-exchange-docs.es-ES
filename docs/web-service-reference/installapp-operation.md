---
title: Operación InstallApp
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 596eae95-3e78-489a-8bb2-d2dd4a026405
description: Busque información sobre la EWS InstallApp operación.
ms.openlocfilehash: ccc5d2dde949070bae905ff1ebb182c892f07fcb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19835951"
---
# <a name="installapp-operation"></a><span data-ttu-id="a678c-103">Operación InstallApp</span><span class="sxs-lookup"><span data-stu-id="a678c-103">InstallApp operation</span></span>

<span data-ttu-id="a678c-104">Obtenga información acerca de la operación de EWS **InstallApp** .</span><span class="sxs-lookup"><span data-stu-id="a678c-104">Find information about the **InstallApp** EWS operation.</span></span> 
  
<span data-ttu-id="a678c-105">La operación de **InstallApp** instala una aplicación de correo para Outlook en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="a678c-105">The **InstallApp** operation installs a mail app for Outlook in a mailbox.</span></span> 
  
<span data-ttu-id="a678c-106">Esta operación se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a678c-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-installapp-operation"></a><span data-ttu-id="a678c-107">Mediante la operación InstallApp</span><span class="sxs-lookup"><span data-stu-id="a678c-107">Using the InstallApp operation</span></span>

<span data-ttu-id="a678c-108">La operación de **InstallApp** toma un argumento único que identifica una aplicación de correo para instalar.</span><span class="sxs-lookup"><span data-stu-id="a678c-108">The **InstallApp** operation takes a single argument that identifies a mail app to install.</span></span> <span data-ttu-id="a678c-109">El argumento contiene el manifiesto con codificación base64 para una aplicación de correo.</span><span class="sxs-lookup"><span data-stu-id="a678c-109">The argument contains the base64-encoded manifest for a mail app.</span></span> 
  
### <a name="installapp-operation-soap-headers"></a><span data-ttu-id="a678c-110">Encabezados SOAP de operación de InstallApp</span><span class="sxs-lookup"><span data-stu-id="a678c-110">InstallApp operation SOAP headers</span></span>

<span data-ttu-id="a678c-111">La operación de **InstallApp** puede utilizar los encabezados SOAP que se enumeran en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="a678c-111">The **InstallApp** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="a678c-112">**Nombre de encabezado**</span><span class="sxs-lookup"><span data-stu-id="a678c-112">**Header name**</span></span>|<span data-ttu-id="a678c-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="a678c-113">**Element**</span></span>|<span data-ttu-id="a678c-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a678c-114">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a678c-115">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="a678c-115">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="a678c-116">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="a678c-116">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="a678c-117">Identifica la versión del esquema para la solicitud de la operación.</span><span class="sxs-lookup"><span data-stu-id="a678c-117">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="a678c-118">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="a678c-118">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="a678c-119">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="a678c-119">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="a678c-120">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="a678c-120">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="a678c-121">Identifica la versión del servidor que ha respondido a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a678c-121">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="a678c-122">Este encabezado es aplicable a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="a678c-122">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="installapp-operation-request-example-install-a-mail-app-in-a-mailbox"></a><span data-ttu-id="a678c-123">Ejemplo de solicitud de operación de InstallApp: instalar una aplicación de correo en un buzón de correo</span><span class="sxs-lookup"><span data-stu-id="a678c-123">InstallApp operation request example: Install a mail app in a mailbox</span></span>

<span data-ttu-id="a678c-124">El siguiente ejemplo de una solicitud de operación **InstallApp** muestra cómo instalar una aplicación de correo para Outlook.</span><span class="sxs-lookup"><span data-stu-id="a678c-124">The following example of an **InstallApp** operation request shows how to install a mail app for Outlook.</span></span> <span data-ttu-id="a678c-125">Puede encontrar el manifiesto de aplicación mediante el uso de la [operación de GetAppManifests](getappmanifests-operation.md).</span><span class="sxs-lookup"><span data-stu-id="a678c-125">The app manifest can be found by using the [GetAppManifests operation](getappmanifests-operation.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="a678c-126">El manifiesto de aplicación con codificación base64 se ha truncado arbitrariamente para conservar la legibilidad y no representan un manifiesto válido.</span><span class="sxs-lookup"><span data-stu-id="a678c-126">The base64-encoded app manifest has been arbitrarily truncated to preserve readability and does not represent a valid manifest.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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

<span data-ttu-id="a678c-127">La solicitud SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="a678c-127">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="a678c-128">InstallApp</span><span class="sxs-lookup"><span data-stu-id="a678c-128">InstallApp</span></span>](installapp.md)
    
- [<span data-ttu-id="a678c-129">Manifest</span><span class="sxs-lookup"><span data-stu-id="a678c-129">Manifest</span></span>](manifest.md)
    
## <a name="successful-installapp-operation-response"></a><span data-ttu-id="a678c-130">Respuesta es correcta de operación InstallApp</span><span class="sxs-lookup"><span data-stu-id="a678c-130">Successful InstallApp operation response</span></span>

<span data-ttu-id="a678c-131">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación **InstallApp** para instalar una aplicación de correo.</span><span class="sxs-lookup"><span data-stu-id="a678c-131">The following example shows a successful response to an **InstallApp** operation request to install a mail app.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="14" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <InstallAppResponse ResponseClass="Success" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
      </InstallAppResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="a678c-132">La respuesta SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="a678c-132">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="a678c-133">InstallAppResponse</span><span class="sxs-lookup"><span data-stu-id="a678c-133">InstallAppResponse</span></span>](installappresponse.md)
    
- [<span data-ttu-id="a678c-134">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="a678c-134">ResponseCode</span></span>](responsecode.md)
    
## <a name="installapp-operation-error-response"></a><span data-ttu-id="a678c-135">Respuesta de error de la operación de InstallApp</span><span class="sxs-lookup"><span data-stu-id="a678c-135">InstallApp operation error response</span></span>

<span data-ttu-id="a678c-136">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **InstallApp** .</span><span class="sxs-lookup"><span data-stu-id="a678c-136">The following example shows an error response to an **InstallApp** operation request.</span></span> <span data-ttu-id="a678c-137">Esta es una respuesta a una solicitud que contiene un manifiesto no válido.</span><span class="sxs-lookup"><span data-stu-id="a678c-137">This is a response to a request that contains an invalid manifest.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="14" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <InstallAppResponse ResponseClass="Error" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>This app can't be installed. Missing OfficeApp element.</MessageText>
         <ResponseCode>ErrorInternalServerError</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </InstallAppResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="a678c-138">La respuesta de error SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="a678c-138">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="a678c-139">InstallAppResponse</span><span class="sxs-lookup"><span data-stu-id="a678c-139">InstallAppResponse</span></span>](installappresponse.md)
    
- [<span data-ttu-id="a678c-140">MessageText</span><span class="sxs-lookup"><span data-stu-id="a678c-140">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="a678c-141">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="a678c-141">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="a678c-142">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="a678c-142">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="a678c-143">Ver también</span><span class="sxs-lookup"><span data-stu-id="a678c-143">See also</span></span>

- [<span data-ttu-id="a678c-144">Operaciones de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="a678c-144">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="a678c-145">Operación DisableApp</span><span class="sxs-lookup"><span data-stu-id="a678c-145">DisableApp operation</span></span>](disableapp-operation.md)
    
- [<span data-ttu-id="a678c-146">Operación UninstallApp</span><span class="sxs-lookup"><span data-stu-id="a678c-146">UninstallApp operation</span></span>](uninstallapp-operation.md)
    
- [<span data-ttu-id="a678c-147">GetAppManifests</span><span class="sxs-lookup"><span data-stu-id="a678c-147">GetAppManifests</span></span>](getappmanifests.md)
    
- [<span data-ttu-id="a678c-148">Operación GetAppMarketplaceUrl</span><span class="sxs-lookup"><span data-stu-id="a678c-148">GetAppMarketplaceUrl operation</span></span>](getappmarketplaceurl-operation.md)
    

