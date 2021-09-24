---
title: Procesar contactos en lotes mediante EWS en Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 455f475b-cb19-4e7a-8ff3-92f7028fceb0
description: Obtenga información sobre cómo crear, obtener, actualizar y eliminar lotes de contactos en una sola llamada mediante la API administrada ews o EWS en Exchange.
ms.openlocfilehash: e70618dc0a9ea3f2d534c79fff627393ced8f1cb
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522225"
---
# <a name="process-contacts-in-batches-by-using-ews-in-exchange"></a>Procesar contactos en lotes mediante EWS en Exchange

Obtenga información sobre cómo crear, obtener, actualizar y eliminar lotes de contactos en una sola llamada mediante la API administrada ews o EWS en Exchange.
  
Puede usar la API administrada ews o EWS para trabajar con lotes de contactos para reducir el número de llamadas que un cliente realiza a un Exchange servidor. Cuando se usa la API administrada ews para crear, obtener, actualizar y eliminar contactos en lotes, se usan métodos de objeto [ExchangeService,](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) mientras que cuando se trabaja con contactos únicos, se usan métodos de objeto [Contact.](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx) Si usa EWS, use las mismas operaciones para trabajar con un solo contacto y lotes de contactos. 
  
**Tabla 1. Métodos de API administrada ews y operaciones EWS para trabajar con lotes de contactos**

