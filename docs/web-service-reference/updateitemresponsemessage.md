---
title: UpdateItemResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateItemResponseMessage
api_type:
- schema
ms.assetid: dc585b05-5afc-4c74-8763-5a54f9a650ec
description: El elemento UpdateItemResponseMessage contiene el estado y el resultado de una única solicitud de operación UpdateItem.
ms.openlocfilehash: c971657813784e68a01539899e8fabea67847325
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840850"
---
# <a name="updateitemresponsemessage"></a>UpdateItemResponseMessage

El elemento **UpdateItemResponseMessage** contiene el estado y el resultado de una única solicitud de [operación UpdateItem](updateitem-operation.md) . 
  
- [UpdateItemResponse](updateitemresponse.md)
- [ResponseMessages](responsemessages.md)
- [UpdateItemResponseMessage](updateitemresponsemessage.md)
  
```xml
<UpdateItemResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Items/>
   <ConflictResults/>
</UpdateItemResponseMessage>
```

 **ItemInfoResponseMessageType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|**ResponseClass** <br/> | Describe el estado de una respuesta de [la operación UpdateItem](updateitem-operation.md) . <br/><br/>Los siguientes valores son válidos para este atributo:  <br/><br/>-Éxito  <br/>-Advertencia  <br/>-Error  <br/> |
   
#### <a name="responseclass-attribute-values"></a>Valores de atributo de ResponseClass

|**Valor**|**Descripción**|
|:-----|:-----|
|**Operación correcta** <br/> |Describe una solicitud que se cumplen los requisitos.  <br/> |
|**Warning** <br/> | Describe una solicitud que no se procesó. Es posible que se devuelve una advertencia si se produjo un error mientras se procesó un elemento en la solicitud y no se podrían procesar los elementos subsiguientes. <br/><br/>Los siguientes son ejemplos de fuentes de advertencias:  <br/><br/>-El almacén de Exchange está sin conexión durante el proceso por lotes.  <br/>-Los servicios de dominio de Active Directory (AD DS) está sin conexión.  <br/>-Se mueven los buzones de correo.  <br/>-La base de datos de mensajes (MDB) está sin conexión.  <br/>-Una contraseña ha expirado.  <br/>-Se ha excedido una cuota.  <br/> |
|**Error** <br/> | Describe una solicitud que no se cumplen los requisitos. <br/><br/>Los siguientes son ejemplos de orígenes de errores:  <br/><br/>-No válida Atributos o elementos  <br/>-Los atributos o elementos fuera del intervalo  <br/>-Etiqueta desconocida  <br/>-De atributo o elemento no es válido en el contexto  <br/>-Intento de acceso no autorizado por parte de cualquier cliente  <br/>-Error server-side en respuesta a una llamada de cliente válida  <br/><br/>  Puede encontrar información sobre el error en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[MessageText](messagetext.md) <br/> |Proporciona una descripción de texto del estado de la respuesta.  <br/> |
|[ResponseCode](responsecode.md) <br/> |Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |Actualmente no se utiliza y está reservado para uso futuro. Contiene un valor de 0.  <br/> |
|[MessageXml](messagexml.md) <br/> |Proporciona información de la respuesta de error adicionales.  <br/> |
|[Items](items.md) <br/> |Contiene una matriz de elementos actualizados.  <br/> |
|[ConflictResults](conflictresults.md) <br/> |Contiene el número de conflictos en una respuesta de [la operación UpdateItem](updateitem-operation.md) .  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange.  <br/> |
   
## <a name="remarks"></a>Notas

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también

- [Operación UpdateItem](updateitem-operation.md)
- [Actualizar contactos](http://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)
- [Actualización de tareas](http://msdn.microsoft.com/library/0a1bf360-d40c-4a99-929b-4c73a14394d5%28Office.15%29.aspx)

