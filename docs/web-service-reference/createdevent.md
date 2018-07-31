---
title: CreatedEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreatedEvent
api_type:
- schema
ms.assetid: f0e53a53-c352-42a5-8280-cd808b0e961b
description: El elemento CreatedEvent representa un evento en el que se crea una carpeta o elemento.
ms.openlocfilehash: 791b8af87c0cc8ae7f07850e3a6fedd9975a251e
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353178"
---
# <a name="createdevent"></a>CreatedEvent

El elemento **CreatedEvent** representa un evento en el que se crea una carpeta o elemento. 
  
```xml
<CreatedEvent>
   <Watermark/>
   <TimeStamp/>
   <ItemId/>
   <ParentFolderId/>
</CreatedEvent>
```

```xml
<CreatedEvent>
   <Watermark/>
   <TimeStamp/>
   <FolderId/>
   <ParentFolderId/>
</CreatedEvent>
```

**BaseObjectChangedEventType**

## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[Watermark](watermark.md) <br/> |Representa un marcador de evento en la tabla de eventos de buzón de correo.  <br/> |
|[TimeStamp](timestamp.md) <br/> |Representa la marca de hora de un evento de buzón de carpeta o elemento creado.  <br/> |
|[FolderId](folderid.md) <br/> |Representa el identificador de la carpeta creada.  <br/> |
|[ItemId](itemid.md) <br/> |Representa el identificador del elemento creado.  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |Representa el identificador de la carpeta principal de la carpeta o el elemento creado.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Notificación](notification-ex15websvcsotherref.md) <br/> |Contiene información acerca de la suscripción y los eventos que se han producido desde la última notificación.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación Subscribe](subscribe-operation.md)  
- [Operación GetEvents](getevents-operation.md)  
- [Operación Unsubscribe](unsubscribe-operation.md)
- [Uso de las suscripciones de extracción](http://msdn.microsoft.com/library/f956bc0e-2b25-4613-966b-54c65456897c%28Office.15%29.aspx) 
- [Notificaciones de eventos en EWS](http://msdn.microsoft.com/library/4fd4b351-d35c-4ccc-9ed9-878932ab9d50%28Office.15%29.aspx)

