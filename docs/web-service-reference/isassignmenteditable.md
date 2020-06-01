---
title: IsAssignmentEditable
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsAssignmentEditable
api_type:
- schema
ms.assetid: 0ddf9181-f65e-4ad6-ad69-7b074ea0f2e7
description: El elemento IsAssignmentEditable representa el tipo de tarea.
ms.openlocfilehash: 5eb091b24e2c97f7aa6072044fed998b6c9c1651
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468057"
---
# <a name="isassignmenteditable"></a>IsAssignmentEditable

El elemento **IsAssignmentEditable** representa el tipo de tarea. 
  
```xml
<IsAssignmentEditable/>
```

 **entero**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Tarea](task.md) <br/> |Representa una tarea del almacén de Exchange.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Esta propiedad es de sólo lectura. En la siguiente tabla se enumeran los valores posibles.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|comprendi  <br/> |El valor predeterminado para todos los elementos de tarea.  <br/> |
|1   <br/> |Una solicitud de tarea.  <br/> |
|segundo  <br/> |Una aceptación de tarea de un destinatario de una solicitud de tarea.  <br/> |
|3  <br/> |Disminución de una tarea de un destinatario de una solicitud de tarea.  <br/> |
|4   <br/> |Una actualización de una solicitud de tarea anterior.  <br/> |
|5   <br/> |No se usa.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

