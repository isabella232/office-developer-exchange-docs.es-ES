---
title: Notificaciones de extracción para eventos de buzón relacionados con la eliminación de EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 83511eea-e0b5-4ef0-83b1-0c5434e6d3ab
description: Descubra los eventos de buzón de correo que se generan cuando se eliminan elementos mediante EWS en Exchange.
ms.openlocfilehash: c3d98ff798e3d0f6d214111d51da2c81278fd17d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457658"
---
# <a name="pull-notifications-for-ews-deletion-related-mailbox-events-in-exchange"></a>Notificaciones de extracción para eventos de buzón relacionados con la eliminación de EWS en Exchange

Descubra los eventos de buzón de correo que se generan cuando se eliminan elementos mediante EWS en Exchange.
  
Cuando se [eliminan elementos y carpetas de un buzón](deleting-items-by-using-ews-in-exchange.md), se desencadena un evento de buzón. Las diferentes versiones de Exchange devuelven diferentes eventos de buzón de correo en respuesta a los cambios en los elementos y las carpetas de un buzón. En la siguiente tabla se identifican los eventos de buzón de correo que se devuelven para las eliminaciones cuando se usan notificaciones de extracción para suscribirse a eventos de buzón. 
  
**Tabla 1: eventos de buzón relacionados con la eliminación para notificaciones de extracción**

|**Tipo de eliminación y operación de EWS**|**Notificación de Exchange 2010 cuando especifica un identificador de carpeta**|**Notificación de Exchange 2010 cuando especifica todas las carpetas**|**Notificación de Exchange Online y Exchange 2013 cuando especifica un identificador de carpeta**|**Exchange Online y Exchange 2013 cuando se especifican todas las carpetas**|
|:-----|:-----|:-----|:-----|:-----|
|Eliminación temporal mediante la [operación DeleteItem](https://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) <br/> |DeletedEvent para el elemento.  <br/> ModifiedEvent para la carpeta principal del elemento.  <br/> |DeletedEvent para el elemento.  <br/> ModifiedEvent para la carpeta principal del elemento.  <br/> |MovedEvent para el elemento. Esto especifica los identificadores de carpeta principal y los nuevos que hay en el antiguo. El elemento se mueve a la carpeta eliminaciones del contenedor.  <br/> ModifiedEvent para la carpeta principal del elemento.  <br/> |DeletedEvent para el elemento.  <br/> DeletedEvent para el elemento de la carpeta de búsqueda AllItems predeterminada.  <br/> ModifiedEvent para la carpeta principal del elemento.  <br/> |
|Eliminación de disco duro mediante la [operación DeleteItem](https://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) <br/> |DeletedEvent para el elemento.  <br/> ModifiedEvent para la carpeta principal del elemento.  <br/> |DeletedEvent para el elemento.  <br/> ModifiedEvent para la carpeta principal del elemento.  <br/> |DeletedEvent para el elemento.  <br/> ModifiedEvent para la carpeta principal del elemento.  <br/> |DeletedEvent para el elemento.  <br/> DeletedEvent para el elemento de la carpeta de búsqueda AllItems predeterminada.  <br/> ModifiedEvent para la carpeta principal del elemento.  <br/> |
|Mover a la carpeta elementos eliminados mediante la [operación DeleteItem](https://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) <br/> |MovedEvent para el elemento. Esto especifica los identificadores de carpeta principal antiguos y nuevos.  <br/> ModifiedEvent de la antigua carpeta principal del elemento.  <br/> ModifiedEvent de la nueva carpeta principal del elemento, que es la carpeta elementos eliminados.  <br/> |MovedEvent para el elemento. Esto especifica los identificadores de carpeta principal antiguos y nuevos.  <br/> ModifiedEvent de la antigua carpeta principal del elemento.  <br/> ModifiedEvent de la nueva carpeta principal del elemento, que es la carpeta elementos eliminados.  <br/> |MovedEvent para el elemento. Esto especifica los identificadores de carpeta principal antiguos y nuevos.  <br/> ModifiedEvent de la antigua carpeta principal del elemento.  <br/> ModifiedEvent de la nueva carpeta principal del elemento, que es la carpeta elementos eliminados.  <br/> |DeletedEvent de la carpeta de búsqueda AllItems predeterminada.  <br/> CreatedEvent para el elemento de la carpeta AllItems.  <br/> ModifiedEvent de la carpeta principal original del elemento.  <br/> ModifiedEvent para la carpeta elementos eliminados.  <br/> |
|Eliminación temporal mediante la [operación DeleteFolder](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> |DeletedEvent para la carpeta.  <br/> ModifiedEvent para la carpeta principal de la carpeta.  <br/> |DeletedEvent para la carpeta.  <br/> ModifiedEvent para la carpeta principal de la carpeta.  <br/> |DeletedEvent para la carpeta.  <br/> ModifiedEvent para la carpeta principal de la carpeta.  <br/> |DeletedEvent para la carpeta.  <br/> ModifiedEvent para la carpeta principal de la carpeta.  <br/> |
|Eliminación de disco duro mediante la [operación DeleteFolder](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> |DeletedEvent para la carpeta.  <br/> ModifiedEvent para la carpeta principal de la carpeta.  <br/> |DeletedEvent para la carpeta.  <br/> ModifiedEvent para la carpeta principal de la carpeta.  <br/> |DeletedEvent para la carpeta.  <br/> ModifiedEvent para la carpeta principal de la carpeta.  <br/> |DeletedEvent para la carpeta.  <br/> ModifiedEvent para la carpeta principal de la carpeta.  <br/> |
|Vaya a la carpeta elementos eliminados mediante la [operación DeleteFolder](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> |MovedEvent para la carpeta. Esto especifica los identificadores de carpeta principal antiguos y nuevos.  <br/> ModifiedEvent para la carpeta primaria antigua de la carpeta.  <br/> ModifiedEvent para la nueva carpeta principal de la carpeta, que es la carpeta elementos eliminados.  <br/> |MovedEvent para la carpeta. Esto especifica los identificadores de carpeta principal antiguos y nuevos.  <br/> ModifiedEvent para la carpeta primaria antigua de la carpeta.  <br/> ModifiedEvent para la nueva carpeta principal de la carpeta, que es la carpeta elementos eliminados.  <br/> |MovedEvent para la carpeta. Esto especifica los identificadores de carpeta principal antiguos y nuevos.  <br/> ModifiedEvent para la carpeta primaria antigua de la carpeta.  <br/> ModifiedEvent para la nueva carpeta principal de la carpeta, que es la carpeta elementos eliminados.  <br/> |ModifiedEvent para la carpeta primaria antigua de la carpeta.  <br/> ModifiedEvent para la nueva carpeta principal de la carpeta que es la carpeta elementos eliminados.  <br/> |
   
## <a name="see-also"></a>Vea también


- [Suscripciones de notificación, eventos de buzón y EWS en Exchange](notification-subscriptions-mailbox-events-and-ews-in-exchange.md)
    
- [Eliminación de elementos mediante EWS en Exchange](deleting-items-by-using-ews-in-exchange.md)
    
- [Administración de errores relacionados con la eliminación en EWS en Exchange](handling-deletion-related-errors-in-ews-in-exchange.md)
    