|**Para**|**Usar este método de API administrada ews**|**Usar esta operación EWS**|
|:-----|:-----|:-----|
|Crear contactos en lotes  <br/> |[ExchangeService.CreateItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) <br/> |[CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) <br/> |
|Obtener contactos en lotes  <br/> |[ExchangeService.BindToItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.bindtoitems%28v=exchg.80%29.aspx) o [ExchangeService.LoadPropertiesForItems](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.loadpropertiesforitems%28v=exchg.80%29.aspx) <br/> |[GetItem](https://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) <br/> |
|Actualizar contactos en lotes  <br/> |[ExchangeService.UpdateItems](https://msdn.microsoft.com/library/dd634705%28v=exchg.80%29.aspx) <br/> |[UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |
|Eliminar contactos en lotes  <br/> |[ExchangeService.DeleteItems](https://msdn.microsoft.com/library/dd635460%28v=exchg.80%29.aspx) <br/> |[DeleteItem](../web-service-reference/deleteitem-operation.md) <br/> |
   
En este artículo, aprenderá a completar tareas básicas para lotes de contactos mediante la API administrada ews o EWS.
  
## <a name="create-contacts-in-batches-by-using-the-ews-managed-api"></a>Crear contactos en lotes mediante la API administrada de EWS
<a name="bk_EWSMA"> </a>

Puede crear contactos en lotes mediante el método [CreateItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) de la API administrada de EWS, como se muestra en el ejemplo siguiente. En este ejemplo se crean tres [objetos Contact](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx) localmente, se agrega cada contacto a una colección y, a continuación, se llama al **método CreateItems** en la colección de contactos. 
  
```cs
public static Collection<ItemId> CreateContactsInBatch(ExchangeService service)
{
    // These are unsaved local instances of a Contact object.
    // Despite the required parameter of an ExchangeService object (service), no call
    // to an Exchange server is made when the objects are instantiated.
    // A call to the Exchange server is made when the service.CreateItems() method is called.
    Contact contact1 = new Contact(service);
    Contact contact2 = new Contact(service);
    Contact contact3 = new Contact(service);
    // Set the properties on the first contact.
    contact1.DisplayName = "Sadie Daniels";
    contact1.EmailAddresses[EmailAddressKey.EmailAddress1] = new EmailAddress("sadie@contoso.com");
    
    // Set the properties on the second contact.
    contact2.DisplayName = "Alfred Welker";
    contact2.EmailAddresses[EmailAddressKey.EmailAddress1] = new EmailAddress("alfred@contoso.com");
    // Set the properties on the third contact.
    contact3.DisplayName = "Hope Gross";
    contact3.EmailAddresses[EmailAddressKey.EmailAddress1] = new EmailAddress("hope@contoso.com");
    // Add the Contact objects to a collection.
    Collection<Contact> contactItems = new Collection<Contact>() { contact1, contact2, contact3 };
    // Create the batch of contacts on the server.
    // This method call results in an CreateItem call to EWS.
    ServiceResponseCollection<ServiceResponse> response = service.CreateItems(contactItems, WellKnownFolderName.Contacts, null, null);
    // Instantiate a collection of item IDs to populate from the values that are returned by the Exchange server.
    Collection<ItemId> itemIds = new Collection<ItemId>();
    // Collect the item IDs from the created contacts.
    foreach (Contact contact in contactItems)
    {
        try
        {
            itemIds.Add(contact.Id);
            Console.WriteLine("Contact '{0}' created successfully.", contact.DisplayName);
        }
        catch (Exception ex)
        {
            // Print out the exception and the last eight characters of the item ID.
            Console.WriteLine("Exception while creating contact {0}: {1}", contact.Id.ToString().Substring(144), ex.Message);
        }
    }
    // Determine whether the CreateItems method call completed successfully.
    if (response.OverallResult == ServiceResult.Success)
    {
            Console.WriteLine("All locally created contacts were successfully created in the Contacts folder.");
            Console.WriteLine("\r\n");
    }
   
    // If the method did not return success, print the result message for each contact.
    else
    {
        int counter = 1;
        foreach (ServiceResponse resp in response)
        {
            // Print out the result and the last eight characters of the item ID.
            Console.WriteLine("Result (contact {0}), id {1}: {2}", counter, itemIds[counter - 1].ToString().Substring(144), resp.Result);
            Console.WriteLine("Error Code: {0}", resp.ErrorCode);
            Console.WriteLine("ErrorMessage: {0}\r\n", resp.ErrorMessage);
            Console.WriteLine("\r\n");
            counter++;
        }
    }
    return itemIds;
}
```

## <a name="create-contacts-in-batches-by-using-ews"></a>Crear contactos en lotes mediante EWS
<a name="bk_EWSMA"> </a>

Puede crear contactos en lotes mediante la [operación EWS CreateItem,](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) como se muestra en el siguiente ejemplo de código. Esta es también la solicitud XML que envía la API administrada ews cuando se usa la API administrada ews para [crear contactos en lotes.](#bk_EWSMA)
  
```XML
<?xml version="1.0" encoding="utf-8"?>
  <soap:Envelope 
xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
    <soap:Header>
      <t:RequestServerVersion Version="Exchange2007_SP1" />
    </soap:Header>
    <soap:Body>
      <m:CreateItem>
        <m:SavedItemFolderId>
          <t:DistinguishedFolderId Id="contacts" />
        </m:SavedItemFolderId>
        <m:Items>
          <t:Contact>
            <t:DisplayName>Sadie Daniels</t:DisplayName>
            <t:EmailAddresses>
              <t:Entry Key="EmailAddress1">sadie@contoso.com</t:Entry>
            </t:EmailAddresses>
          </t:Contact>
          <t:Contact>
            <t:DisplayName>Alfred Welker</t:DisplayName>
            <t:EmailAddresses>
              <t:Entry Key="EmailAddress1">alfred@contoso.com</t:Entry>
            </t:EmailAddresses>
          </t:Contact>
          <t:Contact>
            <t:DisplayName>Hope Gross</t:DisplayName>
            <t:EmailAddresses>
              <t:Entry Key="EmailAddress1">hope@contoso.com</t:Entry>
            </t:EmailAddresses>
          </t:Contact>
        </m:Items>
      </m:CreateItem>
    </soap:Body>
  </soap:Envelope>
```

El servidor responde a la solicitud **CreateItem** con un mensaje [CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) que incluye un valor [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError** para cada uno de los nuevos contactos, lo que indica que cada contacto se creó y guardó correctamente. 
  
## <a name="get-contacts-in-batches-by-using-the-ews-managed-api"></a>Obtener contactos en lotes mediante la API administrada de EWS
<a name="bk_EWSMAGet"> </a>

Puede obtener contactos en lotes mediante el método [BindToItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.bindtoitems%28v=exchg.80%29.aspx) de la API administrada ews, como se muestra en el ejemplo siguiente. En este ejemplo se supone que **el servicio** es un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que el usuario se ha autenticado en un Exchange servidor. 
  
```cs
public static Collection<Contact> BatchGetContactItems(ExchangeService service, Collection<ItemId> itemIds)
        {
            // Create a property set that limits the properties returned by the Bind method to only those that are required.
            PropertySet propSet = new PropertySet(BasePropertySet.IdOnly, ContactSchema.DisplayName);
            // Get the items from the server.
            // This method call results in a GetItem call to EWS.
            ServiceResponseCollection<GetItemResponse> response = service.BindToItems(itemIds, propSet);
            // Instantiate a collection of Contact objects to populate from the values that are returned by the Exchange server.
            Collection<Contact> contactItems = new Collection<Contact>();
            foreach (GetItemResponse getItemResponse in response)
            {
                try
                {
                    Item item = getItemResponse.Item;
                    Contact contact = (Contact)item;
                    contactItems.Add(contact);
                    // Print out confirmation and the last eight characters of the item ID.
                    Console.WriteLine("Found item {0}.", contact.Id.ToString().Substring(144));
                }
                catch (Exception ex)
                {
                    Console.WriteLine("Exception while getting a contact: {0}", ex.Message);
                }
            }
            // Check for success of the BindToItems method call.
            if (response.OverallResult == ServiceResult.Success)
            {
                Console.WriteLine("All contacts retrieved successfully.");
                Console.WriteLine("\r\n");
            }
            return contactItems;
        }

```

## <a name="get-contacts-in-batches-by-using-ews"></a>Obtener contactos en lotes mediante EWS
<a name="bk_EWSMAGet"> </a>

Puede obtener contactos en lotes mediante la operación [EWS GetItem](https://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) y el código del ejemplo siguiente. Esta es también la solicitud XML que envía la API administrada ews cuando se usa la API administrada ews para obtener [contactos en lotes.](#bk_EWSMAGet) El **atributo ItemId** se ha acortado para mejorar la legibilidad. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
  <soap:Envelope 
xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
    <soap:Header>
      <t:RequestServerVersion Version="Exchange2007_SP1" />
    </soap:Header>
    <soap:Body>
      <m:GetItem>
        <m:ItemShape>
          <t:BaseShape>IdOnly</t:BaseShape>
          <t:AdditionalProperties>
            <t:FieldURI FieldURI="contacts:DisplayName" />
          </t:AdditionalProperties>
        </m:ItemShape>
        <m:ItemIds>
          <t:ItemId Id="ceJwVAAA=" ChangeKey="EQAAABYAAAD2WuN+TpqwSrNP9JCCMKC0AAFc51yS" />
          <t:ItemId Id="ceJwWAAA=" ChangeKey="EQAAABYAAAD2WuN+TpqwSrNP9JCCMKC0AAFc51yT" />
          <t:ItemId Id="ceJwXAAA=" ChangeKey="EQAAABYAAAD2WuN+TpqwSrNP9JCCMKC0AAFc51yU" />
        </m:ItemIds>
      </m:GetItem>
    </soap:Body>
  </soap:Envelope>
```

El servidor responde a la solicitud **GetItem** con un mensaje [GetItemResponse](https://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx) que incluye el identificador y el nombre para mostrar de cada uno de los contactos solicitados. 
  
## <a name="update-contacts-in-batches-by-using-the-ews-managed-api"></a>Actualizar contactos en lotes mediante la API administrada de EWS
<a name="bk_EWSMAUpdate"> </a>

Puede actualizar los contactos en lotes mediante el método [UpdateItems](https://msdn.microsoft.com/library/dd634705%28v=exchg.80%29.aspx) de la API administrada de EWS, como se muestra en el ejemplo siguiente. En el ejemplo anterior se crea el contacto, pero no se especifica para quién trabajan. Puede usar el código de este ejemplo para actualizar todos los contactos a la vez para incluir su nombre de empresa. 
  
En este ejemplo se supone que **el servicio** es un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que el usuario se ha autenticado en un Exchange servidor. 
  
```cs
public static Collection<Contact> BatchUpdateContactItems(ExchangeService service, Collection<Contact> contactItems)
        {
            // Update the company name of each contact locally.
            foreach (Contact contact in contactItems)
            {
                // Update the company name of the contact.
                contact.CompanyName = "Contoso";
                // Print out confirmation with the last eight characters of the item ID and the contact company name.
                Console.WriteLine("Updated local contact {0} with the company name '{1}'.", contact.Id.ToString().Substring(144), contact.CompanyName);
            }
            
            // Send the item updates to the server.
            // This method call results in an UpdateItem call to EWS.
            ServiceResponseCollection<UpdateItemResponse> response = service.UpdateItems(contactItems, WellKnownFolderName.Contacts, ConflictResolutionMode.AutoResolve, null, null);
            // Verify the success of the UpdateItems method call.
            if (response.OverallResult == ServiceResult.Success)
            {
                Console.WriteLine("All contacts updated successfully.\r\n");
            }
            // If the method did not return success, print the result message for each contact.
            else
            {
                Console.WriteLine("All contacts were not successfully saved on the server.\r\n");
                int counter = 1;
                foreach (ServiceResponse resp in response)
                {
                    Console.WriteLine("Result for (contact {0}): {1}", counter, resp.Result);
                    Console.WriteLine("Error Code: {0}", resp.ErrorCode);
                    Console.WriteLine("ErrorMessage: {0}\r\n", resp.ErrorMessage);
                    counter++;
                }
            }
            return contactItems;
        }    

```

## <a name="update-contacts-in-batches-by-using-ews"></a>Actualizar contactos en lotes mediante EWS
<a name="bk_EWSMAUpdate"> </a>

Puede actualizar los contactos en lotes mediante la operación [EWS GetItem,](https://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) como se muestra en el siguiente ejemplo de código. También es la solicitud XML que envía la API administrada ews cuando se usa la API administrada ews para [actualizar los contactos en lotes.](#bk_EWSMAUpdate) El **atributo ItemId** se ha acortado para mejorar la legibilidad. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
  <soap:Envelope 
xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
    <soap:Header>
      <t:RequestServerVersion Version="Exchange2007_SP1" />
    </soap:Header>
    <soap:Body>
      <m:UpdateItem ConflictResolution="AutoResolve">
        <m:SavedItemFolderId>
          <t:DistinguishedFolderId Id="contacts" />
        </m:SavedItemFolderId>
        <m:ItemChanges>
          <t:ItemChange>
            <t:ItemId Id="ceJwVAAA=" ChangeKey="EQAAABYAAAD2WuN+TpqwSrNP9JCCMKC0AAFc51yS" />
            <t:Updates>
              <t:SetItemField>
                <t:FieldURI FieldURI="contacts:CompanyName" />
                <t:Contact>
                  <t:CompanyName>Contoso</t:CompanyName>
                </t:Contact>
              </t:SetItemField>
            </t:Updates>
          </t:ItemChange>
          <t:ItemChange>
            <t:ItemId Id="ceJwWAAA=" ChangeKey="EQAAABYAAAD2WuN+TpqwSrNP9JCCMKC0AAFc51yT" />
            <t:Updates>
              <t:SetItemField>
                <t:FieldURI FieldURI="contacts:CompanyName" />
                <t:Contact>
                  <t:CompanyName>Contoso</t:CompanyName>
                </t:Contact>
              </t:SetItemField>
            </t:Updates>
          </t:ItemChange>
          <t:ItemChange>
            <t:ItemId Id="ceJwXAAA=" ChangeKey="EQAAABYAAAD2WuN+TpqwSrNP9JCCMKC0AAFc51yU" />
            <t:Updates>
              <t:SetItemField>
                <t:FieldURI FieldURI="contacts:CompanyName" />
                <t:Contact>
                  <t:CompanyName>Contoso</t:CompanyName>
                </t:Contact>
              </t:SetItemField>
            </t:Updates>
          </t:ItemChange>
        </m:ItemChanges>
      </m:UpdateItem>
    </soap:Body>
  </soap:Envelope>
```

El servidor responde a la solicitud **UpdateItem** con un mensaje [UpdateItemResponse](https://msdn.microsoft.com/library/023b79b4-c675-4669-9112-d85499ec4fc4%28Office.15%29.aspx) que incluye un valor [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, que indica que cada una de las actualizaciones se guardó correctamente en el servidor. Los conflictos se notifican en el [elemento ConflictResult.](https://msdn.microsoft.com/library/08cdd547-4de7-4c7a-b60f-e618dc217d20%28Office.15%29.aspx) 
  
## <a name="delete-contacts-in-batches-by-using-the-ews-managed-api"></a>Eliminar contactos en lotes mediante la API administrada de EWS
<a name="bk_EWSMADelete"> </a>

Puede eliminar contactos en lotes mediante el método [deleteItems](https://msdn.microsoft.com/library/dd635460%28v=exchg.80%29.aspx) EWS Managed API, como se muestra en el ejemplo siguiente. En este ejemplo se supone que **el servicio** es un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que el usuario se ha autenticado en un Exchange servidor. 
  
```cs
public static void BatchDeleteContactItems(ExchangeService service, Collection<ItemId> itemIds)
        {
            // Delete the batch of contact objects.
            // This method call results in an DeleteItem call to EWS.
            ServiceResponseCollection<ServiceResponse> response = service.DeleteItems(itemIds, DeleteMode.SoftDelete, null, AffectedTaskOccurrence.AllOccurrences);
            // Check for success of the DeleteItems method call.
            // DeleteItems returns success even if it does not find all the item IDs.
            if (response.OverallResult == ServiceResult.Success)
            {
                Console.WriteLine("Contacts deleted successfully.\r\n");
            }
            // If the method did not return success, print a message.
            else
            {
                Console.WriteLine("Not all contacts deleted successfully.\r\n");
            }
        }

```

## <a name="delete-contacts-in-batches-by-using-ews"></a>Eliminar contactos en lotes mediante EWS
<a name="bk_EWSMADelete"> </a>

Puede eliminar contactos en lotes mediante la [operación EWS DeleteItem,](../web-service-reference/deleteitem-operation.md) como se muestra en el siguiente ejemplo de código. Esta es también la solicitud XML que envía la API administrada ews cuando se usa la API administrada ews para [eliminar contactos en lotes.](#bk_EWSMADelete) El **atributo ItemId** se ha acortado para mejorar la legibilidad. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
  <soap:Envelope 
xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
    <soap:Header>
      <t:RequestServerVersion Version="Exchange2007_SP1" />
    </soap:Header>
    <soap:Body>
      <m:DeleteItem DeleteType="SoftDelete" AffectedTaskOccurrences="AllOccurrences">
        <m:ItemIds>
          <t:ItemId Id="ceJwYAAA=" ChangeKey="EQAAABYAAAD2WuN+TpqwSrNP9JCCMKC0AAFc51yY" />
          <t:ItemId Id="ceJwZAAA=" ChangeKey="EQAAABYAAAD2WuN+TpqwSrNP9JCCMKC0AAFc51yZ" />
          <t:ItemId Id="ceJwaAAA=" ChangeKey="EQAAABYAAAD2WuN+TpqwSrNP9JCCMKC0AAFc51ya" />
        </m:ItemIds>
      </m:DeleteItem>
    </soap:Body>
  </soap:Envelope>
```

El servidor responde a la solicitud **DeleteItem** con un mensaje [DeleteItemResponse](https://msdn.microsoft.com/library/86463d66-fe47-4a19-a81b-e24841e816ab%28Office.15%29.aspx) que incluye un valor [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError** para cada elemento que se quitó. Tenga en cuenta que la operación también devuelve un resultado correcto si no se pudo encontrar el identificador del elemento. 
  
## <a name="verifying-that-a-batch-process-completed-successfully"></a>Comprobar que un proceso por lotes se completó correctamente
<a name="bk_successful"> </a>

Cuando uno o varios contactos de una solicitud por lotes no se pueden procesar como se solicitó, se devuelve un error para cada contacto que produjo un error y el resto de los contactos del lote se procesan según lo esperado. Los errores en el procesamiento por lotes pueden producirse si el elemento se eliminó y, por lo tanto, no se puede recuperar ni actualizar, o si el elemento se movió a una carpeta diferente y, por lo tanto, tiene un nuevo identificador de elemento y no se puede modificar con el identificador de elemento enviado. La información de esta sección muestra cómo obtener detalles de error sobre errores en el procesamiento por lotes de contactos.
  
Para comprobar el éxito de un proceso por lotes mediante la API administrada ews, puede comprobar que la propiedad [OverallResult](https://msdn.microsoft.com/library/dd634515%28v=exchg.80%29.aspx) de [ServiceResponseCollection](https://msdn.microsoft.com/library/dd633715%28v=exchg.80%29.aspx) es igual a [ServiceResult.Success](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresult%28v=exchg.80%29.aspx). Si es así, todos los contactos se procesaron correctamente. Si **OverallResult** no es igual a **ServiceResult.Success**, uno o varios de los contactos no se procesaron correctamente. Cada uno de los objetos devueltos en **ServiceResponseCollection** contiene las siguientes propiedades: 
  
- [ErrorCode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errorcode%28v=exchg.80%29.aspx)
    
- [ErrorDetails](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errordetails%28v=exchg.80%29.aspx)
    
- [ErrorMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errormessage%28v=exchg.80%29.aspx)
    
- [ErrorProperties](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errorproperties%28v=exchg.80%29.aspx)
    
- [Resultado](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.serviceresponse.result%28v=exchg.80%29.aspx)
    
Estas propiedades contienen información sobre por qué los contactos no se pudieron procesar como se solicitó. En los ejemplos de este artículo se **imprimen Los resultados,** **ErrorCode** y **ErrorMessage** para cada contacto con errores. Puede usar estos resultados para investigar el problema. 
  
Para EWS, para comprobar el éxito de un proceso por lotes, compruebe el atributo [ResponseClass](https://msdn.microsoft.com/library/bf57265a-d354-4cd7-bbfc-d93e19cbede6%28Office.15%29.aspx) para cada elemento que se está procesando. A continuación se muestra la estructura básica de **ResponseMessageType**, el tipo base del que se derivan todos los mensajes de respuesta. 
  
```XML
<ResponseMessage ResponseClass="Success | Warning | Error">
            <MessageText/>
            <ResponseCode/>
            <DescriptiveLinkKey/>
            <MessageXml/>
</ResponseMessage>
```

El **atributo ResponseClass** se establece en **Success** si el contacto se procesó correctamente o **Error** si el contacto no se procesó correctamente. Para los contactos, no encontrará una advertencia **durante** el procesamiento por lotes. Si **ResponseClass** es **Success**, el [elemento ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) siguiente también siempre se establece en **NoError**. Si **ResponseClass** es **Error**, debe comprobar los valores de los elementos [MessageText](https://msdn.microsoft.com/library/59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1%28Office.15%29.aspx), **ResponseCode** y [MessageXml](https://msdn.microsoft.com/library/bcaf9e35-d351-48f3-baad-f90c633cba8a%28Office.15%29.aspx) para determinar qué causó el problema. [DescriptiveLinkKey](https://msdn.microsoft.com/library/f7f36749-00f3-4915-b17c-e3caa0af6e67%28Office.15%29.aspx) está actualmente sin usar. 
  
## <a name="see-also"></a>Ver también


- [Personas y contactos de EWS en Exchange](people-and-contacts-in-ews-in-exchange.md)
    
- [Procesar mensajes de correo electrónico en lotes mediante EWS en Exchange](how-to-process-email-messages-in-batches-by-using-ews-in-exchange.md)
    
- [Procesar elementos de calendario en lotes en Exchange](how-to-process-calendar-items-in-batches-in-exchange.md)
    

