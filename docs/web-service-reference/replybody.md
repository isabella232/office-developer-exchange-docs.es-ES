---
title: ReplyBody
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ReplyBody
api_type:
- schema
ms.assetid: bb184144-3e4b-4419-a883-cc9fab1085e6
description: El elemento ReplyBody contiene un mensaje De Office (OOF) y el idioma usado para el mensaje.
ms.openlocfilehash: 75af64277467246c7edcc2a48708bbf3f3c95c48
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59517955"
---
# <a name="replybody"></a>ReplyBody

El **elemento ReplyBody** contiene un mensaje De Office (OOF) y el idioma usado para el mensaje. 
  
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
|xml:lang  <br/> |Especifica el idioma usado en el **contenido replybody.** Este atributo es opcional. Los valores posibles de este atributo se definen mediante IETF RFC 3066.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Message (Availability)](message-availability.md) <br/> |Contiene la respuesta de fuera de la oficina (OOF).  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[OutOfOffice](outofoffice.md) <br/> |Define el mensaje de respuesta OOF y un tiempo de duración para enviar el mensaje de respuesta para un buzón.  <br/> |
   
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
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

