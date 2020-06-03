---
title: InternetMessageHeader
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- InternetMessageHeader
api_type:
- schema
ms.assetid: c70675f8-6feb-4c89-ba48-bce0479b308b
description: El elemento InternetMessageHeader representa el encabezado de un mensaje de Internet para un encabezado determinado dentro de la colección de encabezados. Para obtener toda la colección de encabezados de mensajes de Internet, use la propiedad PR_TRANSPORT_MESSAGE_HEADERS. Para obtener más información acerca de los encabezados de mensajes de Internet y EWS, Consulteobtener los encabezados de mensajes de Internet en EWS, MIME y los encabezados de mensajes de Internet que faltan.
ms.openlocfilehash: 7b662617e0b1a1fcdcce3449b729485ba6e0956b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459310"
---
# <a name="internetmessageheader"></a>InternetMessageHeader

El elemento **InternetMessageHeader** representa el encabezado de un mensaje de Internet para un encabezado determinado dentro de la colección de encabezados. Para obtener toda la colección de encabezados de mensajes de Internet, use la propiedad **PR_TRANSPORT_MESSAGE_HEADERS** . Para obtener más información acerca de los encabezados de mensajes de Internet y EWS, consulte "obtener encabezados de mensajes de Internet en [EWS, MIME y los encabezados de mensajes de Internet que faltan](https://msdn.microsoft.com/library/exchange/hh545614%28v=exchg.140%29.aspx).
  
```XML
<InternetMessageHeader HeaderName=""/>
```

 **InternetHeaderType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**HeaderName** <br/> |Identifica el nombre del encabezado.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[InternetMessageHeaders](internetmessageheaders.md) <br/> |Representa la colección de todos los encabezados de mensajes de Internet que contiene un elemento en un buzón.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa el valor del encabezado.
  
## <a name="remarks"></a>Comentarios

La siguiente es la definición de propiedad extendida de la API administrada de EWS para la propiedad **PR_TRANSPORT_MESSAGE_HEADERS** . 
  
```cs
ExtendedPropertyDefinition transportMsgHdr = new ExtendedPropertyDefinition(0x007D, MapiPropertyType.String);
```

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


[EWS, MIME y los encabezados de mensajes de Internet que faltan](https://msdn.microsoft.com/library/exchange/hh545614%28v=exchg.140%29.aspx)

