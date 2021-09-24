---
title: Assignees
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 20ef18c2-daa0-4f65-a515-e84e9993a77f
description: El elemento Assignees especifica las personas a las que se asigna una tarea.
ms.openlocfilehash: 1b5368dbe478e51a23f1f0761635e017b935911d
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59525193"
---
# <a name="assignees"></a>Assignees

El **elemento Assignees** especifica las personas a las que se asigna una tarea. 
  
```XML
<Assignees>
    <Name></Name>
    <UserID></UserID>
</Assignees>
```

 **EmailUserType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Name (EmailAddress)](name-emailaddress.md) <br/> |Representa el nombre para mostrar del usuario del buzón.  <br/> |
|[UserId (cadena)](userid-string.md) <br/> |Especifica el identificador de usuario de un usuario de correo electrónico.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[TaskSuggestion](tasksuggestion.md) <br/> |Especifica una tarea propuesta.  <br/> |
   
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

