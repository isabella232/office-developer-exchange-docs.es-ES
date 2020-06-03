---
title: Procesar contactos en lotes mediante EWS en Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 455f475b-cb19-4e7a-8ff3-92f7028fceb0
description: Obtenga información sobre cómo crear, obtener, actualizar y eliminar lotes de contactos en una sola llamada usando la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: 2e122f67693b4ba46120104d9a1f6d36b4d86f97
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527806"
---
# <a name="process-contacts-in-batches-by-using-ews-in-exchange"></a><span data-ttu-id="e60b6-103">Procesar contactos en lotes mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="e60b6-103">Process contacts in batches by using EWS in Exchange</span></span>

<span data-ttu-id="e60b6-104">Obtenga información sobre cómo crear, obtener, actualizar y eliminar lotes de contactos en una sola llamada usando la API administrada de EWS o EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="e60b6-104">Learn how to create, get, update, and delete batches of contacts in a single call by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="e60b6-105">Puede usar la API administrada de EWS o EWS para trabajar con lotes de contactos y reducir el número de llamadas que un cliente realiza a un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e60b6-105">You can use the EWS Managed API or EWS to work with batches of contacts to reduce the number of calls a client makes to an Exchange server.</span></span> <span data-ttu-id="e60b6-106">Cuando se usa la API administrada de EWS para crear, obtener, actualizar y eliminar contactos en lotes, se usan los métodos del objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) , mientras que cuando se trabaja con contactos individuales, se usan los métodos de objeto de [contacto](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="e60b6-106">When you use the EWS Managed API to create, get, update, and delete contacts in batches, you use [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object methods, whereas when you work with single contacts, you use [Contact](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx) object methods.</span></span> <span data-ttu-id="e60b6-107">Si usa EWS, use las mismas operaciones para trabajar con un solo contacto y con lotes de contactos.</span><span class="sxs-lookup"><span data-stu-id="e60b6-107">If you are using EWS, you use the same operations to work with both a single contact and batches of contacts.</span></span> 
  
<span data-ttu-id="e60b6-108">**Tabla 1. Métodos de API administrada de EWS y operaciones de EWS para trabajar con lotes de contactos**</span><span class="sxs-lookup"><span data-stu-id="e60b6-108">**Table 1. EWS Managed API methods and EWS operations for working with batches of contacts**</span></span>

