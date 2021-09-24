---
title: IsHidden
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 2377b584-bd1e-49fc-b80a-a6634721a297
description: El elemento IsHidden contiene un valor booleano que indica si el contacto subyacente debe ocultarse o mostrarse como parte de la persona.
ms.openlocfilehash: 7ff24eaa5e8e7b25c87af0bf299fcca0d88dc0b6
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59532791"
---
# <a name="ishidden"></a>IsHidden

El **elemento IsHidden** contiene un valor booleano que indica si el contacto subyacente debe ocultarse o mostrarse como parte de la persona. 
  
```XML
<IsHidden>true | false</IsHidden>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Attribution (PersonaAttributionType)](attribution-personaattributiontype.md) <br/> |Especifica una instancia en una matriz de atributos para un **elemento Persona.**  <br/> |
   
## <a name="text-value"></a>Valor de texto

Un valor de texto **de true** para el **elemento IsHidden** indica que el contacto subyacente debe ocultarse o mostrarse como parte de la persona. Un valor de **false** indica que el contacto subyacente no debe ocultarse ni mostrarse como parte de la persona. 
  
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

