---
title: IconIndex
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 92020822-2a86-4dfc-aee1-3067af4d4edf
description: El elemento IconIndex identifica el índice de icono de un elemento o conversación.
ms.openlocfilehash: f0c024eeedcbda9aa5ad8afdea09a68f2499798e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59541164"
---
# <a name="iconindex"></a>IconIndex

El **elemento IconIndex** identifica el índice de icono de un elemento o conversación. 
  
```XML
<IconIndex>Default | PostItem | MailRead | MailUnread | MailReplied | MailForwarded | MailEncrypted | MailSmimeSigned | MailEncrytedReplied | MailSmimeSignedReplied | MailEncryptedForwarded | MailSmimeSignedForwarded | MailEncryptedRead | MailSmimeSignedRead | MailIrm | MailIrmForwarded | MailIrmReplied | SmsSubmitted | SmsRoutedToDeliveryPoint | SmsRoutedToExternalMessagingSystem | SmsDelivered | OutlookDefaultForContacts | AppointmentItem | AppointmentRecur | AppointmentMeet | AppointmentMeetRecur | AppointmentMeetNY | AppointmentMeetYes | AppointmentMeetNo | AppointmentMeetMaybe | AppointmentMeetCancel | AppointmentMeetInfo | TaskItem | TaskRecur | TaskOwned | TaskDelegated</IconIndex>
```

 **IconIndexType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[Conversación (ConversationType)](conversation-conversationtype.md)  |  [Elemento](item.md)  |  [Contacto](contact.md)  |  [DistributionList](distributionlist.md)  |  [Mensaje](message-ex15websvcsotherref.md)  |  [CalendarItem](calendaritem.md)  |  [PostItem](postitem.md)  |  [Tarea](task.md)
  
## <a name="text-value"></a>Valor de texto

La tabla siguiente contiene los valores de texto posibles para el **elemento IconIndex.** 
  
|**Valor**|**Descripción**|
|:-----|:-----|
|||
|Predeterminado  <br/> |Especifica el icono predeterminado.  <br/> |
|PostItem  <br/> |Especifica el icono de un elemento de publicación.  <br/> |
|MailRead  <br/> |Especifica el icono de lectura de correo.  <br/> |
|MailUnread  <br/> |Especifica el icono de correo no leído.  <br/> |
|MailReplied  <br/> |Especifica el icono de correo contestado.  <br/> |
|MailForwarded  <br/> |Especifica el icono de correo reenviado.  <br/> |
|MailEncrypted  <br/> |Especifica el icono de correo cifrado.  <br/> |
|MailSmimeSigned  <br/> |Especifica el icono de correo firmado Extensiones seguras/multipropósito de correo de Internet (S/MIME).  <br/> |
|MailEncryptedReplied  <br/> |Especifica el icono de correo cifrado contestado.  <br/> |
|MailSmimeSignedReplied  <br/> |Especifica el icono de correo con firma S/MIME.  <br/> |
|MailEncryptedForwarded  <br/> |Especifica el icono de correo reenviado cifrado.  <br/> |
|MailSmimeSignedForwarded  <br/> |Especifica el icono de correo reenviado firmado por S/MIME.  <br/> |
|MailEncryptedRead  <br/> |Especifica el icono de correo de lectura cifrado.  <br/> |
|MailSmimeSignedRead  <br/> |Especifica el icono de correo de lectura firmado por S/MIME.  <br/> |
|MailIrm  <br/> |Especifica el icono de correo protegido por Information Rights Management (IRM).  <br/> |
|MailIrmForwarded  <br/> |Especifica el icono de correo reenviado protegido por IRM.  <br/> |
|MailIrmReplied  <br/> |Especifica el icono de correo protegido por IRM.  <br/> |
|SmsSubmitted  <br/> |Especifica el correo de icono enviado para el enrutamiento del servicio de mensajes cortos (SMS).  <br/> |
|SmsRoutedToDeliveryPoint  <br/> |Especifica el icono para el enrutamiento de SMS a un punto de entrega externo.  <br/> |
|SmsRoutedToExternalMessagingSystem  <br/> |Especifica el icono para el enrutamiento de SMS a un sistema de mensajería externo.  <br/> |
|SmsDelivered  <br/> |Especifica el icono de correo entregado por SMS.  <br/> |
|OutlookDefaultForContacts  <br/> |Especifica el icono predeterminado para los contactos.  <br/> |
|AppointmentItem  <br/> |Especifica el icono del elemento de cita.  <br/> |
|AppointmentRecur  <br/> |Especifica el icono de cita periódica.  <br/> |
|AppointmentMeet  <br/> |Especifica el icono de reunión.  <br/> |
|AppointmentMeetRecur  <br/> |Especifica el icono de reunión periódica.  <br/> |
|AppointmentMeetNY  <br/> |Especifica el icono de una respuesta provisional a la reunión.  <br/> |
|AppointmentMeetYes  <br/> |Especifica el icono de aceptación de la reunión.  <br/> |
|AppointmentMeetNo  <br/> |Especifica el icono rechazado de la reunión.  <br/> |
|AppointmentMeetMaybe  <br/> |Especifica el icono para una posible respuesta a la reunión.  <br/> |
|AppointmentMeetCancel  <br/> |Especifica el icono de cancelación de reunión.  <br/> |
|AppointmentMeetInfo  <br/> |Especifica el icono de información de la reunión.  <br/> |
|TaskItem  <br/> |Especifica el icono del elemento de tarea.  <br/> |
|TaskRecur  <br/> |Especifica el icono de tarea periódica.  <br/> |
|TaskOwned  <br/> |Especifica el icono propiedad de la tarea.  <br/> |
|TaskDelegated  <br/> |Especifica el icono delegado de la tarea.  <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre del esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |false  <br/> |
   

