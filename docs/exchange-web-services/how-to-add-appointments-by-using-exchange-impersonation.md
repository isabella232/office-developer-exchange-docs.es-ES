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
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455334"
---
# <a name="add-appointments-by-using-exchange-impersonation"></a><span data-ttu-id="00df0-103">Adición de citas mediante la suplantación de Exchange</span><span class="sxs-lookup"><span data-stu-id="00df0-103">Add appointments by using Exchange impersonation</span></span>

<span data-ttu-id="00df0-104">Obtenga información sobre cómo usar la suplantación con la API administrada de EWS o EWS en Exchange para agregar citas a los calendarios de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="00df0-104">Learn how to use impersonation with the EWS Managed API or EWS in Exchange to add appointments to users' calendars.</span></span>
  
<span data-ttu-id="00df0-105">Puede crear una aplicación de servicio que inserte citas directamente en un calendario de Exchange mediante una cuenta de servicio que tenga [habilitada la función](how-to-configure-impersonation.md) **ApplicationImpersonation** .</span><span class="sxs-lookup"><span data-stu-id="00df0-105">You can create a service application that inserts appointments directly into an Exchange calendar by using a service account that has the **ApplicationImpersonation** [role enabled](how-to-configure-impersonation.md).</span></span> <span data-ttu-id="00df0-106">Cuando se utiliza la suplantación, la aplicación actúa como usuario; es como si el usuario agregara la cita al calendario mediante un cliente como Outlook.</span><span class="sxs-lookup"><span data-stu-id="00df0-106">When you use impersonation, the application is acting as the user; it's as if the user added the appointment to the calendar by using a client such as Outlook.</span></span> 
  
<span data-ttu-id="00df0-107">Cuando use la suplantación, tenga en cuenta lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="00df0-107">When you are using impersonation, keep in mind the following:</span></span>
  
- <span data-ttu-id="00df0-108">El objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.aspx) debe estar enlazado a la cuenta de servicio.</span><span class="sxs-lookup"><span data-stu-id="00df0-108">Your [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.aspx) object must be bound to the service account.</span></span> <span data-ttu-id="00df0-109">Puede usar el mismo objeto **ExchangeService** para representar varias cuentas cambiando la propiedad [ImpersonatedUserId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.impersonateduserid.aspx) para cada cuenta que desee suplantar.</span><span class="sxs-lookup"><span data-stu-id="00df0-109">You can use the same **ExchangeService** object to impersonate multiple accounts by changing the [ImpersonatedUserId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.impersonateduserid.aspx) property for each account that you want to impersonate.</span></span> 
    
- <span data-ttu-id="00df0-110">Cualquier elemento que guarde en una cuenta suplantada solo puede usarse una vez.</span><span class="sxs-lookup"><span data-stu-id="00df0-110">Any item that you save to an impersonated account can only be used once.</span></span> <span data-ttu-id="00df0-111">Si desea guardar la misma cita en varias cuentas, por ejemplo, tiene que crear un objeto de [cita](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.aspx) para cada cuenta.</span><span class="sxs-lookup"><span data-stu-id="00df0-111">If you want to save the same appointment in multiple accounts, for example, you have to create an [Appointment](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.aspx) object for each account.</span></span> 
    
## <a name="prerequisites"></a><span data-ttu-id="00df0-112">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="00df0-112">Prerequisites</span></span>

<span data-ttu-id="00df0-113">La aplicación necesita una cuenta para conectarse con el servidor de Exchange antes de poder usar la suplantación.</span><span class="sxs-lookup"><span data-stu-id="00df0-113">Your application needs an account to use to connect to the Exchange server before it can use impersonation.</span></span> <span data-ttu-id="00df0-114">Le recomendamos que use una cuenta de servicio para la aplicación a la que se le haya concedido el rol de suplantación de aplicaciones para las cuentas a las que tendrá acceso.</span><span class="sxs-lookup"><span data-stu-id="00df0-114">We suggest that you use a service account for the application that has been granted the Application Impersonation role for the accounts that it will be accessing.</span></span> <span data-ttu-id="00df0-115">Para obtener más información, vea [configurar la suplantación](how-to-configure-impersonation.md)</span><span class="sxs-lookup"><span data-stu-id="00df0-115">For more information, see [Configure impersonation](how-to-configure-impersonation.md)</span></span>
  
## <a name="add-appointments-by-using-impersonation-with-the-ews-managed-api"></a><span data-ttu-id="00df0-116">Agregar citas con la suplantación con la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="00df0-116">Add appointments by using impersonation with the EWS Managed API</span></span>

<span data-ttu-id="00df0-117">En el siguiente ejemplo se agrega una cita o una reunión al calendario de una o varias cuentas de Exchange.</span><span class="sxs-lookup"><span data-stu-id="00df0-117">The following example adds an appointment or meeting to the calendar of one or more Exchange accounts.</span></span> <span data-ttu-id="00df0-118">El método toma tres parámetros.</span><span class="sxs-lookup"><span data-stu-id="00df0-118">The method takes three parameters.</span></span>
  
