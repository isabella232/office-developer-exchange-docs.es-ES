---
title: Rango
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ee2891e4-3aa6-4258-9727-1f2ee9622508
description: El elemento Range especifica un intervalo de repeticiones de elementos de calendario para un elemento de calendario que se repite.
ms.openlocfilehash: b5fb41709905290326b47e2662383031c34fd9c9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465313"
---
# <a name="range"></a>Rango

El elemento **Range** especifica un intervalo de repeticiones de elementos de calendario para un elemento de calendario que se repite. 
  
```XML
<Range Start="" End="" Count="" CompareOriginalStartTime=""/>
```

 **OccurrencesRangeType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**Start** <br/> |El valor de texto del atributo **Start** es la fecha de inicio del intervalo de elementos periódicos. Se trata de un valor de **fecha y hora** .  <br/> |
|**End** <br/> |El valor de texto del atributo **final** es la fecha de finalización del intervalo de elementos periódicos. Se trata de un valor de **fecha y hora** .  <br/> |
|**Count** <br/> |El valor de texto del atributo **Count** es el número de repeticiones del elemento periódico. Se trata de un valor **entero** .  <br/> |
|**CompareOriginalStartTime** <br/> |El valor de texto de **true** para el atributo **CompareOriginalStartTime** indica que el cliente debe comparar la hora de inicio original con la nueva hora de inicio. Un valor de **false** indica que el cliente no tiene que comparar la hora de inicio original con la nueva hora de inicio.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

[Ranges](ranges.md)
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> ||
   

