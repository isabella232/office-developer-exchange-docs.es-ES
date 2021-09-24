---
title: Operación AddNewImContactToGroup
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 0cb5525f-faa3-48f1-9551-df55ffc26f46
description: Busque información sobre la operación EWS AddNewImContactToGroup.
ms.openlocfilehash: 0060b7a0f169e5d8ce0034625ea0c4b367521301
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520139"
---
# <a name="addnewimcontacttogroup-operation"></a>Operación AddNewImContactToGroup

Busque información sobre la **operación EWS AddNewImContactToGroup.** 
  
La **operación AddNewImContactToGroup** agrega un nuevo contacto a un grupo de mensajería instantánea (MI). 
  
Esta operación se introdujo en Exchange Server 2013.
  
## <a name="using-the-addnewimcontacttogroup-operation"></a>Uso de la operación AddNewImContactToGroup

La **operación AddNewImContactToGroup** toma los tres argumentos siguientes para agregar un nuevo contacto a un grupo de mensajería instantánea: 
  
- **Propiedad ImAddress:** identifica la dirección de mensajería instantánea del contacto. La propiedad es obligatoria. 
    
- **Propiedad DisplayName:** identifica el nombre para mostrar del contacto. 
    
- **Propiedad GroupId:** identifica el grupo al que se ha agregado el contacto. 
    
Esta operación devuelve la persona del contacto que se agregó al grupo.
  
### <a name="addnewimcontacttogroup-operation-soap-headers"></a>Encabezados SOAP de operación AddNewImContactToGroup

La **operación AddNewImContactToGroup** puede usar los encabezados SOAP que se enumeran en la tabla siguiente. 
  
|**Nombre de encabezado**|**Elemento**|**Descripción**|
|:-----|:-----|:-----|
|**Suplantación** <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Identifica el usuario al que la aplicación cliente está suplantando. Este encabezado es aplicable a una solicitud.  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |Identifica la referencia cultural, tal como se define en RFC 3066, "Etiquetas para la identificación de idiomas", que se usará para tener acceso al buzón. Este encabezado es aplicable a una solicitud.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Identifica la versión del esquema para la solicitud de operación. Este encabezado es aplicable a una solicitud.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Identifica la versión del servidor que respondió a la solicitud. Este encabezado es aplicable a una respuesta.  <br/> |
   
## <a name="addnewimcontacttogroup-operation-request-example-add-a-new-im-contact-to-a-group"></a>Ejemplo de solicitud de operación AddNewImContactToGroup: Agregar un nuevo contacto de mensajería instantánea a un grupo

En el siguiente ejemplo de una **solicitud de operación AddNewImContactToGroup** se muestra cómo agregar un nuevo contacto a un grupo de mensajería instantánea existente. El valor de la propiedad **GroupId** de este ejemplo se ha devuelto a partir de los resultados de la [operación AddImGroup](addimgroup-operation.md). La **propiedad ExchangeStoreId** contiene el **valor de la propiedad GroupId.** 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
      <t:MailboxCulture>en-US</t:MailboxCulture>
      <t:TimeZoneContext>
         <t:TimeZoneDefinition Id="GMT Standard Time"/>
      </t:TimeZoneContext>
   </soap:Header>
   <soap:Body >
      <m:AddNewImContactToGroup>
         <m:ImAddress>tsmith@contoso.com</m:ImAddress>
         <m:DisplayName>Tony Smith</m:DisplayName>
         <m:GroupId Id="AAMkAGQ1MjJjMTBkLTc4Y2UtNDAAAQKAAA="
                    ChangeKey="EgAAAA=="/>
      </m:AddNewImContactToGroup>
   </soap:Body>
