---
title: Operación GetSharingMetadata
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetSharingMetadata
api_type:
- schema
ms.assetid: eaf29427-ecf8-4a5e-9a54-db2e6414b35e
description: La operación GetSharingMetadata Obtiene un token de autenticación opaco que identifica una invitación para compartir.
ms.openlocfilehash: e2e04d83310e7a8a731cca655a432325574cd9e8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19835671"
---
# <a name="getsharingmetadata-operation"></a><span data-ttu-id="6427e-103">Operación GetSharingMetadata</span><span class="sxs-lookup"><span data-stu-id="6427e-103">GetSharingMetadata operation</span></span>

<span data-ttu-id="6427e-104">La operación **GetSharingMetadata** Obtiene un token de autenticación opaco que identifica una invitación para compartir.</span><span class="sxs-lookup"><span data-stu-id="6427e-104">The **GetSharingMetadata** operation gets an opaque authentication token that identifies a sharing invitation.</span></span> 
  
## <a name="soap-headers"></a><span data-ttu-id="6427e-105">Encabezados SOAP</span><span class="sxs-lookup"><span data-stu-id="6427e-105">SOAP Headers</span></span>

<span data-ttu-id="6427e-106">La operación de **GetSharingMetadata** puede utilizar los encabezados SOAP que se enumeran y describen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="6427e-106">The **GetSharingMetadata** operation can use the SOAP headers that are listed and described in the following table.</span></span> 
  
