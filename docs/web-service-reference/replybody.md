---
title: ReplyBody
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ReplyBody
api_type:
- schema
ms.assetid: bb184144-3e4b-4419-a883-cc9fab1085e6
description: El elemento ReplyBody contiene un mensaje de fuera de la oficina (OOF) y el idioma usado para el mensaje.
ms.openlocfilehash: 496d336d1f87d9ea493ba7da362eef5a416fd899
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465306"
---
# <a name="replybody"></a>ReplyBody

El elemento **ReplyBody** contiene un mensaje de fuera de la oficina (OOF) y el idioma usado para el mensaje. 
  
```XML
<ReplyBody xml:lang="">
   <Message/>
</ReplyBody>
```

 **ReplyBody**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|XML: lang  <br/> |Especifica el idioma usado en el contenido de **ReplyBody** . Este atributo es opcional. Los valores posibles de este atributo los define el documento RFC 3066 de IETF.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Mensaje (disponibilidad)](message-availability.md) <br/> |Contiene la respuesta de fuera de la oficina (OOF).  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Oficina](outofoffice.md) <br/> |Define el mensaje de respuesta OOF y un tiempo de duración para enviar el mensaje de respuesta de un buzón.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

Se requiere este elemento.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

