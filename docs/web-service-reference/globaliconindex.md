---
title: GlobalIconIndex
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3d28ed70-4cfe-46e4-8d15-593c6e355bcf
description: El elemento GlobalIconIndex identifica el índice de icono global para todos los elementos de una conversación.
ms.openlocfilehash: e8d78bfcfc0e57df9230db86e080d1ee29878094
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19835727"
---
# <a name="globaliconindex"></a>GlobalIconIndex

El elemento **GlobalIconIndex** identifica el índice de icono global para todos los elementos de una conversación. 
  
```XML
<IconIndex>Default | PostItem | MailRead | MailUnread | MailReplied | MailForwarded | MailEncrypted | MailSmimeSigned | MailEncrytedReplied | MailSmimeSignedReplied | MailEncryptedForwarded | MailSmimeSignedForwarded | MailEncryptedRead | MailSmimeSignedRead | MailIrm | MaillrmForwarded | MaillrmReplied | SmsSubmitted | SmsRoutedToDeliveryPoint | SmsRoutedToExternalMessagingSystem | SmsDelivered | OutlookDefaultForContacts | AppointmentItem | AppointmentRecur | AppointmentMeet | AppointmentMeetRecur | AppointmentMeetNY | AppointmentMeetYes | AppointmentMeetNo | AppointmentMeetMaybe | AppointmentMeetCancel | AppointmentMeetInfo | TaskItem | TaskRecur | TaskOwned | TaskDelegated</IconIndex>
```

 **IconIndexType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[Conversación (ConversationType)](conversation-conversationtype.md) | [elemento](item.md) | [contacto](contact.md) | [DistributionList](distributionlist.md) | [mensaje](message-ex15websvcsotherref.md) | [CalendarItem](calendaritem.md) | [PostItem](postitem.md) | [tarea ](task.md)
  
## <a name="text-value"></a>Valor de texto

En la siguiente tabla contiene los posibles valores de texto para el elemento **GlobalIconIndex** . 
  
|**Valor**|**Descripción**|
|:-----|:-----|
|||
|Default  <br/> |Especifica el icono predeterminado.  <br/> |
|Objeto postItem  <br/> |Especifica el icono para un elemento para exponer.  <br/> |
|MailRead  <br/> |Especifica el que icono de leer el correo.  <br/> |
|MailUnread  <br/> |Especifica el icono de correo no leídos.  <br/> |
|MailReplied  <br/> |Especifica la respuesta al icono correo.  <br/> |
|MailForwarded  <br/> |Especifica el icono correo reenviado.  <br/> |
|MailEncrypted  <br/> |Especifica el icono de correo cifrado.  <br/> |
|MailSmimeSigned  <br/> |Especifica el icono de correo firmado de extensiones seguras multipropósito de correo Internet (S/MIME).  <br/> |
|MailEncryptedReplied  <br/> |Especifica que el cifrado respondió al icono correo.  <br/> |
|MailSmimeSignedReplied  <br/> |Especifica que la S/MIME firmados respondido al icono correo.  <br/> |
|MailEncryptedForwarded  <br/> |Especifica el icono de reenvío de correo cifrado.  <br/> |
|MailSmimeSignedForwarded  <br/> |Especifica la S/MIME firmado reenvía el icono de correo.  <br/> |
|MailEncryptedRead  <br/> |Especifica el icono de lectura de correo cifrado.  <br/> |
|MailSmimeSignedRead  <br/> |Especifica la S/MIME firmado leer el icono de correo.  <br/> |
|MailIrm  <br/> |Especifica el icono de correo protegido por Information Rights Management IRM.  <br/> |
|MailIrmForwarded  <br/> |Especifica el protegidos por IRM reenvía el icono de correo.  <br/> |
|MailIrmReplied  <br/> |Especifica que el protegidos por IRM respondió al icono correo.  <br/> |
|SmsSubmitted  <br/> |Especifica el icono de correo electrónico enviado para el enrutamiento de servicio de mensajes cortos (SMS).  <br/> |
|SmsRoutedToDeliveryPoint  <br/> |Especifica el icono para el enrutamiento de SMS en un punto de entrega externos.  <br/> |
|SmsRoutedToExternalMessagingSystem  <br/> |Especifica el icono para el enrutamiento de SMS a un sistema de mensajería externo.  <br/> |
|SmsDelivered  <br/> |Especifica el icono de correo entregado de SMS.  <br/> |
|OutlookDefaultForContacts  <br/> |Especifica el icono predeterminado para los contactos.  <br/> |
|Objeto AppointmentItem  <br/> |Especifica el icono del elemento de cita.  <br/> |
|AppointmentRecur  <br/> |Especifica el icono de una cita periódica.  <br/> |
|AppointmentMeet  <br/> |Especifica el icono de la reunión.  <br/> |
|AppointmentMeetRecur  <br/> |Especifica el icono de reunión periódica.  <br/> |
|AppointmentMeetNY  <br/> |Especifica el icono para una respuesta provisional a la reunión.  <br/> |
|AppointmentMeetYes  <br/> |Especifica la reunión icono de aceptación.  <br/> |
|AppointmentMeetNo  <br/> |Especifica el icono de reunión rechazada.  <br/> |
|AppointmentMeetMaybe  <br/> |Especifica el icono para una respuesta posible a la reunión.  <br/> |
|AppointmentMeetCancel  <br/> |Especifica el icono de cancelación de la reunión.  <br/> |
|AppointmentMeetInfo  <br/> |Especifica la reunión icono de información.  <br/> |
|Objeto TaskItem  <br/> |Especifica el icono del elemento de tarea.  <br/> |
|TaskRecur  <br/> |Especifica el icono de la tarea periódica.  <br/> |
|TaskOwned  <br/> |Especifica la tarea que son propiedad de icono.  <br/> |
|TaskDelegated  <br/> |Especifica el icono delegado de la tarea.  <br/> |
   
## <a name="remarks"></a>Notas

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |falso  <br/> |
   

