---
title: Operación GetNonIndexableItemStatistics
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: ed077877-9d98-4434-b8b6-a4a905e7f7a6
description: Busque información sobre la operación EWS GetNonIndexableItemStatistics.
ms.openlocfilehash: e95cd016f73c92a75d9f366527e58045497363d0
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59546241"
---
# <a name="getnonindexableitemstatistics-operation"></a>Operación GetNonIndexableItemStatistics

Busque información sobre la **operación EWS GetNonIndexableItemStatistics.** 
  
La **operación GetNonIndexableItemStatistics** recupera el recuento de elementos que no se pueden indizar en un buzón. 
  
Esta operación se introdujo en Exchange Server 2013.
  
## <a name="using-the-getnonindexableitemstatistics-operation"></a>Uso de la operación GetNonIndexableItemStatistics

La **operación GetNonIndexableItemStatistics** cuenta los elementos de buzón que no se pueden indizar. Los elementos que no se pueden indizar no se buscan durante una búsqueda de detección. 
  
### <a name="getnonindexableitemstatistics-operation-soap-headers"></a>Encabezados SOAP de la operación GetNonIndexableItemStatistics

La **operación GetNonIndexableItemStatistics** puede usar los encabezados SOAP que se enumeran en la tabla siguiente. 
  
|**Nombre de encabezado**|**Elemento**|**Descripción**|
|:-----|:-----|:-----|
|**ManagementRole** <br/> |[ManagementRole](managementrole.md) <br/> |Identifica los roles de servidor necesarios para que el autor de la llamada realice la solicitud. Este encabezado es aplicable a una solicitud.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Identifica la versión del esquema para la solicitud de operación. Este encabezado es aplicable a una solicitud.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Identifica la versión del servidor que respondió a la solicitud. Este encabezado es aplicable a una respuesta.  <br/> |
   
## <a name="getnonindexableitemstatistics-operation-request-example-get-the-count-of-items-that-cannot-be-indexed-in-a-mailbox"></a>Ejemplo de solicitud de operación GetNonIndexableItemStatistics: Obtener el recuento de elementos que no se pueden indizar en un buzón de correo

En el siguiente ejemplo de una solicitud de **operación GetNonIndexableItemStatistics** se muestra cómo solicitar el recuento de elementos que no se pueden indizar en un buzón. 
  
> [!NOTE]
> Todos los nombres de dominio heredados de este ejemplo se han acortado para conservar la legibilidad. 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:GetNonIndexableItemStatistics>
         <m:Mailboxes>
            <t:LegacyDN>/o=First Organization/ou=Exchange Administrative Group (FYDIDLT)/cn=Recipients/cn=3518cf-Steve</t:LegacyDN>
         </m:Mailboxes>
         <m:SearchArchiveOnly>false</m:SearchArchiveOnly>
      </m:GetNonIndexableItemStatistics>
   </soap:Body>
</soap:Envelope>

```

El cuerpo SOAP de la solicitud contiene los siguientes elementos:
  
- [GetNonIndexableItemStatistics](getnonindexableitemstatistics.md)
    
- [Mailboxes (NonEmptyArrayOfLegacyDNsType)](mailboxes-nonemptyarrayoflegacydnstype.md)
    
- [LegacyDN](legacydn.md)
    
- [SearchArchiveOnly](searcharchiveonly.md)
    
## <a name="successful-getnonindexableitemstatistics-operation-response"></a>Respuesta correcta de la operación GetNonIndexableItemStatistics

En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación **GetNonIndexableItemStatistics** para obtener el recuento de elementos que no se pueden indizar en un buzón. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="526" 
                           MinorBuildNumber="0"
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetNonIndexableItemStatisticsResponse ResponseClass="Success" 
                                             xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <NonIndexableItemStatistics>
            <NonIndexableItemStatistic xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <Mailbox>/o=First Organization/ou=Exchange Administrative Group (FYT)/cn=Recipients/cn=35181acf-Steve</Mailbox>
               <ItemCount>2</ItemCount>
            </NonIndexableItemStatistic>
         </NonIndexableItemStatistics>
      </GetNonIndexableItemStatisticsResponse>
   </s:Body>
</s:Envelope>

```

El cuerpo SOAP de la respuesta contiene los siguientes elementos:
  
- [GetNonIndexableItemStatisticsResponse](getnonindexableitemstatisticsresponse.md)
    
- [ResponseCode](responsecode.md)
    
- [NonIndexableItemStatistics](nonindexableitemstatistics.md)
    
- [NonIndexableItemStatistic](nonindexableitemstatistic.md)
    
- [Mailbox (cadena)](mailbox-string.md)
    
- [ItemCount](itemcount.md)
    
## <a name="getnonindexableitemstatistics-operation-error-response"></a>Respuesta de error de operación GetNonIndexableItemStatistics

En el ejemplo siguiente se muestra una respuesta de error a una solicitud de **operación GetNonIndexableItemStatistics.** Esta es una respuesta a una solicitud para obtener el recuento de elementos que no se pueden indizar desde más de un buzón. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="526" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetNonIndexableItemStatisticsResponse ResponseClass="Error" 
                                             xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>Multiple mailboxes is currently not supported, only single mailbox is supported.</MessageText>
         <ResponseCode>ErrorInvalidArgument</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </GetNonIndexableItemStatisticsResponse>
   </s:Body>
</s:Envelope>

```

El cuerpo SOAP de la respuesta de error contiene los siguientes elementos:
  
- [GetNonIndexableItemStatisticsResponse](getnonindexableitemstatisticsresponse.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
Para obtener códigos de error adicionales genéricos para EWS y específicos de esta operación, vea [ResponseCode](responsecode.md).
  
## <a name="see-also"></a>Consulte también

- [Operaciones ews en Exchange](ews-operations-in-exchange.md)
    
- [Operación GetSearchableMailboxes](getsearchablemailboxes-operation.md)
    
- [Operación SearchMailboxes](searchmailboxes-operation.md)
    
- [Operación GetHoldOnMailboxes](getholdonmailboxes-operation.md)
    
- [Operación SetHoldOnMailboxes](setholdonmailboxes-operation.md)
    
- [Operación GetDiscoverySearchConfiguration](getdiscoverysearchconfiguration-operation.md)
    
- [Operación GetNonIndexableItemDetails](getnonindexableitemdetails-operation.md)
    

