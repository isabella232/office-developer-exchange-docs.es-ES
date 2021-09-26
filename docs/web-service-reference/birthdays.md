---
title: Birthdays
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 5a84c19e-57cd-448e-af4f-c8005fd5f2a2
description: El elemento Birthdays especifica una matriz de cumpleaños, almacenada como cadenas, y los identificadores de sus atribuciones de origen para la persona asociada.
ms.openlocfilehash: a1ed3886d9492ba2819a93183c0042b74f1d364c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543607"
---
# <a name="birthdays"></a>Birthdays

El **elemento Birthdays** especifica una matriz de cumpleaños, almacenada como cadenas, y los identificadores de sus atribuciones de origen para la persona asociada. 
  
```XML
<Birthdays>
   <StringAttributedValue/>
</Birthdays>
```

 **ArrayOfStringAttributedValuesType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[StringAttributedValue](stringattributedvalue.md) <br/> |Especifica una instancia en una matriz de atributos asociados con un elemento persona.  <br/> |
   
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
   
## <a name="see-also"></a>Consulte también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

