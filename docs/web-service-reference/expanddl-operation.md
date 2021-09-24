---
title: Operación ExpandDL
manager: sethgros
ms.date: 07/27/2018
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ExpandDL
api_type:
- schema
ms.assetid: 1f7837e7-9eff-4e10-9577-c40f7ed6af94
description: La operación ExpandDL expone la pertenencia completa a las listas de distribución.
ms.openlocfilehash: 9878ecff0eeee1ef386c7bb26a092eec47f471de
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513783"
---
# <a name="expanddl-operation"></a>Operación ExpandDL

La operación ExpandDL expone la pertenencia completa a las listas de distribución.
  
## <a name="using-the-expanddl-web-method"></a>Uso del método web ExpandDL

La operación ExpandDL usa el servicio web que se encuentra en Exchange.asmx. Este método de servicio web acepta un elemento [Mailbox](mailbox.md) que puede contener un elemento secundario [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) para una expansión de una lista de distribución pública o un elemento secundario [ItemId](itemid.md) para la expansión de una lista de distribución privada. 
  
Las listas de distribución pública se pueden expandir mediante una de las siguientes opciones:
  
1. Alias de lista de distribución
    
2. Dirección del protocolo simple de transferencia de correo (SMTP)
    
3. X400
    
4. X500
    
5. Exchange Dirección heredada
    
6. Nombre de la lista de distribución
    
7. El nombre para mostrar
    
> [!IMPORTANT]
> Los nombres para mostrar no son únicos. Varias cuentas pueden compartir el mismo nombre para mostrar. 
  
## <a name="remarks"></a>Comentarios

No se admite la expansión recursiva. Solo se puede expandir una lista de distribución en una sola llamada. Si más de una lista de distribución coincide con los criterios, el servicio web notifica un error. Una aplicación cliente puede usar una resolución de nombres ambigua (ANR) para buscar listas de distribución ambiguas y, a continuación, elegir la dirección de correo electrónico correcta de la lista de distribución necesaria como parámetro para la operación [ExpandDL](expanddl-operation.md). Para obtener más información, vea [ResolveNames operation](resolvenames-operation.md).
  
Las listas de distribución pública se encuentran en Active Directory. Pueden ser cualquier grupo de distribución dinámico o habilitado para correo. El grupo no debe estar oculto en la lista de direcciones y cada miembro debe tener una dirección de correo electrónico no vacía. Los miembros de la lista de distribución pueden ser usuarios y contactos habilitados para correo, carpetas públicas y listas de distribución habilitadas para correo y grupos dinámicos.
  
Las listas de distribución privadas se encuentran en la carpeta Contactos del buzón de un usuario. Las listas de distribución privadas no tienen direcciones de correo electrónico, por lo que sus identificadores de elementos de almacén se usan en una solicitud ExpandDL. Los miembros de una lista de distribución privada pueden ser cualquier usuario habilitado para correo, contactos o listas de distribución de Active Directory, o contactos o listas de distribución privadas de la carpeta Contactos de un usuario.
  
Para contactos o listas de distribución privadas, los identificadores de elementos se devuelven en la respuesta. Esto se puede usar para obtener información sobre el objeto o para expandir la pertenencia a una lista de distribución privada.
  
## <a name="expanddl-private-distribution-list-request-example"></a>Ejemplo de solicitud de lista de distribución privada ExpandDL

### <a name="description"></a>Descripción

En el siguiente ejemplo de una solicitud ExpandDL se muestra cómo formar una solicitud para expandir una lista de distribución privada.
  
### <a name="code"></a>Código

```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013_SP1" />
  </soap:Header>
  <soap:Body>
    <m:ExpandDL>
      <m:Mailbox>
       <t:EmailAddress>test</t:EmailAddress>
      </m:Mailbox>
    </m:ExpandDL>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Comentarios

Para expandir una lista de distribución privada, el elemento [Mailbox](mailbox.md) contendrá el [elemento ItemId](itemid.md) que identifica una lista de distribución privada en el buzón del usuario. 
  
## <a name="expanddl-public-distribution-list-request-example"></a>Ejemplo de solicitud de lista de distribución pública expandDL

### <a name="description"></a>Descripción

En el siguiente ejemplo de una solicitud ExpandDL se muestra cómo formar una solicitud para expandir una lista de distribución pública. En el ejemplo se muestra el uso de un nombre para mostrar para expandir una lista de distribución.
  
### <a name="code"></a>Código

```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <ExpandDL xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
              xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
        <t:Mailbox>
          <t:EmailAddress>TheDistributionList</t:EmailAddress>
        </t:Mailbox>
    </ExpandDL>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Comentarios

