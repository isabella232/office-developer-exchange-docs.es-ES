---
title: Operación FindFolder
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
description: La operación FindFolder usa los servicios web Exchange para buscar subcarpetas de una carpeta identificada y devuelve un conjunto de propiedades que describen el conjunto de subcarpetas.
ms.openlocfilehash: f1cc199bdaf684d8d74687ed7f064eb66fee48ff
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462587"
---
# <a name="findfolder-operation"></a>Operación FindFolder

La operación **FindFolder** usa los servicios web Exchange para buscar subcarpetas de una carpeta identificada y devuelve un conjunto de propiedades que describen el conjunto de subcarpetas. 
  
## <a name="remarks"></a>Comentarios

FindFolder devuelve solo los primeros 512 bytes de cualquier propiedad streamable. Para Unicode, devuelve los primeros 255 caracteres mediante una cadena Unicode terminada en NULL.
  
Las consultas de recorrido profundo no se pueden realizar en carpetas públicas.
  
Se permiten restricciones y solo deben usarse las propiedades de la carpeta, no las propiedades del elemento. La funcionalidad de ordenación no está disponible para las respuestas de **FindFolder** . Las consultas agrupadas no están disponibles para las consultas de **FindFolder** . 
  
 **Nota:** La operación **FindFolder** también se usa para buscar carpetas administradas. 
  
### <a name="soap-headers"></a>Encabezados SOAP

La operación **FindFolder** puede usar los encabezados SOAP que se enumeran y describen en la siguiente tabla. 
  
|**Header**|**Elemento**|**Descripción**|
|:-----|:-----|:-----|
|Suplantación  <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Identifica al usuario que está suplantando la aplicación cliente.  <br/> |
|MailboxCulture  <br/> |[MailboxCulture](mailboxculture.md) <br/> |Identifica la referencia cultural RFC3066 que se va a usar para obtener acceso al buzón.  <br/> |
|RequestVersion  <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Identifica la versión del esquema para la solicitud de operación.  <br/> |
|ServerVersion  <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Identifica la versión del servidor que respondió a la solicitud.  <br/> |
|TimeZoneContext  <br/> |[TimeZoneContext](timezonecontext.md) <br/> |Identifica la zona horaria que se va a usar para todas las respuestas del servidor.  <br/> |
   
## <a name="findfolder-request-example"></a>Ejemplo de solicitud FindFolder

### <a name="description"></a>Descripción

El siguiente ejemplo de una solicitud **FindFolder** muestra cómo crear una solicitud para buscar todas las carpetas que se encuentran en una bandeja de entrada. 
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindFolder Traversal="Shallow" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

Con el valor predeterminado de [BaseShape](baseshape.md), la respuesta devuelve el nombre de la carpeta, el identificador de la carpeta, el número de subcarpetas, el número de carpetas secundarias que se encuentran en la carpeta y el número de elementos no leídos.
  
### <a name="request-elements"></a>Elementos de solicitud

Esta solicitud de **FindFolder** incluye los siguientes elementos: 
  
- [FindFolder](findfolder.md)
    
- [FolderShape](foldershape.md)
    
- [BaseShape](baseshape.md)
    
- [ParentFolderIds](parentfolderids.md)
    
- [DistinguishedFolderId](distinguishedfolderid.md)
    
 Para obtener más elementos de solicitud de **FindFolder** , vea el esquema. 
  
## <a name="findfolder-response-example"></a>Ejemplo de respuesta FindFolder

### <a name="description"></a>Descripción

El siguiente ejemplo del cuerpo del Protocolo simple de acceso a objetos (SOAP) muestra una respuesta correcta a la solicitud **FindFolder** . La respuesta contiene los elementos que se devuelven cuando se usa el valor predeterminado para [BaseShape](baseshape.md) . 
  
> [!NOTE]
> El identificador de la carpeta y la clave de cambio se han abreviado para preservar la legibilidad. 
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="652" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <FindFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

Las propiedades que se devuelven en la respuesta las determina [BaseShape](baseshape.md) y [AdditionalProperties](additionalproperties.md) si se usan. Una respuesta **FindFolder** correcta incluye los siguientes elementos: 
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [FindFolderResponse](findfolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [FindFolderResponseMessage](findfolderresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [RootFolder (FindItemResponseMessage)](rootfolder-finditemresponsemessage.md)
    
- [Folders](folders-ex15websvcsotherref.md)
    
- [Folder](folder.md)
    
- [FolderId](folderid.md)
    
- [DisplayName (cadena)](displayname-string.md)
    
- [TotalCount](totalcount.md)
    
- [ChildFolderCount](childfoldercount.md)
    
- [UnreadCount](unreadcount.md)
    
### <a name="comments"></a>Comentarios

 **FindFolder** respuestas a una solicitud con la forma respuesta **AllProperties** no devolverán los elementos [totalCount](totalcount.md) y [UnreadCount](unreadcount.md) para las búsquedas de carpetas públicas. 
  
## <a name="findfolder-error-response-example"></a>Ejemplo de respuesta de error FindFolder

### <a name="description"></a>Descripción

El siguiente ejemplo de cuerpo SOAP muestra una respuesta de error que se produce al buscar una carpeta identificada por un identificador de carpeta con formato incorrecto.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
                 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                 xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="652" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <FindFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

- El elemento de la carpeta [displayName (cadena)](displayname-string.md) siempre se incluye en la forma predeterminada. 
    
- El elemento [UnreadCount](unreadcount.md) se incluye en las carpetas de tareas y notas. 
    
- Use el valor **PropertyTag** de 0x672D con un tipo de propiedad de **entero** para identificar una carpeta administrada mediante el elemento [ExtendedFieldURI](extendedfielduri.md) . 
    
## <a name="see-also"></a>Vea también



[Buscar carpetas](https://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)

