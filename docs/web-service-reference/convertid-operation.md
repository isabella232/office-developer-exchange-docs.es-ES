---
title: Operación ConvertId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConvertId
api_type:
- schema
ms.assetid: 47d96cf6-9e2f-4fc0-9682-7258d3fbf918
description: Busque información sobre la EWS ConvertId operación.
ms.openlocfilehash: 5f1bcd8a9f0adc25b7c598ef10cc6bb139dfe02d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763884"
---
# <a name="convertid-operation"></a>Operación ConvertId

Obtenga información acerca de la operación de EWS **ConvertId** . 
  
La operación de Exchange Web Services (EWS) **ConvertId** convierte los identificadores de elemento y carpeta entre formatos que se aceptan por Exchange Online, Exchange Online como parte de Office 365, locales y en las versiones de Exchange a partir de Exchange Server 2013. 
  
## <a name="using-the-convertid-operation"></a>Mediante la operación ConvertId
<a name="bk_usingConvertId"> </a>

Puede convertir los siguientes identificadores mediante el uso de la operación de **ConvertId** : 
  
- El formato de identificador para EWS en la versión inicial de Exchange 2007. Esto está representado por el `EwsLegacyId` valor de la enumeración en la enumeración [IdFormat](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx) . 
    
- El formato de identificador para EWS en Exchange 2007 SP1 o Exchange 2010. Esto está representado por el `EwsId` valor de la enumeración en [IdFormat](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx).
    
- El identificador MAPI, como se muestra en la propiedad de **entrada del objeto** . Esto está representado por el `EntryId` valor de la enumeración en la enumeración [IdFormat](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx) . 
    
- El identificador de evento del calendario de disponibilidad. Ésta es una representación codificada en hexadecimal de la propiedad de **entrada del objeto** . Esto está representado por el `HexEntryId` valor de la enumeración en [IdFormat](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx).
    
- El identificador de almacén de Exchange. Esto está representado por el `StoreId` valor de la enumeración en [IdFormat](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx). La operación **ConvertId** no convierte el identificador de almacén de identificadores de carpetas públicas desde el identificador de EWS. 
    
- El identificador de Outlook Web App. Esto está representado por el `OwaId` valor de la enumeración en [IdFormat](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx)
    
    No se admite el paso de las direcciones URL que se crean desde este identificador a Outlook Web App. El identificador de Outlook Web App es aplicable a Exchange 2007 y Exchange 2010. Outlook Web App para Exchange Online y versiones de Exchange a partir de Exchange Server 2013 usa identificadores EWS.
    
La operación **ConvertId** no funciona según lo esperado cuando se convierte los identificadores de carpetas públicas desde el identificador de EWS al identificador del almacén de Exchange Online y Exchange 2013. Puede actualizar manualmente el identificador que se devuelve como una solución alternativa. Para actualizar manualmente el identificador: 
  
1. En el código de la aplicación, determine si el elemento o la carpeta de destino está en una carpeta pública. 
    
2. Descodificar la cadena de identificador con codificación Base64.
    
3. Compruebe que el tipo byte (byte 21) tiene un valor de 7. Un valor de 7 indica que el identificador está en el formato incorrecto.
    
4. Omitir los primeros cuatro bytes. Debe establecer en cero.
    
5. Actualizar los siguientes 16 bytes con el siguiente GUID: 1A447390AA6611CD9BC800AA002FC45A
    
6. Actualizar el siguiente byte (de tipo byte) con un valor de 9.
    
7. Cambie el identificador a una cadena con codificación Base64.
    
> [!NOTE]
> La operación de **ConvertId** valida que una dirección SMTP concreta tiene un formato válido. La operación no determina si una dirección SMTP representa un buzón válido. 
  
La operación de **ConvertId** puede utilizar los encabezados SOAP que se enumeran en la siguiente tabla. 
  
**La tabla 1. Encabezados SOAP de operación de ConvertId**

