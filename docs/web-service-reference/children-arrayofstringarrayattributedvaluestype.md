---
title: Children (ArrayOfStringArrayAttributedValuesType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: d37b3fd5-63f1-4003-a6ec-54adfce23d52
description: El elemento Children especifica una matriz de nombres secundarios e identificadores de sus atribuciones de origen para la persona asociada.
ms.openlocfilehash: 878f491af3047d313920cd0f3574de2daa8c21f0
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59536977"
---
# <a name="children-arrayofstringarrayattributedvaluestype"></a>Children (ArrayOfStringArrayAttributedValuesType)

El **elemento Children** especifica una matriz de nombres secundarios e identificadores de sus atribuciones de origen para la persona asociada. 
  
```XML
<Children>
    <StringAttributedValue></StringAttributedValue>
</Children>
```

 **ArrayOfStringArrayAttributedValuesType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[StringArrayAttributedValue](stringarrayattributedvalue.md) <br/> |Especifica una instancia de una matriz de datos de cadena para un elemento persona.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Rol](persona.md) <br/> |Especifica un conjunto de datos de persona devueltos por una **solicitud GetPersona.**  <br/> |
   
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

