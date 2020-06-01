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
ms.openlocfilehash: b7dd2f18bd3ef6addeb6d3a7b004510f35b9cb3d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456888"
---
# <a name="percentcomplete"></a>PercentComplete

El elemento **PercentComplete** describe el estado de finalización de una tarea. 
  
```xml
<PercentComplete/>
```

 **hacer**
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

Un valor de texto que representa un entero entre 0 y 100 es necesario.
  
## <a name="remarks"></a>Comentarios

Establecer **PercentComplete** en 100 tiene el mismo efecto que establecer el elemento [CompleteDate](completedate.md) o establecer el elemento [status](status.md) en **completed**. En una solicitud que establece al menos dos propiedades, la última propiedad procesada determinará el valor que se establece para estos elementos. Por ejemplo, si **PercentComplete** es 100, [CompleteDate](completedate.md) es el 1 de enero de 2007 y [status](status.md) es NotStarted, y las propiedades se transmiten en este orden, el efecto será establecer el [Estado](status.md) de la tarea en notstarted, [CompleteDate](completedate.md) en **null**y **PercentComplete** en 0. 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)


[Creación de tareas](https://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx)
  
[Eliminación de tareas](https://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