-  <span data-ttu-id="00df0-119">_servicio_ : objeto **ExchangeService** enlazado a la cuenta de la aplicación de servicio en el servidor Exchange.</span><span class="sxs-lookup"><span data-stu-id="00df0-119">_service_ — An **ExchangeService** object bound to the service application's account on the Exchange server.</span></span> 
    
-  <span data-ttu-id="00df0-120">_emailAddresses_ : un objeto [System. List](https://msdn.microsoft.com/library/6sh2ey19.aspx) que contiene una lista de cadenas de direcciones de correo electrónico SMTP.</span><span class="sxs-lookup"><span data-stu-id="00df0-120">_emailAddresses_ — A [System.List](https://msdn.microsoft.com/library/6sh2ey19.aspx) object containing a list of SMTP email address strings.</span></span> 
    
-  <span data-ttu-id="00df0-121">_Factory_ : un objeto que implementa la interfaz **IAppointmentFactory** .</span><span class="sxs-lookup"><span data-stu-id="00df0-121">_factory_ — An object that implements the **IAppointmentFactory** interface.</span></span> <span data-ttu-id="00df0-122">Esta interfaz tiene un método, **GetAppointment** , que toma un objeto **ExchangeService** como parámetro y devuelve un objeto **appointment** .</span><span class="sxs-lookup"><span data-stu-id="00df0-122">This interface has one method, **GetAppointment** that takes an **ExchangeService** object as a parameter and returns an **Appointment** object.</span></span> <span data-ttu-id="00df0-123">La interfaz **IAppointmentFactory** está definida [IAppointmentFactory interfaz](#bk_IAppointmentFactory).</span><span class="sxs-lookup"><span data-stu-id="00df0-123">The **IAppointmentFactory** interface is defined [IAppointmentFactory interface](#bk_IAppointmentFactory).</span></span>
    
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

<span data-ttu-id="00df0-124">Al guardar la cita, el código comprueba si se ha agregado algún asistente a la propiedad [RequiredAttendees](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.requiredattendees.aspx) .</span><span class="sxs-lookup"><span data-stu-id="00df0-124">When saving the appointment, the code checks to determine whether any attendees have been added to the [RequiredAttendees](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.requiredattendees.aspx) property.</span></span> <span data-ttu-id="00df0-125">Si es así, se llama al método [appointment. Save](https://msdn.microsoft.com/library/dd635394.aspx) con el valor de enumeración [SendToAllAndSaveCopy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.sendinvitationsmode.aspx) para que los asistentes reciban las convocatorias de reunión; de lo contrario, se llama al método **appointment. Save** con el valor de enumeración [SendToNone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.sendinvitationsmode.aspx) para que la cita se guarde en el calendario del usuario suplantado con la propiedad [appointment. IsMeeting](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.ismeeting.aspx) establecida en **false**.</span><span class="sxs-lookup"><span data-stu-id="00df0-125">If they have, the [Appointment.Save](https://msdn.microsoft.com/library/dd635394.aspx) method is called with the [SendToAllAndSaveCopy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.sendinvitationsmode.aspx) enumeration value so that the attendees receive meeting requests; otherwise, the **Appointment.Save** method is called with the [SendToNone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.sendinvitationsmode.aspx) enumeration value so that the appointment is saved into the impersonated user's calendar with the [Appointment.IsMeeting](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.ismeeting.aspx) property set to **false**.</span></span>
  
### <a name="iappointmentfactory-interface"></a><span data-ttu-id="00df0-126">Interfaz IAppointmentFactory</span><span class="sxs-lookup"><span data-stu-id="00df0-126">IAppointmentFactory interface</span></span>
<span data-ttu-id="00df0-127"><a name="bk_IAppointmentFactory"> </a></span><span class="sxs-lookup"><span data-stu-id="00df0-127"><a name="bk_IAppointmentFactory"> </a></span></span>

<span data-ttu-id="00df0-128">Debido a que necesita un nuevo objeto **appointment** cada vez que desea guardar una cita en el calendario de un usuario suplantado, la interfaz **IAppointmentFactory** abstrae el objeto que se usa para rellenar cada objeto **appointment** .</span><span class="sxs-lookup"><span data-stu-id="00df0-128">Because you need a new **Appointment** object each time that you want to save an appointment on an impersonated user's calendar, the **IAppointmentFactory** interface abstracts the object used to populate each **Appointment** object.</span></span> <span data-ttu-id="00df0-129">Esta versión es una interfaz simple que contiene un solo método, **GetAppointment**, que toma un objeto **ExchangeService** como un parámetro y devuelve un nuevo objeto **appointment** enlazado a dicho objeto **ExchangeService** .</span><span class="sxs-lookup"><span data-stu-id="00df0-129">This version is a simple interface that contains only one method, **GetAppointment**, that takes an **ExchangeService** object as a parameter and returns a new **Appointment** object bound to that **ExchangeService** object.</span></span> 
  
```cs
interface IAppointmentFactory
{
  Appointment GetAppointment(ExchangeService service);
}
```

<span data-ttu-id="00df0-130">El siguiente ejemplo de clase **AppointmentFactory** muestra una implementación de la interfaz **IAppointmentFactory** que devuelve una cita sencilla que se produce tres días a partir de ahora.</span><span class="sxs-lookup"><span data-stu-id="00df0-130">The following **AppointmentFactory** class example shows an implementation of the **IAppointmentFactory** interface that returns a simple appointment that occurs three days from now.</span></span> <span data-ttu-id="00df0-131">Si quita la marca de comentario de la `appointment.RequiredAttendees.Add` línea, el método **GetAppointment** devolverá una reunión y la dirección de correo electrónico especificada en esa línea recibirá una convocatoria de reunión con el usuario suplantado que se muestra como organizador.</span><span class="sxs-lookup"><span data-stu-id="00df0-131">If you uncomment the  `appointment.RequiredAttendees.Add` line, the **GetAppointment** method will return a meeting and the email address specified in that line will receive a meeting request with the impersonated user listed as the organizer.</span></span> 
  
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

## <a name="add-appointments-by-using-impersonation-with-ews"></a><span data-ttu-id="00df0-132">Agregar citas mediante la suplantación con EWS</span><span class="sxs-lookup"><span data-stu-id="00df0-132">Add appointments by using impersonation with EWS</span></span>

<span data-ttu-id="00df0-133">EWS permite que la aplicación use la suplantación para agregar elementos a un calendario en nombre del propietario del calendario.</span><span class="sxs-lookup"><span data-stu-id="00df0-133">EWS enables you application to use impersonation to add items to a calendar on behalf the calendar's owner.</span></span> <span data-ttu-id="00df0-134">En este ejemplo se muestra cómo usar la operación [CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) para agregar una cita al calendario de una cuenta suplantada.</span><span class="sxs-lookup"><span data-stu-id="00df0-134">This example shows how to use the [CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) operation to add an appointment to the calendar of an impersonated account.</span></span> 
  
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

<span data-ttu-id="00df0-135">Tenga en cuenta que, aparte de la adición del elemento **ExchangeImpersonation** en el encabezado SOAP para especificar la cuenta que se va a suplantar, esta es la misma solicitud XML que se usa para crear una cita sin usar suplantación.</span><span class="sxs-lookup"><span data-stu-id="00df0-135">Note that other than the addition of the **ExchangeImpersonation** element in the SOAP header to specify the account that we are impersonating, this is the same XML request used to create an appointment without using impersonation.</span></span> 
  
<span data-ttu-id="00df0-136">En el ejemplo siguiente se muestra el XML de respuesta que devuelve la operación **CreateItem** .</span><span class="sxs-lookup"><span data-stu-id="00df0-136">The following example shows the response XML that is returned by the **CreateItem** operation.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="00df0-137">Los atributos **Itemid** y **changekey** se acortan para facilitar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="00df0-137">The **ItemId** and **ChangeKey** attributes are shortened for readability.</span></span> 
  
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

<span data-ttu-id="00df0-138">De nuevo, este es el mismo XML que se devuelve cuando se utiliza la operación **CreateItem** sin usar la suplantación.</span><span class="sxs-lookup"><span data-stu-id="00df0-138">Again, this is the same XML that is returned when you use the **CreateItem** operation without using impersonation.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="00df0-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="00df0-139">See also</span></span>


- [<span data-ttu-id="00df0-140">Suplantación y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="00df0-140">Impersonation and EWS in Exchange</span></span>](impersonation-and-ews-in-exchange.md)
    
- [<span data-ttu-id="00df0-141">Rol ApplicationImpersonation</span><span class="sxs-lookup"><span data-stu-id="00df0-141">ApplicationImpersonation role</span></span>](https://technet.microsoft.com/library/dd776119%28v=exchg.150%29.aspx)
    
- [<span data-ttu-id="00df0-142">Configurar la suplantación</span><span class="sxs-lookup"><span data-stu-id="00df0-142">Configure impersonation</span></span>](how-to-configure-impersonation.md)
    
- [<span data-ttu-id="00df0-143">Identificación de la cuenta que se va a suplantar</span><span class="sxs-lookup"><span data-stu-id="00df0-143">Identify the account to impersonate</span></span>](how-to-identify-the-account-to-impersonate.md)
    
- [<span data-ttu-id="00df0-144">Crear citas y reuniones mediante EWS en Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="00df0-144">Create appointments and meetings by using EWS in Exchange 2013</span></span>](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [<span data-ttu-id="00df0-145">Operación CreateItem (elemento de calendario)</span><span class="sxs-lookup"><span data-stu-id="00df0-145">CreateItem operation (calendar item)</span></span>](../web-service-reference/createitem-operation-calendar-item.md)
    
- [<span data-ttu-id="00df0-146">Propiedad ExchangeService. ImpersonatedUserId</span><span class="sxs-lookup"><span data-stu-id="00df0-146">ExchangeService.ImpersonatedUserId property</span></span>](https://docs.microsoft.com/dotnet/api/microsoft.exchange.webservices.data.exchangeservice.impersonateduserid?view=exchange-ews-api)
    

