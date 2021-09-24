---
title: Operación GetReminders
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 1b56f83f-3b87-4b55-8259-fde6692da681
description: Busque información sobre la operación ews GetReminders.
ms.openlocfilehash: e47dbb6ffceac3535bb72f93ee27bbb3f3f259e6
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513566"
---
# <a name="getreminders-operation"></a>Operación GetReminders

Busque información sobre la **operación ews GetReminders.** 
  
La **operación GetReminders** Exchange Web Services (EWS) recupera los avisos de los elementos de calendario y tarea. 
  
Esta operación se introdujo en Exchange Server 2013.
  
## <a name="using-the-getreminders-operation"></a>Uso de la operación GetReminders

La **operación GetReminders** obtiene avisos para los elementos de calendario y tarea actuales y futuros en el buzón del usuario, en función de los valores de elemento pasados en la solicitud. La operación puede recuperar todos los elementos de calendario actuales y futuros, así como las tareas que tienen un conjunto de avisos. Los elementos del calendario privado se incluyen en las respuestas. Las tareas sin avisos no se incluyen en las respuestas, ni los correos electrónicos con avisos o marcas de seguimiento. 
  
Para recuperar todos los avisos actuales, se recomienda establecer [ReminderType](remindertype.md) en **All** y [EndTime](endtime-remindermessagedatatype.md) en la hora actual. 
  
Si los [elementos BeginTime](begintime.md) y **EndTime** se incluyen en la solicitud, la respuesta incluye avisos para cualquier elemento de calendario y tarea que se produzca entre tener un aviso que se produzca entre **BeginTime** y **EndTime**.
  
En la tabla siguiente se describe el comportamiento del **elemento ReminderType** cuando se incluyen los elementos **BeginTime** y **EndTime.** 
  
|ReminderType** element value**|**Descripción**|
|:-----|:-----|
|Todo  <br/> |Avisos que se producen entre **BeginTime** y **EndTime**.  <br/> |
|Current  <br/> |Avisos devueltos por **All**, además de avisos anteriores a la ventana de tiempo solicitado si el evento sigue en curso, además de todas las citas independientemente de la edad.  <br/> |
|Antiguo  <br/> |Avisos devueltos por **Todos**, menos eventos que aún no se han completado, menos todas las citas. Los **elementos BeginTime** y **EndTime** deben establecerse para usar el **valor Old.**  <br/> |
   
### <a name="getreminders-operation-soap-headers"></a>Encabezados SOAP de operación getReminders

La **operación GetReminders** puede usar los encabezados SOAP que se enumeran en la tabla siguiente. 
  
|**Nombre de encabezado**|**Elemento**|**Descripción**|
|:-----|:-----|:-----|
|**Suplantación** <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Identifica el usuario al que la aplicación cliente está suplantando. Este encabezado es aplicable a una solicitud.  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |Identifica la referencia cultural, tal como se define en RFC 3066, "Etiquetas para la identificación de idiomas", que se usará para tener acceso al buzón. Este encabezado es aplicable a una solicitud.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Identifica la versión del esquema para la solicitud de operación. Este encabezado es aplicable a una solicitud.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Identifica la versión del servidor que respondió a la solicitud. Este encabezado es aplicable a una respuesta.  <br/> |
   
## <a name="getreminders-operation-request-example"></a>Ejemplo de solicitud de operación GetReminders

En el siguiente ejemplo de una solicitud de operación **GetReminders** se muestra cómo recuperar los cinco primeros elementos del calendario que se producen entre **BeginTime** y **EndTime**.
  
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

El cuerpo SOAP de la solicitud de ejemplo contiene los siguientes elementos:
  
- [GetReminders](getreminders.md)
    
- [EndTime](endtime-remindermessagedatatype.md)
    
- [ReminderType](remindertype.md)
    
El cuerpo SOAP también puede contener los siguientes elementos:
  
- [BeginTime](begintime.md)
    
- [MaxItems](maxitems.md)
    
## <a name="successful-getreminders-operation-response"></a>Respuesta de operación GetReminders correcta

En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación **GetReminders.** La respuesta contiene un aviso para el elemento de calendario "Reunión de equipo" y un aviso para la tarea "Tarea para enviar notas de reunión". 
  
> [!NOTE]
> Los identificadores se han acortado para conservar la legibilidad. 
  
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

El cuerpo SOAP de la respuesta contiene los siguientes elementos:
  
- [GetRemindersResponse](getremindersresponse.md)
    
- [Avisos](reminders.md)
    
- [Aviso](reminder.md)
    
- [Asunto](subject.md)
    
- [Location](location-remindermessagedatatype.md)
    
- [ReminderTime](remindertime.md)
    
- [StartDate](startdate.md)
    
- [EndDate](enddate-remindertype.md)
    
- [ItemId](itemid.md)
    
- [RecurringMasterItemId](recurringmasteritemid.md)
    
- [ReminderGroup](remindergroup.md)
    
- [UID](uid-remindertype.md)
    
## <a name="getreminders-operation-error-response-example"></a>Ejemplo de respuesta de error de operación GetReminders

En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **GetReminders.** Esta es una respuesta a una solicitud en la que la fecha de finalización era anterior a la fecha de inicio. 
  
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

El cuerpo SOAP de la respuesta de error contiene los siguientes elementos:
  
- [GetRemindersResponse](getremindersresponse.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
Para obtener códigos de error adicionales genéricos para EWS y específicos de esta operación, vea [ResponseCode](responsecode.md).
  
## <a name="see-also"></a>Ver también


- [PerformReminderAction](performreminderaction.md)
    

