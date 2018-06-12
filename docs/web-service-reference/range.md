---
title: Rango
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ee2891e4-3aa6-4258-9727-1f2ee9622508
description: El elemento de intervalo especifica el intervalo de repeticiones del elemento de calendario para un elemento de calendario periódico.
ms.openlocfilehash: 0264c541604808b46a50e292b8ff75f205796295
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836946"
---
# <a name="range"></a>Rango

El elemento **Range** especifica el intervalo de repeticiones del elemento de calendario para un elemento de calendario periódico. 
  
```XML
<Range Start="" End="" Count="" CompareOriginalStartTime=""/>
```

 **OccurrencesRangeType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|**Start** <br/> |El valor de texto del atributo **Iniciar** es la fecha de inicio del intervalo de elemento periódico. Esto es un valor de **fecha y hora** .  <br/> |
|**End** <br/> |El valor de texto del atributo **final** es la fecha de finalización del intervalo de elemento periódico. Esto es un valor de **fecha y hora** .  <br/> |
|**Count** <br/> |El valor de texto del atributo **Count** es el número de repeticiones del elemento periódico. Esto es un valor **entero** .  <br/> |
|**CompareOriginalStartTime** <br/> |El valor de texto de **true** para el atributo **CompareOriginalStartTime** indica que el cliente debe comparar la hora de inicio original con la nueva hora de inicio. Un valor de **false** indica que el cliente no es necesario comparar la hora de inicio original con la nueva hora de inicio.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[Ranges](ranges.md)
  
## <a name="remarks"></a>Notas

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> ||
   

