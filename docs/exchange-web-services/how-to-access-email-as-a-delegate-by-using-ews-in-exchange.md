---
title: Obtener acceso al correo electrónico como delegado mediante EWS en Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: a8123604-c7c0-405d-a0ed-7a9b4a431bfd
description: Obtenga información sobre cómo obtener acceso al correo electrónico como delegado mediante la API administrada ews o EWS en Exchange.
ms.openlocfilehash: aa921bc36004b3a26caa514390e52249021b304f
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521217"
---
# <a name="access-email-as-a-delegate-by-using-ews-in-exchange"></a>Obtener acceso al correo electrónico como delegado mediante EWS en Exchange

Obtenga información sobre cómo obtener acceso al correo electrónico como delegado mediante la API administrada ews o EWS en Exchange.
  
Puede usar la API administrada ews o EWS para proporcionar a un usuario acceso delegado a la carpeta Bandeja de entrada del propietario de un buzón. A continuación, el delegado puede crear solicitudes de reunión en nombre del propietario del buzón, buscar correo electrónico y recuperar, actualizar y eliminar correo electrónico de la carpeta Bandeja de entrada del propietario del buzón, según sus permisos.
  
Como delegado, usa los mismos métodos y operaciones para tener acceso a la carpeta Bandeja de entrada del propietario de un buzón que se usa para obtener acceso a una carpeta bandeja de entrada sin acceso delegado. La diferencia principal es que [](delegate-access-and-ews-in-exchange.md#bk_explicit) debe usar el acceso explícito para buscar o crear un elemento [](delegate-access-and-ews-in-exchange.md#bk_implicit) de correo electrónico y, después de identificar el identificador del elemento, puede usar el acceso implícito para obtener, actualizar o eliminar el elemento. 
  
**Tabla 1. Métodos de API administrada EWS y operaciones EWS para obtener acceso al correo electrónico como delegado**

|**Si quiere...**|**Use este método de LA API administrada de EWS...**|**Use esta operación EWS...**|
|:-----|:-----|:-----|
|Crear y enviar un correo electrónico como delegado  <br/> |[EmailMessage.Save donde](https://msdn.microsoft.com/library/dd635209%28v=exchg.80%29.aspx) el [parámetro FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) proporciona [acceso explícito](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) a la carpeta Borradores del propietario del buzón  <br/> [EmailMessage.SendAndSaveCopy](https://msdn.microsoft.com/library/dd634248%28v=exchg.80%29.aspx) donde el parámetro [FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) proporciona acceso [explícito](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) a la carpeta Elementos enviados del propietario del buzón  <br/> |[CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) donde el [elemento Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) especifica el [EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) del propietario del buzón  <br/> [SendItem](https://msdn.microsoft.com/library/a966da19-b05a-4504-ac98-91acc1667b9a%28Office.15%29.aspx) donde el [elemento Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) especifica el [EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) del propietario del buzón  <br/> |
|Crear varios mensajes de correo electrónico como delegado  <br/> |[ExchangeService.CreateItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) donde el parámetro **FolderId** proporciona [acceso explícito](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) a la carpeta Bandeja de entrada del propietario del buzón  <br/> |[CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) donde el [elemento Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) especifica el [EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) del propietario del buzón  <br/> |
|Buscar o buscar un correo electrónico como delegado  <br/> |[ExchangeService.FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) donde el parámetro **FolderId** proporciona [acceso explícito](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) a la carpeta Bandeja de entrada del propietario del buzón  <br/> |[FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) donde el [elemento Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) especifica el [EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) del propietario del buzón  <br/> |
|Obtener un correo electrónico como delegado  <br/> |[EmailMessage.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) <br/> |[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |
|Actualizar un correo electrónico como delegado  <br/> |[EmailMessage.Bind seguido](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) de [EmailMessage.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx) <br/> |[GetItem seguido](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) de [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |
|Eliminar un correo electrónico como delegado  <br/> |[EmailMessage.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) seguido de [EmailMessage.Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.delete%28v=exchg.80%29.aspx) <br/> |[GetItem seguido](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) de [DeleteItem](../web-service-reference/deleteitem-operation.md) <br/> |
   
Tenga en cuenta lo siguiente al trabajar con correos electrónicos como delegado:
  
- Si un delegado solo necesita trabajar con las solicitudes de reunión y las respuestas, el delegado no necesita acceso a la carpeta Bandeja de entrada. Para obtener más información, vea [tareas de requisitos previos para obtener acceso a calendarios como delegado.](how-to-access-a-calendar-as-a-delegate-by-using-ews-in-exchange.md#bk_prereq)
    
- Cuando un destinatario recibe un mensaje que se envió en nombre del propietario de un buzón de correo, el remitente aparece como *"Delegado*  en nombre del propietario  *del*  buzón". 
    
> [!NOTE]
> En los ejemplos de código de este artículo, primary@contoso.com es el propietario del buzón. 
  
## <a name="prerequisite-tasks"></a>Tareas de requisitos previos
<a name="bk_prereq"> </a>

Para que un usuario pueda tener acceso a la carpeta Bandeja de entrada del propietario del buzón como delegado, el usuario debe agregarse como delegado con permisos [a](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md) la carpeta Bandeja de entrada del propietario del buzón. 
  
## <a name="create-and-send-an-email-as-a-delegate-by-using-the-ews-managed-api"></a>Crear y enviar un correo electrónico como delegado mediante la API administrada de EWS
<a name="bk_createewsma"> </a>

La API administrada ews permite usar el objeto de servicio para que el usuario delegado cree y envíe correo electrónico en nombre del propietario del buzón. En este ejemplo se muestra cómo usar el método [Save](https://msdn.microsoft.com/library/dd635209%28v=exchg.80%29.aspx) para guardar el mensaje en la carpeta Borradores del propietario del buzón y, a continuación, el método [SendAndSaveCopy](https://msdn.microsoft.com/library/dd634248%28v=exchg.80%29.aspx) para enviar el correo y guardar el mensaje en la carpeta Elementos enviados del propietario del buzón. 
  
En este ejemplo se supone que **el** servicio es un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido para el delegado y que al delegado se le han concedido los permisos adecuados para la carpeta Bandeja de entrada, Borradores y Elementos enviados del propietario del [buzón.](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md)
  
```cs
public static void DelegateAccessCreateEmail(ExchangeService service)
{
    // Create an email message and provide it with connection 
    // configuration information by using an ExchangeService 
    // object named service.
    EmailMessage message = new EmailMessage(service);
    // Set properties on the email message.
    message.Subject = "Company Soccer Team";
    message.Body = "Are you interested in joining?";
    message.ToRecipients.Add("sadie@contoso.com");
    // Save the email to the mailbox owner's Drafts folder.
    // This method call results in a CreateItem call to EWS.
    // The FolderId parameter contains the context for the 
    // mailbox owner's Inbox folder. Any additional actions 
    // taken on this message will be performed in the mailbox 
    // owner's mailbox. 
    message.Save(new FolderId(WellKnownFolderName.Drafts, new Mailbox("primary@contoso.com")));
    // Send the email and save the message in the mailbox owner's 
    // Sent Items folder.
    // This method call results in a SendItem call to EWS.
    message.SendAndSaveCopy(new FolderId(WellKnownFolderName.SentItems, new Mailbox("primary@contoso.com")));
    Console.WriteLine("An email with the subject '" + message.Subject + "' has been sent to '" 
    + message.ToRecipients[0] + "' and saved in the Sent Items folder of the mailbox owner.");
}
```

## <a name="create-and-send-an-email-as-a-delegate-by-using-ews"></a>Crear y enviar un correo electrónico como delegado mediante EWS
<a name="bk_createews"> </a>

EWS permite usar el objeto de servicio para que el usuario delegado cree y envíe correo electrónico en nombre del propietario del buzón. En este ejemplo se muestra cómo usar la operación [CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) para crear un correo electrónico y la operación [SendItem](https://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) para enviar la hora y guardarla en la carpeta Elementos enviados del propietario del buzón. 
  
También es la primera solicitud XML que envía la API administrada ews cuando se usa el **método Save** para crear y enviar un [correo electrónico](#bk_createewsma).
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version=" Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:CreateItem MessageDisposition="SaveOnly">
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="drafts">
          <t:Mailbox>
            <t:EmailAddress>primary@contoso.com</t:EmailAddress>
          </t:Mailbox>
        </t:DistinguishedFolderId>
      </m:SavedItemFolderId>
      <m:Items>
        <t:Message>
          <t:Subject>Company Soccer Team</t:Subject>
          <t:Body BodyType="HTML">Are you interested in joining?</t:Body>
          <t:ToRecipients>
            <t:Mailbox>
              <t:EmailAddress>sadie@contoso.com</t:EmailAddress>
            </t:Mailbox>
          </t:ToRecipients>
        </t:Message>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

El servidor responde a la solicitud **CreateItem** con un mensaje [CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) que incluye un valor de elemento [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, que indica que el correo electrónico se creó y guardó correctamente. La respuesta también contiene el identificador de elemento del correo electrónico recién creado.
  
El **valor ItemId** se ha acortado para mejorar la legibilidad. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="893"
                         MinorBuildNumber="17"
                         Version="V2_10"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body>
    <m:CreateItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:CreateItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Message>
              <t:ItemId Id="iNRaAAA="
                        ChangeKey="CQAAABYAAADOilbYa8KaT7ZgMoTz2P+hAAABiQPU" />
            </t:Message>
          </m:Items>
        </m:CreateItemResponseMessage>
      </m:ResponseMessages>
    </m:CreateItemResponse>
  </s:Body>
</s:Envelope>
```

A continuación, use la **operación SendItem** para enviar el mensaje en nombre del propietario del buzón y guardarlo en la carpeta Elementos enviados del propietario del buzón. 
  
El **valor ItemId** se ha acortado para mejorar la legibilidad. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version=" Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:SendItem SaveItemToFolder="true">
      <m:ItemIds>
        <t:ItemId Id="iNRaAAA="
                  ChangeKey="CQAAABYAAADOilbYa8KaT7ZgMoTz2P+hAAABiQPU" />
      </m:ItemIds>
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="sentitems">
          <t:Mailbox>
            <t:EmailAddress>primary@contoso.com</t:EmailAddress>
          </t:Mailbox>
        </t:DistinguishedFolderId>
      </m:SavedItemFolderId>
    </m:SendItem>
  </soap:Body>
</soap:Envelope>
```

El servidor responde a la solicitud **SendItem** con un mensaje [SendItemResponse](https://msdn.microsoft.com/library/26ac41c7-57d9-473e-ab7a-bae93e1d2aba%28Office.15%29.aspx) que incluye un valor de elemento [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, que indica que el correo electrónico se envió y guardó correctamente en la carpeta Elementos enviados del propietario del buzón.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="893"
                         MinorBuildNumber="17"
                         Version="V2_10"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body>
    <m:SendItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:SendItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:SendItemResponseMessage>
      </m:ResponseMessages>
    </m:SendItemResponse>
  </s:Body>
</s:Envelope>
```

## <a name="search-for-an-email-as-a-delegate-by-using-the-ews-managed-api"></a>Buscar un correo electrónico como delegado mediante la API administrada de EWS
<a name="bk_searchewsma"> </a>

Para buscar un correo electrónico, debe usar uno de los [métodos ExchangeService.FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) que incluye un parámetro [FolderId,](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) de modo que pueda especificar la carpeta Bandeja de entrada del propietario del buzón. 
  
```cs
static void DelegateAccessSearchEmailWithFilter(ExchangeService service)
{
    // Limit the result set to 10 items.
    ItemView view = new ItemView(10);
    // Define the search filter.
    SearchFilter.ContainsSubstring filter = new SearchFilter.ContainsSubstring(ItemSchema.Subject, 
        "soccer", ContainmentMode.Substring, ComparisonMode.IgnoreCase);
    view.PropertySet = new PropertySet(ItemSchema.Subject,
                                       ItemSchema.DateTimeReceived,
                                       EmailMessageSchema.IsRead);
    // Item searches do not support deep traversal.
    view.Traversal = ItemTraversal.Shallow;
    // Sorting.
    view.OrderBy.Add(ItemSchema.DateTimeReceived, SortDirection.Descending);
    try
    {
        // Call FindItems to find matching Inbox items. 
        // The parameters of FindItems must denote the mailbox owner,
        // mailbox, and Inbox folder.
        // This call results in a FindItem call to EWS.
        FindItemsResults<Item> results = service.FindItems(new 
            FolderId(WellKnownFolderName.Inbox, "primary@contoso.com"), 
            filter, view);
        foreach (Item item in results.Items)
        {
            Console.WriteLine("Subject: {0}", item.Subject);
            Console.WriteLine("Id: {0}", item.Id.ToString());
            if (item is EmailMessage)
            {
                EmailMessage message = item as EmailMessage;
                Console.WriteLine("Read: {0}", message.IsRead.ToString());
            }
        }
    }
    catch (Exception ex)
    {
        Console.WriteLine("Exception while enumerating results: {0}", ex.Message);
    }
}
```

Después de que la llamada **FindItems** devuelva una respuesta con un identificador, [](delegate-access-and-ews-in-exchange.md#bk_implicit) puede obtener, actualizar o eliminar ese correo electrónico mediante el identificador y el acceso implícito, y no es necesario especificar la dirección SMTP del propietario del buzón. 
  
## <a name="search-for-an-email-as-a-delegate-by-using-ews"></a>Buscar un correo electrónico como delegado mediante EWS
<a name="bk_searchews"> </a>

EWS permite usar el objeto de servicio para que el usuario delegado busque correos electrónicos que cumplan un conjunto de criterios de búsqueda. En este ejemplo se muestra cómo usar la operación [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) para buscar mensajes en la carpeta Bandeja de entrada del propietario que contengan la palabra "fútbol" en el asunto. 
  
Esta es también la solicitud XML que la API administrada ews envía al [buscar un correo electrónico](#bk_searchewsma).
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version=" Exchange2007_SP1" />
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
          <t:Constant Value="soccer" />
        </t:Contains>
      </m:Restriction>
      <m:SortOrder>
        <t:FieldOrder Order="Descending">
          <t:FieldURI FieldURI="item:DateTimeReceived" />
        </t:FieldOrder>
      </m:SortOrder>
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox">
          <t:Mailbox>
            <t:EmailAddress>primary@contoso.com</t:EmailAddress>
          </t:Mailbox>
        </t:DistinguishedFolderId>
      </m:ParentFolderIds>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

El servidor responde a la solicitud **FindItem** con un mensaje [FindItemResponse](https://msdn.microsoft.com/library/c8b316df-d4ab-49b8-96d4-8e9a016730ef%28Office.15%29.aspx) que incluye un valor de elemento [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, que indica que la búsqueda se completó correctamente. La respuesta contiene un [elemento Message](https://msdn.microsoft.com/library/2400b33c-43b2-4fc2-b6fb-275a99e0e810%28Office.15%29.aspx) para cualquier correo electrónico que cumpla los criterios de búsqueda. En este caso, solo se encuentra un correo electrónico. 
  
El valor del [elemento ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) se ha acortado para mejorar la legibilidad. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="893"
                         MinorBuildNumber="17"
                         Version="V2_10"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body>
    <m:FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="1"
                        TotalItemsInView="1"
                        IncludesLastItemInRange="true">
            <t:Items>
              <t:Message>
                <t:ItemId Id="iNwoAAA="
                          ChangeKey="CQAAABYAAADOilbYa8KaT7ZgMoTz2P+hAAABiQuu" />
                <t:Subject>Soccer team</t:Subject>
                <t:DateTimeReceived>2014-03-10T06:16:55Z</t:DateTimeReceived>
                <t:IsRead>false</t:IsRead>
              </t:Message>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>
```

Ahora que tiene **el ItemId** para el correo electrónico que cumple sus criterios, puede obtener, actualizar o eliminar ese correo electrónico mediante **el ItemId** y el acceso implícito, y no es necesario especificar la dirección SMTP del propietario del buzón. [](delegate-access-and-ews-in-exchange.md#bk_implicit) 
  
## <a name="get-update-or-delete-email-items-as-a-delegate-by-using-the-ews-managed-api"></a>Obtener, actualizar o eliminar elementos de correo electrónico como delegado mediante la API administrada de EWS
<a name="bk_geteswma"> </a>

Puede usar la API administrada de EWS para obtener, actualizar o eliminar un correo electrónico del mismo modo que realiza estas acciones cuando no usa el acceso delegado. La única diferencia es que el **objeto ExchangeService** es para el usuario delegado. El identificador de elemento incluido en la llamada al método **Bind** identifica de forma exclusiva el elemento en el almacén de buzones, en la carpeta Bandeja de entrada del propietario del buzón. 
  
**Tabla 2. Métodos de API administrada ews que trabajan con el correo electrónico como delegado**

|**Tarea**|**Método de la API administrada de EWS**|**Ejemplo de código**|
|:-----|:-----|:-----|
|Obtener un correo electrónico  <br/> |[Enlazar](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) <br/> |[Obtener un elemento mediante la API administrada de EWS](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getewsma) <br/> |
|Actualizar un correo electrónico  <br/> |[Enlazar](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) seguido de [Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx) <br/> |[Actualizar un elemento mediante la API administrada de EWS](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_updateewsma) <br/> |
|Eliminar un correo electrónico  <br/> |[Enlazar](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) seguido de [Eliminar](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.delete%28v=exchg.80%29.aspx) <br/> |[Eliminar un elemento mediante la API administrada de EWS](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteewsma) <br/> |
   
## <a name="get-update-or-delete-email-items-as-a-delegate-by-using-ews"></a>Obtener, actualizar o eliminar elementos de correo electrónico como delegado mediante EWS
<a name="bk_getews"> </a>

Puede usar la API administrada de EWS para obtener, actualizar o eliminar un correo electrónico del mismo modo que realiza estas acciones cuando no usa el acceso delegado. La única diferencia es que el objeto de servicio es para el usuario delegado. El identificador de elemento incluido en la **solicitud GetItem** identifica de forma única el elemento en el almacén de buzones, en la carpeta Bandeja de entrada del propietario del buzón. 
  
**Tabla 3. Operaciones ews para trabajar con correo electrónico como delegado**

|**Tarea**|**Operación de EWS**|**Ejemplo de código**|
|:-----|:-----|:-----|
|Obtener un correo electrónico  <br/> |[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |[Obtener un elemento mediante EWS](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getews) <br/> |
|Actualizar un correo electrónico  <br/> |[GetItem seguido](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) de [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |[Actualizar un elemento mediante EWS](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_updateews) <br/> |
|Eliminar un correo electrónico  <br/> |[GetItem seguido](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) de [DeleteItem](../web-service-reference/deleteitem-operation.md) <br/> |[Eliminar un elemento mediante EWS](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteews) <br/> |
   
## <a name="see-also"></a>Ver también

- [Acceso delegado y EWS en Exchange](delegate-access-and-ews-in-exchange.md)    
- [Agregar y quitar delegados mediante EWS en Exchange](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md)    
- [Establecer permisos de carpeta para otro usuario mediante EWS en Exchange](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md)    
- [Calendarios y EWS en Exchange](calendars-and-ews-in-exchange.md)
    

