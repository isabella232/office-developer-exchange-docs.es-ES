---
title: Adición de citas mediante la suplantación de Exchange
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.assetid: 78d5e51b-900f-4302-b9a8-fdc9aa4b65a5
description: Obtenga información sobre cómo usar la suplantación con la API administrada de EWS o EWS en Exchange para agregar citas a los calendarios de los usuarios.
localization_priority: Priority
ms.openlocfilehash: b1473d72113f8cc07d05364a4d87fedf23c7351d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455334"
---
# <a name="add-appointments-by-using-exchange-impersonation"></a>Adición de citas mediante la suplantación de Exchange

Obtenga información sobre cómo usar la suplantación con la API administrada de EWS o EWS en Exchange para agregar citas a los calendarios de los usuarios.
  
Puede crear una aplicación de servicio que inserte citas directamente en un calendario de Exchange mediante una cuenta de servicio que tenga [habilitada la función](how-to-configure-impersonation.md) **ApplicationImpersonation** . Cuando se utiliza la suplantación, la aplicación actúa como usuario; es como si el usuario agregara la cita al calendario mediante un cliente como Outlook. 
  
Cuando use la suplantación, tenga en cuenta lo siguiente:
  
- El objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.aspx) debe estar enlazado a la cuenta de servicio. Puede usar el mismo objeto **ExchangeService** para representar varias cuentas cambiando la propiedad [ImpersonatedUserId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.impersonateduserid.aspx) para cada cuenta que desee suplantar. 
    
- Cualquier elemento que guarde en una cuenta suplantada solo puede usarse una vez. Si desea guardar la misma cita en varias cuentas, por ejemplo, tiene que crear un objeto de [cita](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.aspx) para cada cuenta. 
    
## <a name="prerequisites"></a>Requisitos previos

La aplicación necesita una cuenta para conectarse con el servidor de Exchange antes de poder usar la suplantación. Le recomendamos que use una cuenta de servicio para la aplicación a la que se le haya concedido el rol de suplantación de aplicaciones para las cuentas a las que tendrá acceso. Para obtener más información, vea [configurar la suplantación](how-to-configure-impersonation.md)
  
## <a name="add-appointments-by-using-impersonation-with-the-ews-managed-api"></a>Agregar citas con la suplantación con la API administrada de EWS

En el siguiente ejemplo se agrega una cita o una reunión al calendario de una o varias cuentas de Exchange. El método toma tres parámetros.
  
-  _servicio_ : objeto **ExchangeService** enlazado a la cuenta de la aplicación de servicio en el servidor Exchange. 
    
