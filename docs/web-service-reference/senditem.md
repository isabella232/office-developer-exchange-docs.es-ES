---
title: SendItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- SendItem
api_type:
- schema
ms.assetid: a966da19-b05a-4504-ac98-91acc1667b9a
description: El elemento SendItem es el elemento raíz de una solicitud para enviar un elemento en el Exchange almacén.
ms.openlocfilehash: 2d1613451e7f876f0b612a3249570412e40b4764
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521623"
---
# <a name="senditem"></a>SendItem

El **elemento SendItem** es el elemento raíz de una solicitud para enviar un elemento en el Exchange almacén. 
  
```xml
<SendItem SaveItemToFolder="">
   <ItemIds/>
   <SavedItemFolderId/>
</SendItem>
```

 **SendItemType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**SaveItemToFolder** <br/> |Identifica si se guarda una copia del elemento enviado. La acción guardar depende del valor **de SaveItemToFolder** y de si [un elemento SavedItemFolderId](saveditemfolderid.md) está presente en la solicitud. Se requiere este elemento.  <br/> |
   
#### <a name="saveitemtofolder-attribute"></a>Atributo SaveItemToFolder

|**Valor**|**Descripción**|
|:-----|:-----|
|**true** <br/> |Si el [elemento SavedItemFolderId](saveditemfolderid.md) no está presente, el elemento se guarda en la carpeta Elementos enviados. Si el [elemento SavedItemFolderId](saveditemfolderid.md) está presente, el elemento se guarda en la carpeta especificada por el [elemento SavedItemFolderId.](saveditemfolderid.md)  <br/> |
|**false** <br/> |Si el [elemento SavedItemFolderId](saveditemfolderid.md) no está presente, el elemento no se guarda. Si el [elemento SavedItemFolderId](saveditemfolderid.md) está presente, se devolverá una respuesta de error con un elemento [ResponseCode](responsecode.md) que contiene el **valor ErrorInvalidSendItemSaveSettings.**  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ItemIds](itemids.md) <br/> |Contiene las identidades únicas de los elementos, los elementos de repetición y los elementos maestros periódicos que se usan para eliminar, enviar, obtener, mover o copiar elementos en el Exchange almacén.  <br/> |
|[SavedItemFolderId](saveditemfolderid.md) <br/> |Identifica la carpeta de destino para las operaciones que actualizan, envían y crean elementos en el Exchange almacén.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Comentarios

Si se envía un elemento de la carpeta Elementos enviados, se elimina el elemento enviado y se coloca una copia en la carpeta Elementos enviados.
  
El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación SendItem](senditem-operation.md)

