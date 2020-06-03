---
title: Operación GetClientAccessToken
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 086876cc-e22c-4e89-89f9-19e78af51217
description: Buscar información sobre la operación de EWS de GetClientAccessToken.
ms.openlocfilehash: 2d49d675fcedb0e7e8312a9715f095c47fcf3d77
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462041"
---
# <a name="getclientaccesstoken-operation"></a><span data-ttu-id="d85db-103">Operación GetClientAccessToken</span><span class="sxs-lookup"><span data-stu-id="d85db-103">GetClientAccessToken operation</span></span>

<span data-ttu-id="d85db-104">Buscar información sobre la operación de EWS de **GetClientAccessToken** .</span><span class="sxs-lookup"><span data-stu-id="d85db-104">Find information about the **GetClientAccessToken** EWS operation.</span></span> 
  
<span data-ttu-id="d85db-105">La operación **GetClientAccessToken** obtiene un token de acceso de cliente para una aplicación de correo de Outlook.</span><span class="sxs-lookup"><span data-stu-id="d85db-105">The **GetClientAccessToken** operation gets a client access token for a mail app for Outlook.</span></span> 
  
<span data-ttu-id="d85db-106">Esta operación se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d85db-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getclientaccesstoken-operation"></a><span data-ttu-id="d85db-107">Uso de la operación GetClientAccessToken</span><span class="sxs-lookup"><span data-stu-id="d85db-107">Using the GetClientAccessToken operation</span></span>

<span data-ttu-id="d85db-108">La solicitud de operación **GetClientAccessToken** toma dos argumentos obligatorios: el identificador de la aplicación y el tipo de token.</span><span class="sxs-lookup"><span data-stu-id="d85db-108">The **GetClientAccessToken** operation request takes two required arguments: the identifier of the app, and the token type.</span></span> <span data-ttu-id="d85db-109">Puede usar la [operación GetAppManifests](getappmanifests-operation.md) para solicitar el identificador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d85db-109">You can use the [GetAppManifests operation](getappmanifests-operation.md) to request the app identifier.</span></span> 
  
### <a name="getclientaccesstoken-operation-soap-headers"></a><span data-ttu-id="d85db-110">Encabezados SOAP de operación GetClientAccessToken</span><span class="sxs-lookup"><span data-stu-id="d85db-110">GetClientAccessToken operation SOAP headers</span></span>

<span data-ttu-id="d85db-111">La operación **GetClientAccessToken** puede usar los encabezados SOAP que se enumeran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="d85db-111">The **GetClientAccessToken** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="d85db-112">**Nombre de encabezado**</span><span class="sxs-lookup"><span data-stu-id="d85db-112">**Header name**</span></span>|<span data-ttu-id="d85db-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="d85db-113">**Element**</span></span>|<span data-ttu-id="d85db-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d85db-114">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d85db-115">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="d85db-115">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="d85db-116">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="d85db-116">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="d85db-117">Identifica la versión del esquema para la solicitud de operación.</span><span class="sxs-lookup"><span data-stu-id="d85db-117">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="d85db-118">Este encabezado se aplica a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="d85db-118">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="d85db-119">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="d85db-119">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="d85db-120">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="d85db-120">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="d85db-121">Identifica la versión del servidor que respondió a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d85db-121">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="d85db-122">Este encabezado se aplica a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="d85db-122">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getclientaccesstoken-operation-request-example-get-a-caller-identity-token"></a><span data-ttu-id="d85db-123">Ejemplo de solicitud de operación GetClientAccessToken: obtener un token de identidad de llamada</span><span class="sxs-lookup"><span data-stu-id="d85db-123">GetClientAccessToken operation request example: Get a caller identity token</span></span>

<span data-ttu-id="d85db-124">El siguiente ejemplo de una solicitud de operación de **GetClientAccessToken** muestra cómo obtener un token de identidad de llamada para una aplicación.</span><span class="sxs-lookup"><span data-stu-id="d85db-124">The following example of a **GetClientAccessToken** operation request shows how to get a caller identity token for an app.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:GetClientAccessToken>
         <m:TokenRequests>
            <t:TokenRequest>
               <t:Id>1C50226D-04B5-4AB2-9FCD-42E236B59E4B</t:Id>
               <t:TokenType>CallerIdentity</t:TokenType>
            </t:TokenRequest>
         </m:TokenRequests>
      </m:GetClientAccessToken>
   </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="d85db-125">El cuerpo SOAP de la solicitud contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="d85db-125">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="d85db-126">GetClientAccessToken</span><span class="sxs-lookup"><span data-stu-id="d85db-126">GetClientAccessToken</span></span>](getclientaccesstoken.md)
    
- [<span data-ttu-id="d85db-127">TokenRequests</span><span class="sxs-lookup"><span data-stu-id="d85db-127">TokenRequests</span></span>](tokenrequests.md)
    
- [<span data-ttu-id="d85db-128">TokenRequest</span><span class="sxs-lookup"><span data-stu-id="d85db-128">TokenRequest</span></span>](tokenrequest.md)
    
- [<span data-ttu-id="d85db-129">ID (cadena)</span><span class="sxs-lookup"><span data-stu-id="d85db-129">ID (String)</span></span>](id-string.md)
    
- [<span data-ttu-id="d85db-130">TokenType</span><span class="sxs-lookup"><span data-stu-id="d85db-130">TokenType</span></span>](tokentype.md)
    
## <a name="successful-getclientaccesstoken-operation-response"></a><span data-ttu-id="d85db-131">Respuesta de operación GetClientAccessToken correcta</span><span class="sxs-lookup"><span data-stu-id="d85db-131">Successful GetClientAccessToken operation response</span></span>

