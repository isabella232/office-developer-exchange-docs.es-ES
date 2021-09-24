---
title: Value (Message Tracking)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Value
api_type:
- schema
ms.assetid: cb2f228f-775a-4c7d-82e7-41c7c953c808
description: El elemento Value representa el valor de la propiedad de un informe de seguimiento de mensajes.
ms.openlocfilehash: c8aa4f3cc41e76b633ee1b244371de2f5410c944
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513965"
---
# <a name="value-message-tracking"></a>Value (Message Tracking)

El **elemento Value** representa el valor de la propiedad de un informe de seguimiento de mensajes. 
  
```xml
<Value/>
```

**String**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[TrackingPropertyType](trackingpropertytype.md) <br/> |Representa un par de nombres y valores de cadenas que se usan para crear propiedades para informes de seguimiento de mensajes.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto es opcional.
  
## <a name="remarks"></a>Comentarios

Este elemento puede producirse como máximo una vez en el [elemento TrackingPropertyType.](trackingpropertytype.md) 
  
El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda Exchange Web Services.Este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también

- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

