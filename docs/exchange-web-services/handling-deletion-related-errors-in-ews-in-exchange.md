---
title: Administración de errores relacionados con la eliminación en EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1bbe8507-7730-45e5-9232-c4f6fc39c2d9
description: Descubra cómo tratar los errores relacionados con la eliminación en las aplicaciones que desarrolle mediante la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: 41c217c1c3815606d898b8237ea327f34869174b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455950"
---
# <a name="handling-deletion-related-errors-in-ews-in-exchange"></a>Administración de errores relacionados con la eliminación en EWS en Exchange

Descubra cómo tratar los errores relacionados con la eliminación en las aplicaciones que desarrolle mediante la API administrada de EWS o EWS en Exchange.
  
Si la aplicación [elimina elementos y carpetas](deleting-items-by-using-ews-in-exchange.md), es posible que deba controlar los errores relacionados con la eliminación. Puede controlar estos errores en tiempo de ejecución, o mientras está desarrollando su aplicación de EWS.
  
**Tabla 1: errores relacionados con la eliminación y cómo controlarlos**

|**Error**|**Se produce cuando se intenta...**|**Controlarla por...**|
|:-----|:-----|:-----|
|ErrorAffectedTaskOccurrencesRequired  <br/> |Elimine una instancia de una tarea repetitiva y no se ha establecido la propiedad **AffectedTaskOccurrence** .  <br/> |Establecer la propiedad **AffectedTaskOccurrence** y volver a intentar la eliminación.  <br/> |
|ErrorCalendarCannotUpdateDeletedItem  <br/> |Actualice un elemento de calendario ubicado en la carpeta elementos eliminados cuando la actualización daría como resultado el envío de una invitación de reunión a los asistentes.  <br/> |Cancelar la actualización o mover el elemento de calendario de nuevo a la carpeta de calendario predeterminada y actualizar el elemento de calendario.  <br/> |
|ErrorCalendarOccurrenceIsDeletedFromRecurrence  <br/> |Hacer referencia a una ocurrencia eliminada de una cita periódica.  <br/> |Quitar una referencia a una ocurrencia eliminada.  <br/> |
|ErrorCannotDeleteObject  <br/> |Eliminar un elemento que no se puede eliminar.  <br/> |Saliendo de los intentos para eliminar el elemento.  <br/> |
|ErrorCannotDeleteTaskOccurrence  <br/> |Eliminar una ocurrencia de una tarea no periódica o eliminar la última repetición de una tarea recurrente.  <br/> |Eliminar una tarea no periódica o salir de los intentos para eliminar la última repetición de una tarea repetitiva.  <br/> |
|ErrorDeleteDistinguishedFolder  <br/> |Eliminar una carpeta distintiva.  <br/> |Que indica que no se pueden eliminar las carpetas predeterminadas.  <br/> |
|ErrorItemNotFound  <br/> |Obtener acceso a un elemento eliminado permanentemente.  <br/> |Quitar referencias a un elemento cuando se elimina de la tienda. Si se recupera un elemento, asegúrese de restablecer las referencias necesarias en el cliente.  <br/> |
|ErrorSendMeetingCancellationsRequired  <br/> |Eliminar un elemento de calendario sin especificar si se deben enviar las cancelaciones de reunión.  <br/> |Especificar que las cancelaciones de reunión deben enviarse o no.  <br/> |
   
## <a name="see-also"></a>Vea también


- [Eliminación de elementos mediante EWS en Exchange](deleting-items-by-using-ews-in-exchange.md)
    
- [Notificaciones de extracción para eventos de buzón relacionados con la eliminación de EWS en Exchange](pull-notifications-for-ews-deletion-related-mailbox-events-in-exchange.md)
    
- [Eliminar citas y cancelar reuniones mediante EWS en Exchange](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)
    

