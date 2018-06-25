---
title: Conjuntos de propiedades y respuesta de formas de EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 04a29804-6067-48e7-9f5c-534e253a230e
description: Obtenga información sobre cómo administrar las formas de respuesta y conjuntos de propiedades que son devueltos por la dirección URL de EWS administran EWS y la API de Exchange.
ms.openlocfilehash: d9fd6c155438dfd03cfc9536397316cf3faa2287
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763315"
---
# <a name="property-sets-and-response-shapes-in-ews-in-exchange"></a>Conjuntos de propiedades y respuesta de formas de EWS en Exchange

Obtenga información sobre cómo administrar las formas de respuesta y conjuntos de propiedades que son devueltos por la dirección URL de EWS administran EWS y la API de Exchange.
  
El almacén de datos de Exchange proporciona una solución de almacenamiento flexible que permite almacenar elementos diferentes, como los contactos y las entradas de calendario, en la misma carpeta; Sin embargo, puede realizar difícil de administrar los datos que se devuelven desde una llamada a una operación de EWS o un método de la API administrada.
  
Para facilitar la administración de los datos que se devuelven por Exchange Online, Exchange Online como parte de Office 365, o la versión de Excahange iniciar con Exchange 2013, la API administrada de EWS utiliza conjuntos de propiedades, y EWS utiliza las formas de la respuesta. Estos son colecciones predefinidas que proporcionan las propiedades más comunes de un elemento del almacén. El conjunto de propiedades que se devuelve se determina por el tipo de elemento. Esto significa que, cuando se enlaza un elemento mediante el método de la API administrada de Exchange [Item.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) , obtendrá un conjunto diferente de propiedades según el tipo de elemento a la que enlazar. Enlace a un elemento de calendario devolverá un conjunto diferente de propiedades que el enlace a un elemento de contacto. Del mismo modo, si usa EWS, la [operación GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) devuelve un conjunto diferente de propiedades según el tipo de elemento que se devuelve. 
  
Enlace a una carpeta con el método [Folder.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) o mediante la [operación GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) devuelve también distintos conjuntos de propiedades basándose en la carpeta que solicita. 
  
**La tabla 1. Formas de respuesta predefinidos**

|**Forma de respuesta**|**Equivalente de la API administrada de EWS**|**Descripción**|
|:-----|:-----|:-----|
|Sólo identificador  <br/> |[BasePropertySet.IdOnly](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.basepropertyset%28v=exchg.80%29.aspx) <br/> |Devuelve solo el identificador del elemento o la carpeta. Mayoría de las aplicaciones debe usar esta forma de respuesta y especificar las propiedades adicionales que son necesarias.  <br/> |
|Default  <br/> |N/D  <br/> |Devuelve un conjunto predefinido de propiedades que son el valor predeterminado para el elemento o la carpeta (sólo EWS).  <br/> |
|Todas las propiedades  <br/> |[BasePropertySet.FirstClassProperties](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.basepropertyset%28v=exchg.80%29.aspx) <br/> |Devuelve las propiedades que las aplicaciones cliente se usan con más frecuencia. Puede devolver propiedades adicionales mediante el uso de una ruta de acceso de propiedad.  <br/> |
   
## <a name="default-response-shapes"></a>Formas de respuesta predeterminada

EWS incluye un conjunto de formas de respuesta predeterminada para las carpetas y elementos. 
  
En la siguiente tabla se enumera las propiedades predeterminadas que se devuelven para cada carpeta por las operaciones [FindFolder](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) y [GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) EWS. 
  
**Tabla 2. Propiedades de la carpeta predeterminada**

|**Propiedad**|**Bandeja de entrada**|**Calendario**|**Contacts**|**Elementos eliminados**|**Borradores**|**Notas**|**Otras carpetas**|**Bandeja de salida**|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
|Nombre para mostrar  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|Identificador de carpeta  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|Recuento de subcarpeta  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|Recuento total  <br/> |X  <br/> ||X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|Recuento de no leído  <br/> |X  <br/> |||X  <br/> |X  <br/> ||X  <br/> |X  <br/> |
   
