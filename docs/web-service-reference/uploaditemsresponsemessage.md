---
title: UploadItemsResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UploadItemsResponseMessage
api_type:
- schema
ms.assetid: 03febd08-c015-4009-b291-1b4296182ffe
description: El elemento UploadItemsResponseMessage contiene el estado y los resultados de una solicitud para cargar un elemento de un solo buzón de correo.
ms.openlocfilehash: 9a1a33011aa1e240ab7e15794e2e89401238ffda
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840886"
---
# <a name="uploaditemsresponsemessage"></a>UploadItemsResponseMessage

El elemento **UploadItemsResponseMessage** contiene el estado y los resultados de una solicitud para cargar un elemento de un solo buzón de correo. 
  
- [UploadItemsResponse](uploaditemsresponse.md) 
- [ResponseMessages](responsemessages.md)
- [UploadItemsResponseMessage](uploaditemsresponsemessage.md)
  
```XML
<UploadItemsResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <ItemId/>
</UploadItemsResponseMessage>
```

 **UploadItemsResponseMessageType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|**ResponseClass** <br/> | Describe el estado de la respuesta. <br/><br/>Los siguientes valores son válidos para este atributo:  <br/><br/>-Éxito  <br/>-Advertencia  <br/>-Error  <br/> |
   
#### <a name="responseclass-attribute-values"></a>Valores de atributo de ResponseClass

|**Valor**|**Descripción**|
|:-----|:-----|
|**Operación correcta** <br/> |Describe una solicitud que se cumplen los requisitos.  <br/> |
|**Warning** <br/> | Describe una solicitud que no se procesó. Es posible que se devuelve una advertencia si se produjo un error mientras procesaba un elemento en la solicitud y no se podrían procesar los elementos subsiguientes. <br/><br/>Los siguientes son ejemplos de fuentes de advertencias:  <br/><br/>-El almacén de Exchange está sin conexión durante el proceso por lotes.  <br/>-Los servicios de dominio de Active Directory (AD DS) está sin conexión.  <br/>-Buzones se han movido.  <br/>-La base de datos de mensajes (MDB) está sin conexión.  <br/>-Una contraseña ha expirado.  <br/>-Se superó una cuota.  <br/> |
|**Error** <br/> | Describe una solicitud que no se cumplen los requisitos. <br/><br/>Los siguientes son ejemplos de orígenes de errores:  <br/><br/>-No válida Atributos o elementos  <br/>-Los atributos o elementos que están fuera del intervalo  <br/>-Una etiqueta desconocida  <br/>-Un atributo o un elemento que no es válido en el contexto  <br/>-Un intento de acceso no autorizado por cualquier cliente  <br/>-Un error del lado del servidor en respuesta a una llamada de cliente válida  <br/> <br/> Puede encontrar información sobre el error en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[MessageText](messagetext.md) <br/> |Proporciona una descripción de texto del estado de la respuesta.  <br/> |
|[ResponseCode](responsecode.md) <br/> |Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |Actualmente no utilizado y reservado para uso futuro. Este elemento contiene un valor de 0.  <br/> |
|[MessageXml](messagexml.md) <br/> |Proporciona información de la respuesta de error adicionales.  <br/> |
|[ItemId](itemid.md) <br/> |Contiene el identificador del elemento de un elemento que se cargan.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Observaciones

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda Exchange Web Services.This elemento fue introdujo en Exchange Server 2010 Service Pack 1 (SP1).
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensaje  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también

- [Operación ExportItems](exportitems-operation.md)
- [Operación UploadItems](uploaditems-operation.md)
- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

