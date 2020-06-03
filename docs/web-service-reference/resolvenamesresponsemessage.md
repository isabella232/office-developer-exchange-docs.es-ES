---
title: ResolveNamesResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ResolveNamesResponseMessage
api_type:
- schema
ms.assetid: edcdaf58-ef63-412e-8c58-409213e6ab0d
description: El elemento ResolveNamesResponseMessage contiene el estado y el resultado de una solicitud de operación ResolveNames.
ms.openlocfilehash: 12f32008dbbc603fca7adf26057f1f1904d3cfb2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455600"
---
# <a name="resolvenamesresponsemessage"></a>ResolveNamesResponseMessage

El elemento **ResolveNamesResponseMessage** contiene el estado y el resultado de una solicitud de [operación ResolveNames](resolvenames-operation.md) . 
  
- [ResolveNamesResponse](resolvenamesresponse.md) 
- [ResponseMessages](responsemessages.md)
- [ResolveNamesResponseMessage](resolvenamesresponsemessage.md)
  
```xml
<ResolveNamesResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <ResolutionSet/>
</ResolveNamesResponseMessage>
```

 **ResolveNamesResponseMessageType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**ResponseClass** <br/> | Describe el estado de una respuesta de [operación de ResolveNames](resolvenames-operation.md) . <br/><br/>Los siguientes valores son válidos para este atributo:  <br/><br/>-Correcto  <br/>-ADVERTENCIA  <br/>-Error  <br/> |
   
#### <a name="responseclass-attribute"></a>Atributo ResponseClass

|**Valor**|**Descripción**|
|:-----|:-----|
|**Success** <br/> |Describe una solicitud que se ha completado. Esto ocurre cuando el nombre solicitado es inequívoco y la respuesta contiene un único destinatario.  <br/> |
|**Advertencia** <br/> | Describe una solicitud que no se ha procesado. Se puede devolver una advertencia si se produjo un error al procesar un elemento de la solicitud y no se pudieron procesar los siguientes elementos. <br/><br/>Los siguientes son ejemplos de fuentes de advertencias:  <br/><br/>-El almacén de Exchange se desconecta durante el lote.  <br/>-Servicios de dominio de Active Directory (AD DS) se desconecta.  <br/>-Se mueven los buzones.  <br/>-La base de datos de buzones (MDB) se desconecta.  <br/>-Una contraseña ha expirado.  <br/>-Se ha superado la cuota.  <br/>-El nombre solicitado es ambiguo y la respuesta contiene varios destinatarios.  <br/> |
|**Error** <br/> | Describe una solicitud que no se puede cumplir. <br/><br/>Los siguientes son ejemplos de orígenes de errores:  <br/><br/>-No se pudo resolver el nombre solicitado.  <br/>-Los atributos o elementos no son válidos.  <br/>-Los atributos o elementos están fuera del intervalo.  <br/>-Se desconoce la etiqueta.  <br/>-Un atributo o elemento no es válido en el contexto.  <br/>-Se produjo un intento de acceso no autorizado por parte de cualquier cliente.  <br/>-Se produjo un error del servidor en respuesta a una llamada válida del lado cliente.  <br/>  <br/>La información sobre el error se puede encontrar en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[MessageText](messagetext.md) <br/> |Proporciona una descripción de texto del estado de la respuesta.  <br/> |
|[ResponseCode](responsecode.md) <br/> |Proporciona información de error sobre la solicitud.  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |Actualmente no se usa y está reservado para su uso en el futuro. Contiene un valor de 0.  <br/> |
|[MessageXml](messagexml.md) <br/> |Proporciona información de respuesta de error adicional.  <br/> |
|[ResolutionSet](resolutionset.md) <br/> |Contiene una matriz de resoluciones para un nombre ambiguo.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |Contiene los mensajes de respuesta de una solicitud de servicios web Exchange.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [ResolveNames](resolvenames.md)
- [ResolveNamesResponse](resolvenamesresponse.md)
- [Operación ResolveNames](resolvenames-operation.md)

