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
ms.openlocfilehash: bb5cddd5ea4fa1b73c424275a0b0219ce3e189e3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763956"
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

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|**MessageDisposition** <br/> |Describe cómo se controlarán el elemento después de crearla. El atributo es necesario para los mensajes de correo electrónico. Este atributo sólo es aplicable a los mensajes de correo electrónico.  <br/> |
|**SendMeetingInvitations** <br/> |Describe cómo se controlan las convocatorias de reunión después de que se crean. Este atributo es necesario para los elementos del calendario.  <br/> |
   
#### <a name="messagedisposition-attribute"></a>Atributo MessageDisposition

|**Valor**|**Descripción**|
|:-----|:-----|
|SaveOnly  <br/> |El elemento de mensaje se guarda en la carpeta que se especifica mediante el elemento [SavedItemFolderId](saveditemfolderid.md) . Los mensajes se pueden enviar más adelante mediante el uso de la [operación de SendItem](senditem-operation.md). Un identificador de elemento se devuelve en la respuesta. No se devuelven los identificadores de elemento para los tipos de elemento, excepto los elementos de mensaje. Esto incluye los objetos de respuesta.  <br/> |
|SendOnly  <br/> |El elemento se envía pero ninguna copia se guarda en la carpeta Elementos enviados. Un identificador de elemento no se devuelve en la respuesta.  <br/> > [!NOTE]> **CreateItem** no admite el acceso de delegado cuando se utiliza la opción SendOnly porque no se puede especificar una carpeta de destino con esta opción. La solución consiste en crear el elemento, obtener el identificador de elemento y, a continuación, use la operación de SendItem para enviar el elemento.           |
|SendAndSaveCopy  <br/> |El elemento se envía y se guarda una copia en la carpeta que se identifica con el elemento [SavedItemFolderId](saveditemfolderid.md) . Un identificador de elemento no se devuelve en la respuesta.  <br/> > [!NOTE]> Las convocatorias de reunión no se guardan en la carpeta que se identifica con la propiedad [SavedItemFolderId](saveditemfolderid.md) . Para el calendario, sólo la operación de guardar se puede especificar la ubicación para los elementos de calendario mediante la propiedad **SavedItemFolderId** . No se puede controlar donde una convocatoria de reunión elemento se ha guardado. Sólo los elementos de calendario asociadas se copian y guardar los datos en la carpeta que se identifica con la propiedad **SavedItemFolderId** .           |
   
#### <a name="sendmeetinginvitations-attribute"></a>Atributo SendMeetingInvitations

|**Valor**|**Descripción**|
|:-----|:-----|
|SendToNone  <br/> |Si el elemento es una convocatoria de reunión, se guarda como un elemento de calendario, aunque no envía.  <br/> |
|SendOnlyToAll  <br/> |La convocatoria de reunión se envía a todos los asistentes, pero no se guarda en la carpeta Elementos enviados.  <br/> |
|SendToAllAndSaveCopy  <br/> |La convocatoria de reunión se envía a todos los asistentes y se guarda una copia en la carpeta que se identifica con el elemento [SavedItemFolderId](saveditemfolderid.md) .  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[SavedItemFolderId](saveditemfolderid.md) <br/> |Identifica la carpeta de destino donde se puede crear un nuevo elemento. Si se establece el atributo **MessageDisposition** en SendOnly, sólo se enviará un mensaje de creación. No se va a colocar el mensaje en la carpeta que se identifica con el elemento [SavedItemFolderId](saveditemfolderid.md) .  <br/> |
|[Elementos (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md) <br/> |Contiene una matriz de elementos que desea crear en la carpeta que se identifica con el elemento [SavedItemFolderId](saveditemfolderid.md) .  <br/> |
   
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



[CreateItemResponse](createitemresponse.md)
  
[Operación CreateItem](createitem-operation.md)
  
 **CreateItemType**


[Creación de mensajes de correo electrónico](http://msdn.microsoft.com/library/05bfb83c-2866-427d-a9fe-14ba3cb02793%28Office.15%29.aspx)
  
[Creación de contactos (servicios Web de Exchange)](http://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)
  
[Creación de tareas](http://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx)
  
[Crear citas](http://msdn.microsoft.com/library/2385391e-c9e7-4d45-b803-c4ff94d5c94e%28Office.15%29.aspx)

