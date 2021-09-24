---
title: InternetMessageHeader
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- InternetMessageHeader
api_type:
- schema
ms.assetid: c70675f8-6feb-4c89-ba48-bce0479b308b
description: El elemento InternetMessageHeader representa el encabezado de mensaje de Internet de un encabezado determinado dentro de la colección headers. Para obtener toda la colección de encabezados de mensajes de Internet, use la PR_TRANSPORT_MESSAGE_HEADERS propiedad. Para obtener más información acerca de los encabezados de mensajes ews e Internet, veaGetting Internet message headers in EWS, MIME, and the missing Internet message headers.
ms.openlocfilehash: 4b3072611e8a3debf87ce2a023f4f68ee4487185
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59541089"
---
# <a name="internetmessageheader"></a>InternetMessageHeader

El **elemento InternetMessageHeader** representa el encabezado de mensaje de Internet de un encabezado determinado dentro de la colección headers. Para obtener toda la colección de encabezados de mensajes de Internet, use la **PR_TRANSPORT_MESSAGE_HEADERS** propiedad. Para obtener más información acerca de los encabezados de mensajes ews e Internet, vea "Obtener encabezados de mensaje de Internet en EWS, MIME y los encabezados de mensaje [de Internet que faltan.](https://msdn.microsoft.com/library/exchange/hh545614%28v=exchg.140%29.aspx)
  
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

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[InternetMessageHeaders](internetmessageheaders.md) <br/> |Representa la colección de todos los encabezados de mensaje de Internet contenidos en un elemento de un buzón.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa el valor del encabezado.
  
## <a name="remarks"></a>Comentarios

A continuación se muestra la definición de propiedad extendida de la API administrada ews **para la PR_TRANSPORT_MESSAGE_HEADERS** propiedad. 
  
```cs
ExtendedPropertyDefinition transportMsgHdr = new ExtendedPropertyDefinition(0x007D, MapiPropertyType.String);
```

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


[EWS, MIME y los encabezados de mensajes de Internet que faltan](https://msdn.microsoft.com/library/exchange/hh545614%28v=exchg.140%29.aspx)

