---
title: NewBodyContent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- NewBodyContent
api_type:
- schema
ms.assetid: 0303600d-16d8-4685-88f2-980c5ca7e9a6
description: El elemento NewBodyContent representa el nuevo contenido del cuerpo de un mensaje.
ms.openlocfilehash: dcfa927bb284ff00e510d8c7b4b31910a70b3cbb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466860"
---
# <a name="newbodycontent"></a>NewBodyContent

El elemento **NewBodyContent** representa el nuevo contenido del cuerpo de un mensaje. 
  
```xml
<NewBodyContent BodyType=""/>
```

 **BodyType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**BodyType** <br/> |Representa el contenido del cuerpo real de un mensaje.  <br/> |
   
#### <a name="bodytype-attribute"></a>Atributo BodyType

|**Valor**|**Descripción**|
|:-----|:-----|
|**HTML** <br/> |Convierte todos los cuerpos en HTML.  <br/> |
|**Text** <br/> |Convierte todos los cuerpos en texto sin formato.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ReplyToItem](replytoitem.md) <br/> |Contiene una respuesta al remitente de un elemento en el almacén de Exchange.  <br/> |
|[ReplyAllToItem](replyalltoitem.md) <br/> |Contiene una respuesta al remitente y a todos los destinatarios identificados de un elemento en el almacén de Exchange.  <br/> |
|[ForwardItem](forwarditem.md) <br/> |Contiene un elemento de almacén de Exchange que se va a reenviar a los destinatarios.  <br/> |
|[CancelCalendarItem](cancelcalendaritem.md) <br/> |Representa el objeto de respuesta que se usa para cancelar una reunión.  <br/> |
|[PostReplyItem](postreplyitem.md) <br/> |Contiene una respuesta a un elemento post. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa el nuevo contenido del cuerpo de un mensaje.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del servidor de Exchange que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

