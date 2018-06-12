---
title: Tratamiento de errores relacionados con la eliminación de EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1bbe8507-7730-45e5-9232-c4f6fc39c2d9
description: Encuentre información acerca de cómo controlar los errores relacionados con la eliminación de las aplicaciones que desarrollar mediante el uso de la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: 0dc16c3350bb75fb1e91650f0a0f0b7423727eeb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763003"
---
# <a name="handling-deletion-related-errors-in-ews-in-exchange"></a>Tratamiento de errores relacionados con la eliminación de EWS en Exchange

Encuentre información acerca de cómo controlar los errores relacionados con la eliminación de las aplicaciones que desarrollar mediante el uso de la API administrada de EWS o EWS en Exchange.
  
Si su aplicación [elimina los elementos y carpetas](deleting-items-by-using-ews-in-exchange.md), es posible que deba controlar errores relacionados con la eliminación. Puede controlar estos errores en tiempo de ejecución, o mientras está desarrollando su aplicación de EWS.
  
**Tabla 1: Errores relacionados con la eliminación y cómo controlarlos**

|**Error**|**Se produce al intentar...**|**Controlarla por...**|
|:-----|:-----|:-----|
|ErrorAffectedTaskOccurrencesRequired  <br/> |Eliminar una instancia de una tarea periódica y no se establece la propiedad **AffectedTaskOccurrence** .  <br/> |Al establecer la propiedad **AffectedTaskOccurrence** y volver a intentar la eliminación.  <br/> |
|ErrorCalendarCannotUpdateDeletedItem  <br/> |Actualizar un elemento de calendario que se encuentra en la carpeta Elementos eliminados cuando diese como resultado la actualización en el envío de una invitación a la reunión a los asistentes.  <br/> |Cancelación de la actualización o se desplaza el elemento de calendario a la carpeta Calendario predeterminada y actualizar el elemento de calendario.  <br/> |
|ErrorCalendarOccurrenceIsDeletedFromRecurrence  <br/> |Hacer referencia a una repetición eliminada de una cita periódica.  <br/> |Eliminación de una referencia a una repetición eliminada.  <br/> |
|ErrorCannotDeleteObject  <br/> |Eliminar un elemento que no se puede eliminar.  <br/> |Salir de intentos para eliminar el elemento.  <br/> |
|ErrorCannotDeleteTaskOccurrence  <br/> |Eliminar una ocurrencia de una tarea no periódica o eliminar la última aparición de una tarea periódica.  <br/> |Eliminación de una tarea no periódica o saliendo intenta eliminar la última aparición de una tarea periódica.  <br/> |
|ErrorDeleteDistinguishedFolder  <br/> |Eliminar una carpeta distintivo.  <br/> |Que indica que no se pueden eliminar las carpetas predeterminadas.  <br/> |
|ErrorItemNotFound  <br/> |Obtener acceso a un elemento eliminado de forma permanente.  <br/> |Quitar referencias a un elemento cuando se elimina de la tienda. Si se recupera un elemento, asegúrese de que restablecer las referencias necesarias al cliente.  <br/> |
|ErrorSendMeetingCancellationsRequired  <br/> |Eliminar un elemento de calendario sin especificar si se deben enviar cancelaciones de reunión.  <br/> |Especifica que cancelaciones de reunión deben o no se deben enviar.  <br/> |
   
## <a name="see-also"></a>Ver también


- [Eliminación de elementos con EWS en Exchange](deleting-items-by-using-ews-in-exchange.md)
    
- [Extraer las notificaciones de eventos de buzón de correo relacionados con la eliminación de EWS en Exchange](pull-notifications-for-ews-deletion-related-mailbox-events-in-exchange.md)
    
- [Eliminar las citas y cancelar reuniones mediante el uso de EWS en Exchange](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)
    

