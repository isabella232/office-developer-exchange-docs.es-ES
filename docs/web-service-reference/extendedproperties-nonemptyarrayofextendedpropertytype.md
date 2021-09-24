---
title: ExtendedProperties (NonEmptyArrayOfExtendedPropertyType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: a7034730-210d-4916-b992-dda342f890f8
description: El elemento ExtendedProperties especifica una matriz de propiedades adicionales.
ms.openlocfilehash: 69099842ad25a0d4f65250b3477563537c569907
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520566"
---
# <a name="extendedproperties-nonemptyarrayofextendedpropertytype"></a>ExtendedProperties (NonEmptyArrayOfExtendedPropertyType)

El **elemento ExtendedProperties** especifica una matriz de propiedades adicionales. 
  
```XML
<ExtendedProperties>
    <ExtendedProperty/>
</ExtendedProperties>
```

 **NonEmptyArrayOfExtendedPropertyType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ExtendedProperty](extendedproperty.md) <br/> |Identifica las propiedades MAPI extendidas en carpetas y elementos.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ImGroup](imgroup.md) <br/> |Representa un grupo de mensajería instantánea.  <br/> |
|[SearchPreviewItem](searchpreviewitem.md) <br/> |Especifica los primeros 256 caracteres de un elemento de buzón para obtener una vista previa sin abrir el elemento.  <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipo  <br/> |
|Archivo de validación  <br/> |types.xsd  <br/> |
|Puede estar vacío  <br/> ||
   
## <a name="see-also"></a>Ver también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

