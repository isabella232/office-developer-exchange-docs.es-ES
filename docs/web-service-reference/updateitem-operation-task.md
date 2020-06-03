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
description: La operación UpdateItem se usa para actualizar las propiedades de los elementos de tarea en el almacén de Exchange.
ms.openlocfilehash: 0041af114d11fd9577037dd154e40b84e8483c35
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459808"
---
# <a name="updateitem-operation-task"></a>Operación UpdateItem (tarea)

La operación UpdateItem se usa para actualizar las propiedades de los elementos de tarea en el almacén de Exchange.
  
## <a name="remarks"></a>Comentarios

No puede usar los servicios web Exchange para enviar solicitudes de tareas. Los servicios Web de Exchange pueden devolver solicitudes de tareas creadas por MicrosoftOfficeOutlook. Si ya se ha enviado una solicitud de tarea, una solicitud para actualizar la tarea devolverá un error.
  
## <a name="updating-the-current-occurrence-of-a-recurring-task"></a>Actualización de la ocurrencia actual de una tarea recurrente

El resultado de una operación UpdateItem en tareas periódicas difiere del resultado de la operación UpdateItem en una sola tarea recurrente. Los cambios en una ocurrencia de una tarea repetitiva provocan que las tareas de uso único se generen cuando se realicen las siguientes actualizaciones:
  
1. La propiedad status de una tarea regenerada o nonregenerating recurrente se establece en **completada**.
    
2. Se cambia la fecha de inicio o la fecha de finalización de una tarea periódica nonregenerating.
    
Por ejemplo, si una solicitud de **UpdateItem** establece el valor completado de una tarea recurrente en **true**, el **UpdateItemResponse** incluirá un nuevo identificador y changekey que representan una tarea de un solo uso recién creada. El identificador que se incluyó en la solicitud sigue siendo válido y la tarea recurrente representada por ese identificador se ha actualizado para representar la siguiente ocurrencia. La ChangeKey que se incluyó en la solicitud ya no es válida porque se ha actualizado la tarea repetitiva. 
  
Puede usar la [operación GetItem](getitem-operation.md) para obtener el último **changekey** de la tarea repetitiva. 
  
Para las tareas no periódicas o para la última repetición de una tarea repetitiva, la respuesta UpdateItem devuelve el mismo **identificador** que se pasó y devuelve el **changekey**actualizado asociado.
  
## <a name="see-also"></a>Vea también



[Operación UpdateItem](updateitem-operation.md)

