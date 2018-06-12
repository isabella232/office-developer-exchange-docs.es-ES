---
title: Obtener listas de las salas mediante el uso de EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 15980e4a-e41c-4194-829a-cadbdf365bf1
description: Obtenga información sobre cómo obtener una lista de todas las listas de sala en la organización o una lista de salas único desde un servidor de Exchange mediante el uso de la API administrada de EWS o EWS.
ms.openlocfilehash: 404a31fb6c8d98bdbba4c79ed6912c333a44d04b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763069"
---
# <a name="get-room-lists-by-using-ews-in-exchange"></a><span data-ttu-id="7195e-103">Obtener listas de las salas mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="7195e-103">Get room lists by using EWS in Exchange</span></span>

<span data-ttu-id="7195e-104">Obtenga información sobre cómo obtener una lista de todas las listas de sala en la organización o una lista de salas único desde un servidor de Exchange mediante el uso de la API administrada de EWS o EWS.</span><span class="sxs-lookup"><span data-stu-id="7195e-104">Learn how to get a list of all the room lists in your organization or a single room list from an Exchange server by using the EWS Managed API or EWS.</span></span>
  
<span data-ttu-id="7195e-105">Puede usar la API administrada de EWS o EWS para obtener información sobre salones y cómo se agrupan las salas en su organización.</span><span class="sxs-lookup"><span data-stu-id="7195e-105">You can use the EWS Managed API or EWS to get information about rooms and how the rooms are grouped in your organization.</span></span> <span data-ttu-id="7195e-106">No existen listas de las salas de forma predeterminada; el administrador debe crear y organícelas.</span><span class="sxs-lookup"><span data-stu-id="7195e-106">Room lists don't exist by default; your administrator needs to create and organize them.</span></span> <span data-ttu-id="7195e-107">Normalmente, está organizadas por ubicación o departamento, tal como se muestra en el siguiente ejemplo.</span><span class="sxs-lookup"><span data-stu-id="7195e-107">Typically, they're organized by location or department, as shown in the following example.</span></span>
  
<span data-ttu-id="7195e-108">**Contoso sala lista de los nombres y direcciones de correo electrónico**</span><span class="sxs-lookup"><span data-stu-id="7195e-108">**Contoso room list names and email addresses**</span></span>

|<span data-ttu-id="7195e-109">**Nombre de la lista de salas**</span><span class="sxs-lookup"><span data-stu-id="7195e-109">**Name of room list**</span></span>|<span data-ttu-id="7195e-110">**Dirección de correo electrónico de la lista de salas**</span><span class="sxs-lookup"><span data-stu-id="7195e-110">**Email address of room list**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7195e-111">Lista de salas 11 de creación</span><span class="sxs-lookup"><span data-stu-id="7195e-111">Building 11 room list</span></span>  <br/> |<span data-ttu-id="7195e-112">Bldg11rooms@contoso.com</span><span class="sxs-lookup"><span data-stu-id="7195e-112">Bldg11rooms@contoso.com</span></span>  <br/> |
|<span data-ttu-id="7195e-113">Lista de salas de conferencia de creación de ciencias de mantenimiento</span><span class="sxs-lookup"><span data-stu-id="7195e-113">Health Science Building Conference Room List</span></span>  <br/> |<span data-ttu-id="7195e-114">HSbldgrooms@contoso.edu</span><span class="sxs-lookup"><span data-stu-id="7195e-114">HSbldgrooms@contoso.edu</span></span>  <br/> |
|<span data-ttu-id="7195e-115">Salas de reuniones de planta de contabilidad</span><span class="sxs-lookup"><span data-stu-id="7195e-115">Accounting Floor Meeting Rooms</span></span>  <br/> |<span data-ttu-id="7195e-116">Acctfloor300@contoso.com</span><span class="sxs-lookup"><span data-stu-id="7195e-116">Acctfloor300@contoso.com</span></span>  <br/> |
   
<span data-ttu-id="7195e-117">Cada sala en una lista de salas tiene asociada una dirección de nombre y correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="7195e-117">Each room in a room list has a name and email address associated with it.</span></span>
  
