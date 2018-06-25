---
title: Operación GetReminders
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1b56f83f-3b87-4b55-8259-fde6692da681
description: Busque información sobre la EWS GetReminders operación.
ms.openlocfilehash: 803dabf51b94dbd8fb01f2709a42ff59a597bfd1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764959"
---
# <a name="getreminders-operation"></a>Operación GetReminders

Obtenga información acerca de la operación de EWS **GetReminders** . 
  
La operación de Exchange Web Services (EWS) **GetReminders** recupera avisos para los elementos de calendario y tareas. 
  
Esta operación se introdujo en Exchange Server 2013.
  
## <a name="using-the-getreminders-operation"></a>Mediante la operación GetReminders

La operación **GetReminders** obtiene avisos de calendario actual y futuro y elementos de tarea en el buzón del usuario, según los valores de elemento que se pasan en la solicitud. La operación puede recuperar todos los elementos de calendario actuales y futuros así como las tareas que tienen un aviso a establecer. Elementos de calendario privados se incluyen en las respuestas. Tareas sin avisos no se incluyen en las respuestas, ni son mensajes de correo electrónico con avisos o marcas de seguimiento. 
  
Para recuperar todos los avisos actuales, se recomienda establecer el [ReminderType](remindertype.md) a **todos** y la [hora de finalización](endtime-remindermessagedatatype.md) a la hora actual. 
  
Si los elementos [BeginTime](begintime.md) y **EndTime** se incluyen en la solicitud, la respuesta incluye avisos para cualquier calendario y elementos de tarea que se producen entre tengan un aviso que se produce entre el **BeginTime** y **EndTime**.
  
En la siguiente tabla se describe el comportamiento del elemento **ReminderType** cuando se incluyen los elementos **BeginTime** y **EndTime** . 
  
|ReminderType ** elemento valor **|**Descripción**|
|:-----|:-----|
|Todos  <br/> |Avisos que se producen entre el **BeginTime** y **EndTime**.  <br/> |
|Actual  <br/> |Avisos devueltos por **todos los**, además de avisos que sean anteriores a la ventana de tiempo solicitado si el evento todavía está en curso, además de todas las citas independientemente de su antigüedad.  <br/> |
|Antiguo  <br/> |Avisos devueltos por **todos los**, menos eventos que no se han completado todavía, menos todas las citas. Los elementos **BeginTime** y **EndTime** deben establecerse para usar el valor **anterior** .  <br/> |
   
### <a name="getreminders-operation-soap-headers"></a>Encabezados SOAP de operación de GetReminders

La operación de **GetReminders** puede utilizar los encabezados SOAP que se enumeran en la siguiente tabla. 
  
|**Nombre de encabezado**|**Element**|**Descripción**|
|:-----|:-----|:-----|
|**Suplantación** <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Identifica el usuario que está realizando la suplantación de la aplicación cliente. Este encabezado es aplicable a una solicitud.  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |Identifica la referencia cultural, como se define en RFC 3066, "Etiquetas para la identificación de idiomas," que se utilizará para acceder al buzón. Este encabezado es aplicable a una solicitud.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Identifica la versión del esquema para la solicitud de la operación. Este encabezado es aplicable a una solicitud.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Identifica la versión del servidor que ha respondido a la solicitud. Este encabezado es aplicable a una respuesta.  <br/> |
   
## <a name="getreminders-operation-request-example"></a>Ejemplo de solicitud de operación de GetReminders

El siguiente ejemplo de una solicitud de operación **GetReminders** muestra cómo recuperar los primeros elementos de cinco calendario que se producen entre el **BeginTime** y **EndTime**.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
  <soap:Body>
    <m:GetReminders>
      <m:EndTime>2014-04-16T21:00:00Z</m:EndTime>
      <m:ReminderType>All</m:ReminderType>
    </m:GetReminders>
  </soap:Body>
