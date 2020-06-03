---
title: CreateItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateItem
api_type:
- schema
ms.assetid: c3707feb-3fd4-4b8a-a68f-2abadd455163
description: El elemento CreateItem define una solicitud para crear un elemento en el almacén de Exchange.
ms.openlocfilehash: 235664b7baeceeccb14135fd346123f0f7d99346
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527064"
---
# <a name="createitem"></a>CreateItem

El elemento **CreateItem** define una solicitud para crear un elemento en el almacén de Exchange. 
  
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

|Atributo|Descripción|
|:-----|:-----|
|**MessageDisposition** <br/> |Describe cómo se controlará el elemento una vez creado. El atributo es necesario para los mensajes de correo electrónico. Este atributo solo es aplicable a los mensajes de correo electrónico.  <br/> |
|**SendMeetingInvitations** <br/> |Describe cómo se controlan las convocatorias de reunión después de su creación. Este atributo es necesario para los elementos de calendario.  <br/> |
   
#### <a name="messagedisposition-attribute"></a>Atributo MessageDisposition

|Valor|Description|
|:-----|:-----|
|SaveOnly  <br/> |El elemento de mensaje se guarda en la carpeta especificada por el elemento [SavedItemFolderId](saveditemfolderid.md) . Los mensajes se pueden enviar más tarde mediante la [operación SendItem](senditem-operation.md). Se devuelve un identificador de elemento en la respuesta. Los identificadores de elemento no se devuelven para ningún tipo de elemento excepto para los elementos de mensaje. Esto incluye los objetos de respuesta.  <br/> |
|SendOnly  <br/> |El elemento se envía, pero no se guarda ninguna copia en la carpeta elementos enviados. No se devuelve un identificador de elemento en la respuesta.<br/><br/>**Nota**: **CreateItem** no admite el acceso delegado cuando se usa la opción SendOnly porque no se puede especificar una carpeta de destino con esta opción. La solución alternativa es crear el elemento, obtener el identificador del elemento y, a continuación, usar la operación SendItem para enviar el elemento.           |
|SendAndSaveCopy  <br/> |El elemento se envía y se guarda una copia en la carpeta identificada por el elemento [SavedItemFolderId](saveditemfolderid.md) . No se devuelve un identificador de elemento en la respuesta.<br/><br/>**Nota**: las convocatorias de reunión no se guardan en la carpeta identificada por la propiedad [SavedItemFolderId](saveditemfolderid.md) . En el caso de los calendarios, la propiedad **SavedItemFolderId** solo puede especificar la ubicación en la que se guardan los elementos del calendario. No puede controlar dónde se guarda un elemento de convocatoria de reunión. Solo los elementos de calendario asociados se copian y se guardan en la carpeta identificada por la propiedad **SavedItemFolderId** .           |
   
#### <a name="sendmeetinginvitations-attribute"></a>Atributo SendMeetingInvitations

|Valor|Description|
|:-----|:-----|
|SendToNone  <br/> |Si el elemento es una convocatoria de reunión, se guarda como un elemento de calendario pero no se envía.  <br/> |
|SendOnlyToAll  <br/> |La convocatoria de reunión se envía a todos los asistentes, pero no se guarda en la carpeta elementos enviados.  <br/> |
|SendToAllAndSaveCopy  <br/> |La convocatoria de reunión se envía a todos los asistentes y se guarda una copia en la carpeta identificada por el elemento [SavedItemFolderId](saveditemfolderid.md) .  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|Elemento|Descripción|
|:-----|:-----|
|[SavedItemFolderId](saveditemfolderid.md) <br/> |Identifica la carpeta de destino en la que se puede crear un nuevo elemento. Si el atributo **MessageDisposition** se establece en SendOnly, solo se enviará un mensaje creado. El mensaje no se colocará en la carpeta identificada por el elemento [SavedItemFolderId](saveditemfolderid.md) .  <br/> |
|[Elementos (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md) <br/> |Contiene una matriz de elementos que se van a crear en la carpeta identificada por el elemento [SavedItemFolderId](saveditemfolderid.md) .  <br/> |
   
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

- [CreateItemResponse](createitemresponse.md)  
- [Operación CreateItem](createitem-operation.md)
- [Crear mensajes de correo electrónico](https://msdn.microsoft.com/library/05bfb83c-2866-427d-a9fe-14ba3cb02793%28Office.15%29.aspx) 
- [Creación de contactos (servicios Web de Exchange)](https://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)  
- [Creación de tareas](https://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx) 
- [Crear citas](https://msdn.microsoft.com/library/2385391e-c9e7-4d45-b803-c4ff94d5c94e%28Office.15%29.aspx)

