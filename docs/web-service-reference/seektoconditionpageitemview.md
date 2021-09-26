---
title: SeekToConditionPageItemView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: b3b86720-d086-47c3-94af-921fdd719edf
description: El elemento SeekToConditionPageItemView identifica la condición que se usa para identificar el final de una búsqueda, el índice inicial de una búsqueda, las entradas máximas que se devolverán y las direcciones de búsqueda de una búsqueda FindItem o FindConversation.
ms.openlocfilehash: 6f4797a6b90456a50922db1c829757711816273e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59546108"
---
# <a name="seektoconditionpageitemview"></a>SeekToConditionPageItemView

El **elemento SeekToConditionPageItemView** identifica la condición que se usa para identificar el final de una búsqueda, el índice inicial de una búsqueda, las entradas máximas que se devolverán y las direcciones de búsqueda de una búsqueda **FindItem** o **FindConversation.** 
  
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
|BasePoint  <br/> |El valor de texto del **atributo BasePoint** es el punto base desde el que se iniciará la búsqueda. Un valor de texto **de Beginning** indica que la búsqueda se iniciará al principio del conjunto de resultados. Un valor de texto **de End** indica que la búsqueda se iniciará al final del conjunto de resultados.  <br/> |
|MaxEntriesReturned  <br/> |El valor de texto del **atributo MaxEntriesReturned** es el número máximo de elementos que se pueden devolver en un conjunto de resultados.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

[Condition (RestrictionType)](condition-restrictiontype.md)
  
### <a name="parent-elements"></a>Elementos principales

[FindConversation](findconversation.md)  |  [FindItem](finditem.md)
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre del esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |false  <br/> |
   

