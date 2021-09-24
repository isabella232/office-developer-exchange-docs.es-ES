---
title: Controlar errores relacionados con la eliminación en EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 1bbe8507-7730-45e5-9232-c4f6fc39c2d9
description: Descubra cómo controlar los errores relacionados con la eliminación en las aplicaciones que desarrolle mediante la API administrada ews o EWS en Exchange.
ms.openlocfilehash: d82901a2ebc8577258e191cbd014db93cc40d099
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513258"
---
# <a name="handling-deletion-related-errors-in-ews-in-exchange"></a>Controlar errores relacionados con la eliminación en EWS en Exchange

Descubra cómo controlar los errores relacionados con la eliminación en las aplicaciones que desarrolle mediante la API administrada ews o EWS en Exchange.
  
Si la aplicación [elimina elementos y carpetas,](deleting-items-by-using-ews-in-exchange.md)es posible que tenga que controlar los errores relacionados con la eliminación. Puede controlar estos errores en tiempo de ejecución, o mientras está desarrollando su aplicación de EWS.
  
**Tabla 1: Errores relacionados con la eliminación y cómo controlarlos**

|**Error**|**Se produce cuando se intenta...**|**Controlarla por...**|
|:-----|:-----|:-----|
|ErrorAffectedTaskOccurrencesRequired  <br/> |Elimine una instancia de una tarea periódica y no se establezca la **propiedad AffectedTaskOccurrence.**  <br/> |Establecer la **propiedad AffectedTaskOccurrence** y volver a intentar la eliminación.  <br/> |
|ErrorCalendarCannotUpdateDeletedItem  <br/> |Actualice un elemento de calendario ubicado en la carpeta Elementos eliminados cuando la actualización daría como resultado el envío de una invitación a una reunión a los asistentes.  <br/> |Cancelar la actualización o mover el elemento de calendario de vuelta a la carpeta calendario predeterminada y actualizar el elemento de calendario.  <br/> |
|ErrorCalendarOccurrenceIsDeletedFromRecurrence  <br/> |Haga referencia a una repetición eliminada de una cita periódica.  <br/> |Quitar una referencia a una repetición eliminada.  <br/> |
|ErrorCannotDeleteObject  <br/> |Elimine un elemento que no se pueda eliminar.  <br/> |Salir de los intentos de eliminar el elemento.  <br/> |
|ErrorCannotDeleteTaskOccurrence  <br/> |Elimine una repetición de una tarea no recurrente o elimine la última aparición de una tarea periódica.  <br/> |Eliminar una tarea no recurrente o salir de los intentos de eliminar la última aparición de una tarea periódica.  <br/> |
|ErrorDeleteDistinguishedFolder  <br/> |Eliminar una carpeta distinguida.  <br/> |Indica que las carpetas predeterminadas no se pueden eliminar.  <br/> |
|ErrorItemNotFound  <br/> |Obtener acceso a un elemento eliminado permanentemente.  <br/> |Quitar referencias a un elemento cuando se elimina del almacén. Si se recupera un elemento, asegúrese de restablecer las referencias necesarias al cliente.  <br/> |
|ErrorSendMeetingCancellationsRequired  <br/> |Elimine un elemento de calendario sin especificar si se deben enviar cancelaciones de reunión.  <br/> |Especificar que las cancelaciones de reuniones deben enviarse o no.  <br/> |
   
## <a name="see-also"></a>Ver también


- [Eliminar elementos mediante EWS en Exchange](deleting-items-by-using-ews-in-exchange.md)
    
- [Extraer notificaciones para eventos de buzones de correo relacionados con la eliminación de EWS en Exchange](pull-notifications-for-ews-deletion-related-mailbox-events-in-exchange.md)
    
- [Eliminar citas y cancelar reuniones mediante EWS en Exchange](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)
    

