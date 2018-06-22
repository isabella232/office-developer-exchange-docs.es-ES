---
title: Administrar la configuración de aplicación persistente mediante el uso de EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 90f561f2-e40e-4f5b-b321-f86dbf4a1b71
description: Obtenga información sobre cómo crear, buscar, obtener, actualizar y eliminar la configuración de la aplicación persistentes mediante el uso de la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: ab5a9cc927bd0a6c4efacce622cc71db1a9b02a3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763102"
---
# <a name="manage-persistent-application-settings-by-using-ews-in-exchange"></a><span data-ttu-id="e6af8-103">Administrar la configuración de aplicación persistente mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="e6af8-103">Manage persistent application settings by using EWS in Exchange</span></span>

<span data-ttu-id="e6af8-104">Obtenga información sobre cómo crear, buscar, obtener, actualizar y eliminar la configuración de la aplicación persistentes mediante el uso de la API administrada de EWS o EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="e6af8-104">Learn how to create, find, get, update, and delete persistent application settings by using the EWS Managed API or EWS in Exchange.</span></span> 
  
<span data-ttu-id="e6af8-105">Objetos de configuración de usuario son la mejor opción para almacenar la configuración para la aplicación de cliente de Exchange, principalmente debido a que están ocultos de los resultados de búsqueda en la mayoría de las aplicaciones cliente.</span><span class="sxs-lookup"><span data-stu-id="e6af8-105">User configuration objects are the best option for storing configuration settings for your Exchange client application, primarily because they are hidden from search results in most client applications.</span></span> <span data-ttu-id="e6af8-106">Las aplicaciones cliente normalmente ocultación estas opciones de configuración debido a que el usuario final no necesita verlos y, por lo que el usuario accidentalmente no tener acceso a esta información.</span><span class="sxs-lookup"><span data-stu-id="e6af8-106">Client applications typically hide these settings because the end user doesn't need to see them, and so that the user doesn't accidentally access this information.</span></span> <span data-ttu-id="e6af8-107">Los ejemplos de código en este artículo muestran que cómo puede usar objetos de configuración de usuario para administrar la configuración persistente, incluido cómo crear, busca, obtener, actualiza y elimina la configuración de aplicación persistente que se almacena en objetos de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="e6af8-107">The code examples in this article show you how you can use user configuration objects to manage persistent settings, including how to create, find, get, update, and delete persistent application settings that are stored in user configuration objects.</span></span>

<span data-ttu-id="e6af8-108"><a name="createconfiguration"> </a></span><span class="sxs-lookup"><span data-stu-id="e6af8-108"></span></span>

## <a name="create-an-application-setting-by-using-the-ews-managed-api"></a><span data-ttu-id="e6af8-109">Crear una configuración de aplicación mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="e6af8-109">Create an application setting by using the EWS Managed API</span></span>

<span data-ttu-id="e6af8-110">Puede usar el método de la API administrada de EWS [UserConfiguration.Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.userconfiguration.save%28v=exchg.80%29.aspx) para crear una opción de configuración personalizado.</span><span class="sxs-lookup"><span data-stu-id="e6af8-110">You can use the [UserConfiguration.Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.userconfiguration.save%28v=exchg.80%29.aspx) EWS Managed API method to create a custom configuration setting.</span></span> <span data-ttu-id="e6af8-111">Un objeto de configuración de usuario puede contener XML, binario, un diccionario de datos o una combinación de los tres tipos de datos.</span><span class="sxs-lookup"><span data-stu-id="e6af8-111">A user configuration object can contain XML, binary, a data dictionary, or a combination of those three data types.</span></span> <span data-ttu-id="e6af8-112">En el ejemplo siguiente se muestra cómo guardar un objeto de configuración de usuario denominado ContosoDraftSettings que contiene datos binarios en la carpeta Borrador mediante el uso de la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="e6af8-112">The following example shows how to save a user configuration object named ContosoDraftSettings that contains binary data to your Drafts folder by using the EWS Managed API.</span></span> <span data-ttu-id="e6af8-113">Esto puede resultar útil si desea almacenar la información de configuración acerca de cómo se muestran los elementos de borrador en la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="e6af8-113">This might be useful if you want to store configuration information about how draft items are displayed in your client application.</span></span> 
  
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

