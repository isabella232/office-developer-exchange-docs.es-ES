---
title: Operación GetSharingFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- GetSharingFolder
api_type:
- schema
ms.assetid: 75fee92a-a7f8-4a62-ad2b-17acbaada186
description: La operación GetSharingFolder obtiene el identificador de carpeta local de una carpeta compartida especificada.
ms.openlocfilehash: 20ee49b85d026ec2c14794599e0713b9939384eb
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59515827"
---
# <a name="getsharingfolder-operation"></a>Operación GetSharingFolder

La **operación GetSharingFolder** obtiene el identificador de carpeta local de una carpeta compartida especificada. 
  
## <a name="soap-headers"></a>Encabezados SOAP

La **operación GetSharingFolder** puede usar los encabezados SOAP que se enumeran y describen en la tabla siguiente. 
  
|**Header**|**Elemento**|**Descripción**|
|:-----|:-----|:-----|
|RequestVersion  <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Identifica la versión del esquema para la solicitud de operación.  <br/> |
|ServerVersion  <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Identifica la versión del servidor que respondió a la solicitud.  <br/> |
   
## <a name="getsharingfolder-request-example"></a>Ejemplo de solicitud GetSharingFolder

### <a name="getting-the-local-folder-identifier-by-specifying-the-sharedfolderid-element-of-the-folder-being-shared"></a>Obtener el identificador de carpeta local especificando el elemento SharedFolderId de la carpeta que se comparte

En el siguiente ejemplo de código se muestra cómo formar una solicitud para obtener el identificador de la carpeta local que corresponde a la carpeta que se está compartindo. La carpeta que se comparte se identifica mediante la dirección SMTP del buzón que contiene la carpeta que se comparte y por el elemento [SharedFolderId](sharedfolderid.md) que representa el identificador de esa carpeta. En este ejemplo, la carpeta que se comparte es propiedad de user1@contoso.com. 
  
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
    <m:GetSharingFolder>
      <m:SmtpAddress>user1@contoso.com</m:SmtpAddress>
      <m:SharedFolderId>AAMkA=</m:SharedFolderId>
    </m:GetSharingFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="getting-the-local-folder-identifier-by-specifying-the-datatype-element-of-the-folder-being-shared"></a>Obtener el identificador de carpeta local especificando el elemento DataType de la carpeta que se comparte

En el siguiente ejemplo de código se muestra cómo formar una solicitud para obtener el identificador de la carpeta local que corresponde a la carpeta que se está compartindo. La carpeta que se comparte se identifica mediante la dirección SMTP del buzón que contiene la carpeta que se está compartindo y por el elemento [DataType](datatype.md) que representa el tipo de datos de esa carpeta. En este ejemplo, la carpeta que se comparte es la carpeta Contactos que es propiedad de user1@contoso.com. 
  
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
    <m:GetSharingFolder>
      <m:SmtpAddress>user1@contoso.com</m:SmtpAddress>
      <m:DataType>Contacts</m:DataType>
    </m:GetSharingFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Comentarios

Para obtener información sobre los valores posibles del **elemento DataType,** vea [DataType](datatype.md).
  
## <a name="successful-getsharingfolder-response"></a>Respuesta getSharingFolder correcta

### <a name="description"></a>Descripción

En el ejemplo siguiente se muestra una respuesta correcta a una **solicitud GetSharingFolder.** El **atributo Id** del elemento [SharingFolderId](sharingfolderid.md) representa el identificador de la carpeta local en la relación de uso compartido. 
  
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
    <GetSharingFolderResponseMessage ResponseClass="Success"
                                xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                                xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                                xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseCode>NoError</m:ResponseCode>
      <m:SharingFolderId Id="AAMkAD=" ChangeKey="AwAAA=" />
    </GetSharingFolderResponseMessage>
  </soap:Body>
</soap:Envelope>
```

## <a name="getsharingfolder-error-response"></a>Respuesta de error getSharingFolder

### <a name="description"></a>Descripción

En el ejemplo siguiente se muestra una respuesta de error a una **solicitud GetSharingFolder.** En este ejemplo, se produjo el error porque la solicitud especificaba los [elementos SharingFolderId](sharingfolderid.md) y [DataType.](datatype.md) Tenga en cuenta que solo se puede especificar uno u otro de esos dos elementos, pero no ambos. 
  
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
    <GetSharingFolderResponseMessage ResponseClass="Error" 
                                xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                                xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                                xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:MessageText>Either DataType or SharedFolderId must be specified, but not both.</m:MessageText>
      <m:ResponseCode>ErrorInvalidGetSharingFolderRequest</m:ResponseCode>
      <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
    </GetSharingFolderResponseMessage>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>Ver también



[GetSharingFolder](getsharingfolder.md)
  
[GetSharingFolderType](https://msdn.microsoft.com/library/ExchangeWebServices.GetSharingFolderType.aspx)
  
[GetSharingFolderResponseMessage](getsharingfolderresponsemessage.md)
  
[GetSharingFolderResponseMessageType](https://msdn.microsoft.com/library/ExchangeWebServices.GetSharingFolderResponseMessageType.aspx)


[Operaciones ews en Exchange](ews-operations-in-exchange.md)
  
- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

