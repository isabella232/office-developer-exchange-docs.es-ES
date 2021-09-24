---
title: Operación ResolveNames
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ResolveNames
api_type:
- schema
ms.assetid: 6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb
description: La operación ResolveNames resuelve direcciones de correo electrónico ambiguas y nombres para mostrar.
ms.openlocfilehash: f5ab0e3ee23cc085d8aa425c6eeb0ac7c392b9bb
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59509451"
---
# <a name="resolvenames-operation"></a>Operación ResolveNames

La **operación ResolveNames** resuelve direcciones de correo electrónico ambiguas y nombres para mostrar. 
  
## <a name="using-the-resolvenames-operation"></a>Uso de la operación ResolveNames

Esta operación se puede usar para comprobar alias y resolver nombres para mostrar al usuario de buzón adecuado. Si existen nombres ambiguos, la respuesta de la operación **ResolveNames** proporciona información sobre cada usuario de buzón de correo para que la aplicación cliente pueda resolver los nombres. 
  
## <a name="remarks"></a>Comentarios

La respuesta ResolveNames devuelve un máximo de 100 candidatos. Los 100 candidatos que se devuelven son los primeros 100 que se encuentran en la operación de búsqueda.
  
Las direcciones de correo electrónico con tipos de enrutamiento con prefijo, como smtp o sip, se guardan en una matriz de varios valores. La **operación ResolveNames** realiza una coincidencia parcial con cada valor de esa matriz cuando se agrega el tipo de enrutamiento al principio del nombre no resuelto, como "sip:User1@Contoso.com". Si no especifica un tipo de enrutamiento, **ResolveNames** será el tipo de enrutamiento predeterminado de smtp, lo coincidirá con una propiedad de dirección smtp principal y no buscará en la matriz de varios valores. 
  
Solo se puede especificar un nombre ambiguo en una sola solicitud. Primero se busca en Active Directory y, a continuación, se busca en la carpeta de contactos del usuario. Las entradas resueltas de la carpeta de contactos de un usuario tienen una propiedad **ItemId** que no es nula, que se puede usar en una solicitud GetItem. Si es el identificador de una lista de distribución privada, se puede usar en una [operación ExpandDL](expanddl-operation.md). Si el **atributo ReturnFullContactData** se establece en **true**, las entradas de Active Directory encontradas con la operación **ResolveNames** devolverán propiedades adicionales que describen un [objeto Contact](contact.md). El **atributo ReturnFullContactData** no afecta a los datos que se devuelven para los contactos y las listas de distribución privadas de la carpeta de contactos del usuario. 
  
## <a name="resolvenames-request-example"></a>Ejemplo de solicitud ResolveNames

### <a name="description"></a>Descripción

En el siguiente ejemplo de una **solicitud ResolveNames** se muestra cómo resolver la entrada de User.
  
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

La respuesta a esta solicitud devolverá todas las entradas que comiencen por "Jo" o "Mi". Los elementos devueltos son buzones públicos, listas de distribución públicas y privadas y contactos.
  
> [!NOTE]
> Solo se buscan los contactos de la carpeta contactos personales predeterminada. 
  
A continuación se muestran los posibles resultados de una **solicitud ResolveNames:** 
  
- Las respuestas que no contienen una entidad resuelta devolverán un valor de atributo **ResponseClass** igual a **Error**. El **elemento MessageText** contendrá **"No se encuentran resultados."**
    
- Las respuestas que contienen una única entidad resuelta devolverán un valor de atributo **ResponseClass** igual a **Success**.
    
- Las respuestas que contienen varias entidades posibles devolverán un valor de atributo **ResponseClass** igual a **Warning**. En este caso, la entidad no se pudo resolver con una identidad única. El **elemento MessageText** contendrá "Se encuentran varios resultados". 
    
### <a name="request-elements"></a>Elementos Request

En la solicitud se usan los siguientes elementos:
  
- [ResolveNames](resolvenames.md)
    
- [UnresolvedEntry](unresolvedentry.md)
    
## <a name="successful-resolvenames-operation-response-example"></a>Ejemplo de respuesta de operación ResolveNames correcta

### <a name="description"></a>Descripción

En el ejemplo siguiente se muestra una respuesta correcta a una **solicitud ResolveNames.** 
  
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
    
- [Name (EmailAddressType)](name-emailaddresstype.md)
    
- [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md)
    
- [RoutingType (EmailAddressType)](routingtype-emailaddresstype.md)
    
- [MailboxType](mailboxtype.md)
    
- [Contact](contact.md)
    
- [DisplayName (cadena)](displayname-string.md)
    
- [EmailAddresses](emailaddresses.md)
    
- [Entry (EmailAddress)](entry-emailaddress.md)
    
- [ContactSource](contactsource.md)
    
## <a name="resolvenames-operation-error-response"></a>Respuesta de error de operación ResolveNames

### <a name="description"></a>Descripción

En el ejemplo siguiente se muestra una respuesta de error a una **solicitud ResolveNames.** El error se debe a que intenta resolver un nombre que no se puede resolver. 
  
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

En la respuesta de error se usan los siguientes elementos:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [ResolveNamesResponse](resolvenamesresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [ResolveNamesResponseMessage](resolvenamesresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
## <a name="see-also"></a>Ver también



[Operación ExpandDL](expanddl-operation.md)


[Uso de la resolución de nombres](https://msdn.microsoft.com/library/9257fb07-89d2-46eb-b885-e2173fe6fbc1%28Office.15%29.aspx)

