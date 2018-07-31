---
title: Contactos de proceso por lotes mediante EWS en Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 455f475b-cb19-4e7a-8ff3-92f7028fceb0
description: Obtenga información sobre cómo crear, obtener, actualizar y eliminar lotes de contactos en una sola llamada mediante la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: ce1a61615767f3b03354bc79b036582613f15e7e
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/28/2018
ms.locfileid: "21354032"
---
# <a name="process-contacts-in-batches-by-using-ews-in-exchange"></a>Contactos de proceso por lotes mediante EWS en Exchange

Obtenga información sobre cómo crear, obtener, actualizar y eliminar lotes de contactos en una sola llamada mediante la API administrada de EWS o EWS en Exchange.
  
Puede usar la API administrada de EWS o realiza EWS para trabajar con lotes de contactos para reducir el número de llamadas de un cliente a un servidor de Exchange. Cuando se usa la API administrada de EWS para crear, obtener, actualizar y eliminar los contactos por lotes, use métodos del objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) , mientras que cuando se trabaja con contactos único, use los métodos del objeto de [contacto](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx) . Si usa EWS, use las mismas operaciones para trabajar con un solo contacto y lotes de contactos. 
  
**La tabla 1. Métodos de la API administrada de EWS y las operaciones de EWS para trabajar con lotes de contactos**

