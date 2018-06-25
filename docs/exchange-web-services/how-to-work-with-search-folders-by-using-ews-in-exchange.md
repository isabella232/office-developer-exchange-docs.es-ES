---
title: Trabajar con las carpetas de búsqueda con EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: abe703c5-6d85-46d9-bf20-230c34782a9f
description: Obtenga información acerca de cómo crear, obtener, actualizar y eliminar las carpetas de búsqueda mediante la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: e38ff50fcdb5e42cea3f4b2e25345375f84ae6eb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763221"
---
# <a name="work-with-search-folders-by-using-ews-in-exchange"></a><span data-ttu-id="ae45d-103">Trabajar con las carpetas de búsqueda con EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="ae45d-103">Work with search folders by using EWS in Exchange</span></span>

<span data-ttu-id="ae45d-104">Obtenga información acerca de cómo crear, obtener, actualizar y eliminar las carpetas de búsqueda mediante la API administrada de EWS o EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="ae45d-104">Find out how to create, get, update, and delete search folders by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="ae45d-105">Una carpeta de búsqueda representa una búsqueda persistente "siempre activado" en el buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="ae45d-105">A search folder represents a persistent "always-on" search in a user's mailbox.</span></span> <span data-ttu-id="ae45d-106">Una carpeta de búsqueda tiene el aspecto y actúa como una carpeta de buzón normal.</span><span class="sxs-lookup"><span data-stu-id="ae45d-106">A search folder looks and acts like a regular mailbox folder.</span></span> <span data-ttu-id="ae45d-107">Sin embargo, en lugar de que contiene los elementos, contiene una copia de los elementos de las carpetas en su ámbito de búsqueda que coinciden con los criterios de búsqueda establecidos en la carpeta "virtual".</span><span class="sxs-lookup"><span data-stu-id="ae45d-107">However, instead of containing items, it contains a "virtual" copy of items from any folders in its search scope that match the search criteria set on the folder.</span></span> <span data-ttu-id="ae45d-108">Las aplicaciones y los usuarios finales pueden usar carpetas de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ae45d-108">Both applications and end-users can use search folders.</span></span> <span data-ttu-id="ae45d-109">¿La aplicación necesita para llevar a cabo la misma búsqueda una y otra vez?</span><span class="sxs-lookup"><span data-stu-id="ae45d-109">Does your application need to perform the same search over and over?</span></span> <span data-ttu-id="ae45d-110">Las carpetas de búsqueda son una gran herramienta para esta tarea.</span><span class="sxs-lookup"><span data-stu-id="ae45d-110">Search folders are a great tool for this task.</span></span> <span data-ttu-id="ae45d-111">O quizá simplemente desea ofrecer a los usuarios la capacidad de obtener acceso y administrar las carpetas de búsqueda en el cliente.</span><span class="sxs-lookup"><span data-stu-id="ae45d-111">Or maybe you just want to give your users the ability to access and manage search folders in your client.</span></span> <span data-ttu-id="ae45d-112">Con independencia del escenario, la API administrada de EWS y EWS habilite la aplicación para interactuar totalmente con las carpetas de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ae45d-112">Whatever your scenario, the EWS Managed API and EWS enable your application to fully interact with search folders.</span></span>
  
<span data-ttu-id="ae45d-113">**La tabla 1. Métodos de la API administrada de EWS y las operaciones de EWS para trabajar con carpetas de búsqueda**</span><span class="sxs-lookup"><span data-stu-id="ae45d-113">**Table 1. EWS Managed API methods and EWS operations for working with search folders**</span></span>

