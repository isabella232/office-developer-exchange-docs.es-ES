---
title: Operación RefreshSharingFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- RefreshSharingFolder
api_type:
- schema
ms.assetid: 1b047e34-40f0-459f-ac9e-e9f8e7349479
description: La operación RefreshSharingFolder actualiza la carpeta local especificada con los datos más recientes de la carpeta que se está compartiendo.
ms.openlocfilehash: 4bf30132d84c4288123c91247afa8bd13a05348c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59512544"
---
# <a name="refreshsharingfolder-operation"></a>Operación RefreshSharingFolder

La **operación RefreshSharingFolder** actualiza la carpeta local especificada con los datos más recientes de la carpeta que se está compartiendo. 
  
## <a name="soap-headers"></a>Encabezados SOAP

La **operación RefreshSharingFolder** puede usar los encabezados SOAP que se enumeran y se describen en la tabla siguiente. 
  
|**Header**|**Elemento**|**Descripción**|
|:-----|:-----|:-----|
|RequestVersion  <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Identifica la versión del esquema para la solicitud de operación.  <br/> |
|ServerVersion  <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Identifica la versión del servidor que respondió a la solicitud.  <br/> |
   
## <a name="refreshsharingfolder-request-example"></a>Ejemplo de solicitud RefreshSharingFolder

### <a name="description"></a>Descripción

En el ejemplo siguiente se muestra cómo formar una solicitud para actualizar la carpeta local especificada con los datos más recientes de la carpeta que se está compartindo. El [elemento SharingFolderId](sharingfolderid.md) especifica el identificador de la carpeta local que se va a actualizar. 
  
### <a name="code"></a>Código

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
    <RefreshSharingFolder xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:SharingFolderId Id="AAMkAD=" ChangeKey="AwAAA=" />
    </RefreshSharingFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a>Elementos Request

En la solicitud se usan los siguientes elementos:
  
- [RequestServerVersion](requestserverversion.md)
    
- [RefreshSharingFolder](refreshsharingfolder.md)
    
- [SharingFolderId](sharingfolderid.md)
    
## <a name="successful-refreshsharingfolder-response"></a>Respuesta refreshSharingFolder correcta

### <a name="description"></a>Descripción

En el ejemplo siguiente se muestra una respuesta correcta a una **solicitud RefreshSharingFolder.** 
  
### <a name="code"></a>Código

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
    <RefreshSharingFolderResponseMessage ResponseClass="Success"
                                xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                                xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                                xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseCode>NoError</m:ResponseCode>
    </RefreshSharingFolderResponseMessage>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-response-elements"></a>Elementos de respuesta correctos

En la respuesta se usan los siguientes elementos:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [RefreshSharingFolderResponseMessage](refreshsharingfolderresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
## <a name="refreshsharingfolder-error-response"></a>Respuesta de error RefreshSharingFolder

### <a name="description"></a>Descripción

En el ejemplo siguiente se muestra una respuesta de error a una **solicitud RefreshSharingFolder.** En este ejemplo, se ha producido un error en la solicitud **RefreshSharingFolder** porque no se encontró una suscripción que corresponda a la carpeta local especificada. 
  
### <a name="code"></a>Código

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
    <RefreshSharingFolderResponseMessage ResponseClass="Error"
                                xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                                xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                                xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:MessageText>Failed to synchronize the sharing folder.</m:MessageText>
      <m:ResponseCode>ErrorSharingSynchronizationFailed</m:ResponseCode>
      <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
      <m:MessageXml>
        <t:Value Name="ErrorDetails">Microsoft.Exchange.InfoWorker.Common.Sharing.SubscriptionNotFoundException: The subscription wasn't found.;</t:Value>
      </m:MessageXml>
    </RefreshSharingFolderResponseMessage>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a>Elementos de respuesta de error

En la respuesta de error se usan los siguientes elementos:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [RefreshSharingFolderResponseMessage](refreshsharingfolderresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
- [MessageXml](messagexml.md)
    
## <a name="see-also"></a>Ver también



[RefreshSharingFolder](refreshsharingfolder.md)
  
[RefreshSharingFolderType](https://msdn.microsoft.com/library/ExchangeWebServices.RefreshSharingFolderType.aspx)
  
[RefreshSharingFolderResponseMessage](refreshsharingfolderresponsemessage.md)
  
[RefreshSharingFolderResponseMessageType](https://msdn.microsoft.com/library/ExchangeWebServices.RefreshSharingFolderResponseMessageType.aspx)


[Operaciones ews en Exchange](ews-operations-in-exchange.md)
  
- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

