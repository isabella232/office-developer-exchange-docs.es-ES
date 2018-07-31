---
title: Obtener acceso a un calendario como delegado mediante el uso de EWS en Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: d7db4a1e-9ed6-41da-8529-a73ca285cdf2
description: Obtenga información sobre cómo obtener acceso a un calendario como delegado mediante la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: 609e5f0bb22c78174289a2eb10210999c8391a3d
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353843"
---
#  <a name="access-a-calendar-as-a-delegate-by-using-ews-in-exchange"></a>Obtener acceso a un calendario como delegado mediante el uso de EWS en Exchange

Obtenga información sobre cómo obtener acceso a un calendario como delegado mediante la API administrada de EWS o EWS en Exchange.
  
Puede usar la API administrada de EWS o EWS para dar a un usuario delegar el acceso a la carpeta del calendario del propietario del buzón. El delegado puede, a continuación, crear convocatorias de reunión en nombre del propietario del buzón de correo, crear citas, responder a las convocatorias de reunión y recuperar, actualizar y eliminar las reuniones de la carpeta del calendario del propietario del buzón, en función de sus permisos.
  
Como delegado, use los mismos métodos y operaciones para tener acceso a la carpeta de calendario de un propietario buzón de correo que use para tener acceso a su propia carpeta de calendario. La diferencia principal es que se debe usar [acceso explícito](delegate-access-and-ews-in-exchange.md#bk_explicit) para buscar o crear un elemento de calendario o una subcarpeta de calendario y, a continuación, después de identificar el identificador de elemento o carpeta, puede usar [acceso implícito](delegate-access-and-ews-in-exchange.md#bk_implicit) para obtener, actualizar o eliminar el elemento. 
  
**La tabla 1. Métodos de la API administrada de EWS y las operaciones de EWS para obtener acceso a un calendario como delegado**

|**Si quiere...**|**Use este método de la API administrada de EWS...**|**Use esta operación de EWS...**|
|:-----|:-----|:-----|
|Crear una reunión o cita como delegado  <br/> |[Appointment.Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) donde el parámetro [FolderId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) proporciona [acceso explícito](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) a la carpeta del calendario del propietario del buzón  <br/> |[CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) donde el elemento de [buzón de correo](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) especifica la [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) del propietario del buzón  <br/> |
|Crear varias reuniones o citas como delegado  <br/> |[ExchangeService.CreateItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) donde el parámetro **FolderId** proporciona [acceso explícito](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) a la carpeta del calendario del propietario del buzón  <br/> |[CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) donde el elemento de [buzón de correo](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) especifica la [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) del propietario del buzón  <br/> |
|Buscar o buscar una cita o reunión como delegado  <br/> |[ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) donde el parámetro **FolderId** proporciona [acceso explícito](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) a la carpeta del calendario del propietario del buzón  <br/> |[FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) donde el elemento de [buzón de correo](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) especifica la [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) del propietario del buzón  <br/> |
|Obtener una cita o reunión como delegado  <br/> |[Appointment.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) <br/> |[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |
|Actualización de una cita o reunión como delegado  <br/> |[Appointment.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) seguido de [Appointment.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx) <br/> |[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) seguido [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |
|Eliminación de una cita o reunión como delegado  <br/> |[Appointment.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) seguido de [Appointment.Delete](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx) <br/> |[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) seguido [DeleteItem](../web-service-reference/deleteitem-operation.md) <br/> |
   
> [!NOTE]
> En los ejemplos de código de este artículo, primary@contoso.com es el propietario del buzón. 
  
## <a name="prerequisite-tasks"></a>Tareas de requisitos previos
<a name="bk_prereq"> </a>

Antes de que un usuario puede obtener acceso a la carpeta de calendario de un propietario buzón de correo como delegado, el usuario debe ser [agregado como delegado con permisos](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md) para la carpeta del calendario del propietario del buzón. 
  
Un delegado debe tener un buzón vinculado a su cuenta para actualizar el calendario de un propietario del buzón.
  
Si un delegado necesita para trabajar con convocatorias de reunión y las respuestas sólo, se puede agregar al delegado a la carpeta Calendario y usar el valor de enumeración de API administrada de EWS de [MeetingRequestsDeliveryScope.DelegatesAndSendInformationToMe](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.meetingrequestsdeliveryscope%28v=exchg.80%29.aspx) predeterminado o la [ DeliverMeetingRequests](http://msdn.microsoft.com/library/04b999af-0b27-4e6d-a8b1-400955a1afaa%28Office.15%29.aspx) valor de elemento EWS de **DelegatesAndSendInformationToMe** para enviar las solicitudes al delegado y los mensajes informativos al propietario del buzón. A continuación, el delegado no necesita tener acceso a la carpeta de bandeja de entrada del propietario del buzón. 
  
## <a name="create-a-meeting-or-appointment-as-a-delegate-by-using-the-ews-managed-api"></a>Crear una reunión o cita como delegado mediante el uso de la API administrada de EWS
<a name="bk_createewsma"> </a>

La API administrada de EWS le permite usar el objeto de servicio para el usuario delegado para crear elementos de calendario para el propietario del buzón. En este ejemplo se muestra cómo utilizar el método [Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) para crear una reunión y enviar convocatorias de reunión a los asistentes. 
  
En este ejemplo se da por supuesto que **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido para el delegado y que el delegado se ha concedido los permisos adecuados para la carpeta del calendario del propietario del buzón. 
  
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

Tenga en cuenta que cuando se guarda el elemento, la llamada al método [Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) debe identificar carpeta del calendario del propietario del buzón. Si no se especifica la carpeta del calendario del propietario del buzón, la convocatoria de reunión obtiene guardan en el calendario del delegado y no la carpeta de calendario del propietario del buzón. Puede incluir la carpeta del calendario del propietario del buzón en la llamada al método **Guardar** de dos maneras. Se recomienda que se cree una instancia de una nueva instancia del objeto [FolderId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) mediante el uso de la [WellKnownFolderName](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) y la dirección SMTP del propietario del buzón. 
  
```cs
meeting.Save(new FolderId(WellKnownFolderName.Calendar,
    "primary@contoso.com"), SendInvitationsMode.SendToAllAndSaveCopy);
```

Sin embargo, también puede [enlazar](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) a la carpeta Calendario en primer lugar y, a continuación, use el identificador de la carpeta en la llamada al método **Save** . Tenga en cuenta, sin embargo, esto crea una llamada EWS adicional. 
  
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

## <a name="create-a-meeting-or-appointment-as-a-delegate-by-using-ews"></a>Crear una reunión o cita como delegado mediante el uso de EWS
<a name="bk_createews"> </a>

EWS le permite usar el objeto de servicio para el usuario delegado para crear elementos de calendario para el propietario del buzón. En este ejemplo se muestra cómo usar la operación [CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) para crear una reunión y enviar convocatorias de reunión a los asistentes. 
  
También es la solicitud XML que la API administrada de EWS envía cuando se utiliza el método **Save** para [crear una reunión o cita como delegado](#bk_createewsma).
  
El encabezado SOAP se ha quitado el siguiente ejemplo para mayor brevedad.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
         xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
         xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

El servidor responde a la solicitud **CreateItem** con un mensaje de [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) que incluye un valor de elemento [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, lo que indica que la reunión se ha creado correctamente. La respuesta también contiene el identificador de elemento de la reunión recién creado.
  
## <a name="search-for-a-meeting-or-appointment-as-a-delegate-by-using-the-ews-managed-api"></a>Búsqueda de una reunión o cita como delegado mediante el uso de la API administrada de EWS
<a name="bk_searchewsma"> </a>

Para buscar una reunión, debe usar uno de los métodos de [ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) que incluya un parámetro [FolderId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) , por lo que puede especificar la carpeta del calendario del propietario del buzón. 
  
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

Después de la llamada **FindItems** devuelve una respuesta con el identificador, puede obtener, actualizar o eliminar dicha reunión mediante el identificador y el [acceso implícito](delegate-access-and-ews-in-exchange.md#bk_implicit) , y no es necesario especificar la dirección de SMTP del propietario del buzón. 
  
## <a name="search-for-a-meeting-or-appointment-as-a-delegate-by-using-ews"></a>Búsqueda de una reunión o cita como delegado mediante el uso de EWS
<a name="bk_searchews"> </a>

EWS le permite usar el objeto de servicio para el usuario delegado para buscar las citas y reuniones que cumplen un conjunto de criterios de búsqueda. En este ejemplo se muestra cómo usar la operación [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) para buscar las reuniones en la carpeta del calendario del propietario del buzón que contengan la palabra "building" en el asunto. 
  
También es la solicitud XML que la API administrada de EWS envía cuando se utiliza el método **FindItem** a la [búsqueda de una reunión o cita como delegado](#bk_searchewsma).
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

El servidor responde a la solicitud de **FindItem** con un mensaje de [FindItemResponse](http://msdn.microsoft.com/library/c8b316df-d4ab-49b8-96d4-8e9a016730ef%28Office.15%29.aspx) que incluye un valor de elemento [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, lo que indica que la búsqueda que se realizó correctamente. La respuesta contiene un [CalendarItem](http://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) para cualquier citas o reuniones que cumplen los criterios de búsqueda. En este caso, se ha encontrado sólo una de las reuniones. 
  
El valor del elemento [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) se ha acortado para mejorar la legibilidad. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="893"
                         MinorBuildNumber="10"
                         Version="V2_10"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body>
    <m:FindItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

Ahora que tiene la **ItemId** para la reunión que cumpla los criterios, obtener, actualizar o eliminar dicha reunión mediante el [acceso implícito](delegate-access-and-ews-in-exchange.md#bk_implicit) y **ItemId** , y no es necesario especificar la dirección de SMTP del propietario del buzón. 
  
## <a name="get-update-or-delete-calendar-items-as-a-delegate-by-using-the-ews-managed-api"></a>Obtener, actualizar o eliminar elementos de calendario como delegado mediante el uso de la API administrada de EWS
<a name="bk_geteswma"> </a>

Puede usar la API administrada de EWS para obtener, actualizar o eliminar una reunión o una cita de la misma manera que se realizan estas acciones cuando no está utilizando acceso delegado. La única diferencia es que el objeto de servicio para el usuario delegado. El identificador de elemento incluido en la llamada al método **enlazar** de forma única identifica el elemento en el almacén de buzón de correo, en la carpeta del calendario del propietario del buzón. 
  
**Tabla 2. Métodos de la API administrada de EWS para trabajar con las citas y reuniones como delegado**

|**Tarea**|**Método de la API administrada de EWS**|**Code example**|
|:-----|:-----|:-----|
|Obtener una cita o reunión  <br/> |[Enlazar](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) <br/> |[Obtener un elemento mediante el uso de la API administrada de EWS](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getewsma) <br/> |
|Actualización de una cita o reunión  <br/> |[Enlazar](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) seguido de [actualización](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx) <br/> |[Actualización de una reunión mediante el uso de la API administrada de EWS](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md#bk_UpdateMtgEWSMA) <br/> |
|Eliminar una reunión o cita  <br/> |[Enlazar](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) seguido de [Eliminar](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx) <br/> |[Eliminar una reunión mediante el uso de la API administrada de EWS](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md#bk_DeleteMtgEWSMA) <br/> |
   
## <a name="get-update-or-delete-calendar-items-as-a-delegate-by-using-ews"></a>Obtener, actualizar o eliminar elementos de calendario como delegado mediante el uso de EWS
<a name="bk_getews"> </a>

Puede usar EWS para obtener, actualizar o eliminar una reunión o una cita de la misma manera que se realizan estas acciones cuando no está utilizando acceso delegado. La única diferencia es que el objeto de servicio para el usuario delegado. El identificador de elemento incluido en la llamada al método [GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) identifica de forma exclusiva identifica el elemento en el almacén de buzón de correo, en la carpeta del calendario del propietario del buzón. 
  
**Tabla 3. Operaciones de EWS para trabajar con las citas y reuniones como delegado**

|**Tarea**|**Operación de EWS**|**Code example**|
|:-----|:-----|:-----|
|Obtener una cita o reunión  <br/> |[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |[Obtener un elemento mediante el uso de EWS](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getews) <br/> |
|Actualización de una cita o reunión  <br/> |[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) seguido [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |[Actualización de una reunión mediante el uso de EWS](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md#bk_UpdateMtgEWS) <br/> |
|Eliminar una reunión o cita  <br/> |[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) seguido [DeleteItem](../web-service-reference/deleteitem-operation.md) <br/> |[](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md#bk_DeleteMtgEWSMA) <br/> |
   
## <a name="see-also"></a>Vea también

- [Acceso delegado y EWS en Exchange](delegate-access-and-ews-in-exchange.md)   
- [Agregar y quitar delegados mediante EWS en Exchange](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md)
- [Establecer permisos de carpeta de otro usuario mediante el uso de EWS en Exchange](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md) 
- [Calendarios y EWS en Exchange](calendars-and-ews-in-exchange.md)
    

