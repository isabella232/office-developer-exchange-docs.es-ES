---
title: Actualización de una serie periódica mediante el uso de EWS
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7e61bee9-4840-4773-a0a7-47b11e1fdf59
description: Obtenga información sobre cómo modificar las citas de una serie periódica mediante la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: ecee78457d2e6f91483cf897cfb4976fbd83400c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763187"
---
# <a name="update-a-recurring-series-by-using-ews"></a><span data-ttu-id="32a11-103">Actualización de una serie periódica mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="32a11-103">Update a recurring series by using EWS</span></span>

<span data-ttu-id="32a11-104">Obtenga información sobre cómo modificar las citas de una serie periódica mediante la API administrada de EWS o EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="32a11-104">Learn how to modify appointments in a recurring series by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="32a11-105">Puede usar la API administrada de EWS o EWS para actualizar una serie periódica puede ser [Actualizar toda la serie](how-to-update-a-recurring-series-by-using-ews-in-exchange.md), o mediante la actualización de una sola aparición.</span><span class="sxs-lookup"><span data-stu-id="32a11-105">You can use the EWS Managed API or EWS to update a recurring series by either [updating the entire series](how-to-update-a-recurring-series-by-using-ews-in-exchange.md), or by updating a single occurrence.</span></span> <span data-ttu-id="32a11-106">En este artículo se explica cómo actualizar una sola aparición.</span><span class="sxs-lookup"><span data-stu-id="32a11-106">In this article we'll discuss how to update a single occurrence.</span></span>
  
