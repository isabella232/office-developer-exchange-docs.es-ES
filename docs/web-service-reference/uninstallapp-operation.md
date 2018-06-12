---
title: Operación UninstallApp
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7707aa6a-381d-43f7-a454-54f6343ed127
description: Busque información sobre la EWS UninstallApp operación.
ms.openlocfilehash: 4f44224651993023336eef5540ec29b7f6a6e32e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840760"
---
# <a name="uninstallapp-operation"></a><span data-ttu-id="158be-103">Operación UninstallApp</span><span class="sxs-lookup"><span data-stu-id="158be-103">UninstallApp operation</span></span>

<span data-ttu-id="158be-104">Obtenga información acerca de la operación de EWS **UninstallApp** .</span><span class="sxs-lookup"><span data-stu-id="158be-104">Find information about the **UninstallApp** EWS operation.</span></span> 
  
<span data-ttu-id="158be-105">La operación **UninstallApp** desinstala una aplicación de correo para Outlook.</span><span class="sxs-lookup"><span data-stu-id="158be-105">The **UninstallApp** operation uninstalls a mail app for Outlook.</span></span> 
  
<span data-ttu-id="158be-106">Esta operación se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="158be-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-uninstallapp-operation"></a><span data-ttu-id="158be-107">Mediante la operación UninstallApp</span><span class="sxs-lookup"><span data-stu-id="158be-107">Using the UninstallApp operation</span></span>

<span data-ttu-id="158be-108">La operación de **UninstallApp** toma un argumento en la solicitud que identifica la aplicación de correo para desinstalar.</span><span class="sxs-lookup"><span data-stu-id="158be-108">The **UninstallApp** operation takes one argument in the request that identifies the mail app to uninstall.</span></span> 
  
### <a name="uninstallapp-operation-soap-headers"></a><span data-ttu-id="158be-109">Encabezados SOAP de operación de UninstallApp</span><span class="sxs-lookup"><span data-stu-id="158be-109">UninstallApp operation SOAP headers</span></span>

<span data-ttu-id="158be-110">La operación de **UninstallApp** puede utilizar los encabezados SOAP que se enumeran en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="158be-110">The **UninstallApp** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="158be-111">**Nombre de encabezado**</span><span class="sxs-lookup"><span data-stu-id="158be-111">**Header name**</span></span>|<span data-ttu-id="158be-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="158be-112">**Element**</span></span>|<span data-ttu-id="158be-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="158be-113">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="158be-114">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="158be-114">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="158be-115">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="158be-115">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="158be-116">Identifica la versión del esquema para la solicitud de la operación.</span><span class="sxs-lookup"><span data-stu-id="158be-116">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="158be-117">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="158be-117">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="158be-118">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="158be-118">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="158be-119">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="158be-119">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="158be-120">Identifica la versión del servidor que ha respondido a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="158be-120">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="158be-121">Este encabezado es aplicable a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="158be-121">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="uninstallapp-operation-request-example-uninstall-a-mail-app-in-a-mailbox"></a><span data-ttu-id="158be-122">Ejemplo de solicitud de operación de UninstallApp: desinstalar una aplicación de correo en un buzón de correo</span><span class="sxs-lookup"><span data-stu-id="158be-122">UninstallApp operation request example: Uninstall a mail app in a mailbox</span></span>

<span data-ttu-id="158be-123">El siguiente ejemplo de una operación de **UninstallApp** solicitar muestra cómo a una desinstalación de una aplicación de correo mediante el identificador de aplicación.</span><span class="sxs-lookup"><span data-stu-id="158be-123">The following example of an **UninstallApp** operation request shows how to a uninstall a mail app by using the app identifier.</span></span> <span data-ttu-id="158be-124">El identificador de la aplicación puede encontrarse en el manifiesto de aplicación que es devuelto por la [operación de GetAppManifests](getappmanifests-operation.md).</span><span class="sxs-lookup"><span data-stu-id="158be-124">The app identifier can be found in the app manifest that is returned by the [GetAppManifests operation](getappmanifests-operation.md).</span></span>
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:UninstallApp>
         <m:ID>1C50226D-04B5-4AB2-9FCD-42E236B59E4B</m:ID>
      </m:UninstallApp>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="158be-125">La solicitud SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="158be-125">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="158be-126">UninstallApp</span><span class="sxs-lookup"><span data-stu-id="158be-126">UninstallApp</span></span>](uninstallapp.md)
    
