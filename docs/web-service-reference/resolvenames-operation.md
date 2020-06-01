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
description: La operación ResolveNames resuelve direcciones de correo electrónico ambiguas y nombres para mostrar.
ms.openlocfilehash: 51728addddd2bfb9d35b874ae8c11e83a4c8629b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468281"
---
# <a name="resolvenames-operation"></a>Operación ResolveNames

La operación **ResolveNames** resuelve direcciones de correo electrónico ambiguas y nombres para mostrar. 
  
## <a name="using-the-resolvenames-operation"></a>Uso de la operación ResolveNames

Esta operación puede usarse para comprobar los alias y resolver los nombres para mostrar al usuario del buzón de correo apropiado. Si existen nombres ambiguos, la respuesta de operación **ResolveNames** proporciona información acerca de cada usuario de buzón para que la aplicación cliente pueda resolver los nombres. 
  
## <a name="remarks"></a>Comentarios

La respuesta ResolveNames devuelve un máximo de 100 candidatos. Los 100 candidatos que se devuelven son los primeros 100 que se encuentran en la operación de búsqueda.
  
Las direcciones de correo electrónico con tipos de enrutamiento prefijados, como SMTP o SIP, se guardan en una matriz de varios valores. La operación **ResolveNames** realiza una coincidencia parcial con cada valor de la matriz cuando se agrega el tipo de enrutamiento al principio del nombre sin resolver, como "SIP:user1@Contoso.com". Si no especifica un tipo de enrutamiento, **ResolveNames** se establecerá de forma predeterminada en el tipo de enrutamiento de SMTP, lo hará coincidir con una propiedad de dirección SMTP principal y no buscará en la matriz de varios valores. 
  
Solo se puede especificar un nombre ambiguo en una sola solicitud. En primer lugar, se busca en Active Directory y, a continuación, se busca en la carpeta de contactos del usuario. Las entradas resueltas de la carpeta de contactos de un usuario tienen una propiedad **Itemid** que no es null, que se puede usar en una solicitud GetItem. Si es el identificador de una lista de distribución privada, puede usarse en una [operación ExpandDL](expanddl-operation.md). Si el atributo **ReturnFullContactData** se establece en **true**, las entradas de Active Directory que se encuentran con la operación **ResolveNames** devolverán propiedades adicionales que describen un [contacto](contact.md). El atributo **ReturnFullContactData** no afecta a los datos que se devuelven para contactos y listas de distribución privadas de la carpeta de contactos del usuario. 
  
## <a name="resolvenames-request-example"></a>Ejemplo de solicitud ResolveNames

### <a name="description"></a>Descripción

El siguiente ejemplo de una solicitud **ResolveNames** muestra cómo resolver la entrada del usuario.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <ResolveNames xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                  ReturnFullContactData="true">
      <UnresolvedEntry>User2</UnresolvedEntry>
    </ResolveNames>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Comentarios

La respuesta a esta solicitud devolverá todas las entradas que empiecen por "Jo" o "mi". Los elementos devueltos son buzones públicos, listas de distribución públicas y privadas y contactos.
  
> [!NOTE]
> Solo se busca en los contactos de la carpeta de contactos personales predeterminada. 
  
Los siguientes son los posibles resultados de una solicitud de **ResolveNames** : 
  
- Las respuestas que no contienen una entidad resolved devolverán un valor de atributo **ResponseClass** igual a **error**. El elemento **MessageText** contendrá " **no se encuentra ningún resultado**".
    
- Las respuestas que contienen una única entidad resolved devolverán un valor de atributo **ResponseClass** igual a **Success**.
    
- Las respuestas que contienen varias entidades posibles devolverán un valor de atributo **ResponseClass** igual a **ADVERTENCIA**. En este caso, la entidad no se pudo resolver como una identidad única. El elemento **MessageText** contendrá "se encuentran varios resultados". 
    
### <a name="request-elements"></a>Elementos de solicitud

Los siguientes elementos se usan en la solicitud:
  
- [ResolveNames](resolvenames.md)
    
- [UnresolvedEntry](unresolvedentry.md)
    
## <a name="successful-resolvenames-operation-response-example"></a>Ejemplo de respuesta de operación ResolveNames correcta

### <a name="description"></a>Descripción

En el ejemplo siguiente se muestra una respuesta correcta a una solicitud **ResolveNames** . 
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ResolveNamesResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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
    
- [Resolución](resolution.md)
    
- [Buzón](mailbox.md)
    
- [Nombre (EmailAddressType)](name-emailaddresstype.md)
    
- [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md)
    
- [RoutingType (EmailAddressType)](routingtype-emailaddresstype.md)
    
- [MailboxType](mailboxtype.md)
    
- [Contacto](contact.md)
    
- [DisplayName (cadena)](displayname-string.md)
    
- [EmailAddresses](emailaddresses.md)
    
- [Entrada (EmailAddress)](entry-emailaddress.md)
    
- [ContactSource](contactsource.md)
    
## <a name="resolvenames-operation-error-response"></a>Respuesta de error de operación de ResolveNames

### <a name="description"></a>Descripción

En el ejemplo siguiente se muestra una respuesta de error a una solicitud **ResolveNames** . El error se produce al intentar resolver un nombre que no se puede resolver. 
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ResolveNamesResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

Los siguientes elementos se usan en la respuesta de error:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [ResolveNamesResponse](resolvenamesresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [ResolveNamesResponseMessage](resolvenamesresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
## <a name="see-also"></a>Vea también



[Operación ExpandDL](expanddl-operation.md)


[Uso de la resolución de nombres](https://msdn.microsoft.com/library/9257fb07-89d2-46eb-b885-e2173fe6fbc1%28Office.15%29.aspx)

