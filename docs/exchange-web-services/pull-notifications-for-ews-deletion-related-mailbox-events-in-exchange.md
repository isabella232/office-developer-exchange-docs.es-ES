---
title: Extraer las notificaciones de eventos de buzón de correo relacionados con la eliminación de EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 83511eea-e0b5-4ef0-83b1-0c5434e6d3ab
description: Descubra qué eventos de buzón de correo se ha generado al eliminar elementos mediante el uso de EWS en Exchange.
ms.openlocfilehash: b12d6a16cc539f36b6b4dcd7274529e9def3c247
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763296"
---
# <a name="pull-notifications-for-ews-deletion-related-mailbox-events-in-exchange"></a>Extraer las notificaciones de eventos de buzón de correo relacionados con la eliminación de EWS en Exchange

Descubra qué eventos de buzón de correo se ha generado al eliminar elementos mediante el uso de EWS en Exchange.
  
Cuando la [eliminación de elementos y carpetas de un buzón de correo](deleting-items-by-using-ews-in-exchange.md), desencadena un evento de buzón de correo. Las diferentes versiones de Exchange devuelvan eventos de buzón de correo diferentes en respuesta a cambios a elementos y carpetas en un buzón de correo. En la siguiente tabla identifica los eventos de buzón de correo que se devuelven para eliminaciones al usar notificaciones de extracción para suscribirse a eventos de buzón de correo. 
  
**La tabla 1: Eventos de buzón de correo relacionados con la eliminación para las notificaciones de extracción**

|**Tipo de la operación de EWS y eliminación**|**Notificación de Exchange 2010 cuando especifique cada identificador de carpeta**|**Notificación de Exchange 2010 cuando especifique todas las carpetas**|**Exchange Online y Exchange 2013 notificación cuando especifique cada identificador de carpeta**|**Cuando especifique todas las carpetas de Exchange Online y Exchange 2013**|
|:-----|:-----|:-----|:-----|:-----|
|Eliminar suave a través de la [operación DeleteItem](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) <br/> |DeletedEvent para el elemento.  <br/> ModifiedEvent para la carpeta del elemento primario.  <br/> |DeletedEvent para el elemento.  <br/> ModifiedEvent para la carpeta del elemento primario.  <br/> |MovedEvent para el elemento. Especifica los identificadores de carpeta de principales antiguos y nuevos. El elemento se mueve a la carpeta de eliminaciones en el volcado de archivos.  <br/> ModifiedEvent para la carpeta del elemento primario.  <br/> |DeletedEvent para el elemento.  <br/> DeletedEvent para el elemento de la carpeta de búsqueda AllItems tal y predeterminada.  <br/> ModifiedEvent para la carpeta del elemento primario.  <br/> |
|Disco duro eliminar a través de la [operación DeleteItem](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) <br/> |DeletedEvent para el elemento.  <br/> ModifiedEvent para la carpeta del elemento primario.  <br/> |DeletedEvent para el elemento.  <br/> ModifiedEvent para la carpeta del elemento primario.  <br/> |DeletedEvent para el elemento.  <br/> ModifiedEvent para la carpeta del elemento primario.  <br/> |DeletedEvent para el elemento.  <br/> DeletedEvent para el elemento de la carpeta de búsqueda AllItems tal y predeterminada.  <br/> ModifiedEvent para la carpeta del elemento primario.  <br/> |
|Mover a la carpeta Elementos eliminados a través de la [operación DeleteItem](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) <br/> |MovedEvent para el elemento. Esto especifica ambos identificadores de primario anterior y la nueva carpeta.  <br/> ModifiedEvent para la carpeta del elemento anterior primario.  <br/> ModifiedEvent para la carpeta del elemento nuevo primario, que es la carpeta Elementos eliminados.  <br/> |MovedEvent para el elemento. Esto especifica ambos identificadores de primario anterior y la nueva carpeta.  <br/> ModifiedEvent para la carpeta del elemento anterior primario.  <br/> ModifiedEvent para la carpeta del elemento nuevo primario, que es la carpeta Elementos eliminados.  <br/> |MovedEvent para el elemento. Esto especifica ambos identificadores de primario anterior y la nueva carpeta.  <br/> ModifiedEvent para la carpeta del elemento anterior primario.  <br/> ModifiedEvent para la carpeta del elemento nuevo primario, que es la carpeta Elementos eliminados.  <br/> |DeletedEvent desde la carpeta de búsqueda predeterminada AllItems tal y.  <br/> CreatedEvent para el elemento en la carpeta AllItems tal y.  <br/> ModifiedEvent para la carpeta del elemento original primario.  <br/> ModifiedEvent para la carpeta Elementos eliminados.  <br/> |
|Eliminar suave a través de la [operación DeleteFolder](http://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> |DeletedEvent para la carpeta.  <br/> ModifiedEvent para la carpeta principal.  <br/> |DeletedEvent para la carpeta.  <br/> ModifiedEvent para la carpeta principal.  <br/> |DeletedEvent para la carpeta.  <br/> ModifiedEvent para la carpeta principal.  <br/> |DeletedEvent para la carpeta.  <br/> ModifiedEvent para la carpeta principal.  <br/> |
|Disco duro eliminar a través de la [operación DeleteFolder](http://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> |DeletedEvent para la carpeta.  <br/> ModifiedEvent para la carpeta principal.  <br/> |DeletedEvent para la carpeta.  <br/> ModifiedEvent para la carpeta principal.  <br/> |DeletedEvent para la carpeta.  <br/> ModifiedEvent para la carpeta principal.  <br/> |DeletedEvent para la carpeta.  <br/> ModifiedEvent para la carpeta principal.  <br/> |
|Mover a la carpeta Elementos eliminados a través de la [operación DeleteFolder](http://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> |MovedEvent para la carpeta. Esto especifica ambos identificadores de primario anterior y la nueva carpeta.  <br/> ModifiedEvent para la antigua carpeta principal.  <br/> ModifiedEvent para la nueva carpeta principal, que es la carpeta Elementos eliminados.  <br/> |MovedEvent para la carpeta. Esto especifica ambos identificadores de primario anterior y la nueva carpeta.  <br/> ModifiedEvent para la antigua carpeta principal.  <br/> ModifiedEvent para la nueva carpeta principal, que es la carpeta Elementos eliminados.  <br/> |MovedEvent para la carpeta. Esto especifica ambos identificadores de primario anterior y la nueva carpeta.  <br/> ModifiedEvent para la antigua carpeta principal.  <br/> ModifiedEvent para la nueva carpeta principal, que es la carpeta Elementos eliminados.  <br/> |ModifiedEvent para la antigua carpeta principal.  <br/> ModifiedEvent para la nueva carpeta principal que es la carpeta Elementos eliminados.  <br/> |
   
## <a name="see-also"></a>Ver también


- [Suscripciones de notificación de eventos de buzón de correo y EWS en Exchange](notification-subscriptions-mailbox-events-and-ews-in-exchange.md)
    
- [Eliminación de elementos con EWS en Exchange](deleting-items-by-using-ews-in-exchange.md)
    
- [Tratamiento de errores relacionados con la eliminación de EWS en Exchange](handling-deletion-related-errors-in-ews-in-exchange.md)
    

