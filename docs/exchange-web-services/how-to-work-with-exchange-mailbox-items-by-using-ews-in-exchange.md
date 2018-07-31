---
title: Trabajar con los elementos del buzón de Exchange mediante EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 721deb84-f85d-45d0-84c1-0ed55f359969
description: Obtenga información sobre cómo crear, obtener, actualizar y eliminar elementos mediante la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: a40cd7ae682c1fb0a8d2f9cfcb10d99d4ab08052
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353969"
---
# <a name="work-with-exchange-mailbox-items-by-using-ews-in-exchange"></a>Trabajar con los elementos del buzón de Exchange mediante EWS en Exchange

Obtenga información sobre cómo crear, obtener, actualizar y eliminar elementos mediante la API administrada de EWS o EWS en Exchange.
  
Puede usar la API administrada de EWS o EWS para trabajar con elementos de un buzón de correo. Puede usar los elementos genéricos: objetos de [elemento](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) de API administrada de EWS o tipos de [elemento](http://msdn.microsoft.com/library/4dfe8f48-e7b4-444d-bdf9-a34e180f598b%28Office.15%29.aspx) EWS: para realizar algunas operaciones (obtención de un elemento o eliminación de un elemento con el identificador del elemento); Sin embargo, la mayor parte de la hora en que tendrá que usar un [elemento con establecimiento inflexible de tipos](folders-and-items-in-ews-in-exchange.md#bk_item) para llevar a cabo una operación get o la operación de actualización debido a que tendrá acceso a las propiedades que son específicas para el elemento fuertemente tipado. 

Por ejemplo, no puede usar un elemento genérico para recuperar un elemento que contiene un inicio y fecha de finalización: necesita un objeto de la API administrada de EWS [cita](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) o un tipo de EWS [CalendarItem](http://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) para hacerlo. Y si se usa la API administrada de EWS, siempre debe crear elementos fuertemente tipados, porque la clase de **elemento** genérica no tiene un constructor. Si está trabajando con un elemento que no está fuertemente tipado, siempre puede usar la clase de **elemento** base para trabajar con el elemento. 
  
**La tabla 1. Métodos de la API administrada de EWS y las operaciones de EWS para trabajar con elementos**

|**Con el fin...**|**Método de la API administrada de EWS**|**Operación de EWS**|
|:-----|:-----|:-----|
|Crear un elemento genérico  <br/> |Ninguno. Sólo se pueden crear tipos de elemento específico mediante el uso de la API administrada de EWS; no se puede crear los elementos genéricos.  <br/> |[CreateItem](http://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) <br/> |
|Obtener un elemento  <br/> |[Item.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) <br/> |[GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/> |
|Actualizar un elemento  <br/> |[Item.Update](http://msdn.microsoft.com/en-us/library/office/dd635915%28v=exchg.80%29.aspx) <br/> |[UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |
|Eliminar un elemento  <br/> |[Item.Delete](http://msdn.microsoft.com/en-us/library/office/dd635072%28v=exchg.80%29.aspx) <br/> |[DeleteItem](../web-service-reference/deleteitem-operation.md) <br/> |
   
En este artículo, aprenderá cuándo se puede utilizar la clase base genérica y cuándo debe utilizar un elemento fuertemente tipado para llevar a cabo su tarea. Los ejemplos de código muestran cómo usar la clase base y qué hacer cuando no se puede usar la clase base o no ajuste a sus necesidades.
  
## <a name="create-an-item-by-using-the-ews-managed-api"></a>Crear un elemento mediante el uso de la API administrada de EWS
<a name="bk_createewsma"> </a>

La API administrada de EWS no tiene un constructor públicamente disponible para la clase de [elemento](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) , por lo que debe usar el constructor para el tipo de elemento específico que desea crear con el fin de crear un elemento. Por ejemplo, use el [constructor de la clase EmailMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.emailmessage%28v=exchg.80%29.aspx) para crear un nuevo mensaje de correo electrónico y [póngase en contacto con el constructor de clase](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx) para crear un nuevo contacto. Del mismo modo, el servidor nunca devuelve objetos de **elemento** genéricos de respuestas; todos los elementos genéricos se devuelven como objetos **EmailMessage** . 
  
Cuando conoce el tipo de elemento que se va a crear, puede completar la tarea en unos cuantos pasos. Los pasos son similares para todos los tipos de elemento:
  
1. Inicializar una nueva instancia de una de las clases de [elemento](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) con el objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) como un parámetro. 
    
2. Establecer propiedades en el elemento. Los esquemas son diferentes para cada tipo de elemento, por lo que distintas propiedades están disponibles para elementos diferentes.
    
3. Guardar el elemento, o guardar y enviar el elemento.
    
Por ejemplo, puede crear un objeto [EmailMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) , establezca las propiedades de [ToRecipients](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.torecipients%28v=exchg.80%29.aspx) , el [cuerpo](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.body%28v=exchg.80%29.aspx)y el [asunto](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.subject%28v=exchg.80%29.aspx)y, a continuación, enviarlo mediante el método [EmailMessage.SendAndSaveCopy](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx) . 
  
```cs
// Create an email message and provide it with connection 
// configuration information by using an ExchangeService object named service.
EmailMessage message = new EmailMessage(service);
// Set properties on the email message.
message.Subject = "Company Soccer Team";
message.Body = "Are you interested in joining?";
message.ToRecipients.Add("sadie@contoso.com");
// Send the email message and save a copy.
// This method call results in a CreateItem call to EWS.
message.SendAndSaveCopy();
```

Para obtener información sobre cómo crear un elemento de cita o reunión mediante el uso de la API administrada de EWS, consulte [crear citas y reuniones mediante el uso de EWS en Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md).
  
## <a name="create-an-item-by-using-ews"></a>Crear un elemento mediante el uso de EWS
<a name="bk_createews"> </a>

Puede crear un elemento genérico o un elemento fuertemente tipado mediante el uso de EWS. Los pasos son similares para todos los tipos de elemento:
  
1. Use la operación [CreateItem](http://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) para crear un elemento en el almacén de Exchange. 
    
2. Use el elemento de [los elementos](http://msdn.microsoft.com/library/0811a73e-bf1f-4889-9219-73902dd47639%28Office.15%29.aspx) que contienen uno o más elementos para crear. 
    
3. Establecer propiedades en el elemento.
    
Por ejemplo, puede crear un mensaje de correo electrónico y enviar mediante el código en el siguiente ejemplo. También es la solicitud XML que la API administrada de EWS envía cuando se llama al método [SendAndSaveCopy](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx) . 
  
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
    <m:CreateItem MessageDisposition="SendAndSaveCopy">
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="sentitems" />
      </m:SavedItemFolderId>
      <m:Items>
        <t:Message>
          <t:Subject>Company Soccer Team</t:Subject>
          <t:Body BodyType="HTML">Are you interested in joining?</t:Body>
          <t:ToRecipients>
            <t:Mailbox>
              <t:EmailAddress>sadie@contoso.com </t:EmailAddress>
              </t:Mailbox>
          </t:ToRecipients>
        </t:Message>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

El servidor responde a la solicitud **CreateItem** con un mensaje de [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) que incluye un valor [ResponseCode](http://msdn.microsoft.com/en-us/library/aa580757%28v=exchg.150%29.aspx) **NoError**, lo que indica que el correo electrónico se ha creado correctamente y la [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) de la recientemente mensaje de creación. 
  
Para obtener información sobre cómo crear un elemento de cita o reunión mediante el uso de EWS, consulte [crear citas y reuniones mediante el uso de EWS en Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md).
  
## <a name="get-an-item-by-using-the-ews-managed-api"></a>Obtener un elemento mediante el uso de la API administrada de EWS
<a name="bk_getewsma"> </a>

Para usar la API administrada de EWS para obtener un elemento si conoce el [Item.Id](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) del elemento para recuperar, simplemente llama a uno de los métodos de [enlace](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) en el elemento y el elemento se recuperará. Como procedimiento recomendado, se recomienda limitar las propiedades devueltas a aquellos que son necesarios. En este ejemplo se devuelve la propiedad de **identificador** de elemento y la propiedad **Subject** . 
  
En este ejemplo se da por supuesto que **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que se ha autenticado el usuario a un servidor de Exchange. La variable local *itemId* es el [identificador](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) del elemento que se debe actualizar. 
  
```cs
// As a best practice, limit the properties returned to only those that are required.
PropertySet propSet = new PropertySet(BasePropertySet.IdOnly, ItemSchema.Subject);
// Bind to the existing item by using the ItemId.
// This method call results in a GetItem call to EWS.
Item item = Item.Bind(service, itemId, propSet);

```

Si está buscando un elemento que cumple determinados criterios, realice lo siguiente:
  
1. Enlazar a la carpeta que contiene los elementos que desea obtener.
    
2. Crear una instancia de un [SearchFilter.SearchFilterCollection](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.searchfiltercollection%28v=exchg.80%29.aspx) o un [PropertySet](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.propertyset%28v=exchg.80%29.aspx) para filtrar los elementos para devolver. 
    
3. Crear una instancia de un objeto [CalendarView](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.calendarview%28v=exchg.80%29.aspx) o de [artículoVer](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemview%28v=EXCHG.80%29.aspx) para especificar el número de elementos para devolver. 
    
4. Llame al método [ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) o [ExchangeService.FindAppointments](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx) . 
    
Por ejemplo, si desea recuperar los mensajes de correo electrónico no leído en la Bandeja de entrada, use el código en el siguiente ejemplo. En este ejemplo se usa un **SearchFilterCollection** para limitar los resultados del método **FindItems** a los mensajes no leídos y se limita el **artículoVer** para limitar los resultados a un elemento. Este código determinado sólo funciona en objetos [EmailMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) debido a que el valor de [EmailMessageSchema.IsRead](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessageschema.isread%28v=exchg.80%29.aspx) es parte de la **SearchFilter**. 
  
```cs
// Bind the Inbox folder to the service object.
Folder inbox = Folder.Bind(service, WellKnownFolderName.Inbox);
// The search filter to get unread email.
SearchFilter sf = new SearchFilter.SearchFilterCollection(LogicalOperator.And, new SearchFilter.IsEqualTo(EmailMessageSchema.IsRead, false));
ItemView view = new ItemView(1);
// Fire the query for the unread items.
// This method call results in a FindItem call to EWS.
FindItemsResults<Item> findResults = service.FindItems(WellKnownFolderName.Inbox, sf, view);
```

Como alternativa, puede usar un [PropertySet](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) para limitar los resultados de la búsqueda, tal como se muestra en el siguiente ejemplo de código. En este ejemplo se usa el método [FindAppointments](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx) para recuperar hasta cinco las citas que se producen en los próximos 30 días. Evidentemente este código sólo funciona en los elementos del calendario. 
  
```cs
// Initialize values for the start and end times, and the number of appointments to retrieve.
DateTime startDate = DateTime.Now;
DateTime endDate = startDate.AddDays(30);
const int NUM_APPTS = 5;
// Bind the Calendar folder to the service object.
// This method call results in a GetFolder call to EWS.
CalendarFolder calendar = CalendarFolder.Bind(service, WellKnownFolderName.Calendar, new PropertySet());
// Set the start and end time and number of appointments to retrieve.
CalendarView cView = new CalendarView(startDate, endDate, NUM_APPTS);
// Limit the properties returned to the appointment's subject, start time, and end time.
cView.PropertySet = new PropertySet(AppointmentSchema.Subject, AppointmentSchema.Start, AppointmentSchema.End);
// Retrieve a collection of appointments by using the calendar view.
// This method call results in a FindAppointments call to EWS.
FindItemsResults<Appointment> appointments = calendar.FindAppointments(cView);
```

Tenga en cuenta que la información del servidor se devuelve en la respuesta de método **enlazar** es diferente de la información que el servidor devuelve una respuesta de método **FindItem** o **FindAppointment** . El método **Bind** puede devolver todas las propiedades esquematizadas, mientras que los métodos **FindItem** y **FindAppointment** no devuelven todas las propiedades esquematizadas. Por lo que si necesita acceso total al elemento, debe usar el método **Bind** . Si no tiene el elemento **Id** del elemento que le gustaría recuperar, use los métodos **FindItem** o **FindAppointment** para recuperar el identificador y, a continuación, utilice el método **Bind** para recuperar las propiedades que necesita. 
  
Para obtener información sobre cómo obtener un elemento de cita o reunión mediante el uso de la API administrada de EWS, vea [obtener las citas y reuniones mediante el uso de EWS en Exchange](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md).
  
## <a name="get-an-item-by-using-ews"></a>Obtener un elemento mediante el uso de EWS
<a name="bk_getews"> </a>

Si conoce el [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) del elemento para recuperar, puede obtener el elemento mediante la operación [GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) . 
  
En el ejemplo siguiente se muestra la solicitud XML para obtener el [asunto](http://msdn.microsoft.com/library/c140d6c2-deb1-4f67-a908-9397197c4ae7%28Office.15%29.aspx) de un elemento con un determinado **ItemId**. También es la solicitud XML que la API administrada de EWS envía al llamar al método [enlazar](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) en un **ItemId**. Los valores de algunos elementos y atributos se han abreviado para mejorar la legibilidad.
  
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
    <m:GetItem>
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:ItemIds>
        <t:ItemId Id="GJc/NAAA=" />
      </m:ItemIds>
    </m:GetItem>
  </soap:Body>
</soap:Envelope>
```

En el ejemplo siguiente se muestra la respuesta XML que el servidor devuelve una vez que procesa la operación **GetItem** . La respuesta indica que el elemento se recuperó correctamente. Los valores de algunos elementos y atributos se han abreviado para mejorar la legibilidad. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" 
                         MinorVersion="0" 
                         MajorBuildNumber="815" 
                         MinorBuildNumber="6" 
                         Version="V2_7" 
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Message>
              <t:ItemId Id="GJc/NAAA=" ChangeKey="CQAAABYAAAAPxolXAHv3TaHUnjW8wWqXAAAGJd9Z"/>
              <t:Subject>Company Soccer Team</t:Subject>
            </t:Message>
          </m:Items>
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </m:GetItemResponse>
  </s:Body>
</s:Envelope>
```

Si no conoce el **ItemId** del elemento que desea recuperar, puede usar la operación [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) para buscar el elemento. Para poder usar la operación **FindItem** , primero debe identificar la carpeta que se va a buscar. Puede identificar la carpeta mediante el uso de su **DistinguinguishedFolderName** o mediante el [FolderId](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx). Puede usar las operaciones de la [FindFolder](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) o [SyncFolderHierarchy](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) para obtener el **FolderId** necesita. A continuación, use la operación **FindItem** para buscar esa carpeta para obtener los resultados que coinciden con el filtro de búsqueda. A diferencia de la API administrada de EWS, EWS no proporciona una operación de búsqueda independiente para las citas. La operación **FindItem** recupera los elementos de todos los tipos. 
  
En el ejemplo siguiente se muestra la solicitud de operación XML **FindItem** que se envía al servidor para buscar citas en la carpeta de calendario que se producen en los próximos 30 días. Los valores de algunos elementos y atributos se han abreviado para mejorar la legibilidad. 
  
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
          <t:FieldURI FieldURI="calendar:Start" />
          <t:FieldURI FieldURI="calendar:End" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:CalendarView MaxEntriesReturned="5" StartDate="2013-10-16T17:04:28.722Z" EndDate="2013-11-15T18:04:28.722Z" />
      <m:ParentFolderIds>
        <t:FolderId Id="AAAEOAAA=" ChangeKey="AgAAABYAAAAqRr3mNdNMSasqx/o9J13UAAAAAAA3" />
      </m:ParentFolderIds>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

El servidor responde a la solicitud de **FindItem** con un mensaje de [FindItemResponse](http://msdn.microsoft.com/library/c8b316df-d4ab-49b8-96d4-8e9a016730ef%28Office.15%29.aspx) que incluye el valor [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, lo que indica que la operación que se realizó correctamente. Si los elementos de calendario cumplen los criterios de filtrado, se incluyen en la respuesta.
  
Tenga en cuenta que la información del servidor se devuelve en la respuesta de la operación **GetItem** es diferente de la información que el servidor devuelve en una **FindItem** o una respuesta de la operación de **FindAppointment** . La operación **GetItem** puede devolver todas las propiedades esquematizadas, mientras que las operaciones **FindItem** y **FindAppointment** no devuelven todas las propiedades esquematizadas. Por lo que si necesita acceso total al elemento, debe usar la operación **GetItem** . Si no dispone de la **ItemId** del elemento que le gustaría recuperar, use las operaciones **FindItem** o **FindAppointment** para recuperar la **ItemId**y, a continuación, use la operación **GetItem** para recuperar los elementos que necesita. 
  
Para obtener información sobre cómo obtener un elemento de cita o reunión mediante el uso de EWS, vea [obtener las citas y reuniones mediante el uso de EWS en Exchange](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md).
  
## <a name="update-an-item-by-using-the-ews-managed-api"></a>Actualizar un elemento mediante el uso de la API administrada de EWS
<a name="bk_updateewsma"> </a>

Los pasos para actualizar un elemento mediante la API administrada de EWS son similares para todos los tipos de elemento; Sin embargo, las propiedades de elemento son diferentes para cada tipo de elemento y el método de [actualización](http://msdn.microsoft.com/en-us/library/office/dd635915%28v=exchg.80%29.aspx) tiene muchos métodos sobrecargados para elegir. Para actualizar un elemento: 
  
1. Utilice el método [Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) para obtener la versión más reciente del elemento, a menos que ya tiene. Para actualizar propiedades específicas a un elemento fuertemente tipado, tendrá que enlazar a ese tipo de elemento. Para actualizar las propiedades disponibles en el tipo de elemento genérico, se puede enlazar al objeto de [elemento](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) . 
    
2. Actualizar las propiedades en el elemento.
    
3. Llame al método **Update** . 
    
Por ejemplo, puede actualizar al asunto de un correo electrónico con el tipo de elemento genérico, como se muestra en el código en el siguiente ejemplo.
  
En este ejemplo se da por supuesto que **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que se ha autenticado el usuario a un servidor de Exchange. La variable local *itemId* es el [identificador](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) del elemento que se debe actualizar. 
  
```cs
// Bind to the existing item, using the ItemId.
// This method call results in a GetItem call to EWS.
Item item = Item.Bind(service, itemId);
// Update the Subject of the email.
item.Subject = "New subject";
// Save the updated email.
// This method call results in an UpdateItem call to EWS.
item.Update(ConflictResolutionMode.AlwaysOverwrite);
```

Para obtener información sobre cómo actualizar un elemento de cita o reunión mediante el uso de la API administrada de EWS, consulte [actualizar las citas y reuniones mediante el uso de EWS en Exchange](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md).
  
## <a name="update-an-item-by-using-ews"></a>Actualizar un elemento mediante el uso de EWS
<a name="bk_updateews"> </a>

Para actualizar un elemento mediante el uso de EWS, haga lo siguiente:
  
1. Use la operación [GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) para obtener la versión más reciente del elemento, a menos que ya tiene. 
    
2. Use la operación [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) para especificar campos para actualizar y asignar nuevos valores a esos campos. 
    
En el ejemplo siguiente se muestra la solicitud de operación XML **UpdateItem** que se envía al servidor para actualizar el valor de [asunto](http://msdn.microsoft.com/library/c140d6c2-deb1-4f67-a908-9397197c4ae7%28Office.15%29.aspx) del mensaje de correo electrónico. Los valores de algunos elementos y atributos se han abreviado para mejorar la legibilidad. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010_SP1" />
  </soap:Header>
  <soap:Body>
    <m:UpdateItem MessageDisposition="SaveOnly" ConflictResolution="AlwaysOverwrite">
      <m:ItemChanges>
        <t:ItemChange>
          <t:ItemId Id="APdZjAAA=" ChangeKey="CQAAABYAAAAqRr3mNdNMSasqx/o9J13UAAAAPdgr" />
          <t:Updates>
            <t:SetItemField>
              <t:FieldURI FieldURI="item:Subject" />
              <t:Message>
                <t:Subject>New subject</t:Subject>
              </t:Message>
            </t:SetItemField>
          </t:Updates>
        </t:ItemChange>
      </m:ItemChanges>
    </m:UpdateItem>
  </soap:Body>
</soap:Envelope>
```

El servidor responde a la solicitud de **UpdateItem** con un mensaje de [UpdateItemResponse](http://msdn.microsoft.com/library/023b79b4-c675-4669-9112-d85499ec4fc4%28Office.15%29.aspx) que incluye el valor [ResponseCode](http://msdn.microsoft.com/en-us/library/aa580757%28v=exchg.150%29.aspx) **NoError**, que indica que la actualización de elemento se realizó correctamente.
  
Para obtener información sobre cómo actualizar un elemento de cita o reunión mediante el uso de EWS, consulte [actualizar las citas y reuniones mediante el uso de EWS en Exchange](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md).
  
## <a name="delete-an-item-by-using-the-ews-managed-api"></a>Eliminar un elemento mediante el uso de la API administrada de EWS
<a name="bk_deleteewsma"> </a>

Puede eliminar elementos moviendo a la carpeta Elementos eliminados o al volcado de archivos. Si conoce el [ItemId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) del elemento para eliminar, simplemente llame al método [Delete](http://msdn.microsoft.com/en-us/library/office/dd635072%28v=exchg.80%29.aspx) en el elemento. 
  
Si necesita buscar el elemento antes de eliminarla, haga lo siguiente:
  
1. Llame al método [FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) o [FindAppointments](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx) para buscar el elemento que desea eliminar. 
    
1. Crear una instancia de un [PropertySet](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.propertyset%28v=exchg.80%29.aspx) y limitar a las propiedades para devolver o utilizar una [SearchFilterCollection](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.searchfiltercollection%28v=exchg.80%29.aspx) para buscar elementos específicos. 
    
2. Crear una instancia de un [artículoVer](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemview%28v=EXCHG.80%29.aspx) o [CalendarView](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.calendarview%28v=exchg.80%29.aspx) para especificar el número de elementos para devolver. 
    
2. Llamar al método [Delete](http://msdn.microsoft.com/en-us/library/office/dd635072%28v=exchg.80%29.aspx) . 
    
Por ejemplo, el código siguiente muestra cómo mover un mensaje de correo electrónico a la carpeta Elementos eliminados.
  
En este ejemplo se da por supuesto que **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que se ha autenticado el usuario a un servidor de Exchange. La variable local *itemId* es el [identificador](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) del elemento que se debe actualizar. 
  
```cs
// Bind to the existing item, using the ItemId.
// This method call results in a GetItem call to EWS.
Item item = Item.Bind(service, itemId);
// Delete the item by moving it to the Deleted Items folder.
// This method call results in a DeleteItem call to EWS.
item.Delete(DeleteMode.MoveToDeletedItems);
```

Para obtener más información acerca de cómo eliminar elementos, vea [Eliminar elementos mediante el uso de EWS en Exchange](deleting-items-by-using-ews-in-exchange.md). Para obtener información sobre cómo eliminar un elemento de cita o reunión mediante el uso de la API administrada de EWS, vea [Eliminar citas y cancelar reuniones mediante el uso de EWS en Exchange](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md).
  
## <a name="delete-an-item-by-using-ews"></a>Eliminar un elemento mediante el uso de EWS
<a name="bk_deleteews"> </a>

Puede eliminar un elemento mediante la operación [DeleteItem](../web-service-reference/deleteitem-operation.md) . 
  
En el ejemplo siguiente se muestra la solicitud XML que se envía al servidor para mover el mensaje de correo electrónico a la carpeta Elementos eliminados. Los valores de algunos elementos y atributos se han abreviado para mejorar la legibilidad.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010_SP1" />
  </soap:Header>
  <soap:Body>
    <m:DeleteItem DeleteType="MoveToDeletedItems">
      <m:ItemIds>
        <t:ItemId Id="APdZjAAA=" ChangeKey="CQAAABYAAAAqRr3mNdNMSasqx/o9J13UAAANIFzC" />
      </m:ItemIds>
    </m:DeleteItem>
  </soap:Body>
</soap:Envelope>
```

El servidor responde a la solicitud de **DeleteItem** con un mensaje de [DeleteItemResponse](http://msdn.microsoft.com/library/86463d66-fe47-4a19-a81b-e24841e816ab%28Office.15%29.aspx) que incluye el valor [ResponseCode](http://msdn.microsoft.com/en-us/library/aa580757%28v=exchg.150%29.aspx) **NoError**, que indica que la eliminación del elemento se realizó correctamente.
  
Para obtener más información acerca de cómo eliminar elementos, vea [Eliminar elementos mediante el uso de EWS en Exchange](deleting-items-by-using-ews-in-exchange.md). Para obtener información sobre cómo eliminar un elemento de cita o reunión mediante el uso de EWS, vea [Eliminar citas y cancelar reuniones mediante el uso de EWS en Exchange](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md).
  
## <a name="move-or-copy-items-to-another-mailbox"></a>Mover o copiar elementos a otro buzón
<a name="bk_movecopybtnmailboxes"> </a>

Puede mover o copiar elementos entre buzones de correo mediante el uso de las operaciones de [ExportItems](http://msdn.microsoft.com/library/e2846abb-0b16-4732-bbd8-038a674672f6%28Office.15%29.aspx) y [UploadItems](http://msdn.microsoft.com/library/a88cbe99-7968-454d-a545-4f92c330909f%28Office.15%29.aspx) . Para obtener más información, consulte [exportación e importación de elementos mediante el uso de EWS en Exchange](exporting-and-importing-items-by-using-ews-in-exchange.md).
  
## <a name="see-also"></a>Vea también

- [Las carpetas y elementos de EWS en Exchange](folders-and-items-in-ews-in-exchange.md)    
- [Trabajar con carpetas mediante EWS en Exchange](how-to-work-with-folders-by-using-ews-in-exchange.md)    
- [Eliminación de elementos con EWS en Exchange](deleting-items-by-using-ews-in-exchange.md)
    

