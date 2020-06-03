---
title: Operación GetReminders
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1b56f83f-3b87-4b55-8259-fde6692da681
description: Buscar información sobre la operación de EWS de GetReminders.
ms.openlocfilehash: dcbe20c674d7524a7776d374fa6964899abf472f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458309"
---
# <a name="getreminders-operation"></a>Operación GetReminders

Buscar información sobre la operación de EWS de **GetReminders** . 
  
La operación **GetReminders** de servicios web Exchange (EWS) recupera avisos para los elementos de calendario y tarea. 
  
Esta operación se introdujo en Exchange Server 2013.
  
## <a name="using-the-getreminders-operation"></a>Uso de la operación GetReminders

La operación **GetReminders** obtiene avisos para los elementos de calendario y tarea actuales y futuros en el buzón de correo del usuario, en función de los valores de elemento que se pasan en la solicitud. La operación puede recuperar todos los elementos de calendario actuales y futuros, así como las tareas que tienen un conjunto de avisos. Los elementos de calendario privados se incluyen en las respuestas. Las tareas sin avisos no se incluyen en las respuestas ni son mensajes de correo electrónico con avisos o marcas de seguimiento. 
  
Para recuperar todos los avisos actuales, se recomienda establecer [ReminderType](remindertype.md) en **All** y el [EndTime](endtime-remindermessagedatatype.md) en la hora actual. 
  
Si los elementos [BeginTime](begintime.md) y **EndTime** se incluyen en la solicitud, la respuesta incluye avisos para todos los elementos de calendario y tarea que se producen entre los que tienen un aviso entre la BeginTime **y la**hora de finalización. **BeginTime**
  
En la tabla siguiente se describe el comportamiento del elemento **ReminderType** cuando se incluyen los elementos **BeginTime** y **EndTime** . 
  
|Valor del elemento ReminderType * * * *|**Descripción**|
|:-----|:-----|
|Todo  <br/> |Avisos que se producen entre los **BeginTime** y **EndTime**.  <br/> |
|Current  <br/> |Avisos devueltos por **All**, además de los avisos anteriores a la ventana de tiempo solicitada si el evento sigue en curso, además de todas las citas independientemente de la antigüedad.  <br/> |
|Obsolet  <br/> |Avisos devueltos por **All**, menos eventos que todavía no se han completado, pero menos todas las citas. Los elementos **BeginTime** y **EndTime** deben estar configurados para usar el valor **anterior** .  <br/> |
   
### <a name="getreminders-operation-soap-headers"></a>Encabezados SOAP de operación GetReminders

La operación **GetReminders** puede usar los encabezados SOAP que se enumeran en la tabla siguiente. 
  
|**Nombre de encabezado**|**Elemento**|**Descripción**|
|:-----|:-----|:-----|
|**Suplantación** <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Identifica al usuario que está suplantando la aplicación cliente. Este encabezado se aplica a una solicitud.  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |Identifica la referencia cultural, tal y como se define en RFC 3066, "etiquetas para la identificación de idiomas", que se va a usar para obtener acceso al buzón. Este encabezado se aplica a una solicitud.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Identifica la versión del esquema para la solicitud de operación. Este encabezado se aplica a una solicitud.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Identifica la versión del servidor que respondió a la solicitud. Este encabezado se aplica a una respuesta.  <br/> |
   
## <a name="getreminders-operation-request-example"></a>Ejemplo de solicitud de operación GetReminders

El siguiente ejemplo de una solicitud de operación de **GetReminders** muestra cómo recuperar los cinco primeros elementos de calendario que se producen entre la **BeginTime** y la **hora de finalización.**
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
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

El cuerpo SOAP de solicitud de ejemplo contiene los siguientes elementos:
  
- [GetReminders](getreminders.md)
    
- [EndTime](endtime-remindermessagedatatype.md)
    
- [ReminderType](remindertype.md)
    
El cuerpo de SOAP también puede contener los siguientes elementos:
  
- [BeginTime](begintime.md)
    
- [MaxItems](maxitems.md)
    
## <a name="successful-getreminders-operation-response"></a>Respuesta de operación GetReminders correcta

En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación de **GetReminders** . La respuesta contiene un aviso para el elemento de calendario "Team Meeting" y un aviso para la tarea "tarea para enviar notas de reunión". 
  
> [!NOTE]
> Los identificadores se han abreviado para preservar la legibilidad. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <ServerVersionInfo MajorVersion="15"
                       MinorVersion="0"
                       MajorBuildNumber="918"
                       MinorBuildNumber="7"
                       Version="V2_10"
                       xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetRemindersResponse ResponseClass="Success"
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <Reminders>
        <Reminder xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
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
        <Reminder xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
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

El cuerpo SOAP de respuesta contiene los siguientes elementos:
  
- [GetRemindersResponse](getremindersresponse.md)
    
- [Avisos](reminders.md)
    
- [Aviso](reminder.md)
    
- [Asunto](subject.md)
    
- [Ubicación](location-remindermessagedatatype.md)
    
- [ReminderTime](remindertime.md)
    
- [StartDate](startdate.md)
    
- [EndDate](enddate-remindertype.md)
    
- [ItemId](itemid.md)
    
- [RecurringMasterItemId](recurringmasteritemid.md)
    
- [ReminderGroup](remindergroup.md)
    
- [EXCLUSIVO](uid-remindertype.md)
    
## <a name="getreminders-operation-error-response-example"></a>Ejemplo de respuesta de error de operación GetReminders

En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **GetReminders** . Se trata de una respuesta a una solicitud en la que la fecha de finalización era anterior a la fecha de inicio. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <ServerVersionInfo MajorVersion="15"
                       MinorVersion="0"
                       MajorBuildNumber="918"
                       MinorBuildNumber="7"
                       Version="V2_10"
                       xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetRemindersResponse ResponseClass="Error"
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <MessageText>EndDate is earlier than StartDate</MessageText>
      <ResponseCode>ErrorInvalidOperation</ResponseCode>
      <DescriptiveLinkKey>0</DescriptiveLinkKey>
    </GetRemindersResponse>
  </s:Body>
</s:Envelope>
```

El cuerpo SOAP de respuesta de error contiene los siguientes elementos:
  
- [GetRemindersResponse](getremindersresponse.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
Para obtener los códigos de error adicionales que son genéricos para EWS y específicos de esta operación, vea [ResponseCode](responsecode.md).
  
## <a name="see-also"></a>Vea también


- [PerformReminderAction](performreminderaction.md)
    

