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
description: La operación GetSharingMetadata obtiene un token de autenticación opaco que identifica una invitación de uso compartido.
ms.openlocfilehash: 0390b9caa7b2e9847b1e8dcdc1b911a35e3c5864
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530186"
---
# <a name="getsharingmetadata-operation"></a><span data-ttu-id="eb638-103">Operación GetSharingMetadata</span><span class="sxs-lookup"><span data-stu-id="eb638-103">GetSharingMetadata operation</span></span>

<span data-ttu-id="eb638-104">La operación **GetSharingMetadata** obtiene un token de autenticación opaco que identifica una invitación de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="eb638-104">The **GetSharingMetadata** operation gets an opaque authentication token that identifies a sharing invitation.</span></span> 
  
## <a name="soap-headers"></a><span data-ttu-id="eb638-105">Encabezados SOAP</span><span class="sxs-lookup"><span data-stu-id="eb638-105">SOAP Headers</span></span>

<span data-ttu-id="eb638-106">La operación **GetSharingMetadata** puede usar los encabezados SOAP que se enumeran y describen en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="eb638-106">The **GetSharingMetadata** operation can use the SOAP headers that are listed and described in the following table.</span></span> 
  
|<span data-ttu-id="eb638-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="eb638-107">**Header**</span></span>|<span data-ttu-id="eb638-108">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="eb638-108">**Element**</span></span>|<span data-ttu-id="eb638-109">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="eb638-109">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="eb638-110">RequestVersion</span><span class="sxs-lookup"><span data-stu-id="eb638-110">RequestVersion</span></span>  <br/> |[<span data-ttu-id="eb638-111">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="eb638-111">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="eb638-112">Identifica la versión del esquema para la solicitud de operación.</span><span class="sxs-lookup"><span data-stu-id="eb638-112">Identifies the schema version for the operation request.</span></span>  <br/> |
|<span data-ttu-id="eb638-113">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="eb638-113">ServerVersion</span></span>  <br/> |[<span data-ttu-id="eb638-114">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="eb638-114">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="eb638-115">Identifica la versión del servidor que respondió a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="eb638-115">Identifies the version of the server that responded to the request.</span></span>  <br/> |
   
## <a name="getsharingmetadata-request-example"></a><span data-ttu-id="eb638-116">Ejemplo de solicitud GetSharingMetadata</span><span class="sxs-lookup"><span data-stu-id="eb638-116">GetSharingMetadata request example</span></span>

### <a name="description"></a><span data-ttu-id="eb638-117">Description</span><span class="sxs-lookup"><span data-stu-id="eb638-117">Description</span></span>

<span data-ttu-id="eb638-118">En el siguiente ejemplo se muestra cómo crear una solicitud para obtener un token de autenticación opaco que identifique una invitación de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="eb638-118">The following example shows how to form a request to get an opaque authentication token that identifies a sharing invitation.</span></span> <span data-ttu-id="eb638-119">En este ejemplo, user1@contoso.com desea compartir la carpeta especificada por el elemento [IdOfFolderToShare](idoffoldertoshare.md) con user1@fabikam.com y user2@test.com.</span><span class="sxs-lookup"><span data-stu-id="eb638-119">In this example, user1@contoso.com wants to share the folder that is specified by the [IdOfFolderToShare](idoffoldertoshare.md) element with user1@fabikam.com and user2@test.com.</span></span> 
  
### <a name="code"></a><span data-ttu-id="eb638-120">Código</span><span class="sxs-lookup"><span data-stu-id="eb638-120">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

### <a name="comments"></a><span data-ttu-id="eb638-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="eb638-121">Comments</span></span>

<span data-ttu-id="eb638-122">El elemento [Recipients (ArrayOfSmtpAddressType)](recipients-arrayofsmtpaddresstype.md) contiene un elemento [SmtpAddress](smtpaddress.md) para cada destinatario previsto de la invitación para uso compartido.</span><span class="sxs-lookup"><span data-stu-id="eb638-122">The [Recipients (ArrayOfSmtpAddressType)](recipients-arrayofsmtpaddresstype.md) element contains one [SmtpAddress](smtpaddress.md) element for each intended recipient of the sharing invitation.</span></span> 
  
## <a name="successful-getsharingmetadata-response"></a><span data-ttu-id="eb638-123">Respuesta GetSharingMetadata correcta</span><span class="sxs-lookup"><span data-stu-id="eb638-123">Successful GetSharingMetadata Response</span></span>

### <a name="description"></a><span data-ttu-id="eb638-124">Description</span><span class="sxs-lookup"><span data-stu-id="eb638-124">Description</span></span>

<span data-ttu-id="eb638-125">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud **GetSharingMetadata** .</span><span class="sxs-lookup"><span data-stu-id="eb638-125">The following example shows a successful response to a **GetSharingMetadata** request.</span></span> <span data-ttu-id="eb638-126">En este ejemplo, se han especificado dos destinatarios en la solicitud **GetSharingMetadata** correspondiente: user1@fabrikam.com y user2@test.com.</span><span class="sxs-lookup"><span data-stu-id="eb638-126">In this example, two recipients were specified in the corresponding **GetSharingMetadata** request: user1@fabrikam.com and user2@test.com.</span></span> 
  
### <a name="code"></a><span data-ttu-id="eb638-127">Código</span><span class="sxs-lookup"><span data-stu-id="eb638-127">Code</span></span>

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
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetSharingMetadataResponseMessage ResponseClass="Success" 
                                xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                                xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                                xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a><span data-ttu-id="eb638-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="eb638-128">Comments</span></span>

<span data-ttu-id="eb638-129">La respuesta contiene un elemento [EncryptedSharedFolderData](encryptedsharedfolderdata.md) para cada organización representada por destinatarios válidos que se especifican en la solicitud **GetSharingMetadata** .</span><span class="sxs-lookup"><span data-stu-id="eb638-129">The response contains one [EncryptedSharedFolderData](encryptedsharedfolderdata.md) element for each organization that is represented by valid recipients that are specified in the **GetSharingMetadata** request.</span></span> 
  
<span data-ttu-id="eb638-130">La solicitud **GetSharingMetadata** se realizará correctamente incluso si se especifican destinatarios no válidos en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="eb638-130">The **GetSharingMetadata** request will succeed even if invalid recipients are specified in the request.</span></span> <span data-ttu-id="eb638-131">El elemento [InvalidRecipients](invalidrecipients.md) contiene información sobre los destinatarios no válidos.</span><span class="sxs-lookup"><span data-stu-id="eb638-131">The [InvalidRecipients](invalidrecipients.md) element contains information about invalid recipients.</span></span> <span data-ttu-id="eb638-132">Para obtener información sobre los motivos por los que un destinatario podría no ser válido, vea [ResponseCode (InvalidRecipientResponseCodeType)](responsecode-invalidrecipientresponsecodetype.md).</span><span class="sxs-lookup"><span data-stu-id="eb638-132">For information about the reasons why a recipient might be invalid, see [ResponseCode (InvalidRecipientResponseCodeType)](responsecode-invalidrecipientresponsecodetype.md).</span></span>
  
<span data-ttu-id="eb638-133">Si todos los destinatarios previstos no son válidos, el elemento [EncryptedSharedFolderDataCollection](encryptedsharedfolderdatacollection.md) estará vacío.</span><span class="sxs-lookup"><span data-stu-id="eb638-133">If all intended recipients are invalid, the [EncryptedSharedFolderDataCollection](encryptedsharedfolderdatacollection.md) element will be empty.</span></span> 
  
## <a name="getsharingmetadata-error-response"></a><span data-ttu-id="eb638-134">Respuesta de error de GetSharingMetadata</span><span class="sxs-lookup"><span data-stu-id="eb638-134">GetSharingMetadata error response</span></span>

### <a name="description"></a><span data-ttu-id="eb638-135">Description</span><span class="sxs-lookup"><span data-stu-id="eb638-135">Description</span></span>

<span data-ttu-id="eb638-136">En el ejemplo siguiente se muestra una respuesta de error a una solicitud **GetSharingMetadata** .</span><span class="sxs-lookup"><span data-stu-id="eb638-136">The following example shows an error response to a **GetSharingMetadata** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="eb638-137">Código</span><span class="sxs-lookup"><span data-stu-id="eb638-137">Code</span></span>

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
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetSharingMetadataResponseMessage ResponseClass="Error" 
                                xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                                xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                                xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:MessageText>The SMTP address format is invalid.</MessageText>
      <m:ResponseCode>ErrorInvalidSmtpAddress</ResponseCode>
      <m:DescriptiveLinkKey>0</DescriptiveLinkKey>
    </GetSharingMetadataResponseMessage>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="eb638-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="eb638-138">See also</span></span>



[<span data-ttu-id="eb638-139">GetSharingMetadata</span><span class="sxs-lookup"><span data-stu-id="eb638-139">GetSharingMetadata</span></span>](getsharingmetadata.md)
  
[<span data-ttu-id="eb638-140">GetSharingMetadataType</span><span class="sxs-lookup"><span data-stu-id="eb638-140">GetSharingMetadataType</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.GetSharingMetadataType.aspx)
  
[<span data-ttu-id="eb638-141">GetSharingMetadataResponseMessage</span><span class="sxs-lookup"><span data-stu-id="eb638-141">GetSharingMetadataResponseMessage</span></span>](getsharingmetadataresponsemessage.md)
  
[<span data-ttu-id="eb638-142">GetSharingMetadataResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="eb638-142">GetSharingMetadataResponseMessageType</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.GetSharingMetadataResponseMessageType.aspx)


[<span data-ttu-id="eb638-143">Operaciones de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="eb638-143">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
  
- [<span data-ttu-id="eb638-144">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="eb638-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

