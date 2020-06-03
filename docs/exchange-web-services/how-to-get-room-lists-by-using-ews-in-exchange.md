---
title: Obtener listas de salas con EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 15980e4a-e41c-4194-829a-cadbdf365bf1
description: Obtenga información sobre cómo obtener una lista de todas las listas de salas de la organización o una sola lista de salas de un servidor de Exchange mediante la API administrada de EWS o EWS.
localization_priority: Priority
ms.openlocfilehash: 7c571b0550f861552cdbe8c5b30138101c9fc788
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455796"
---
# <a name="get-room-lists-by-using-ews-in-exchange"></a><span data-ttu-id="b9f25-103">Obtener listas de salas con EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="b9f25-103">Get room lists by using EWS in Exchange</span></span>

<span data-ttu-id="b9f25-104">Obtenga información sobre cómo obtener una lista de todas las listas de salas de la organización o una sola lista de salas de un servidor de Exchange mediante la API administrada de EWS o EWS.</span><span class="sxs-lookup"><span data-stu-id="b9f25-104">Learn how to get a list of all the room lists in your organization or a single room list from an Exchange server by using the EWS Managed API or EWS.</span></span>
  
<span data-ttu-id="b9f25-105">Puede usar la API administrada de EWS o EWS para obtener información sobre los salones y cómo se agrupan las salas en su organización.</span><span class="sxs-lookup"><span data-stu-id="b9f25-105">You can use the EWS Managed API or EWS to get information about rooms and how the rooms are grouped in your organization.</span></span> <span data-ttu-id="b9f25-106">Las listas de salas no existen de forma predeterminada; el administrador debe crear y organizarlos.</span><span class="sxs-lookup"><span data-stu-id="b9f25-106">Room lists don't exist by default; your administrator needs to create and organize them.</span></span> <span data-ttu-id="b9f25-107">Normalmente, están organizados por ubicación o departamento, como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="b9f25-107">Typically, they're organized by location or department, as shown in the following example.</span></span>
  
<span data-ttu-id="b9f25-108">**Nombres y direcciones de correo electrónico de la lista de salas de Contoso**</span><span class="sxs-lookup"><span data-stu-id="b9f25-108">**Contoso room list names and email addresses**</span></span>

|<span data-ttu-id="b9f25-109">**Nombre de la lista de salas**</span><span class="sxs-lookup"><span data-stu-id="b9f25-109">**Name of room list**</span></span>|<span data-ttu-id="b9f25-110">**Dirección de correo electrónico de la lista de salas**</span><span class="sxs-lookup"><span data-stu-id="b9f25-110">**Email address of room list**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b9f25-111">Edificio 11 lista de salas</span><span class="sxs-lookup"><span data-stu-id="b9f25-111">Building 11 room list</span></span>  <br/> |<span data-ttu-id="b9f25-112">Bldg11rooms@contoso.com</span><span class="sxs-lookup"><span data-stu-id="b9f25-112">Bldg11rooms@contoso.com</span></span>  <br/> |
|<span data-ttu-id="b9f25-113">Lista de salas de conferencia de desarrollo de Ciencias de la salud</span><span class="sxs-lookup"><span data-stu-id="b9f25-113">Health Science Building Conference Room List</span></span>  <br/> |<span data-ttu-id="b9f25-114">HSbldgrooms@contoso.edu</span><span class="sxs-lookup"><span data-stu-id="b9f25-114">HSbldgrooms@contoso.edu</span></span>  <br/> |
|<span data-ttu-id="b9f25-115">Salas de reuniones del piso de cuentas</span><span class="sxs-lookup"><span data-stu-id="b9f25-115">Accounting Floor Meeting Rooms</span></span>  <br/> |<span data-ttu-id="b9f25-116">Acctfloor300@contoso.com</span><span class="sxs-lookup"><span data-stu-id="b9f25-116">Acctfloor300@contoso.com</span></span>  <br/> |
   
<span data-ttu-id="b9f25-117">Cada habitación de una lista de salas tiene un nombre y una dirección de correo electrónico asociados.</span><span class="sxs-lookup"><span data-stu-id="b9f25-117">Each room in a room list has a name and email address associated with it.</span></span>
  
