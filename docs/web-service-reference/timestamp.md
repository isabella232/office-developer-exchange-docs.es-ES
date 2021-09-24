---
title: TimeStamp
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- TimeStamp
api_type:
- schema
ms.assetid: 5eae859a-5a74-4bf6-b196-d1b2fd38501a
description: El elemento Timestamp representa la marca de tiempo de un evento de buzón.
ms.openlocfilehash: 87264f25cb8902d7306e1c8c42bef600520175be
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59531378"
---
# <a name="timestamp"></a>TimeStamp

El **elemento Timestamp** representa la marca de tiempo de un evento de buzón. 
  
```xml
<TimeStamp/>
```

 **DateTime**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[CopiedEvent](copiedevent.md) <br/> |Representa un evento donde se copia un elemento o carpeta.  <br/> |
|[CreatedEvent](createdevent.md) <br/> |Representa un evento donde se crea un elemento o carpeta.  <br/> |
|[DeletedEvent](deletedevent.md) <br/> |Representa un evento donde se elimina un elemento o una carpeta.  <br/> |
|[ModifiedEvent](modifiedevent.md) <br/> |Representa un evento donde se modifica un elemento o carpeta.  <br/> |
|[MovedEvent](movedevent.md) <br/> |Representa un evento en el que se mueve un elemento o una carpeta de una carpeta primaria a otra carpeta primaria.  <br/> |
|[NewMailEvent](newmailevent.md) <br/> |Representa un evento desencadenado por un nuevo elemento de correo en un buzón.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Esta propiedad es de sólo lectura.
  
## <a name="remarks"></a>Comentarios

Este elemento está disponible principalmente para su uso en la determinación del cliente de la frecuencia de eventos. Esto no está presente en [StatusEvent](statusevent.md).
  
El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre del esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación de suscripción](subscribe-operation.md)
  
[Operación GetEvents](getevents-operation.md)
  
[Operación Darse de baja](unsubscribe-operation.md)

