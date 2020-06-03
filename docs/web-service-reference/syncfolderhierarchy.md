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
ms.openlocfilehash: 68b607dbf603e955f74dfaccadd3ce6c4c9fb6ab
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466650"
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

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FolderShape](foldershape.md) <br/> |Identifica las propiedades de carpeta que se deben incluir en una respuesta [SyncFolderHierarchy](syncfolderhierarchy.md) .  <br/> |
|[SyncFolderId](syncfolderid.md) <br/> |Representa la carpeta que contiene los elementos que se van a sincronizar. Este elemento es opcional.  <br/> |
|[SyncState](syncstate-ex15websvcsotherref.md) <br/> |Contiene una forma codificada en Base64 de los datos de sincronización que se actualizan después de cada solicitud correcta. Se usa para identificar el estado de sincronización.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación SyncFolderHierarchy](syncfolderhierarchy-operation.md)


- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