|**Con el fin...**|**Use este método de la API administrada de EWS**|**Use esta operación de EWS**|
|:-----|:-----|:-----|
|Crear contactos por lotes  <br/> |[ExchangeService.CreateItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) <br/> |[CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) <br/> |
|Obtener contactos por lotes  <br/> |[ExchangeService.BindToItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.bindtoitems%28v=exchg.80%29.aspx) o [ExchangeService.LoadPropertiesForItems](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.loadpropertiesforitems%28v=exchg.80%29.aspx) <br/> |[GetItem](http://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) <br/> |
|Contactos de actualización por lotes  <br/> |[ExchangeService.UpdateItems](http://msdn.microsoft.com/en-us/library/dd634705%28v=exchg.80%29.aspx) <br/> |[UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |
|Eliminar contactos por lotes  <br/> |[ExchangeService.DeleteItems](http://msdn.microsoft.com/en-us/library/dd635460%28v=exchg.80%29.aspx) <br/> |[DeleteItem](../web-service-reference/deleteitem-operation.md) <br/> |
   
En este artículo, aprenderá cómo completar tareas básicas de lotes de contactos mediante el uso de la API administrada de EWS o EWS.
  
## <a name="create-contacts-in-batches-by-using-the-ews-managed-api"></a>Crear contactos en lotes mediante el uso de la API administrada de EWS
<a name="bk_EWSMA"> </a>

Puede crear contactos en lotes mediante el método de la API administrada de EWS [CreateItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) , tal como se muestra en el siguiente ejemplo. En este ejemplo se crean tres [póngase en contacto con](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx) objetos localmente, agrega cada contacto a una colección, a continuación, se llama al método **CreateItems** en la colección de contactos. 
  
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

## <a name="create-contacts-in-batches-by-using-ews"></a>Crear contactos en lotes mediante el uso de EWS
<a name="bk_EWSMA"> </a>

Puede crear contactos en lotes mediante la operación [CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) EWS, tal como se muestra en el siguiente ejemplo de código. También es la solicitud XML que la API administrada de EWS envía al usar la API administrada de EWS para [crear contactos en lotes](#bk_EWSMA).
  
```XML
<?xml version="1.0" encoding="utf-8"?>
  <soap:Envelope 
xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

El servidor responde a la solicitud **CreateItem** con un mensaje de [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) que incluye un valor [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError** para cada uno de los nuevos contactos, lo que indica que cada contacto se ha creado y guardado correctamente. 
  
## <a name="get-contacts-in-batches-by-using-the-ews-managed-api"></a>Obtener contactos en lotes mediante el uso de la API administrada de EWS
<a name="bk_EWSMAGet"> </a>

Para obtener los contactos en lotes mediante el método de la API administrada de EWS [BindToItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.bindtoitems%28v=exchg.80%29.aspx) , tal como se muestra en el siguiente ejemplo. En este ejemplo se da por supuesto que **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que se ha autenticado el usuario a un servidor de Exchange. 
  
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

## <a name="get-contacts-in-batches-by-using-ews"></a>Obtener contactos en lotes mediante el uso de EWS
<a name="bk_EWSMAGet"> </a>

Puede obtener los contactos en lotes mediante la operación de EWS [GetItem](http://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) y el código en el siguiente ejemplo. También es la solicitud XML que la API administrada de EWS envía al usar la API administrada de EWS para [obtener los contactos por lotes](#bk_EWSMAGet). El atributo **ItemId** se ha acortado para mejorar la legibilidad. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
  <soap:Envelope 
xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

El servidor responde a la solicitud de **GetItem** con un mensaje de [GetItemResponse](http://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx) que incluye el identificador y el nombre para mostrar para cada uno de los contactos solicitados. 
  
## <a name="update-contacts-in-batches-by-using-the-ews-managed-api"></a>Contactos de actualización por lotes mediante el uso de la API administrada de EWS
<a name="bk_EWSMAUpdate"> </a>

Puede actualizar los contactos en lotes mediante el método de la API administrada de EWS [UpdateItems](http://msdn.microsoft.com/en-us/library/dd634705%28v=exchg.80%29.aspx) , tal como se muestra en el siguiente ejemplo. En el ejemplo anterior se crea el contacto, pero no se especifica que trabajan para. Puede usar el código en este ejemplo, para actualizar todos los contactos a la vez para que incluya su nombre de la compañía. 
  
En este ejemplo se da por supuesto que **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que se ha autenticado el usuario a un servidor de Exchange. 
  
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

## <a name="update-contacts-in-batches-by-using-ews"></a>Contactos de actualización por lotes mediante el uso de EWS
<a name="bk_EWSMAUpdate"> </a>

Puede actualizar los contactos en lotes mediante la operación de EWS [GetItem](http://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) , tal como se muestra en el siguiente ejemplo de código. También es la solicitud XML que la API administrada de EWS envía al usar la API administrada de EWS para [actualizar los contactos por lotes](#bk_EWSMAUpdate). El atributo **ItemId** se ha acortado para mejorar la legibilidad. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
  <soap:Envelope 
xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

El servidor responde a la solicitud de **UpdateItem** con un mensaje de [UpdateItemResponse](http://msdn.microsoft.com/library/023b79b4-c675-4669-9112-d85499ec4fc4%28Office.15%29.aspx) que incluye un valor [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, lo que indica que cada una de las actualizaciones se guardó correctamente en el servidor. Se informa de los conflictos en el elemento [ConflictResult](http://msdn.microsoft.com/library/08cdd547-4de7-4c7a-b60f-e618dc217d20%28Office.15%29.aspx) . 
  
## <a name="delete-contacts-in-batches-by-using-the-ews-managed-api"></a>Eliminar contactos por lotes mediante el uso de la API administrada de EWS
<a name="bk_EWSMADelete"> </a>

Puede eliminar los contactos en lotes mediante el método de la API administrada de EWS [DeleteItems](http://msdn.microsoft.com/en-us/library/dd635460%28v=exchg.80%29.aspx) , tal como se muestra en el siguiente ejemplo. En este ejemplo se da por supuesto que **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que se ha autenticado el usuario a un servidor de Exchange. 
  
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

## <a name="delete-contacts-in-batches-by-using-ews"></a>Eliminar contactos por lotes mediante el uso de EWS
<a name="bk_EWSMADelete"> </a>

Puede eliminar los contactos en lotes mediante la operación de EWS [DeleteItem](../web-service-reference/deleteitem-operation.md) , tal como se muestra en el siguiente ejemplo de código. También es la solicitud XML que la API administrada de EWS envía al usar la API administrada de EWS para [eliminar los contactos por lotes](#bk_EWSMADelete). El atributo **ItemId** se ha acortado para mejorar la legibilidad. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
  <soap:Envelope 
xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

El servidor responde a la solicitud de **DeleteItem** con un mensaje de [DeleteItemResponse](http://msdn.microsoft.com/library/86463d66-fe47-4a19-a81b-e24841e816ab%28Office.15%29.aspx) que incluye un valor [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError** para cada elemento que se ha quitado. Tenga en cuenta que la operación también devuelve success si no se pudo encontrar el identificador de elemento. 
  
## <a name="verifying-that-a-batch-process-completed-successfully"></a>Comprobar que un proceso por lotes se completó correctamente
<a name="bk_successful"> </a>

Cuando no se puede procesar uno o varios contactos en una solicitud por lotes como se ha solicitado, se devuelve un error para cada contacto que no se pudo, y el resto de los contactos en el lote se procesan según lo previsto. Pueden producirse errores en el procesamiento por lotes si el elemento se ha eliminado y por lo tanto, no puede recuperarse o actualizarse, o si el elemento movido a una carpeta diferente y por lo tanto, tiene un nuevo identificador de elemento y no se puede modificar con el identificador de elemento que se envía. La información de esta sección muestra cómo obtener detalles acerca de los errores del error en el procesamiento por lotes de contactos.
  
Para comprobar el éxito de un proceso por lotes mediante el uso de la API administrada de EWS, puede comprobar que la propiedad [OverallResult](http://msdn.microsoft.com/en-us/library/dd634515%28v=exchg.80%29.aspx) de la [ServiceResponseCollection](http://msdn.microsoft.com/en-us/library/dd633715%28v=exchg.80%29.aspx) es igual a [ServiceResult.Success](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresult%28v=exchg.80%29.aspx). Si es así, todos los contactos se procesan correctamente. Si el **OverallResult** no es igual a **ServiceResult.Success**, uno o varios de los contactos no se procesó correctamente. Cada uno de los objetos devueltos en la **ServiceResponseCollection** contiene las siguientes propiedades: 
  
- [ErrorCode](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse.errorcode%28v=exchg.80%29.aspx)
    
- [ErrorDetails](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse.errordetails%28v=exchg.80%29.aspx)
    
- [ErrorMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse.errormessage%28v=exchg.80%29.aspx)
    
- [ErrorProperties](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse.errorproperties%28v=exchg.80%29.aspx)
    
- [Resultado](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.serviceresponse.result%28v=exchg.80%29.aspx)
    
Estas propiedades contienen información acerca de por qué los contactos no se podrían procesar como se solicitó. Imprimen el **resultado**, **ErrorCode**, los ejemplos de este artículo y **ErrorMessage** para cada error al contacto. Puede utilizar estos resultados para investigar el problema. 
  
Para EWS, para comprobar el éxito de un proceso por lotes, consulte el atributo [ResponseClass](http://msdn.microsoft.com/library/bf57265a-d354-4cd7-bbfc-d93e19cbede6%28Office.15%29.aspx) para cada elemento que se está procesando. La siguiente es la estructura básica de la **ResponseMessageType**, el tipo base de qué respuesta todos los mensajes se derivan. 
  
```XML
<ResponseMessage ResponseClass="Success | Warning | Error">
            <MessageText/>
            <ResponseCode/>
            <DescriptiveLinkKey/>
            <MessageXml/>
</ResponseMessage>
```

El atributo **ResponseClass** se establece en **Error** o **éxito** si el contacto se procesó correctamente si el contacto no se procesó correctamente. Para los contactos, no se producirá una **Advertencia** durante el procesamiento por lotes. Si la **ResponseClass** es **correcto**, el elemento [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) que sigue también siempre se establece en **NoError**. Si la **ResponseClass** es **Error**, debe comprobar los valores de los elementos [MessageText](http://msdn.microsoft.com/library/59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1%28Office.15%29.aspx), **ResponseCode**y [MessageXml](http://msdn.microsoft.com/library/bcaf9e35-d351-48f3-baad-f90c633cba8a%28Office.15%29.aspx) para determinar la causa del problema. [DescriptiveLinkKey](http://msdn.microsoft.com/library/f7f36749-00f3-4915-b17c-e3caa0af6e67%28Office.15%29.aspx) se utiliza actualmente. 
  
## <a name="see-also"></a>Vea también


- [Las personas y los contactos de EWS en Exchange](people-and-contacts-in-ews-in-exchange.md)
    
- [Mensajes de correo electrónico de proceso por lotes mediante el uso de EWS en Exchange](how-to-process-email-messages-in-batches-by-using-ews-in-exchange.md)
    
- [Procesar por lotes los elementos del calendario en Exchange](how-to-process-calendar-items-in-batches-in-exchange.md)
    

