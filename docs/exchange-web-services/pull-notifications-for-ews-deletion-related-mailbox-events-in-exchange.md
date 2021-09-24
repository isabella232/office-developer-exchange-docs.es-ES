---
title: Extraer notificaciones para eventos de buzones de correo relacionados con la eliminación de EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 83511eea-e0b5-4ef0-83b1-0c5434e6d3ab
description: Descubra qué eventos de buzón se genera al eliminar elementos mediante EWS en Exchange.
ms.openlocfilehash: fa04d49f02cfec621f00a9b51b121cff22ca393b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510417"
---
# <a name="pull-notifications-for-ews-deletion-related-mailbox-events-in-exchange"></a>Extraer notificaciones para eventos de buzones de correo relacionados con la eliminación de EWS en Exchange

Descubra qué eventos de buzón se genera al eliminar elementos mediante EWS en Exchange.
  
Al eliminar [elementos y carpetas de un buzón](deleting-items-by-using-ews-in-exchange.md)de correo, se desencadena un evento de buzón. Las diferentes versiones de Exchange devuelven diferentes eventos de buzón de correo en respuesta a los cambios realizados en los elementos y carpetas de un buzón. En la tabla siguiente se identifican los eventos de buzón que se devuelven para eliminaciones cuando se usan notificaciones de extracción para suscribirse a eventos de buzón. 
  
**Tabla 1: Eventos de buzón relacionados con eliminación para notificaciones de extracción**

|**Tipo de eliminación y la operación EWS**|**Exchange de 2010 al especificar cada identificador de carpeta**|**Exchange de 2010 al especificar todas las carpetas**|**Exchange Online y Exchange de 2013 al especificar cada identificador de carpeta**|**Exchange Online y Exchange 2013 al especificar todas las carpetas**|
|:-----|:-----|:-----|:-----|:-----|
|Eliminación suave mediante la [operación DeleteItem](https://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) <br/> |DeletedEvent para el elemento.  <br/> ModifiedEvent para la carpeta principal del elemento.  <br/> |DeletedEvent para el elemento.  <br/> ModifiedEvent para la carpeta principal del elemento.  <br/> |MovedEvent para el elemento. Esto especifica los identificadores de carpetas primarias antiguas y nuevas. El elemento se mueve a la carpeta Eliminaciones del contenedor.  <br/> ModifiedEvent para la carpeta principal del elemento.  <br/> |DeletedEvent para el elemento.  <br/> DeletedEvent para el elemento de la carpeta de búsqueda predeterminada AllItems.  <br/> ModifiedEvent para la carpeta principal del elemento.  <br/> |
|Eliminación permanente mediante la [operación DeleteItem](https://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) <br/> |DeletedEvent para el elemento.  <br/> ModifiedEvent para la carpeta principal del elemento.  <br/> |DeletedEvent para el elemento.  <br/> ModifiedEvent para la carpeta principal del elemento.  <br/> |DeletedEvent para el elemento.  <br/> ModifiedEvent para la carpeta principal del elemento.  <br/> |DeletedEvent para el elemento.  <br/> DeletedEvent para el elemento de la carpeta de búsqueda predeterminada AllItems.  <br/> ModifiedEvent para la carpeta principal del elemento.  <br/> |
|Mover a la carpeta Elementos eliminados mediante la [operación DeleteItem](https://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) <br/> |MovedEvent para el elemento. Esto especifica identificadores de carpetas primarias antiguas y nuevas.  <br/> ModifiedEvent para la carpeta principal antigua del elemento.  <br/> ModifiedEvent para la nueva carpeta principal del elemento, que es la carpeta Elementos eliminados.  <br/> |MovedEvent para el elemento. Esto especifica identificadores de carpetas primarias antiguas y nuevas.  <br/> ModifiedEvent para la carpeta principal antigua del elemento.  <br/> ModifiedEvent para la nueva carpeta principal del elemento, que es la carpeta Elementos eliminados.  <br/> |MovedEvent para el elemento. Esto especifica identificadores de carpetas primarias antiguas y nuevas.  <br/> ModifiedEvent para la carpeta principal antigua del elemento.  <br/> ModifiedEvent para la nueva carpeta principal del elemento, que es la carpeta Elementos eliminados.  <br/> |DeletedEvent de la carpeta de búsqueda predeterminada AllItems.  <br/> CreatedEvent para el elemento de la carpeta AllItems.  <br/> ModifiedEvent para la carpeta principal original del elemento.  <br/> ModifiedEvent para la carpeta Elementos eliminados.  <br/> |
|Eliminación suave mediante la [operación DeleteFolder](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> |DeletedEvent para la carpeta.  <br/> ModifiedEvent para la carpeta principal de la carpeta.  <br/> |DeletedEvent para la carpeta.  <br/> ModifiedEvent para la carpeta principal de la carpeta.  <br/> |DeletedEvent para la carpeta.  <br/> ModifiedEvent para la carpeta principal de la carpeta.  <br/> |DeletedEvent para la carpeta.  <br/> ModifiedEvent para la carpeta principal de la carpeta.  <br/> |
|Eliminación permanente mediante la [operación DeleteFolder](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> |DeletedEvent para la carpeta.  <br/> ModifiedEvent para la carpeta principal de la carpeta.  <br/> |DeletedEvent para la carpeta.  <br/> ModifiedEvent para la carpeta principal de la carpeta.  <br/> |DeletedEvent para la carpeta.  <br/> ModifiedEvent para la carpeta principal de la carpeta.  <br/> |DeletedEvent para la carpeta.  <br/> ModifiedEvent para la carpeta principal de la carpeta.  <br/> |
|Mover a la carpeta Elementos eliminados mediante la [operación DeleteFolder](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> |MovedEvent para la carpeta. Esto especifica identificadores de carpetas primarias antiguas y nuevas.  <br/> ModifiedEvent para la carpeta principal antigua de la carpeta.  <br/> ModifiedEvent para la nueva carpeta principal de la carpeta, que es la carpeta Elementos eliminados.  <br/> |MovedEvent para la carpeta. Esto especifica identificadores de carpetas primarias antiguas y nuevas.  <br/> ModifiedEvent para la carpeta principal antigua de la carpeta.  <br/> ModifiedEvent para la nueva carpeta principal de la carpeta, que es la carpeta Elementos eliminados.  <br/> |MovedEvent para la carpeta. Esto especifica identificadores de carpetas primarias antiguas y nuevas.  <br/> ModifiedEvent para la carpeta principal antigua de la carpeta.  <br/> ModifiedEvent para la nueva carpeta principal de la carpeta, que es la carpeta Elementos eliminados.  <br/> |ModifiedEvent para la carpeta principal antigua de la carpeta.  <br/> ModifiedEvent para la nueva carpeta principal de la carpeta, que es la carpeta Elementos eliminados.  <br/> |
   
## <a name="see-also"></a>Ver también


- [Suscripciones de notificación, eventos de buzón, y EWS en Exchange](notification-subscriptions-mailbox-events-and-ews-in-exchange.md)
    
- [Eliminar elementos mediante EWS en Exchange](deleting-items-by-using-ews-in-exchange.md)
    
- [Controlar errores relacionados con la eliminación en EWS en Exchange](handling-deletion-related-errors-in-ews-in-exchange.md)
    

