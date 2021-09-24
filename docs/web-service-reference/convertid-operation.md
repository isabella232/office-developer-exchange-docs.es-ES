---
title: Operación ConvertId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ConvertId
api_type:
- schema
ms.assetid: 47d96cf6-9e2f-4fc0-9682-7258d3fbf918
description: Busque información sobre la operación EWS ConvertId.
ms.openlocfilehash: 04f20d8446ab3117adb3f00ea17f93c068eeffb9
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59536634"
---
# <a name="convertid-operation"></a>Operación ConvertId

Busque información sobre la **operación EWS ConvertId.** 
  
La **operación ConvertId** Exchange Web Services (EWS) convierte los identificadores de elementos y carpetas entre formatos aceptados por Exchange Online, Exchange Online como parte de Office 365 y versiones locales de Exchange a partir de Exchange Server 2013. 
  
## <a name="using-the-convertid-operation"></a>Uso de la operación ConvertId
<a name="bk_usingConvertId"> </a>

Puede convertir los siguientes identificadores mediante la **operación ConvertId:** 
  
- El formato de identificador de EWS en la versión de lanzamiento inicial de Exchange 2007. Esto se representa mediante el valor `EwsLegacyId` de enumeración en la [enumeración IdFormat.](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx) 
    
- El formato de identificador de EWS en Exchange 2007 SP1 o Exchange 2010. Esto se representa mediante el valor  `EwsId` de enumeración [en IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx).
    
- El identificador MAPI, como en la **PR_ENTRYID** propiedad. Esto se representa mediante el valor `EntryId` de enumeración en la [enumeración IdFormat.](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx) 
    
- Identificador de evento del calendario de disponibilidad. Se trata de una representación con codificación hexadecimal de la **PR_ENTRYID** propiedad. Esto se representa mediante el valor  `HexEntryId` de enumeración [en IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx).
    
- Identificador Exchange almacén. Esto se representa mediante el valor  `StoreId` de enumeración [en IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx). La **operación ConvertId** no convierte los identificadores de carpetas públicas del identificador EWS al identificador de almacén. 
    
- El Outlook Web App de datos. Esto se representa mediante el valor  `OwaId` de enumeración en [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx)
    
    No se admite el paso de direcciones URL que se crean a partir de este identificador Outlook Web App. El Outlook Web App es aplicable a Exchange 2007 y Exchange 2010. Outlook Web App para Exchange Online versiones de Exchange a partir de Exchange Server 2013 usa identificadores EWS.
    
La **operación ConvertId** no funciona como se esperaba al convertir identificadores de carpetas públicas del identificador EWS al identificador de almacén en Exchange Online y Exchange 2013. Puede actualizar manualmente el identificador que se devuelve como solución alternativa. Para actualizar manualmente el identificador: 
  
1. En el código de la aplicación, determine si el elemento o carpeta de destino se encuentra en una carpeta pública. 
    
2. Descodificar la cadena de identificador codificada en Base64.
    
3. Compruebe que el byte de tipo (byte 21) tiene un valor de 7. Un valor de 7 indica que el identificador tiene un formato incorrecto.
    
4. Omita los primeros cuatro bytes. Deben establecerse en cero.
    
5. Actualice los siguientes 16 bytes con el siguiente GUID: 1A447390AAA6611CD9BC800AA002FC45A
    
6. Actualice el byte siguiente (byte de tipo) con un valor de 9.
    
7. Cambie el identificador a una cadena codificada en Base64.
    
> [!NOTE]
> La **operación ConvertId** valida que una dirección SMTP determinada tiene un formato válido. La operación no determina si una dirección SMTP representa un buzón válido. 
  
La **operación ConvertId** puede usar los encabezados SOAP que se enumeran en la tabla siguiente. 
  
**Tabla 1. Encabezados SOAP de operación ConvertId**

|**Header**|**Elemento**|**Descripción**|
|:-----|:-----|:-----|
|Suplantación  <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Identifica el usuario al que la aplicación cliente está suplantando. Esto es aplicable a una solicitud.  <br/> |
|RequestVersion  <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Identifica la versión del esquema de la solicitud de operación Esto es aplicable a una solicitud.  <br/> |
|ServerVersion  <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Identifica la versión del servidor que respondió a la solicitud. Esto es aplicable a una respuesta.  <br/> |
   
## <a name="convertid-operation-request-example"></a>Ejemplo de solicitud de operación ConvertId
<a name="bk_usingConvertId"> </a>

En el siguiente ejemplo de una **solicitud ConvertId** se muestra cómo convertir de un identificador EWS a un Outlook Web App identificador. 
  
El [elemento RequestServerVersion](requestserverversion.md) del encabezado SOAP debe establecerse en Exchange2007_SP1 o posterior para que esta operación funcione. 
  
> [!NOTE]
> El identificador del elemento se ha acortado para conservar la legibilidad. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010"/>
  </soap:Header>
  <soap:Body>
    <ConvertId xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               DestinationFormat="OwaId">
      <SourceIds>
        <t:AlternateId Format="EwsId" Id="AAMkAGZhN2IxYTA0LWNiNzItN="
                       Mailbox="user1@example.com"/>
      </SourceIds>
    </ConvertId>
  </soap:Body>
</soap:Envelope>
```

## <a name="convertid-operation-response-example"></a>Ejemplo de respuesta de operación ConvertId
<a name="bk_usingConvertId"> </a>

En el ejemplo siguiente se muestra una respuesta correcta a una **solicitud ConvertId.** Este ejemplo de respuesta contiene un Outlook Web App identificador. 
  
> [!NOTE]
> El Outlook Web App se ha acortado para conservar la legibilidad. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="1" 
                         MajorBuildNumber="191" MinorBuildNumber="0" 
                         Version="Exchange2010" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ConvertIdResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

## <a name="convertid-operation-error-response-example"></a>Ejemplo de respuesta de error de operación ConvertId
<a name="bk_usingConvertId"> </a>

En el ejemplo siguiente se muestra la respuesta a una solicitud que contiene el tipo incorrecto de formato de identificador.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <ServerVersionInfo MajorVersion="8" MinorVersion="1" 
                       MajorBuildNumber="206" MinorBuildNumber="0"
                       Version="Exchange2010" 
                       xmlns="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ConvertIdResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

El formato del identificador EWS cambió entre la versión de lanzamiento inicial de Exchange 2007 y Exchange 2007 Service Pack 1 (SP1). Exchange Online como parte de las versiones Office 365, Exchange Online y local de Exchange a partir de Exchange 2010 usan el mismo formato de identificador que Exchange 2007 SP1.
  
La **operación ConvertId** convierte los identificadores de carpetas públicas del identificador EWS al identificador de almacén en Exchange 2007 y Exchange 2010. 
  
## <a name="see-also"></a>Ver también
<a name="bk_ConvertIdVersionDiff"> </a>

- [Conversión de identificadores](https://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)
    
- [ConvertIdType](https://msdn.microsoft.com/library/ExchangeWebServices.ConvertIdType.aspx)
    
- [ConvertId](https://msdn.microsoft.com/library/ExchangeWebServices.ExchangeServiceBinding.ConvertId.aspx)
    