|<span data-ttu-id="ae45d-114">**Si quiere...**</span><span class="sxs-lookup"><span data-stu-id="ae45d-114">**If you want to…**</span></span>|<span data-ttu-id="ae45d-115">**En la API administrada de EWS, use...**</span><span class="sxs-lookup"><span data-stu-id="ae45d-115">**In the EWS Managed API, use…**</span></span>|<span data-ttu-id="ae45d-116">**En EWS, use...**</span><span class="sxs-lookup"><span data-stu-id="ae45d-116">**In EWS, use…**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ae45d-117">Crear una carpeta de búsqueda</span><span class="sxs-lookup"><span data-stu-id="ae45d-117">Create a search folder</span></span>  <br/> |[<span data-ttu-id="ae45d-118">SearchFolder.Save</span><span class="sxs-lookup"><span data-stu-id="ae45d-118">SearchFolder.Save</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfolder.save%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="ae45d-119">Operación CreateFolder</span><span class="sxs-lookup"><span data-stu-id="ae45d-119">CreateFolder operation</span></span>](http://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="ae45d-120">Obtener una carpeta de búsqueda</span><span class="sxs-lookup"><span data-stu-id="ae45d-120">Get a search folder</span></span>  <br/> |[<span data-ttu-id="ae45d-121">SearchFolder.Bind</span><span class="sxs-lookup"><span data-stu-id="ae45d-121">SearchFolder.Bind</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfolder.bind%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="ae45d-122">Operación GetFolder</span><span class="sxs-lookup"><span data-stu-id="ae45d-122">GetFolder operation</span></span>](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="ae45d-123">Actualización de una carpeta de búsqueda</span><span class="sxs-lookup"><span data-stu-id="ae45d-123">Update a search folder</span></span>  <br/> |[<span data-ttu-id="ae45d-124">SearchFolder.Update</span><span class="sxs-lookup"><span data-stu-id="ae45d-124">SearchFolder.Update</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="ae45d-125">Operación UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="ae45d-125">UpdateFolder operation</span></span>](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="ae45d-126">Eliminar una carpeta de búsqueda</span><span class="sxs-lookup"><span data-stu-id="ae45d-126">Delete a search folder</span></span>  <br/> |[<span data-ttu-id="ae45d-127">SearchFolder.Delete</span><span class="sxs-lookup"><span data-stu-id="ae45d-127">SearchFolder.Delete</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.delete%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="ae45d-128">Operación DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="ae45d-128">DeleteFolder operation</span></span>](http://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> |
   
## <a name="core-concepts-to-know-for-working-with-search-folders"></a><span data-ttu-id="ae45d-129">Conceptos básicos necesarios para trabajar con las carpetas de búsqueda</span><span class="sxs-lookup"><span data-stu-id="ae45d-129">Core concepts to know for working with search folders</span></span>
<span data-ttu-id="ae45d-130"><a name="bk_CoreConcepts"> </a></span><span class="sxs-lookup"><span data-stu-id="ae45d-130"></span></span>

<span data-ttu-id="ae45d-131">Antes de comenzar a trabajar con las carpetas de búsqueda, desea estar familiarizado con el funcionamiento de los filtros de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ae45d-131">Before you start working with search folders, you'll want to be familiar with how search filters work.</span></span> <span data-ttu-id="ae45d-132">Las carpetas de búsqueda se basan en filtros de búsqueda para expresar sus criterios.</span><span class="sxs-lookup"><span data-stu-id="ae45d-132">Search folders rely on search filters to express their criteria.</span></span> <span data-ttu-id="ae45d-133">Filtros de búsqueda de las carpetas de búsqueda se construyen a partir de la misma forma en que se construyen ese [filtros de búsqueda para las operaciones de búsqueda](how-to-use-search-filters-with-ews-in-exchange.md) .</span><span class="sxs-lookup"><span data-stu-id="ae45d-133">Search filters for search folders are constructed in the same way that [search filters for search operations](how-to-use-search-filters-with-ews-in-exchange.md) are constructed.</span></span> 
  
## <a name="create-a-search-folder-by-using-the-ews-managed-api"></a><span data-ttu-id="ae45d-134">Crear una carpeta de búsqueda mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="ae45d-134">Create a search folder by using the EWS Managed API</span></span>
<span data-ttu-id="ae45d-135"><a name="bk_CreateEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="ae45d-135"></span></span>

<span data-ttu-id="ae45d-136">Básicamente, cree una carpeta de búsqueda con la API administrada de EWS de la misma manera que se crea una carpeta normal.</span><span class="sxs-lookup"><span data-stu-id="ae45d-136">Basically, you create a search folder using the EWS Managed API in the same way that you create a regular folder.</span></span> <span data-ttu-id="ae45d-137">Sin embargo, en lugar de usar la [clase de carpeta](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder%28v=exchg.80%29.aspx), utilice la [clase SearchFolder](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfolder%28v=exchg.80%29.aspx)y establezca la [propiedad SearchParameters](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfolder.searchparameters%28v=exchg.80%29.aspx) para configurar los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ae45d-137">However, instead of using the [Folder class](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder%28v=exchg.80%29.aspx), you use the [SearchFolder class](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfolder%28v=exchg.80%29.aspx), and set the [SearchParameters property](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfolder.searchparameters%28v=exchg.80%29.aspx) to configure the search criteria.</span></span> 
  
