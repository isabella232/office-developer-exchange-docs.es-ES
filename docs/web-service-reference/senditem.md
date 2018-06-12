---
title: SendItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SendItem
api_type:
- schema
ms.assetid: a966da19-b05a-4504-ac98-91acc1667b9a
description: El elemento de SendItem es el elemento raíz en una solicitud para enviar un elemento en el almacén de Exchange.
ms.openlocfilehash: c5ce52ee4643219aa31ae59e8b7d40d7a904c8ab
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837340"
---
# <a name="senditem"></a>SendItem

El elemento de **SendItem** es el elemento raíz en una solicitud para enviar un elemento en el almacén de Exchange. 
  
```xml
<SendItem SaveItemToFolder="">
   <ItemIds/>
   <SavedItemFolderId/>
</SendItem>
```

 **SendItemType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|**SaveItemToFolder** <br/> |Identifica si se guarda una copia del elemento enviado. La operación de guardar acción depende del valor de **SaveItemToFolder** y si está presente en la solicitud de un elemento [SavedItemFolderId](saveditemfolderid.md) . Se requiere este elemento.  <br/> |
   
#### <a name="saveitemtofolder-attribute"></a>Atributo SaveItemToFolder

|**Valor**|**Descripción**|
|:-----|:-----|
|**True** <br/> |Si el elemento [SavedItemFolderId](saveditemfolderid.md) no está presente, el elemento se guarda en la carpeta Elementos enviados. Si el elemento [SavedItemFolderId](saveditemfolderid.md) está presente, el elemento se guarda en la carpeta que se especifica mediante el elemento [SavedItemFolderId](saveditemfolderid.md) .  <br/> |
|**False** <br/> |Si el elemento [SavedItemFolderId](saveditemfolderid.md) no está presente, no se guarda el elemento. Si el elemento [SavedItemFolderId](saveditemfolderid.md) está presente, se devolverá una respuesta de error con un elemento [ResponseCode](responsecode.md) que contiene el valor de **ErrorInvalidSendItemSaveSettings** .  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[ItemId](itemids.md) <br/> |Contiene las identidades únicas de los elementos, elementos de aparición y elementos maestros periódicos que se usan para eliminar, enviar, obtener, mover o copiar elementos en el almacén de Exchange.  <br/> |
|[SavedItemFolderId](saveditemfolderid.md) <br/> |Identifica la carpeta de destino para las operaciones que actualizar, enviar y crear elementos en el almacén de Exchange.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Observaciones

Si se envía un elemento en la carpeta Elementos enviados, se elimina el elemento enviado y se coloca una copia de él en la carpeta Elementos enviados.
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación SendItem](senditem-operation.md)

