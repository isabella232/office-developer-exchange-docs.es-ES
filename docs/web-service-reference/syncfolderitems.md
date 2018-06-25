---
title: SyncFolderItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SyncFolderItems
api_type:
- schema
ms.assetid: 463ed78c-bf82-4cd8-971a-d18425e9e7be
description: El elemento SyncFolderItems define una solicitud para sincronizar los elementos en una carpeta de almacén de Exchange.
ms.openlocfilehash: 368e19babfccaeab40380103495c63d30647905c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840614"
---
# <a name="syncfolderitems"></a>SyncFolderItems

El elemento **SyncFolderItems** define una solicitud para sincronizar los elementos en una carpeta de almacén de Exchange. 
  
```xml
<SyncFolderItems>
   <ItemShape/>
   <SyncFolderId/>
   <SyncState/>
   <Ignore/>
   <MaxChangesReturned/>   <SyncScope/>
</SyncFolderItems>
```

 **SyncFolderItemsType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[ItemShape](itemshape.md) <br/> |Identifica las propiedades de elemento y el contenido que desea incluir en una respuesta SyncFolderItems. Se requiere este elemento.  <br/> |
|[SyncFolderId](syncfolderid.md) <br/> |Representa la carpeta que contiene los elementos para sincronizar. Se requiere este elemento.  <br/> |
|[Estado de sincronización](syncstate-ex15websvcsotherref.md) <br/> |Contiene un formulario con codificación base64 de los datos de sincronización que se actualizan después de cada solicitud realizada correctamente. Esto se usa para identificar el estado de sincronización. Este elemento es opcional.  <br/> |
|[Ignorar](ignore.md) <br/> |Identifica a los elementos que se debe omitir durante la sincronización. Este elemento es opcional.  <br/> |
|[MaxChangesReturned](maxchangesreturned.md) <br/> |Describe el número máximo de cambios que se pueden devolver en una respuesta de sincronización. Se requiere este elemento.  <br/> |
|[SyncScope](syncscope.md) <br/> |Especifica si se devuelven sólo los elementos o elementos y la carpeta asociada información en una respuesta de sincronización. Este elemento es opcional.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server que tiene instalada la función del servidor acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación SyncFolderItems](syncfolderitems-operation.md)


- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

