---
title: SortOrder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- SortOrder
api_type:
- schema
ms.assetid: c2413f0b-8c03-46ae-9990-13338b3c53a6
description: El elemento SortOrder define cómo se ordenan los elementos en una solicitud FindItem o FindConversation.
ms.openlocfilehash: eefa10c4af32d550414d83f8f524b5b088fcfa7c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59531704"
---
# <a name="sortorder"></a>SortOrder

El **elemento SortOrder** define cómo se ordenan los elementos en una **solicitud FindItem** o **FindConversation.** 
  
```xml
<SortOrder>
   <FieldOrder/>
</SortOrder>
```

 **NonEmptyArrayOfFieldOrdersType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FieldOrder](fieldorder.md) <br/> |Representa un único campo por el que se ordenan los resultados e indica la dirección de la ordenación. Se pueden incluir uno o varios de estos elementos. [Los elementos FieldOrder](fieldorder.md) se aplican en el orden especificado para la ordenación.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FindItem](finditem.md) <br/> |Define una solicitud para buscar elementos en un buzón.  <br/> A continuación se muestra la expresión XPath de este elemento:  `/FindItem` <br/> |
|[FindConversation](findconversation.md) <br/> |Define una solicitud para buscar conversaciones en un buzón.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación FindItem](finditem-operation.md)
  
[Operación FindConversation](findconversation-operation.md)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

