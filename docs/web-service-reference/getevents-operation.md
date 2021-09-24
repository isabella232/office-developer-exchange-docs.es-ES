---
title: Operación GetEvents
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- GetEvents
api_type:
- schema
ms.assetid: f268efe5-9a1a-41a2-b6a6-51fcde7720a1
description: La operación GetEvents se usa mediante la extracción de clientes de suscripción para solicitar notificaciones desde el servidor de acceso de cliente. La respuesta de la operación GetEvents devuelve una matriz de elementos y eventos que se han producido en un buzón desde la última notificación.
ms.openlocfilehash: 72d99a654921794115d56d28327a39a21c9ea378
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59511603"
---
# <a name="getevents-operation"></a>Operación GetEvents

La **operación GetEvents** se usa mediante la extracción de clientes de suscripción para solicitar notificaciones desde el servidor de acceso de cliente. La **respuesta de la operación GetEvents** devuelve una matriz de elementos y eventos que se han producido en un buzón desde la última notificación. 
  
> [!IMPORTANT]
> La **operación DeleteUserConfiguration** desencadenará un evento move para el sistema de notificación de eventos. El objeto de configuración de usuario se desplazará al contenedor. 
  
## <a name="notes"></a>Notas

Los cambios en los elementos de calendario pueden provocar la generación de varios eventos. Estos eventos son el resultado de los elementos temporales que se crean en el buzón de correo, los elementos de almacenamiento de datos de disponibilidad que se cambian como parte de las operaciones normales del calendario, o ambos. Eventos para la clase de elemento "IPM. Los clientes de servicio web deben omitir SchedulePlus.FreeBusy.BinaryData". Estos elementos temporales se eliminan después de su creación; por lo tanto, si se intenta recuperar estos elementos, se devolverá un error que indica que no se encontró el elemento.
  
## <a name="getevents-request-example"></a>Ejemplo de solicitud GetEvents

### <a name="description"></a>Descripción

En el ejemplo siguiente se muestra cómo solicitar los eventos y elementos asociados con una suscripción que se identifica mediante el identificador de suscripción y la marca de agua.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetEvents xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <SubscriptionId>f6bc657d-dde1-4f94-952d-143b95d6483d</SubscriptionId>
      <Watermark>AAAAAMAGAAAAAAAAAQ==</Watermark>
    </GetEvents>
  </soap:Body>
</soap:Envelope>
```

### <a name="getevents-request-elements"></a>Elementos de solicitud GetEvents

En la solicitud se usan los siguientes elementos:
  
- [GetEvents](getevents.md)
    
- [SubscriptionId (GetEvents)](subscriptionid-getevents.md)
    
- [Watermark](watermark.md)
    
## <a name="successful-getevents-response-example"></a>Ejemplo de respuesta GetEvents correcta

### <a name="description"></a>Descripción

En el ejemplo siguiente de una respuesta se muestra una notificación de la existencia de dos nuevos mensajes de correo desde que se envió la última solicitud de notificación al servidor.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetEventsResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                       xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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
> Los identificadores de elementos y carpetas se han acortado para conservar la legibilidad. 
  
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
    
- [Watermark](watermark.md)
    
- [TimeStamp](timestamp.md)
    
- [ItemId](itemid.md)
    
- [ParentFolderId](parentfolderid.md)
    
Para buscar otras opciones para el mensaje de respuesta de la **operación GetEvents,** explore la jerarquía de esquema. Comience en el [elemento Notification.](notification-ex15websvcsotherref.md) 
  
## <a name="getevents-error-response-example"></a>Ejemplo de respuesta GetEvents Error

### <a name="description"></a>Descripción

En el ejemplo siguiente se muestra una respuesta de error a una **solicitud GetEvents.** 
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
                 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                 xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetEventsResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

## <a name="remarks"></a>Comentarios

Al procesar una **solicitud GetEvents,** el servidor de acceso de cliente realiza los siguientes pasos: 
  
1. El SubscriptionID de la solicitud se confirma como una suscripción válida hospedada en el servidor de acceso de cliente. Si no es así, se produce un error en la llamada **GetEvents.** 
    
2. La dirección SMTP del usuario autenticado para la solicitud se compara con la dirección SMTP del usuario que creó la suscripción. Si no coinciden, se produce un error en la solicitud **GetEvents.** 
    
3. Se consulta a la cola de suscripción para los eventos que están a la espera de ser enviados al cliente. Si la cola no está vacía, los primeros 50 eventos de la cola se extraen de la cola y se codifican en una notificación.
    
4. Si no se encuentra ningún evento en la cola, se genera un StatusEvent y se codifica en una respuesta de notificación.
    
5. La respuesta de notificación se devuelve al cliente.
    
6. Los eventos que se incluyen en la notificación se quitan de la cola de suscripción y la última marca de agua local del servidor de acceso de cliente para la suscripción se establece en la marca de agua del último evento que se devuelve.
    
7. El temporizador de tiempo de espera de la suscripción se restablece.
    
## <a name="see-also"></a>Ver también



[Operación de suscripción](subscribe-operation.md)
  
[Operación Darse de baja](unsubscribe-operation.md)


[Uso de suscripciones de extracción](https://msdn.microsoft.com/library/f956bc0e-2b25-4613-966b-54c65456897c%28Office.15%29.aspx)

