---
title: Estado
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Status
api_type:
- schema
ms.assetid: 80121e41-291b-4fc0-a55e-6f677d4b5fb5
description: El elemento Status representa el estado de un elemento de tarea.
ms.openlocfilehash: 5ec50e3f0c06ad3ec8301ddbe8e7bd249b1e8fe9
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59525543"
---
# <a name="status"></a>Estado

El **elemento Status** representa el estado de un elemento de tarea. 
  
```xml
<Status/>
```

 **TaskStatusType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Tarea](task.md) <br/> |Representa una tarea en el Exchange almacén.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto. Los siguientes son los valores de texto posibles para este elemento:
  
- NotStarted
    
- InProgress
    
- Completado
    
- WaitingOnOthers
    
- Diferido
    
## <a name="remarks"></a>Comentarios

Establecer [CompleteDate](completedate.md) tiene el mismo efecto que establecer [PercentComplete](percentcomplete.md) en 100 o **Status** en **Completed**. En una solicitud que establece al menos dos de estas propiedades, la última propiedad procesada determinará el valor que se establece para estos elementos. Por ejemplo, si **PercentComplete** es 100, **CompleteDate** es 1/1/2007 y **Status** es NotStarted y las propiedades  se transmiten en este orden, el efecto será establecer el estado de la tarea en NotStarted, **CompleteDate** en **null** y **PercentComplete** en 0. 
  
El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)


[Creación de tareas](https://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx)
  
[Eliminación de tareas](https://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