En la siguiente tabla se enumera las propiedades predeterminadas que se devuelven para cada tipo de elemento mediante las operaciones [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) y EWS [GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) . 
  
**Tabla 3. Propiedades de elementos de forma predeterminada**

|**Propiedad**|**Elemento de calendario**|**Elemento de contacto**|**Elemento de mensaje**|**Elemento de tarea**|
|:-----|:-----|:-----|:-----|:-----|
|Cuerpo  <br/> |||X (1)  <br/> ||
|CalendarItemType  <br/> ||x  <br/> |||
|CompanyName  <br/> ||x  <br/> |||
|CompleteName  <br/> ||x  <br/> |||
|DateTimeCreated  <br/> |||x  <br/> ||
|DateTimeSent  <br/> |||x  <br/> ||
|DueDate  <br/> ||||x(2)  <br/> |
|EmailAddresses  <br/> ||x  <br/> |||
|End  <br/> |x  <br/> ||||
|Archivar como  <br/> ||x  <br/> |||
|De  <br/> |||x  <br/> ||
|HasAttachments  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|ImAddresses  <br/> ||x  <br/> |||
|IsAssociated  <br/> |x  <br/> ||x  <br/> ||
|IsDeliveryReceiptRequested  <br/> |||x  <br/> ||
|ItemId  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|JobTitle  <br/> ||x  <br/> |||
|LegacyFreeBusyStatus  <br/> |x  <br/> ||||
|Ubicación  <br/> |x  <br/> ||||
|Organizador  <br/> |x  <br/> ||||
|PercentComplete  <br/> ||||x  <br/> |
|PhoneNumbers  <br/> ||x  <br/> |||
|PhysicalAddresses  <br/> ||x  <br/> |||
|ResponseObjects  <br/> |x (1)  <br/> ||x (1)  <br/> ||
|Sensitity  <br/> |||x  <br/> ||
|Tama?o  <br/> |||x  <br/> ||
|StartDate  <br/> ||||x(2)  <br/> |
|Estado  <br/> ||||x  <br/> |
|Subject  <br/> |x  <br/> ||x  <br/> |x  <br/> |
   
Notas:
  
1. Se incluyen en la respuesta de la operación **GetItem** . No se incluyen en la respuesta de la operación **FindItem** . 
    
2. Sólo se incluyen en la respuesta si el campo contiene datos. No se incluyen en la respuesta si el campo está en blanco.
    
### <a name="all-properties-set-and-response-shape"></a>Todas las formas de conjunto y respuesta de propiedades

En la siguiente tabla se enumera las propiedades de primera clase que se devuelven mediante una llamada a la API administrada de EWS [Item.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) y métodos de la API administrada de EWS [Item.FindItems](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) y la forma de respuesta "todas las propiedades" devueltos por la [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) y [ GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) las operaciones de EWS. 
  
Puede agregar propiedades adicionales a la propiedad establecer o incluyan propiedades extendidas. Para obtener información detallada, vea [las propiedades y las propiedades extendidas de EWS en Exchange](properties-and-extended-properties-in-ews-in-exchange.md).
  
**Tabla 4. Propiedades de primera clase**

