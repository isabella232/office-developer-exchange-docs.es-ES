---
title: Data (base64Binary)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Data
api_type:
- schema
ms.assetid: 26d8c2d0-bed2-4aed-b381-20e2ace6892f
description: El elemento Data contiene los datos de un solo elemento exportado o de un elemento que se cargará en un buzón.
ms.openlocfilehash: 69e15746f17febb74a0ec2f56eef0eaa1e298015
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59535937"
---
# <a name="data-base64binary"></a>Data (base64Binary)

El **elemento Data** contiene los datos de un solo elemento exportado o de un elemento que se cargará en un buzón. 
  
```XML
<Data/>
```

**xs:base64Binary**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ExportItemsResponseMessage](exportitemsresponsemessage.md) <br/> |Contiene el estado y los resultados de una solicitud para exportar un único elemento de buzón.  <br/> |
|[Item (UploadItemType)](item-uploaditemtype.md) <br/> |Representa un único elemento para cargar en un buzón.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El **elemento Data** contiene los nombres de propiedad y los valores de un elemento exportado o un elemento que se cargará en un buzón. 
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda Exchange Web Services.Este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensaje  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también

- [Operación ExportItems](exportitems-operation.md)
- [Operación UploadItems](uploaditems-operation.md)

