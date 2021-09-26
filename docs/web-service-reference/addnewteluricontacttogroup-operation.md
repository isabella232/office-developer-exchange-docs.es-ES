---
title: Operación AddNewTelUriContactToGroup
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: c9688ce8-2465-45bb-8bd2-94b32ed4885c
description: Encuentre información sobre cómo usar la operación EWS AddNewTelUriContactToGroup.
ms.openlocfilehash: 2ad0f55c044e92e2f18a1705ab53be467a804091
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544300"
---
# <a name="addnewteluricontacttogroup-operation"></a>Operación AddNewTelUriContactToGroup

Encuentre información sobre cómo usar la **operación EWS AddNewTelUriContactToGroup.** 
  
La **operación AddNewTelUriContactToGroup** agrega un nuevo contacto a un grupo en función del número de teléfono de un contacto. 
  
Esta operación se introdujo en Exchange Server 2013.
  
## <a name="using-the-addnewteluricontacttogroup-operation"></a>Uso de la operación AddNewTelUriContactToGroup

Una **solicitud de operación AddNewTelUriContactToGroup** envía el URI tel. de un contacto, uri de SIP, número de teléfono y el grupo al que se va a agregar el contacto. Una **respuesta de operación AddNewTelUriContactToGroup** crea una persona para el nuevo contacto. Esta operación permite a los clientes agregar un nuevo contacto incluso si el contacto no tiene un nombre. 
  
### <a name="addnewteluricontacttogroup-operation-soap-headers"></a>Encabezados SOAP de la operación AddNewTelUriContactToGroup

La **operación AddNewTelUriContactToGroup** puede usar los encabezados SOAP que se enumeran en la tabla siguiente. 
  
|**Nombre de encabezado**|**Elemento**|**Descripción**|
|:-----|:-----|:-----|
|**Suplantación** <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Identifica el usuario al que la aplicación cliente está suplantando. Este encabezado es aplicable a una solicitud.  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |Identifica la referencia cultural, tal como se define en RFC 3066, "Etiquetas para la identificación de idiomas", que se usará para tener acceso al buzón. Este encabezado es aplicable a una solicitud.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Identifica la versión del esquema para la solicitud de operación. Este encabezado es aplicable a una solicitud.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Identifica la versión del servidor que respondió a la solicitud. Este encabezado es aplicable a una respuesta.  <br/> |
   
## <a name="addnewteluricontacttogroup-operation-request-example-add-a-new-contact-to-a-group"></a>Ejemplo de solicitud de operación AddNewTelUriContactToGroup: Agregar un nuevo contacto a un grupo

En el siguiente ejemplo de una solicitud de operación **AddNewTelUriContactToGroup** se muestra cómo crear un nuevo contacto y agregar el nuevo contacto a un grupo de mensajería instantánea (MI) mediante los URI de TEL y SIP del contacto. 
  
> [!NOTE]
> Todos los identificadores de elementos y las claves de cambio de este artículo se han acortado para conservar la legibilidad. 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
      <t:MailboxCulture>en-US</t:MailboxCulture>
   </soap:Header>
   <soap:Body >
      <m:AddNewTelUriContactToGroup>
         <m:TelUriAddress>tel:5625550100</m:TelUriAddress>
         <m:ImContactSipUriAddress>sip:john@contoso.com</m:ImContactSipUriAddress>
         <m:ImTelephoneNumber>5625550100</m:ImTelephoneNumber>
         <m:GroupId Id="AAMkADEzOTm4QrAABY7+0GAAA="/>
      </m:AddNewTelUriContactToGroup>
   </soap:Body>
