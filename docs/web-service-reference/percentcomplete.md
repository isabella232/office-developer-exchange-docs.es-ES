---
title: PercentComplete
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PercentComplete
api_type:
- schema
ms.assetid: 58a67f8a-c4dc-42dc-97ae-a9e5cc672d2d
description: El elemento PercentComplete describe el estado de finalización de una tarea.
ms.openlocfilehash: 18e53221ecdf60df195445ed7692c03795bdcc1e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836717"
---
# <a name="percentcomplete"></a>PercentComplete

El elemento **PercentComplete** describe el estado de finalización de una tarea. 
  
```xml
<PercentComplete/>
```

 **doble**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Tarea](task.md) <br/> |Representa una tarea en el almacén de Exchange.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto que representa un número entero entre 0 y 100.
  
## <a name="remarks"></a>Comentarios

Si se establece **PercentComplete** en 100 tiene el mismo efecto que establecer el elemento [CompleteDate](completedate.md) o establecer el elemento de [estado](status.md) en **completada**. En una solicitud que conjuntos de al menos dos de estas propiedades, la última propiedad procesada determinará el valor que se establece para estos elementos. Por ejemplo, si **PercentComplete** es 100, [CompleteDate](completedate.md) es el 1 de enero de 2007 y [estado](status.md) es no iniciado y las propiedades se transmiten en este orden, el efecto será establecer el [estado](status.md) de la tarea en NotStarted, el [ CompleteDate](completedate.md) en **null**y **PercentComplete** en 0. 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)


[Creación de tareas](http://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx)
  
[Eliminación de tareas](http://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