</soap:Envelope>
```

El ejemplo de solicitud SOAP body contiene los siguientes elementos:
  
- [GetReminders](getreminders.md)
    
- [Hora de finalización](endtime-remindermessagedatatype.md)
    
- [ReminderType](remindertype.md)
    
El cuerpo SOAP también puede contener los siguientes elementos:
  
- [BeginTime](begintime.md)
    
- [MaxItems](maxitems.md)
    
## <a name="successful-getreminders-operation-response"></a>Respuesta es correcta de operación GetReminders

En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación **GetReminders** . La respuesta contiene un aviso para el elemento de calendario "Reunión de equipo" y un aviso para la tarea "De tareas para enviar notas de la reunión". 
  
> [!NOTE]
> Se han abreviado identificadores para conservar la legibilidad. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <ServerVersionInfo MajorVersion="15"
                       MinorVersion="0"
                       MajorBuildNumber="918"
                       MinorBuildNumber="7"
                       Version="V2_10"
                       xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetRemindersResponse ResponseClass="Success"
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <Reminders>
        <Reminder xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
          <Subject>Team meeting</Subject>
          <Location />
          <ReminderTime>2014-04-15T21:00:00Z</ReminderTime>
          <StartDate>2014-04-15T21:00:00Z</StartDate>
          <EndDate>2014-04-15T21:30:00Z</EndDate>
          <ItemId Id="vQAAAA=="
                  ChangeKey="DwAAABYAAAB4to43JyybTYwHLBM1k8MxAAACRoV4" />
          <RecurringMasterItemId Id="K7u5AAA=" ChangeKey="DwAAABYAAAB4to43JyybTYwHLBM1k8MxAAACRoV0" />
          <ReminderGroup>Calendar</ReminderGroup>
          <UID>6CF2FA62</UID>
        </Reminder>
        <Reminder xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
          <Subject>Task to send meeting notes</Subject>
          <Location />
          <ReminderTime>2014-04-16T14:00:00Z</ReminderTime>
          <StartDate>0001-01-02T00:00:00Z</StartDate>
          <EndDate>0001-01-02T00:00:00Z</EndDate>
          <ItemId Id="vAAAAA=="
                  ChangeKey="EwAAABQAAACOs0HEMq1WTKpI7sNu5qXNAAAIDg==" />
          <ReminderGroup>Task</ReminderGroup>
          <UID>vAAAAA==</UID>
        </Reminder>
      </Reminders>
    </GetRemindersResponse>
  </s:Body>
</s:Envelope>
```

La respuesta SOAP body contiene los siguientes elementos:
  
- [GetRemindersResponse](getremindersresponse.md)
    
- [Reminders](reminders.md)
    
- [Aviso](reminder.md)
    
- [Subject](subject.md)
    
- [Location](location-remindermessagedatatype.md)
    
- [ReminderTime](remindertime.md)
    
- [StartDate](startdate.md)
    
- [EndDate](enddate-remindertype.md)
    
- [ItemId](itemid.md)
    
- [RecurringMasterItemId](recurringmasteritemid.md)
    
- [ReminderGroup](remindergroup.md)
    
- [UID](uid-remindertype.md)
    
## <a name="getreminders-operation-error-response-example"></a>Ejemplo de respuesta de error de operación de GetReminders

En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **GetReminders** . Esta es una respuesta a una solicitud en el que la fecha de finalización era anterior a la fecha de inicio. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <ServerVersionInfo MajorVersion="15"
                       MinorVersion="0"
                       MajorBuildNumber="918"
                       MinorBuildNumber="7"
                       Version="V2_10"
                       xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetRemindersResponse ResponseClass="Error"
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <MessageText>EndDate is earlier than StartDate</MessageText>
      <ResponseCode>ErrorInvalidOperation</ResponseCode>
      <DescriptiveLinkKey>0</DescriptiveLinkKey>
    </GetRemindersResponse>
  </s:Body>
</s:Envelope>
```

La respuesta de error SOAP body contiene los siguientes elementos:
  
- [GetRemindersResponse](getremindersresponse.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
Para códigos de error adicionales que son genéricos para EWS y específicos de esta operación, vea [ResponseCode](responsecode.md).
  
## <a name="see-also"></a>Vea también


- [PerformReminderAction](performreminderaction.md)
    

