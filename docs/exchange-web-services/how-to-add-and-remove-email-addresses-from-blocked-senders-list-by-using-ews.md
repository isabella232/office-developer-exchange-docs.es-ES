---
title: Agregar y quitar direcciones de correo electrónico de la lista de remitentes bloqueados mediante el uso de EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: b88288ee-6af7-45b5-a55c-5929cd0c16f1
description: Descubra cómo usar la API administrada ews o EWS para agregar direcciones de correo electrónico y quitarlas de la lista de remitentes bloqueados.
ms.openlocfilehash: 4deacbfa6e146675e3248e3932734a1492645246
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59512208"
---
# <a name="add-and-remove-email-addresses-from-the-blocked-senders-list-by-using-ews-in-exchange"></a>Agregar y quitar direcciones de correo electrónico de la lista de remitentes bloqueados mediante el uso de EWS en Exchange

Descubra cómo usar la API administrada ews o EWS para agregar direcciones de correo electrónico y quitarlas de la lista de remitentes bloqueados.
  
La lista de remitentes bloqueados en las opciones de correo no deseado de un usuario proporciona una forma de mover todos los mensajes de correo electrónico de remitentes especificados a la carpeta Correo no deseado. Puede habilitar la API administrada ews o la aplicación EWS para agregar direcciones de correo electrónico o quitarlas de la lista de remitentes bloqueados.
  