|<span data-ttu-id="6427e-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="6427e-107">**Header**</span></span>|<span data-ttu-id="6427e-108">**Element**</span><span class="sxs-lookup"><span data-stu-id="6427e-108">**Element**</span></span>|<span data-ttu-id="6427e-109">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6427e-109">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6427e-110">RequestVersion</span><span class="sxs-lookup"><span data-stu-id="6427e-110">RequestVersion</span></span>  <br/> |[<span data-ttu-id="6427e-111">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="6427e-111">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="6427e-112">Identifica la versión del esquema para la solicitud de la operación.</span><span class="sxs-lookup"><span data-stu-id="6427e-112">Identifies the schema version for the operation request.</span></span>  <br/> |
|<span data-ttu-id="6427e-113">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="6427e-113">ServerVersion</span></span>  <br/> |[<span data-ttu-id="6427e-114">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="6427e-114">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="6427e-115">Identifica la versión del servidor que ha respondido a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6427e-115">Identifies the version of the server that responded to the request.</span></span>  <br/> |
   
## <a name="getsharingmetadata-request-example"></a><span data-ttu-id="6427e-116">Ejemplo de solicitud de GetSharingMetadata</span><span class="sxs-lookup"><span data-stu-id="6427e-116">GetSharingMetadata request example</span></span>

### <a name="description"></a><span data-ttu-id="6427e-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="6427e-117">Description</span></span>

<span data-ttu-id="6427e-118">En el ejemplo siguiente se muestra cómo formar una solicitud para obtener un token de autenticación opaco que identifica una invitación para compartir.</span><span class="sxs-lookup"><span data-stu-id="6427e-118">The following example shows how to form a request to get an opaque authentication token that identifies a sharing invitation.</span></span> <span data-ttu-id="6427e-119">En este ejemplo, user1@contoso.com desea compartir la carpeta que se especifica mediante el elemento de [IdOfFolderToShare](idoffoldertoshare.md) con user1@fabikam.com y user2@test.com.</span><span class="sxs-lookup"><span data-stu-id="6427e-119">In this example, user1@contoso.com wants to share the folder that is specified by the [IdOfFolderToShare](idoffoldertoshare.md) element with user1@fabikam.com and user2@test.com.</span></span> 
  
### <a name="code"></a><span data-ttu-id="6427e-120">Código</span><span class="sxs-lookup"><span data-stu-id="6427e-120">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010"/>
  </soap:Header>
  <soap:Body>
    <m:GetSharingMetadata>
      <m:IdOfFolderToShare Id="AAMkAD=" ChangeKey="AwAAA=" />
      <m:SenderSmtpAddress>user1@contoso.com</m:SenderSmtpAddress>
      <m:Recipients>
        <t:SmtpAddress>user1@fabrikam.com</t:SmtpAddress>
        <t:SmtpAddress>user2@test.com</t:SmtpAddress>
      </m:Recipients>
    </m:GetSharingMetadata>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="6427e-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6427e-121">Comments</span></span>

<span data-ttu-id="6427e-122">El elemento de [destinatarios (ArrayOfSmtpAddressType)](recipients-arrayofsmtpaddresstype.md) contiene un elemento [SmtpAddress](smtpaddress.md) para cada destinatario de la invitación para compartir.</span><span class="sxs-lookup"><span data-stu-id="6427e-122">The [Recipients (ArrayOfSmtpAddressType)](recipients-arrayofsmtpaddresstype.md) element contains one [SmtpAddress](smtpaddress.md) element for each intended recipient of the sharing invitation.</span></span> 
  
## <a name="successful-getsharingmetadata-response"></a><span data-ttu-id="6427e-123">GetSharingMetadata la respuesta es correcta</span><span class="sxs-lookup"><span data-stu-id="6427e-123">Successful GetSharingMetadata Response</span></span>

### <a name="description"></a><span data-ttu-id="6427e-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="6427e-124">Description</span></span>

<span data-ttu-id="6427e-125">En el ejemplo siguiente se muestra una respuesta a una solicitud **GetSharingMetadata** correcta.</span><span class="sxs-lookup"><span data-stu-id="6427e-125">The following example shows a successful response to a **GetSharingMetadata** request.</span></span> <span data-ttu-id="6427e-126">En este ejemplo, se han especificado los dos destinatarios en la solicitud **GetSharingMetadata** correspondiente: user1@fabrikam.com y user2@test.com.</span><span class="sxs-lookup"><span data-stu-id="6427e-126">In this example, two recipients were specified in the corresponding **GetSharingMetadata** request: user1@fabrikam.com and user2@test.com.</span></span> 
  
### <a name="code"></a><span data-ttu-id="6427e-127">Código</span><span class="sxs-lookup"><span data-stu-id="6427e-127">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="0" 
                         MajorBuildNumber="639" 
                         MinorBuildNumber="11" 
                         Version="Exchange2010" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetSharingMetadataResponseMessage ResponseClass="Success" 
                                xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
                                xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                                xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseCode>NoError</ResponseCode>
      <m:EncryptedSharedFolderDataCollection>
        <t:EncryptedSharedFolderData>
          <t:Token>
            <EncryptedData Id="Assertion0" Type="http://www.w3.org/2001/04/xmlenc#Element" xmlns="http://www.w3.org/2001/04/xmlenc#">
              <EncryptionMethod Algorithm="http://www.w3.org/2001/04/xmlenc#tripledes-cbc"></EncryptionMethod>
              <ds:KeyInfo xmlns:ds="http://www.w3.org/2000/09/xmldsig#">
                <EncryptedKey>
                  <EncryptionMethod Algorithm="http://www.w3.org/2001/04/xmlenc#rsa-oaep-mgf1p"></EncryptionMethod>
                  <ds:KeyInfo Id="keyinfo">
                    <wsse:SecurityTokenReference xmlns:wsse="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-secext-1.0.xsd">
                      <wsse:KeyIdentifier 
                                  EncodingType="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-soap-message-security-1.0#Base64Binary" 
                                  ValueType="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-x509-token-profile-1.0#X509SubjectKeyIdentifier">
                        B4VEEAf=
                      </wsse:KeyIdentifier>
                    </wsse:SecurityTokenReference>
                  </ds:KeyInfo>
                  <CipherData>
                    <CipherValue>GI/Dxqvw2na==</CipherValue>
                  </CipherData>
                </EncryptedKey>
              </ds:KeyInfo>
              <CipherData>
                <CipherValue>L77I7Hr06z</CipherValue>
              </CipherData>
            </EncryptedData>
          </t:Token>
          <t:Data>
            <EncryptedData Type="http://www.w3.org/2001/04/xmlenc#Element" xmlns="http://www.w3.org/2001/04/xmlenc#">
              <EncryptionMethod Algorithm="http://www.w3.org/2001/04/xmlenc#aes256-cbc" />
              <KeyInfo xmlns="http://www.w3.org/2000/09/xmldsig#">
                <EncryptedKey xmlns="http://www.w3.org/2001/04/xmlenc#">
                  <EncryptionMethod Algorithm="http://www.w3.org/2001/04/xmlenc#kw-tripledes" />
                  <KeyInfo xmlns="http://www.w3.org/2000/09/xmldsig#">
                    <KeyName>key</KeyName>
                  </KeyInfo>
                  <CipherData>
                    <CipherValue>9UgtjrHiU</CipherValue>
                  </CipherData>
                </EncryptedKey>
              </KeyInfo>
              <CipherData>
                <CipherValue>NCNsJoGtQ==</CipherValue>
              </CipherData>
            </EncryptedData>
          </t:Data>
        </t:EncryptedSharedFolderData>
      </m:EncryptedSharedFolderDataCollection>
      <m:InvalidRecipients>
        <t:InvalidRecipient>
          <t:SmtpAddress>user2@test.com</t:SmtpAddress>
          <t:ResponseCode>RecipientOrganizationNotFederated</t:ResponseCode>
          <m:MessageText>The organization of these recipients is not federated for external sharing.</m:MessageText>
        </t:InvalidRecipient>
      </m:InvalidRecipients>
    </GetSharingMetadataResponseMessage>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="6427e-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6427e-128">Comments</span></span>

<span data-ttu-id="6427e-129">La respuesta contiene un elemento [EncryptedSharedFolderData](encryptedsharedfolderdata.md) para cada organización que está representada por destinatarios válidos que se especifican en la solicitud **GetSharingMetadata** .</span><span class="sxs-lookup"><span data-stu-id="6427e-129">The response contains one [EncryptedSharedFolderData](encryptedsharedfolderdata.md) element for each organization that is represented by valid recipients that are specified in the **GetSharingMetadata** request.</span></span> 
  
<span data-ttu-id="6427e-130">La solicitud de **GetSharingMetadata** se realizará correctamente, incluso si se especifican los destinatarios no válidos en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6427e-130">The **GetSharingMetadata** request will succeed even if invalid recipients are specified in the request.</span></span> <span data-ttu-id="6427e-131">El elemento [InvalidRecipients](invalidrecipients.md) contiene información acerca de los destinatarios no válidos.</span><span class="sxs-lookup"><span data-stu-id="6427e-131">The [InvalidRecipients](invalidrecipients.md) element contains information about invalid recipients.</span></span> <span data-ttu-id="6427e-132">Para obtener información acerca de los motivos por qué un destinatario podría no ser válido, vea [ResponseCode (InvalidRecipientResponseCodeType)](responsecode-invalidrecipientresponsecodetype.md).</span><span class="sxs-lookup"><span data-stu-id="6427e-132">For information about the reasons why a recipient might be invalid, see [ResponseCode (InvalidRecipientResponseCodeType)](responsecode-invalidrecipientresponsecodetype.md).</span></span>
  
<span data-ttu-id="6427e-133">Si todos los destinatarios a los que no son válidos, el elemento [EncryptedSharedFolderDataCollection](encryptedsharedfolderdatacollection.md) estará vacío.</span><span class="sxs-lookup"><span data-stu-id="6427e-133">If all intended recipients are invalid, the [EncryptedSharedFolderDataCollection](encryptedsharedfolderdatacollection.md) element will be empty.</span></span> 
  
## <a name="getsharingmetadata-error-response"></a><span data-ttu-id="6427e-134">Respuesta de error de GetSharingMetadata</span><span class="sxs-lookup"><span data-stu-id="6427e-134">GetSharingMetadata error response</span></span>

### <a name="description"></a><span data-ttu-id="6427e-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="6427e-135">Description</span></span>

<span data-ttu-id="6427e-136">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de **GetSharingMetadata** .</span><span class="sxs-lookup"><span data-stu-id="6427e-136">The following example shows an error response to a **GetSharingMetadata** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="6427e-137">Código</span><span class="sxs-lookup"><span data-stu-id="6427e-137">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="0" 
                         MajorBuildNumber="639" 
                         MinorBuildNumber="11" 
                         Version="Exchange2010" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetSharingMetadataResponseMessage ResponseClass="Error" 
                                xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
                                xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                                xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:MessageText>The SMTP address format is invalid.</MessageText>
      <m:ResponseCode>ErrorInvalidSmtpAddress</ResponseCode>
      <m:DescriptiveLinkKey>0</DescriptiveLinkKey>
    </GetSharingMetadataResponseMessage>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="6427e-138">Ver también</span><span class="sxs-lookup"><span data-stu-id="6427e-138">See also</span></span>



[<span data-ttu-id="6427e-139">GetSharingMetadata</span><span class="sxs-lookup"><span data-stu-id="6427e-139">GetSharingMetadata</span></span>](getsharingmetadata.md)
  
[<span data-ttu-id="6427e-140">GetSharingMetadataType</span><span class="sxs-lookup"><span data-stu-id="6427e-140">GetSharingMetadataType</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.GetSharingMetadataType.aspx)
  
[<span data-ttu-id="6427e-141">GetSharingMetadataResponseMessage</span><span class="sxs-lookup"><span data-stu-id="6427e-141">GetSharingMetadataResponseMessage</span></span>](getsharingmetadataresponsemessage.md)
  
[<span data-ttu-id="6427e-142">GetSharingMetadataResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="6427e-142">GetSharingMetadataResponseMessageType</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.GetSharingMetadataResponseMessageType.aspx)


[<span data-ttu-id="6427e-143">Operaciones de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="6427e-143">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
  
- [<span data-ttu-id="6427e-144">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="6427e-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

