---
title: Operación DisableApp
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 211731a3-2470-49af-bda3-1ddfc15a8e46
description: Busque información sobre la EWS DisableApp operación.
ms.openlocfilehash: be9e124d7464012ffa797a69192893d85804a004
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764172"
---
# <a name="disableapp-operation"></a><span data-ttu-id="ae988-103">Operación DisableApp</span><span class="sxs-lookup"><span data-stu-id="ae988-103">DisableApp operation</span></span>

<span data-ttu-id="ae988-104">Obtenga información acerca de la operación de EWS **DisableApp** .</span><span class="sxs-lookup"><span data-stu-id="ae988-104">Find information about the **DisableApp** EWS operation.</span></span> 
  
<span data-ttu-id="ae988-105">La operación **DisableApp** deshabilita una aplicación de correo para Outlook.</span><span class="sxs-lookup"><span data-stu-id="ae988-105">The **DisableApp** operation disables a mail app for Outlook.</span></span> 
  
<span data-ttu-id="ae988-106">Esta operación se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ae988-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-disableapp-operation"></a><span data-ttu-id="ae988-107">Mediante la operación DisableApp</span><span class="sxs-lookup"><span data-stu-id="ae988-107">Using the DisableApp operation</span></span>

<span data-ttu-id="ae988-108">La operación **DisableApp** toma dos argumentos en la solicitud que identifican la aplicación de correo para deshabilitar y el motivo por qué se ha deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="ae988-108">The **DisableApp** operation takes two arguments in the request that identify the mail app to disable and the reason why it was disabled.</span></span> 
  
### <a name="disableapp-operation-soap-headers"></a><span data-ttu-id="ae988-109">Encabezados SOAP de operación de DisableApp</span><span class="sxs-lookup"><span data-stu-id="ae988-109">DisableApp operation SOAP headers</span></span>

<span data-ttu-id="ae988-110">La operación de **DisableApp** puede utilizar los encabezados SOAP que se enumeran en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="ae988-110">The **DisableApp** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="ae988-111">**Nombre de encabezado**</span><span class="sxs-lookup"><span data-stu-id="ae988-111">**Header name**</span></span>|<span data-ttu-id="ae988-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="ae988-112">**Element**</span></span>|<span data-ttu-id="ae988-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ae988-113">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ae988-114">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="ae988-114">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="ae988-115">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="ae988-115">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="ae988-116">Identifica la versión del esquema para la solicitud de la operación.</span><span class="sxs-lookup"><span data-stu-id="ae988-116">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="ae988-117">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="ae988-117">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="ae988-118">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="ae988-118">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="ae988-119">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="ae988-119">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="ae988-120">Identifica la versión del servidor que ha respondido a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ae988-120">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="ae988-121">Este encabezado es aplicable a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="ae988-121">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="disableapp-operation-request-example-disable-a-mail-app-installed-in-a-mailbox"></a><span data-ttu-id="ae988-122">Ejemplo de solicitud de operación de DisableApp: deshabilitar una aplicación de correo instalada en un buzón de correo</span><span class="sxs-lookup"><span data-stu-id="ae988-122">DisableApp operation request example: Disable a mail app installed in a mailbox</span></span>

<span data-ttu-id="ae988-123">Cómo se muestra en el siguiente ejemplo de una operación de **DisableApp** de solicitudes para deshabilitar una aplicación de correo.</span><span class="sxs-lookup"><span data-stu-id="ae988-123">The following example of a **DisableApp** operation request shows how to a disable a mail app.</span></span> <span data-ttu-id="ae988-124">El identificador de la aplicación puede encontrarse en el manifiesto de la aplicación que se devuelve en una respuesta de la [operación de GetAppManifests](getappmanifests-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="ae988-124">The app identifier can be found in the app manifest that is returned in a [GetAppManifests operation](getappmanifests-operation.md) response.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
      <t:MailboxCulture>en-US</t:MailboxCulture>
      <t:TimeZoneContext>
         <t:TimeZoneDefinition Id="GMT Standard Time"/>
      </t:TimeZoneContext>
   </soap:Header>
   <soap:Body >
      <m:DisableApp>
         <m:ID>1C50226D-04B5-4AB2-9FCD-42E236B59E4B</m:ID>
         <m:DisableReason>NoReason</m:DisableReason>
      </m:DisableApp>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="ae988-125">La solicitud SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="ae988-125">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="ae988-126">DisableApp</span><span class="sxs-lookup"><span data-stu-id="ae988-126">DisableApp</span></span>](disableapp.md)
    