## <a name="create-an-application-setting-by-using-ews"></a><span data-ttu-id="e6af8-114">Crear una configuración de aplicación mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="e6af8-114">Create an application setting by using EWS</span></span>
<span data-ttu-id="e6af8-115"><a name="bk_createEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="e6af8-115"></span></span>

<span data-ttu-id="e6af8-116">Puede usar la operación de EWS [CreateUserConfiguration](http://msdn.microsoft.com/library/eb5b8ab6-9743-481c-aac9-f9aa889bd353%28Office.15%29.aspx) para crear una opción de configuración personalizado.</span><span class="sxs-lookup"><span data-stu-id="e6af8-116">You can use the [CreateUserConfiguration](http://msdn.microsoft.com/library/eb5b8ab6-9743-481c-aac9-f9aa889bd353%28Office.15%29.aspx) EWS operation to create a custom configuration setting.</span></span> <span data-ttu-id="e6af8-117">En el ejemplo siguiente se muestra la solicitud de XML para la creación de un objeto de configuración de usuario denominado ContosoDraftSettings.</span><span class="sxs-lookup"><span data-stu-id="e6af8-117">The following example shows the request XML for creating a user configuration object named ContosoDraftSettings.</span></span> <span data-ttu-id="e6af8-118">La solicitud intenta guardar una secuencia binaria a un objeto de configuración de usuario en la carpeta Borradores.</span><span class="sxs-lookup"><span data-stu-id="e6af8-118">The request attempts to save a binary stream to a user configuration object on the Drafts folder.</span></span> <span data-ttu-id="e6af8-119">Este es el mismo XML generado por el ejemplo de la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="e6af8-119">This is the same XML that is generated by the EWS Managed API example.</span></span> 
  
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

<span data-ttu-id="e6af8-120">El [XML de la respuesta](http://msdn.microsoft.com/library/eb5b8ab6-9743-481c-aac9-f9aa889bd353%28Office.15%29.aspx) es simple y se indica si la solicitud de creación fue correcta o si se produjo un error.</span><span class="sxs-lookup"><span data-stu-id="e6af8-120">The [response XML](http://msdn.microsoft.com/library/eb5b8ab6-9743-481c-aac9-f9aa889bd353%28Office.15%29.aspx) is simple and indicates whether the create request was successful or whether an error occurred.</span></span> 
  
## <a name="find-an-application-setting-by-using-the-ews-managed-api"></a><span data-ttu-id="e6af8-121">Buscar configuración de la aplicación mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="e6af8-121">Find an application setting by using the EWS Managed API</span></span>
<span data-ttu-id="e6af8-122"><a name="findconfiguration"> </a></span><span class="sxs-lookup"><span data-stu-id="e6af8-122"></span></span>

<span data-ttu-id="e6af8-123">Puede usar el método de la API administrada de EWS [Folder.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx) con la opción de cruce seguro de los asociados para buscar objetos de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="e6af8-123">You can use the [Folder.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx) EWS Managed API method with the associated traversal option to find user configuration objects.</span></span> <span data-ttu-id="e6af8-124">En el ejemplo de código siguiente se muestra cómo buscar objetos de configuración de usuario almacenados en la carpeta Borradores mediante la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="e6af8-124">The following code example shows you how to find user configuration objects stored on the Drafts folder by using the EWS Managed API.</span></span> 
  
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

## <a name="find-an-application-setting-by-using-ews"></a><span data-ttu-id="e6af8-125">Buscar configuración de la aplicación mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="e6af8-125">Find an application setting by using EWS</span></span>
<span data-ttu-id="e6af8-126"><a name="bk_findEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="e6af8-126"></span></span>

<span data-ttu-id="e6af8-127">Puede usar la operación de EWS [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) para buscar objetos de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="e6af8-127">You can use the [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) EWS operation to find user configuration objects.</span></span> 
  
<span data-ttu-id="e6af8-128">En el ejemplo siguiente se muestra la solicitud XML para buscar objetos de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="e6af8-128">The following example shows the request XML for finding user configuration objects.</span></span> <span data-ttu-id="e6af8-129">Este es el mismo XML generado por el ejemplo de la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="e6af8-129">This is the same XML that is generated by the EWS Managed API example.</span></span>
  
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

<span data-ttu-id="e6af8-130">En el ejemplo siguiente se muestra el XML de la respuesta correcta para buscar objetos de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="e6af8-130">The following example shows the successful response XML for finding user configuration objects.</span></span> <span data-ttu-id="e6af8-131">Este es el mismo XML que se procesa en el ejemplo de la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="e6af8-131">This is the same XML that is processed by the EWS Managed API example.</span></span> <span data-ttu-id="e6af8-132">Tenga en cuenta lo siguiente en esta respuesta XML:</span><span class="sxs-lookup"><span data-stu-id="e6af8-132">Note the following in this response XML:</span></span> 
  
- <span data-ttu-id="e6af8-133">Se acortan las claves de identificador y cambiar para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="e6af8-133">We shortened the identifier and change keys for readability.</span></span>
    
- <span data-ttu-id="e6af8-134">Los objetos de configuración de dos usuario se devuelven como mensajes.</span><span class="sxs-lookup"><span data-stu-id="e6af8-134">The two user configuration objects are returned as messages.</span></span> <span data-ttu-id="e6af8-135">Esto es debido a que la operación **FindItem** devuelve todos los elementos que no están definidos en el esquema EWS como elementos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="e6af8-135">This is because the **FindItem** operation returns all items that are not defined in the EWS schema as message items.</span></span> 
    
- <span data-ttu-id="e6af8-136">Las propiedades [ItemClass](http://msdn.microsoft.com/library/56020078-50b4-4880-894a-a9f234033cfb%28Office.15%29.aspx) para los objetos de configuración de dos usuario son diferentes.</span><span class="sxs-lookup"><span data-stu-id="e6af8-136">The [ItemClass](http://msdn.microsoft.com/library/56020078-50b4-4880-894a-a9f234033cfb%28Office.15%29.aspx) properties for the two user configuration objects are different.</span></span> <span data-ttu-id="e6af8-137">El primer objeto de configuración de usuario se ha creado mediante EWS.</span><span class="sxs-lookup"><span data-stu-id="e6af8-137">The first user configuration object was created by using EWS.</span></span> <span data-ttu-id="e6af8-138">El segundo objeto fue creado por otra API.</span><span class="sxs-lookup"><span data-stu-id="e6af8-138">The second object was created by another API.</span></span> 
    
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" 
                         MinorVersion="0" 
                         MajorBuildNumber="800" 
                         MinorBuildNumber="5" 
                         Version="V2_6" 
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="get-and-update-application-settings-by-using-the-ews-managed-api"></a><span data-ttu-id="e6af8-139">Obtener y actualizar la configuración de la aplicación mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="e6af8-139">Get and update application settings by using the EWS Managed API</span></span>
<span data-ttu-id="e6af8-140"><a name="getconfiguration"> </a></span><span class="sxs-lookup"><span data-stu-id="e6af8-140"></span></span>

<span data-ttu-id="e6af8-141">Después de encontrar un objeto de configuración de usuario, puede usar el método de la API administrada de EWS [UserConfiguration.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.userconfiguration.bind%28v=exchg.80%29.aspx) para obtener el objeto de configuración desde el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="e6af8-141">After you find a user configuration object, you can use the [UserConfiguration.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.userconfiguration.bind%28v=exchg.80%29.aspx) EWS Managed API method to get the configuration object from the mailbox.</span></span> <span data-ttu-id="e6af8-142">Después de obtener el objeto de configuración, puede usar el método [UserConfiguration.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.userconfiguration.bind%28v=exchg.80%29.aspx) para actualizarlo.</span><span class="sxs-lookup"><span data-stu-id="e6af8-142">After you get the configuration object, you can use the [UserConfiguration.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.userconfiguration.bind%28v=exchg.80%29.aspx) method to update it.</span></span> <span data-ttu-id="e6af8-143">En el ejemplo siguiente se muestra cómo obtener y actualizar un objeto de configuración de usuario mediante el uso de la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="e6af8-143">The following example shows how to get and update a user configuration object by using the EWS Managed API.</span></span> 
  
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

## <a name="get-and-update-application-settings-by-using-ews"></a><span data-ttu-id="e6af8-144">Obtener y actualizar la configuración de la aplicación mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="e6af8-144">Get and update application settings by using EWS</span></span>
<span data-ttu-id="e6af8-145"><a name="bk_getEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="e6af8-145"></span></span>

<span data-ttu-id="e6af8-146">Puede usar la operación de EWS [GetUserConfiguration](http://msdn.microsoft.com/library/71d50e3c-92bd-435f-8118-b28bb85f8138%28Office.15%29.aspx) para recuperar el objeto de configuración desde el buzón de correo y el [UpdateUserConfiguration](http://msdn.microsoft.com/library/eda73b62-6a3a-43ae-8fd9-f30892811f27%28Office.15%29.aspx) para actualizar el objeto.</span><span class="sxs-lookup"><span data-stu-id="e6af8-146">You can use the [GetUserConfiguration](http://msdn.microsoft.com/library/71d50e3c-92bd-435f-8118-b28bb85f8138%28Office.15%29.aspx) EWS operation to retrieve the configuration object from the mailbox, and the [UpdateUserConfiguration](http://msdn.microsoft.com/library/eda73b62-6a3a-43ae-8fd9-f30892811f27%28Office.15%29.aspx) to update the object.</span></span> <span data-ttu-id="e6af8-147">En el ejemplo siguiente se muestra la solicitud de XML para obtener un objeto de configuración de usuario denominado TestConfig.</span><span class="sxs-lookup"><span data-stu-id="e6af8-147">The following example shows the request XML for getting a user configuration object named TestConfig.</span></span> <span data-ttu-id="e6af8-148">La solicitud se indica que se deben devolver todas las configuraciones en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e6af8-148">The request states that all configurations should be returned in the response.</span></span> <span data-ttu-id="e6af8-149">Este es el mismo XML generado por el ejemplo de la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="e6af8-149">This is the same XML that is generated by the EWS Managed API example.</span></span> 
  
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
    <m:GetUserConfiguration>
      <m:UserConfigurationName Name="TestConfig">
        <t:DistinguishedFolderId Id="drafts" />
      </m:UserConfigurationName>
      <m:UserConfigurationProperties>All</m:UserConfigurationProperties>
    </m:GetUserConfiguration>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="e6af8-150">En el ejemplo siguiente se muestra el XML de la respuesta correcta para obtener los objetos de configuración de un usuario.</span><span class="sxs-lookup"><span data-stu-id="e6af8-150">The following example shows the successful response XML for getting a user configuration objects.</span></span> <span data-ttu-id="e6af8-151">La respuesta contiene un diccionario de datos.</span><span class="sxs-lookup"><span data-stu-id="e6af8-151">The response contains a data dictionary.</span></span> <span data-ttu-id="e6af8-152">Este es el mismo XML que se procesa en el ejemplo de la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="e6af8-152">This is the same XML that is processed by the EWS Managed API example.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" 
                         MinorVersion="0" 
                         MajorBuildNumber="800" 
                         MinorBuildNumber="5" 
                         Version="V2_6" 
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetUserConfigurationResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                                    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="e6af8-153">En el ejemplo siguiente se muestra la solicitud XML para actualizar un objeto de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="e6af8-153">The following example shows the request XML for updating a user configuration object.</span></span> <span data-ttu-id="e6af8-154">La solicitud se indica que se deben devolver todas las configuraciones en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e6af8-154">The request states that all configurations should be returned in the response.</span></span> <span data-ttu-id="e6af8-155">Este es el mismo XML generado por el ejemplo de la API administrada de EWS que llama al método **UserConfiguration.Update** .</span><span class="sxs-lookup"><span data-stu-id="e6af8-155">This is the same XML that is generated by the EWS Managed API example that calls the **UserConfiguration.Update** method.</span></span> <span data-ttu-id="e6af8-156">Puede ver que la actualización de XML contiene las entradas de diccionario existente y la adicional que se ha agregado antes de la actualización.</span><span class="sxs-lookup"><span data-stu-id="e6af8-156">You can see that the update XML contains the existing dictionary entries and the additional one that was added before the update.</span></span> 
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="e6af8-157">El [XML de la respuesta](http://msdn.microsoft.com/library/eda73b62-6a3a-43ae-8fd9-f30892811f27%28Office.15%29.aspx) es simple y se indica si la finalización correcta de la actualización o si se produjo un error.</span><span class="sxs-lookup"><span data-stu-id="e6af8-157">The [response XML](http://msdn.microsoft.com/library/eda73b62-6a3a-43ae-8fd9-f30892811f27%28Office.15%29.aspx) is simple and indicates whether the update was successful or whether an error occurred.</span></span> 
  
## <a name="delete-an-application-setting-by-using-the-ews-managed-api"></a><span data-ttu-id="e6af8-158">Eliminar una configuración de aplicación mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="e6af8-158">Delete an application setting by using the EWS Managed API</span></span>
<span data-ttu-id="e6af8-159"><a name="deleteconfiguration"> </a></span><span class="sxs-lookup"><span data-stu-id="e6af8-159"></span></span>

<span data-ttu-id="e6af8-160">Puede usar el método de la API administrada de EWS [UserConfiguration.Delete](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.userconfiguration.delete%28v=exchg.80%29.aspx) para eliminar objetos de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="e6af8-160">You can use the [UserConfiguration.Delete](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.userconfiguration.delete%28v=exchg.80%29.aspx) EWS Managed API method to delete user configuration objects.</span></span> <span data-ttu-id="e6af8-161">En el ejemplo de código siguiente se muestra cómo eliminar el objeto de configuración de usuario de ContosoDraftSettings mediante el uso de la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="e6af8-161">The following code example shows you how to delete the ContosoDraftSettings user configuration object by using the EWS Managed API.</span></span> 
  
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

## <a name="delete-an-application-setting-by-using-ews"></a><span data-ttu-id="e6af8-162">Eliminar una configuración de aplicación mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="e6af8-162">Delete an application setting by using EWS</span></span>
<span data-ttu-id="e6af8-163"><a name="bk_deleteEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="e6af8-163"></span></span>

<span data-ttu-id="e6af8-164">Puede usar la operación de EWS [DeleteUserConfiguration](http://msdn.microsoft.com/library/93e44690-be2d-4fdb-96a8-4ded3c193aed%28Office.15%29.aspx) para eliminar objetos de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="e6af8-164">You can use the [DeleteUserConfiguration](http://msdn.microsoft.com/library/93e44690-be2d-4fdb-96a8-4ded3c193aed%28Office.15%29.aspx) EWS operation to delete user configuration objects.</span></span> 
  
<span data-ttu-id="e6af8-165">En el ejemplo siguiente se muestra la solicitud XML para eliminar un objeto de configuración de usuario denominado ContosoDraftSettings que se aplicó a la carpeta Borradores.</span><span class="sxs-lookup"><span data-stu-id="e6af8-165">The following example shows the request XML for deleting a user configuration object named ContosoDraftSettings that was applied to the Drafts folder.</span></span> <span data-ttu-id="e6af8-166">Este es el mismo XML generado por el ejemplo de la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="e6af8-166">This is the same XML that is generated by the EWS Managed API example.</span></span>
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="e6af8-167">El [XML de la respuesta](http://msdn.microsoft.com/library/93e44690-be2d-4fdb-96a8-4ded3c193aed%28Office.15%29.aspx) es simple y se indica si la solicitud de eliminación fue un éxito o si se produjo un error.</span><span class="sxs-lookup"><span data-stu-id="e6af8-167">The [response XML](http://msdn.microsoft.com/library/93e44690-be2d-4fdb-96a8-4ded3c193aed%28Office.15%29.aspx) is simple and indicates whether the delete request was a success or whether an error occurred.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e6af8-168">Ver también</span><span class="sxs-lookup"><span data-stu-id="e6af8-168">See also</span></span>

- [<span data-ttu-id="e6af8-169">Configuración de aplicación persistente EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="e6af8-169">Persistent application settings in EWS in Exchange</span></span>](persistent-application-settings-in-ews-in-exchange.md)
- [<span data-ttu-id="e6af8-170">Introducción al diseño de EWS cliente de Exchange</span><span class="sxs-lookup"><span data-stu-id="e6af8-170">EWS client design overview for Exchange</span></span>](ews-client-design-overview-for-exchange.md)   
- [<span data-ttu-id="e6af8-171">Desarrollo de clientes de servicios web de Exchange</span><span class="sxs-lookup"><span data-stu-id="e6af8-171">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)
    