<span data-ttu-id="32a11-107">Modificación de una cita única de una serie es muy similar a la [modificación de una cita de una sola instancia](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="32a11-107">Modifying a single appointment in a series is very similar to [modifying a single instance appointment](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md).</span></span> <span data-ttu-id="32a11-108">Usar los mismos métodos y operaciones, pero use el identificador de elemento de la aparición que desea cambiar.</span><span class="sxs-lookup"><span data-stu-id="32a11-108">You use the same methods and operations, but you use the item ID of the occurrence you want to change.</span></span>
  
<span data-ttu-id="32a11-109">Cuando se cambia una sola aparición de una serie, esa aparición se agrega a una matriz de citas modificadas asociadas con el patrón de la serie periódico.</span><span class="sxs-lookup"><span data-stu-id="32a11-109">When you change a single occurrence in a series, that occurrence is added to an array of modified appointments associated with the recurring master for the series.</span></span> <span data-ttu-id="32a11-110">Puede usar la propiedad de la API administrada de EWS [Appointment.ModifiedOccurrences](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.modifiedoccurrences%28v=exchg.80%29.aspx) o el elemento EWS [ModifiedOccurrences](http://msdn.microsoft.com/library/552932fc-b3b4-486e-8d73-32c0bb10bd68%28Office.15%29.aspx) para tener acceso a todas las citas de una serie que se han modificado.</span><span class="sxs-lookup"><span data-stu-id="32a11-110">You can use the [Appointment.ModifiedOccurrences](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.modifiedoccurrences%28v=exchg.80%29.aspx) EWS Managed API property or the [ModifiedOccurrences](http://msdn.microsoft.com/library/552932fc-b3b4-486e-8d73-32c0bb10bd68%28Office.15%29.aspx) EWS element to access all the appointments in a series that have been modified.</span></span> 
  
## <a name="modify-a-single-occurrence-in-a-series-by-using-the-ews-managed-api"></a><span data-ttu-id="32a11-111">Modificar una única incidencia de una serie mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="32a11-111">Modify a single occurrence in a series by using the EWS Managed API</span></span>

<span data-ttu-id="32a11-112">Para modificar una sola instancia de una serie,:</span><span class="sxs-lookup"><span data-stu-id="32a11-112">To modify a single instance in a series, you:</span></span>
  
1. <span data-ttu-id="32a11-113">Enlazar a la instancia que desee modificar mediante el método de [Appointment.BindToOccurrence](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.appointment.bindtooccurrence%28v=exchg.80%29.aspx) con su valor de índice del elemento, o el método [Appointment.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) con el identificador de. de la aparición</span><span class="sxs-lookup"><span data-stu-id="32a11-113">Bind to the occurrence you want to modify by using either the [Appointment.BindToOccurrence](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.appointment.bindtooccurrence%28v=exchg.80%29.aspx) method with the item's index value, or the [Appointment.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) method with the occurrence's ID.</span></span> <span data-ttu-id="32a11-114">Obtener este identificador desde bien la propiedad [Id](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) de un objeto de [cita](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) que corresponde a la instancia, o desde la propiedad [ItemId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.occurrenceinfo.itemid%28v=exchg.80%29.aspx) del objeto [OccurrenceInfo](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.occurrenceinfo%28v=exchg.80%29.aspx) que corresponde a la aparición.</span><span class="sxs-lookup"><span data-stu-id="32a11-114">You obtain this ID from either the [Id](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) property of an [Appointment](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) object that corresponds to the occurrence, or from the [ItemId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.occurrenceinfo.itemid%28v=exchg.80%29.aspx) property of the [OccurrenceInfo](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.occurrenceinfo%28v=exchg.80%29.aspx) object that corresponds to the occurrence.</span></span> 
    
2. <span data-ttu-id="32a11-115">Actualizar las propiedades en el objeto de la aparición una cita.</span><span class="sxs-lookup"><span data-stu-id="32a11-115">Update the properties on the occurrence's Appointment object.</span></span>
    
3. <span data-ttu-id="32a11-116">Guardar los cambios en el objeto de cita de la aparición mediante el método [Appointment.Save](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="32a11-116">Save the changes to the occurrence's appointment object by using the [Appointment.Save](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) method.</span></span> 
    
<span data-ttu-id="32a11-117">En el ejemplo siguiente se actualiza una cita en una serie periódica y comprueba que se actualiza la cita modificada en el maestro de periódico.</span><span class="sxs-lookup"><span data-stu-id="32a11-117">The following example updates an appointment in a recurring series and verifies that the modified appointment is updated on the recurring master.</span></span> <span data-ttu-id="32a11-118">En este ejemplo se supone que se han autenticado a un servidor de Exchange y ha adquirido un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) con el nombre de **servicio**.</span><span class="sxs-lookup"><span data-stu-id="32a11-118">This example assumes that you have authenticated to an Exchange server and have acquired an [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object named **service**.</span></span> <span data-ttu-id="32a11-119">El `recurrenceMasterId` parámetro es un identificador asociado con el patrón de periódico de la repetición modificar.</span><span class="sxs-lookup"><span data-stu-id="32a11-119">The  `recurrenceMasterId` parameter is an identifier associated with the recurring master for the occurrence to modify.</span></span> 
  
```cs
public static ItemId ModifyARecurringSeries(ExchangeService service, ItemId recurrenceMasterId)
{
    Appointment calendarItem = Appointment.Bind(service, recurrenceMasterId, new PropertySet(AppointmentSchema.AppointmentType));
    Appointment recurrMaster = new Appointment(service);
    if (calendarItem.AppointmentType == AppointmentType.RecurringMaster)
    {
        // Get the recurring master from an occurrence in a recurring series with the properties you need.
        recurrMaster = Appointment.Bind(service,
                                        recurrenceMasterId,
                                        new PropertySet(AppointmentSchema.AppointmentType,
                                                        AppointmentSchema.Subject,
                                                        AppointmentSchema.FirstOccurrence,
                                                        AppointmentSchema.LastOccurrence,
                                                        AppointmentSchema.ModifiedOccurrences,
                                                        AppointmentSchema.DeletedOccurrences));
    }
    else
    {
        Console.WriteLine("Item id was not for a recurring master.");
        return recurrenceMasterId;
    }
    // Bind to the second occurrence in the series with the properties to modify.
    Appointment occurrenceToModify = Appointment.BindToOccurrence(service,
                                                                    recurrMaster.Id,
                                                                    2,
                                                                    new PropertySet(AppointmentSchema.Location,
                                                                                    AppointmentSchema.Start,
                                                                                    AppointmentSchema.End,
                                                                                    AppointmentSchema.RequiredAttendees,
                                                                                    AppointmentSchema.Subject));
    // Update the properties you want to change.
    occurrenceToModify.Location = "Helipad of Contoso Bldg 1";
    occurrenceToModify.Start = occurrenceToModify.Start.AddDays(1);
    occurrenceToModify.End = occurrenceToModify.End.AddDays(1);
    occurrenceToModify.RequiredAttendees.Add("Contoso CEO", "sadie@contoso");
    occurrenceToModify.RequiredAttendees.Add("Contoso Head of Research", "ronnie@contoso.com");
    occurrenceToModify.RequiredAttendees.Add("Contoso Head of Security", "alfred@contoso.com");
    occurrenceToModify.Subject = occurrenceToModify.Subject.ToString() + ":Mandatory";
    // Update the occurrence in your calendar folder and send meeting update requests to attendees.
    // This method call results in an UpdateItem request to EWS.
    occurrenceToModify.Update(ConflictResolutionMode.AlwaysOverwrite, SendInvitationsOrCancellationsMode.SendToAllAndSaveCopy);
    // View updated and deleted occurrences on the recurring master prior to retrieving updated information.
    Console.WriteLine("Modified Occurrences prior to updating recurring master: {0}",
                    (recurrMaster.ModifiedOccurrences == null ? "None" : recurrMaster.ModifiedOccurrences.Count.ToString()));
    // Update the recurring master to view the modified and deleted occurrences.
    recurrMaster = Appointment.Bind(service, recurrenceMasterId, new PropertySet(AppointmentSchema.ModifiedOccurrences,
                                                                        AppointmentSchema.DeletedOccurrences));
    // View updated and deleted occurrences on the recurring master after retrieving updated information.
    Console.WriteLine("Modified Occurrences after updating recurring master:\t {0}",
                    (recurrMaster.ModifiedOccurrences == null ? "None" : recurrMaster.ModifiedOccurrences.Count.ToString()));
    return recurrMaster.Id;            
}

```

## <a name="modify-a-single-occurrence-in-a-series-by-using-ews"></a><span data-ttu-id="32a11-120">Modificar una única incidencia de una serie mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="32a11-120">Modify a single occurrence in a series by using EWS</span></span>

<span data-ttu-id="32a11-121">Modificación de una sola instancia de una serie es básicamente el mismo que la modificación de una cita de una sola instancia.</span><span class="sxs-lookup"><span data-stu-id="32a11-121">Modifying a single instance in a series is essentially the same as modifying a single instance appointment.</span></span> <span data-ttu-id="32a11-122">Puede especificar la aparición para cambiar mediante un [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) o un elemento [OccurrenceItemId](http://msdn.microsoft.com/library/4a15bbc3-5b93-4193-b9ec-da32f0a9a552%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="32a11-122">You can specify the occurrence to change by using either an [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) or an [OccurrenceItemId](http://msdn.microsoft.com/library/4a15bbc3-5b93-4193-b9ec-da32f0a9a552%28Office.15%29.aspx) element.</span></span> 
  
<span data-ttu-id="32a11-123">En el ejemplo siguiente se muestra la solicitud XML al usar la operación [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) para actualizar una ocurrencia en una serie de citas periódicas.</span><span class="sxs-lookup"><span data-stu-id="32a11-123">The following example shows the request XML when you use the [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) operation to update an occurrence in a recurring series of appointments.</span></span> <span data-ttu-id="32a11-124">El **ItemId** y **ChangeKey** son más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="32a11-124">The **ItemId** and **ChangeKey** are shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010" />
  </soap:Header>
  <soap:Body>
    <m:UpdateItem ConflictResolution="AlwaysOverwrite" SendMeetingInvitationsOrCancellations="SendToAllAndSaveCopy">
      <m:ItemChanges>
        <t:ItemChange>
          <t:ItemId Id="AAMkA" ChangeKey="DwAAAB" />
          <t:Updates>
            <t:SetItemField>
              <t:FieldURI FieldURI="calendar:Location" />
              <t:CalendarItem>
                <t:Location>Helipad of Contoso Bldg 1</t:Location>
              </t:CalendarItem>
            </t:SetItemField>
            <t:SetItemField>
              <t:FieldURI FieldURI="calendar:Start" />
              <t:CalendarItem>
                <t:Start>2014-03-27T19:33:00.000-07:00</t:Start>
              </t:CalendarItem>
            </t:SetItemField>
            <t:SetItemField>
              <t:FieldURI FieldURI="calendar:End" />
              <t:CalendarItem>
                <t:End>2014-03-27T20:33:00.000-07:00</t:End>
              </t:CalendarItem>
            </t:SetItemField>
            <t:SetItemField>
              <t:FieldURI FieldURI="calendar:RequiredAttendees" />
              <t:CalendarItem>
                <t:RequiredAttendees>
                  <t:Attendee>
                    <t:Mailbox>
                      <t:Name>Mack@contoso.com</t:Name>
                      <t:EmailAddress>Mack@contoso.com</t:EmailAddress>
                      <t:RoutingType>SMTP</t:RoutingType>
                    </t:Mailbox>
                  </t:Attendee>
                  <t:Attendee>
                    <t:Mailbox>
                      <t:Name>Sadie@contoso.com</t:Name>
                      <t:EmailAddress>Sadie@contoso.com</t:EmailAddress>
                      <t:RoutingType>SMTP</t:RoutingType>
                    </t:Mailbox>
                  </t:Attendee>
                  <t:Attendee>
                    <t:Mailbox>
                      <t:Name>Magdalena@contoso.com</t:Name>
                      <t:EmailAddress>Magdalena@contoso.com</t:EmailAddress>
                      <t:RoutingType>SMTP</t:RoutingType>
                    </t:Mailbox>
                  </t:Attendee>
                  <t:Attendee>
                    <t:Mailbox>
                      <t:Name>Contoso CEO</t:Name>
                      <t:EmailAddress>sadie@contoso</t:EmailAddress>
                    </t:Mailbox>
                  </t:Attendee>
                  <t:Attendee>
                    <t:Mailbox>
                      <t:Name>Contoso Head of Research</t:Name>
                      <t:EmailAddress>ronnie@contoso.com</t:EmailAddress>
                    </t:Mailbox>
                  </t:Attendee>
                  <t:Attendee>
                    <t:Mailbox>
                      <t:Name>Contoso Head of Security</t:Name>
                      <t:EmailAddress>alfred@contoso.com</t:EmailAddress>
                    </t:Mailbox>
                  </t:Attendee>
                </t:RequiredAttendees>
              </t:CalendarItem>
            </t:SetItemField>
            <t:SetItemField>
              <t:FieldURI FieldURI="item:Subject" />
              <t:CalendarItem>
                <t:Subject>Weekly Update Meeting:Mandatory</t:Subject>
              </t:CalendarItem>
            </t:SetItemField>
          </t:Updates>
        </t:ItemChange>
      </m:ItemChanges>
    </m:UpdateItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="32a11-125">El servidor responde a la solicitud de **UpdateItem** con un mensaje de [UpdateItemResponse](http://msdn.microsoft.com/library/023b79b4-c675-4669-9112-d85499ec4fc4%28Office.15%29.aspx) que incluye un valor [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **NoError**, lo que indica que la repetición se ha actualizado correctamente y la [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) de la cita actualizada.</span><span class="sxs-lookup"><span data-stu-id="32a11-125">The server responds to the **UpdateItem** request with an [UpdateItemResponse](http://msdn.microsoft.com/library/023b79b4-c675-4669-9112-d85499ec4fc4%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError**, which indicates that the occurrence was updated successfully, and the [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) of the updated appointment.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="32a11-126">Ver también</span><span class="sxs-lookup"><span data-stu-id="32a11-126">See also</span></span>


- [<span data-ttu-id="32a11-127">Calendarios y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="32a11-127">Calendars and EWS in Exchange</span></span>](calendars-and-ews-in-exchange.md)
    
- [<span data-ttu-id="32a11-128">Actualizar las citas y reuniones con EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="32a11-128">Update appointments and meetings by using EWS in Exchange</span></span>](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="32a11-129">Patrones de periodicidad y EWS</span><span class="sxs-lookup"><span data-stu-id="32a11-129">Recurrence patterns and EWS</span></span>](recurrence-patterns-and-ews.md)
    
- [<span data-ttu-id="32a11-130">Obtener acceso a una serie periódica mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="32a11-130">Access a recurring series by using EWS in Exchange</span></span>](how-to-access-a-recurring-series-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="32a11-131">Creación de una serie periódica mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="32a11-131">Create a recurring series by using EWS in Exchange</span></span>](how-to-create-a-recurring-series-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="32a11-132">Eliminar las citas de una serie periódica mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="32a11-132">Delete appointments in a recurring series by using EWS in Exchange</span></span>](how-to-delete-appointments-in-a-recurring-series-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="32a11-133">Actualización de una serie periódica mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="32a11-133">Update a recurring series by using EWS in Exchange</span></span>](how-to-update-a-recurring-series-by-using-ews-in-exchange.md)
    