Tenga en cuenta que debe existir un mensaje de la dirección de correo electrónico en el buzón del usuario para poder agregar la dirección de correo electrónico o quitarla de la lista de remitentes bloqueados. El método de API administrada EWS [ExchangeService.MarkAsJunk](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.markasjunk%28v=exchg.80%29.aspx) y la [operación EWS MarkAsJunk](https://msdn.microsoft.com/library/1f71f04d-56a9-4fee-a4e7-d1034438329e%28Office.15%29.aspx) usan una colección de IDs de elementos. Los IDs de elementos de la colección indican los mensajes del buzón para los que se debe cambiar el estado del correo no deseado. 
  
Puede usar los cmdlets [Get-MailboxJunkEmailConfiguration](https://technet.microsoft.com/library/dd979784%28v=exchg.150%29.aspx) y [Set-MailboxJunkEmailConfiguration](https://technet.microsoft.com/library/dd979780%28v=exchg.150%29.aspx) Exchange Shell de administración para obtener acceso directamente a la lista de remitentes bloqueados. 
  
## <a name="add-an-email-address-to-or-remove-it-from-the-blocked-senders-list-by-using-the-ews-managed-api"></a>Agregar o quitar una dirección de correo electrónico de la lista de remitentes bloqueados mediante la API administrada de EWS
<a name="bk_AddRemoveEWSMA"> </a>

Para agregar el remitente de un mensaje de correo electrónico a la lista de remitentes bloqueados, use el **método MarkAsJunk** y establezca el **parámetro isJunk** en **true**. Para quitar el remitente de un mensaje de correo electrónico de la lista de remitentes bloqueados, establezca el **parámetro isJunk** en **false**.
  
En el ejemplo siguiente se muestra cómo usar el **método MarkAsJunk** para cambiar el estado de correo no deseado de un mensaje. 
  
```cs
private static void MarkMessageAsJunk(ExchangeService service, ItemId messageId, bool isJunk, bool moveItem)
{
    List<ItemId> junkItemIds = new List<ItemId>();
    junkItemIds.Add(messageId);
    ServiceResponseCollection<MarkAsJunkResponse> responseCollection = null;
    try
    {
        // If isJunk is true, the sender of the email message is added to 
        // the Blocked Senders List. If isJunk is false, the sender is removed
        // from the list (if present).
        responseCollection = service.MarkAsJunk(junkItemIds, isJunk, moveItem);
    }
    catch (ServiceResponseException ex)
    {
        Console.WriteLine("Error marking item as junk: {0}", ex.ErrorCode);
        return;
    }
    foreach (MarkAsJunkResponse response in responseCollection)
    {
        if (response.Result == ServiceResult.Success)
        {
            Console.WriteLine("Successfully marked message as {0}junk.", isJunk ? "": "NOT ");
            if (moveItem)
            {
                Console.WriteLine("New item ID: {0}", response.MovedItemId.ToString());
            }
        }
        else
        {
            Console.WriteLine("[{0}]: {1}", response.Result.ToString(),
                response.ErrorCode.ToString());
        }
    }
}
```

## <a name="add-an-email-address-to-or-remove-it-from-the-blocked-senders-list-by-using-ews"></a>Agregar o quitar una dirección de correo electrónico de la lista de remitentes bloqueados mediante EWS
<a name="bk_AddRemoveEWS"> </a>

La siguiente solicitud SOAP de EWS marca un elemento como correo no deseado estableciendo el atributo **IsJunk** en el [elemento MarkAsJunk](https://msdn.microsoft.com/library/f06bafc6-7ee3-4b2b-9fd1-7c51328f4729%28Office.15%29.aspx) en **true**. También mueve el mensaje a la carpeta Correo no deseado estableciendo el atributo **MoveItem** en el **elemento MarkAsJunk** en **true**.
  
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
    <m:MarkAsJunk IsJunk="true" MoveItem="true">
      <m:ItemIds>
        <t:ItemId Id="AAMkADg1OWUwODcyLTg4M2MtNDAyMS05YjI0LTI5ZGM5OTU4Njk3YwBGAAAAAADPriAxh444TpHj2GoQxWQNBwAN+VjmVZl5Rq1ymCq5eFKOAAAAAAENAAAN+VjmVZl5Rq1ymCq5eFKOAAAAAAEuAAA=" 
            ChangeKey="CQAAABYAAAAN+VjmVZl5Rq1ymCq5eFKOAAAAAADi" />
      </m:ItemIds>
    </m:MarkAsJunk>
  </soap:Body>
</soap:Envelope>
```

La siguiente respuesta SOAP de EWS muestra la respuesta correcta. El [elemento MovedItemId](https://msdn.microsoft.com/library/7d5425ab-1e75-43d1-b801-802ff5139df6%28Office.15%29.aspx) de la respuesta contiene el identificador de elemento del elemento después de moverlo. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="712" MinorBuildNumber="22" Version="V2_3" 
        xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:MarkAsJunkResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:MarkAsJunkResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:MovedItemId Id="AAMkADg1OWUwODcyLTg4M2MtNDAyMS05YjI0LTI5ZGM5OTU4Njk3YwBGAAAAAADPriAxh444TpHj2GoQxWQNBwAN+VjmVZl5Rq1ymCq5eFKOAAAAAAEbAAAN+VjmVZl5Rq1ymCq5eFKOAAAE59DIAAA="
              ChangeKey="CQAAABYAAAAN+VjmVZl5Rq1ymCq5eFKOAAAE59E+" />
        </m:MarkAsJunkResponseMessage>
      </m:ResponseMessages>
    </m:MarkAsJunkResponse>
  </s:Body>
</s:Envelope>
```

## <a name="see-also"></a>Vea también

- [Administración de la Bandeja de entrada y EWS en Exchange](inbox-management-and-ews-in-exchange.md)   
- [ExchangeService.MarkAsJunk](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.markasjunk%28v=exchg.80%29.aspx)   
- [Operación MarkAsJunk](https://msdn.microsoft.com/library/1f71f04d-56a9-4fee-a4e7-d1034438329e%28Office.15%29.aspx)   
- [Get-MailboxJunkEmailConfiguration](https://technet.microsoft.com/library/dd979784%28v=exchg.150%29.aspx)   
- [Set-MailboxJunkEmailConfiguration](https://technet.microsoft.com/library/dd979780%28v=exchg.150%29.aspx) 
- [Exchange Management Shell](../management/exchange-management-shell.md)
    

