---
title: Marca
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- TimeStamp
api_type:
- schema
ms.assetid: 5eae859a-5a74-4bf6-b196-d1b2fd38501a
description: El elemento timestamp representa la marca de hora de un evento de buzón.
ms.openlocfilehash: f2280d4eab67b603963c4f0a7468bf35a2b63a88
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459892"
---
# <a name="timestamp"></a>Marca

El elemento **timestamp** representa la marca de hora de un evento de buzón. 
  
```xml
<TimeStamp/>
```

 **DateTime**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[CopiedEvent](copiedevent.md) <br/> |Representa un evento en el que se copia un elemento o una carpeta.  <br/> |
|[CreatedEvent](createdevent.md) <br/> |Representa un evento en el que se crea un elemento o una carpeta.  <br/> |
|[DeletedEvent](deletedevent.md) <br/> |Representa un evento en el que se elimina un elemento o carpeta.  <br/> |
|[ModifiedEvent](modifiedevent.md) <br/> |Representa un evento en el que se modifica un elemento o una carpeta.  <br/> |
|[MovedEvent](movedevent.md) <br/> |Representa un evento en el que se mueve un elemento o una carpeta de una carpeta principal a otra carpeta principal.  <br/> |
|[NewMailEvent](newmailevent.md) <br/> |Representa un evento desencadenado por un nuevo elemento de correo en un buzón.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Esta propiedad es de sólo lectura.
  
## <a name="remarks"></a>Comentarios

Este elemento está disponible principalmente para su uso en el cliente que determina la frecuencia de eventos. Esto no está presente en [StatusEvent](statusevent.md).
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
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