<span data-ttu-id="d85db-132">En el siguiente ejemplo se muestra una respuesta correcta a una solicitud de operación de **GetClientAccessToken** para obtener un token de identidad de llamada para una aplicación.</span><span class="sxs-lookup"><span data-stu-id="d85db-132">The following example shows a successful response to a **GetClientAccessToken** operation request to get a caller identity token for an app.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d85db-133">Los valores de token de este artículo se han reducido para preservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="d85db-133">The token values in this article have been shortened to preserve readability.</span></span> 
  
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
      <m:GetClientAccessTokenResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
         <m:ResponseMessages>
            <m:GetClientAccessTokenResponseMessage ResponseClass="Success">
               <m:ResponseCode>NoError</m:ResponseCode>
               <m:Token>
                  <t:Id>1C50226D-04B5-4AB2-9FCD-42E236B59E4B</t:Id>
                  <t:TokenType>CallerIdentity</t:TokenType>
                  <t:TokenValue>eyJ0eXAmv0QitaJg</t:TokenValue>
                  <t:TTL>479</t:TTL>
               </m:Token>
            </m:GetClientAccessTokenResponseMessage>
         </m:ResponseMessages>
      </m:GetClientAccessTokenResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="d85db-134">El cuerpo SOAP de respuesta contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="d85db-134">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="d85db-135">GetClientAccessTokenResponse</span><span class="sxs-lookup"><span data-stu-id="d85db-135">GetClientAccessTokenResponse</span></span>](getclientaccesstokenresponse.md)
    
- [<span data-ttu-id="d85db-136">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="d85db-136">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="d85db-137">GetClientAccessTokenResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d85db-137">GetClientAccessTokenResponseMessage</span></span>](getclientaccesstokenresponsemessage.md)
    
- [<span data-ttu-id="d85db-138">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="d85db-138">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="d85db-139">Token (ClientAccessTokenType)</span><span class="sxs-lookup"><span data-stu-id="d85db-139">Token (ClientAccessTokenType)</span></span>](token-clientaccesstokentype.md)
    
- [<span data-ttu-id="d85db-140">ID (cadena)</span><span class="sxs-lookup"><span data-stu-id="d85db-140">ID (String)</span></span>](id-string.md)
    
- [<span data-ttu-id="d85db-141">TokenType (ClientAccessTokenType)</span><span class="sxs-lookup"><span data-stu-id="d85db-141">TokenType (ClientAccessTokenType)</span></span>](tokentype-clientaccesstokentype.md)
    
- [<span data-ttu-id="d85db-142">TokenValue</span><span class="sxs-lookup"><span data-stu-id="d85db-142">TokenValue</span></span>](tokenvalue.md)
    
- [<span data-ttu-id="d85db-143">TTL (ClientAccessTokenTypeType)</span><span class="sxs-lookup"><span data-stu-id="d85db-143">TTL (ClientAccessTokenTypeType)</span></span>](ttl-clientaccesstokentypetype.md)
    
## <a name="getclientaccesstoken-operation-error-response"></a><span data-ttu-id="d85db-144">Respuesta de error de operación de GetClientAccessToken</span><span class="sxs-lookup"><span data-stu-id="d85db-144">GetClientAccessToken operation error response</span></span>

<span data-ttu-id="d85db-145">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **GetClientAccessToken** .</span><span class="sxs-lookup"><span data-stu-id="d85db-145">The following example shows an error response to a **GetClientAccessToken** operation request.</span></span> <span data-ttu-id="d85db-146">Se trata de una respuesta a una solicitud para obtener un token de devolución de llamada de extensión sin los permisos adecuados.</span><span class="sxs-lookup"><span data-stu-id="d85db-146">This is a response to a request to get an extension callback token without the appropriate permissions.</span></span> 
  
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
      <m:GetClientAccessTokenResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
         <m:ResponseMessages>
            <m:GetClientAccessTokenResponseMessage ResponseClass="Error">
               <m:MessageText>The caller does not have enough permission for this token request.</m:MessageText>
               <m:ResponseCode>ErrorInvalidClientAccessTokenRequest</m:ResponseCode>
               <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
            </m:GetClientAccessTokenResponseMessage>
         </m:ResponseMessages>
      </m:GetClientAccessTokenResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="d85db-147">El cuerpo SOAP de respuesta de error contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="d85db-147">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="d85db-148">GetClientAccessTokenResponse</span><span class="sxs-lookup"><span data-stu-id="d85db-148">GetClientAccessTokenResponse</span></span>](getclientaccesstokenresponse.md)
    
- [<span data-ttu-id="d85db-149">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="d85db-149">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="d85db-150">GetClientAccessTokenResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d85db-150">GetClientAccessTokenResponseMessage</span></span>](getclientaccesstokenresponsemessage.md)
    
- [<span data-ttu-id="d85db-151">MessageText</span><span class="sxs-lookup"><span data-stu-id="d85db-151">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="d85db-152">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="d85db-152">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="d85db-153">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="d85db-153">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="d85db-154">Para obtener los códigos de error adicionales que son genéricos para EWS y específicos de esta operación, vea [ResponseCode](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="d85db-154">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d85db-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="d85db-155">See also</span></span>

- [<span data-ttu-id="d85db-156">Operaciones de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="d85db-156">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="d85db-157">Operación GetAppManifests</span><span class="sxs-lookup"><span data-stu-id="d85db-157">GetAppManifests operation</span></span>](getappmanifests-operation.md)
    
- [<span data-ttu-id="d85db-158">Complementos de Outlook</span><span class="sxs-lookup"><span data-stu-id="d85db-158">Outlook add-ins</span></span>](https://msdn.microsoft.com/library/71e64bc9-e347-4f5d-8948-0a47b5dd93e6%28Office.15%29.aspx)
    

