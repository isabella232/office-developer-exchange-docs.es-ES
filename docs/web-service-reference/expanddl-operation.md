---
title: Operación de ExpandDL
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ExpandDL
api_type:
- schema
ms.assetid: 1f7837e7-9eff-4e10-9577-c40f7ed6af94
description: La operación de ExpandDL expone la pertenencia completa de las listas de distribución.
ms.openlocfilehash: e4654120881f81a79358e0e7c0ab016f94db3288
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764495"
---
# <a name="expanddl-operation"></a>Operación de ExpandDL

La operación de ExpandDL expone la pertenencia completa de las listas de distribución.
  
## <a name="using-the-expanddl-web-method"></a>Mediante el método Web ExpandDL

La operación de ExpandDL usa el servicio Web que se encuentra en Exchange.asmx. Este método de servicio Web acepta un elemento de [buzón de correo](mailbox.md) que puede contener un elemento secundario de [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) para una expansión de una lista de distribución pública o un elemento secundario de [ItemId](itemid.md) para la expansión de privado lista de distribución. 
  
Listas de distribución públicas pueden ampliarse mediante uno de los procedimientos siguientes:
  
1. Alias de la lista de distribución
    
2. La dirección de Protocolo Simple de transferencia de correo (SMTP)
    
3. X400
    
4. X500
    
5. Dirección de Exchange heredado
    
6. El nombre de la lista de distribución
    
7. El nombre para mostrar
    
> [!IMPORTANT]
> Nombres para mostrar no son únicos. Varias cuentas pueden compartir el mismo nombre para mostrar. 
  
## <a name="remarks"></a>Notas

No se admite la expansión de recursiva. Lista de distribución de un solo se puede expandir en una sola llamada. Si más de una lista de distribución coinciden con los criterios, el servicio Web de informes de un error. Una aplicación cliente puede usar resolución de nombres ambiguos (ANR) para encontrar la distribución ambiguo se enumera y, a continuación, eligió la dirección de correo electrónico correcta de la lista de distribución necesarios como un parámetro para la [operación de ExpandDL](expanddl-operation.md). Para obtener más información, vea [ResolveNames operación](resolvenames-operation.md).
  
Listas de distribución públicas se encuentran en Active Directory. Pueden ser cualquier grupo de distribución dinámico o habilitados para correo. El grupo no debería estar oculto desde la lista de direcciones y cada miembro debe tener una dirección de correo electrónico no está vacía. Los miembros de la lista de distribución pueden ser usuarios habilitados para correo y contactos, carpetas públicas y las listas de distribución habilitados para correo y grupos dinámicos.
  
Listas de distribución privadas se encuentran en la carpeta de contactos del buzón de un usuario. Listas de distribución privadas no tienen direcciones de correo electrónico para que sus identificadores de elemento de almacenamiento se usan en una solicitud de ExpandDL. Los miembros de una lista de distribución privada pueden ser cualquier usuario habilitado para correo, contactos o listas de distribución de Active Directory o listas de contactos o distribución privada de carpeta de contactos de un usuario.
  
Para los contactos o listas de distribución privadas, se devuelven los identificadores de elemento en la respuesta. Esto se puede usar para obtener información sobre el objeto o para expandir la pertenencia en una lista de distribución privada.
  
## <a name="expanddl-private-distribution-list-request-example"></a>Ejemplo de solicitud de la lista de distribución privada de ExpandDL

### <a name="description"></a>Descripción

El siguiente ejemplo de una solicitud de ExpandDL muestra cómo formar una solicitud para expandir una lista de distribución privada.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <ExpandDL xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
              xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
        <t:Mailbox>
          <t:ItemId Id="xASUAd==" ChangeKey="AAts0Q=="/>
        </t:Mailbox>
    </ExpandDL>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Comentarios

Para expandir una lista de distribución privada, el elemento de [buzón de correo](mailbox.md) contendrá el elemento de [ItemId](itemid.md) que identifica una lista de distribución privada en el buzón del usuario. 
  
