---
title: Operación FindFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FindFolder
api_type:
- schema
ms.assetid: 7a9855aa-06cc-45ba-ad2a-645c15b7d031
description: La operación FindFolder usa Exchange Web Services para buscar subcarpetas de una carpeta identificada y devuelve un conjunto de propiedades que describen el conjunto de subcarpetas.
ms.openlocfilehash: 8c2776a9d60244fe77b6012a09ffbad230d86f63
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59518473"
---
# <a name="findfolder-operation"></a>Operación FindFolder

La **operación FindFolder** usa Exchange Web Services para buscar subcarpetas de una carpeta identificada y devuelve un conjunto de propiedades que describen el conjunto de subcarpetas. 
  
## <a name="remarks"></a>Comentarios

FindFolder devuelve solo los primeros 512 bytes de cualquier propiedad que se puede transmitir. Para Unicode, devuelve los primeros 255 caracteres mediante una cadena Unicode terminada en null.
  
Las consultas de recorrido profundo no se pueden realizar en carpetas públicas.
  
Las restricciones están permitidas y solo deben usarse las propiedades de la carpeta, no las propiedades del elemento. La funcionalidad de ordenación no está disponible para **las respuestas FindFolder.** Las consultas agrupadas no están disponibles para las **consultas FindFolder.** 
  
 **Nota** La **operación FindFolder** también se usa para buscar carpetas administradas. 
  
### <a name="soap-headers"></a>Encabezados SOAP

La **operación FindFolder** puede usar los encabezados SOAP que se enumeran y se describen en la tabla siguiente. 
  
|**Header**|**Elemento**|**Descripción**|
|:-----|:-----|:-----|
|Suplantación  <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Identifica el usuario al que la aplicación cliente está suplantando.  <br/> |
|MailboxCulture  <br/> |[MailboxCulture](mailboxculture.md) <br/> |Identifica la referencia cultural RFC3066 que se usará para tener acceso al buzón.  <br/> |
|RequestVersion  <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Identifica la versión del esquema para la solicitud de operación.  <br/> |
|ServerVersion  <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Identifica la versión del servidor que respondió a la solicitud.  <br/> |
|TimeZoneContext  <br/> |[TimeZoneContext](timezonecontext.md) <br/> |Identifica la zona horaria que se usará para todas las respuestas del servidor.  <br/> |
   
## <a name="findfolder-request-example"></a>Ejemplo de solicitud FindFolder

### <a name="description"></a>Description

En el siguiente ejemplo de una **solicitud FindFolder** se muestra cómo formar una solicitud para buscar todas las carpetas ubicadas en una Bandeja de entrada. 
  
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

Con el valor Predeterminado de [BaseShape](baseshape.md), la respuesta devuelve el nombre de la carpeta, el identificador de carpeta, el número de subcarpetas, el número de carpetas secundarias encontradas en la carpeta y el recuento de elementos no leídos.
  
### <a name="request-elements"></a>Elementos Request

Esta **solicitud FindFolder** incluye los siguientes elementos: 
  
- [FindFolder](findfolder.md)
    
- [FolderShape](foldershape.md)
    
- [BaseShape](baseshape.md)
    
- [ParentFolderIds](parentfolderids.md)
    
- [DistinguishedFolderId](distinguishedfolderid.md)
    
 Para obtener **más elementos de solicitud FindFolder,** consulte el esquema. 
  
## <a name="findfolder-response-example"></a>Ejemplo de respuesta FindFolder

### <a name="description"></a>Description

El siguiente ejemplo de cuerpo del Protocolo simple de acceso a objetos (SOAP) muestra una respuesta correcta a la **solicitud FindFolder.** La respuesta contiene los elementos que se devuelven cuando se usa el valor Predeterminado para [la BaseShape.](baseshape.md) 
  
> [!NOTE]
> El identificador de carpeta y la clave de cambio se han acortado para conservar la legibilidad. 
  
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

Las propiedades que se devuelven en la respuesta están determinadas por [BaseShape](baseshape.md) y [AdditionalProperties](additionalproperties.md) si se usan. Una respuesta **FindFolder** correcta incluye los siguientes elementos: 
  
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

 **Las respuestas FindFolder** a una solicitud con la forma de respuesta **AllProperties** no devolverán los elementos [TotalCount](totalcount.md) y [UnreadCount](unreadcount.md) para las búsquedas en carpetas públicas. 
  
## <a name="findfolder-error-response-example"></a>Ejemplo de respuesta de error FindFolder

### <a name="description"></a>Description

En el siguiente ejemplo de cuerpo SOAP se muestra una respuesta de error que se produce cuando se busca una carpeta identificada por un identificador de carpeta malformada.
  
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

- El elemento [DisplayName (cadena) de](displayname-string.md) la carpeta siempre se incluye en la forma predeterminada. 
    
- El [elemento UnreadCount](unreadcount.md) se incluye en las carpetas Tareas y Notas. 
    
- Use el **valor PropertyTag** de 0x672D con un tipo de propiedad **integer** para identificar una carpeta administrada mediante el [elemento ExtendedFieldURI.](extendedfielduri.md) 
    
## <a name="see-also"></a>Ver también



[Buscar carpetas](https://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)

