---
title: SeekToConditionPageItemView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b3b86720-d086-47c3-94af-921fdd719edf
description: El elemento SeekToConditionPageItemView identifica la condición que se usa para identificar el final de una búsqueda, el índice inicial de una búsqueda, las entradas máximas que se devolverán y las direcciones de búsqueda de una búsqueda de FindItem o FindConversation.
ms.openlocfilehash: dbb073263740ccdf75367f85f672b7d5ec78f7a0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466839"
---
# <a name="seektoconditionpageitemview"></a>SeekToConditionPageItemView

El elemento **SeekToConditionPageItemView** identifica la condición que se usa para identificar el final de una búsqueda, el índice inicial de una búsqueda, las entradas máximas que se devolverán y las direcciones de búsqueda de una búsqueda de **FindItem** o **FindConversation** . 
  
```XML
<SeekToConditionPageItemView BasePoint="" MaxEntriesReturned="">
   <Condition/>
</SeekToConditionPageItemView>
```

 **SeekToConditionPageViewType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|BasePoint  <br/> |El valor de texto del atributo **BasePoint** es el punto base desde el que se iniciará la búsqueda. Un valor de texto **inicial** indica que la búsqueda se iniciará al principio del conjunto de resultados. Un valor de texto de **End** indica que la búsqueda comenzará al final del conjunto de resultados.  <br/> |
|MaxEntriesReturned  <br/> |El valor de texto del atributo **MaxEntriesReturned** es el número máximo de elementos que se pueden devolver en un conjunto de resultados.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

[Condición (RestrictionType)](condition-restrictiontype.md)
  
### <a name="parent-elements"></a>Elementos principales

[FindConversation](findconversation.md)  |  [FindItem](finditem.md)
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |false  <br/> |
   

