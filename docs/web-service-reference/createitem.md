---
title: CreateItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- CreateItem
api_type:
- schema
ms.assetid: c3707feb-3fd4-4b8a-a68f-2abadd455163
description: El elemento CreateItem define una solicitud para crear un elemento en el Exchange almacén.
ms.openlocfilehash: 7276b88bd3b90edc68d7ac8fd4a7646324eadb61
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59526501"
---
# <a name="createitem"></a>CreateItem

El **elemento CreateItem** define una solicitud para crear un elemento en el Exchange almacén. 
  
```xml
<CreateItem MessageDisposition="" SendMeetingInvitations="">
   <SavedItemFolderId/>
   <Items/>
</CreateItem>
```

**CreateItemType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|Atributo|Description|
|:-----|:-----|
|**MessageDisposition** <br/> |Describe cómo se controlará el elemento después de crearlo. El atributo es necesario para los mensajes de correo electrónico. Este atributo solo se aplica a los mensajes de correo electrónico.  <br/> |
|**SendMeetingInvitations** <br/> |Describe cómo se administran las solicitudes de reunión después de crearse. Este atributo es necesario para los elementos del calendario.  <br/> |
   
#### <a name="messagedisposition-attribute"></a>Atributo MessageDisposition

|Valor|Description|
|:-----|:-----|
|SaveOnly  <br/> |El elemento de mensaje se guarda en la carpeta especificada por el [elemento SavedItemFolderId.](saveditemfolderid.md) Los mensajes se pueden enviar más adelante mediante la [operación SendItem](senditem-operation.md). Se devuelve un identificador de elemento en la respuesta. Los identificadores de elementos no se devuelven para ningún tipo de elemento excepto para los elementos de mensaje. Esto incluye objetos de respuesta.  <br/> |
|SendOnly  <br/> |El elemento se envía pero no se guarda ninguna copia en la carpeta Elementos enviados. No se devuelve un identificador de elemento en la respuesta.<br/><br/>**NOTA:** **CreateItem** no admite el acceso delegado cuando se usa la opción SendOnly porque no se puede especificar una carpeta de destino con esta opción. La solución alternativa es crear el elemento, obtener el identificador del elemento y, a continuación, usar la operación SendItem para enviar el elemento.           |
|SendAndSaveCopy  <br/> |El elemento se envía y se guarda una copia en la carpeta identificada por el [elemento SavedItemFolderId.](saveditemfolderid.md) No se devuelve un identificador de elemento en la respuesta.<br/><br/>**NOTA:** Las solicitudes de reunión no se guardan en la carpeta identificada por la [propiedad SavedItemFolderId.](saveditemfolderid.md) Para el calendario, solo la propiedad **SavedItemFolderId** puede especificar la ubicación de guardado de los elementos del calendario. No puede controlar dónde se guarda un elemento de solicitud de reunión. Solo los elementos de calendario asociados se copian y se guardan en la carpeta identificada por la **propiedad SavedItemFolderId.**           |
   
#### <a name="sendmeetinginvitations-attribute"></a>Atributo SendMeetingInvitations

|Valor|Description|
|:-----|:-----|
|SendToNone  <br/> |Si el elemento es una solicitud de reunión, se guarda como un elemento de calendario pero no se envía.  <br/> |
|SendOnlyToAll  <br/> |La solicitud de reunión se envía a todos los asistentes, pero no se guarda en la carpeta Elementos enviados.  <br/> |
|SendToAllAndSaveCopy  <br/> |La solicitud de reunión se envía a todos los asistentes y se guarda una copia en la carpeta identificada por el [elemento SavedItemFolderId.](saveditemfolderid.md)  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|Elemento|Descripción|
|:-----|:-----|
|[SavedItemFolderId](saveditemfolderid.md) <br/> |Identifica la carpeta de destino donde se puede crear un nuevo elemento. Si el **atributo MessageDisposition** se establece en SendOnly, solo se enviará un mensaje creado. El mensaje no se colocará en la carpeta identificada por el [elemento SavedItemFolderId.](saveditemfolderid.md)  <br/> |
|[Items (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md) <br/> |Contiene una matriz de elementos para crear en la carpeta identificada por el [elemento SavedItemFolderId.](saveditemfolderid.md)  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también

- [CreateItemResponse](createitemresponse.md)  
- [Operación CreateItem](createitem-operation.md)
- [Creación de mensajes de correo electrónico](https://msdn.microsoft.com/library/05bfb83c-2866-427d-a9fe-14ba3cb02793%28Office.15%29.aspx) 
- [Creación de contactos (Exchange Web Services)](https://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)  
- [Creación de tareas](https://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx) 
- [Creación de citas](https://msdn.microsoft.com/library/2385391e-c9e7-4d45-b803-c4ff94d5c94e%28Office.15%29.aspx)

