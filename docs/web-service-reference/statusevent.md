---
title: Objeto StatusEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- StatusEvent
api_type:
- schema
ms.assetid: d3901818-2640-4bed-aad8-21a61aee62a1
description: El elemento de objeto StatusEvent representa una notificación que no se ha producido ninguna actividad de nuevo en el buzón de correo.
ms.openlocfilehash: e214918f9795e9e29061d4aac72ab144d2b24267
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837592"
---
# <a name="statusevent"></a>Objeto StatusEvent

El elemento de **objeto StatusEvent** representa una notificación que no se ha producido ninguna actividad de nuevo en el buzón de correo. 
  
```xml
<StatusEvent>
   <Watermark/>
</StatusEvent>
```

 **BaseNotificationEventType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[Marca de agua](watermark.md) <br/> |Representa la última marca de agua válido para una suscripción a.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Notificación](notification-ex15websvcsotherref.md) <br/> |Contiene información acerca de la suscripción y los eventos que se han producido desde la última notificación.  <br/> |
   
## <a name="remarks"></a>Notas

El elemento de **objeto StatusEvent** se devuelve en una notificación para uno de los siguientes motivos: 
  
- Un cliente de extracción emite una solicitud GetEvents en una suscripción que no tiene ninguna actividad.
    
- Un cliente de inserción no tiene eventos en la cola cuando se ha alcanzado el [StatusFrequency](statusfrequency.md) . 
    
El **objeto StatusEvent**[marca de agua](watermark.md) se usa en una aplicación cliente de la misma manera que las demás marcas de agua de tipo de evento. Sin embargo, la marca de agua para el **objeto StatusEvent** no es el mismo que las marcas de agua que se usa para otros eventos. Por ejemplo, una suscripción tiene eventos con marcas de agua de 1, 2 y 3 y los eventos se han comunicado correctamente en una notificación. Se produce un período de inactividad y se envía una solicitud de **GetEvents** . El servidor de acceso de cliente (CAS) devuelve un evento de estado e incluye la última marca de agua, 3, como la [PreviousWatermark](previouswatermark.md) y la actual [marca de agua](watermark.md).
  
La marca de agua no seguirá siendo la misma en todos los casos. Entradas de eventos se mantienen durante 30 días. Para mantener una suscripción activa, las entidades Emisoras actualizan periódicamente las marcas de agua para las colas de suscripción. Las marcas de agua actualizados se envían a los clientes para mantener una suscripción activa.
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación de suscripción](subscribe-operation.md)
  
[Operación GetEvents](getevents-operation.md)
  
[Cancelar la operación de suscripción](unsubscribe-operation.md)

