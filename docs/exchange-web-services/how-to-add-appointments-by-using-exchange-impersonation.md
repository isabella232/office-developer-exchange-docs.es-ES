---
title: Agregar citas mediante el uso de la suplantación de Exchange
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 78d5e51b-900f-4302-b9a8-fdc9aa4b65a5
description: Obtenga información sobre cómo usar suplantación con la API administrada de EWS o EWS en Exchange para agregar citas a los calendarios de los usuarios.
ms.openlocfilehash: fe737658b88aca66d8b4c2860245db000888ba17
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763055"
---
# <a name="add-appointments-by-using-exchange-impersonation"></a>Agregar citas mediante el uso de la suplantación de Exchange

Obtenga información sobre cómo usar suplantación con la API administrada de EWS o EWS en Exchange para agregar citas a los calendarios de los usuarios.
  
Puede crear una aplicación de servicio que inserta citas directamente en un calendario de Exchange mediante el uso de una cuenta de servicio que tiene la **AppplicationImpersonation**[habilitada la función](how-to-configure-impersonation.md). Cuando se utiliza la suplantación, la aplicación actúa como el usuario; es como si el usuario agrega la cita al calendario mediante el uso de un cliente como Outlook. 
  
Cuando se utiliza la suplantación, tenga en cuenta lo siguiente:
  
- El objeto [ExchangeService](http://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.aspx) debe estar enlazado a la cuenta de servicio. Puede usar el mismo objeto **ExchangeService** para suplantar a varias cuentas cambiando la propiedad [ImpersonatedUserId](http://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.impersonateduserid.aspx) para cada cuenta que se va a suplantar. 
    
- Cualquier elemento que guarde en una cuenta suplantada sólo se puede usar una vez. Si desea guardar la cita de la misma en varias cuentas, por ejemplo, se debe crear un objeto de [cita](http://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.aspx) para cada cuenta de. 
    
## <a name="prerequisites"></a>Requisitos previos

La aplicación necesita una cuenta para usar para conectarse al servidor de Exchange antes de que puede usar la suplantación. Es recomendable que use una cuenta de servicio para la aplicación que se ha concedido a la función de suplantación de la aplicación para las cuentas que se va a obtener acceso a. Para obtener más información, vea [Configure suplantación](how-to-configure-impersonation.md)
  
## <a name="add-appointments-by-using-impersonation-with-the-ews-managed-api"></a>Agregar citas mediante la suplantación con la API administrada de EWS

En el ejemplo siguiente se agrega una reunión o cita en el calendario de una o más cuentas de Exchange. El método toma tres parámetros.
  
-  _servicio_ : un objeto **ExchangeService** enlazado a la cuenta de la aplicación de servicio en el servidor de Exchange. 
    
-  _emailAddresses_ : un objeto [System.List](http://msdn.microsoft.com/library/6sh2ey19.aspx) que contiene una lista de cadenas de dirección de correo electrónico SMTP. 
    
-  _configuración de fábrica_ , un objeto que implementa la interfaz **IAppointmentFactory** . Esta interfaz tiene un método, **GetAppointment** que toma un objeto **ExchangeService** como un parámetro y devuelve un objeto de la **cita** . Se define la interfaz **IAppointmentFactory** [interfaz IAppointmentFactory](#bk_IAppointmentFactory).
    
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

Cuando se guarda la cita, el código comprueba para determinar si los asistentes que se han agregado a la propiedad [RequiredAttendees](http://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.requiredattendees.aspx) . Si tienen, se llama al método de [Appointment.Save](http://msdn.microsoft.com/library/dd635394.aspx) con el valor de la enumeración [SendToAllAndSaveCopy](http://msdn.microsoft.com/library/microsoft.exchange.webservices.data.sendinvitationsmode.aspx) para que los asistentes reciban las convocatorias de reunión; de lo contrario, se llama al método de **Appointment.Save** con el valor de la enumeración [SendToNone](http://msdn.microsoft.com/library/microsoft.exchange.webservices.data.sendinvitationsmode.aspx) para que la cita se guarda en el calendario del usuario suplantado con la propiedad [Appointment.IsMeeting](http://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.ismeeting.aspx) establecida en **false**.
  
### <a name="iappointmentfactory-interface"></a>Interfaz IAppointmentFactory
<a name="bk_IAppointmentFactory"> </a>

Debido a que se necesita un nuevo objeto de **cita** cada vez que se desea guardar una cita en el calendario de un usuario suplantado, la interfaz **IAppointmentFactory** resume el objeto que se utiliza para rellenar cada objeto de la **cita** . Esta versión es una interfaz simple que contiene un solo método, **GetAppointment**, que toma un objeto **ExchangeService** como un parámetro y devuelve un nuevo objeto de **cita** enlazado a ese objeto **ExchangeService** . 
  
```cs
interface IAppointmentFactory
{
  Appointment GetAppointment(ExchangeService service);
}
```

El siguiente ejemplo de clase de **AppointmentFactory** se muestra una implementación de la interfaz **IAppointmentFactory** que devuelve una cita simple que se produce tres días desde ahora. Si quita el comentario de la `appointment.RequiredAttendees.Add` línea, el método **GetAppointment** devolverá una reunión y la dirección de correo electrónico especificada en que la línea recibirán una convocatoria de reunión con el usuario suplantado aparece como el organizador. 
  
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

## <a name="add-appointments-by-using-impersonation-with-ews"></a>Agregue citas con suplantación de EWS

EWS habilita la aplicación para usar suplantación para agregar elementos a un calendario en nombre propietario del calendario. En este ejemplo se muestra cómo usar la operación [CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) para agregar una cita en el calendario de una cuenta suplantada. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
       xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
       xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

Tenga en cuenta que no sea la adición del elemento **ExchangeImpersonation** en el encabezado SOAP para especificar la cuenta que nos estamos suplantación, esto es la misma solicitud XML usada para crear una cita sin usar suplantación. 
  
En el ejemplo siguiente se muestra la respuesta XML que es devuelto por la operación **CreateItem** . 
  
> [!NOTE]
> Los atributos **ItemId** y **ChangeKey** son más cortos para mejorar la legibilidad. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="775" MinorBuildNumber="7" Version="V2_4" 
 xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:CreateItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

Una vez más, esto es el mismo XML que se devuelve cuando se usa la operación **CreateItem** sin usar suplantación. 
  
## <a name="see-also"></a>Vea también


- [Suplantación y EWS en Exchange](impersonation-and-ews-in-exchange.md)
    
- [Rol ApplicationImpersonation](http://technet.microsoft.com/en-us/library/dd776119%28v=exchg.150%29.aspx)
    
- [Configurar la suplantación](how-to-configure-impersonation.md)
    
- [Identificación de la cuenta para suplantar a](how-to-identify-the-account-to-impersonate.md)
    
- [Crear citas y reuniones mediante el uso de EWS en Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [Operación CreateItem (elemento de calendario)](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx)
    
- [ExchangeService.ImpersonatedUserId (propiedad)](http://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.impersonateduserid.aspx.aspx)
    

