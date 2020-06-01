---
title: GlobalIconIndex
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3d28ed70-4cfe-46e4-8d15-593c6e355bcf
description: El elemento GlobalIconIndex identifica el índice del icono global para todos los elementos de una conversación.
ms.openlocfilehash: 9900a80136a1a7eaae4634afd31568679f6dba1b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459464"
---
# <a name="globaliconindex"></a>GlobalIconIndex

El elemento **GlobalIconIndex** identifica el índice del icono global para todos los elementos de una conversación. 
  
```XML
<IconIndex>Default | PostItem | MailRead | MailUnread | MailReplied | MailForwarded | MailEncrypted | MailSmimeSigned | MailEncrytedReplied | MailSmimeSignedReplied | MailEncryptedForwarded | MailSmimeSignedForwarded | MailEncryptedRead | MailSmimeSignedRead | MailIrm | MaillrmForwarded | MaillrmReplied | SmsSubmitted | SmsRoutedToDeliveryPoint | SmsRoutedToExternalMessagingSystem | SmsDelivered | OutlookDefaultForContacts | AppointmentItem | AppointmentRecur | AppointmentMeet | AppointmentMeetRecur | AppointmentMeetNY | AppointmentMeetYes | AppointmentMeetNo | AppointmentMeetMaybe | AppointmentMeetCancel | AppointmentMeetInfo | TaskItem | TaskRecur | TaskOwned | TaskDelegated</IconIndex>
```

 **IconIndexType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

[Conversación (ConversationType)](conversation-conversationtype.md)  |  [Elemento](item.md)  |  [Contacto](contact.md)  |  [DistributionList](distributionlist.md)  |  [Mensaje de error](message-ex15websvcsotherref.md)  |  [CalendarItem](calendaritem.md)  |  [PostItem](postitem.md)  |  [Tarea](task.md)
  
## <a name="text-value"></a>Valor de texto

La siguiente tabla contiene los valores de texto posibles para el elemento **GlobalIconIndex** . 
  
|**Valor**|**Descripción**|
|:-----|:-----|
|||
|Predeterminado  <br/> |Especifica el icono predeterminado.  <br/> |
|PostItem  <br/> |Especifica el icono para un elemento post.  <br/> |
|MailRead  <br/> |Especifica el icono de lectura de correo.  <br/> |
|MailUnread  <br/> |Especifica el icono correo no leído.  <br/> |
|MailReplied  <br/> |Especifica el icono de respuesta a correo.  <br/> |
|MailForwarded  <br/> |Especifica el icono de correo reenviado.  <br/> |
|MailEncrypted  <br/> |Especifica el icono de correo cifrado.  <br/> |
|MailSmimeSigned  <br/> |Especifica el icono de correo firmado de extensiones seguras multipropósito de correo Internet (S/MIME).  <br/> |
|MailEncryptedReplied  <br/> |Especifica el icono cifrado respondido al correo.  <br/> |
|MailSmimeSignedReplied  <br/> |Especifica el icono de respuesta de S/MIME firmado para el correo.  <br/> |
|MailEncryptedForwarded  <br/> |Especifica el icono de correo reenviado cifrado.  <br/> |
|MailSmimeSignedForwarded  <br/> |Especifica el icono de correo reenviado con firma S/MIME.  <br/> |
|MailEncryptedRead  <br/> |Especifica el icono cifrado de lectura de correo.  <br/> |
|MailSmimeSignedRead  <br/> |Especifica el icono de lectura de correo firmado con S/MIME.  <br/> |
|MailIrm  <br/> |Especifica el icono de correo protegido por Information Rights Management (IRM).  <br/> |
|MailIrmForwarded  <br/> |Especifica el icono de correo reenviado protegido por IRM.  <br/> |
|MailIrmReplied  <br/> |Especifica el icono de respuesta con protección IRM en el correo.  <br/> |
|SmsSubmitted  <br/> |Especifica el icono para el enrutamiento de correo enviado para el servicio de mensajes cortos (SMS).  <br/> |
|SmsRoutedToDeliveryPoint  <br/> |Especifica el icono para el enrutamiento SMS a un punto de entrega externo.  <br/> |
|SmsRoutedToExternalMessagingSystem  <br/> |Especifica el icono para el enrutamiento SMS a un sistema de mensajería externo.  <br/> |
|SmsDelivered  <br/> |Especifica el icono de correo entregado por SMS.  <br/> |
|OutlookDefaultForContacts  <br/> |Especifica el icono predeterminado para contactos.  <br/> |
|AppointmentItem  <br/> |Especifica el icono del elemento de cita.  <br/> |
|AppointmentRecur  <br/> |Especifica el icono de cita periódica.  <br/> |
|AppointmentMeet  <br/> |Especifica el icono de la reunión.  <br/> |
|AppointmentMeetRecur  <br/> |Especifica el icono de reunión periódica.  <br/> |
|AppointmentMeetNY  <br/> |Especifica el icono para una respuesta tentativa de la reunión.  <br/> |
|AppointmentMeetYes  <br/> |Especifica el icono de aceptación de la reunión.  <br/> |
|AppointmentMeetNo  <br/> |Especifica el icono de la reunión rechazada.  <br/> |
|AppointmentMeetMaybe  <br/> |Especifica el icono de una respuesta posible a la reunión.  <br/> |
|AppointmentMeetCancel  <br/> |Especifica el icono de cancelación de la reunión.  <br/> |
|AppointmentMeetInfo  <br/> |Especifica el icono de información de la reunión.  <br/> |
|TaskItem  <br/> |Especifica el icono del elemento de tarea.  <br/> |
|TaskRecur  <br/> |Especifica el icono de tarea repetitiva.  <br/> |
|TaskOwned  <br/> |Especifica el icono de propiedad de la tarea.  <br/> |
|TaskDelegated  <br/> |Especifica el icono delegado de la tarea.  <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |false  <br/> |
   