<span data-ttu-id="b9f25-118">**Nombres de salas y direcciones de correo electrónico de Contoso**</span><span class="sxs-lookup"><span data-stu-id="b9f25-118">**Contoso room names and email addresses**</span></span>

|<span data-ttu-id="b9f25-119">**Nombre del salón**</span><span class="sxs-lookup"><span data-stu-id="b9f25-119">**Name of room**</span></span>|<span data-ttu-id="b9f25-120">**Dirección de correo electrónico del salón**</span><span class="sxs-lookup"><span data-stu-id="b9f25-120">**Email address of room**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b9f25-121">Conf Room 11/101 (8) AV</span><span class="sxs-lookup"><span data-stu-id="b9f25-121">Conf Room 11/101 (8) AV</span></span>  <br/> |<span data-ttu-id="b9f25-122">Cf11101@contoso.com</span><span class="sxs-lookup"><span data-stu-id="b9f25-122">Cf11101@contoso.com</span></span>  <br/> |
|<span data-ttu-id="b9f25-123">Laboratorio de demostración de HS (100)</span><span class="sxs-lookup"><span data-stu-id="b9f25-123">HS Demonstration Lab (100)</span></span>  <br/> |<span data-ttu-id="b9f25-124">Hs101@contoso.edu</span><span class="sxs-lookup"><span data-stu-id="b9f25-124">Hs101@contoso.edu</span></span>  <br/> |
|<span data-ttu-id="b9f25-125">Contabilidad 305 WB</span><span class="sxs-lookup"><span data-stu-id="b9f25-125">Accounting 305 WB</span></span>  <br/> |<span data-ttu-id="b9f25-126">Acct305@contoso.com</span><span class="sxs-lookup"><span data-stu-id="b9f25-126">Acct305@contoso.com</span></span>  <br/> |
   