La respuesta a esta solicitud contendrá elementos **Mailbox** que identifican cada buzón de la lista de distribución. Si una lista de distribución está incluida en una lista de distribución, se debe realizar una expansión de lista de distribución independiente en la lista de distribución incrustada. Si la lista de distribución no tiene miembros o la lista de distribución solicitada no existe, el atributo **ResponseClass** contendrá un valor igual a Success. 
  
### <a name="request-elements"></a>Elementos Request

En la solicitud se usan los siguientes elementos:
  
- [ExpandDL](expanddl.md)
    
- [Buzón](mailbox.md)
    
- [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) se usa para identificar listas de distribución públicas. El [elemento ItemId](itemid.md) se usa para identificar listas de distribución privadas. 
    
> [!NOTE]
> El esquema que describe estos elementos se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente. 
  
## <a name="successful-expanddl-response-example"></a>Ejemplo de respuesta expandDL correcta

### <a name="description"></a>Descripción

En el siguiente ejemplo de una respuesta ExpandDL se muestra una respuesta a la solicitud descrita anteriormente. La expansión de la lista de distribución describe lo siguiente: 
  
- Número de miembros de la lista de distribución que se devuelven en la respuesta.
    
- Si la respuesta contiene todos los miembros de la lista de distribución.
    
- Nombre del buzón.
    
- Dirección de correo electrónico del buzón.
    
- Tipo de enrutamiento para el buzón.
    
- El tipo de buzón.
    
> [!NOTE]
> El nombre de la lista de distribución no se incluye en la respuesta; por lo tanto, debe realizar un seguimiento del nombre de la solicitud. 
  
### <a name="code"></a>Código

```xml
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" 
                         MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ExpandDLResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:ExpandDLResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:DLExpansion TotalItemsInView="3" IncludesLastItemInRange="true">
            <t:Mailbox>
              <t:Name>Dan Park</t:Name>
              <t:EmailAddress>dpark@exampledomain.com</t:EmailAddress>
              <t:RoutingType>SMTP</t:RoutingType>
              <t:MailboxType>Mailbox</t:MailboxType>
            </t:Mailbox>
            <t:Mailbox>
              <t:Name>Jeff Price</t:Name>
              <t:EmailAddress>jprice@exampledomain.com</t:EmailAddress>
              <t:RoutingType>SMTP</t:RoutingType>
              <t:MailboxType>Mailbox</t:MailboxType>
            </t:Mailbox>
            <t:Mailbox>
              <t:Name>Tanja Plate</t:Name>
              <t:EmailAddress>tplate@exampledomain.com</t:EmailAddress>
              <t:RoutingType>SMTP</t:RoutingType>
              <t:MailboxType>Mailbox</t:MailboxType>
            </t:Mailbox>
          </m:DLExpansion>
        </m:ExpandDLResponseMessage>
      </m:ResponseMessages>
    </ExpandDLResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-response-elements"></a>Elementos de respuesta correctos

En la respuesta se usan los siguientes elementos:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [ExpandDLResponse](expanddlresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [ExpandDLResponseMessage](expanddlresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [DLExpansion](dlexpansion.md)
    
- [Buzón](mailbox.md)
    
- [Name (EmailAddressType)](name-emailaddresstype.md)
    
- [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md)
    
- [RoutingType (EmailAddressType)](routingtype-emailaddresstype.md)
    
- [MailboxType](mailboxtype.md)
    
Para buscar otras opciones para el mensaje de respuesta de la operación ExpandDL, explore la jerarquía de esquema. Comience en el [elemento ExpandDLResponse.](expanddlresponse.md) 
  
## <a name="expanddl-error-response"></a>Respuesta de error expandDL

### <a name="description"></a>Descripción

En el ejemplo siguiente se muestra una respuesta de error a una solicitud ExpandDL.
  
### <a name="code"></a>Código

```xml
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" 
                         MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ExpandDLResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:ExpandDLResponseMessage ResponseClass="Error">
          <m:MessageText>No results are found.</m:MessageText>
          <m:ResponseCode>ErrorNameResolutionNoResults</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:ExpandDLResponseMessage>
      </m:ResponseMessages>
    </ExpandDLResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a>Elementos de respuesta de error

En la respuesta de error se usan los siguientes elementos:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [ExpandDLResponse](expanddlresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [ExpandDLResponseMessage](expanddlresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
Para buscar otras opciones para el mensaje de respuesta de la operación ExpandDL, explore la jerarquía de esquema. Comience en el [elemento ExpandDLResponse.](expanddlresponse.md) 
  
## <a name="see-also"></a>Ver también

- [Operación ResolveNames](resolvenames-operation.md)
- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

