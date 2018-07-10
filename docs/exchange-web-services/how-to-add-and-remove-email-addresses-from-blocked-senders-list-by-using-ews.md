---
title: Agregar y quitar direcciones de correo electrónico de la lista de remitentes bloqueados mediante el uso de EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: b88288ee-6af7-45b5-a55c-5929cd0c16f1
description: Descubra cómo usar la API administrada de EWS o EWS para agregar direcciones de correo electrónico a y quitar de la lista de remitentes bloqueados.
ms.openlocfilehash: c03ed585ebd62802000179d8c837786ba5f9aab4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763015"
---
# <a name="add-and-remove-email-addresses-from-the-blocked-senders-list-by-using-ews-in-exchange"></a><span data-ttu-id="84322-103">Agregar y quitar direcciones de correo electrónico de la lista de remitentes bloqueados mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="84322-103">Add and remove email addresses from the Blocked Senders List by using EWS in Exchange</span></span>

<span data-ttu-id="84322-104">Descubra cómo usar la API administrada de EWS o EWS para agregar direcciones de correo electrónico a y quitar de la lista de remitentes bloqueados.</span><span class="sxs-lookup"><span data-stu-id="84322-104">Find out how to use the EWS Managed API or EWS to add email addresses to and remove them from the Blocked Senders List.</span></span>
  
<span data-ttu-id="84322-105">La lista de remitentes bloqueados en Opciones de correo electrónico no deseado de un usuario proporciona una manera para mover todos los mensajes de correo electrónico de los remitentes especificados a la carpeta correo electrónico no deseado.</span><span class="sxs-lookup"><span data-stu-id="84322-105">The Blocked Senders List in a user's Junk Email options provides a way to move all email messages from specified senders to the Junk Email folder.</span></span> <span data-ttu-id="84322-106">Puede habilitar la API administrada de EWS o aplicación de EWS agregar las direcciones de correo electrónico o quitarlos de la lista de remitentes bloqueados.</span><span class="sxs-lookup"><span data-stu-id="84322-106">You can enable your EWS Managed API or EWS application to add email addresses to or remove them from the Blocked Senders List.</span></span>
  
<span data-ttu-id="84322-107">Tenga en cuenta que debe existir un mensaje desde la dirección de correo electrónico en el buzón del usuario antes de que se puede agregar la dirección de correo electrónico a o quitarlo de la lista de remitentes bloqueados.</span><span class="sxs-lookup"><span data-stu-id="84322-107">Note that a message from the email address must exist in the user's mailbox before you can add the email address to or remove it from the Blocked Senders List.</span></span> <span data-ttu-id="84322-108">El método de la API administrada de EWS [ExchangeService.MarkAsJunk](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice.markasjunk%28v=exchg.80%29.aspx) y la operación de EWS [MarkAsJunk](http://msdn.microsoft.com/library/1f71f04d-56a9-4fee-a4e7-d1034438329e%28Office.15%29.aspx) utilizan una colección de identificadores de elemento.</span><span class="sxs-lookup"><span data-stu-id="84322-108">The [ExchangeService.MarkAsJunk](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice.markasjunk%28v=exchg.80%29.aspx) EWS Managed API method and the [MarkAsJunk](http://msdn.microsoft.com/library/1f71f04d-56a9-4fee-a4e7-d1034438329e%28Office.15%29.aspx) EWS operation use a collection of item IDs.</span></span> <span data-ttu-id="84322-109">El elemento de los identificadores de la colección indican los mensajes en el buzón de correo para la que se debe cambiar el estado de correo electrónico no deseado.</span><span class="sxs-lookup"><span data-stu-id="84322-109">The item IDs in the collection indicate messages in the mailbox for which the junk mail status should be changed.</span></span> 
  
