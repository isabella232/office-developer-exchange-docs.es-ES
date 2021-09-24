---
title: Operación UpdateItem (tarea)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- UpdateItem
api_type:
- schema
ms.assetid: b0a7f114-d040-40eb-a8f3-05ea6489e472
description: La operación UpdateItem se usa para actualizar las propiedades del elemento de tarea en el Exchange de tareas.
ms.openlocfilehash: a268b4b281f149f14bc6c48a774fc9071093ebb5
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510753"
---
# <a name="updateitem-operation-task"></a>Operación UpdateItem (tarea)

La operación UpdateItem se usa para actualizar las propiedades del elemento de tarea en el Exchange de tareas.
  
## <a name="remarks"></a>Comentarios

No puede usar Exchange Web Services para enviar solicitudes de tareas. Exchange Los servicios web pueden devolver solicitudes de tareas creadas por MicrosoftOfficeOutlook. Si ya se ha enviado una solicitud de tarea, una solicitud para actualizar la tarea devolverá un error.
  
## <a name="updating-the-current-occurrence-of-a-recurring-task"></a>Actualización de la repetición actual de una tarea periódica

El resultado de una operación UpdateItem en tareas periódicas difiere del resultado de la operación UpdateItem en una sola tarea no recurrente. Los cambios en una repetición de una tarea periódica hacen que las tareas únicas se generen cuando se realicen las siguientes actualizaciones:
  
1. La propiedad status de una tarea recurrente regeneradora o no generadora se establece en **Completed**.
    
2. Se cambia la fecha de inicio o la fecha de finalización de una tarea recurrente no generadora.
    
Por ejemplo, si una solicitud **UpdateItem** establece el valor Completado de una tarea periódica en **true**, **UpdateItemResponse** incluirá un nuevo Identificador y ChangeKey que representan una tarea única recién creada. El identificador que se incluyó en la solicitud sigue siendo válido y la tarea periódica representada por ese identificador se ha actualizado para representar la siguiente repetición. La clave de cambio que se incluyó en la solicitud ya no es válida porque se ha actualizado la tarea periódica. 
  
Puede usar la operación [GetItem para](getitem-operation.md) obtener el **changekey** más reciente para la tarea periódica. 
  
Para las tareas no recurrentes o para la última aparición de una tarea periódica, la respuesta UpdateItem devuelve el mismo **identificador** que se le pasó y devuelve el changekey actualizado **asociado.**
  
## <a name="see-also"></a>Ver también



[Operación UpdateItem](updateitem-operation.md)