- [<span data-ttu-id="158be-127">Identificador (cadena)</span><span class="sxs-lookup"><span data-stu-id="158be-127">ID (String)</span></span>](id-string.md)
    
## <a name="successful-uninstallapp-operation-response"></a><span data-ttu-id="158be-128">Respuesta es correcta de operación UninstallApp</span><span class="sxs-lookup"><span data-stu-id="158be-128">Successful UninstallApp operation response</span></span>

<span data-ttu-id="158be-129">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación **UninstallApp** para desinstalar una aplicación de correo.</span><span class="sxs-lookup"><span data-stu-id="158be-129">The following example shows a successful response to an **UninstallApp** operation request to uninstall a mail app.</span></span> 
  
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
      <UninstallAppResponse ResponseClass="Success" 
                            xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
      </UninstallAppResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="158be-130">La respuesta SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="158be-130">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="158be-131">UninstallAppResponse</span><span class="sxs-lookup"><span data-stu-id="158be-131">UninstallAppResponse</span></span>](uninstallappresponse.md)
    
- [<span data-ttu-id="158be-132">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="158be-132">ResponseCode</span></span>](responsecode.md)
    
## <a name="uninstallapp-operation-error-response"></a><span data-ttu-id="158be-133">Respuesta de error de la operación de UninstallApp</span><span class="sxs-lookup"><span data-stu-id="158be-133">UninstallApp operation error response</span></span>

<span data-ttu-id="158be-134">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **UninstallApp** .</span><span class="sxs-lookup"><span data-stu-id="158be-134">The following example shows an error response to an **UninstallApp** operation request.</span></span> <span data-ttu-id="158be-135">Esta es una respuesta a una solicitud para desinstalar una aplicación de correo que ya se ha desinstalado.</span><span class="sxs-lookup"><span data-stu-id="158be-135">This is a response to a request to uninstall a mail app that has already been uninstalled.</span></span> 
  
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
      <UninstallAppResponse ResponseClass="Error" 
                            xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>Extension ID 1c50226d-04b5-4ab2-9fcd-42e236b59e4b can't be found.</MessageText>
         <ResponseCode>ErrorInternalServerError</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </UninstallAppResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="158be-136">La respuesta de error SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="158be-136">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="158be-137">UninstallAppResponse</span><span class="sxs-lookup"><span data-stu-id="158be-137">UninstallAppResponse</span></span>](uninstallappresponse.md)
    
- [<span data-ttu-id="158be-138">MessageText</span><span class="sxs-lookup"><span data-stu-id="158be-138">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="158be-139">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="158be-139">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="158be-140">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="158be-140">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="158be-141">Para códigos de error adicionales que son genéricos para EWS y específicos de esta operación, vea [ResponseCode](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="158be-141">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="158be-142">Ver también</span><span class="sxs-lookup"><span data-stu-id="158be-142">See also</span></span>

- [<span data-ttu-id="158be-143">Operaciones de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="158be-143">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="158be-144">Operación InstallApp</span><span class="sxs-lookup"><span data-stu-id="158be-144">InstallApp operation</span></span>](installapp-operation.md)
    
- [<span data-ttu-id="158be-145">Operación DisableApp</span><span class="sxs-lookup"><span data-stu-id="158be-145">DisableApp operation</span></span>](disableapp-operation.md)
    
- [<span data-ttu-id="158be-146">GetAppManifests</span><span class="sxs-lookup"><span data-stu-id="158be-146">GetAppManifests</span></span>](getappmanifests.md)
    
- [<span data-ttu-id="158be-147">Operación GetAppMarketplaceUrl</span><span class="sxs-lookup"><span data-stu-id="158be-147">GetAppMarketplaceUrl operation</span></span>](getappmarketplaceurl-operation.md)
    

