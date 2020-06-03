---
title: Administración de la configuración de aplicaciones persistentes mediante EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 90f561f2-e40e-4f5b-b321-f86dbf4a1b71
description: Obtenga información sobre cómo crear, buscar, obtener, actualizar y eliminar la configuración de la aplicación persistente mediante la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: ab7b3ef5f87d8a26a412ca7187dc93c58d73112f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455733"
---
# <a name="manage-persistent-application-settings-by-using-ews-in-exchange"></a><span data-ttu-id="7014e-103">Administración de la configuración de aplicaciones persistentes mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="7014e-103">Manage persistent application settings by using EWS in Exchange</span></span>

<span data-ttu-id="7014e-104">Obtenga información sobre cómo crear, buscar, obtener, actualizar y eliminar la configuración de la aplicación persistente mediante la API administrada de EWS o EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="7014e-104">Learn how to create, find, get, update, and delete persistent application settings by using the EWS Managed API or EWS in Exchange.</span></span> 
  
<span data-ttu-id="7014e-105">Los objetos de configuración de usuario son la mejor opción para almacenar las opciones de configuración de la aplicación cliente de Exchange, principalmente porque están ocultos de los resultados de búsqueda en la mayoría de las aplicaciones cliente.</span><span class="sxs-lookup"><span data-stu-id="7014e-105">User configuration objects are the best option for storing configuration settings for your Exchange client application, primarily because they are hidden from search results in most client applications.</span></span> <span data-ttu-id="7014e-106">Normalmente, las aplicaciones cliente ocultan esta configuración porque el usuario final no tiene que verlas y, por lo tanto, el usuario no tiene acceso a esta información por accidente.</span><span class="sxs-lookup"><span data-stu-id="7014e-106">Client applications typically hide these settings because the end user doesn't need to see them, and so that the user doesn't accidentally access this information.</span></span> <span data-ttu-id="7014e-107">Los ejemplos de código de este artículo muestran cómo puede usar los objetos de configuración de usuario para administrar la configuración persistente, incluido cómo crear, buscar, obtener, actualizar y eliminar la configuración de aplicaciones persistentes que se almacenan en los objetos de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="7014e-107">The code examples in this article show you how you can use user configuration objects to manage persistent settings, including how to create, find, get, update, and delete persistent application settings that are stored in user configuration objects.</span></span>

<span data-ttu-id="7014e-108"><a name="createconfiguration"> </a></span><span class="sxs-lookup"><span data-stu-id="7014e-108"><a name="createconfiguration"> </a></span></span>

## <a name="create-an-application-setting-by-using-the-ews-managed-api"></a><span data-ttu-id="7014e-109">Crear una configuración de aplicación mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="7014e-109">Create an application setting by using the EWS Managed API</span></span>

<span data-ttu-id="7014e-110">Puede usar el método de la API administrada de EWS [UserConfiguration. Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.save%28v=exchg.80%29.aspx) para crear una opción de configuración personalizada.</span><span class="sxs-lookup"><span data-stu-id="7014e-110">You can use the [UserConfiguration.Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.save%28v=exchg.80%29.aspx) EWS Managed API method to create a custom configuration setting.</span></span> <span data-ttu-id="7014e-111">Un objeto de configuración de usuario puede contener XML, Binary, un diccionario de datos o una combinación de estos tres tipos de datos.</span><span class="sxs-lookup"><span data-stu-id="7014e-111">A user configuration object can contain XML, binary, a data dictionary, or a combination of those three data types.</span></span> <span data-ttu-id="7014e-112">En el siguiente ejemplo se muestra cómo guardar un objeto de configuración de usuario denominado ContosoDraftSettings que contiene datos binarios en la carpeta Borradores mediante la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="7014e-112">The following example shows how to save a user configuration object named ContosoDraftSettings that contains binary data to your Drafts folder by using the EWS Managed API.</span></span> <span data-ttu-id="7014e-113">Esto puede ser útil si desea almacenar información de configuración acerca de cómo se muestran los elementos borradores en la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="7014e-113">This might be useful if you want to store configuration information about how draft items are displayed in your client application.</span></span> 
  
