---
title: PreviousWatermark
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PreviousWatermark
api_type:
- schema
ms.assetid: 474f4f7c-47da-47d4-8126-230012172fb5
description: El elemento PreviousWatermark representa la marca de agua del último evento que se comunicó correctamente al cliente para la suscripción.
ms.openlocfilehash: c46e18c7a58405fe2149666531cb2af773110816
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543026"
---
# <a name="previouswatermark"></a>PreviousWatermark

El **elemento PreviousWatermark** representa la marca de agua del último evento que se comunicó correctamente al cliente para la suscripción. 
  
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

La **propiedad PreviousWatermark** es útil para el cliente para determinar la última notificación correcta. Por ejemplo, si una suscripción tiene tres eventos con marcas de agua 1, 2 y 3, y la siguiente notificación se envía con un valor **previousWatermark** de 3, el cliente puede comparar este valor con el valor de marca de agua de la última notificación recibida. Esto permite al cliente garantizar la continuidad de los eventos. 
  
Para los clientes de inserción, **previousWatermark** se compara con la última marca de agua conocida local del lado cliente. Si los valores son diferentes, el cliente ha perdido una notificación de evento y debe restablecer una suscripción mediante la marca de agua local más reciente. Por ejemplo, si un cliente de inserción recibe tres eventos para una suscripción con marcas de agua 1, 2 y 3, y la siguiente notificación viene con un valor **PreviousWatermark** de 5, el cliente ha perdido al menos una notificación y debe crear una nueva suscripción, pasando un 3 como marca de agua. 
  
En el caso de un cliente de extracción, el valor de **PreviousWatermark** será el mismo que la [marca](watermark.md) de agua incluida por el cliente en la llamada GetEvents. 
  
El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Consulte también



[Operación de suscripción](subscribe-operation.md)
  
[Operación GetEvents](getevents-operation.md)
  
[Operación Darse de baja](unsubscribe-operation.md)

