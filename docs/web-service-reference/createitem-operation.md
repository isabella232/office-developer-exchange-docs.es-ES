---
title: Operación CreateItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- CreateItem
api_type:
- schema
ms.assetid: 78a52120-f1d0-4ed7-8748-436e554f75b6
description: La operación CreateItem crea elementos en el Exchange almacén.
ms.openlocfilehash: 2aee80d883aa623b8074ecc523d1a45fa71962da
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59538404"
---
# <a name="createitem-operation"></a>Operación CreateItem

La operación CreateItem crea elementos en el Exchange almacén.
  
## <a name="using-the-createitem-operation"></a>Uso de la operación CreateItem

Puede usar la operación CreateItem para crear lo siguiente:
  
- Elementos de calendario
    
- Mensajes de correo electrónico.
    
- Convocatorias de reunión
    
- Tareas
    
- Contactos
    
Para obtener más información, vea [CreateItem operation (calendar item),](createitem-operation-calendar-item.md) [CreateItem operation (email message),](createitem-operation-email-message.md) [CreateItem operation (meeting request),](createitem-operation-meeting-request.md) [CreateItem operation (task)](createitem-operation-task.md)y [CreateItem operation (contact).](createitem-operation-contact.md)
  
La operación CreateItem admite el uso de objetos de respuesta. Los objetos de respuesta admiten la aceptación y el rechazo de las reuniones y el control de los botones de votación que se incluyen en un mensaje de correo electrónico estándar. En la tabla siguiente se enumeran los objetos de respuesta que se controlan en la operación CreateItem.
  
|**Response (objeto)**|**Action**|
|:-----|:-----|
|AcceptItem  <br/> |Aceptar una solicitud de reunión.  <br/> |
|CancelCalendarItem  <br/> |Cancelar una reunión. Esto difiere de eliminar todos los asistentes porque elimina la reunión para el organizador también.  <br/> |
|DeclineItem  <br/> |Rechazar una solicitud de reunión.  <br/> |
|ForwardItem  <br/> |Enviar una solicitud de reunión a otra persona como una solicitud de reunión.  <br/> |
|RemoveItem  <br/> |Quite una reunión cancelada del calendario.  <br/> |
|ReplyAllToItem  <br/> |Envíe un mensaje que incluya el cuerpo de la solicitud de reunión original a todos los asistentes a la reunión.  <br/> |
|ReplyToItem  <br/> |Envíe un mensaje que incluya el cuerpo de la solicitud de reunión original al remitente de la solicitud de reunión.  <br/> |
|SendReadReceipt  <br/> |Enviar un recibo de lectura al remitente de la solicitud de reunión.  <br/> |
|TentativelyAcceptItem  <br/> |Acepte provisionalmente una solicitud de reunión.  <br/> |
   
La operación CreateItem también admite objetos de reunión adicionales. En la tabla siguiente se enumeran los objetos adicionales que admite la operación CreateItem.
  
|**Objeto Meeting**|**Descripción**|
|:-----|:-----|
|Mensaje de reunión  <br/> |Representa un mensaje de reunión en el Exchange almacén. Este es el objeto base de los otros objetos de reunión.  <br/> |
|Convocatoria de reunión  <br/> |Representa una solicitud de reunión en Exchange almacén.  <br/> |
|Respuesta a la reunión  <br/> |Representa una respuesta de reunión en Exchange almacén.  <br/> |
|Cancelación de reunión  <br/> |Representa una cancelación de reunión en el Exchange local.  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación CreateItem (elemento de calendario)](createitem-operation-calendar-item.md)
  
[Operación CreateItem (contacto)](createitem-operation-contact.md)
  
[Operación CreateItem (mensaje de correo electrónico)](createitem-operation-email-message.md)
  
[Operación CreateItem (convocatoria de reunión)](createitem-operation-meeting-request.md)
  
[Operación CreateItem (tarea)](createitem-operation-task.md)
  
 **CreateItemType**

