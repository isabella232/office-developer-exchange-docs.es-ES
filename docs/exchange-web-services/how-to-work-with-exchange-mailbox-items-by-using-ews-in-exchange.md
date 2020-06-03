---
title: Trabajar con elementos de buzón de Exchange mediante EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 721deb84-f85d-45d0-84c1-0ed55f359969
description: Obtenga información sobre cómo crear, obtener, actualizar y eliminar elementos con la API administrada de EWS o EWS en Exchange.
localization_priority: Priority
ms.openlocfilehash: e86affbe8efe0dfc312f5ed5fadec2547f1352ea
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527589"
---
# <a name="work-with-exchange-mailbox-items-by-using-ews-in-exchange"></a>Trabajar con elementos de buzón de Exchange mediante EWS en Exchange

Obtenga información sobre cómo crear, obtener, actualizar y eliminar elementos con la API administrada de EWS o EWS en Exchange.
  
Puede usar la API administrada de EWS o EWS para trabajar con elementos en un buzón. Puede usar elementos genéricos (objetos de [elemento](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) de la API administrada de EWS o tipos de [elementos](https://msdn.microsoft.com/library/4dfe8f48-e7b4-444d-bdf9-a34e180f598b%28Office.15%29.aspx) EWS) para realizar algunas operaciones (obtener un elemento o eliminar un elemento mediante el identificador del elemento); sin embargo, la mayoría de las veces tendrá que usar un [elemento con establecimiento inflexible de tipos](folders-and-items-in-ews-in-exchange.md#bk_item) para realizar una operación de obtención o actualización, ya que necesitará tener acceso a las propiedades que son específicas del elemento con establecimiento inflexible de tipos. 

Por ejemplo, no puede usar un elemento genérico para recuperar un elemento que contenga una fecha de inicio y de finalización, necesita un objeto de [cita](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) de API administrada EWS o un tipo [CalendarItem](https://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) de EWS para ello. Y, si usa la API administrada de EWS, siempre tendrá que crear elementos con establecimiento inflexible de tipos, ya que la clase de **elemento** genérico no tiene un constructor. Si está trabajando con un elemento que no tiene establecimiento inflexible de tipos, puede usar siempre la clase de **elemento** base para trabajar con el elemento. 
  
**Tabla 1. Métodos de API administrada de EWS y operaciones de EWS para trabajar con elementos**

|**Para**|**Método de la API administrada de EWS**|**Operación de EWS**|
|:-----|:-----|:-----|
|Crear un elemento genérico  <br/> |Ninguna. Solo se pueden crear tipos de elementos específicos mediante la API administrada de EWS; no se pueden crear elementos genéricos.  <br/> |[CreateItem](https://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) <br/> |
|Obtener un elemento  <br/> |[Item. bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) <br/> |[GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/> |
|Actualizar un elemento  <br/> |[Item. Update](https://msdn.microsoft.com/library/office/dd635915%28v=exchg.80%29.aspx) <br/> |[UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |
|Eliminar un elemento  <br/> |[Item. Delete](https://msdn.microsoft.com/library/office/dd635072%28v=exchg.80%29.aspx) <br/> |[DeleteItem](../web-service-reference/deleteitem-operation.md) <br/> |
   
En este artículo, aprenderá a usar la clase base genérica y cuando necesite usar un elemento con establecimiento inflexible de tipos para completar la tarea. En los ejemplos de código se muestra cómo usar la clase base y qué hacer cuando no se puede usar la clase base o no se ajusta a sus necesidades.
  
## <a name="create-an-item-by-using-the-ews-managed-api"></a>Crear un elemento mediante la API administrada de EWS
<a name="bk_createewsma"> </a>

La API administrada de EWS no tiene un constructor disponible públicamente para la clase de [elemento](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) , por lo que debe usar el constructor para el tipo de elemento específico que desea crear para crear un elemento. Por ejemplo, use el [constructor de la clase EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.emailmessage%28v=exchg.80%29.aspx) para crear un nuevo mensaje de correo electrónico y el [constructor de clase Contact](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx) para crear un contacto nuevo. Del mismo modo, el servidor nunca devuelve objetos de **elementos** genéricos en las respuestas; todos los elementos genéricos se devuelven como objetos **EmailMessage** . 
  
Cuando conoce el tipo de elemento que se va a crear, puede completar la tarea en tan solo unos pocos pasos. Los pasos son similares para todos los tipos de elementos:
  
1. Inicialice una nueva instancia de una de las clases de [elemento](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) con el objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) como parámetro. 
    
2. Establecer propiedades en el elemento. Los esquemas son distintos para cada tipo de elemento, por lo que hay distintas propiedades disponibles para los distintos elementos.
    
3. Guarda el elemento o guarda y envía el elemento.
    
Por ejemplo, puede crear un objeto [EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) , establecer las propiedades [Subject](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.subject%28v=exchg.80%29.aspx), [Body](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.body%28v=exchg.80%29.aspx)y [ToRecipients](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.torecipients%28v=exchg.80%29.aspx) y, a continuación, enviarlo mediante el método [EmailMessage. SendAndSaveCopy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx) . 
  
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

Para obtener información sobre cómo crear un elemento de reunión o cita mediante la API administrada de EWS, vea [crear citas y reuniones mediante EWS en Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md).
  
## <a name="create-an-item-by-using-ews"></a>Crear un elemento mediante EWS
<a name="bk_createews"> </a>

Puede crear un elemento genérico o un elemento con establecimiento inflexible de tipos mediante EWS. Los pasos son similares para todos los tipos de elementos:
  
1. Use la operación [CreateItem](https://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) para crear un elemento en el almacén de Exchange. 
    
2. Use el elemento [Items](https://msdn.microsoft.com/library/0811a73e-bf1f-4889-9219-73902dd47639%28Office.15%29.aspx) para contener uno o más elementos que se van a crear. 
    
3. Establecer propiedades en el elemento.
    
Por ejemplo, puede crear un mensaje de correo electrónico y enviarlo mediante el código del ejemplo siguiente. También es la solicitud XML que la API administrada de EWS envía cuando se llama al método [SendAndSaveCopy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx) . 
  
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

El servidor responde a la solicitud **CreateItem** con un mensaje [CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) que incluye un valor [ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx) de **NoError**, que indica que el correo electrónico se ha creado correctamente y el [Itemid](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) del mensaje recién creado. 
  
Para obtener información sobre cómo crear un elemento de cita o reunión con EWS, vea [crear citas y reuniones mediante EWS en Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md).
  
## <a name="get-an-item-by-using-the-ews-managed-api"></a>Obtener un elemento mediante la API administrada de EWS
<a name="bk_getewsma"> </a>

Para usar la API administrada de EWS para obtener un elemento si conoce el [Item.ID](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) del elemento que se va a recuperar, simplemente debe llamar a uno de los métodos de [enlace](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) en el elemento y se recuperará el elemento. Como práctica recomendada, le recomendamos que limite las propiedades que se devuelven solo a las que son necesarias. En este ejemplo se devuelven la propiedad **ID** del elemento y la propiedad **Subject** . 
  
En este ejemplo se supone que el **servicio** es un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que el usuario se ha autenticado en un servidor de Exchange. La variable local *Itemid* es el [identificador](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) del elemento que se va a actualizar. 
  
```cs
// As a best practice, limit the properties returned to only those that are required.
PropertySet propSet = new PropertySet(BasePropertySet.IdOnly, ItemSchema.Subject);
// Bind to the existing item by using the ItemId.
// This method call results in a GetItem call to EWS.
Item item = Item.Bind(service, itemId, propSet);

```

Si está buscando un elemento que cumpla determinados criterios, haga lo siguiente:
  
1. Enlazar a la carpeta que contiene los elementos que se van a obtener.
    
2. Crea una instancia de [SearchFilter. SearchFilterCollection](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.searchfiltercollection%28v=exchg.80%29.aspx) o un [PropertySet](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.propertyset%28v=exchg.80%29.aspx) para filtrar los elementos que se van a devolver. 
    
3. Cree una instancia de un objeto [ItemView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview%28v=EXCHG.80%29.aspx) o [CalendarView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.calendarview%28v=exchg.80%29.aspx) para especificar el número de elementos que se van a devolver. 
    
4. Llame al método [ExchangeService. FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) o [ExchangeService. FindAppointments](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx) . 
    
Por ejemplo, si desea recuperar los mensajes de correo electrónico no leídos en la bandeja de entrada, use el código del ejemplo siguiente. En este ejemplo se usa un **SearchFilterCollection** para limitar los resultados del método **FindItems** a mensajes no leídos y se limita el **ItemView** para limitar los resultados a un elemento. Este código en concreto solo funciona en objetos [EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) porque el valor [EmailMessageSchema. IsRead](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessageschema.isread%28v=exchg.80%29.aspx) forma parte de la **SearchFilter**. 
  
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

Como alternativa, puedes usar un [PropertySet](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) para limitar los resultados de la búsqueda, como se muestra en el siguiente ejemplo de código. En este ejemplo, se usa el método [FindAppointments](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx) para recuperar hasta cinco citas que se producen en los próximos 30 días. Este código de curso solo funciona en los elementos de calendario. 
  
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

Tenga en cuenta que la información que devuelve el servidor en la respuesta del método de **enlace** es diferente de la información que devuelve el servidor para una respuesta del método **FindItem** o **FindAppointment** . El método **BIND** puede devolver todas las propiedades esquematizado, mientras que los métodos **FindItem** y **FindAppointment** no devuelven todas las propiedades de esquematizado. Por lo tanto, si necesita acceso total al elemento, tendrá que usar el método **BIND** . Si no tiene el **identificador** de elemento del elemento que le gustaría recuperar, use los métodos **FindItem** o **FindAppointment** para recuperar el identificador y, a continuación, use el método **BIND** para recuperar las propiedades que necesita. 
  
Para obtener información sobre cómo obtener un elemento de reunión o cita mediante la API administrada de EWS, vea [obtener citas y reuniones mediante EWS en Exchange](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md).
  
## <a name="get-an-item-by-using-ews"></a>Obtener un elemento mediante EWS
<a name="bk_getews"> </a>

Si conoce el elemento [Itemid](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) del elemento que se va a recuperar, puede obtener el elemento mediante la operación [GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) . 
  
En el ejemplo siguiente se muestra la solicitud XML para obtener el [asunto](https://msdn.microsoft.com/library/c140d6c2-deb1-4f67-a908-9397197c4ae7%28Office.15%29.aspx) de un elemento con un **Itemid**específico. También es la solicitud XML que la API administrada de EWS envía cuando llama al método [BIND](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) en un **Itemid**. Los valores de algunos atributos y elementos se han abreviado para facilitar su lectura.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

En el ejemplo siguiente se muestra la respuesta XML que devuelve el servidor después de procesar la operación **GetItem** . La respuesta indica que el elemento se recuperó correctamente. Los valores de algunos atributos y elementos se han abreviado para facilitar su lectura. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" 
                         MinorVersion="0" 
                         MajorBuildNumber="815" 
                         MinorBuildNumber="6" 
                         Version="V2_7" 
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

Si no conoce el elemento **Itemid** del elemento que desea recuperar, puede usar la operación [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) para buscar el elemento. Para poder usar la operación **FindItem** , primero debe identificar la carpeta en la que está buscando. Puede identificar la carpeta con su **DistinguinguishedFolderName** o con el [FolderId](https://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx). Puede usar las operaciones [FindFolder](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) o [SyncFolderHierarchy](https://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) para obtener la **FolderId** que necesita. A continuación, use la operación **FindItem** para buscar en esa carpeta los resultados que coinciden con el filtro de búsqueda. A diferencia de la API administrada de EWS, EWS no proporciona una operación de búsqueda independiente para las citas. La operación **FindItem** recupera elementos de todos los tipos. 
  
En el siguiente ejemplo se muestra la solicitud de operación de **FINDITEM** XML que se envía al servidor para buscar citas en la carpeta calendario que se producen en los próximos 30 días. Los valores de algunos atributos y elementos se han abreviado para facilitar su lectura. 
  
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

El servidor responde a la solicitud **FindItem** con un mensaje [FindItemResponse](https://msdn.microsoft.com/library/c8b316df-d4ab-49b8-96d4-8e9a016730ef%28Office.15%29.aspx) que incluye el valor [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, que indica que la operación se completó correctamente. Si alguno de los elementos del calendario cumple los criterios de filtrado, se incluyen en la respuesta.
  
Tenga en cuenta que la información que devuelve el servidor en la respuesta de la operación **GetItem** es diferente de la información que devuelve el servidor en una respuesta de operación **FindItem** o **FindAppointment** . La operación **GetItem** puede devolver todas las propiedades esquematizado, mientras que las operaciones **FindItem** y **FindAppointment** no devuelven todas las propiedades de esquematizado. Por lo tanto, si necesita acceso total al elemento, tendrá que usar la operación **GetItem** . Si no tiene el elemento **Itemid** del elemento que quiere recuperar, use las operaciones **FindItem** o **FindAppointment** para recuperar el **Itemid**y, a continuación, use la operación **GetItem** para recuperar los elementos que necesita. 
  
Para obtener información sobre cómo obtener un elemento de reunión o cita con EWS, vea [obtener citas y reuniones mediante EWS en Exchange](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md).
  
## <a name="update-an-item-by-using-the-ews-managed-api"></a>Actualizar un elemento mediante la API administrada de EWS
<a name="bk_updateewsma"> </a>

Los pasos para actualizar un elemento mediante la API administrada de EWS son similares para todos los tipos de elementos; sin embargo, las propiedades de elemento son diferentes para cada tipo de elemento y el método [Update](https://msdn.microsoft.com/library/office/dd635915%28v=exchg.80%29.aspx) tiene muchos métodos sobrecargados para elegir. Para actualizar un elemento: 
  
1. Use el método [BIND](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) para obtener la versión más reciente del elemento, a menos que ya la tenga. Para actualizar las propiedades específicas de un elemento con establecimiento inflexible de tipos, tendrá que enlazar a ese tipo de elemento. Para actualizar las propiedades disponibles en el tipo de elemento genérico, puede enlazar al objeto de [elemento](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) . 
    
2. Actualice las propiedades del elemento.
    
3. Llamar al método **Update** . 
    
Por ejemplo, puede actualizar el asunto de un mensaje de correo electrónico usando el tipo de elemento genérico, como se muestra en el código del siguiente ejemplo.
  
En este ejemplo se supone que el **servicio** es un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que el usuario se ha autenticado en un servidor de Exchange. La variable local *Itemid* es el [identificador](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) del elemento que se va a actualizar. 
  
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

Para obtener información sobre cómo actualizar un elemento de reunión o cita mediante la API administrada de EWS, vea [actualizar citas y reuniones mediante EWS en Exchange](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md).
  
## <a name="update-an-item-by-using-ews"></a>Actualizar un elemento mediante EWS
<a name="bk_updateews"> </a>

Para actualizar un elemento mediante EWS, haga lo siguiente:
  
1. Use la operación [GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) para obtener la versión más reciente del elemento, a menos que ya la tenga. 
    
2. Use la operación [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) para especificar los campos que se actualizarán y asigne nuevos valores a esos campos. 
    
En el ejemplo siguiente se muestra la solicitud de operación XML **UpdateItem** que se envía al servidor para actualizar el valor de [asunto](https://msdn.microsoft.com/library/c140d6c2-deb1-4f67-a908-9397197c4ae7%28Office.15%29.aspx) del mensaje de correo electrónico. Los valores de algunos atributos y elementos se han abreviado para facilitar su lectura. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

El servidor responde a la solicitud **UpdateItem** con un mensaje [UpdateItemResponse](https://msdn.microsoft.com/library/023b79b4-c675-4669-9112-d85499ec4fc4%28Office.15%29.aspx) que incluye el valor [ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx) de **NoError**, que indica que la actualización del elemento se realizó correctamente.
  
Para obtener información sobre cómo actualizar un elemento de reunión o cita mediante EWS, consulte [actualizar citas y reuniones mediante EWS en Exchange](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md).
  
## <a name="delete-an-item-by-using-the-ews-managed-api"></a>Eliminar un elemento mediante la API administrada de EWS
<a name="bk_deleteewsma"> </a>

Puede eliminar elementos moviéndolos a la carpeta elementos eliminados o al contenedor. Si conoce el elemento [Itemid](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) del elemento que se va a eliminar, solo tiene que llamar al método [Delete](https://msdn.microsoft.com/library/office/dd635072%28v=exchg.80%29.aspx) en el elemento. 
  
Si necesita buscar el elemento antes de eliminarlo, haga lo siguiente:
  
1. Llame al método [FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) o [FindAppointments](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx) para buscar el elemento que se va a eliminar. 
    
1. Crea una instancia de una [PropertySet](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.propertyset%28v=exchg.80%29.aspx) y la limita a las propiedades que se van a devolver, o usa una [SearchFilterCollection](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.searchfiltercollection%28v=exchg.80%29.aspx) para buscar elementos específicos. 
    
2. Cree una instancia de [ItemView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview%28v=EXCHG.80%29.aspx) o [CalendarView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.calendarview%28v=exchg.80%29.aspx) para especificar el número de elementos que se devolverán. 
    
2. Llamar al método [Delete](https://msdn.microsoft.com/library/office/dd635072%28v=exchg.80%29.aspx) . 
    
Por ejemplo, el siguiente código muestra cómo mover un mensaje de correo electrónico a la carpeta elementos eliminados.
  
En este ejemplo se supone que el **servicio** es un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que el usuario se ha autenticado en un servidor de Exchange. La variable local *Itemid* es el [identificador](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) del elemento que se va a actualizar. 
  
```cs
// Bind to the existing item, using the ItemId.
// This method call results in a GetItem call to EWS.
Item item = Item.Bind(service, itemId);
// Delete the item by moving it to the Deleted Items folder.
// This method call results in a DeleteItem call to EWS.
item.Delete(DeleteMode.MoveToDeletedItems);
```

Para obtener más información sobre cómo eliminar elementos, vea [eliminar elementos mediante EWS en Exchange](deleting-items-by-using-ews-in-exchange.md). Para obtener información sobre cómo eliminar una reunión o un elemento de cita mediante la API administrada de EWS, vea [eliminar citas y cancelar reuniones mediante EWS en Exchange](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md).
  
## <a name="delete-an-item-by-using-ews"></a>Eliminar un elemento mediante EWS
<a name="bk_deleteews"> </a>

Puede eliminar un elemento mediante la operación [DeleteItem](../web-service-reference/deleteitem-operation.md) . 
  
En el ejemplo siguiente se muestra la solicitud XML que se envía al servidor para mover el mensaje de correo electrónico a la carpeta elementos eliminados. Los valores de algunos atributos y elementos se han abreviado para facilitar su lectura.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

El servidor responde a la solicitud **DeleteItem** con un mensaje [DeleteItemResponse](https://msdn.microsoft.com/library/86463d66-fe47-4a19-a81b-e24841e816ab%28Office.15%29.aspx) que incluye el valor [ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx) de **NoError**, lo que indica que la eliminación del elemento se ha realizado correctamente.
  
Para obtener más información sobre cómo eliminar elementos, vea [eliminar elementos mediante EWS en Exchange](deleting-items-by-using-ews-in-exchange.md). Para obtener información sobre cómo eliminar una reunión o un elemento de cita mediante EWS, vea [eliminar citas y cancelar reuniones mediante EWS en Exchange](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md).
  
## <a name="move-or-copy-items-to-another-mailbox"></a>Mover o copiar elementos a otro buzón
<a name="bk_movecopybtnmailboxes"> </a>

Puede mover o copiar elementos entre buzones de correo mediante el uso de las operaciones [ExportItems](https://msdn.microsoft.com/library/e2846abb-0b16-4732-bbd8-038a674672f6%28Office.15%29.aspx) y [UploadItems](https://msdn.microsoft.com/library/a88cbe99-7968-454d-a545-4f92c330909f%28Office.15%29.aspx) . Para obtener más información, vea [exportar e importar elementos mediante EWS en Exchange](exporting-and-importing-items-by-using-ews-in-exchange.md).
  
## <a name="see-also"></a>Vea también

- [Carpetas y elementos de EWS en Exchange](folders-and-items-in-ews-in-exchange.md)    
- [Trabajar con carpetas mediante EWS en Exchange](how-to-work-with-folders-by-using-ews-in-exchange.md)    
- [Eliminación de elementos mediante EWS en Exchange](deleting-items-by-using-ews-in-exchange.md)
    

