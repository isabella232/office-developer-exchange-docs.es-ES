---
title: Obtener acceso a un calendario como delegado mediante EWS en Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.assetid: d7db4a1e-9ed6-41da-8529-a73ca285cdf2
description: Obtenga información sobre cómo obtener acceso a un calendario como delegado mediante la API administrada de EWS o EWS en Exchange.
localization_priority: Priority
ms.openlocfilehash: 20ec294ddc4ccf014f0b2148c786c8c3ef8a6069
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528296"
---
#  <a name="access-a-calendar-as-a-delegate-by-using-ews-in-exchange"></a>Obtener acceso a un calendario como delegado mediante EWS en Exchange

Obtenga información sobre cómo obtener acceso a un calendario como delegado mediante la API administrada de EWS o EWS en Exchange.
  
Puede usar la API administrada de EWS o EWS para conceder a un usuario acceso delegado a la carpeta de calendario de un propietario del buzón. A continuación, el delegado puede crear convocatorias de reunión en nombre del propietario del buzón, crear citas, responder a convocatorias de reunión y recuperar, actualizar y eliminar reuniones de la carpeta calendario del propietario del buzón, en función de sus permisos.
  
Como delegado, se usan los mismos métodos y operaciones para tener acceso a la carpeta Calendario de un propietario del buzón que se usa para tener acceso a su propia carpeta calendario. La principal diferencia es que tiene que usar el [acceso explícito](delegate-access-and-ews-in-exchange.md#bk_explicit) para buscar o crear un elemento de calendario o una subcarpeta de calendario y, después, después de identificar el identificador de elemento o la carpeta, puede usar el [acceso implícito](delegate-access-and-ews-in-exchange.md#bk_implicit) para obtener, actualizar o eliminar el elemento. 
  
**Tabla 1. Métodos de la API administrada de EWS y operaciones EWS para tener acceso a un calendario como delegado**

|**Si quiere...**|**Use este método de API administrada de EWS...**|**Usar esta operación de EWS...**|
|:-----|:-----|:-----|
|Crear una reunión o una cita como delegado  <br/> |[Appointment. Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) donde el parámetro [FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) proporciona [acceso explícito](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) a la carpeta de calendario del propietario del buzón de correo  <br/> |[CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) donde el elemento [Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) especifica el [EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) del propietario del buzón de correo  <br/> |
|Crear varias reuniones o citas como delegado  <br/> |[ExchangeService. CreateItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) donde el parámetro **FolderId** proporciona [acceso explícito](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) a la carpeta de calendario del propietario del buzón de correo  <br/> |[CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) donde el elemento [Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) especifica el [EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) del propietario del buzón de correo  <br/> |
|Buscar o buscar una cita o reunión como delegado  <br/> |[ExchangeService. FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) donde el parámetro **FolderId** proporciona [acceso explícito](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) a la carpeta de calendario del propietario del buzón de correo  <br/> |[FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) donde el elemento [Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) especifica el [EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) del propietario del buzón.  <br/> |
|Obtener una cita o reunión como delegado  <br/> |[Appointment. bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) <br/> |[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |
|Actualizar una cita o una reunión como delegado  <br/> |[Appointment. bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) seguido de [appointment. Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx) <br/> |[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) seguido de [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |
|Eliminar una cita o una reunión como delegado  <br/> |[Appointment. bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) seguido de [appointment. Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx) <br/> |[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) seguido de [DeleteItem](../web-service-reference/deleteitem-operation.md) <br/> |
   
> [!NOTE]
> En los ejemplos de código de este artículo, primary@contoso.com es el propietario del buzón. 
  
## <a name="prerequisite-tasks"></a>Tareas de requisitos previos
<a name="bk_prereq"> </a>

Para que un usuario pueda tener acceso a la carpeta del calendario de un propietario del buzón como delegado, el usuario debe [agregarse como delegado con permisos](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md) para la carpeta de calendario del propietario del buzón. 
  
Un delegado debe tener un buzón adjunto a su cuenta para actualizar el calendario de un propietario del buzón.
  
Si un delegado solo tiene que trabajar con convocatorias de reunión y respuestas, puede Agregar el delegado a la carpeta calendario y usar el valor predeterminado [MeetingRequestsDeliveryScope. DelegatesAndSendInformationToMe](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.meetingrequestsdeliveryscope%28v=exchg.80%29.aspx) de la enumeración de API administrada EWS o el valor [DeliverMeetingRequests](https://msdn.microsoft.com/library/04b999af-0b27-4e6d-a8b1-400955a1afaa%28Office.15%29.aspx) del elemento EWS de **DelegatesAndSendInformationToMe** para enviar las solicitudes al delegado y los mensajes informativos al propietario del buzón. A continuación, no es necesario dar acceso al delegado a la carpeta Bandeja de entrada del propietario del buzón. 
  
## <a name="create-a-meeting-or-appointment-as-a-delegate-by-using-the-ews-managed-api"></a>Crear una reunión o una cita como delegado mediante la API administrada de EWS
<a name="bk_createewsma"> </a>

La API administrada de EWS permite usar el objeto de servicio para que el usuario delegado cree elementos de calendario para el propietario del buzón. En este ejemplo se muestra cómo usar el método [Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) para crear una reunión y enviar las convocatorias de reunión a los asistentes. 
  
En este ejemplo se supone que el **servicio** es un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido para el delegado y que se han concedido al delegado los permisos adecuados para la carpeta de calendario del propietario del buzón. 
  
```cs
private static void DelegateAccessCreateMeeting(ExchangeService service)
{
    Appointment meeting = new Appointment(service);
    // Set the properties on the meeting object to create the meeting.
    meeting.Subject = "Team building exercise";
    meeting.Body = "Let's learn to really work as a team and then have lunch!";
    meeting.Start = DateTime.Now.AddDays(2);
    meeting.End = meeting.Start.AddHours(4);
    meeting.Location = "Conference Room 12";
    meeting.RequiredAttendees.Add("sadie@contoso.com");
    meeting.ReminderMinutesBeforeStart = 60;
    // Save the meeting to the Calendar folder for 
    // the mailbox owner and send the meeting request.
    // This method call results in a CreateItem call to EWS.
    meeting.Save(new FolderId(WellKnownFolderName.Calendar, 
        "primary@contoso.com"), 
        SendInvitationsMode.SendToAllAndSaveCopy);
    // Verify that the meeting was created.
    Item item = Item.Bind(service, meeting.Id, new PropertySet(ItemSchema.Subject));
    Console.WriteLine("\nMeeting created: " + item.Subject + "\n");
}
```

Tenga en cuenta que, al guardar el elemento, la llamada al método [Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) debe identificar la carpeta de calendario del propietario del buzón. Si no se especifica la carpeta calendario del propietario del buzón, la convocatoria de reunión se guarda en el calendario del delegado y no en la carpeta calendario del propietario del buzón. Puede incluir la carpeta de calendario del propietario del buzón de correo en la llamada al método **Save** de dos maneras. Se recomienda crear una instancia de una nueva instancia del objeto [FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) con el [WellKnownFolderName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) y la dirección SMTP del propietario del buzón. 
  
```cs
meeting.Save(new FolderId(WellKnownFolderName.Calendar,
    "primary@contoso.com"), SendInvitationsMode.SendToAllAndSaveCopy);
```

Sin embargo, también puede [enlazar](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) a la carpeta de calendario y, a continuación, usar el identificador de la carpeta en la llamada al método **Save** . Sin embargo, tenga en cuenta que esto crea una llamada a EWS adicional. 
  
```cs
    // Identify the mailbox owner's SMTP address
    // and bind to their Calendar folder.
    Mailbox primary = new Mailbox("primary@contoso.com"); 
    Folder primaryCalendar = Folder.Bind(service, 
        new FolderId(WellKnownFolderName.Calendar, primary)); 
…
    // Save the meeting to the Calendar folder for the mailbox owner and send the meeting request.
    meeting.Save(primaryCalendar.Id, 
        SendInvitationsMode.SendToAllAndSaveCopy);
```

## <a name="create-a-meeting-or-appointment-as-a-delegate-by-using-ews"></a>Crear una reunión o una cita como delegado mediante EWS
<a name="bk_createews"> </a>

EWS permite usar el objeto de servicio para que el usuario delegado cree elementos de calendario para el propietario del buzón. En este ejemplo se muestra cómo usar la operación [CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) para crear una reunión y enviar las convocatorias de reunión a los asistentes. 
  
También es la solicitud XML que la API administrada de EWS envía cuando se usa el método **Save** para [crear una reunión o cita como delegado](#bk_createewsma).
  
El encabezado SOAP se ha quitado del ejemplo siguiente por motivos de brevedad.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
         xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
         xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
…
  <soap:Body>
    <m:CreateItem SendMeetingInvitations="SendToAllAndSaveCopy">
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="calendar">
          <t:Mailbox>
            <t:EmailAddress>primary@contoso.com</t:EmailAddress>
          </t:Mailbox>
        </t:DistinguishedFolderId>
      </m:SavedItemFolderId>
      <m:Items>
        <t:CalendarItem>
          <t:Subject>Team building exercise</t:Subject>
          <t:Body BodyType="HTML">Let's learn to really work as a 
              team and then have lunch!</t:Body>
          <t:ReminderMinutesBeforeStart>60</t:ReminderMinutesBeforeStart>
          <t:Start>2014-03-09T23:26:33.756-05:00</t:Start>
          <t:End>2014-03-10T03:26:33.756-05:00</t:End>
          <t:Location>Conference Room 12</t:Location>
          <t:RequiredAttendees>
            <t:Attendee>
              <t:Mailbox>
                <t:EmailAddress>sadie@contoso.com</t:EmailAddress>
              </t:Mailbox>
            </t:Attendee>
          </t:RequiredAttendees>
        </t:CalendarItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>

```

El servidor responde a la solicitud **CreateItem** con un mensaje [CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) que incluye un valor de elemento [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, que indica que la reunión se ha creado correctamente. La respuesta también contiene el identificador de elemento de la reunión recién creada.
  
## <a name="search-for-a-meeting-or-appointment-as-a-delegate-by-using-the-ews-managed-api"></a>Buscar una reunión o una cita como delegado mediante la API administrada de EWS
<a name="bk_searchewsma"> </a>

Para buscar una reunión, debe usar uno de los métodos [ExchangeService. FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) que incluya un parámetro [FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) , de modo que pueda especificar la carpeta de calendario del propietario del buzón. 
  
```cs
static void DelegateAccessSearchWithFilter
    (ExchangeService service, SearchFilter filter)
{
    // Limit the result set to 10 items.
    ItemView view = new ItemView(10);
    view.PropertySet = new PropertySet(ItemSchema.Subject,
                                       ItemSchema.DateTimeReceived,
                                       EmailMessageSchema.IsRead);
    // Item searches do not support deep traversal.
    view.Traversal = ItemTraversal.Shallow;
    // Define the sort order.
    view.OrderBy.Add(ItemSchema.DateTimeReceived, SortDirection.Descending);
    try
    {
        // Call FindItems to find matching calendar items. 
        // The FindItems parameters must denote the mailbox owner,
        // mailbox, and Calendar folder.
        // This method call results in a FindItem call to EWS.
        FindItemsResults<Item> results = service.FindItems(
        new FolderId(WellKnownFolderName.Calendar, 
            "primary@contoso.com"), 
            filter, 
            view);
        foreach (Item item in results.Items)
        {
            Console.WriteLine("Subject: {0}", item.Subject);
            Console.WriteLine("Id: {0}", item.Id.ToString());
        }
    }
    catch (Exception ex)
    {
        Console.WriteLine("Exception while 
            enumerating results: {0}", ex.Message);
    }
}
```

Una vez que la llamada de **FindItems** devuelve una respuesta con un identificador, puede obtener, actualizar o eliminar esa reunión con el identificador y el [acceso implícito](delegate-access-and-ews-in-exchange.md#bk_implicit) , y no es necesario especificar la dirección SMTP del propietario del buzón. 
  
## <a name="search-for-a-meeting-or-appointment-as-a-delegate-by-using-ews"></a>Buscar una reunión o una cita como delegado mediante EWS
<a name="bk_searchews"> </a>

EWS permite usar el objeto de servicio para que el usuario delegado busque citas y reuniones que cumplan un conjunto de criterios de búsqueda. En este ejemplo se muestra cómo usar la operación [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) para buscar reuniones en la carpeta calendario del propietario del buzón que contengan la palabra "Building" en el asunto. 
  
También es la solicitud XML que la API administrada de EWS envía cuando se usa el método **FindItem** para [buscar una reunión o cita como delegado](#bk_searchewsma).
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:FindItem Traversal="Shallow">
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
          <t:FieldURI FieldURI="item:DateTimeReceived" />
          <t:FieldURI FieldURI="message:IsRead" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:IndexedPageItemView MaxEntriesReturned="10"
                             Offset="0"
                             BasePoint="Beginning" />
      <m:Restriction>
        <t:Contains ContainmentMode="Substring"
                    ContainmentComparison="IgnoreCase">
          <t:FieldURI FieldURI="item:Subject" />
          <t:Constant Value="building" />
        </t:Contains>
      </m:Restriction>
      <m:SortOrder>
        <t:FieldOrder Order="Descending">
          <t:FieldURI FieldURI="item:DateTimeReceived" />
        </t:FieldOrder>
      </m:SortOrder>
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="calendar">
          <t:Mailbox>
            <t:EmailAddress>primary@contoso.com</t:EmailAddress>
          </t:Mailbox>
        </t:DistinguishedFolderId>
      </m:ParentFolderIds>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

El servidor responde a la solicitud **FindItem** con un mensaje [FindItemResponse](https://msdn.microsoft.com/library/c8b316df-d4ab-49b8-96d4-8e9a016730ef%28Office.15%29.aspx) que incluye un valor de elemento [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, lo que indica que la búsqueda se ha completado correctamente. La respuesta contiene un [CalendarItem](https://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) para las citas o reuniones que cumplen los criterios de búsqueda. En este caso, solo se encuentra una reunión. 
  
El valor del elemento [Itemid](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) se ha abreviado para facilitar su lectura. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="893"
                         MinorBuildNumber="10"
                         Version="V2_10"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body>
    <m:FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="1"
                        TotalItemsInView="1"
                        IncludesLastItemInRange="true">
            <t:Items>
              <t:CalendarItem>
                <t:ItemId Id="IJpUAAA="
                          ChangeKey="DwAAABYAAADOilbYa8KaT7ZgMoTz2P+hAAAAIKhS" />
                <t:Subject>Team building exercise</t:Subject>
                <t:DateTimeReceived>2014-03-04T21:27:22Z</t:DateTimeReceived>
              </t:CalendarItem>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>
```

Ahora que tiene el **Itemid** para la reunión que cumple con los criterios, puede obtener, actualizar o eliminar esa reunión mediante el uso de **Itemid** y el [acceso implícito](delegate-access-and-ews-in-exchange.md#bk_implicit) , y no es necesario especificar la dirección SMTP del propietario del buzón. 
  
## <a name="get-update-or-delete-calendar-items-as-a-delegate-by-using-the-ews-managed-api"></a>Obtener, actualizar o eliminar elementos de calendario como delegado mediante la API administrada de EWS
<a name="bk_geteswma"> </a>

Puede usar la API administrada de EWS para obtener, actualizar o eliminar una reunión o cita de la misma manera en que realiza estas acciones cuando no usa el acceso de delegado. La única diferencia es que el objeto de servicio es para el usuario delegado. El identificador de elemento incluido en la llamada al método **BIND** identifica de forma única el elemento en el almacén de buzones, en la carpeta calendario del propietario del buzón. 
  
**Tabla 2. Métodos de la API administrada de EWS para trabajar con citas y reuniones como delegado**

|**Tarea**|**Método de la API administrada de EWS**|**Ejemplo de código**|
|:-----|:-----|:-----|
|Obtener una cita o una reunión  <br/> |[BIND](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) <br/> |[Obtener un elemento mediante la API administrada de EWS](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getewsma) <br/> |
|Actualizar una cita o una reunión  <br/> |[Enlazar](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) seguido de [Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx) <br/> |[Actualizar una reunión mediante la API administrada de EWS](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md#bk_UpdateMtgEWSMA) <br/> |
|Eliminar una cita o una reunión  <br/> |[Enlazar](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) seguida de [eliminar](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx) <br/> |[Eliminar una reunión mediante la API administrada de EWS](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md#bk_DeleteMtgEWSMA) <br/> |
   
## <a name="get-update-or-delete-calendar-items-as-a-delegate-by-using-ews"></a>Obtener, actualizar o eliminar elementos de calendario como delegado mediante EWS
<a name="bk_getews"> </a>

Puede usar EWS para obtener, actualizar o eliminar una reunión o cita de la misma manera en que realiza estas acciones cuando no está usando acceso delegado. La única diferencia es que el objeto de servicio es para el usuario delegado. El identificador de elemento incluido en la llamada al método [GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) identifica de forma única el elemento en el almacén de buzones, en la carpeta calendario del propietario del buzón. 
  
**Tabla 3. Operaciones de EWS para trabajar con citas y reuniones como delegado**

|**Tarea**|**Operación de EWS**|**Ejemplo de código**|
|:-----|:-----|:-----|
|Obtener una cita o una reunión  <br/> |[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |[Obtener un elemento mediante EWS](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getews) <br/> |
|Actualizar una cita o una reunión  <br/> |[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) seguido de [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |[Actualizar una reunión con EWS](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md#bk_UpdateMtgEWS) <br/> |
|Eliminar una cita o una reunión  <br/> |[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) seguido de [DeleteItem](../web-service-reference/deleteitem-operation.md) <br/> |[](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md#bk_DeleteMtgEWSMA) <br/> |
   
## <a name="see-also"></a>Vea también

- [Acceso delegado y EWS en Exchange](delegate-access-and-ews-in-exchange.md)   
- [Agregar y quitar delegados mediante EWS en Exchange](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md)
- [Establecer los permisos de carpeta para otro usuario mediante EWS en Exchange](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md) 
- [Calendarios y EWS en Exchange](calendars-and-ews-in-exchange.md)
    