-  _emailAddresses_ : un objeto [System. List](https://msdn.microsoft.com/library/6sh2ey19.aspx) que contiene una lista de cadenas de direcciones de correo electrónico SMTP. 
    
-  _Factory_ : un objeto que implementa la interfaz **IAppointmentFactory** . Esta interfaz tiene un método, **GetAppointment** , que toma un objeto **ExchangeService** como parámetro y devuelve un objeto **appointment** . La interfaz **IAppointmentFactory** está definida [IAppointmentFactory interfaz](#bk_IAppointmentFactory).
    
```cs
private static void CreateAppointments(ExchangeService service, List<string> emailAddresses, IAppointmentFactory factory)
{
  // Loop through the list of email addresses to add the appointment.
  foreach (var emailAddress in emailAddresses)
  {
    Console.WriteLine(string.Format("  Placing appointment in calendar for {0}.", emailAddress));
    // Set the email address of the account to get the appointment.
    service.ImpersonatedUserId = new ImpersonatedUserId(ConnectingIdType.SmtpAddress, emailAddress);
    // Get the appointment to add.
    Appointment appointment = factory.GetAppointment(service);
    // Save the appointment.
    try
    {
      if (appointment.RequiredAttendees.Count > 0)
      {
        // The appointment has attendees so send them the meeting request.
        appointment.Save(SendInvitationsMode.SendToAllAndSaveCopy);
      }
      else
      {
        // The appointment does not have attendees, so just save to calendar.
        appointment.Save(SendInvitationsMode.SendToNone);
      }
    }
    catch (ServiceResponseException ex)
    {
      Console.WriteLine(string.Format("Could not create appointment for {0}", emailAddress));
      Console.WriteLine(ex.Message);
    }
  }
}
```

Al guardar la cita, el código comprueba si se ha agregado algún asistente a la propiedad [RequiredAttendees](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.requiredattendees.aspx) . Si es así, se llama al método [appointment. Save](https://msdn.microsoft.com/library/dd635394.aspx) con el valor de enumeración [SendToAllAndSaveCopy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.sendinvitationsmode.aspx) para que los asistentes reciban las convocatorias de reunión; de lo contrario, se llama al método **appointment. Save** con el valor de enumeración [SendToNone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.sendinvitationsmode.aspx) para que la cita se guarde en el calendario del usuario suplantado con la propiedad [appointment. IsMeeting](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.ismeeting.aspx) establecida en **false**.
  
### <a name="iappointmentfactory-interface"></a>Interfaz IAppointmentFactory
<a name="bk_IAppointmentFactory"> </a>

Debido a que necesita un nuevo objeto **appointment** cada vez que desea guardar una cita en el calendario de un usuario suplantado, la interfaz **IAppointmentFactory** abstrae el objeto que se usa para rellenar cada objeto **appointment** . Esta versión es una interfaz simple que contiene un solo método, **GetAppointment**, que toma un objeto **ExchangeService** como un parámetro y devuelve un nuevo objeto **appointment** enlazado a dicho objeto **ExchangeService** . 
  
```cs
interface IAppointmentFactory
{
  Appointment GetAppointment(ExchangeService service);
}
```

El siguiente ejemplo de clase **AppointmentFactory** muestra una implementación de la interfaz **IAppointmentFactory** que devuelve una cita sencilla que se produce tres días a partir de ahora. Si quita la marca de comentario de la `appointment.RequiredAttendees.Add` línea, el método **GetAppointment** devolverá una reunión y la dirección de correo electrónico especificada en esa línea recibirá una convocatoria de reunión con el usuario suplantado que se muestra como organizador. 
  
```cs
class AppointmentFactory : IAppointmentFactory
{
  public Appointment GetAppointment(ExchangeService service)
  {
    // First create the appointment to add.
    Appointment appointment = new Appointment(service);
    // Set the properties on the appointment.
    appointment.Subject = "Tennis lesson";
    appointment.Body = "Focus on backhand this week.";
    appointment.Start = DateTime.Now.AddDays(3);
    appointment.End = appointment.Start.AddHours(1);
    appointment.Location = "Tennis club";
    // appointment.RequiredAttendees.Add(new Attendee("sonyaf@contoso1000.onmicrosoft.com"));
    return appointment;
  }
}

```

## <a name="add-appointments-by-using-impersonation-with-ews"></a>Agregar citas mediante la suplantación con EWS

EWS permite que la aplicación use la suplantación para agregar elementos a un calendario en nombre del propietario del calendario. En este ejemplo se muestra cómo usar la operación [CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) para agregar una cita al calendario de una cuenta suplantada. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
       xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
       xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Pacific Standard Time" />
    </t:TimeZoneContext>
    <t:ExchangeImpersonation>
      <t:ConnectingSID>
        <t:SmtpAddress>alfred@contoso.com</t:SmtpAddress>
      </t:ConnectingSID>
    </t:ExchangeImpersonation>
  </soap:Header>
  <soap:Body>
    <m:CreateItem SendMeetingInvitations="SendToNone">
      <m:Items>
        <t:CalendarItem>
          <t:Subject>Tennis lesson</t:Subject>
          <t:Body BodyType="HTML">Focus on backhand this week.</t:Body>
          <t:ReminderDueBy>2013-09-19T14:37:10.732-07:00</t:ReminderDueBy>
          <t:Start>2013-09-21T19:00:00.000Z</t:Start>
          <t:End>2013-09-21T20:00:00.000Z</t:End>
          <t:Location>Tennis club</t:Location>
          <t:MeetingTimeZone TimeZoneName="Pacific Standard Time" />
        </t:CalendarItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

Tenga en cuenta que, aparte de la adición del elemento **ExchangeImpersonation** en el encabezado SOAP para especificar la cuenta que se va a suplantar, esta es la misma solicitud XML que se usa para crear una cita sin usar suplantación. 
  
En el ejemplo siguiente se muestra el XML de respuesta que devuelve la operación **CreateItem** . 
  
> [!NOTE]
> Los atributos **Itemid** y **changekey** se acortan para facilitar la legibilidad. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="775" MinorBuildNumber="7" Version="V2_4" 
 xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:CreateItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:CreateItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:CalendarItem>
              <t:ItemId Id="AAMkA" ChangeKey="DwAAA" />
            </t:CalendarItem>
          </m:Items>
        </m:CreateItemResponseMessage>
      </m:ResponseMessages>
    </m:CreateItemResponse>
  </s:Body>
</s:Envelope>

```

De nuevo, este es el mismo XML que se devuelve cuando se utiliza la operación **CreateItem** sin usar la suplantación. 
  
## <a name="see-also"></a>Vea también


- [Suplantación y EWS en Exchange](impersonation-and-ews-in-exchange.md)
    
- [Rol ApplicationImpersonation](https://technet.microsoft.com/library/dd776119%28v=exchg.150%29.aspx)
    
- [Configurar la suplantación](how-to-configure-impersonation.md)
    
- [Identificación de la cuenta que se va a suplantar](how-to-identify-the-account-to-impersonate.md)
    
- [Crear citas y reuniones mediante EWS en Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [Operación CreateItem (elemento de calendario)](../web-service-reference/createitem-operation-calendar-item.md)
    
- [Propiedad ExchangeService. ImpersonatedUserId](https://docs.microsoft.com/dotnet/api/microsoft.exchange.webservices.data.exchangeservice.impersonateduserid?view=exchange-ews-api)
    

