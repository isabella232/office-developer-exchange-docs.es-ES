---
title: Operación UpdateItem (tarea)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateItem
api_type:
- schema
ms.assetid: b0a7f114-d040-40eb-a8f3-05ea6489e472
description: La operación UpdateItem se utiliza para actualizar las propiedades del elemento de tarea en el almacén de Exchange.
ms.openlocfilehash: d6f966fa663300b476383a136d30cf611d6bfb9b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840840"
---
# <a name="updateitem-operation-task"></a>Operación UpdateItem (tarea)

La operación UpdateItem se utiliza para actualizar las propiedades del elemento de tarea en el almacén de Exchange.
  
## <a name="remarks"></a>Comentarios

No puede usar servicios Web de Exchange para enviar solicitudes de tareas. Servicios Web de Exchange puede devolver las solicitudes de tarea que se crean de forma MicrosoftOfficeOutlook. Si ya se ha enviado una solicitud de tarea, una solicitud para actualizar la tarea devolverá un error.
  
## <a name="updating-the-current-occurrence-of-a-recurring-task"></a>Actualizar la aparición actual de una tarea periódica

El resultado de una operación UpdateItem en tareas repetitivas difiere el resultado de la operación UpdateItem en una sola tarea no periódica. Los cambios realizados en una ocurrencia de una tarea periódica que constituye tareas se generan cuando se realizan las siguientes actualizaciones:
  
1. La propiedad de estado de una tarea periódica regenerada o nonregenerating se establece como **completada**.
    
2. Se cambia la fecha de comienzo o fecha de finalización de una tarea periódica nonregenerating.
    
Por ejemplo, si una solicitud **UpdateItem** establece el valor de completado de una tarea periódica en **true**, la **UpdateItemResponse** incluirá un nuevo identificador y ChangeKey que representan una tarea de uso único recién creada. El identificador que se ha incluido en la solicitud todavía es válido y se ha actualizado la tarea periódica que está representada por el Id para representar la siguiente aparición. El ChangeKey que se ha incluido en la solicitud ya no es válido porque se ha actualizado la tarea repetitiva. 
  
Puede usar la [operación GetItem](getitem-operation.md) para obtener la más reciente **ChangeKey** para la tarea repetitiva. 
  
Para las tareas no periódicas o la última aparición de una tarea periódica, la respuesta UpdateItem devuelve el mismo **identificador** que se pasó a ella y devuelve que el asociado actualizó **ChangeKey**.
  
## <a name="see-also"></a>Vea también



[Operación UpdateItem](updateitem-operation.md)