|**Header**|**Element**|**Descripción**|
|:-----|:-----|:-----|
|Suplantación  <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Identifica el usuario que está realizando la suplantación de la aplicación cliente. Esto es aplicable a una solicitud.  <br/> |
|RequestVersion  <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Identifica la versión del esquema para la solicitud de la operación es aplicable a una solicitud.  <br/> |
|ServerVersion  <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Identifica la versión del servidor que ha respondido a la solicitud. Esto es aplicable a una respuesta.  <br/> |
   
## <a name="convertid-operation-request-example"></a>Ejemplo de solicitud de operación de ConvertId
<a name="bk_usingConvertId"> </a>

El siguiente ejemplo de una solicitud de **ConvertId** muestra cómo convertir un identificador EWS de a un identificador de Outlook Web App. 
  
El elemento [RequestServerVersion](requestserverversion.md) en el encabezado SOAP debe establecerse en Exchange2007_SP1 o posterior para realizar esta operación para que funcione. 
  
> [!NOTE]
> El identificador del elemento se ha acortado para conservar la legibilidad. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010"/>
  </soap:Header>
  <soap:Body>
    <ConvertId xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               DestinationFormat="OwaId">
      <SourceIds>
        <t:AlternateId Format="EwsId" Id="AAMkAGZhN2IxYTA0LWNiNzItN="
                       Mailbox="user1@example.com"/>
      </SourceIds>
    </ConvertId>
  </soap:Body>
</soap:Envelope>
```

## <a name="convertid-operation-response-example"></a>Ejemplo de respuesta la operación ConvertId
<a name="bk_usingConvertId"> </a>

En el ejemplo siguiente se muestra una respuesta a una solicitud **ConvertId** correcta. En este ejemplo de respuesta contiene un identificador de Outlook Web App. 
  
> [!NOTE]
> Se ha reducido el identificador de Outlook Web App para conservar la legibilidad. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="1" 
                         MajorBuildNumber="191" MinorBuildNumber="0" 
                         Version="Exchange2010" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ConvertIdResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseMessages>
        <ConvertIdResponseMessage ResponseClass="Success">
          <ResponseCode>NoError</ResponseCode>
          <AlternateId xsi:type="t:AlternateIdType" Format="OwaId" Id="RgAAAAAS2%2" 
                         Mailbox="user@example.com" />
        </ConvertIdResponseMessage>
      </ResponseMessages>
    </ConvertIdResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="convertid-operation-error-response-example"></a>Ejemplo de respuesta de error de operación de ConvertId
<a name="bk_usingConvertId"> </a>

En el ejemplo siguiente se muestra la respuesta a una solicitud que contiene el tipo de formato de identificador incorrecto.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <ServerVersionInfo MajorVersion="8" MinorVersion="1" 
                       MajorBuildNumber="206" MinorBuildNumber="0"
                       Version="Exchange2010" 
                       xmlns="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ConvertIdResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseMessages>
        <ConvertIdResponseMessage ResponseClass="Error">
          <MessageText>Id is malformed.</MessageText>
          <ResponseCode>ErrorInvalidIdMalformed</ResponseCode>
          <DescriptiveLinkKey>0</DescriptiveLinkKey>
        </ConvertIdResponseMessage>
      </ResponseMessages>
    </ConvertIdResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="version-differences"></a>Diferencias de versión
<a name="bk_ConvertIdVersionDiff"> </a>

El formato de identificador de EWS han cambiado entre la versión de lanzamiento inicial de Exchange 2007 y Exchange 2007 Service Pack 1 (SP1). Exchange Online como parte de Office 365, Exchange Online y versiones locales de Exchange a partir de Exchange 2010 usan el mismo formato de identificador que usa Exchange 2007 SP1.
  
La operación **ConvertId** convierte los identificadores de carpetas públicas desde el identificador de EWS al identificador del almacén de Exchange 2007 y Exchange 2010. 
  
## <a name="see-also"></a>Vea también
<a name="bk_ConvertIdVersionDiff"> </a>

- [Convertir identificadores](http://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)
    
- [ConvertIdType](https://msdn.microsoft.com/library/ExchangeWebServices.ConvertIdType.aspx)
    
- [ConvertId](https://msdn.microsoft.com/library/ExchangeWebServices.ExchangeServiceBinding.ConvertId.aspx)
    

