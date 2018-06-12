---
title: SeekToConditionPageItemView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b3b86720-d086-47c3-94af-921fdd719edf
description: El elemento SeekToConditionPageItemView identifica la condición que se usa para identificar el final de una búsqueda, el índice de inicio de una búsqueda, las entradas máximas para devolver y las instrucciones de búsqueda para una búsqueda FindItem o FindConversation.
ms.openlocfilehash: e95246079f8c6e7acffac1dabb278895265767d9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837328"
---
# <a name="seektoconditionpageitemview"></a>SeekToConditionPageItemView

El elemento **SeekToConditionPageItemView** identifica la condición que se usa para identificar el final de una búsqueda, el índice de inicio de una búsqueda, las entradas máximas para devolver y las instrucciones de búsqueda para un **FindItem** o **FindConversation **búsqueda. 
  
```XML
<SeekToConditionPageItemView BasePoint="" MaxEntriesReturned="">
   <Condition/>
</SeekToConditionPageItemView>
```

 **SeekToConditionPageViewType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|Punto base  <br/> |El valor de texto del atributo **punto base** es el punto de partida desde donde se iniciará la búsqueda. Un valor de texto de **principio** indica que la búsqueda se iniciará al principio del conjunto de resultados. Un valor de texto de **final** indica que la búsqueda se iniciará al final del conjunto de resultados.  <br/> |
|MaxEntriesReturned  <br/> |El valor de texto del atributo **MaxEntriesReturned** es el número máximo de elementos que se pueden devolver en un conjunto de resultados.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

[Condición (RestrictionType)](condition-restrictiontype.md)
  
### <a name="parent-elements"></a>Elementos principales

[FindConversation](findconversation.md) | [FindItem](finditem.md)
  
## <a name="remarks"></a>Notas

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |falso  <br/> |
   

