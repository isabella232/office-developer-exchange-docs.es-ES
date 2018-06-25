---
title: SyncFolderHierarchy
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SyncFolderHierarchy
api_type:
- schema
ms.assetid: 55df4d01-e48e-4263-a851-78a66ad1093a
description: El elemento SyncFolderHierarchy define una solicitud para sincronizar una jerarquía de carpetas en un cliente.
ms.openlocfilehash: f72640e5605dd83e92cd323cb00e4d2f64406245
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840610"
---
# <a name="syncfolderhierarchy"></a>SyncFolderHierarchy

El elemento **SyncFolderHierarchy** define una solicitud para sincronizar una jerarquía de carpetas en un cliente. 
  
```xml
<SyncFolderHierarchy>
   <FolderShape/>   <SyncFolderId/>
   <SyncState/>
</SyncFolderHierarchy>
```

 **SyncFolderHierarchyType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[FolderShape](foldershape.md) <br/> |Identifica las propiedades de carpeta para incluir en una respuesta [SyncFolderHierarchy](syncfolderhierarchy.md) .  <br/> |
|[SyncFolderId](syncfolderid.md) <br/> |Representa la carpeta que contiene los elementos para sincronizar. Este elemento es opcional.  <br/> |
|[Estado de sincronización](syncstate-ex15websvcsotherref.md) <br/> |Contiene un formulario con codificación base64 de los datos de sincronización que se actualizan después de cada solicitud realizada correctamente. Esto se usa para identificar el estado de sincronización.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación SyncFolderHierarchy](syncfolderhierarchy-operation.md)


- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