<span data-ttu-id="7195e-118">**Nombre del salón de Contoso y direcciones de correo electrónico**</span><span class="sxs-lookup"><span data-stu-id="7195e-118">**Contoso room names and email addresses**</span></span>

|<span data-ttu-id="7195e-119">**Nombre del salón**</span><span class="sxs-lookup"><span data-stu-id="7195e-119">**Name of room**</span></span>|<span data-ttu-id="7195e-120">**Dirección de correo electrónico de salón**</span><span class="sxs-lookup"><span data-stu-id="7195e-120">**Email address of room**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7195e-121">Sala conf 11/101 (8) AV</span><span class="sxs-lookup"><span data-stu-id="7195e-121">Conf Room 11/101 (8) AV</span></span>  <br/> |<span data-ttu-id="7195e-122">Cf11101@contoso.com</span><span class="sxs-lookup"><span data-stu-id="7195e-122">Cf11101@contoso.com</span></span>  <br/> |
|<span data-ttu-id="7195e-123">Laboratorio de demostración de SA (100)</span><span class="sxs-lookup"><span data-stu-id="7195e-123">HS Demonstration Lab (100)</span></span>  <br/> |<span data-ttu-id="7195e-124">Hs101@contoso.edu</span><span class="sxs-lookup"><span data-stu-id="7195e-124">Hs101@contoso.edu</span></span>  <br/> |
|<span data-ttu-id="7195e-125">Contabilidad 305 WB</span><span class="sxs-lookup"><span data-stu-id="7195e-125">Accounting 305 WB</span></span>  <br/> |<span data-ttu-id="7195e-126">Acct305@contoso.com</span><span class="sxs-lookup"><span data-stu-id="7195e-126">Acct305@contoso.com</span></span>  <br/> |
   