## <a name="expanddl-public-distribution-list-request-example"></a>Ejemplo de solicitud de la lista de distribución públicas ExpandDL

### <a name="description"></a>Descripción

El siguiente ejemplo de una solicitud de ExpandDL muestra cómo formar una solicitud para expandir una lista de distribución públicas. En el ejemplo se muestra el uso de un nombre para mostrar para expandir una lista de distribución.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <ExpandDL xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
              xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
        <t:Mailbox>
          <t:EmailAddress>TheDistributionList</t:EmailAddress>
        </t:Mailbox>
    </ExpandDL>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Comentarios

La respuesta a esta solicitud contendrá los elementos de **buzón de correo** que identifican cada buzón de correo en la lista de distribución. Si una lista de distribución está dentro de una lista de distribución, debe realizarse una expansión de lista de distribución independiente en la lista de distribución incrustado. Si la lista de distribución no tiene miembros o la lista de distribución solicitado no existe, el atributo **ResponseClass** contendrá un valor igual a correcto. 
  
### <a name="request-elements"></a>Elementos de solicitud

En la solicitud se usan los siguientes elementos:
  
- [ExpandDL](expanddl.md)
    
- [Buzón de correo](mailbox.md)
    
- [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) se usa para identificar las listas de distribución públicas. El elemento [ItemId](itemid.md) se usa para identificar las listas de distribución privadas. 
    
> [!NOTE]
> El esquema que describe estos elementos se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente. 
  
## <a name="successful-expanddl-response-example"></a>Ejemplo de respuesta correcta de ExpandDL

### <a name="description"></a>Descripción

El siguiente ejemplo de una respuesta ExpandDL muestra una respuesta a la solicitud que se ha descrito anteriormente. La expansión de la lista de distribución describe lo siguiente: 
  
- El número de miembros de la lista de distribución que se devuelven en la respuesta.
    
- Si la respuesta contiene a todos los miembros de la lista de distribución.
    
- El nombre del buzón.
    
- La dirección de correo electrónico del buzón.
    
- El tipo de distribución para el buzón de correo.
    
- El tipo de buzón de correo.
    
> [!NOTE]
> El nombre de la lista de distribución no se incluye en la respuesta; por lo tanto, debe realizar un seguimiento del nombre de la solicitud. 
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" 
                         MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ExpandDLResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="successful-response-elements"></a>Elementos de respuesta correcta

En la respuesta se usan los siguientes elementos:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [ExpandDLResponse](expanddlresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [ExpandDLResponseMessage](expanddlresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [DLExpansion](dlexpansion.md)
    
- [Buzón de correo](mailbox.md)
    
- [Nombre (EmailAddressType)](name-emailaddresstype.md)
    
- [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md)
    
- [RoutingType (EmailAddressType)](routingtype-emailaddresstype.md)
    
- [MailboxType](mailboxtype.md)
    
Para buscar otras opciones para el mensaje de respuesta de la operación de ExpandDL, explore la jerarquía de esquema. Comenzar en el elemento de [ExpandDLResponse](expanddlresponse.md) . 
  
## <a name="expanddl-error-response"></a>Respuesta de error de ExpandDL

### <a name="description"></a>Descripción

En el ejemplo siguiente se muestra una respuesta de error a una solicitud de ExpandDL.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" 
                         MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ExpandDLResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

En la respuesta de error, se usan los siguientes elementos:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [ExpandDLResponse](expanddlresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [ExpandDLResponseMessage](expanddlresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
Para buscar otras opciones para el mensaje de respuesta de la operación de ExpandDL, explore la jerarquía de esquema. Comenzar en el elemento de [ExpandDLResponse](expanddlresponse.md) . 
  
## <a name="see-also"></a>Ver también

- [Operación ResolveNames](resolvenames-operation.md)
- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

