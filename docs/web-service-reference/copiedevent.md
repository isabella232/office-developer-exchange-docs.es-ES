---
title: CopiedEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CopiedEvent
api_type:
- schema
ms.assetid: 82f2fcac-deaa-4ff8-801f-4fe28d8a19f5
description: El elemento CopiedEvent representa un evento en el que se copia un elemento o carpeta.
ms.openlocfilehash: 89ca9fb1fd2f4187efdec0e087d840bfee197a29
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763890"
---
# <a name="copiedevent"></a>CopiedEvent

El elemento **CopiedEvent** representa un evento en el que se copia un elemento o carpeta. 
  
```xml
<CopiedEvent>
   <Watermark/>
   <TimeStamp/>
   <FolderId/>
   <ParentFolderId/>
   <OldFolderId/>
   <OldParentFolderId/>
</CopiedEvent>
```

 **MovedCopiedEventType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[Marca de agua](watermark.md) <br/> |Representa un marcador de eventos en la tabla de eventos de buzón de correo.  <br/> |
|[Marca de tiempo](timestamp.md) <br/> |Representa la marca de hora de un evento de buzón de correo del elemento o la carpeta de copia.  <br/> |
|[FolderId](folderid.md) <br/> |Representa el identificador de la carpeta.  <br/> |
|[ItemId](itemid.md) <br/> |Representa el identificador del elemento.  <br/> |
|[Id](parentfolderid.md) <br/> |Representa el identificador de la carpeta que contiene la copia.  <br/> |
|[OldFolderId](oldfolderid.md) <br/> |Representa el identificador de la carpeta de la carpeta original antes de se ha copiado.  <br/> |
|[OldItemId](olditemid.md) <br/> |Contiene el identificador único del elemento original antes de se ha copiado.  <br/> |
|[OldParentFolderId](oldparentfolderid.md) <br/> |Contiene el identificador de la carpeta principal original de un elemento o carpeta que se ha copiado.  <br/> |
   
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



[Operación de suscripción](subscribe-operation.md)
  
[Operación GetEvents](getevents-operation.md)
  
[Cancelar la operación de suscripción](unsubscribe-operation.md)


[Uso de las suscripciones de extracción](http://msdn.microsoft.com/library/f956bc0e-2b25-4613-966b-54c65456897c%28Office.15%29.aspx)
  
[Aplicación de ejemplo de notificación de inserción](http://msdn.microsoft.com/library/db1f8523-fa44-483f-bdb6-ab5939b52eee%28Office.15%29.aspx)