<span data-ttu-id="7195e-127">Puede obtener una lista que contiene todas las listas de las salas mediante el método de la API administrada de EWS [ExchangeService.GetRoomLists](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.getroomlists%28v=exchg.80%29.aspx) o la operación de EWS [GetRoomLists](http://msdn.microsoft.com/library/55d451f9-547f-44ac-872e-9cb220ea7b7c%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="7195e-127">You can get a list that contains all room lists by using either the [ExchangeService.GetRoomLists](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.getroomlists%28v=exchg.80%29.aspx) EWS Managed API method or the [GetRoomLists](http://msdn.microsoft.com/library/55d451f9-547f-44ac-872e-9cb220ea7b7c%28Office.15%29.aspx) EWS operation.</span></span> 
  
<span data-ttu-id="7195e-128">Puede recuperar una lista de salas único que contiene todas las salas para una ubicación o un departamento proporcionando su dirección de correo electrónico mediante el método de la API administrada de EWS [GetRooms](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.getrooms%28v=exchg.80%29.aspx) o la operación de EWS [GetRooms](http://msdn.microsoft.com/library/5501ddc0-3bfa-4da6-8e15-4223ca5499a3%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="7195e-128">You can retrieve a single room list that contains all the rooms for a location or department by supplying its email address by using the [GetRooms](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.getrooms%28v=exchg.80%29.aspx) EWS Managed API method or the [GetRooms](http://msdn.microsoft.com/library/5501ddc0-3bfa-4da6-8e15-4223ca5499a3%28Office.15%29.aspx) EWS operation.</span></span> <span data-ttu-id="7195e-129">Cuando haya una colección de salones asociado con una lista de salas, a continuación, puede buscar a través de la colección que se va a identificar la sala o salas que desee, ya sea por la dirección de correo electrónico o mediante la búsqueda de palabras clave en el nombre, como "AV" o "Laboratorio".</span><span class="sxs-lookup"><span data-stu-id="7195e-129">When you have a collection of rooms associated with a room list, you can then search through the collection to identify the room or rooms you want, either by email address, or by looking for key words in the name, such as "AV", or "Lab".</span></span> 
  
## <a name="get-all-room-lists-by-using-the-ews-managed-api"></a><span data-ttu-id="7195e-130">Obtener todas las listas de las salas mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="7195e-130">Get all room lists by using the EWS Managed API</span></span>
<span data-ttu-id="7195e-131"><a name="bk_GetRoomListewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="7195e-131"></span></span>

<span data-ttu-id="7195e-132">En el ejemplo siguiente se muestra cómo obtener una lista que contiene todas las listas de sala en la organización mediante el método [GetRoomLists](https://msdn.microsoft.com/library/Microsoft.Exchange.WebServices.Data.ExchangeService.GetRoomLists.aspx) .</span><span class="sxs-lookup"><span data-stu-id="7195e-132">The following example shows how to get a list that contains all the room lists in your organization by using the [GetRoomLists](https://msdn.microsoft.com/library/Microsoft.Exchange.WebServices.Data.ExchangeService.GetRoomLists.aspx) method.</span></span> 
  
<span data-ttu-id="7195e-133">En este ejemplo se supone que se han autenticado a un servidor de Exchange y ha adquirido un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) con el nombre de **servicio**.</span><span class="sxs-lookup"><span data-stu-id="7195e-133">This example assumes that you have authenticated to an Exchange server and have acquired an [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object named **service**.</span></span> 
  
```cs
// Return all the room lists in the organization.
// This method call results in a GetRoomLists call to EWS.
EmailAddressCollection myRoomLists = service.GetRoomLists();
// Display the room lists.
foreach (EmailAddress address in myRoomLists)
{
    Console.WriteLine("Email Address: {0} Mailbox Type: {1}", address.Address, address.MailboxType);
}

```

## <a name="get-all-room-lists-by-using-ews"></a><span data-ttu-id="7195e-134">Obtener todas las listas de las salas mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="7195e-134">Get all room lists by using EWS</span></span>
<span data-ttu-id="7195e-135"><a name="bk_GetRoomListews"> </a></span><span class="sxs-lookup"><span data-stu-id="7195e-135"></span></span>

<span data-ttu-id="7195e-136">En el ejemplo siguiente se muestra cómo obtener una colección de todos los de su organización [RoomLists](http://msdn.microsoft.com/library/2b190823-b11e-4635-97e4-3aba5865fd05%28Office.15%29.aspx) mediante la operación [GetRoomLists](http://msdn.microsoft.com/library/55d451f9-547f-44ac-872e-9cb220ea7b7c%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="7195e-136">The following example shows how to get a collection of all your organization's [RoomLists](http://msdn.microsoft.com/library/2b190823-b11e-4635-97e4-3aba5865fd05%28Office.15%29.aspx) by using the [GetRoomLists](http://msdn.microsoft.com/library/55d451f9-547f-44ac-872e-9cb220ea7b7c%28Office.15%29.aspx) operation.</span></span> <span data-ttu-id="7195e-137">También es la solicitud XML que la API administrada de EWS envía al usar la API administrada de EWS para [obtener todas las listas de las salas](#bk_GetRoomListewsma).</span><span class="sxs-lookup"><span data-stu-id="7195e-137">This is also the XML request that the EWS Managed API sends when you use the EWS Managed API to [get all room lists](#bk_GetRoomListewsma).</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010" />
  </soap:Header>
  <soap:Body>
    <m:GetRoomLists />
  </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="7195e-138">El servidor responde a la solicitud de [GetRoomLists](http://msdn.microsoft.com/library/55d451f9-547f-44ac-872e-9cb220ea7b7c%28Office.15%29.aspx) con un mensaje de [GetRoomListsResponse](http://msdn.microsoft.com/library/8c736f68-1026-496a-b12f-c169c078abd0%28Office.15%29.aspx) que contiene las listas de las salas para su organización.</span><span class="sxs-lookup"><span data-stu-id="7195e-138">The server responds to the [GetRoomLists](http://msdn.microsoft.com/library/55d451f9-547f-44ac-872e-9cb220ea7b7c%28Office.15%29.aspx) request with a [GetRoomListsResponse](http://msdn.microsoft.com/library/8c736f68-1026-496a-b12f-c169c078abd0%28Office.15%29.aspx) message that contains the room lists for your organization.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="868" MinorBuildNumber="8" Version="V2_9" 
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetRoomListsResponse ResponseClass="Success" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                            xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseCode>NoError</m:ResponseCode>
      <m:RoomLists>
        <t:Address>
          <t:Name>Contoso Building 1 Room List</t:Name>
          <t:EmailAddress>bldg1rooms@contoso.com</t:EmailAddress>
          <t:RoutingType>SMTP</t:RoutingType>
          <t:MailboxType>PublicDL</t:MailboxType>
        </t:Address>
        <t:Address>
          <t:Name>Contoso Building 2 Room List</t:Name>
          <t:EmailAddress>bldg2rooms@contoso.com</t:EmailAddress>
          <t:RoutingType>SMTP</t:RoutingType>
          <t:MailboxType>PublicDL</t:MailboxType>
        </t:Address>
        <t:Address>
          <t:Name>Contoso Building 3 Room List</t:Name>
          <t:EmailAddress>bldg3rooms@contoso.com</t:EmailAddress>
          <t:RoutingType>SMTP</t:RoutingType>
          <t:MailboxType>PublicDL</t:MailboxType>
        </t:Address>
      </m:RoomLists>
    </m:GetRoomListsResponse>
  </s:Body>
</s:Envelope>

```

## <a name="get-all-the-rooms-in-a-room-list-by-using-the-ews-managed-api"></a><span data-ttu-id="7195e-139">Obtener todas las salas de una lista de salas mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="7195e-139">Get all the rooms in a room list by using the EWS Managed API</span></span>
<span data-ttu-id="7195e-140"><a name="bk_FindRoomewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="7195e-140"></span></span>

<span data-ttu-id="7195e-141">En el ejemplo siguiente se muestra cómo obtener una colección de salas en una lista de salas mediante el método [GetRooms](https://msdn.microsoft.com/library/Microsoft.Exchange.WebServices.Data.ExchangeService.GetRooms.aspx) .</span><span class="sxs-lookup"><span data-stu-id="7195e-141">The following example shows how to get a collection of rooms in a room list by using the [GetRooms](https://msdn.microsoft.com/library/Microsoft.Exchange.WebServices.Data.ExchangeService.GetRooms.aspx) method.</span></span> 
  
```cs
EmailAddress myRoomList = "bldg3rooms@contoso.com";
// This method call results in a GetRooms call to EWS.
System.Collections.ObjectModel.Collection<EmailAddress> myRoomAddresses = service.GetRooms(myRoomList);
// Display the individual rooms.
foreach (EmailAddress address in myRoomAddresses)
{
    Console.WriteLine("Email Address: {0}", address.Address);
}

```

## <a name="get-all-the-rooms-in-a-room-list-by-using-ews"></a><span data-ttu-id="7195e-142">Obtener todas las salas de una lista de salas mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="7195e-142">Get all the rooms in a room list by using EWS</span></span>
<span data-ttu-id="7195e-143"><a name="bk_FindRoomews"> </a></span><span class="sxs-lookup"><span data-stu-id="7195e-143"></span></span>

<span data-ttu-id="7195e-144">En el ejemplo siguiente se muestra cómo obtener una lista de [salas](http://msdn.microsoft.com/library/57b6079a-3d83-4429-861e-c551e9e1a991%28Office.15%29.aspx) en una [RoomList](http://msdn.microsoft.com/library/cb02bdf0-df9f-4e31-b7dd-cd9f2f2cc2b2%28Office.15%29.aspx) mediante la operación [GetRooms](http://msdn.microsoft.com/library/5501ddc0-3bfa-4da6-8e15-4223ca5499a3%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="7195e-144">The following example shows how to get a list of [rooms](http://msdn.microsoft.com/library/57b6079a-3d83-4429-861e-c551e9e1a991%28Office.15%29.aspx) in a [RoomList](http://msdn.microsoft.com/library/cb02bdf0-df9f-4e31-b7dd-cd9f2f2cc2b2%28Office.15%29.aspx) by using the [GetRooms](http://msdn.microsoft.com/library/5501ddc0-3bfa-4da6-8e15-4223ca5499a3%28Office.15%29.aspx) operation.</span></span> <span data-ttu-id="7195e-145">También es la solicitud XML que la API administrada de EWS envía al usar la API administrada de EWS para [obtener todas las salas de una lista de salas](#bk_FindRoomewsma).</span><span class="sxs-lookup"><span data-stu-id="7195e-145">This is also the XML request that the EWS Managed API sends when you use the EWS Managed API to [get all the rooms in a room list](#bk_FindRoomewsma).</span></span>
  
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
    <m:GetRooms>
      <m:RoomList>
        <t:EmailAddress>bldg3rooms@contoso.com</t:EmailAddress>
      </m:RoomList>
    </m:GetRooms>
  </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="7195e-146">El servidor responde a la solicitud de [GetRooms](http://msdn.microsoft.com/library/5501ddc0-3bfa-4da6-8e15-4223ca5499a3%28Office.15%29.aspx) con un mensaje de [GetRoomsResponse](http://msdn.microsoft.com/library/a8c85f65-bb63-4e7a-b0ca-7c9a04560a58%28Office.15%29.aspx) que contiene las salas en la lista de salas.</span><span class="sxs-lookup"><span data-stu-id="7195e-146">The server responds to the [GetRooms](http://msdn.microsoft.com/library/5501ddc0-3bfa-4da6-8e15-4223ca5499a3%28Office.15%29.aspx) request with a [GetRoomsResponse](http://msdn.microsoft.com/library/a8c85f65-bb63-4e7a-b0ca-7c9a04560a58%28Office.15%29.aspx) message that contains the rooms in the room list.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="873" MinorBuildNumber="9" 
                         Version="V2_9" xmlns:h="http://scemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetRoomsResponse ResponseClass="Success" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://scemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseCode>NoError</m:ResponseCode>
      <m:Rooms>
        <t:Room>
          <t:Id>
            <t:Name>Conf Room 3/101 (16) AV</t:Name>
            <t:EmailAddress>cf3101@contoso.com</t:EmailAddress>
            <t:RoutingType>SMTP</t:RoutingType>
            <t:MailboxType>Mailbox</t:MailboxType>
          </t:Id>
        </t:Room>
        <t:Room>
          <t:Id>
            <t:Name>Conf Room 3/102 (8) AV</t:Name>
            <t:EmailAddress>cf3102@contoso.com</t:EmailAddress>
            <t:RoutingType>SMTP</t:RoutingType>
            <t:MailboxType>Mailbox</t:MailboxType>
          </t:Id>
        </t:Room>
        <t:Room>
          <t:Id>
            <t:Name>Conf Room 3/103 (14) AV RoundTable</t:Name>
            <t:EmailAddress>cf3103@contoso.com</t:EmailAddress>
            <t:RoutingType>SMTP</t:RoutingType>
            <t:MailboxType>Mailbox</t:MailboxType>
          </t:Id>
        </t:Room>
      </m:Rooms>
    </m:GetRoomsResponse>
  </s:Body>
</s:Envelope>

```

## <a name="see-also"></a><span data-ttu-id="7195e-147">Ver también</span><span class="sxs-lookup"><span data-stu-id="7195e-147">See also</span></span>


- [<span data-ttu-id="7195e-148">Calendarios y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="7195e-148">Calendars and EWS in Exchange</span></span>](calendars-and-ews-in-exchange.md)
    
- [<span data-ttu-id="7195e-149">Obtener información de disponibilidad con EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="7195e-149">Get free/busy information by using EWS in Exchange</span></span>](how-to-get-free-busy-information-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="7195e-150">Crear y administrar buzones de sala</span><span class="sxs-lookup"><span data-stu-id="7195e-150">Create and Manage Room Mailboxes</span></span>](http://technet.microsoft.com/en-us/library/jj215781%28v=exchg.150%29.aspx)
    