|<span data-ttu-id="e60b6-109">**Para**</span><span class="sxs-lookup"><span data-stu-id="e60b6-109">**In order to…**</span></span>|<span data-ttu-id="e60b6-110">**Usar este método de API administrada de EWS**</span><span class="sxs-lookup"><span data-stu-id="e60b6-110">**Use this EWS Managed API method**</span></span>|<span data-ttu-id="e60b6-111">**Usar esta operación de EWS**</span><span class="sxs-lookup"><span data-stu-id="e60b6-111">**Use this EWS operation**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e60b6-112">Crear contactos en lotes</span><span class="sxs-lookup"><span data-stu-id="e60b6-112">Create contacts in batches</span></span>  <br/> |[<span data-ttu-id="e60b6-113">ExchangeService. CreateItems</span><span class="sxs-lookup"><span data-stu-id="e60b6-113">ExchangeService.CreateItems</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="e60b6-114">CreateItem</span><span class="sxs-lookup"><span data-stu-id="e60b6-114">CreateItem</span></span>](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="e60b6-115">Obtener contactos en lotes</span><span class="sxs-lookup"><span data-stu-id="e60b6-115">Get contacts in batches</span></span>  <br/> |<span data-ttu-id="e60b6-116">[ExchangeService. BindToItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.bindtoitems%28v=exchg.80%29.aspx) o [ExchangeService. LoadPropertiesForItems](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.loadpropertiesforitems%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e60b6-116">[ExchangeService.BindToItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.bindtoitems%28v=exchg.80%29.aspx) or [ExchangeService.LoadPropertiesForItems](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.loadpropertiesforitems%28v=exchg.80%29.aspx)</span></span> <br/> |[<span data-ttu-id="e60b6-117">GetItem</span><span class="sxs-lookup"><span data-stu-id="e60b6-117">GetItem</span></span>](https://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="e60b6-118">Actualizar contactos en lotes</span><span class="sxs-lookup"><span data-stu-id="e60b6-118">Update contacts in batches</span></span>  <br/> |[<span data-ttu-id="e60b6-119">ExchangeService. UpdateItems</span><span class="sxs-lookup"><span data-stu-id="e60b6-119">ExchangeService.UpdateItems</span></span>](https://msdn.microsoft.com/library/dd634705%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="e60b6-120">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="e60b6-120">UpdateItem</span></span>](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="e60b6-121">Eliminar contactos en lotes</span><span class="sxs-lookup"><span data-stu-id="e60b6-121">Delete contacts in batches</span></span>  <br/> |[<span data-ttu-id="e60b6-122">ExchangeService. DeleteItems</span><span class="sxs-lookup"><span data-stu-id="e60b6-122">ExchangeService.DeleteItems</span></span>](https://msdn.microsoft.com/library/dd635460%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="e60b6-123">DeleteItem</span><span class="sxs-lookup"><span data-stu-id="e60b6-123">DeleteItem</span></span>](../web-service-reference/deleteitem-operation.md) <br/> |
   
<span data-ttu-id="e60b6-124">En este artículo, aprenderá a completar tareas básicas para lotes de contactos mediante la API administrada de EWS o EWS.</span><span class="sxs-lookup"><span data-stu-id="e60b6-124">In this article, you'll learn how to complete basic tasks for batches of contacts by using the EWS Managed API or EWS.</span></span>
  
## <a name="create-contacts-in-batches-by-using-the-ews-managed-api"></a><span data-ttu-id="e60b6-125">Crear contactos en lotes mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="e60b6-125">Create contacts in batches by using the EWS Managed API</span></span>
<span data-ttu-id="e60b6-126"><a name="bk_EWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="e60b6-126"><a name="bk_EWSMA"> </a></span></span>

<span data-ttu-id="e60b6-127">Puede crear contactos en lotes con el método [CreateItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) de la API administrada de EWS, como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="e60b6-127">You can create contacts in batches by using the EWS Managed API [CreateItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) method, as shown in the following example.</span></span> <span data-ttu-id="e60b6-128">En este ejemplo se crean tres objetos [Contact](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx) localmente, se agrega cada contacto a una colección y, a continuación, se llama al método **CreateItems** en la colección de contactos.</span><span class="sxs-lookup"><span data-stu-id="e60b6-128">This example creates three [Contact](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx) objects locally, adds each contact to a collection, then calls the **CreateItems** method on the collection of contacts.</span></span> 
  
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

## <a name="create-contacts-in-batches-by-using-ews"></a><span data-ttu-id="e60b6-129">Crear contactos en lotes mediante EWS</span><span class="sxs-lookup"><span data-stu-id="e60b6-129">Create contacts in batches by using EWS</span></span>
<span data-ttu-id="e60b6-130"><a name="bk_EWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="e60b6-130"><a name="bk_EWSMA"> </a></span></span>

<span data-ttu-id="e60b6-131">Puede crear contactos en lotes mediante la operación de EWS de [CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) , como se muestra en el siguiente ejemplo de código.</span><span class="sxs-lookup"><span data-stu-id="e60b6-131">You can create contacts in batches by using the [CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) EWS operation, as shown in the following code example.</span></span> <span data-ttu-id="e60b6-132">También es la solicitud XML que la API administrada de EWS envía cuando usa la API administrada de EWS para [crear contactos en lotes](#bk_EWSMA).</span><span class="sxs-lookup"><span data-stu-id="e60b6-132">This is also the XML request that the EWS Managed API sends when you use the EWS Managed API to [create contacts in batches](#bk_EWSMA).</span></span>
  
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

<span data-ttu-id="e60b6-133">El servidor responde a la solicitud **CreateItem** con un mensaje [CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) que incluye un valor [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError** para cada uno de los nuevos contactos, lo que indica que cada contacto se creó y guardó correctamente.</span><span class="sxs-lookup"><span data-stu-id="e60b6-133">The server responds to the **CreateItem** request with a [CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError** for each of the new contacts, which indicates that each contact was created and saved successfully.</span></span> 
  
## <a name="get-contacts-in-batches-by-using-the-ews-managed-api"></a><span data-ttu-id="e60b6-134">Obtener contactos en lotes mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="e60b6-134">Get contacts in batches by using the EWS Managed API</span></span>
<span data-ttu-id="e60b6-135"><a name="bk_EWSMAGet"> </a></span><span class="sxs-lookup"><span data-stu-id="e60b6-135"><a name="bk_EWSMAGet"> </a></span></span>

<span data-ttu-id="e60b6-136">Puede obtener contactos en lotes con el método [BindToItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.bindtoitems%28v=exchg.80%29.aspx) de la API administrada de EWS, como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="e60b6-136">You can get contacts in batches by using the EWS Managed API [BindToItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.bindtoitems%28v=exchg.80%29.aspx) method, as shown in the following example.</span></span> <span data-ttu-id="e60b6-137">En este ejemplo se supone que el **servicio** es un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que el usuario se ha autenticado en un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e60b6-137">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
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

## <a name="get-contacts-in-batches-by-using-ews"></a><span data-ttu-id="e60b6-138">Obtener contactos en lotes mediante EWS</span><span class="sxs-lookup"><span data-stu-id="e60b6-138">Get contacts in batches by using EWS</span></span>
<span data-ttu-id="e60b6-139"><a name="bk_EWSMAGet"> </a></span><span class="sxs-lookup"><span data-stu-id="e60b6-139"><a name="bk_EWSMAGet"> </a></span></span>

<span data-ttu-id="e60b6-140">Puede obtener contactos en lotes mediante la operación de EWS de [GetItem](https://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) y el código del siguiente ejemplo.</span><span class="sxs-lookup"><span data-stu-id="e60b6-140">You can get contacts in batches by using the [GetItem](https://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) EWS operation and the code in the following example.</span></span> <span data-ttu-id="e60b6-141">También es la solicitud XML que la API administrada de EWS envía cuando usa la API administrada de EWS para [obtener contactos en lotes](#bk_EWSMAGet).</span><span class="sxs-lookup"><span data-stu-id="e60b6-141">This is also the XML request that the EWS Managed API sends when you use the EWS Managed API to [get contacts in batches](#bk_EWSMAGet).</span></span> <span data-ttu-id="e60b6-142">El atributo **Itemid** se ha abreviado para facilitar su lectura.</span><span class="sxs-lookup"><span data-stu-id="e60b6-142">The **ItemId** attribute has been shortened for readability.</span></span> 
  
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

<span data-ttu-id="e60b6-143">El servidor responde a la solicitud **GetItem** con un mensaje [GetItemResponse](https://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx) que incluye el identificador y el nombre para mostrar de cada uno de los contactos solicitados.</span><span class="sxs-lookup"><span data-stu-id="e60b6-143">The server responds to the **GetItem** request with a [GetItemResponse](https://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx) message that includes the ID and the display name for each of the requested contacts.</span></span> 
  
## <a name="update-contacts-in-batches-by-using-the-ews-managed-api"></a><span data-ttu-id="e60b6-144">Actualizar los contactos en lotes mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="e60b6-144">Update contacts in batches by using the EWS Managed API</span></span>
<span data-ttu-id="e60b6-145"><a name="bk_EWSMAUpdate"> </a></span><span class="sxs-lookup"><span data-stu-id="e60b6-145"><a name="bk_EWSMAUpdate"> </a></span></span>

<span data-ttu-id="e60b6-146">Puede actualizar los contactos en lotes con el método [UpdateItems](https://msdn.microsoft.com/library/dd634705%28v=exchg.80%29.aspx) de la API administrada de EWS, como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="e60b6-146">You can update contacts in batches by using the EWS Managed API [UpdateItems](https://msdn.microsoft.com/library/dd634705%28v=exchg.80%29.aspx) method, as shown in the following example.</span></span> <span data-ttu-id="e60b6-147">En el ejemplo anterior, se crea el contacto pero no se especifican para quién trabajan.</span><span class="sxs-lookup"><span data-stu-id="e60b6-147">The previous example creates the contact but does not specify who they work for.</span></span> <span data-ttu-id="e60b6-148">Puede usar el código de este ejemplo para actualizar todos los contactos a la vez para incluir el nombre de su compañía.</span><span class="sxs-lookup"><span data-stu-id="e60b6-148">You can use the code in this example to update all your contacts at once to include their company name.</span></span> 
  
<span data-ttu-id="e60b6-149">En este ejemplo se supone que el **servicio** es un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que el usuario se ha autenticado en un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e60b6-149">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
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

## <a name="update-contacts-in-batches-by-using-ews"></a><span data-ttu-id="e60b6-150">Actualizar los contactos en lotes mediante EWS</span><span class="sxs-lookup"><span data-stu-id="e60b6-150">Update contacts in batches by using EWS</span></span>
<span data-ttu-id="e60b6-151"><a name="bk_EWSMAUpdate"> </a></span><span class="sxs-lookup"><span data-stu-id="e60b6-151"><a name="bk_EWSMAUpdate"> </a></span></span>

<span data-ttu-id="e60b6-152">Puede actualizar los contactos por lotes mediante la operación de EWS de [GetItem](https://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) , como se muestra en el siguiente ejemplo de código.</span><span class="sxs-lookup"><span data-stu-id="e60b6-152">You can update contacts in batches by using the [GetItem](https://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) EWS operation, as shown in following code example.</span></span> <span data-ttu-id="e60b6-153">También es la solicitud XML que la API administrada de EWS envía cuando usa la API administrada de EWS para [Actualizar contactos en lotes](#bk_EWSMAUpdate).</span><span class="sxs-lookup"><span data-stu-id="e60b6-153">This is also the XML request that the EWS Managed API sends when you use the EWS Managed API to [update contacts in batches](#bk_EWSMAUpdate).</span></span> <span data-ttu-id="e60b6-154">El atributo **Itemid** se ha abreviado para facilitar su lectura.</span><span class="sxs-lookup"><span data-stu-id="e60b6-154">The **ItemId** attribute has been shortened for readability.</span></span> 
  
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

<span data-ttu-id="e60b6-155">El servidor responde a la solicitud **UpdateItem** con un mensaje [UpdateItemResponse](https://msdn.microsoft.com/library/023b79b4-c675-4669-9112-d85499ec4fc4%28Office.15%29.aspx) que incluye un [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) valor de **NoError**, lo que indica que cada una de las actualizaciones se guardaron correctamente en el servidor.</span><span class="sxs-lookup"><span data-stu-id="e60b6-155">The server responds to the **UpdateItem** request with an [UpdateItemResponse](https://msdn.microsoft.com/library/023b79b4-c675-4669-9112-d85499ec4fc4%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError**, which indicates that each of the updates was saved successfully on the server.</span></span> <span data-ttu-id="e60b6-156">Los conflictos se notifican en el elemento [ConflictResult](https://msdn.microsoft.com/library/08cdd547-4de7-4c7a-b60f-e618dc217d20%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="e60b6-156">Any conflicts are reported in the [ConflictResult](https://msdn.microsoft.com/library/08cdd547-4de7-4c7a-b60f-e618dc217d20%28Office.15%29.aspx) element.</span></span> 
  
## <a name="delete-contacts-in-batches-by-using-the-ews-managed-api"></a><span data-ttu-id="e60b6-157">Eliminar contactos en lotes mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="e60b6-157">Delete contacts in batches by using the EWS Managed API</span></span>
<span data-ttu-id="e60b6-158"><a name="bk_EWSMADelete"> </a></span><span class="sxs-lookup"><span data-stu-id="e60b6-158"><a name="bk_EWSMADelete"> </a></span></span>

<span data-ttu-id="e60b6-159">Puede eliminar contactos en lotes con el método de la API administrada de EWS de [DeleteItems](https://msdn.microsoft.com/library/dd635460%28v=exchg.80%29.aspx) , como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="e60b6-159">You can delete contacts in batches by using the [DeleteItems](https://msdn.microsoft.com/library/dd635460%28v=exchg.80%29.aspx) EWS Managed API method, as shown in the following example.</span></span> <span data-ttu-id="e60b6-160">En este ejemplo se supone que el **servicio** es un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que el usuario se ha autenticado en un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e60b6-160">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
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

## <a name="delete-contacts-in-batches-by-using-ews"></a><span data-ttu-id="e60b6-161">Eliminar contactos en lotes mediante EWS</span><span class="sxs-lookup"><span data-stu-id="e60b6-161">Delete contacts in batches by using EWS</span></span>
<span data-ttu-id="e60b6-162"><a name="bk_EWSMADelete"> </a></span><span class="sxs-lookup"><span data-stu-id="e60b6-162"><a name="bk_EWSMADelete"> </a></span></span>

<span data-ttu-id="e60b6-163">Puede eliminar contactos en lotes mediante la operación de EWS [DeleteItem](../web-service-reference/deleteitem-operation.md) , tal como se muestra en el siguiente ejemplo de código.</span><span class="sxs-lookup"><span data-stu-id="e60b6-163">You can delete contacts in batches by using the [DeleteItem](../web-service-reference/deleteitem-operation.md) EWS operation, as shown in the following code example.</span></span> <span data-ttu-id="e60b6-164">También es la solicitud XML que la API administrada de EWS envía cuando usa la API administrada de EWS para [eliminar contactos en lotes](#bk_EWSMADelete).</span><span class="sxs-lookup"><span data-stu-id="e60b6-164">This is also the XML request that the EWS Managed API sends when you use the EWS Managed API to [delete contacts in batches](#bk_EWSMADelete).</span></span> <span data-ttu-id="e60b6-165">El atributo **Itemid** se ha abreviado para facilitar su lectura.</span><span class="sxs-lookup"><span data-stu-id="e60b6-165">The **ItemId** attribute has been shortened for readability.</span></span> 
  
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

<span data-ttu-id="e60b6-166">El servidor responde a la solicitud **DeleteItem** con un mensaje [DeleteItemResponse](https://msdn.microsoft.com/library/86463d66-fe47-4a19-a81b-e24841e816ab%28Office.15%29.aspx) que incluye un valor [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError** para cada elemento que se ha quitado.</span><span class="sxs-lookup"><span data-stu-id="e60b6-166">The server responds to the **DeleteItem** request with a [DeleteItemResponse](https://msdn.microsoft.com/library/86463d66-fe47-4a19-a81b-e24841e816ab%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError** for each item that was removed.</span></span> <span data-ttu-id="e60b6-167">Tenga en cuenta que la operación también devuelve SUCCESS si no se encuentra el identificador de elemento.</span><span class="sxs-lookup"><span data-stu-id="e60b6-167">Note that the operation also returns success if the item ID could not be found.</span></span> 
  
## <a name="verifying-that-a-batch-process-completed-successfully"></a><span data-ttu-id="e60b6-168">Comprobación de la finalización correcta de un proceso por lotes</span><span class="sxs-lookup"><span data-stu-id="e60b6-168">Verifying that a batch process completed successfully</span></span>
<span data-ttu-id="e60b6-169"><a name="bk_successful"> </a></span><span class="sxs-lookup"><span data-stu-id="e60b6-169"><a name="bk_successful"> </a></span></span>

<span data-ttu-id="e60b6-170">Cuando uno o más contactos de una solicitud por lotes no se pueden procesar como se solicitan, se devuelve un error para cada contacto en el que se ha producido un error y el resto de los contactos del lote se procesan como se esperaba.</span><span class="sxs-lookup"><span data-stu-id="e60b6-170">When one or more contacts in a batched request can't be processed as requested, an error is returned for each contact that failed, and the rest of the contacts in the batch are processed as expected.</span></span> <span data-ttu-id="e60b6-171">Los errores en el procesamiento por lotes pueden producirse si el elemento se eliminó y, por lo tanto, no se puede recuperar o actualizar, o si el elemento se movió a una carpeta diferente, y por lo tanto, tiene un identificador de elemento nuevo y no se puede modificar con el identificador de elemento enviado.</span><span class="sxs-lookup"><span data-stu-id="e60b6-171">Failures in batch processing can occur if the item was deleted, and therefore can't be retrieved, or updated, or if the item moved to a different folder, and therefore has a new item ID, and cannot be modified with the item ID sent.</span></span> <span data-ttu-id="e60b6-172">La información de esta sección muestra cómo obtener detalles de error sobre errores en el procesamiento por lotes de contactos.</span><span class="sxs-lookup"><span data-stu-id="e60b6-172">The information in this section shows how to get error details about failures in batch processing of contacts.</span></span>
  
<span data-ttu-id="e60b6-173">Para comprobar que el proceso por lotes se ha realizado correctamente mediante la API administrada de EWS, puede comprobar que la propiedad [OverallResult](https://msdn.microsoft.com/library/dd634515%28v=exchg.80%29.aspx) de [ServiceResponseCollection](https://msdn.microsoft.com/library/dd633715%28v=exchg.80%29.aspx) es igual a [ServiceResult. Success](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresult%28v=exchg.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="e60b6-173">To verify the success of a batch process by using the EWS Managed API, you can check that the [OverallResult](https://msdn.microsoft.com/library/dd634515%28v=exchg.80%29.aspx) property of the [ServiceResponseCollection](https://msdn.microsoft.com/library/dd633715%28v=exchg.80%29.aspx) is equal to [ServiceResult.Success](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresult%28v=exchg.80%29.aspx).</span></span> <span data-ttu-id="e60b6-174">Si es así, todos los contactos se procesaron correctamente.</span><span class="sxs-lookup"><span data-stu-id="e60b6-174">If so, all the contacts were processed successfully.</span></span> <span data-ttu-id="e60b6-175">Si **OverallResult** no es igual a **ServiceResult. Success**, uno o más de los contactos no se procesaron correctamente.</span><span class="sxs-lookup"><span data-stu-id="e60b6-175">If the **OverallResult** is not equal to **ServiceResult.Success**, one or more of the contacts were not processed successfully.</span></span> <span data-ttu-id="e60b6-176">Cada uno de los objetos devueltos en **ServiceResponseCollection** contiene las siguientes propiedades:</span><span class="sxs-lookup"><span data-stu-id="e60b6-176">Each of the objects returned in the **ServiceResponseCollection** contains the following properties:</span></span> 
  
- [<span data-ttu-id="e60b6-177">ErrorCode</span><span class="sxs-lookup"><span data-stu-id="e60b6-177">ErrorCode</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errorcode%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="e60b6-178">ErrorDetails</span><span class="sxs-lookup"><span data-stu-id="e60b6-178">ErrorDetails</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errordetails%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="e60b6-179">ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="e60b6-179">ErrorMessage</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errormessage%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="e60b6-180">ErrorProperties</span><span class="sxs-lookup"><span data-stu-id="e60b6-180">ErrorProperties</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errorproperties%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="e60b6-181">Resultado</span><span class="sxs-lookup"><span data-stu-id="e60b6-181">Result</span></span>](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.serviceresponse.result%28v=exchg.80%29.aspx)
    
<span data-ttu-id="e60b6-182">Estas propiedades contienen información sobre por qué los contactos no se pudieron procesar como se solicitó.</span><span class="sxs-lookup"><span data-stu-id="e60b6-182">These properties contain information about why the contacts could not be processed as requested.</span></span> <span data-ttu-id="e60b6-183">Los ejemplos de este artículo imprimen el **resultado**, **ErrorCode**y **errorMessage** de cada contacto con errores.</span><span class="sxs-lookup"><span data-stu-id="e60b6-183">The examples in this article print out the **Result**, **ErrorCode**, and **ErrorMessage** for each failed contact.</span></span> <span data-ttu-id="e60b6-184">Puede usar estos resultados para investigar el problema.</span><span class="sxs-lookup"><span data-stu-id="e60b6-184">You can use these results to investigate the issue.</span></span> 
  
<span data-ttu-id="e60b6-185">Para EWS, para comprobar que el proceso por lotes se ha realizado correctamente, compruebe el atributo [ResponseClass](https://msdn.microsoft.com/library/bf57265a-d354-4cd7-bbfc-d93e19cbede6%28Office.15%29.aspx) para cada elemento que se está procesando.</span><span class="sxs-lookup"><span data-stu-id="e60b6-185">For EWS, to verify the success of a batched process, check the [ResponseClass](https://msdn.microsoft.com/library/bf57265a-d354-4cd7-bbfc-d93e19cbede6%28Office.15%29.aspx) attribute for each item being processed.</span></span> <span data-ttu-id="e60b6-186">La siguiente es la estructura básica de **ResponseMessageType**, el tipo base del que se derivan todos los mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="e60b6-186">The following is the basic structure of the **ResponseMessageType**, the base type from which all response messages are derived.</span></span> 
  
```XML
<ResponseMessage ResponseClass="Success | Warning | Error">
            <MessageText/>
            <ResponseCode/>
            <DescriptiveLinkKey/>
            <MessageXml/>
</ResponseMessage>
```

<span data-ttu-id="e60b6-187">El atributo **ResponseClass** se establece en **Success** si el contacto se ha procesado correctamente, o **error** si el contacto no se ha procesado correctamente.</span><span class="sxs-lookup"><span data-stu-id="e60b6-187">The **ResponseClass** attribute is set to **Success** if the contact was processed successfully, or **Error** if the contact was not processed successfully.</span></span> <span data-ttu-id="e60b6-188">Para los contactos, no encontrará ninguna **ADVERTENCIA** durante el procesamiento por lotes.</span><span class="sxs-lookup"><span data-stu-id="e60b6-188">For contacts, you will not encounter a **Warning** during batch processing.</span></span> <span data-ttu-id="e60b6-189">Si el **ResponseClass** es **correcto**, el elemento [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) que sigue también se establece siempre en **NoError**.</span><span class="sxs-lookup"><span data-stu-id="e60b6-189">If the **ResponseClass** is **Success**, the [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element that follows is also always set to **NoError**.</span></span> <span data-ttu-id="e60b6-190">Si el **ResponseClass** es **error**, debe comprobar los valores de los elementos [MessageText](https://msdn.microsoft.com/library/59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1%28Office.15%29.aspx), **ResponseCode**y [MessageXml](https://msdn.microsoft.com/library/bcaf9e35-d351-48f3-baad-f90c633cba8a%28Office.15%29.aspx) para determinar la causa del problema.</span><span class="sxs-lookup"><span data-stu-id="e60b6-190">If the **ResponseClass** is **Error**, you need to check the values of the [MessageText](https://msdn.microsoft.com/library/59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1%28Office.15%29.aspx), **ResponseCode**, and [MessageXml](https://msdn.microsoft.com/library/bcaf9e35-d351-48f3-baad-f90c633cba8a%28Office.15%29.aspx) elements to determine what caused the problem.</span></span> <span data-ttu-id="e60b6-191">[DescriptiveLinkKey](https://msdn.microsoft.com/library/f7f36749-00f3-4915-b17c-e3caa0af6e67%28Office.15%29.aspx) actualmente no está en uso.</span><span class="sxs-lookup"><span data-stu-id="e60b6-191">[DescriptiveLinkKey](https://msdn.microsoft.com/library/f7f36749-00f3-4915-b17c-e3caa0af6e67%28Office.15%29.aspx) is currently unused.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e60b6-192">Vea también</span><span class="sxs-lookup"><span data-stu-id="e60b6-192">See also</span></span>


- [<span data-ttu-id="e60b6-193">Personas y contactos de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="e60b6-193">People and contacts in EWS in Exchange</span></span>](people-and-contacts-in-ews-in-exchange.md)
    
- [<span data-ttu-id="e60b6-194">Procesar mensajes de correo electrónico en lotes mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="e60b6-194">Process email messages in batches by using EWS in Exchange</span></span>](how-to-process-email-messages-in-batches-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="e60b6-195">Procesar elementos de calendario en lotes en Exchange</span><span class="sxs-lookup"><span data-stu-id="e60b6-195">Process calendar items in batches in Exchange</span></span>](how-to-process-calendar-items-in-batches-in-exchange.md)
    