<span data-ttu-id="ae45d-138">En el siguiente ejemplo, se crea una carpeta de búsqueda para buscar todos los mensajes en la Bandeja de entrada y sus subcarpetas que se han enviado por el administrador del usuario, sadie@contoso.com.</span><span class="sxs-lookup"><span data-stu-id="ae45d-138">In the following example, a search folder is created to find all messages in the Inbox and its subfolders that were sent by the user's manager, sadie@contoso.com.</span></span> <span data-ttu-id="ae45d-139">La carpeta se crea como un elemento secundario de la carpeta de las carpetas de búsqueda en el buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="ae45d-139">The folder is created as a child of the Search Folders folder in the user's mailbox.</span></span>
  
> [!NOTE]
> <span data-ttu-id="ae45d-140">Puede crear una carpeta de búsqueda como un elemento secundario de cualquier carpeta en el buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="ae45d-140">You can create a search folder as a child of any folder in the user's mailbox.</span></span> <span data-ttu-id="ae45d-141">Sin embargo, si desea que la carpeta recién creada para mostrar la copia de seguridad en las carpetas de búsqueda en Outlook, crearla bajo la carpeta conocida de las carpetas de búsqueda, utilizando el valor de **SearchFolders** de la [enumeración WellKnownFolderName](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="ae45d-141">However, if you want the newly created folder to show up under Search Folders in Outlook, create it under the Search Folders well-known folder, using the **SearchFolders** value of the [WellKnownFolderName enumeration](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx).</span></span> 
  
