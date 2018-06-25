---
title: PreviousWatermark
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PreviousWatermark
api_type:
- schema
ms.assetid: 474f4f7c-47da-47d4-8126-230012172fb5
description: El elemento PreviousWatermark representa la marca de agua del evento más reciente que se ha comunicado correctamente al cliente para la suscripción.
ms.openlocfilehash: 93c6f90d0866ae13618391b8544ab593fe33922b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836886"
---
# <a name="previouswatermark"></a>PreviousWatermark

El elemento **PreviousWatermark** representa la marca de agua del evento más reciente que se ha comunicado correctamente al cliente para la suscripción. 
  
```xml
<PreviousWatermark/>
```

 **WatermarkType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Notificación](notification-ex15websvcsotherref.md) <br/> |Contiene información acerca de la suscripción y los eventos que se han producido desde la última notificación.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto. El valor de texto representa la última marca de agua. El valor de texto no puede ser una cadena vacía.
  
## <a name="remarks"></a>Comentarios

La propiedad **PreviousWatermark** es útil para el cliente en la determinación de la última notificación correcta. Por ejemplo, si una suscripción tiene tres eventos con marcas de agua de 1, 2 y 3, y se envía la notificación siguiente con un valor de **PreviousWatermark** de 3, el cliente puede comparar este valor en el valor de marca de agua de la última notificación recibida. Esto permite que el cliente garantizar la continuidad de eventos. 
  
Para los clientes de inserción, el **PreviousWatermark** se compara con la local, de cliente última conocido marca de agua. Si los valores son diferentes, el cliente no ha realizado una notificación de eventos y debe volver a establecer una suscripción mediante el uso de la marca de agua local más reciente. Por ejemplo, si un cliente de inserción recibe tres eventos para una suscripción con marcas de agua de 1, 2 y 3, y la siguiente notificación viene con un valor de **PreviousWatermark** de 5, el cliente no ha realizado al menos una notificación y debe crear una nueva suscripción, pasando un 3 como la marca de agua. 
  
En el caso de un cliente de extracción, el valor de **PreviousWatermark** será la misma que la [marca de agua](watermark.md) incluidas por el cliente en la llamada GetEvents. 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación de suscripción](subscribe-operation.md)
  
[Operación GetEvents](getevents-operation.md)
  
[Cancelar la operación de suscripción](unsubscribe-operation.md)

