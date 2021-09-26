---
title: IsAssignmentEditable
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IsAssignmentEditable
api_type:
- schema
ms.assetid: 0ddf9181-f65e-4ad6-ad69-7b074ea0f2e7
description: El elemento IsAssignmentEditable representa el tipo de tarea.
ms.openlocfilehash: 10676cc8c6196a7294f3550856a47dce7d717e6a
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544953"
---
# <a name="isassignmenteditable"></a>IsAssignmentEditable

El **elemento IsAssignmentEditable** representa el tipo de tarea. 
  
```xml
<IsAssignmentEditable/>
```

 **entero**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Tarea](task.md) <br/> |Representa una tarea en el Exchange almacén.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Esta propiedad es de sólo lectura. En la tabla siguiente se enumeran los valores posibles.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|0  <br/> |Valor predeterminado para todos los elementos de tarea.  <br/> |
|1  <br/> |Una solicitud de tarea.  <br/> |
|2  <br/> |Una aceptación de tarea de un destinatario de una solicitud de tarea.  <br/> |
|3  <br/> |Declinación de tareas de un destinatario de una solicitud de tarea.  <br/> |
|4   <br/> |Una actualización de una solicitud de tarea anterior.  <br/> |
|5  <br/> |No se usa.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Consulte también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

