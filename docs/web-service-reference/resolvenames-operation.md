---
title: Operación ResolveNames
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ResolveNames
api_type:
- schema
ms.assetid: 6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb
description: La ResolveNames operación las direcciones de correo electrónico ambigua resuelve y nombres para mostrar.
ms.openlocfilehash: 8443cf834dfdf104daeaaa92fdee3742c3fa3719
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837162"
---
# <a name="resolvenames-operation"></a>Operación ResolveNames

La **ResolveNames** operación las direcciones de correo electrónico ambigua resuelve y nombres para mostrar. 
  
## <a name="using-the-resolvenames-operation"></a>Mediante la operación ResolveNames

Esta operación puede usarse para comprobar los alias y resolver nombres para mostrar para el usuario del buzón correspondiente. Si existen nombres ambiguos, la respuesta de la operación **ResolveNames** proporciona información acerca de cada usuario de buzón de correo para que la aplicación cliente pueda resolver los nombres. 
  
## <a name="remarks"></a>Comentarios

La respuesta ResolveNames devuelve un máximo de 100 candidatos. Los candidatos de 100 que se devuelven son los 100 primeros que se encuentran en la operación de búsqueda.
  
Direcciones de correo electrónico con tipos de enrutamiento de prefijo, como smtp o sip, se guardan en una matriz con varios valores. La operación **ResolveNames** lleva a cabo a una coincidencia parcial con respecto a cada valor de dicha matriz al agregar el tipo de distribución al principio del nombre sin resolver, como "sip:User1@Contoso.com". Si no especifica un tipo de distribución, **ResolveNames** de forma predeterminada en el tipo de distribución de smtp, match a una propiedad de dirección smtp principal y no buscar en la matriz con varios valores. 
  
Nombre ambiguo solo se puede especificar en una única solicitud. Active Directory se busca en primer lugar y, a continuación, se busca la carpeta de contactos del usuario. Resuelto las entradas de la carpeta de contactos de un usuario tienen una propiedad de **ItemId** no es null, que, a continuación, se puede usar en una solicitud GetItem. Si es el identificador de una lista de distribución privada, a continuación, se puede utilizar en una [operación de ExpandDL](expanddl-operation.md). Si el atributo **ReturnFullContactData** está establecido en **true**, las entradas de Active Directory que se encuentra con la operación **ResolveNames** devolverá las propiedades adicionales que describen a un [contacto](contact.md). El atributo **ReturnFullContactData** no afecta a los datos que se devuelven para los contactos y private las listas de distribución desde la carpeta de contactos del usuario. 
  
## <a name="resolvenames-request-example"></a>Ejemplo de solicitud ResolveNames

### <a name="description"></a>Descripción

El siguiente ejemplo de una solicitud de **ResolveNames** muestra cómo resolver la entrada del usuario.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <ResolveNames xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
                  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
                  ReturnFullContactData="true">
      <UnresolvedEntry>User2</UnresolvedEntry>
    </ResolveNames>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Comentarios

La respuesta a esta solicitud devolverá todas las entradas que empiecen por "Jo" o "Mi". Los elementos devueltos son públicas buzones, listas de distribución públicas y privadas y contactos.
  
> [!NOTE]
> Se buscan sólo los contactos de la carpeta de contactos personal de forma predeterminada. 
  
Los siguientes son los resultados posibles para una solicitud de **ResolveNames** : 
  
- Las respuestas que no contienen una entidad resuelta devolverá un valor de atributo de **ResponseClass** igual a **Error**. El elemento **MessageText** contendrá " **No se encontraron resultados**".
    
- Las respuestas que contienen una única entidad resuelta devolverá un valor de atributo de **ResponseClass** igual a **correcto**.
    
- Las respuestas que contienen varias entidades posibles devolverá un valor de atributo de **ResponseClass** igual a la **Advertencia**. En este caso, la entidad no se pudo resolver a una identidad única. El elemento **MessageText** contendrá "se encuentran varios resultados". 
    
### <a name="request-elements"></a>Elementos de solicitud

En la solicitud se usan los siguientes elementos:
  
- [ResolveNames](resolvenames.md)
    
- [UnresolvedEntry](unresolvedentry.md)
    
## <a name="successful-resolvenames-operation-response-example"></a>Ejemplo de respuesta correcto de la operación de ResolveNames

### <a name="description"></a>Descripción

En el ejemplo siguiente se muestra una respuesta a una solicitud de **ResolveNames** correcta. 
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ResolveNamesResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:ResolveNamesResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:ResolutionSet TotalItemsInView="1" IncludesLastItemInRange="true">
            <t:Resolution>
              <t:Mailbox>
                <t:Name>User2</t:Name>
                <t:EmailAddress>User2@example.com</t:EmailAddress>
                <t:RoutingType>SMTP</t:RoutingType>
                <t:MailboxType>Mailbox</t:MailboxType>
              </t:Mailbox>
              <t:Contact>
                <t:DisplayName>User2</t:DisplayName>
                <t:EmailAddresses>
                  <t:Entry Key="EmailAddress1">SMTP:User2@example.com</t:Entry>
                </t:EmailAddresses>
                <t:ContactSource>ActiveDirectory</t:ContactSource>
              </t:Contact>
            </t:Resolution>
          </m:ResolutionSet>
        </m:ResolveNamesResponseMessage>
      </m:ResponseMessages>
    </ResolveNamesResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-resolvenames-response-elements"></a>Elementos de respuesta ResolveNames correctos

En la respuesta se usan los siguientes elementos:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [ResolveNamesResponse](resolvenamesresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [ResolveNamesResponseMessage](resolvenamesresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [ResolutionSet](resolutionset.md)
    
- [Resoluci?n](resolution.md)
    
- [Buzón de correo](mailbox.md)
    
- [Nombre (EmailAddressType)](name-emailaddresstype.md)
    
- [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md)
    
- [RoutingType (EmailAddressType)](routingtype-emailaddresstype.md)
    
- [MailboxType](mailboxtype.md)
    
- [Contact](contact.md)
    
- [DisplayName (cadena)](displayname-string.md)
    
- [EmailAddresses](emailaddresses.md)
    
- [Entrada (EmailAddress)](entry-emailaddress.md)
    
- [ContactSource](contactsource.md)
    
## <a name="resolvenames-operation-error-response"></a>Respuesta de error de la operación ResolveNames

### <a name="description"></a>Descripción

En el ejemplo siguiente se muestra una respuesta de error a una solicitud de **ResolveNames** . El error está causado por intenta resolver un nombre que no se puede resolver. 
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ResolveNamesResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:ResolveNamesResponseMessage ResponseClass="Error">
          <m:MessageText>No results were found.</m:MessageText>
          <m:ResponseCode>ErrorNameResolutionNoResults</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:ResolveNamesResponseMessage>
      </m:ResponseMessages>
    </ResolveNamesResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a>Elementos de respuesta de error

En la respuesta de error, se usan los siguientes elementos:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [ResolveNamesResponse](resolvenamesresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [ResolveNamesResponseMessage](resolvenamesresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
## <a name="see-also"></a>Vea también



[Operación de ExpandDL](expanddl-operation.md)


[Uso de la resolución de nombres](http://msdn.microsoft.com/library/9257fb07-89d2-46eb-b885-e2173fe6fbc1%28Office.15%29.aspx)

