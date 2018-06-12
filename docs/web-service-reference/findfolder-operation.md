---
title: FindFolder Operation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FindFolder
api_type:
- schema
ms.assetid: 7a9855aa-06cc-45ba-ad2a-645c15b7d031
description: La operación FindFolder usa los servicios Web de Exchange para buscar las subcarpetas de una carpeta identificada y devuelve un conjunto de propiedades que describen el conjunto de subcarpetas.
ms.openlocfilehash: 655455b46d4a3192b294bee9d85352d95ded49ae
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764618"
---
# <a name="findfolder-operation"></a>FindFolder Operation

La operación **FindFolder** usa los servicios Web de Exchange para buscar las subcarpetas de una carpeta identificada y devuelve un conjunto de propiedades que describen el conjunto de subcarpetas. 
  
## <a name="remarks"></a>Notas

FindFolder devuelve sólo el primer 512 bytes de cualquier propiedad que se pueden transmitir. Para Unicode, devuelve los primeros 255 caracteres mediante el uso de una cadena Unicode terminada en null.
  
No se puede realizar consultas de recorrido profundo en las carpetas públicas.
  
Las restricciones se permiten y deben usar sólo las propiedades de carpeta, no las propiedades del elemento. Las funcionalidades de ordenación no está disponible para las respuestas **FindFolder** . Las consultas agrupadas no están disponibles para las consultas de **FindFolder** . 
  
 **Nota** La operación **FindFolder** también se usa para buscar las carpetas administradas. 
  
### <a name="soap-headers"></a>Encabezados SOAP

La operación **FindFolder** puede usar los encabezados SOAP que se enumeran y describen en la tabla siguiente. 
  
|**Header**|**Element**|**Descripción**|
|:-----|:-----|:-----|
|Suplantación  <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Identifica el usuario que está realizando la suplantación de la aplicación cliente.  <br/> |
|MailboxCulture  <br/> |[MailboxCulture](mailboxculture.md) <br/> |Identifica la referencia cultural de RFC3066 va a usar para tener acceso al buzón.  <br/> |
|RequestVersion  <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Identifica la versión del esquema para la solicitud de la operación.  <br/> |
|ServerVersion  <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Identifica la versión del servidor que ha respondido a la solicitud.  <br/> |
|TimeZoneContext  <br/> |[TimeZoneContext](timezonecontext.md) <br/> |Identifica la zona horaria que se usará para todas las respuestas desde el servidor.  <br/> |
   
## <a name="findfolder-request-example"></a>Ejemplo de solicitud FindFolder

### <a name="description"></a>Descripción

El siguiente ejemplo de una solicitud de **FindFolder** muestra cómo formar una solicitud para buscar todas las carpetas que se encuentra en una bandeja de entrada. 
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindFolder Traversal="Shallow" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <FolderShape>
        <t:BaseShape>Default</t:BaseShape>
      </FolderShape>
      <ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox"/>
      </ParentFolderIds>
    </FindFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Comentarios

Usa el valor predeterminado para el [BaseShape](baseshape.md), la respuesta que devuelve el nombre de la carpeta, el identificador de la carpeta, el número de subcarpetas, el número de carpetas secundarias que se encuentran en la carpeta y el recuento de elementos no leídos.
  
### <a name="request-elements"></a>Elementos de solicitud

Esta solicitud **FindFolder** incluye los siguientes elementos: 
  
- [FindFolder](findfolder.md)
    
- [FolderShape](foldershape.md)
    
- [BaseShape](baseshape.md)
    
- [ParentFolderIds](parentfolderids.md)
    
- [DistinguishedFolderId](distinguishedfolderid.md)
    
 Para los elementos de solicitud **FindFolder** adicionales, vea el esquema. 
  
## <a name="findfolder-response-example"></a>Ejemplo de respuesta FindFolder

### <a name="description"></a>Descripción

El siguiente ejemplo de cuerpo de SOAP Simple Object Access Protocol () muestra una respuesta correcta a la solicitud de **FindFolder** . La respuesta contiene los elementos que se devuelven cuando se usa el valor predeterminado para la [BaseShape](baseshape.md) . 
  
> [!NOTE]
> El identificador de la carpeta y la clave de cambio se han abreviado para conservar la legibilidad. 
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="652" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <FindFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:FindFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder TotalItemsInView="1" IncludesLastItemInRange="true">
            <t:Folders>
              <t:Folder>
                <t:FolderId Id="AQAnAH" ChangeKey="AQAAABY" />
                <t:DisplayName>TestFolder</t:DisplayName>
                <t:TotalCount>0</t:TotalCount>
                <t:ChildFolderCount>0</t:ChildFolderCount>
                <t:UnreadCount>0</t:UnreadCount>
              </t:Folder>
            </t:Folders>
          </m:RootFolder>
        </m:FindFolderResponseMessage>
      </m:ResponseMessages>
    </FindFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="response-elements"></a>Elementos de respuesta

Las propiedades que se devuelven en la respuesta se determinan mediante el [BaseShape](baseshape.md) y el [AdditionalProperties](additionalproperties.md) si se usan. Una respuesta correcta de **FindFolder** incluye los siguientes elementos: 
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [FindFolderResponse](findfolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [FindFolderResponseMessage](findfolderresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [RootFolder (FindItemResponseMessage)](rootfolder-finditemresponsemessage.md)
    
- [Carpetas](folders-ex15websvcsotherref.md)
    
- [Folder](folder.md)
    
- [FolderId](folderid.md)
    
- [DisplayName (cadena)](displayname-string.md)
    
- [TotalCount](totalcount.md)
    
- [ChildFolderCount](childfoldercount.md)
    
- [UnreadCount](unreadcount.md)
    
### <a name="comments"></a>Comentarios

 **FindFolder** respuestas a una solicitud con la forma de respuesta **AllProperties** no devolverá el [TotalCount](totalcount.md) y los elementos de [UnreadCount](unreadcount.md) para las búsquedas de la carpeta pública. 
  
## <a name="findfolder-error-response-example"></a>Ejemplo de respuesta de FindFolder Error

### <a name="description"></a>Descripción

El siguiente ejemplo de cuerpo SOAP muestra una respuesta de error que se produce cuando se busca una carpeta que se identifica con un identificador de la carpeta con formato incorrecto.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
                 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                 xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="652" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <FindFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:FindFolderResponseMessage ResponseClass="Error">
          <m:MessageText>Id is malformed.</m:MessageText>
          <m:ResponseCode>ErrorInvalidIdMalformed</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:FindFolderResponseMessage>
      </m:ResponseMessages>
    </FindFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a>Elementos de respuesta de error

La respuesta de error **FindFolder** incluye los siguientes elementos: 
  
- [FindFolderResponse](findfolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
## <a name="additional-information"></a>Información adicional

- El elemento [DisplayName (string)](displayname-string.md) de carpeta siempre se incluye en la forma predeterminada. 
    
- El elemento [UnreadCount](unreadcount.md) está incluido en las carpetas de tareas y notas. 
    
- Use el valor de **PropertyTag** de 0x672D con un tipo de propiedad de **entero** para identificar una carpeta administrada mediante el elemento [ExtendedFieldURI](extendedfielduri.md) . 
    
## <a name="see-also"></a>Ver también



[Buscar carpetas](http://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)

