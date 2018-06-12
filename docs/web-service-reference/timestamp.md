---
title: Marca de tiempo
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
description: El elemento de marca de tiempo representa la marca de hora de un evento de buzón de correo.
ms.openlocfilehash: d020d9a4cf3a128d26e0ff2b83be9f3deb024339
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840719"
---
# <a name="timestamp"></a>Marca de tiempo

El elemento de **marca de tiempo** representa la marca de hora de un evento de buzón de correo. 
  
```xml
<TimeStamp/>
```

 **DateTime**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[CopiedEvent](copiedevent.md) <br/> |Representa un evento donde se copia una carpeta o elemento.  <br/> |
|[CreatedEvent](createdevent.md) <br/> |Representa un evento que se crea una carpeta o elemento.  <br/> |
|[DeletedEvent](deletedevent.md) <br/> |Representa un evento que se elimina un elemento o carpeta.  <br/> |
|[ModifiedEvent](modifiedevent.md) <br/> |Representa un evento que se modifica una carpeta o elemento.  <br/> |
|[MovedEvent](movedevent.md) <br/> |Representa un evento donde una carpeta o elemento se mueve desde la carpeta principal de una a otra carpeta primaria.  <br/> |
|[NewMailEvent](newmailevent.md) <br/> |Representa un evento activado por un nuevo elemento de correo en un buzón de correo.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Esta propiedad es de sólo lectura.
  
## <a name="remarks"></a>Notas

Este elemento está principalmente disponible para su uso en la determinación de cliente de la frecuencia de los eventos. Esto no está presente en el [objeto StatusEvent](statusevent.md).
  
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