<span data-ttu-id="b9f25-127">Puede obtener una lista que contiene todas las listas de salas con el método de API administrada de EWS [ExchangeService. GetRoomLists](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.getroomlists%28v=exchg.80%29.aspx) o la operación de EWS [GetRoomLists](https://msdn.microsoft.com/library/55d451f9-547f-44ac-872e-9cb220ea7b7c%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b9f25-127">You can get a list that contains all room lists by using either the [ExchangeService.GetRoomLists](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.getroomlists%28v=exchg.80%29.aspx) EWS Managed API method or the [GetRoomLists](https://msdn.microsoft.com/library/55d451f9-547f-44ac-872e-9cb220ea7b7c%28Office.15%29.aspx) EWS operation.</span></span> 
  
<span data-ttu-id="b9f25-128">Puede recuperar una lista de salas única que contenga todas las salas para una ubicación o departamento proporcionando su dirección de correo electrónico mediante el método de la API administrada de EWS de [GetRooms](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.getrooms%28v=exchg.80%29.aspx) o la operación de EWS [GetRooms](https://msdn.microsoft.com/library/5501ddc0-3bfa-4da6-8e15-4223ca5499a3%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b9f25-128">You can retrieve a single room list that contains all the rooms for a location or department by supplying its email address by using the [GetRooms](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.getrooms%28v=exchg.80%29.aspx) EWS Managed API method or the [GetRooms](https://msdn.microsoft.com/library/5501ddc0-3bfa-4da6-8e15-4223ca5499a3%28Office.15%29.aspx) EWS operation.</span></span> <span data-ttu-id="b9f25-129">Cuando tiene una colección de salones asociados con una lista de salas, puede buscar en la colección para identificar la sala o las salas que desee, ya sea por una dirección de correo electrónico o buscando palabras clave en el nombre, como "AV" o "Lab".</span><span class="sxs-lookup"><span data-stu-id="b9f25-129">When you have a collection of rooms associated with a room list, you can then search through the collection to identify the room or rooms you want, either by email address, or by looking for key words in the name, such as "AV", or "Lab".</span></span> 
  
## <a name="get-all-room-lists-by-using-the-ews-managed-api"></a><span data-ttu-id="b9f25-130">Obtener todas las listas de salas mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="b9f25-130">Get all room lists by using the EWS Managed API</span></span>
<span data-ttu-id="b9f25-131"><a name="bk_GetRoomListewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="b9f25-131"><a name="bk_GetRoomListewsma"> </a></span></span>

<span data-ttu-id="b9f25-132">En el siguiente ejemplo se muestra cómo obtener una lista que contiene todas las listas de salas de su organización mediante el método [GetRoomLists](https://msdn.microsoft.com/library/Microsoft.Exchange.WebServices.Data.ExchangeService.GetRoomLists.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b9f25-132">The following example shows how to get a list that contains all the room lists in your organization by using the [GetRoomLists](https://msdn.microsoft.com/library/Microsoft.Exchange.WebServices.Data.ExchangeService.GetRoomLists.aspx) method.</span></span> 
  
<span data-ttu-id="b9f25-133">En este ejemplo se supone que se ha autenticado en un servidor de Exchange y que se ha adquirido un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) denominado **Service**.</span><span class="sxs-lookup"><span data-stu-id="b9f25-133">This example assumes that you have authenticated to an Exchange server and have acquired an [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object named **service**.</span></span> 
  
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

## <a name="get-all-room-lists-by-using-ews"></a><span data-ttu-id="b9f25-134">Obtener todas las listas de salas mediante EWS</span><span class="sxs-lookup"><span data-stu-id="b9f25-134">Get all room lists by using EWS</span></span>
<span data-ttu-id="b9f25-135"><a name="bk_GetRoomListews"> </a></span><span class="sxs-lookup"><span data-stu-id="b9f25-135"><a name="bk_GetRoomListews"> </a></span></span>

<span data-ttu-id="b9f25-136">En el ejemplo siguiente se muestra cómo obtener una colección de todos los [RoomLists](https://msdn.microsoft.com/library/2b190823-b11e-4635-97e4-3aba5865fd05%28Office.15%29.aspx) de la organización mediante el uso de la operación [GetRoomLists](https://msdn.microsoft.com/library/55d451f9-547f-44ac-872e-9cb220ea7b7c%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b9f25-136">The following example shows how to get a collection of all your organization's [RoomLists](https://msdn.microsoft.com/library/2b190823-b11e-4635-97e4-3aba5865fd05%28Office.15%29.aspx) by using the [GetRoomLists](https://msdn.microsoft.com/library/55d451f9-547f-44ac-872e-9cb220ea7b7c%28Office.15%29.aspx) operation.</span></span> <span data-ttu-id="b9f25-137">También es la solicitud XML que la API administrada de EWS envía cuando usa la API administrada de EWS para [obtener todas las listas de salas](#bk_GetRoomListewsma).</span><span class="sxs-lookup"><span data-stu-id="b9f25-137">This is also the XML request that the EWS Managed API sends when you use the EWS Managed API to [get all room lists](#bk_GetRoomListewsma).</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010" />
  </soap:Header>
  <soap:Body>
    <m:GetRoomLists />
  </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="b9f25-138">El servidor responde a la solicitud [GetRoomLists](https://msdn.microsoft.com/library/55d451f9-547f-44ac-872e-9cb220ea7b7c%28Office.15%29.aspx) con un mensaje [GetRoomListsResponse](https://msdn.microsoft.com/library/8c736f68-1026-496a-b12f-c169c078abd0%28Office.15%29.aspx) que contiene las listas de salas de su organización.</span><span class="sxs-lookup"><span data-stu-id="b9f25-138">The server responds to the [GetRoomLists](https://msdn.microsoft.com/library/55d451f9-547f-44ac-872e-9cb220ea7b7c%28Office.15%29.aspx) request with a [GetRoomListsResponse](https://msdn.microsoft.com/library/8c736f68-1026-496a-b12f-c169c078abd0%28Office.15%29.aspx) message that contains the room lists for your organization.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="868" MinorBuildNumber="8" Version="V2_9" 
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetRoomListsResponse ResponseClass="Success" xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                            xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="get-all-the-rooms-in-a-room-list-by-using-the-ews-managed-api"></a><span data-ttu-id="b9f25-139">Obtener todas las salas de una lista de salas mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="b9f25-139">Get all the rooms in a room list by using the EWS Managed API</span></span>
<span data-ttu-id="b9f25-140"><a name="bk_FindRoomewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="b9f25-140"><a name="bk_FindRoomewsma"> </a></span></span>

<span data-ttu-id="b9f25-141">En el ejemplo siguiente se muestra cómo obtener una colección de salas en una lista de salas con el método [GetRooms](https://msdn.microsoft.com/library/Microsoft.Exchange.WebServices.Data.ExchangeService.GetRooms.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b9f25-141">The following example shows how to get a collection of rooms in a room list by using the [GetRooms](https://msdn.microsoft.com/library/Microsoft.Exchange.WebServices.Data.ExchangeService.GetRooms.aspx) method.</span></span> 
  
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

## <a name="get-all-the-rooms-in-a-room-list-by-using-ews"></a><span data-ttu-id="b9f25-142">Obtener todas las salas de una lista de salas con EWS</span><span class="sxs-lookup"><span data-stu-id="b9f25-142">Get all the rooms in a room list by using EWS</span></span>
<span data-ttu-id="b9f25-143"><a name="bk_FindRoomews"> </a></span><span class="sxs-lookup"><span data-stu-id="b9f25-143"><a name="bk_FindRoomews"> </a></span></span>

<span data-ttu-id="b9f25-144">En el ejemplo siguiente se muestra cómo obtener una lista de [salas](https://msdn.microsoft.com/library/57b6079a-3d83-4429-861e-c551e9e1a991%28Office.15%29.aspx) en un [RoomList](https://msdn.microsoft.com/library/cb02bdf0-df9f-4e31-b7dd-cd9f2f2cc2b2%28Office.15%29.aspx) mediante la operación [GetRooms](https://msdn.microsoft.com/library/5501ddc0-3bfa-4da6-8e15-4223ca5499a3%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b9f25-144">The following example shows how to get a list of [rooms](https://msdn.microsoft.com/library/57b6079a-3d83-4429-861e-c551e9e1a991%28Office.15%29.aspx) in a [RoomList](https://msdn.microsoft.com/library/cb02bdf0-df9f-4e31-b7dd-cd9f2f2cc2b2%28Office.15%29.aspx) by using the [GetRooms](https://msdn.microsoft.com/library/5501ddc0-3bfa-4da6-8e15-4223ca5499a3%28Office.15%29.aspx) operation.</span></span> <span data-ttu-id="b9f25-145">También es la solicitud XML que la API administrada de EWS envía cuando usa la API administrada de EWS para [obtener todas las salas en una lista de salas](#bk_FindRoomewsma).</span><span class="sxs-lookup"><span data-stu-id="b9f25-145">This is also the XML request that the EWS Managed API sends when you use the EWS Managed API to [get all the rooms in a room list](#bk_FindRoomewsma).</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="b9f25-146">El servidor responde a la solicitud [GetRooms](https://msdn.microsoft.com/library/5501ddc0-3bfa-4da6-8e15-4223ca5499a3%28Office.15%29.aspx) con un mensaje [GetRoomsResponse](https://msdn.microsoft.com/library/a8c85f65-bb63-4e7a-b0ca-7c9a04560a58%28Office.15%29.aspx) que contiene las salas de la lista de salas.</span><span class="sxs-lookup"><span data-stu-id="b9f25-146">The server responds to the [GetRooms](https://msdn.microsoft.com/library/5501ddc0-3bfa-4da6-8e15-4223ca5499a3%28Office.15%29.aspx) request with a [GetRoomsResponse](https://msdn.microsoft.com/library/a8c85f65-bb63-4e7a-b0ca-7c9a04560a58%28Office.15%29.aspx) message that contains the rooms in the room list.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="873" MinorBuildNumber="9" 
                         Version="V2_9" xmlns:h="http://scemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetRoomsResponse ResponseClass="Success" xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
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

## <a name="see-also"></a><span data-ttu-id="b9f25-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="b9f25-147">See also</span></span>


- [<span data-ttu-id="b9f25-148">Calendarios y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="b9f25-148">Calendars and EWS in Exchange</span></span>](calendars-and-ews-in-exchange.md)
    
- [<span data-ttu-id="b9f25-149">Obtener información de disponibilidad mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="b9f25-149">Get free/busy information by using EWS in Exchange</span></span>](how-to-get-free-busy-information-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="b9f25-150">Crear y administrar buzones de sala</span><span class="sxs-lookup"><span data-stu-id="b9f25-150">Create and Manage Room Mailboxes</span></span>](https://technet.microsoft.com/library/jj215781%28v=exchg.150%29.aspx)
    

