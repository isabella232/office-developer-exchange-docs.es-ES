---
title: Datos (base64Binary)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Data
api_type:
- schema
ms.assetid: 26d8c2d0-bed2-4aed-b381-20e2ace6892f
description: El elemento Data contiene los datos de un elemento exportado único o un elemento que se va a cargar en un buzón.
ms.openlocfilehash: 43ee16ca7caf634756ca00a88715d9834adad92b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526973"
---
# <a name="data-base64binary"></a>Datos (base64Binary)

El elemento **Data** contiene los datos de un elemento exportado único o un elemento que se va a cargar en un buzón. 
  
```XML
<Data/>
```

**XS: base64Binary**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ExportItemsResponseMessage](exportitemsresponsemessage.md) <br/> |Contiene el estado y los resultados de una solicitud para exportar un solo elemento de buzón.  <br/> |
|[Item (UploadItemType)](item-uploaditemtype.md) <br/> |Representa un solo elemento que se va a cargar en un buzón.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El elemento **Data** contiene los nombres y los valores de las propiedades de un elemento exportado o un elemento que se cargará en un buzón. 
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange. este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación ExportItems](exportitems-operation.md)
- [Operación UploadItems](uploaditems-operation.md)