<span data-ttu-id="84322-110">Puede usar los cmdlets [Get-MailboxJunkEmailConfiguration](http://technet.microsoft.com/es-es/library/dd979784%28v=exchg.150%29.aspx) y [Set-MailboxJunkEmailConfiguration](http://technet.microsoft.com/es-es/library/dd979780%28v=exchg.150%29.aspx) Shell de administración de Exchange para tener acceso directamente a la lista de remitentes bloqueados.</span><span class="sxs-lookup"><span data-stu-id="84322-110">You can use the [Get-MailboxJunkEmailConfiguration](http://technet.microsoft.com/es-es/library/dd979784%28v=exchg.150%29.aspx) and [Set-MailboxJunkEmailConfiguration](http://technet.microsoft.com/es-es/library/dd979780%28v=exchg.150%29.aspx) Exchange Management Shell cmdlets to access the Blocked Senders List directly.</span></span> 
  
## <a name="add-an-email-address-to-or-remove-it-from-the-blocked-senders-list-by-using-the-ews-managed-api"></a><span data-ttu-id="84322-111">Agregar una dirección de correo electrónico a o quitarlo de la lista de remitentes bloqueados mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="84322-111">Add an email address to or remove it from the Blocked Senders List by using the EWS Managed API</span></span>
<span data-ttu-id="84322-112"><a name="bk_AddRemoveEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="84322-112"></span></span>

<span data-ttu-id="84322-113">Para agregar el remitente de un mensaje de correo electrónico a la lista de remitentes bloqueados, utilice el método **MarkAsJunk** y establezca el parámetro **isJunk** en **true**.</span><span class="sxs-lookup"><span data-stu-id="84322-113">To add the sender of an email message to the Blocked Senders List, use the **MarkAsJunk** method and set the **isJunk** parameter to **true**.</span></span> <span data-ttu-id="84322-114">Para quitar el remitente de un mensaje de correo electrónico de la lista de remitentes bloqueados, establezca el parámetro **isJunk** en **false**.</span><span class="sxs-lookup"><span data-stu-id="84322-114">To remove the sender of an email message from the Blocked Senders List, set the **isJunk** parameter to **false**.</span></span>
  
<span data-ttu-id="84322-115">En el ejemplo siguiente se muestra cómo utilizar el método **MarkAsJunk** para cambiar el estado de un mensaje no deseado.</span><span class="sxs-lookup"><span data-stu-id="84322-115">The following example shows how to use the **MarkAsJunk** method to change the junk status of a message.</span></span> 
  
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

## <a name="add-an-email-address-to-or-remove-it-from-the-blocked-senders-list-by-using-ews"></a><span data-ttu-id="84322-116">Agregar una dirección de correo electrónico a o quitarlo de la lista de remitentes bloqueados mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="84322-116">Add an email address to or remove it from the Blocked Senders List by using EWS</span></span>
<span data-ttu-id="84322-117"><a name="bk_AddRemoveEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="84322-117"></span></span>

<span data-ttu-id="84322-118">La siguiente solicitud SOAP de EWS marca un elemento como correo no deseado estableciendo el atributo **IsJunk** en el elemento [MarkAsJunk](http://msdn.microsoft.com/library/f06bafc6-7ee3-4b2b-9fd1-7c51328f4729%28Office.15%29.aspx) en **true**.</span><span class="sxs-lookup"><span data-stu-id="84322-118">The following EWS SOAP request marks an item as junk by setting the **IsJunk** attribute on the [MarkAsJunk](http://msdn.microsoft.com/library/f06bafc6-7ee3-4b2b-9fd1-7c51328f4729%28Office.15%29.aspx) element to **true**.</span></span> <span data-ttu-id="84322-119">También se mueve el mensaje a la carpeta correo electrónico no deseado estableciendo el atributo **MoveItem** en el elemento **MarkAsJunk** en **true**.</span><span class="sxs-lookup"><span data-stu-id="84322-119">It also moves the message to the Junk Email folder by setting the **MoveItem** attribute on the **MarkAsJunk** element to **true**.</span></span>
  
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
    <m:MarkAsJunk IsJunk="true" MoveItem="true">
      <m:ItemIds>
        <t:ItemId Id="AAMkADg1OWUwODcyLTg4M2MtNDAyMS05YjI0LTI5ZGM5OTU4Njk3YwBGAAAAAADPriAxh444TpHj2GoQxWQNBwAN+VjmVZl5Rq1ymCq5eFKOAAAAAAENAAAN+VjmVZl5Rq1ymCq5eFKOAAAAAAEuAAA=" 
            ChangeKey="CQAAABYAAAAN+VjmVZl5Rq1ymCq5eFKOAAAAAADi" />
      </m:ItemIds>
    </m:MarkAsJunk>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="84322-120">La respuesta SOAP de EWS siguiente muestra la respuesta correcta.</span><span class="sxs-lookup"><span data-stu-id="84322-120">The following EWS SOAP response shows the successful response.</span></span> <span data-ttu-id="84322-121">El elemento [MovedItemId](http://msdn.microsoft.com/library/7d5425ab-1e75-43d1-b801-802ff5139df6%28Office.15%29.aspx) en la respuesta contiene el identificador de elemento para el elemento después de que se ha movido.</span><span class="sxs-lookup"><span data-stu-id="84322-121">The [MovedItemId](http://msdn.microsoft.com/library/7d5425ab-1e75-43d1-b801-802ff5139df6%28Office.15%29.aspx) element in the response contains the item ID for the item after it was moved.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="712" MinorBuildNumber="22" Version="V2_3" 
        xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:MarkAsJunkResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="see-also"></a><span data-ttu-id="84322-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="84322-122">See also</span></span>

- [<span data-ttu-id="84322-123">Administración de la Bandeja de entrada y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="84322-123">Inbox management and EWS in Exchange</span></span>](inbox-management-and-ews-in-exchange.md)   
- [<span data-ttu-id="84322-124">ExchangeService.MarkAsJunk</span><span class="sxs-lookup"><span data-stu-id="84322-124">ExchangeService.MarkAsJunk</span></span>](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice.markasjunk%28v=exchg.80%29.aspx)   
- [<span data-ttu-id="84322-125">MarkAsJunk Operation</span><span class="sxs-lookup"><span data-stu-id="84322-125">MarkAsJunk operation</span></span>](http://msdn.microsoft.com/library/1f71f04d-56a9-4fee-a4e7-d1034438329e%28Office.15%29.aspx)   
- [<span data-ttu-id="84322-126">Get-MailboxJunkEmailConfiguration</span><span class="sxs-lookup"><span data-stu-id="84322-126">Get-MailboxJunkEmailConfiguration</span></span>](http://technet.microsoft.com/es-es/library/dd979784%28v=exchg.150%29.aspx)   
- [<span data-ttu-id="84322-127">Set-MailboxJunkEmailConfiguration</span><span class="sxs-lookup"><span data-stu-id="84322-127">Set-MailboxJunkEmailConfiguration</span></span>](http://technet.microsoft.com/es-es/library/dd979780%28v=exchg.150%29.aspx) 
- [<span data-ttu-id="84322-128">Shell de administración de Exchange</span><span class="sxs-lookup"><span data-stu-id="84322-128">Exchange Management Shell</span></span>](../management/exchange-management-shell.md)
    

