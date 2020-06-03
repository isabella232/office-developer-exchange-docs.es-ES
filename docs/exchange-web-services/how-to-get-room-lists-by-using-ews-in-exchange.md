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
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455796"
---
# <a name="get-room-lists-by-using-ews-in-exchange"></a>Obtener listas de salas con EWS en Exchange

Obtenga información sobre cómo obtener una lista de todas las listas de salas de la organización o una sola lista de salas de un servidor de Exchange mediante la API administrada de EWS o EWS.
  
Puede usar la API administrada de EWS o EWS para obtener información sobre los salones y cómo se agrupan las salas en su organización. Las listas de salas no existen de forma predeterminada; el administrador debe crear y organizarlos. Normalmente, están organizados por ubicación o departamento, como se muestra en el ejemplo siguiente.
  
**Nombres y direcciones de correo electrónico de la lista de salas de Contoso**

|**Nombre de la lista de salas**|**Dirección de correo electrónico de la lista de salas**|
|:-----|:-----|
|Edificio 11 lista de salas  <br/> |Bldg11rooms@contoso.com  <br/> |
|Lista de salas de conferencia de desarrollo de Ciencias de la salud  <br/> |HSbldgrooms@contoso.edu  <br/> |
|Salas de reuniones del piso de cuentas  <br/> |Acctfloor300@contoso.com  <br/> |
   
Cada habitación de una lista de salas tiene un nombre y una dirección de correo electrónico asociados.
  
**Nombres de salas y direcciones de correo electrónico de Contoso**

|**Nombre del salón**|**Dirección de correo electrónico del salón**|
|:-----|:-----|
|Conf Room 11/101 (8) AV  <br/> |Cf11101@contoso.com  <br/> |
|Laboratorio de demostración de HS (100)  <br/> |Hs101@contoso.edu  <br/> |
|Contabilidad 305 WB  <br/> |Acct305@contoso.com  <br/> |
   
Puede obtener una lista que contiene todas las listas de salas con el método de API administrada de EWS [ExchangeService. GetRoomLists](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.getroomlists%28v=exchg.80%29.aspx) o la operación de EWS [GetRoomLists](https://msdn.microsoft.com/library/55d451f9-547f-44ac-872e-9cb220ea7b7c%28Office.15%29.aspx) . 
  
Puede recuperar una lista de salas única que contenga todas las salas para una ubicación o departamento proporcionando su dirección de correo electrónico mediante el método de la API administrada de EWS de [GetRooms](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.getrooms%28v=exchg.80%29.aspx) o la operación de EWS [GetRooms](https://msdn.microsoft.com/library/5501ddc0-3bfa-4da6-8e15-4223ca5499a3%28Office.15%29.aspx) . Cuando tiene una colección de salones asociados con una lista de salas, puede buscar en la colección para identificar la sala o las salas que desee, ya sea por una dirección de correo electrónico o buscando palabras clave en el nombre, como "AV" o "Lab". 
  
## <a name="get-all-room-lists-by-using-the-ews-managed-api"></a>Obtener todas las listas de salas mediante la API administrada de EWS
<a name="bk_GetRoomListewsma"> </a>

En el siguiente ejemplo se muestra cómo obtener una lista que contiene todas las listas de salas de su organización mediante el método [GetRoomLists](https://msdn.microsoft.com/library/Microsoft.Exchange.WebServices.Data.ExchangeService.GetRoomLists.aspx) . 
  
En este ejemplo se supone que se ha autenticado en un servidor de Exchange y que se ha adquirido un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) denominado **Service**. 
  
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

## <a name="get-all-room-lists-by-using-ews"></a>Obtener todas las listas de salas mediante EWS
<a name="bk_GetRoomListews"> </a>

En el ejemplo siguiente se muestra cómo obtener una colección de todos los [RoomLists](https://msdn.microsoft.com/library/2b190823-b11e-4635-97e4-3aba5865fd05%28Office.15%29.aspx) de la organización mediante el uso de la operación [GetRoomLists](https://msdn.microsoft.com/library/55d451f9-547f-44ac-872e-9cb220ea7b7c%28Office.15%29.aspx) . También es la solicitud XML que la API administrada de EWS envía cuando usa la API administrada de EWS para [obtener todas las listas de salas](#bk_GetRoomListewsma).
  
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

El servidor responde a la solicitud [GetRoomLists](https://msdn.microsoft.com/library/55d451f9-547f-44ac-872e-9cb220ea7b7c%28Office.15%29.aspx) con un mensaje [GetRoomListsResponse](https://msdn.microsoft.com/library/8c736f68-1026-496a-b12f-c169c078abd0%28Office.15%29.aspx) que contiene las listas de salas de su organización. 
  
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

## <a name="get-all-the-rooms-in-a-room-list-by-using-the-ews-managed-api"></a>Obtener todas las salas de una lista de salas mediante la API administrada de EWS
<a name="bk_FindRoomewsma"> </a>

En el ejemplo siguiente se muestra cómo obtener una colección de salas en una lista de salas con el método [GetRooms](https://msdn.microsoft.com/library/Microsoft.Exchange.WebServices.Data.ExchangeService.GetRooms.aspx) . 
  
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

## <a name="get-all-the-rooms-in-a-room-list-by-using-ews"></a>Obtener todas las salas de una lista de salas con EWS
<a name="bk_FindRoomews"> </a>

En el ejemplo siguiente se muestra cómo obtener una lista de [salas](https://msdn.microsoft.com/library/57b6079a-3d83-4429-861e-c551e9e1a991%28Office.15%29.aspx) en un [RoomList](https://msdn.microsoft.com/library/cb02bdf0-df9f-4e31-b7dd-cd9f2f2cc2b2%28Office.15%29.aspx) mediante la operación [GetRooms](https://msdn.microsoft.com/library/5501ddc0-3bfa-4da6-8e15-4223ca5499a3%28Office.15%29.aspx) . También es la solicitud XML que la API administrada de EWS envía cuando usa la API administrada de EWS para [obtener todas las salas en una lista de salas](#bk_FindRoomewsma).
  
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

El servidor responde a la solicitud [GetRooms](https://msdn.microsoft.com/library/5501ddc0-3bfa-4da6-8e15-4223ca5499a3%28Office.15%29.aspx) con un mensaje [GetRoomsResponse](https://msdn.microsoft.com/library/a8c85f65-bb63-4e7a-b0ca-7c9a04560a58%28Office.15%29.aspx) que contiene las salas de la lista de salas. 
  
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

## <a name="see-also"></a>Vea también


- [Calendarios y EWS en Exchange](calendars-and-ews-in-exchange.md)
    
- [Obtener información de disponibilidad mediante EWS en Exchange](how-to-get-free-busy-information-by-using-ews-in-exchange.md)
    
- [Crear y administrar buzones de sala](https://technet.microsoft.com/library/jj215781%28v=exchg.150%29.aspx)
    

