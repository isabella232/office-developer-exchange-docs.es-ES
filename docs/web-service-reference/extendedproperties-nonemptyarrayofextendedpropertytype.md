---
title: ExtendedProperties (NonEmptyArrayOfExtendedPropertyType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a7034730-210d-4916-b992-dda342f890f8
description: El elemento ExtendedProperties especifica una matriz de propiedades adicionales.
ms.openlocfilehash: 36011e0252ed391daefab190d4da679fb3a3f856
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463100"
---
# <a name="extendedproperties-nonemptyarrayofextendedpropertytype"></a>ExtendedProperties (NonEmptyArrayOfExtendedPropertyType)

El elemento **ExtendedProperties** especifica una matriz de propiedades adicionales. 
  
```XML
<ExtendedProperties>
    <ExtendedProperty/>
</ExtendedProperties>
```

 **NonEmptyArrayOfExtendedPropertyType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Las extendedproperty](extendedproperty.md) <br/> |Identifica las propiedades de MAPI extendidas en carpetas y elementos.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Desagrupo](imgroup.md) <br/> |Representa un grupo de mensajería instantánea.  <br/> |
|[SearchPreviewItem](searchpreviewitem.md) <br/> |Especifica los primeros 256 caracteres de un elemento de buzón de correo para la vista previa sin abrir el elemento.  <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipo  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> ||
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