|||||||
|:-----|:-----|:-----|:-----|:-----|:-----|
|Property  <br/> |Elemento de calendario  <br/> |Elemento de contacto  <br/> |Elemento de mensaje  <br/> |Elemento para exponer  <br/> |Elemento de tarea  <br/> |
|ActualWork  <br/> |||||x  <br/> |
|AdjacentMeetingCount  <br/> |x  <br/> |||||
|AdjacentMeetings  <br/> |x  <br/> |||||
|Alias  <br/> ||x  <br/> ||||
|AllowNewTimeProposal  <br/> |x  <br/> |||||
|AppointmentReplyTime  <br/> |x  <br/> |||||
|AppointmentSequenceNumber  <br/> |x  <br/> |||||
|AppointmentState  <br/> |x  <br/> |||||
|AssignedTime  <br/> |||||x  <br/> |
|AssistantName  <br/> ||x  <br/> ||||
|BccRecipients  <br/> |||x  <br/> |||
|BillingInformation  <br/> |||||x  <br/> |
|Cuerpo  <br/> |x (1)  <br/> |x (1)  <br/> |x (1)  <br/> ||x (1)  <br/> |
|BusinessHomePage  <br/> ||x  <br/> |x  <br/> |||
|CalendarItemType  <br/> |x  <br/> |||||
|Categorías  <br/> |x  <br/> ||x  <br/> |x  <br/> |x  <br/> |
|CcRecipients  <br/> |||x  <br/> |||
|ChangeCount  <br/> |||||x  <br/> |
|Children  <br/> ||x  <br/> ||||
|Companies  <br/> |||||x  <br/> |
|CompleteDate  <br/> |||||x  <br/> |
|CompleteName  <br/> ||x  <br/> ||||
|ConferenceType  <br/> |x  <br/> |||||
|ConflictingMeetingCount  <br/> |x  <br/> |||||
|ConflictingMeetings  <br/> |x  <br/> |||||
|Contactos  <br/> |||||x  <br/> |
|ContactSource  <br/> ||x  <br/> ||||
|ConversationId  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|ConversationIndex  <br/> |||x  <br/> |x  <br/> ||
|ConversationTopic  <br/> |||x  <br/> |x  <br/> ||
|Culture  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|DateTimeCreated  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|DateTimeReceived  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|DateTimeSent  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|DateTimeStamp  <br/> |x  <br/> |||||
|DelegationState  <br/> |||||x  <br/> |
|Delegator  <br/> |||||x  <br/> |
|DeletedOccurances  <br/> |x  <br/> |||||
|Departamento  <br/> ||x  <br/> ||||
|DirectoryId  <br/> ||x  <br/> ||||
|DirectReports  <br/> ||x  <br/> ||||
|DisplayCc  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|DisplayName  <br/> ||x  <br/> ||||
|DisplayTo  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|DueDate  <br/> |||||x  <br/> |
|Duración  <br/> |x  <br/> |||||
|EffectiveRights  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|EmailAddresses  <br/> ||x  <br/> ||||
|End  <br/> |x  <br/> |||||
|EndTimeZone  <br/> |x  <br/> |||||
|Archivar como  <br/> ||x  <br/> ||||
|FileAsMapping  <br/> ||x  <br/> ||||
|FirstOccurance  <br/> |x  <br/> |||||
|De  <br/> |||x  <br/> |x  <br/> ||
|Generación  <br/> ||x  <br/> ||||
|GivenName  <br/> ||x  <br/> ||||
|HasAttachments  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|HasPicture  <br/> ||x  <br/> ||||
|ImAddresses  <br/> ||x  <br/> ||||
|Importancia  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|Iniciales  <br/> ||x  <br/> ||||
|InReplyTo  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|InternetMessageId  <br/> |||x  <br/> |x  <br/> ||
|InternetMessageHeaders  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|IsAllDayEvent  <br/> |x  <br/> |||||
|IsAssociated  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|IsCancelled  <br/> |x  <br/> |||||
|Haya finalizado  <br/> |||||x  <br/> |
|IsDeliveryReceiptRequested  <br/> |||x  <br/> |||
|IsDraft  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|IsFromMe  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|IsMeeting  <br/> |x  <br/> |||||
|IsOnlineMeeting  <br/> |x  <br/> |||||
|Estáleído  <br/> |||x  <br/> |||
|IsReadReceiptRequested  <br/> |||x  <br/> |||
|IsRecurring  <br/> |x  <br/> ||||x  <br/> |
|IsResend  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|IsResponseRequested  <br/> |x  <br/> ||x  <br/> |||
|IsSubmitted  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|IsUnmodified  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|ItemClass  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|ItemId  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|JobTitle  <br/> ||x  <br/> ||||
|LastModifiedName  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|LastModifiedTime  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|LastOccurrance  <br/> |x  <br/> |||||
|LegacyFreeBusyStatus  <br/> |x  <br/> |||||
|Ubicación  <br/> |x  <br/> |||||
|Administrador  <br/> ||x  <br/> ||||
|MeetingRequestWasSent  <br/> |x  <br/> |||||
|MeetingTimeZone  <br/> |x  <br/> |||||
|MeetingWorkspaceUrl  <br/> |x  <br/> |||||
|MiddleName  <br/> ||x  <br/> ||||
|Kilometraje  <br/> ||x  <br/> |||x  <br/> |
|ModifiedOccurrances  <br/> |x  <br/> |||||
|MyResponseType  <br/> |x  <br/> |||||
|NetShowUrl  <br/> |x  <br/> |||||
|Alias  <br/> ||x  <br/> ||||
|Notas  <br/> ||x  <br/> ||||
|OfficeLocation  <br/> ||x  <br/> ||||
|OptionalAttendees  <br/> |x  <br/> |||||
|Organizador  <br/> |x  <br/> |||||
|OriginalStart  <br/> |x  <br/> |||||
|Owner  <br/> |||||x  <br/> |
|Id  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|PercentComplete  <br/> |||||x  <br/> |
|PhoneNumbers  <br/> ||x  <br/> ||||
|PhoneticFirstName  <br/> ||x  <br/> ||||
|PhoneticFullName  <br/> ||x  <br/> ||||
|PhoneticLastName  <br/> ||x  <br/> ||||
|Foto  <br/> ||x  <br/> ||||
|PhysicalAddresses  <br/> ||x  <br/> ||||
|PostalAddressIndex  <br/> ||x  <br/> ||||
|PostedTime  <br/> ||||x  <br/> ||
|Profesión  <br/> ||x  <br/> ||||
|ReceivedBy  <br/> |||x  <br/> |||
|ReceivedRepresenting  <br/> |||x  <br/> |||
|Reccurrence  <br/> |x  <br/> ||||x  <br/> |
|Referencias  <br/> |||x  <br/> |x  <br/> ||
|ReminderDueBy  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|ReminderIsSet  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|ReminderMinutesBeforeStart  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|ReplyTo  <br/> |||x  <br/> |||
|RequiredAttendees  <br/> |x  <br/> |||||
|Recursos  <br/> |x  <br/> |||||
|ResponseObjects  <br/> |x (1)  <br/> |x (1)  <br/> |x (1)  <br/> |x (1)  <br/> |x (1)  <br/> |
|Remitente  <br/> |||x  <br/> |x  <br/> ||
|Confidencialidad  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|Tama?o  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|NombreCónyuge  <br/> ||x  <br/> ||||
|Inicio  <br/> |x  <br/> |||||
|StartDate  <br/> |||||x  <br/> |
|StartTimeZone  <br/> |x  <br/> |||||
|Estado  <br/> |||||x  <br/> |
|StatusDescription  <br/> |||||x  <br/> |
|Subject  <br/> |x  <br/> |x  <br/> |x  <br/> ||x  <br/> |
|Apellido  <br/> ||x  <br/> ||||
|TimeZone  <br/> |x  <br/> |||||
|ToRecipients  <br/> |||x  <br/> |||
|TotalWork  <br/> |||||x  <br/> |
|WebClientEditFormQueryString  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|WebClientReadFormQueryString  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
   
Notas:
  
1. Incluye cuándo se [enlace a un elemento](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) y en la respuesta de la [operación GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx). No se incluyen en el resultado del método [Item.FindItems](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) o la respuesta de la [operación FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx).
    
## <a name="see-also"></a>Vea también

- [Desarrollo de clientes de servicios web de Exchange](develop-web-service-clients-for-exchange.md)
    
- [Operación FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    
- [Operación GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx)
    
- [Operación FindFolder](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)
    
- [Operación GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx)
    

