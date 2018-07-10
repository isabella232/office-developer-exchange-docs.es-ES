---
title: Eliminar las citas y cancelar reuniones mediante el uso de EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 42412265-3968-468a-a8c2-7e8af3c6deb9
description: Obtenga información sobre cómo eliminar las citas y reuniones mediante la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: bd7eac803fedffc51133324259f68fd25652fcff
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763060"
---
# <a name="delete-appointments-and-cancel-meetings-by-using-ews-in-exchange"></a><span data-ttu-id="b7d53-103">Eliminar las citas y cancelar reuniones mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="b7d53-103">Delete appointments and cancel meetings by using EWS in Exchange</span></span>

<span data-ttu-id="b7d53-104">Obtenga información sobre cómo eliminar las citas y reuniones mediante la API administrada de EWS o EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="b7d53-104">Learn how to delete appointments and meetings by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="b7d53-105">La diferencia entre las reuniones y citas esencial es que las reuniones tienen asistentes, y no las citas.</span><span class="sxs-lookup"><span data-stu-id="b7d53-105">The essential difference between meetings and appointments is that meetings have attendees, and appointments don't.</span></span> <span data-ttu-id="b7d53-106">Las citas y reuniones pueden ser instancias únicas o parte de una serie periódica pero, debido a que las citas no incluyen los asistentes, salas o recursos, no requieren que se envíe un mensaje.</span><span class="sxs-lookup"><span data-stu-id="b7d53-106">Both appointments and meetings can be single instances or part of a recurring series, but because appointments don't include attendees, rooms, or resources, they do not require a message to be sent.</span></span> <span data-ttu-id="b7d53-107">Internamente, Exchange utiliza el mismo objeto para las reuniones y citas.</span><span class="sxs-lookup"><span data-stu-id="b7d53-107">Internally, Exchange uses the same object for both meetings and appointments.</span></span> <span data-ttu-id="b7d53-108">Usar la API administrada de EWS [clase de cita](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) o el elemento EWS [CalendarItem](http://msdn.microsoft.com/library/Title Topic ID Project Name Writer Editor Publish Preview.aspx) para trabajar con las reuniones y citas.</span><span class="sxs-lookup"><span data-stu-id="b7d53-108">You use the EWS Managed API [Appointment class](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) or the EWS [CalendarItem](http://msdn.microsoft.com/library/Title Topic ID Project Name Writer Editor Publish Preview.aspx) element to work with meetings and appointments.</span></span> 
  
<span data-ttu-id="b7d53-109">**La tabla 1. Métodos de la API administrada de EWS y las operaciones de EWS para eliminar las citas y reuniones**</span><span class="sxs-lookup"><span data-stu-id="b7d53-109">**Table 1. EWS Managed API methods and EWS operations for deleting appointments and meetings**</span></span>

|<span data-ttu-id="b7d53-110">**Método de la API administrada de EWS**</span><span class="sxs-lookup"><span data-stu-id="b7d53-110">**EWS Managed API method**</span></span>|<span data-ttu-id="b7d53-111">**Operación de EWS**</span><span class="sxs-lookup"><span data-stu-id="b7d53-111">**EWS Operation**</span></span>|<span data-ttu-id="b7d53-112">**Para qué sirve**</span><span class="sxs-lookup"><span data-stu-id="b7d53-112">**What it does**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b7d53-113">Appointment.Delete</span><span class="sxs-lookup"><span data-stu-id="b7d53-113">Appointment.Delete</span></span>](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="b7d53-114">DeleteItem</span><span class="sxs-lookup"><span data-stu-id="b7d53-114">DeleteItem</span></span>](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) <br/> |<span data-ttu-id="b7d53-115">Elimina una cita.</span><span class="sxs-lookup"><span data-stu-id="b7d53-115">Deletes an appointment.</span></span>  <br/> |
|[<span data-ttu-id="b7d53-116">Appointment.Delete</span><span class="sxs-lookup"><span data-stu-id="b7d53-116">Appointment.Delete</span></span>](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="b7d53-117">CreateItem (elemento de calendario)</span><span class="sxs-lookup"><span data-stu-id="b7d53-117">CreateItem (calendar item)</span></span>](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) <br/> |<span data-ttu-id="b7d53-118">Elimina una reunión.</span><span class="sxs-lookup"><span data-stu-id="b7d53-118">Deletes a meeting.</span></span>  <br/> |
   
<span data-ttu-id="b7d53-119">Tenga en cuenta que al eliminar una cita mediante el uso de EWS, use la operación [DeleteItem](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) , pero cuando se elimina una reunión, use la operación [CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b7d53-119">Note that when you delete an appointment by using EWS, you use the [DeleteItem](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) operation, but when you delete a meeting, you use the [CreateItem ](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) operation.</span></span> <span data-ttu-id="b7d53-120">Esto puede parecer poco intuitiva, pero es debido a que tiene que crear una reunión mensajes del objeto response para enviar la cancelación de la reunión a los asistentes.</span><span class="sxs-lookup"><span data-stu-id="b7d53-120">This might seem counterintuitive, but it is because you have to create a meeting response object to send meeting cancellation messages to attendees.</span></span> 
  
## <a name="delete-an-appointment-by-using-the-ews-managed-api"></a><span data-ttu-id="b7d53-121">Eliminación de una cita mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="b7d53-121">Delete an appointment by using the EWS Managed API</span></span>
<span data-ttu-id="b7d53-122"><a name="bk_DeleteApptEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="b7d53-122"></span></span>

<span data-ttu-id="b7d53-123">En el ejemplo de código siguiente se muestra cómo usar el método [Delete](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx) para eliminar una cita de la carpeta Calendario y el método [ExchangeService.FindItems](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) para comprobar que la cita se ha suprimido busca en la carpeta Elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="b7d53-123">The following code example shows how to use the [Delete](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx) method to delete an appointment from your calendar folder, and the [ExchangeService.FindItems](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) method to verify that the appointment was deleted by looking for it in the Deleted Items folder.</span></span> 
  
<span data-ttu-id="b7d53-124">En este ejemplo se supone que se han autenticado a un servidor de Exchange y ha adquirido un objeto [ExchangeService](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) con el nombre de **servicio**.</span><span class="sxs-lookup"><span data-stu-id="b7d53-124">This example assumes that you have authenticated to an Exchange server and have acquired an [ExchangeService](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object named **service**.</span></span> <span data-ttu-id="b7d53-125">La variable local `appointmentId` es un identificador asociado con una cita existente.</span><span class="sxs-lookup"><span data-stu-id="b7d53-125">The local variable  `appointmentId` is an identifier associated with an existing appointment.</span></span> 
  
```cs
// Instantiate an appointment object by binding to it by using the ItemId.
// As a best practice, limit the properties returned to only the ones you need.
Appointment appointment = Appointment.Bind(service, appointmentId, new PropertySet());
// Delete the appointment. Note that the item ID will change when the item is moved to the Deleted Items folder.
appointment.Delete(DeleteMode.MoveToDeletedItems);
// Verify that the appointment has been deleted by looking for a matching subject in the Deleted Items folder's first entry.
ItemView itemView = new ItemView(1);
itemView.Traversal = ItemTraversal.Shallow;
// Just retrieve the properties you need.
itemView.PropertySet = new PropertySet(ItemSchema.Id, ItemSchema.ParentFolderId, ItemSchema.Subject);
// Note that the FindItems method results in a call to EWS.
FindItemsResults<Item> deletedItems = service.FindItems(WellKnownFolderName.DeletedItems, itemView);
Item deletedItem = deletedItems.First();
Folder parentFolder = Folder.Bind(service, deletedItem.ParentFolderId, new PropertySet(FolderSchema.DisplayName));
Console.WriteLine("The appointment " + "\"" + deletedItem.Subject + "\"" + " is now in the " + parentFolder.DisplayName + " folder.");

```

<span data-ttu-id="b7d53-126">En este ejemplo se muestra una forma sencilla de comprobar que se ha eliminado la cita, comprobando que el asunto del primer elemento en la carpeta Elementos eliminados coincide con el de la cita eliminada.</span><span class="sxs-lookup"><span data-stu-id="b7d53-126">This example shows a simple way to verify that the appointment was deleted, by verifying that the subject of the first item in the Deleted Items folder matches that of the deleted appointment.</span></span> <span data-ttu-id="b7d53-127">¿Cómo decide comprobar que se ha eliminado la cita variará en función de las necesidades de su aplicación.</span><span class="sxs-lookup"><span data-stu-id="b7d53-127">How you choose to verify that your appointment was deleted will vary based the needs of your application.</span></span>
  
<span data-ttu-id="b7d53-128">Como puede ver, la eliminación de una cita es sencilla y prácticamente todo lo que podría esperarse.</span><span class="sxs-lookup"><span data-stu-id="b7d53-128">As you can see, deleting an appointment is straightforward and pretty much what you might expect.</span></span> <span data-ttu-id="b7d53-129">Nota Cuando se crea el paso de comprobación que el elemento de cita en la carpeta Elementos eliminados tiene un ItemId diferente que el elemento de cita en la carpeta Calendario.</span><span class="sxs-lookup"><span data-stu-id="b7d53-129">Note when you create your verification step that the appointment item in the Deleted Items folder has a different ItemId than the appointment item in the calendar folder.</span></span> <span data-ttu-id="b7d53-130">El elemento se copian y eliminado en lugar de simplemente se mueve a la carpeta Elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="b7d53-130">The item is copied and deleted rather than simply moved to the Deleted Items folder.</span></span> 
  
## <a name="delete-an-appointment-by-using-ews"></a><span data-ttu-id="b7d53-131">Eliminación de una cita mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="b7d53-131">Delete an appointment by using EWS</span></span>
<span data-ttu-id="b7d53-132"><a name="bk_DeleteApptEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="b7d53-132"></span></span>

<span data-ttu-id="b7d53-133">La solicitud y respuesta XML en los ejemplos siguientes corresponden a las llamadas realizadas por el código de la API administrada de EWS en [Eliminar una cita mediante el uso de la API administrada de EWS](#bk_DeleteApptEWSMA).</span><span class="sxs-lookup"><span data-stu-id="b7d53-133">The request and response XML in the following examples correspond to calls made by the EWS Managed API code in [Delete an appointment by using the EWS Managed API](#bk_DeleteApptEWSMA).</span></span> <span data-ttu-id="b7d53-134">La solicitud y la respuesta se muestra así como XML que comprueba que es el elemento de cita en la carpeta Elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="b7d53-134">The request and response XML that verifies that the appointment item is in the Deleted Items folder is shown as well.</span></span>
  
<span data-ttu-id="b7d53-135">En el ejemplo siguiente se muestra la solicitud XML para la operación [DeleteItem](http://msdn.microsoft.com/library/e2152410-41ce-1fe7-8169-f206d5081ebc%28Office.15%29.aspx) eliminar una cita.</span><span class="sxs-lookup"><span data-stu-id="b7d53-135">The following example shows the request XML for the [DeleteItem](http://msdn.microsoft.com/library/e2152410-41ce-1fe7-8169-f206d5081ebc%28Office.15%29.aspx) operation to delete an appointment.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Pacific Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:DeleteItem DeleteType="MoveToDeletedItems" SendMeetingCancellations="SendToAllAndSaveCopy">
      <m:ItemIds>
        <t:ItemId Id="AAMkA" ChangeKey="DwAAA" />
      </m:ItemIds>
    </m:DeleteItem>
  </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="b7d53-136">En el ejemplo siguiente se muestra la respuesta XML que es devuelto por la [operación DeleteItem](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="b7d53-136">The following example shows the response XML that is returned by the [DeleteItem operation](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx).</span></span> <span data-ttu-id="b7d53-137">Los atributos **ItemId** y **ChangeKey** son más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="b7d53-137">The **ItemId** and **ChangeKey** attributes are shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="800" MinorBuildNumber="5" Version="V2_6" 
 xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:DeleteItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:DeleteItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:DeleteItemResponseMessage>
      </m:ResponseMessages>
    </m:DeleteItemResponse>
  </s:Body>
</s:Envelope>

```

<span data-ttu-id="b7d53-138">En el ejemplo siguiente se muestra la solicitud XML para la operación [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) que recupera el primer elemento de la carpeta Elementos eliminados para comparar el asunto del elemento con el que el objeto de cita eliminada.</span><span class="sxs-lookup"><span data-stu-id="b7d53-138">The following example shows the request XML for the [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) operation that retrieves the first item in the Deleted Items folder in order to compare the item's subject with that of the deleted appointment object.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages
" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Pacific Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:FindItem Traversal="Shallow">
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:ItemId" />
          <t:FieldURI FieldURI="item:ParentFolderId" />
          <t:FieldURI FieldURI="item:Subject" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:IndexedPageItemView MaxEntriesReturned="1" Offset="0" BasePoint="Beginning" />
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="deleteditems" />
      </m:ParentFolderIds>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="b7d53-139">En el ejemplo siguiente se muestra el XML que es devuelto por la operación [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) durante el paso de comprobación de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b7d53-139">The following example shows the response XML that is returned by the [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) operation during the verification step.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="b7d53-140">Los atributos **ItemId** y **ChangeKey** son más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="b7d53-140">The **ItemId** and **ChangeKey** attributes are shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="800" MinorBuildNumber="5" Version="V2_6" 
 xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="1" TotalItemsInView="10748" IncludesLastItemInRange="false">
            <t:Items>
              <t:CalendarItem>
                <t:ItemId Id="AAMkA=" ChangeKey="DwAAA" />
                <t:ParentFolderId Id="AAMkA" ChangeKey="AQAAA" />
                <t:Subject>Tennis lesson</t:Subject>
              </t:CalendarItem>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>

```

<span data-ttu-id="b7d53-141"><a name="bk_DeleteMtgEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="b7d53-141"></span></span>

## <a name="delete-a-meeting-by-using-the-ews-managed-api"></a><span data-ttu-id="b7d53-142">Eliminar una reunión mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="b7d53-142">Delete a meeting by using the EWS Managed API</span></span>

<span data-ttu-id="b7d53-143">Cuando se elimina una reunión, además de quitar el elemento de cita de la carpeta del calendario, es posible que también desee enviar cancelaciones de reunión a los asistentes.</span><span class="sxs-lookup"><span data-stu-id="b7d53-143">When you delete a meeting, in addition to removing the appointment item from the calendar folder, you might also want to send meeting cancellations to attendees.</span></span> <span data-ttu-id="b7d53-144">Puede usar los tres métodos siguientes para cancelar una reunión:</span><span class="sxs-lookup"><span data-stu-id="b7d53-144">You can use the following three methods to cancel a meeting:</span></span>
  
- [<span data-ttu-id="b7d53-145">Appointment.Delete</span><span class="sxs-lookup"><span data-stu-id="b7d53-145">Appointment.Delete</span></span>](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="b7d53-146">Appointment.CancelMeeting</span><span class="sxs-lookup"><span data-stu-id="b7d53-146">Appointment.CancelMeeting</span></span>](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.appointment.cancelmeeting%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="b7d53-147">CancelMeetingMessage</span><span class="sxs-lookup"><span data-stu-id="b7d53-147">CancelMeetingMessage</span></span>](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.cancelmeetingmessage%28v=exchg.80%29.aspx)
    
<span data-ttu-id="b7d53-148">El método que elija depende del nivel de detalle que se debe proporcionar en el mensaje de cancelación.</span><span class="sxs-lookup"><span data-stu-id="b7d53-148">The method that you choose depends on the level of detail you need to provide in your cancellation message.</span></span> <span data-ttu-id="b7d53-149">[Appointment.CancelMeeting](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.appointment.cancelmeeting%28v=exchg.80%29.aspx) facilita el mensaje de cancelación de actualización pasando un mensaje actualizado como un parámetro.</span><span class="sxs-lookup"><span data-stu-id="b7d53-149">[Appointment.CancelMeeting](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.appointment.cancelmeeting%28v=exchg.80%29.aspx) makes it easy to update the cancellation message by passing an updated message as a parameter.</span></span> <span data-ttu-id="b7d53-150">[CancelMeetingMessage](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.cancelmeetingmessage%28v=exchg.80%29.aspx) le permite modificar las propiedades en el mensaje antes de enviar una cancelación, por lo que puede hacer cosas como la solicitud de un recibo.</span><span class="sxs-lookup"><span data-stu-id="b7d53-150">[CancelMeetingMessage](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.cancelmeetingmessage%28v=exchg.80%29.aspx) allows you to modify properties on your message before sending a cancellation, so you can do things like request a receipt.</span></span> 
  
<span data-ttu-id="b7d53-151">Los ejemplos de código de esta sección muestran las distintas maneras de eliminar una reunión y enviar cancelaciones de reuniones.</span><span class="sxs-lookup"><span data-stu-id="b7d53-151">The code examples in this section show the different ways to delete a meeting and send meeting cancellations.</span></span> <span data-ttu-id="b7d53-152">Los ejemplos se supone que se han autenticado a un servidor de Exchange y ha adquirido un objeto [ExchangeService](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) con el nombre de **servicio**.</span><span class="sxs-lookup"><span data-stu-id="b7d53-152">The examples assume that you have authenticated to an Exchange server and have acquired an [ExchangeService](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object named **service**.</span></span> <span data-ttu-id="b7d53-153">La variable local `meetingId` es un identificador asociado a una reunión existente donde el usuario de destino es el organizador de la reunión.</span><span class="sxs-lookup"><span data-stu-id="b7d53-153">The local variable  `meetingId` is an identifier associated with an existing meeting where the target user is the meeting organizer.</span></span> 
  
<span data-ttu-id="b7d53-154">En el ejemplo de código siguiente se muestra cómo eliminar una reunión mediante el método [Appointment.Delete](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b7d53-154">The following code example shows how to delete a meeting by using the [Appointment.Delete](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx) method.</span></span> 
  
```cs
// Instantiate an appointment object for the meeting by binding to it using the ItemId.
// As a best practice, limit the properties returned to only the Appointment ID.
            
Appointment meeting = Appointment.Bind(service, meetingId, new PropertySet());
// Delete the meeting by using the Delete method.
meeting.Delete(DeleteMode.MoveToDeletedItems, SendCancellationsMode.SendToAllAndSaveCopy);
// Verify that the meeting has been deleted by looking for a matching subject in the Deleted Items folder's first entry.
ItemView itemView = new ItemView(1);
itemView.Traversal = ItemTraversal.Shallow;
// Just retrieve the properties you need.
itemView.PropertySet = new PropertySet(ItemSchema.Id, ItemSchema.ParentFolderId, ItemSchema.Subject);
// Note that the FindItems method results in a call to EWS.
FindItemsResults<Item> deletedItems = service.FindItems(WellKnownFolderName.DeletedItems, itemView);
Item deletedItem = deletedItems.First();
Folder parentFolder = Folder.Bind(service, deletedItem.ParentFolderId, new PropertySet(FolderSchema.DisplayName));
Console.WriteLine("The meeting " + "\"" + deletedItem.Subject + "\"" + " is now in the " + parentFolder.DisplayName + " folder.");

```

<span data-ttu-id="b7d53-155">En el ejemplo de código siguiente se muestra cómo eliminar una reunión mediante el método [CancelMeeting](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.appointment.cancelmeeting%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b7d53-155">The following code example shows how to delete a meeting by using the [CancelMeeting](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.appointment.cancelmeeting%28v=exchg.80%29.aspx) method.</span></span> 
  
```cs
// Instantiate an appointment object by binding to it using the ItemId.
// As a best practice, limit the properties returned to only the Appointment ID.
Appointment meeting = Appointment.Bind(service, meetingId, new PropertySet());
// Delete the meeting by using the CancelMeeting method.
meeting.CancelMeeting("The outdoor meeting has been cancelled due to hailstorms.");

```

<span data-ttu-id="b7d53-156">En el ejemplo de código siguiente se muestra cómo eliminar una reunión mediante el método [Appointment.CreateCancelMeetingMessage](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.appointment.createcancelmeetingmessage%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b7d53-156">The following code example shows how to delete a meeting by using the [Appointment.CreateCancelMeetingMessage](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.appointment.createcancelmeetingmessage%28v=exchg.80%29.aspx) method.</span></span> 
  
```cs
// Instantiate an appointment object by binding to it using the ItemId.
// As a best practice, limit the properties returned to only the Appointment ID.
Appointment meeting = Appointment.Bind(service, meetingId, new PropertySet());
// Delete the meeting by using the CreateCancelMeetingMessage method.
CancelMeetingMessage cancelMessage = meeting.CreateCancelMeetingMessage();
cancelMessage.Body = new MessageBody("The outdoor meeting has been canceled due to hailstorms.");
cancelMessage.IsReadReceiptRequested = true;
cancelMessage.SendAndSaveCopy();

```

## <a name="delete-a-meeting-by-using-ews"></a><span data-ttu-id="b7d53-157">Eliminar una reunión mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="b7d53-157">Delete a meeting by using EWS</span></span>
<span data-ttu-id="b7d53-158"><a name="bk_EWSDeleteApptAndMeeting"> </a></span><span class="sxs-lookup"><span data-stu-id="b7d53-158"></span></span>

<span data-ttu-id="b7d53-159">La solicitud y respuesta XML en los ejemplos siguientes corresponden a las llamadas realizadas por el código de la API administrada de EWS en [Eliminar una reunión mediante el uso de la API administrada de EWS](#bk_DeleteMtgEWSMA) mediante el método [Appointment.Delete](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b7d53-159">The request and response XML in the following examples correspond to calls made by the EWS Managed API code in [Delete a meeting by using the EWS Managed API](#bk_DeleteMtgEWSMA) by using the [Appointment.Delete](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx) method.</span></span> 
  
<span data-ttu-id="b7d53-160">En el ejemplo siguiente se muestra la solicitud XML al usar la operación [CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) para enviar mensajes de cancelación a los asistentes y eliminar una reunión.</span><span class="sxs-lookup"><span data-stu-id="b7d53-160">The following example shows the request XML when you use the [CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) operation to send cancellation messages to attendees and delete a meeting.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Pacific Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:CreateItem MessageDisposition="SendAndSaveCopy">
      <m:Items>
        <t:CancelCalendarItem>
          <t:ReferenceItemId Id="AAMkA" ChangeKey="DwAAA" />
          <t:NewBodyContent BodyType="HTML">The outdoor meeting has been canceled due to hailstorms.</t:NewBodyContent>
        </t:CancelCalendarItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="b7d53-161">En el ejemplo siguiente se muestra el XML que se devuelve en respuesta a una solicitud de operación [CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) usada para eliminar una reunión.</span><span class="sxs-lookup"><span data-stu-id="b7d53-161">The following example shows the XML that is returned in response to a [CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) operation request used to delete a meeting.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="b7d53-162">Los atributos **ItemId** y **ChangeKey** son más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="b7d53-162">The **ItemId** and **ChangeKey** attributes are shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="800" MinorBuildNumber="5" Version="V2_6" 
 xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:CreateItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="b7d53-163">En el ejemplo siguiente se muestra la solicitud XML para la operación [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) que recupera el primer elemento de la carpeta Elementos eliminados para comparar el asunto del elemento con el que el objeto de cita eliminada.</span><span class="sxs-lookup"><span data-stu-id="b7d53-163">The following example shows the request XML for the [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) operation that retrieves the first item in the Deleted Items folder in order to compare the item's subject with that of the deleted appointment object.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Pacific Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:FindItem Traversal="Shallow">
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:ItemId" />
          <t:FieldURI FieldURI="item:ParentFolderId" />
          <t:FieldURI FieldURI="item:Subject" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:IndexedPageItemView MaxEntriesReturned="1" Offset="0" BasePoint="Beginning" />
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="deleteditems" />
      </m:ParentFolderIds>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="b7d53-164">En el ejemplo siguiente se muestra el XML que es devuelto por la operación [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) durante el paso de comprobación.</span><span class="sxs-lookup"><span data-stu-id="b7d53-164">The following example shows the XML that is returned by the [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) operation during the verification step.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="b7d53-165">Los atributos **Id** y **ChangeKey** son más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="b7d53-165">The **Id** and **ChangeKey** attributes are shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="800" MinorBuildNumber="5" Version="V2_6" 
 xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="1" TotalItemsInView="10750" IncludesLastItemInRange="false">
            <t:Items>
              <t:CalendarItem>
                <t:ItemId Id="AAMkA" ChangeKey="DwAAA" />
                <t:ParentFolderId Id="AAMkA" ChangeKey="AQAAA" />
                <t:Subject>Team building exercise</t:Subject>
              </t:CalendarItem>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>

```

## <a name="see-also"></a><span data-ttu-id="b7d53-166">Vea también</span><span class="sxs-lookup"><span data-stu-id="b7d53-166">See also</span></span>

- [<span data-ttu-id="b7d53-167">Calendarios y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="b7d53-167">Calendars and EWS in Exchange</span></span>](calendars-and-ews-in-exchange.md)    
- [<span data-ttu-id="b7d53-168">Crear citas y reuniones mediante el uso de EWS en Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="b7d53-168">Create appointments and meetings by using EWS in Exchange 2013</span></span>](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)  
- [<span data-ttu-id="b7d53-169">Obtener las citas y reuniones con EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="b7d53-169">Get appointments and meetings by using EWS in Exchange</span></span>](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md) 
- [<span data-ttu-id="b7d53-170">Actualizar las citas y reuniones con EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="b7d53-170">Update appointments and meetings by using EWS in Exchange</span></span>](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)  
- [<span data-ttu-id="b7d53-171">Proponer una nueva hora de reunión mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="b7d53-171">Propose a new meeting time by using EWS in Exchange</span></span>](how-to-propose-a-new-meeting-time-by-using-ews-in-exchange.md) 
- [<span data-ttu-id="b7d53-172">Proponer una nueva hora de reunión mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="b7d53-172">Propose a new meeting time by using EWS in Exchange</span></span>](how-to-propose-a-new-meeting-time-by-using-ews-in-exchange.md)
    

