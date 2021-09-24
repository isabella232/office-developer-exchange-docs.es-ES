---
title: SyncFolderItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- SyncFolderItems
api_type:
- schema
ms.assetid: 463ed78c-bf82-4cd8-971a-d18425e9e7be
description: El elemento SyncFolderItems define una solicitud para sincronizar elementos en una carpeta Exchange almacén.
ms.openlocfilehash: a3e5aa83335a6bc29b832021e227e6adad4092bf
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513286"
---
# <a name="syncfolderitems"></a>SyncFolderItems

El **elemento SyncFolderItems** define una solicitud para sincronizar elementos en una carpeta Exchange almacén. 
  
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

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ItemShape](itemshape.md) <br/> |Identifica las propiedades y el contenido del elemento que se incluirán en una respuesta SyncFolderItems. Se requiere este elemento.  <br/> |
|[SyncFolderId](syncfolderid.md) <br/> |Representa la carpeta que contiene los elementos que se deben sincronizar. Se requiere este elemento.  <br/> |
|[SyncState](syncstate-ex15websvcsotherref.md) <br/> |Contiene una forma codificada en base64 de los datos de sincronización que se actualizan después de cada solicitud correcta. Esto se usa para identificar el estado de sincronización. Este elemento es opcional.  <br/> |
|[Ignore](ignore.md) <br/> |Identifica los elementos que se omitirán durante la sincronización. Este elemento es opcional.  <br/> |
|[MaxChangesReturned](maxchangesreturned.md) <br/> |Describe el número máximo de cambios que se pueden devolver en una respuesta de sincronización. Se requiere este elemento.  <br/> |
|[SyncScope](syncscope.md) <br/> |Especifica si solo se devuelven elementos o elementos y la información asociada a la carpeta en una respuesta de sincronización. Este elemento es opcional.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre del esquema  <br/> |esquema de mensajes  <br/> |
|Archivo de validación  <br/> |messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación SyncFolderItems](syncfolderitems-operation.md)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