</soap:Envelope>
```

> [!NOTE]
> El **valor GroupId** se ha acortado para conservar la legibilidad. 
  
El cuerpo SOAP de la solicitud contiene los siguientes elementos:
  
- [AddNewImContactToGroup](addnewimcontacttogroup.md)
    
- [ImAddress (Cadena)](imaddress-string.md)
    
- [DisplayName (cadena)](displayname-string.md)
    
- [GroupId](groupid.md)
    
## <a name="successful-addnewimcontacttogroup-operation-response"></a>Respuesta de operación AddNewImContactToGroup correcta

En el ejemplo siguiente se muestra una respuesta correcta a una **solicitud de operación AddNewImContactToGroup.** La respuesta contiene la persona del contacto recién creado. El contacto se agrega a la carpeta Contactos rápidos en Exchange. 
  
> [!NOTE]
> Los identificadores se han acortado para conservar la legibilidad. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" 
                         MinorVersion="0" 
                         MajorBuildNumber="349" 
                         MinorBuildNumber="0" 
                         Version="Exchange2013" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <AddNewImContactToGroupResponse ResponseClass="Success" 
                                    xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <Persona>
        <PersonaId Id="AAQkAGQ1MjJjMTBkLTc4Y2UtNDA5Ny04ZjU5LWI3MTYzNGNkZmRkYQAQAJ3EkhEEXN5KufGbSYJanZk=" 
                   xmlns="https://schemas.microsoft.com/exchange/services/2006/types" />
        <PersonaType xmlns="https://schemas.microsoft.com/exchange/services/2006/types">Person</PersonaType>
        <CreationTime xmlns="https://schemas.microsoft.com/exchange/services/2006/types">2012-01-05T23:06:58Z</CreationTime>
        <DisplayName xmlns="https://schemas.microsoft.com/exchange/services/2006/types">Tony Smith</DisplayName>
        <DisplayNameFirstLast xmlns="https://schemas.microsoft.com/exchange/services/2006/types">Tony Smith</DisplayNameFirstLast>
        <DisplayNameLastFirst xmlns="https://schemas.microsoft.com/exchange/services/2006/types">Tony Smith</DisplayNameLastFirst>
        <FileAsId xmlns="https://schemas.microsoft.com/exchange/services/2006/types">None</FileAsId>
        <EmailAddress xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <Name>Tony Smith</Name>
          <Address>tsmith@contoso.com</Address>
          <RoutingType>SMTP</RoutingType>
        </EmailAddress>
        <EmailAddresses xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <EmailAddress>
            <Name>Tony Smith</Name>
            <Address>tsmith@contoso.com</Address>
            <RoutingType>SMTP</RoutingType>
          </EmailAddress>
        </EmailAddresses>
        <ImAddress xmlns="https://schemas.microsoft.com/exchange/services/2006/types">tsmith@contoso.com</ImAddress>
        <RelevanceScore xmlns="https://schemas.microsoft.com/exchange/services/2006/types">2147483647</RelevanceScore>
        <Attributions xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <Attribution>
            <Id>0</Id>
            <SourceId Id="BtF8oI7iVOQatt/bhQoTbWAAAAAAvcAAA=" 
                      ChangeKey="EQAAABYAAABtF8oIQoTbWAAAAAAyg" />
            <DisplayName>Outlook</DisplayName>
            <IsWritable>true</IsWritable>
            <IsQuickContact>true</IsQuickContact>
            <IsHidden>false</IsHidden>
            <FolderId Id="AAMkAGQ1MjJjMTBkLTc4YhQoTbWAAAAAAvZAAA=" 
                      ChangeKey="AQAAAA==" />
          </Attribution>
        </Attributions>
        <DisplayNames xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <StringAttributedValue>
            <Value>Tony Smith</Value>
            <Attributions>
              <Attribution>0</Attribution>
            </Attributions>
          </StringAttributedValue>
        </DisplayNames>
        <FileAsIds xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <StringAttributedValue>
            <Value>None</Value>
            <Attributions>
              <Attribution>0</Attribution>
            </Attributions>
          </StringAttributedValue>
        </FileAsIds>
        <Emails1 xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <EmailAddressAttributedValue>
            <Value>
              <Name>Tony Smith</Name>
              <Address>tsmith@contoso.com</Address>
              <RoutingType>SMTP</RoutingType>
            </Value>
            <Attributions>
              <Attribution>0</Attribution>
            </Attributions>
          </EmailAddressAttributedValue>
        </Emails1>
        <ImAddresses xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <StringAttributedValue>
            <Value>tsmith@contoso.com</Value>
            <Attributions>
              <Attribution>0</Attribution>
            </Attributions>
          </StringAttributedValue>
        </ImAddresses>
      </Persona>
    </AddNewImContactToGroupResponse>
  </s:Body>
</s:Envelope>
```