- [<span data-ttu-id="ae988-127">Identificador (cadena)</span><span class="sxs-lookup"><span data-stu-id="ae988-127">ID (String)</span></span>](id-string.md)
    
- [<span data-ttu-id="ae988-128">DisableReason</span><span class="sxs-lookup"><span data-stu-id="ae988-128">DisableReason</span></span>](disablereason.md)
    
## <a name="successful-disableapp-operation-response"></a><span data-ttu-id="ae988-129">Respuesta es correcta de operación DisableApp</span><span class="sxs-lookup"><span data-stu-id="ae988-129">Successful DisableApp operation response</span></span>

<span data-ttu-id="ae988-130">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación de **DisableApp** para deshabilitar una aplicación de correo.</span><span class="sxs-lookup"><span data-stu-id="ae988-130">The following example shows a successful response to a **DisableApp** operation request to disable a mail app.</span></span> 
  
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
      <DisableAppResponse ResponseClass="Success" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
      </DisableAppResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="ae988-131">La respuesta SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="ae988-131">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="ae988-132">DisableAppResponse</span><span class="sxs-lookup"><span data-stu-id="ae988-132">DisableAppResponse</span></span>](disableappresponse.md)
    
- [<span data-ttu-id="ae988-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="ae988-133">ResponseCode</span></span>](responsecode.md)
    
## <a name="disableapp-operation-error-response"></a><span data-ttu-id="ae988-134">Respuesta de error de la operación de DisableApp</span><span class="sxs-lookup"><span data-stu-id="ae988-134">DisableApp operation error response</span></span>

<span data-ttu-id="ae988-135">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **DisableApp** .</span><span class="sxs-lookup"><span data-stu-id="ae988-135">The following example shows an error response to a **DisableApp** operation request.</span></span> <span data-ttu-id="ae988-136">Esta es una respuesta a una solicitud para deshabilitar una aplicación de correo que no está instalada en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="ae988-136">This is a response to a request to disable a mail app that is not installed in a mailbox.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="556" MinorBuildNumber="14" Version="Exchange2013" xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" xmlns="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <DisableAppResponse ResponseClass="Error" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>Extension ID 1C50226D-04B5-4AB2-9FCD-42E236B59E4A can't be found.</MessageText>
         <ResponseCode>ErrorExtensionNotFound</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </DisableAppResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="ae988-137">La respuesta de error SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="ae988-137">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="ae988-138">DisableAppResponse</span><span class="sxs-lookup"><span data-stu-id="ae988-138">DisableAppResponse</span></span>](disableappresponse.md)
    
- [<span data-ttu-id="ae988-139">MessageText</span><span class="sxs-lookup"><span data-stu-id="ae988-139">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="ae988-140">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="ae988-140">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="ae988-141">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="ae988-141">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="ae988-142">Para códigos de error adicionales que son genéricos para EWS y específicos de esta operación, vea [ResponseCode](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="ae988-142">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ae988-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="ae988-143">See also</span></span>

- [<span data-ttu-id="ae988-144">Operaciones de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="ae988-144">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)   
- [<span data-ttu-id="ae988-145">Operación InstallApp</span><span class="sxs-lookup"><span data-stu-id="ae988-145">InstallApp operation</span></span>](installapp-operation.md)   
- [<span data-ttu-id="ae988-146">Operación UninstallApp</span><span class="sxs-lookup"><span data-stu-id="ae988-146">UninstallApp operation</span></span>](uninstallapp-operation.md)   
- [<span data-ttu-id="ae988-147">GetAppManifests</span><span class="sxs-lookup"><span data-stu-id="ae988-147">GetAppManifests</span></span>](getappmanifests.md)   
- [<span data-ttu-id="ae988-148">Operación GetAppMarketplaceUrl</span><span class="sxs-lookup"><span data-stu-id="ae988-148">GetAppMarketplaceUrl operation</span></span>](getappmarketplaceurl-operation.md)   
- [<span data-ttu-id="ae988-149">Complementos de Outlook</span><span class="sxs-lookup"><span data-stu-id="ae988-149">Outlook add-ins</span></span>](http://msdn.microsoft.com/library/71e64bc9-e347-4f5d-8948-0a47b5dd93e6%28Office.15%29.aspx)
    

