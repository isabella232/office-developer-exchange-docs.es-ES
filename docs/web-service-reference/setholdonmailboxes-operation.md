---
title: Operación SetHoldOnMailboxes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9015a0d8-3495-461b-aa79-797d23169585
description: Busque información sobre la EWS SetHoldOnMailboxes operación.
ms.openlocfilehash: 1091ed14ceb25dfd275499b9db47ae4e41b5f1a0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837412"
---
# <a name="setholdonmailboxes-operation"></a>Operación SetHoldOnMailboxes

Obtenga información acerca de la operación de EWS **SetHoldOnMailboxes** . 
  
La operación **SetHoldOnMailboxes** establece una directiva de retención de buzón de correo en los buzones de correo. 
  
Esta operación se introdujo en Exchange Server 2013.
  
## <a name="using-the-setholdonmailboxes-operation"></a>Mediante la operación SetHoldOnMailboxes

La operación **SetHoldOnMailboxes** establece una suspensión de buzón de correo en uno o más buzones. 
  
### <a name="setholdonmailboxes-operation-soap-headers"></a>Encabezados SOAP de operación de SetHoldOnMailboxes

La operación de **SetHoldOnMailboxes** puede utilizar los encabezados SOAP que se enumeran en la siguiente tabla. 
  
|**Nombre de encabezado**|**Element**|**Descripción**|
|:-----|:-----|:-----|
|**ManagementRole** <br/> |[ManagementRole](managementrole.md) <br/> |Identifica las funciones de servidor que son necesarias en orden para el autor de la llamada realizar la solicitud. Este encabezado es aplicable a una solicitud.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Identifica la versión del esquema para la solicitud de la operación. Este encabezado es aplicable a una solicitud.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Identifica la versión del servidor que ha respondido a la solicitud. Este encabezado es aplicable a una respuesta.  <br/> |
   
## <a name="setholdonmailboxes-operation-request-example-apply-a-hold-on-a-mailbox"></a>Ejemplo de solicitud de operación de SetHoldOnMailboxes: aplicar una suspensión en un buzón de correo

El siguiente ejemplo de una solicitud de operación **SetHoldOnMailboxes** muestra cómo aplicar una suspensión en dos buzones. La suspensión de buzón de correo se ha creado mediante el comando [New-MailboxSearch](http://technet.microsoft.com/en-us/library/dd298064.aspx) . 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:SetHoldOnMailboxes>
         <m:ActionType>Create</m:ActionType>
         <m:HoldId>HoldId2</m:HoldId>
         <m:Query>test</m:Query>
         <m:Mailboxes>
            <t:String>/o=First/ou=Exchange(DLT)/cn=Recipients/cn=1fa441ff5e4749ba43ecc0fd94c21adf-Willi</t:String>
            <t:String>/o=First/ou=Exchange(DLT)/cn=Recipients/cn=aed2346adaa34ffc9f0f339917e8de95-Micha</t:String>
         </m:Mailboxes>
         <m:Language>English</m:Language>
         <m:IncludeNonIndexableItems>false</m:IncludeNonIndexableItems>
         <m:Deduplication>true</m:Deduplication>
      </m:SetHoldOnMailboxes>
   </soap:Body>
</soap:Envelope>

```

La solicitud SOAP body contiene los siguientes elementos:
  
- [SetHoldOnMailboxes](setholdonmailboxes.md)
    
- [ActionType (HoldActionType)](actiontype-holdactiontype.md)
    
- [HoldId](holdid.md)
    
- [Consulta](query.md)
    
- [Buzones de correo (ArrayOfStringsType)](mailboxes-arrayofstringstype.md)
    
- [String](string.md)
    
- [Idioma](language.md)
    
- [IncludeNonIndexableItems](includenonindexableitems.md)
    
- [Desduplicación](deduplication.md)
    
## <a name="successful-setholdonmailboxes-operation-response"></a>Respuesta es correcta de operación SetHoldOnMailboxes

En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación de **SetHoldOnMailboxes** para poner dos buzones en suspensión. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="526" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <SetHoldOnMailboxesResponse ResponseClass="Success" 
                                  xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <MailboxHoldResult>
            <HoldId xmlns="http://schemas.microsoft.com/exchange/services/2006/types">HoldId2</HoldId>
            <Query xmlns="http://schemas.microsoft.com/exchange/services/2006/types">test</Query>
            <MailboxHoldStatuses xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
               <MailboxHoldStatus>
                  <Mailbox>o=First/ou=Exchange(DLT)/cn=Recipients/cn=1fa441ff5e4749ba43ecc0fd94c21adf-Willi</Mailbox>
                  <Status>Pending</Status>
                  <AdditionalInfo/>
               </MailboxHoldStatus>
               <MailboxHoldStatus>
                  <Mailbox>/o=First/ou=Exchange(DLT)/cn=Recipients/cn=aed2346adaa34ffc9f0f339917e8de95-Micha</Mailbox>
                  <Status>Pending</Status>
                  <AdditionalInfo/>
               </MailboxHoldStatus>
            </MailboxHoldStatuses>
         </MailboxHoldResult>
      </SetHoldOnMailboxesResponse>
   </s:Body>
</s:Envelope>

```

La respuesta SOAP body contiene los siguientes elementos:
  
- [SetHoldOnMailboxesResponse](setholdonmailboxesresponse.md)
    
- [ResponseCode](responsecode.md)
    
- [MailboxHoldResult](mailboxholdresult.md)
    
- [HoldId](holdid.md)
    
- [Consulta](query.md)
    
- [MailboxHoldStatuses](mailboxholdstatuses.md)
    
- [MailboxHoldStatus](mailboxholdstatus.md)
    
- [Buzón de correo (cadena)](mailbox-string.md)
    
- [Estado (HoldStatusType)](status-holdstatustype.md)
    
- [AdditionalInfo](additionalinfo.md)
    
## <a name="setholdonmailboxes-operation-error-response"></a>Respuesta de error de la operación de SetHoldOnMailboxes

En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **SetHoldOnMailboxes** . Esta es una respuesta a una solicitud que contiene un identificador de buzón de correo especificado incorrectamente. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="526" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013"
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <SetHoldOnMailboxesResponse ResponseClass="Error" 
                                  xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>No mailbox is specified for hold operation. If specified in the request, then it could be the object does not exist in AD or is a Distribution Group.</MessageText>
         <ResponseCode>ErrorInvalidOperation</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </SetHoldOnMailboxesResponse>
   </s:Body>
</s:Envelope>

```

La respuesta de error SOAP body contiene los siguientes elementos:
  
- [SetHoldOnMailboxesResponse](setholdonmailboxesresponse.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
Para códigos de error adicionales que son genéricos para EWS y específicos de esta operación, vea [ResponseCode](responsecode.md).
  
## <a name="see-also"></a>Ver también

- [Operaciones de EWS en Exchange](ews-operations-in-exchange.md)
    
- [Operación GetSearchableMailboxes](getsearchablemailboxes-operation.md)
    
- [Operación SearchMailboxes](searchmailboxes-operation.md)
    
- [Operación GetHoldOnMailboxes](getholdonmailboxes-operation.md)
    
- [Operación GetDiscoverySearchConfiguration](getdiscoverysearchconfiguration-operation.md)
    
- [Operación GetNonIndexableItemDetails](getnonindexableitemdetails-operation.md)
    
- [Operación GetNonIndexableItemStatistics](getnonindexableitemstatistics-operation.md)
    