El cuerpo SOAP de la respuesta contiene los siguientes elementos:
  
- [AddNewImContactToGroupResponse](addnewimcontacttogroupresponse.md)
    
- [Rol](persona.md)
    
- [PersonaId](personaid.md)
    
- [PersonaType](personatype.md)
    
- [CreationTime](creationtime.md)
    
- [DisplayName (cadena)](displayname-string.md)
    
- [DisplayNameFirstLast](displaynamefirstlast.md)
    
- [DisplayNameLastFirst](displaynamelastfirst.md)
    
- [FileAsId](fileasid.md)
    
- [EmailAddress (EmailAddressType)](emailaddress-emailaddresstype.md)
    
- [Name (EmailAddressType)](name-emailaddresstype.md)
    
- [Address (cadena)](address-string.md)
    
- [RoutingType (EmailAddressType)](routingtype-emailaddresstype.md)
    
- [ImAddress (Cadena)](imaddress-string.md)
    
- [RelevanceScore](relevancescore.md)
    
- [Attributions (ArrayOfPersonaAttributionsType)](attributions-arrayofpersonaattributionstype.md)
    
- [Attribution (PersonaAttributionType)](attribution-personaattributiontype.md)
    
- [ID (Cadena)](id-string.md)
    
- [SourceId](sourceid.md)
    
- [IsWritable](iswritable.md)
    
- [IsQuickContact](isquickcontact.md)
    
- [IsHidden](ishidden.md)
    
- [FolderId](folderid.md)
    
- [DisplayNames](displaynames.md)
    
- [StringAttributedValue](stringattributedvalue.md)
    
- [Value (ArrayOfStringValueType)](value-arrayofstringvaluetype.md)
    
- [FileAsIds](fileasids.md)
    
- [Emails1](emails1.md)
    
- [EmailAddressAttributedValue](emailaddressattributedvalue.md)
    
- [ImAddresses](imaddresses.md)
    
## <a name="addnewimcontacttogroup-operation-error-response"></a>Respuesta de error de operación AddNewImContactToGroup

En el ejemplo siguiente se muestra una respuesta de error a una **solicitud de operación AddNewImContactToGroup.** Esta es una respuesta a una solicitud para agregar un contacto a un grupo que no está en el buzón del solicitante. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="578" 
                           MinorBuildNumber="11" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <AddNewImContactToGroupResponse ResponseClass="Error" 
                                      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>No mailbox with such guid.</MessageText>
         <ResponseCode>ErrorNonExistentMailbox</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
         <MessageXml>
            <t:Value Name="MailboxGuid" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">d5fasdadcw3d-23de-2341-8f59-b71523fsddda</t:Value>
         </MessageXml>
      </AddNewImContactToGroupResponse>
   </s:Body>
</s:Envelope>
```

El cuerpo SOAP de la respuesta de error contiene los siguientes elementos:
  
- [AddNewImContactToGroupResponse](addnewimcontacttogroupresponse.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
- [MessageXml](messagexml.md)
    
Para obtener códigos de error adicionales genéricos para EWS y específicos de esta operación, vea [ResponseCode](responsecode.md).
  
## <a name="see-also"></a>Ver también



[Operación AddImGroup](addimgroup-operation.md)
  
[Operación AddImContactToGroup](addimcontacttogroup-operation.md)
  
[Operación AddImGroup](addimgroup-operation.md)
  
[Operación RemoveImGroup](removeimgroup-operation.md)
  
[Operación SetImGroup](setimgroup-operation.md)


[Personas y contactos de EWS en Exchange](https://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)