```cs
private static void CreateUserConfiguration(ExchangeService service, byte[] binaryData)
{
    // Create the user configuration object.
    UserConfiguration configDrafts = new UserConfiguration(service);
    // Add user configuration data to the BinaryData property.
    configDrafts.BinaryData = binaryData;
    // Name and save the user configuration object on the Drafts folder.
    // This results in a call to EWS.
    configDrafts.Save("ContosoDraftSettings", WellKnownFolderName.Drafts);
}
```

## <a name="create-an-application-setting-by-using-ews"></a><span data-ttu-id="7014e-114">Crear una configuración de aplicación mediante EWS</span><span class="sxs-lookup"><span data-stu-id="7014e-114">Create an application setting by using EWS</span></span>
<span data-ttu-id="7014e-115"><a name="bk_createEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="7014e-115"><a name="bk_createEWS"> </a></span></span>

<span data-ttu-id="7014e-116">Puede usar la operación de EWS de [CreateUserConfiguration](https://msdn.microsoft.com/library/eb5b8ab6-9743-481c-aac9-f9aa889bd353%28Office.15%29.aspx) para crear una opción de configuración personalizada.</span><span class="sxs-lookup"><span data-stu-id="7014e-116">You can use the [CreateUserConfiguration](https://msdn.microsoft.com/library/eb5b8ab6-9743-481c-aac9-f9aa889bd353%28Office.15%29.aspx) EWS operation to create a custom configuration setting.</span></span> <span data-ttu-id="7014e-117">En el ejemplo siguiente se muestra el XML de la solicitud para crear un objeto de configuración de usuario denominado ContosoDraftSettings.</span><span class="sxs-lookup"><span data-stu-id="7014e-117">The following example shows the request XML for creating a user configuration object named ContosoDraftSettings.</span></span> <span data-ttu-id="7014e-118">La solicitud intenta guardar una secuencia binaria en un objeto de configuración de usuario de la carpeta Borradores.</span><span class="sxs-lookup"><span data-stu-id="7014e-118">The request attempts to save a binary stream to a user configuration object on the Drafts folder.</span></span> <span data-ttu-id="7014e-119">Se trata del mismo XML generado por el ejemplo de la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="7014e-119">This is the same XML that is generated by the EWS Managed API example.</span></span> 
  
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
    <m:CreateUserConfiguration>
      <m:UserConfiguration>
        <t:UserConfigurationName Name="ContosoDraftSettings">
          <t:DistinguishedFolderId Id="drafts" />
        </t:UserConfigurationName>
        <t:BinaryData>iVBORw0KGH5UhKquRSzaeAAAAAElFTkSuQmCC</t:BinaryData>
      </m:UserConfiguration>
    </m:CreateUserConfiguration>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="7014e-120">El [XML de respuesta](https://msdn.microsoft.com/library/eb5b8ab6-9743-481c-aac9-f9aa889bd353%28Office.15%29.aspx) es sencillo e indica si la solicitud de creación se ha realizado correctamente o si se ha producido un error.</span><span class="sxs-lookup"><span data-stu-id="7014e-120">The [response XML](https://msdn.microsoft.com/library/eb5b8ab6-9743-481c-aac9-f9aa889bd353%28Office.15%29.aspx) is simple and indicates whether the create request was successful or whether an error occurred.</span></span> 
  
## <a name="find-an-application-setting-by-using-the-ews-managed-api"></a><span data-ttu-id="7014e-121">Buscar una configuración de aplicación mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="7014e-121">Find an application setting by using the EWS Managed API</span></span>
<span data-ttu-id="7014e-122"><a name="findconfiguration"> </a></span><span class="sxs-lookup"><span data-stu-id="7014e-122"><a name="findconfiguration"> </a></span></span>

<span data-ttu-id="7014e-123">Puede usar el método de API administrada [Folder. FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx) EWS con la opción de recorrido asociada para buscar objetos de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="7014e-123">You can use the [Folder.FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx) EWS Managed API method with the associated traversal option to find user configuration objects.</span></span> <span data-ttu-id="7014e-124">En el ejemplo de código siguiente se muestra cómo buscar objetos de configuración de usuario almacenados en la carpeta Borradores mediante la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="7014e-124">The following code example shows you how to find user configuration objects stored on the Drafts folder by using the EWS Managed API.</span></span> 
  
```cs
private static void FindAssociated(ExchangeService service)
{
    // This is the ItemClass prefix of user configuration objects that are created by using EWS.
    const string userConfigPrefix = "IPM.Configuration.";
            
    // This is the name of a configuration setting created by using EWS.
    string userConfigName = "TestConfig";
    // Return the first five items. 
    ItemView view = new ItemView(5);
    // Request only the properties that you need. Because all the results will be user configuration 
    // objects, you won't need to request the ItemSchema.IsAssociated property, which identifies 
    // user configuration objects.
    PropertySet props = new PropertySet(BasePropertySet.IdOnly, 
                                        ItemSchema.ItemClass);
    view.PropertySet = props;
            
    // Set the traversal to find user configuration objects. 
    view.Traversal = ItemTraversal.Associated;
    // Send the request to search the Drafts folder for all the user configuration objects 
    // in the folder. You do not have to use a search restriction because you will not return
    // a large number of search results. For this scenario, it is better to sort the results
    // on the client. This method results in a call to EWS.
    FindItemsResults<Item> findResults = service.FindItems(WellKnownFolderName.Drafts, view);
    // Output a list of the item classes for the associated items. 
    foreach (Item item in findResults)
    {
        if (item.ItemClass == userConfigPrefix + userConfigName)
        {
            Console.WriteLine("You found the configuration: " + userConfigPrefix + userConfigName);
        }
    }
}
```

## <a name="find-an-application-setting-by-using-ews"></a><span data-ttu-id="7014e-125">Buscar una configuración de aplicación mediante EWS</span><span class="sxs-lookup"><span data-stu-id="7014e-125">Find an application setting by using EWS</span></span>
<span data-ttu-id="7014e-126"><a name="bk_findEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="7014e-126"><a name="bk_findEWS"> </a></span></span>

<span data-ttu-id="7014e-127">Puede usar la operación de EWS de [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) para buscar objetos de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="7014e-127">You can use the [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) EWS operation to find user configuration objects.</span></span> 
  
<span data-ttu-id="7014e-128">En el ejemplo siguiente se muestra la solicitud XML para buscar objetos de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="7014e-128">The following example shows the request XML for finding user configuration objects.</span></span> <span data-ttu-id="7014e-129">Se trata del mismo XML generado por el ejemplo de la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="7014e-129">This is the same XML that is generated by the EWS Managed API example.</span></span>
  
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
    <m:FindItem Traversal="Associated">
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:ItemClass" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:IndexedPageItemView MaxEntriesReturned="5" Offset="0" BasePoint="Beginning" />
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="drafts" />
      </m:ParentFolderIds>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="7014e-130">En el ejemplo siguiente se muestra el XML de respuesta correcto para buscar objetos de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="7014e-130">The following example shows the successful response XML for finding user configuration objects.</span></span> <span data-ttu-id="7014e-131">Este es el mismo XML que se procesa mediante el ejemplo de la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="7014e-131">This is the same XML that is processed by the EWS Managed API example.</span></span> <span data-ttu-id="7014e-132">Tenga en cuenta lo siguiente en este XML de respuesta:</span><span class="sxs-lookup"><span data-stu-id="7014e-132">Note the following in this response XML:</span></span> 
  
- <span data-ttu-id="7014e-133">Se ha abreviado el identificador y las teclas de cambio para facilitar su lectura.</span><span class="sxs-lookup"><span data-stu-id="7014e-133">We shortened the identifier and change keys for readability.</span></span>
    
- <span data-ttu-id="7014e-134">Los dos objetos de configuración de usuario se devuelven como mensajes.</span><span class="sxs-lookup"><span data-stu-id="7014e-134">The two user configuration objects are returned as messages.</span></span> <span data-ttu-id="7014e-135">Esto se debe a que la operación **FindItem** devuelve todos los elementos que no están definidos en el esquema EWS como elementos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="7014e-135">This is because the **FindItem** operation returns all items that are not defined in the EWS schema as message items.</span></span> 
    
- <span data-ttu-id="7014e-136">Las propiedades [ItemClass](https://msdn.microsoft.com/library/56020078-50b4-4880-894a-a9f234033cfb%28Office.15%29.aspx) de los dos objetos de configuración de usuario son diferentes.</span><span class="sxs-lookup"><span data-stu-id="7014e-136">The [ItemClass](https://msdn.microsoft.com/library/56020078-50b4-4880-894a-a9f234033cfb%28Office.15%29.aspx) properties for the two user configuration objects are different.</span></span> <span data-ttu-id="7014e-137">El primer objeto de configuración de usuario se creó con EWS.</span><span class="sxs-lookup"><span data-stu-id="7014e-137">The first user configuration object was created by using EWS.</span></span> <span data-ttu-id="7014e-138">El segundo objeto fue creado por otra API.</span><span class="sxs-lookup"><span data-stu-id="7014e-138">The second object was created by another API.</span></span> 
    
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" 
                         MinorVersion="0" 
                         MajorBuildNumber="800" 
                         MinorBuildNumber="5" 
                         Version="V2_6" 
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="2" 
                        TotalItemsInView="2" 
                        IncludesLastItemInRange="true">
            <t:Items>
              <t:Message>
                <t:ItemId Id="AAMkDEY9M6AAA=" ChangeKey="CQAAACYnYF5aFMwP0T" />
                <t:ItemClass>IPM.Configuration.TestConfig</t:ItemClass>
              </t:Message>
              <t:Message>
                <t:ItemId Id="AAkADEzOzFAAA=" ChangeKey="CQAAABQAAABAByOw==" />
                <t:ItemClass>IPM.Microsoft.FolderDesign.NamedView</t:ItemClass>
              </t:Message>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>
```

## <a name="get-and-update-application-settings-by-using-the-ews-managed-api"></a><span data-ttu-id="7014e-139">Obtener y actualizar la configuración de la aplicación mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="7014e-139">Get and update application settings by using the EWS Managed API</span></span>
<span data-ttu-id="7014e-140"><a name="getconfiguration"> </a></span><span class="sxs-lookup"><span data-stu-id="7014e-140"><a name="getconfiguration"> </a></span></span>

<span data-ttu-id="7014e-141">Después de encontrar un objeto de configuración de usuario, puede usar el método de la API administrada de EWS [UserConfiguration. bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.bind%28v=exchg.80%29.aspx) para obtener el objeto de configuración del buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="7014e-141">After you find a user configuration object, you can use the [UserConfiguration.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.bind%28v=exchg.80%29.aspx) EWS Managed API method to get the configuration object from the mailbox.</span></span> <span data-ttu-id="7014e-142">Después de obtener el objeto Configuration, puede usar el método [UserConfiguration. Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.bind%28v=exchg.80%29.aspx) para actualizarlo.</span><span class="sxs-lookup"><span data-stu-id="7014e-142">After you get the configuration object, you can use the [UserConfiguration.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.bind%28v=exchg.80%29.aspx) method to update it.</span></span> <span data-ttu-id="7014e-143">En el siguiente ejemplo, se muestra cómo obtener y actualizar un objeto de configuración de usuario mediante la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="7014e-143">The following example shows how to get and update a user configuration object by using the EWS Managed API.</span></span> 
  
```cs
private static void GetAndUpdateUserConfiguration(ExchangeService service)
{
    // Binds to a user configuration object named "TestConfig" in the user's mailbox. 
    // Results in a call to EWS. You can also use the Load method to get the latest
    // server version of the user configuration object.
    UserConfiguration usrConfig = UserConfiguration.Bind(service,
                                                         "TestConfig",
                                                         WellKnownFolderName.Drafts,
                                                         UserConfigurationProperties.All);
            
    // Display the returned configuration object property values.
    if (usrConfig.XmlData != null)
    {
        Console.WriteLine("XmlData: " + Encoding.UTF8.GetString(usrConfig.XmlData));
    }
    if (usrConfig.BinaryData != null)
    {
        Console.WriteLine("BinaryData: " + Encoding.UTF8.GetString(usrConfig.BinaryData));
    }
    if (usrConfig.Dictionary.Count > 0)
    {
        Console.WriteLine("Contains {0} dictionary entries", usrConfig.Dictionary.Count);
    }
    // Add dictionary property values to the local copy of the object.
    usrConfig.Dictionary.Add("Key5", 1);
    // Updates the server version of the user configuration object 
    // if it has changed on the client. Results in a call to EWS.
    if (usrConfig.IsDirty)
    {
        usrConfig.Update();
    }
}
```

## <a name="get-and-update-application-settings-by-using-ews"></a><span data-ttu-id="7014e-144">Obtener y actualizar la configuración de la aplicación mediante EWS</span><span class="sxs-lookup"><span data-stu-id="7014e-144">Get and update application settings by using EWS</span></span>
<span data-ttu-id="7014e-145"><a name="bk_getEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="7014e-145"><a name="bk_getEWS"> </a></span></span>

<span data-ttu-id="7014e-146">Puede usar la operación de EWS de [GetUserConfiguration](https://msdn.microsoft.com/library/71d50e3c-92bd-435f-8118-b28bb85f8138%28Office.15%29.aspx) para recuperar el objeto de configuración del buzón de correo y el [UpdateUserConfiguration](https://msdn.microsoft.com/library/eda73b62-6a3a-43ae-8fd9-f30892811f27%28Office.15%29.aspx) para actualizar el objeto.</span><span class="sxs-lookup"><span data-stu-id="7014e-146">You can use the [GetUserConfiguration](https://msdn.microsoft.com/library/71d50e3c-92bd-435f-8118-b28bb85f8138%28Office.15%29.aspx) EWS operation to retrieve the configuration object from the mailbox, and the [UpdateUserConfiguration](https://msdn.microsoft.com/library/eda73b62-6a3a-43ae-8fd9-f30892811f27%28Office.15%29.aspx) to update the object.</span></span> <span data-ttu-id="7014e-147">En el siguiente ejemplo se muestra la solicitud XML para obtener un objeto de configuración de usuario denominado TestConfig.</span><span class="sxs-lookup"><span data-stu-id="7014e-147">The following example shows the request XML for getting a user configuration object named TestConfig.</span></span> <span data-ttu-id="7014e-148">La solicitud indica que todas las configuraciones deben devolverse en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7014e-148">The request states that all configurations should be returned in the response.</span></span> <span data-ttu-id="7014e-149">Se trata del mismo XML generado por el ejemplo de la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="7014e-149">This is the same XML that is generated by the EWS Managed API example.</span></span> 
  
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
    <m:GetUserConfiguration>
      <m:UserConfigurationName Name="TestConfig">
        <t:DistinguishedFolderId Id="drafts" />
      </m:UserConfigurationName>
      <m:UserConfigurationProperties>All</m:UserConfigurationProperties>
    </m:GetUserConfiguration>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="7014e-150">En el ejemplo siguiente se muestra el XML de respuesta correcta para obtener objetos de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="7014e-150">The following example shows the successful response XML for getting a user configuration objects.</span></span> <span data-ttu-id="7014e-151">La respuesta contiene un diccionario de datos.</span><span class="sxs-lookup"><span data-stu-id="7014e-151">The response contains a data dictionary.</span></span> <span data-ttu-id="7014e-152">Este es el mismo XML que se procesa mediante el ejemplo de la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="7014e-152">This is the same XML that is processed by the EWS Managed API example.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" 
                         MinorVersion="0" 
                         MajorBuildNumber="800" 
                         MinorBuildNumber="5" 
                         Version="V2_6" 
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetUserConfigurationResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetUserConfigurationResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:UserConfiguration>
            <t:UserConfigurationName Name="TestConfig">
              <t:DistinguishedFolderId Id="drafts" />
            </t:UserConfigurationName>
            <t:ItemId Id="AAMkDEY9M6AAA=" ChangeKey="CQAAACYnYF5aFMwP0T" />
            <t:Dictionary>
              <t:DictionaryEntry>
                <t:DictionaryKey>
                  <t:Type>String</t:Type>
                  <t:Value>Key1</t:Value>
                </t:DictionaryKey>
                <t:DictionaryValue>
                  <t:Type>Integer32</t:Type>
                  <t:Value>1</t:Value>
                </t:DictionaryValue>
              </t:DictionaryEntry>
              <t:DictionaryEntry>
                <t:DictionaryKey>
                  <t:Type>String</t:Type>
                  <t:Value>PhoneNumber</t:Value>
                </t:DictionaryKey>
                <t:DictionaryValue>
                  <t:Type>String</t:Type>
                  <t:Value>555-555-1111</t:Value>
                </t:DictionaryValue>
              </t:DictionaryEntry>
            </t:Dictionary>
          </m:UserConfiguration>
        </m:GetUserConfigurationResponseMessage>
      </m:ResponseMessages>
    </m:GetUserConfigurationResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="7014e-153">En el ejemplo siguiente se muestra el XML de la solicitud para actualizar un objeto de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="7014e-153">The following example shows the request XML for updating a user configuration object.</span></span> <span data-ttu-id="7014e-154">La solicitud indica que todas las configuraciones deben devolverse en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7014e-154">The request states that all configurations should be returned in the response.</span></span> <span data-ttu-id="7014e-155">Se trata del mismo XML generado por el ejemplo de la API administrada de EWS que llama al método **UserConfiguration. Update** .</span><span class="sxs-lookup"><span data-stu-id="7014e-155">This is the same XML that is generated by the EWS Managed API example that calls the **UserConfiguration.Update** method.</span></span> <span data-ttu-id="7014e-156">Puede ver que el XML de actualización contiene las entradas de diccionario existentes y la adicional que se agregó antes de la actualización.</span><span class="sxs-lookup"><span data-stu-id="7014e-156">You can see that the update XML contains the existing dictionary entries and the additional one that was added before the update.</span></span> 
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
  <soap:Body>
    <m:UpdateUserConfiguration>
      <m:UserConfiguration>
        <t:UserConfigurationName Name="TestConfig">
          <t:DistinguishedFolderId Id="drafts" />
        </t:UserConfigurationName>
        <t:Dictionary>
          <t:DictionaryEntry>
            <t:DictionaryKey>
              <t:Type>String</t:Type>
              <t:Value>Key1</t:Value>
            </t:DictionaryKey>
            <t:DictionaryValue>
              <t:Type>Integer32</t:Type>
              <t:Value>1</t:Value>
            </t:DictionaryValue>
          </t:DictionaryEntry>
          <t:DictionaryEntry>
            <t:DictionaryKey>
              <t:Type>String</t:Type>
              <t:Value>PhoneNumber</t:Value>
            </t:DictionaryKey>
            <t:DictionaryValue>
              <t:Type>String</t:Type>
              <t:Value>555-555-1111</t:Value>
            </t:DictionaryValue>
          </t:DictionaryEntry>
          <t:DictionaryEntry>
            <t:DictionaryKey>
              <t:Type>String</t:Type>
              <t:Value>Key5</t:Value>
            </t:DictionaryKey>
            <t:DictionaryValue>
              <t:Type>Integer32</t:Type>
              <t:Value>1</t:Value>
            </t:DictionaryValue>
          </t:DictionaryEntry>
        </t:Dictionary>
      </m:UserConfiguration>
    </m:UpdateUserConfiguration>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="7014e-157">El [XML de respuesta](https://msdn.microsoft.com/library/eda73b62-6a3a-43ae-8fd9-f30892811f27%28Office.15%29.aspx) es sencillo e indica si la actualización se ha realizado correctamente o si se ha producido un error.</span><span class="sxs-lookup"><span data-stu-id="7014e-157">The [response XML](https://msdn.microsoft.com/library/eda73b62-6a3a-43ae-8fd9-f30892811f27%28Office.15%29.aspx) is simple and indicates whether the update was successful or whether an error occurred.</span></span> 
  
## <a name="delete-an-application-setting-by-using-the-ews-managed-api"></a><span data-ttu-id="7014e-158">Eliminar una configuración de aplicación mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="7014e-158">Delete an application setting by using the EWS Managed API</span></span>
<span data-ttu-id="7014e-159"><a name="deleteconfiguration"> </a></span><span class="sxs-lookup"><span data-stu-id="7014e-159"><a name="deleteconfiguration"> </a></span></span>

<span data-ttu-id="7014e-160">Puede usar el método [UserConfiguration. Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.delete%28v=exchg.80%29.aspx) de la API administrada de EWS para eliminar objetos de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="7014e-160">You can use the [UserConfiguration.Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.delete%28v=exchg.80%29.aspx) EWS Managed API method to delete user configuration objects.</span></span> <span data-ttu-id="7014e-161">El siguiente ejemplo de código muestra cómo eliminar el objeto de configuración de usuario ContosoDraftSettings mediante la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="7014e-161">The following code example shows you how to delete the ContosoDraftSettings user configuration object by using the EWS Managed API.</span></span> 
  
```cs
private static void DeleteUserConfiguration(ExchangeService service)
{
    // Binds to a user configuration object. Results in a call to EWS.
    UserConfiguration usrConfig = UserConfiguration.Bind(service,
                                                        "ContosoDraftSettings",
                                                        WellKnownFolderName.Drafts,
                                                        UserConfigurationProperties.Id);
    // Deletes the user configuration object.
    // Results in a call to EWS.
    usrConfig.Delete();
}
```

## <a name="delete-an-application-setting-by-using-ews"></a><span data-ttu-id="7014e-162">Eliminar una configuración de aplicación mediante EWS</span><span class="sxs-lookup"><span data-stu-id="7014e-162">Delete an application setting by using EWS</span></span>
<span data-ttu-id="7014e-163"><a name="bk_deleteEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="7014e-163"><a name="bk_deleteEWS"> </a></span></span>

<span data-ttu-id="7014e-164">Puede usar la operación de EWS de [DeleteUserConfiguration](https://msdn.microsoft.com/library/93e44690-be2d-4fdb-96a8-4ded3c193aed%28Office.15%29.aspx) para eliminar objetos de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="7014e-164">You can use the [DeleteUserConfiguration](https://msdn.microsoft.com/library/93e44690-be2d-4fdb-96a8-4ded3c193aed%28Office.15%29.aspx) EWS operation to delete user configuration objects.</span></span> 
  
<span data-ttu-id="7014e-165">En el siguiente ejemplo se muestra el XML de la solicitud para eliminar un objeto de configuración de usuario denominado ContosoDraftSettings que se aplicó a la carpeta Borradores.</span><span class="sxs-lookup"><span data-stu-id="7014e-165">The following example shows the request XML for deleting a user configuration object named ContosoDraftSettings that was applied to the Drafts folder.</span></span> <span data-ttu-id="7014e-166">Se trata del mismo XML generado por el ejemplo de la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="7014e-166">This is the same XML that is generated by the EWS Managed API example.</span></span>
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
  <soap:Body>
    <m:DeleteUserConfiguration>
      <m:UserConfigurationName Name="ContosoDraftSettings">
        <t:DistinguishedFolderId Id="drafts" />
      </m:UserConfigurationName>
    </m:DeleteUserConfiguration>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="7014e-167">El [XML de respuesta](https://msdn.microsoft.com/library/93e44690-be2d-4fdb-96a8-4ded3c193aed%28Office.15%29.aspx) es sencillo e indica si la solicitud de eliminación se ha realizado correctamente o si se ha producido un error.</span><span class="sxs-lookup"><span data-stu-id="7014e-167">The [response XML](https://msdn.microsoft.com/library/93e44690-be2d-4fdb-96a8-4ded3c193aed%28Office.15%29.aspx) is simple and indicates whether the delete request was a success or whether an error occurred.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7014e-168">Vea también</span><span class="sxs-lookup"><span data-stu-id="7014e-168">See also</span></span>

- [<span data-ttu-id="7014e-169">Configuración de aplicación persistente en EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="7014e-169">Persistent application settings in EWS in Exchange</span></span>](persistent-application-settings-in-ews-in-exchange.md)
- [<span data-ttu-id="7014e-170">Introducción al diseño de EWS cliente de Exchange</span><span class="sxs-lookup"><span data-stu-id="7014e-170">EWS client design overview for Exchange</span></span>](ews-client-design-overview-for-exchange.md)   
- [<span data-ttu-id="7014e-171">Desarrollo de clientes de servicios web de Exchange</span><span class="sxs-lookup"><span data-stu-id="7014e-171">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)
    