<span data-ttu-id="ae45d-142">En este ejemplo se da por supuesto que se ha inicializado el objeto **ExchangeService** con valores válidos en las propiedades de [las credenciales](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) y [dirección Url](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="ae45d-142">This example assumes that the **ExchangeService** object has been initialized with valid values in the [Credentials](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) and [Url](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) properties.</span></span> 
  
```cs
using Microsoft.Exchange.WebServices.Data;
static void CreateSearchFolder(ExchangeService service)
{
    // Create the folder.
    SearchFolder searchFolder = new SearchFolder(service);
    searchFolder.DisplayName = "From Manager";
    // Create a search filter to express the criteria
    // for the folder.
    EmailAddress manager = new EmailAddress("sadie@contoso.com");
    SearchFilter.IsEqualTo fromManagerFilter =
        new SearchFilter.IsEqualTo(EmailMessageSchema.Sender, manager);
    // Set the search filter.
    searchFolder.SearchParameters.SearchFilter = fromManagerFilter;
    // Set the folder to search.
    searchFolder.SearchParameters.RootFolderIds.Add(WellKnownFolderName.Inbox);
    // Set the search traversal. Deep will search all subfolders.
    searchFolder.SearchParameters.Traversal = SearchFolderTraversal.Deep;
    // Call Save to make the EWS call to create the folder.
    searchFolder.Save(WellKnownFolderName.SearchFolders);
}
```

## <a name="create-a-search-folder-by-using-ews"></a><span data-ttu-id="ae45d-143">Crear una carpeta de búsqueda mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="ae45d-143">Create a search folder by using EWS</span></span>
<span data-ttu-id="ae45d-144"><a name="bk_CreateEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="ae45d-144"></span></span>

<span data-ttu-id="ae45d-145">Si usa EWS, use la [operación CreateFolder](http://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) con un elemento [SearchFolder](http://msdn.microsoft.com/library/1a7d408b-2e98-4391-8834-085ed6d5757c%28Office.15%29.aspx) para crear una carpeta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ae45d-145">If you are using EWS, use the [CreateFolder operation](http://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) with a [SearchFolder](http://msdn.microsoft.com/library/1a7d408b-2e98-4391-8834-085ed6d5757c%28Office.15%29.aspx) element to create a search folder.</span></span> <span data-ttu-id="ae45d-146">En el siguiente ejemplo de solicitud, se crea una carpeta de búsqueda para buscar todos los mensajes en la Bandeja de entrada y sus subcarpetas que se han enviado por el administrador del usuario, sadie@contoso.com.</span><span class="sxs-lookup"><span data-stu-id="ae45d-146">In the following request example, a search folder is created to find all messages in the Inbox and its subfolders that were sent by the user's manager, sadie@contoso.com.</span></span> <span data-ttu-id="ae45d-147">La carpeta se crea en la carpeta de las carpetas de búsqueda en el buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="ae45d-147">The folder is created in the Search Folders folder in the user's mailbox.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ae45d-148">Puede crear una carpeta de búsqueda como un elemento secundario de cualquier carpeta en el buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="ae45d-148">You can create a search folder as a child of any folder in the user's mailbox.</span></span> <span data-ttu-id="ae45d-149">Sin embargo, si desea que la carpeta recién creada para mostrar la copia de seguridad en las carpetas de búsqueda en Outlook, crearla bajo la carpeta conocida de las carpetas de búsqueda, utilizando el valor de **searchfolders** en el atributo **Id** del elemento [DistinguishedFolderId](http://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="ae45d-149">However, if you want the newly created folder to show up under Search Folders in Outlook, create it under the Search Folders well-known folder, using the **searchfolders** value in the **Id** attribute of the [DistinguishedFolderId](http://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) element.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Eastern Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:CreateFolder>
      <m:ParentFolderId>
        <t:DistinguishedFolderId Id="searchfolders" />
      </m:ParentFolderId>
      <m:Folders>
        <t:SearchFolder>
          <t:DisplayName>From Manager</t:DisplayName>
          <t:SearchParameters Traversal="Deep">
            <t:Restriction>
              <t:IsEqualTo>
                <t:FieldURI FieldURI="message:Sender" />
                <t:FieldURIOrConstant>
                  <t:Constant Value="sadie@contoso.com" />
                </t:FieldURIOrConstant>
              </t:IsEqualTo>
            </t:Restriction>
            <t:BaseFolderIds>
              <t:DistinguishedFolderId Id="inbox" />
            </t:BaseFolderIds>
          </t:SearchParameters>
        </t:SearchFolder>
      </m:Folders>
    </m:CreateFolder>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="ae45d-150">El servidor responde con un mensaje de [CreateFolderResponse](http://msdn.microsoft.com/library/158adecc-491a-47d9-af73-acc2cd3f8566%28Office.15%29.aspx) que incluye un valor [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, lo que indica el éxito.</span><span class="sxs-lookup"><span data-stu-id="ae45d-150">The server responds with a [CreateFolderResponse](http://msdn.microsoft.com/library/158adecc-491a-47d9-af73-acc2cd3f8566%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError**, which indicates success.</span></span>
  
## <a name="get-a-search-folder-by-using-the-ews-managed-api"></a><span data-ttu-id="ae45d-151">Obtener una carpeta de búsqueda mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="ae45d-151">Get a search folder by using the EWS Managed API</span></span>
<span data-ttu-id="ae45d-152"><a name="bk_RetrieveEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="ae45d-152"></span></span>

<span data-ttu-id="ae45d-153">Use el método de la API administrada de EWS [ExchangeService.FindFolders](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx) para buscar las carpetas de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ae45d-153">Use the [ExchangeService.FindFolders](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx) EWS Managed API method to find search folders.</span></span> <span data-ttu-id="ae45d-154">Sin embargo, tenga en cuenta que no se puede limitar los resultados para que incluya sólo las carpetas de búsqueda; desea tenga en cuenta al procesar los resultados.</span><span class="sxs-lookup"><span data-stu-id="ae45d-154">Note, however, that you can't limit your results to only include search folders; you'll want to keep that in mind when you process the results.</span></span> <span data-ttu-id="ae45d-155">Use el método [SearchFolder.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfolder.bind%28v=exchg.80%29.aspx) para obtener las carpetas de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ae45d-155">Use the [SearchFolder.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfolder.bind%28v=exchg.80%29.aspx) method to get search folders.</span></span> 
  
<span data-ttu-id="ae45d-156">En el ejemplo siguiente se buscan las 10 primeros carpetas en la carpeta de las carpetas de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ae45d-156">The following example finds the first 10 folders in the Search Folders folder.</span></span> <span data-ttu-id="ae45d-157">Comprueba para determinar si cada uno de ellos es una carpeta de búsqueda y, si, por lo tanto, se obtiene la carpeta de búsqueda y se muestra el número de carpetas de destino que busca.</span><span class="sxs-lookup"><span data-stu-id="ae45d-157">It checks to determine whether each one is a search folder, and if so, it gets the search folder and displays how many target folders it searches.</span></span>
  
```cs
using Microsoft.Exchange.WebServices.Data;
static void GetSearchFolders(ExchangeService service)
{
    FolderView folderView = new FolderView(10);
    folderView.PropertySet = new PropertySet(FolderSchema.DisplayName);
    try
    {
        FindFoldersResults findResults = service.FindFolders(WellKnownFolderName.SearchFolders, folderView);
        foreach (Folder folder in findResults.Folders)
        {
            // You can't request only search folders in 
            // a FindFolders request, so other search folders might also be present.
            if (folder is SearchFolder)
            {
                Console.WriteLine("{0} is a search folder.", folder.DisplayName);
                // In order to access the SearchParameters property,
                // you have to bind to the folder. SearchParameters are not
                // returned in FindFolders results.
                SearchFolder searchFolder = SearchFolder.Bind(service, folder.Id);
                Console.WriteLine("Number of folders searched: {0}.",
                    searchFolder.SearchParameters.RootFolderIds.Count);
            }
            else
            {
                Console.WriteLine("{0} is NOT a search folder.", folder.DisplayName);
            }
        }
    }
    catch (Exception ex)
    {
        Console.WriteLine("Exception while enumerating results: {0}", ex.Message);
    }
}
```

## <a name="get-a-search-folder-by-using-ews"></a><span data-ttu-id="ae45d-158">Obtener una carpeta de búsqueda mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="ae45d-158">Get a search folder by using EWS</span></span>
<span data-ttu-id="ae45d-159"><a name="bk_RetrieveEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="ae45d-159"></span></span>

<span data-ttu-id="ae45d-160">Si está usando EWS, use la [operación FindFolder](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) para buscar las carpetas de búsqueda y la [operación GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) para obtener las carpetas de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ae45d-160">If you're using EWS, use the [FindFolder operation](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) to find search folders, and the [GetFolder operation](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) to get search folders.</span></span> <span data-ttu-id="ae45d-161">Una respuesta correcta de **GetFolder** para una carpeta de búsqueda va a contener un elemento [SearchFolder](http://msdn.microsoft.com/library/1a7d408b-2e98-4391-8834-085ed6d5757c%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="ae45d-161">A successful **GetFolder** response for a search folder will contain a [SearchFolder](http://msdn.microsoft.com/library/1a7d408b-2e98-4391-8834-085ed6d5757c%28Office.15%29.aspx) element.</span></span> <span data-ttu-id="ae45d-162">En el ejemplo de solicitud siguiente se busca las 10 primeros carpetas en la carpeta de las carpetas de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ae45d-162">The following request example finds the first 10 folders in the Search Folders folder.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Eastern Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:FindFolder Traversal="Shallow">
      <m:FolderShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="folder:DisplayName" />
        </t:AdditionalProperties>
      </m:FolderShape>
      <m:IndexedPageFolderView MaxEntriesReturned="10" Offset="0" BasePoint="Beginning" />
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="searchfolders" />
      </m:ParentFolderIds>
    </m:FindFolder>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="ae45d-163">El servidor devuelve la respuesta siguiente, que muestra una carpeta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ae45d-163">The server returns the following response, which shows one search folder.</span></span>
  
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
    <m:FindFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="3" TotalItemsInView="3" IncludesLastItemInRange="true">
            <t:Folders>
              <t:SearchFolder>
                <t:FolderId Id="AAMkAGM2..." ChangeKey="CAAAABYA..." />
                <t:DisplayName>From Manager</t:DisplayName>
              </t:SearchFolder>
            </t:Folders>
          </m:RootFolder>
        </m:FindFolderResponseMessage>
      </m:ResponseMessages>
    </m:FindFolderResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="ae45d-164">El siguiente ejemplo de una solicitud usa el valor del elemento [FolderId](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) desde la respuesta anterior en una solicitud de operación **GetFolder** para obtener la carpeta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ae45d-164">The following example of a request uses the value of the [FolderId](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) element from the previous response in a **GetFolder** operation request to get the search folder.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Eastern Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:GetFolder>
      <m:FolderShape>
        <t:BaseShape>AllProperties</t:BaseShape>
      </m:FolderShape>
      <m:FolderIds>
        <t:FolderId Id="AAMkAGM2..." ChangeKey="CAAAABYA..." />
      </m:FolderIds>
    </m:GetFolder>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="ae45d-165">El servidor devuelve la respuesta siguiente con todas las propiedades de primera clase para la carpeta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ae45d-165">The server returns the following response with all the first-class properties for the search folder.</span></span>
  
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
    <m:GetFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:SearchFolder>
              <t:FolderId Id="AAMkAGM2..." ChangeKey="CAAAABYA..." />
              <t:ParentFolderId Id="AQMkAGM2..." ChangeKey="AQAAAA==" />
              <t:FolderClass>IPF.Note</t:FolderClass>
              <t:DisplayName>From Manager</t:DisplayName>
              <t:TotalCount>8</t:TotalCount>
              <t:ChildFolderCount>0</t:ChildFolderCount>
              <t:EffectiveRights>
                <t:CreateAssociated>true</t:CreateAssociated>
                <t:CreateContents>true</t:CreateContents>
                <t:CreateHierarchy>true</t:CreateHierarchy>
                <t:Delete>true</t:Delete>
                <t:Modify>true</t:Modify>
                <t:Read>true</t:Read>
                <t:ViewPrivateItems>true</t:ViewPrivateItems>
              </t:EffectiveRights>
              <t:UnreadCount>0</t:UnreadCount>
              <t:SearchParameters Traversal="Deep">
                <t:Restriction>
                  <t:IsEqualTo>
                    <t:FieldURI FieldURI="message:Sender" />
                    <t:FieldURIOrConstant>
                      <t:Constant Value="/o=First Organization/ou=Exchange Administrative Group (FYDIBOHF23SPDLT)/cn=Recipients/cn=8d84a3f4cbb34d48838a3aecf99795c0-Sadie" />
                    </t:FieldURIOrConstant>
                  </t:IsEqualTo>
                </t:Restriction>
                <t:BaseFolderIds>
                  <t:FolderId Id="AQMkAGM2..." ChangeKey="AQAAAA==" />
                </t:BaseFolderIds>
              </t:SearchParameters>
            </t:SearchFolder>
          </m:Folders>
        </m:GetFolderResponseMessage>
      </m:ResponseMessages>
    </m:GetFolderResponse>
  </s:Body>
</s:Envelope>
```

## <a name="update-a-search-folder-by-using-the-ews-managed-api"></a><span data-ttu-id="ae45d-166">Actualización de una carpeta de búsqueda mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="ae45d-166">Update a search folder by using the EWS Managed API</span></span>
<span data-ttu-id="ae45d-167"><a name="bk_UpdateEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="ae45d-167"></span></span>

<span data-ttu-id="ae45d-168">Use el método de la API administrada de EWS [Folder.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) en un objeto **SearchFolder** para actualizar una carpeta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ae45d-168">Use the [Folder.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) EWS Managed API method on a **SearchFolder** object to update a search folder.</span></span> <span data-ttu-id="ae45d-169">El siguiente ejemplo actualiza los criterios de búsqueda en una carpeta de búsqueda con el nombre para mostrar "Desde el administrador".</span><span class="sxs-lookup"><span data-stu-id="ae45d-169">The following example updates the search criteria on a search folder with the display name "From Manager".</span></span> 
  
```cs
using Microsoft.Exchange.WebServices.Data;
static void UpdateSearchFolder(ExchangeService service)
{
    FolderView folderView = new FolderView(10);
    folderView.PropertySet = new PropertySet(FolderSchema.DisplayName);
    try
    {
        FindFoldersResults findResults = service.FindFolders(WellKnownFolderName.SearchFolders, folderView);
        foreach (Folder folder in findResults.Folders)
        {
            // You cannot request only search folders in 
            // a FindFolders request, so other search folders might also be present.
            if (folder is SearchFolder &amp;&amp; folder.DisplayName.Equals("From Manager"))
            {
                Console.WriteLine("\"{0}\" folder found.", folder.DisplayName);
                SearchFolder searchFolder = folder as SearchFolder;
                EmailAddress newManager = new EmailAddress("hope@contoso.com");
                SearchFilter.IsEqualTo newManagerFilter =
                    new SearchFilter.IsEqualTo(EmailMessageSchema.Sender, newManager);
                searchFolder.SearchParameters.SearchFilter = newManagerFilter;
                searchFolder.SearchParameters.RootFolderIds.Add(WellKnownFolderName.Inbox);
                searchFolder.SearchParameters.Traversal = SearchFolderTraversal.Deep;
                searchFolder.Update();
                Console.WriteLine("\"{0}\" folder updated.", folder.DisplayName);
            }
        }
    }
    catch (Exception ex)
    {
        Console.WriteLine("Exception while enumerating results: {0}", ex.Message);
    }
}
```

## <a name="update-a-search-folder-by-using-ews"></a><span data-ttu-id="ae45d-170">Actualización de una carpeta de búsqueda mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="ae45d-170">Update a search folder by using EWS</span></span>
<span data-ttu-id="ae45d-171"><a name="bk_UpdateEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="ae45d-171"></span></span>

<span data-ttu-id="ae45d-172">Si está usando EWS, use la [operación UpdateFolder](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) con un elemento [SearchFolder](http://msdn.microsoft.com/library/1a7d408b-2e98-4391-8834-085ed6d5757c%28Office.15%29.aspx) para actualizar una carpeta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ae45d-172">If you're using EWS, use the [UpdateFolder operation](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) with a [SearchFolder](http://msdn.microsoft.com/library/1a7d408b-2e98-4391-8834-085ed6d5757c%28Office.15%29.aspx) element to update a search folder.</span></span> <span data-ttu-id="ae45d-173">El siguiente ejemplo de solicitud actualiza los criterios de búsqueda en la carpeta de búsqueda "Desde el administrador".</span><span class="sxs-lookup"><span data-stu-id="ae45d-173">The following request example updates the search criteria on the "From Manager" search folder.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Eastern Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:UpdateFolder>
      <m:FolderChanges>
        <t:FolderChange>
          <t:FolderId Id="AAMkAGM2..." ChangeKey="CAAAABYA..." />
          <t:Updates>
            <t:SetFolderField>
              <t:FieldURI FieldURI="folder:SearchParameters" />
              <t:SearchFolder>
                <t:SearchParameters Traversal="Deep">
                  <t:Restriction>
                    <t:IsEqualTo>
                      <t:FieldURI FieldURI="message:Sender" />
                      <t:FieldURIOrConstant>
                        <t:Constant Value="hope@contoso.com" />
                      </t:FieldURIOrConstant>
                    </t:IsEqualTo>
                  </t:Restriction>
                  <t:BaseFolderIds>
                    <t:DistinguishedFolderId Id="inbox" />
                  </t:BaseFolderIds>
                </t:SearchParameters>
              </t:SearchFolder>
            </t:SetFolderField>
          </t:Updates>
        </t:FolderChange>
      </m:FolderChanges>
    </m:UpdateFolder>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="ae45d-174">El servidor responde con un mensaje de [UpdateFolderResponse](http://msdn.microsoft.com/library/31f47739-dc9c-46ba-9e3f-cce25dc85e6e%28Office.15%29.aspx) que incluye un valor [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, lo que indica el éxito.</span><span class="sxs-lookup"><span data-stu-id="ae45d-174">The server responds with an [UpdateFolderResponse](http://msdn.microsoft.com/library/31f47739-dc9c-46ba-9e3f-cce25dc85e6e%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError**, which indicates success.</span></span>
  
## <a name="delete-a-search-folder-by-using-the-ews-managed-api"></a><span data-ttu-id="ae45d-175">Eliminar una carpeta de búsqueda mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="ae45d-175">Delete a search folder by using the EWS Managed API</span></span>
<span data-ttu-id="ae45d-176"><a name="bk_DeleteEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="ae45d-176"></span></span>

<span data-ttu-id="ae45d-177">Use el método de la API administrada de EWS [Folder.Delete](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.delete%28v=exchg.80%29.aspx) en un objeto **SearchFolder** para eliminar una carpeta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ae45d-177">Use the [Folder.Delete](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.delete%28v=exchg.80%29.aspx) EWS Managed API method on a **SearchFolder** object to delete a search folder.</span></span> <span data-ttu-id="ae45d-178">En el ejemplo siguiente se elimina una carpeta de búsqueda con el nombre para mostrar "Desde el administrador".</span><span class="sxs-lookup"><span data-stu-id="ae45d-178">The following example deletes a search folder with the display name "From Manager".</span></span> <span data-ttu-id="ae45d-179">La carpeta de búsqueda eliminada se mueve a la carpeta Elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="ae45d-179">The deleted search folder is moved to the Deleted Items folder.</span></span> 
  
```cs
using Microsoft.Exchange.WebServices.Data;
static void DeleteSearchFolder(ExchangeService service)
{
    FolderView folderView = new FolderView(10);
    folderView.PropertySet = new PropertySet(FolderSchema.DisplayName);
    try
    {
        FindFoldersResults findResults = service.FindFolders(WellKnownFolderName.SearchFolders, folderView);
        foreach (Folder folder in findResults.Folders)
        {
            // You cannot request only search folders in 
            // a FindFolders request, so other folders might also be present.
            if (folder is SearchFolder &amp;&amp; folder.DisplayName.Equals("From Manager"))
            {
                Console.WriteLine("\"{0}\" folder found.", folder.DisplayName);
                folder.Delete(DeleteMode.MoveToDeletedItems);
                Console.WriteLine("\"{0}\" folder deleted.", folder.DisplayName);
            }
        }
    }
    catch (Exception ex)
    {
        Console.WriteLine("Exception while enumerating results: {0}", ex.Message);
    }
}
```

## <a name="delete-a-search-folder-by-using-ews"></a><span data-ttu-id="ae45d-180">Eliminar una carpeta de búsqueda mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="ae45d-180">Delete a search folder by using EWS</span></span>
<span data-ttu-id="ae45d-181"><a name="bk_DeleteEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="ae45d-181"></span></span>

<span data-ttu-id="ae45d-182">Si está usando EWS, use la [operación DeleteFolder](http://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) para eliminar una carpeta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ae45d-182">If you're using EWS, use the [DeleteFolder operation](http://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) to delete a search folder.</span></span> <span data-ttu-id="ae45d-183">En el ejemplo siguiente se elimina una carpeta de búsqueda y lo mueve a la carpeta Elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="ae45d-183">The following example deletes a search folder and moves it to the Deleted Items folder.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Eastern Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:DeleteFolder DeleteType="MoveToDeletedItems">
      <m:FolderIds>
        <t:FolderId Id="AAMkAGM2..." ChangeKey="CAAAABYA..." />
      </m:FolderIds>
    </m:DeleteFolder>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="ae45d-184">El servidor responde con un mensaje de [DeleteFolderResponse](http://msdn.microsoft.com/library/27578bda-ef0a-4a33-bccc-2c1bc1735424%28Office.15%29.aspx) que incluye un valor [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, lo que indica el éxito.</span><span class="sxs-lookup"><span data-stu-id="ae45d-184">The server responds with a [DeleteFolderResponse](http://msdn.microsoft.com/library/27578bda-ef0a-4a33-bccc-2c1bc1735424%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError**, which indicates success.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ae45d-185">Vea también</span><span class="sxs-lookup"><span data-stu-id="ae45d-185">See also</span></span>


- [<span data-ttu-id="ae45d-186">Búsqueda y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="ae45d-186">Search and EWS in Exchange</span></span>](search-and-ews-in-exchange.md)
    
- [<span data-ttu-id="ae45d-187">Use los filtros de búsqueda con EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="ae45d-187">Use search filters with EWS in Exchange</span></span>](how-to-use-search-filters-with-ews-in-exchange.md)
    
- [<span data-ttu-id="ae45d-188">Clase SearchFolder</span><span class="sxs-lookup"><span data-stu-id="ae45d-188">SearchFolder class</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfolder%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="ae45d-189">Operación CreateFolder</span><span class="sxs-lookup"><span data-stu-id="ae45d-189">CreateFolder operation</span></span>](http://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx)
    
- [<span data-ttu-id="ae45d-190">Operación FindFolder</span><span class="sxs-lookup"><span data-stu-id="ae45d-190">FindFolder operation</span></span>](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)
    
- [<span data-ttu-id="ae45d-191">Operación GetFolder</span><span class="sxs-lookup"><span data-stu-id="ae45d-191">GetFolder operation</span></span>](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx)
    
- [<span data-ttu-id="ae45d-192">Operación UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="ae45d-192">UpdateFolder operation</span></span>](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx)
    
- [<span data-ttu-id="ae45d-193">Operación DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="ae45d-193">DeleteFolder operation</span></span>](http://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx)
    

