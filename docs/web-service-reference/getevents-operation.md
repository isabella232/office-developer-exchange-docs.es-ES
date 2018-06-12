---
title: Operación GetEvents
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetEvents
api_type:
- schema
ms.assetid: f268efe5-9a1a-41a2-b6a6-51fcde7720a1
description: La operación GetEvents se usa en los clientes de suscripción de extracción a las notificaciones de solicitud desde el servidor de acceso de cliente. La respuesta de la operación GetEvents devuelve una matriz de elementos y eventos que se han producido en un buzón de correo desde la última vez la notificación.
ms.openlocfilehash: 1a23a9d570a4554e54becb7927f25dff89888c74
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764821"
---
# <a name="getevents-operation"></a>Operación GetEvents

La operación **GetEvents** se usa en los clientes de suscripción de extracción a las notificaciones de solicitud desde el servidor de acceso de cliente. La respuesta de la operación **GetEvents** devuelve una matriz de elementos y eventos que se han producido en un buzón de correo desde la última vez la notificación. 
  
> [!IMPORTANT]
> La operación de **DeleteUserConfiguration** activará un evento de mover para el sistema de notificación de eventos. El objeto de configuración de usuario se moverán al volcado de archivos. 
  
## <a name="remarks"></a>Notas

En la generación de varios eventos pueden ocasionar que los cambios realizados en los elementos del calendario. Estos eventos son el resultado de elementos temporales que se crean en el buzón de correo, los elementos de almacenamiento de datos de disponibilidad que se está cambiando como parte de las operaciones de calendario normales, o ambos. Eventos de elemento de clase "IPM. SchedulePlus.FreeBusy.BinaryData"se debe omitir los clientes de servicios Web. Estos elementos temporales se eliminan después de que se crean; por lo tanto, si se realiza un intento para recuperar estos elementos, un error se devolverán que indica que no se encontró el elemento.
  
## <a name="getevents-request-example"></a>Ejemplo de solicitud GetEvents

### <a name="description"></a>Descripción

En el ejemplo siguiente se muestra cómo solicitar los eventos y los elementos que están asociados con una suscripción que se identifica con el identificador de suscripción y la marca de agua.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetEvents xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <SubscriptionId>f6bc657d-dde1-4f94-952d-143b95d6483d</SubscriptionId>
      <Watermark>AAAAAMAGAAAAAAAAAQ==</Watermark>
    </GetEvents>
  </soap:Body>
</soap:Envelope>
```

### <a name="getevents-request-elements"></a>Elementos de solicitudes GetEvents

En la solicitud se usan los siguientes elementos:
  
- [GetEvents](getevents.md)
    
- [SubscriptionId (GetEvents)](subscriptionid-getevents.md)
    
- [Marca de agua](watermark.md)
    
## <a name="successful-getevents-response-example"></a>Ejemplo de respuesta correcta de GetEvents

### <a name="description"></a>Descripción

El siguiente ejemplo de una respuesta muestra una notificación de la existencia de dos nuevos mensajes de correo desde que se envió la última solicitud de notificación en el servidor.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetEventsResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                       xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:GetEventsResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Notification>
            <t:SubscriptionId>f6bc657d-dde1-4f94-952d-143b95d6483d</t:SubscriptionId>
            <t:PreviousWatermark>AAAAAMAGAAAAAAAAAQ==</t:PreviousWatermark>
            <t:MoreEvents>false</t:MoreEvents>
            <t:NewMailEvent>
              <t:Watermark>AAAAAM4GAAAAAAAAAQ==</t:Watermark>
              <t:TimeStamp>2006-08-22T00:36:29Z</t:TimeStamp>
              <t:ItemId Id="AQApAHR" ChangeKey="CQAAAA==" />
              <t:ParentFolderId Id="AQApAH" ChangeKey="AQAAAA==" />
            </t:NewMailEvent>
            <t:NewMailEvent>
              <t:Watermark>AAAAAOQGAAAAAAAAAQ==</t:Watermark>
              <t:TimeStamp>2006-08-22T01:00:50Z</t:TimeStamp>
              <t:ItemId Id="AQApAHRw" ChangeKey="CQAAAA==" />
              <t:ParentFolderId Id="AQApAH" ChangeKey="AQAAAA==" />
            </t:NewMailEvent>
          </m:Notification>
        </m:GetEventsResponseMessage>
      </m:ResponseMessages>
    </GetEventsResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Comentarios

> [!NOTE]
> Los identificadores de elemento y carpeta se han abreviado para conservar la legibilidad. 
  
### <a name="getevents-response-elements"></a>Elementos de respuesta GetEvents

En la respuesta se usan los siguientes elementos:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [GetEventsResponse](geteventsresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [GetEventsResponseMessage](geteventsresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Notificación](notification-ex15websvcsotherref.md)
    
- [SubscriptionId (GetEvents)](subscriptionid-getevents.md)
    
- [PreviousWatermark](previouswatermark.md)
    
- [MoreEvents](moreevents.md)
    
- [NewMailEvent](newmailevent.md)
    
- [Marca de agua](watermark.md)
    
- [Marca de tiempo](timestamp.md)
    
- [ItemId](itemid.md)
    
- [Id](parentfolderid.md)
    
Para buscar otras opciones para el mensaje de respuesta de la operación **GetEvents** , explore la jerarquía de esquema. Comenzar en el elemento de [notificación](notification-ex15websvcsotherref.md) . 
  
## <a name="getevents-error-response-example"></a>Ejemplo de respuesta de GetEvents Error

### <a name="description"></a>Descripción

En el ejemplo siguiente se muestra una respuesta de error a una solicitud de **GetEvents** . 
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
                 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                 xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetEventsResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:GetEventsResponseMessage ResponseClass="Error">
          <m:MessageText>Access is denied. Only the subscription owner may access the subscription.</m:MessageText>
          <m:ResponseCode>ErrorSubscriptionAccessDenied</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:GetEventsResponseMessage>
      </m:ResponseMessages>
    </GetEventsResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="remarks"></a>Notas

Cuando se procesa una solicitud **GetEvents** , el servidor de acceso de cliente lleva a cabo los siguientes pasos: 
  
1. El identificador de suscripción de la solicitud es confirmado como una suscripción válida que se hospeda en el servidor de acceso de cliente. Si no es así, se produce un error en la llamada **GetEvents** . 
    
2. La dirección SMTP del usuario autenticado para la solicitud se compara con la dirección SMTP del usuario que creó la suscripción. Si no coinciden, se produce un error en la solicitud de **GetEvents** . 
    
3. La cola de suscripción se consulta para los eventos que se esperan que se envíen al cliente. Si la cola no está vacía, los 50 primeros eventos de la cola se extrae de la cola y codificados en una notificación.
    
4. Si no se encontraron eventos en la cola, un objeto StatusEvent se genera y se codifican en una respuesta de notificación.
    
5. La respuesta de notificación se devuelve al cliente.
    
6. Se quitan los eventos que se incluyen en la notificación de la cola de suscripción y se establece el acceso de cliente local última marca de agua server para la suscripción a la marca de agua del último evento que se devuelve.
    
7. Se restablece el temporizador de tiempo de espera de la suscripción.
    
## <a name="see-also"></a>Ver también



[Operación de suscripción](subscribe-operation.md)
  
[Cancelar la operación de suscripción](unsubscribe-operation.md)


[Uso de las suscripciones de extracción](http://msdn.microsoft.com/library/f956bc0e-2b25-4613-966b-54c65456897c%28Office.15%29.aspx)