</soap:Envelope>
```

El cuerpo SOAP de la solicitud contiene los siguientes elementos:
  
- [AddNewTelUriContactToGroup](addnewteluricontacttogroup.md)
    
- [TelUriAddress](teluriaddress.md)
    
- [ImContactSipUriAddress](imcontactsipuriaddress.md)
    
- [ImTelephoneNumber](imtelephonenumber.md)
    
- [GroupId](groupid.md)
    
## <a name="successful-addnewteluricontacttogroup-operation-response"></a>Respuesta de operación AddNewTelUriContactToGroup correcta

En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de **operación AddNewTelUriContactToGroup** para crear un contacto. La respuesta contiene el identificador de persona asociado para el contacto, el nombre para mostrar de la persona, que en este caso se basa en el número de teléfono del contacto y el identificador de elemento del contacto, que se muestra como parte de la atribución del identificador de origen. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/"                           
            xmlns:xsd="http://www.w3.org/2001/XMLSchema"
            xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
            xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="545" 
                           MinorBuildNumber="11" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" />
   </s:Header>
   <s:Body>
      <AddNewTelUriContactToGroupResponse ResponseClass="Success" 
                                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <Persona>
            <t:PersonaId Id="AAQkADE686dX3s="/>
            <t:PersonaType>Person</t:PersonaType>
            <t:CreationTime>2012-10-29T23:10:13Z</t:CreationTime>
            <t:DisplayName/>
            <t:DisplayNameFirstLast>5625550100</t:DisplayNameFirstLast>
            <t:DisplayNameLastFirst>5625550100</t:DisplayNameLastFirst>
            <t:FileAs/>
            <t:FileAsId >None</t:FileAsId>
            <t:RelevanceScore >2147483647</t:RelevanceScore>
            <t:Attributions>
               <t:Attribution>
                  <t:Id>0</t:Id>
                  <t:SourceId Id="ABhHuhCAAA=" ChangeKey="EQAAABxFU"/>
                  <t:DisplayName>Lync Contacts</t:DisplayName>
                  <t:IsWritable>false</t:IsWritable>
                  <t:IsQuickContact>true</t:IsQuickContact>
                  <t:IsHidden>false</t:IsHidden>
               </t:Attribution>
            </t:Attributions>
            <t:FileAsIds>
               <t:StringAttributedValue>
                  <t:Value>None</t:Value>
                  <t:Attributions>
                     <t:Attribution>0</t:Attribution>
                  </t:Attributions>
               </t:StringAttributedValue>
            </t:FileAsIds>
            <t:OtherTelephones>
               <t:PhoneNumberAttributedValue>
                  <t:Value>
                     <t:Number>5625550100</t:Number>
                     <t:Type>Other</t:Type>
                  </t:Value>
                  <t:Attributions>
                     <t:Attribution>0</t:Attribution>
                  </t:Attributions>
               </t:PhoneNumberAttributedValue>
            </t:OtherTelephones>
         </Persona>
      </AddNewTelUriContactToGroupResponse>
   </s:Body>
</s:Envelope>
```

El cuerpo SOAP de la respuesta contiene los siguientes elementos:
  
- [AddNewTelUriContactToGroupResponse](addnewteluricontacttogroupresponse.md)
    
- [ResponseCode](responsecode.md)
    
- [Rol](persona.md)
    
- [PersonaId](personaid.md)
    
- [PersonaType](personatype.md)
    
- [CreationTime](creationtime.md)
    
- [DisplayName (cadena)](displayname-string.md)
    
- [DisplayNameFirstLast](displaynamefirstlast.md)
    
- [DisplayNameLastFirst](displaynamelastfirst.md)
    
- [FileAs](fileas.md)
    
- [FileAsId](fileasid.md)
    
- [RelevanceScore](relevancescore.md)
    
- [Attributions (ArrayOfPersonaAttributionsType)](attributions-arrayofpersonaattributionstype.md)
    
- [Attribution (PersonaAttributionType)](attribution-personaattributiontype.md)
    
- [ID (Cadena)](id-string.md)
    
- [SourceId](sourceid.md)
    
- [DisplayName (cadena)](displayname-string.md)
    
- [IsWritable](iswritable.md)
    
- [IsQuickContact](isquickcontact.md)
    
- [IsHidden](ishidden.md)
    
- [FileAsIds](fileasids.md)
    
- [StringAttributedValue](stringattributedvalue.md)
    
- [Valor](value.md)
    
- [Attributions (ArrayOfValueAttributionsType)](attributions-arrayofvalueattributionstype.md)
    
- [Attribution (cadena)](attribution-string.md)
    
- [OtherTelephones](othertelephones.md)
    
- [PhoneNumberAttributedValue](phonenumberattributedvalue.md)
    
- [Valor](value.md)
    
- [Number](number.md)
    
- [Tipo (cadena)](type-string.md)
    
- [Attributions (ArrayOfValueAttributionsType)](attributions-arrayofvalueattributionstype.md)
    
- [Attribution (cadena)](attribution-string.md)
    
## <a name="addnewteluricontacttogroup-operation-error-response-example"></a>Ejemplo de respuesta de error de operación AddNewTelUriContactToGroup

En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **AddNewTelUriContactToGroup** cuando el identificador de grupo contiene un valor bien formado que no identifica un grupo en el buzón. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="545" 
                           MinorBuildNumber="11" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <AddNewTelUriContactToGroupResponse ResponseClass="Error" 
                                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>The specified object was not found in the store.</MessageText>
         <ResponseCode>ErrorItemNotFound</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </AddNewTelUriContactToGroupResponse>
   </s:Body>
</s:Envelope>

```

El cuerpo SOAP de la respuesta de error contiene los siguientes elementos:
  
- [AddNewTelUriContactToGroupResponse](addnewteluricontacttogroupresponse.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
## <a name="see-also"></a>Consulte también

- [Operaciones ews en Exchange](ews-operations-in-exchange.md)
    
- [Personas y contactos de EWS en Exchange](https://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)
    

