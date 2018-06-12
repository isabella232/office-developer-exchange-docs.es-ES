---
title: CreateItem Operation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateItem
api_type:
- schema
ms.assetid: 78a52120-f1d0-4ed7-8748-436e554f75b6
description: La operación CreateItem crea elementos en el almacén de Exchange.
ms.openlocfilehash: 7e1808c685cdbaa1e8867aa7425b2cc52218d001
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763955"
---
# <a name="createitem-operation"></a>CreateItem Operation

La operación CreateItem crea elementos en el almacén de Exchange.
  
## <a name="using-the-createitem-operation"></a>Mediante la operación CreateItem

Puede usar la operación CreateItem para crear lo siguiente:
  
- Elementos de calendario
    
- Mensajes de correo electrónico.
    
- Convocatoria de reunión
    
- Tareas
    
- Contacts
    
Para obtener más información, vea [operación CreateItem (elemento de calendario)](createitem-operation-calendar-item.md), [operación CreateItem (mensaje de correo electrónico)](createitem-operation-email-message.md), [operación CreateItem (convocatoria de reunión)](createitem-operation-meeting-request.md), [operación CreateItem (tarea)](createitem-operation-task.md)y [operación CreateItem (contacto) ](createitem-operation-contact.md).
  
La operación CreateItem admite el uso de objetos de respuesta. Objetos de respuesta admiten la aceptación y rechazo de las reuniones y el control de botones de voto que se incluyen en un mensaje de correo electrónico estándar. En la siguiente tabla se enumera los objetos de respuesta que se administran en la operación CreateItem.
  
|**Objeto de respuesta**|**Acción**|
|:-----|:-----|
|AcceptItem  <br/> |Aceptar una convocatoria de reunión.  <br/> |
|CancelCalendarItem  <br/> |Cancelar una reunión. Esto difiere de la eliminación de todos los asistentes debido a que elimina la reunión para el Organizador también.  <br/> |
|DeclineItem  <br/> |Rechazar una convocatoria de reunión.  <br/> |
|ForwardItem  <br/> |Enviar una convocatoria de reunión a otra persona como una convocatoria de reunión.  <br/> |
|RemoveItem  <br/> |Quitar una reunión cancelada del calendario.  <br/> |
|ReplyAllToItem  <br/> |Enviar un mensaje que incluye el cuerpo de la convocatoria de reunión original a todos los asistentes a la reunión.  <br/> |
|ReplyToItem  <br/> |Enviar un mensaje que incluye el cuerpo de la convocatoria de reunión original al remitente de la convocatoria de reunión.  <br/> |
|SendReadReceipt  <br/> |Enviar una confirmación de lectura para el remitente de la convocatoria de reunión.  <br/> |
|TentativelyAcceptItem  <br/> |Aceptar provisionalmente una convocatoria de reunión.  <br/> |
   
La operación CreateItem también es compatible con objetos adicionales de la reunión. En la siguiente tabla se enumera los objetos adicionales que admite la operación CreateItem.
  
|**Objeto de la reunión**|**Descripción**|
|:-----|:-----|
|Mensaje de la reunión  <br/> |Representa un mensaje de reunión en el almacén de Exchange. Éste es el objeto base para los demás objetos de la reunión.  <br/> |
|Convocatoria de reunión  <br/> |Representa una convocatoria de reunión en el almacén de Exchange.  <br/> |
|Respuesta a la reunión  <br/> |Representa una respuesta a la reunión en el almacén de Exchange.  <br/> |
|Cancelación de reunión  <br/> |Representa la cancelación de la reunión en el almacén de Exchange.  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación CreateItem (elemento de calendario)](createitem-operation-calendar-item.md)
  
[Operación CreateItem (contacto)](createitem-operation-contact.md)
  
[Operación CreateItem (mensaje de correo electrónico)](createitem-operation-email-message.md)
  
[Operación CreateItem (convocatoria de reunión)](createitem-operation-meeting-request.md)
  
[Operación CreateItem (tarea)](createitem-operation-task.md)
  
 **CreateItemType**

