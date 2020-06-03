---
title: Operación CreateItem
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
ms.openlocfilehash: f6aaa9ed8e8257f19780492d6137fb015c1b6136
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458869"
---
# <a name="createitem-operation"></a>Operación CreateItem

La operación CreateItem crea elementos en el almacén de Exchange.
  
## <a name="using-the-createitem-operation"></a>Uso de la operación CreateItem

Puede usar la operación CreateItem para crear lo siguiente:
  
- Elementos de calendario
    
- Mensajes de correo electrónico.
    
- Convocatorias de reunión
    
- Tareas
    
- Contactos
    
Para obtener más información, vea [operación CreateItem (elemento de calendario)](createitem-operation-calendar-item.md), [operación CreateItem (mensaje de correo electrónico)](createitem-operation-email-message.md), [operación CreateItem (convocatoria de reunión)](createitem-operation-meeting-request.md), [operación CreateItem (tarea)](createitem-operation-task.md)y [operación CreateItem (contacto)](createitem-operation-contact.md).
  
La operación CreateItem admite el uso de objetos Response. Los objetos de respuesta admiten la aceptación y el rechazo de las reuniones y el tratamiento de los botones de voto incluidos en un mensaje de correo electrónico estándar. En la siguiente tabla se enumeran los objetos de respuesta que se controlan en la operación CreateItem.
  
|**Response (objeto)**|**Action**|
|:-----|:-----|
|AcceptItem  <br/> |Aceptar una convocatoria de reunión.  <br/> |
|CancelCalendarItem  <br/> |Cancelar una reunión. Esto difiere de la eliminación de todos los asistentes porque también elimina la reunión del organizador.  <br/> |
|DeclineItem  <br/> |Rechazar una convocatoria de reunión.  <br/> |
|ForwardItem  <br/> |Envíe una convocatoria de reunión a otra persona como convocatoria de reunión.  <br/> |
|RemoveItem  <br/> |Quitar una reunión cancelada del calendario.  <br/> |
|ReplyAllToItem  <br/> |Envíe un mensaje que incluya el cuerpo de la convocatoria de reunión original a todos los asistentes a la reunión.  <br/> |
|ReplyToItem  <br/> |Envíe un mensaje que incluya el cuerpo de la convocatoria de reunión original al remitente de la convocatoria de reunión.  <br/> |
|SendReadReceipt  <br/> |Enviar una confirmación de lectura al remitente de la convocatoria de reunión.  <br/> |
|TentativelyAcceptItem  <br/> |Acepta provisionalmente una convocatoria de reunión.  <br/> |
   
La operación CreateItem también admite objetos de reunión adicionales. En la tabla siguiente se enumeran los objetos adicionales que admite la operación CreateItem.
  
|**Objeto de reunión**|**Descripción**|
|:-----|:-----|
|Mensaje de reunión  <br/> |Representa un mensaje de reunión en el almacén de Exchange. Se trata del objeto base de los otros objetos de la reunión.  <br/> |
|Convocatoria de reunión  <br/> |Representa una convocatoria de reunión en el almacén de Exchange.  <br/> |
|Respuesta a la reunión  <br/> |Representa una respuesta a una reunión en el almacén de Exchange.  <br/> |
|Cancelación de reunión  <br/> |Representa una cancelación de reunión en el almacén de Exchange.  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación CreateItem (elemento de calendario)](createitem-operation-calendar-item.md)
  
[Operación CreateItem (contacto)](createitem-operation-contact.md)
  
[Operación CreateItem (mensaje de correo electrónico)](createitem-operation-email-message.md)
  
[Operación CreateItem (convocatoria de reunión)](createitem-operation-meeting-request.md)
  
[Operación CreateItem (tarea)](createitem-operation-task.md)
  
 **CreateItemType**

