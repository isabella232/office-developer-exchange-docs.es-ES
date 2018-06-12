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
description: El elemento InternetMessageHeader representa el encabezado del mensaje de Internet para un determinado encabezado dentro de la colección de encabezados. Para obtener la colección completa de los encabezados de mensaje de Internet, utilice la propiedad PR_TRANSPORT_MESSAGE_HEADERS. Para obtener más información acerca de los encabezados de mensaje EWS y Internet, seeGetting los encabezados de mensaje de Internet en EWS, MIME y los encabezados de mensaje de Internet que faltan.
ms.openlocfilehash: 9457cdabe99c0adcb8183cbc039cc86db881fec7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19835952"
---
# <a name="internetmessageheader"></a>InternetMessageHeader

El elemento **InternetMessageHeader** representa el encabezado del mensaje de Internet para un determinado encabezado dentro de la colección de encabezados. Para obtener la colección completa de los encabezados de mensaje de Internet, utilice la propiedad **PR_TRANSPORT_MESSAGE_HEADERS** . Para obtener más información acerca de los encabezados de mensaje EWS y en Internet, vea "encabezados de mensajes de Internet de introducción de [EWS, MIME y los encabezados de mensaje de Internet que faltan](http://msdn.microsoft.com/en-us/library/exchange/hh545614%28v=exchg.140%29.aspx).
  
```XML
<InternetMessageHeader HeaderName=""/>
```

 **InternetHeaderType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|**HeaderName** <br/> |Identifica el nombre de encabezado.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[InternetMessageHeaders](internetmessageheaders.md) <br/> |Representa la colección de todos los encabezados de mensaje de Internet que están contenidos en un elemento en un buzón de correo.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa el valor del encabezado.
  
## <a name="remarks"></a>Notas

La siguiente es la API administrada de EWS extendido definición de propiedad para la propiedad **PR_TRANSPORT_MESSAGE_HEADERS** . 
  
```cs
ExtendedPropertyDefinition transportMsgHdr = new ExtendedPropertyDefinition(0x007D, MapiPropertyType.String);
```

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)


[EWS, MIME y los encabezados de mensaje de Internet que faltan](http://msdn.microsoft.com/en-us/library/exchange/hh545614%28v=exchg.140%29.aspx)

