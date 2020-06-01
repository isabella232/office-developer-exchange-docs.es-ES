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
description: El elemento PreviousWatermark representa la marca de agua del último evento que se comunicó correctamente al cliente para la suscripción.
ms.openlocfilehash: 1b26a645a5ec6dbbd2874b118f968866aadc32af
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461656"
---
# <a name="previouswatermark"></a>PreviousWatermark

El elemento **PreviousWatermark** representa la marca de agua del último evento que se comunicó correctamente al cliente para la suscripción. 
  
```xml
<PreviousWatermark/>
```

 **WatermarkType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Notificación](notification-ex15websvcsotherref.md) <br/> |Contiene información sobre la suscripción y los eventos que se han producido desde la última notificación.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto. El valor de texto representa la marca de agua más reciente. El valor de texto no puede ser una cadena vacía.
  
## <a name="remarks"></a>Comentarios

La propiedad **PreviousWatermark** es útil para el cliente de determinar la última notificación que se ha realizado correctamente. Por ejemplo, si una suscripción tiene tres eventos con las marcas de agua 1, 2 y 3, y la siguiente notificación se envía con un valor de **PreviousWatermark** de 3, el cliente puede comparar este valor con el valor de marca de agua de la última notificación recibida. Esto permite al cliente garantizar la continuidad de los eventos. 
  
Para los clientes de inserción, el **PreviousWatermark** se compara con el último margen de agua conocido local del lado cliente. Si los valores son diferentes, el cliente ha perdido una notificación de evento y debe restablecer una suscripción mediante la marca de agua local más reciente. Por ejemplo, si un cliente de inserción recibe tres eventos para una suscripción con marcas de agua 1, 2 y 3, y la siguiente notificación incluye un valor de **PreviousWatermark** de 5, el cliente ha perdido al menos una notificación y debe crear una nueva suscripción, pasando un 3 como la marca de agua. 
  
En el caso de un cliente de extracción, el valor de **PreviousWatermark** será el mismo que el de la [marca de agua](watermark.md) que incluye el cliente en la llamada GetEvents. 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación subscribe](subscribe-operation.md)
  
[Operación GetEvents](getevents-operation.md)
  
[Operación unsubscribe](unsubscribe-operation.md)

