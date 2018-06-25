---
title: Operación GetSharingFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetSharingFolder
api_type:
- schema
ms.assetid: 75fee92a-a7f8-4a62-ad2b-17acbaada186
description: La operación GetSharingFolder Obtiene el identificador de la carpeta local de una carpeta compartida especificada.
ms.openlocfilehash: 23adb10b22623fcbc1dd6b33bd674afafdaa8b19
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835670"
---
# <a name="getsharingfolder-operation"></a>Operación GetSharingFolder

La operación **GetSharingFolder** Obtiene el identificador de la carpeta local de una carpeta compartida especificada. 
  
## <a name="soap-headers"></a>Encabezados SOAP

La operación de **GetSharingFolder** puede utilizar los encabezados SOAP que se enumeran y describen en la tabla siguiente. 
  
|**Header**|**Element**|**Descripción**|
|:-----|:-----|:-----|
|RequestVersion  <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Identifica la versión del esquema para la solicitud de la operación.  <br/> |
|ServerVersion  <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Identifica la versión del servidor que ha respondido a la solicitud.  <br/> |
   
## <a name="getsharingfolder-request-example"></a>Ejemplo de solicitud de GetSharingFolder

### <a name="getting-the-local-folder-identifier-by-specifying-the-sharedfolderid-element-of-the-folder-being-shared"></a>Obtener el identificador de la carpeta Local mediante la especificación del elemento SharedFolderId de la carpeta que se está compartida

En el ejemplo de código siguiente se muestra cómo formar una solicitud para obtener el identificador de la carpeta local que corresponde a la carpeta que se está compartiendo. La carpeta que se está compartiendo se identifica con la dirección SMTP del buzón que contiene la carpeta que se está compartiendo y por el elemento [SharedFolderId](sharedfolderid.md) que representa el identificador de esa carpeta. En este ejemplo, la carpeta que se está compartiendo la propiedad user1@contoso.com. 
  
### <a name="code"></a>Código

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
    <m:GetSharingFolder>
      <m:SmtpAddress>user1@contoso.com</m:SmtpAddress>
      <m:SharedFolderId>AAMkA=</m:SharedFolderId>
    </m:GetSharingFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="getting-the-local-folder-identifier-by-specifying-the-datatype-element-of-the-folder-being-shared"></a>Obtener el identificador de la carpeta Local especificando el tipo del elemento de la carpeta que se está compartida

En el ejemplo de código siguiente se muestra cómo formar una solicitud para obtener el identificador de la carpeta local que corresponde a la carpeta que se está compartiendo. La carpeta que se está compartiendo se identifica con la dirección SMTP del buzón que contiene la carpeta que se está compartiendo y por el elemento de [tipo de datos](datatype.md) que representa el tipo de datos en esa carpeta. En este ejemplo, la carpeta que se está compartiendo es la carpeta de contactos cuyo propietario es user1@contoso.com. 
  
### <a name="code"></a>Código

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
    <m:GetSharingFolder>
      <m:SmtpAddress>user1@contoso.com</m:SmtpAddress>
      <m:DataType>Contacts</m:DataType>
    </m:GetSharingFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Comentarios

Para obtener información acerca de los valores posibles del elemento de **tipo de datos** , vea el [tipo de datos](datatype.md).
  
## <a name="successful-getsharingfolder-response"></a>GetSharingFolder la respuesta es correcta

### <a name="description"></a>Descripción

En el ejemplo siguiente se muestra una respuesta a una solicitud **GetSharingFolder** correcta. El atributo **Id** del elemento [SharingFolderId](sharingfolderid.md) representa el identificador de la carpeta local en la relación de uso compartida. 
  
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
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetSharingFolderResponseMessage ResponseClass="Success"
                                xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
                                xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                                xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseCode>NoError</m:ResponseCode>
      <m:SharingFolderId Id="AAMkAD=" ChangeKey="AwAAA=" />
    </GetSharingFolderResponseMessage>
  </soap:Body>
</soap:Envelope>
```

## <a name="getsharingfolder-error-response"></a>Respuesta de error de GetSharingFolder

### <a name="description"></a>Descripción

En el ejemplo siguiente se muestra una respuesta de error a una solicitud de **GetSharingFolder** . En este ejemplo, se produjo el error debido a que la solicitud de los elementos de la [SharingFolderId](sharingfolderid.md) y el [tipo de datos](datatype.md) especificados. Tenga en cuenta que sólo uno u otro de esos dos elementos puede especificarse, pero no ambos. 
  
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
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetSharingFolderResponseMessage ResponseClass="Error" 
                                xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
                                xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                                xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:MessageText>Either DataType or SharedFolderId must be specified, but not both.</m:MessageText>
      <m:ResponseCode>ErrorInvalidGetSharingFolderRequest</m:ResponseCode>
      <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
    </GetSharingFolderResponseMessage>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>Vea también



[GetSharingFolder](getsharingfolder.md)
  
[GetSharingFolderType](https://msdn.microsoft.com/library/ExchangeWebServices.GetSharingFolderType.aspx)
  
[GetSharingFolderResponseMessage](getsharingfolderresponsemessage.md)
  
[GetSharingFolderResponseMessageType](https://msdn.microsoft.com/library/ExchangeWebServices.GetSharingFolderResponseMessageType.aspx)


[Operaciones de EWS en Exchange](ews-operations-in-exchange.md)
  
- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

