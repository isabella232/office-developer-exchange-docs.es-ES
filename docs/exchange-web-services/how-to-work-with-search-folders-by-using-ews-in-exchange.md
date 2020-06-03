---
title: Trabajar con carpetas de búsqueda mediante EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: abe703c5-6d85-46d9-bf20-230c34782a9f
description: Descubra cómo crear, obtener, actualizar y eliminar carpetas de búsqueda mediante la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: 880c14bc99c4f6c674d4f7566036c4b8f5f19e55
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456370"
---
# <a name="work-with-search-folders-by-using-ews-in-exchange"></a><span data-ttu-id="ff0b5-103">Trabajar con carpetas de búsqueda mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="ff0b5-103">Work with search folders by using EWS in Exchange</span></span>

<span data-ttu-id="ff0b5-104">Descubra cómo crear, obtener, actualizar y eliminar carpetas de búsqueda mediante la API administrada de EWS o EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="ff0b5-104">Find out how to create, get, update, and delete search folders by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="ff0b5-105">Una carpeta de búsqueda representa una búsqueda persistente "siempre activa" en el buzón de un usuario.</span><span class="sxs-lookup"><span data-stu-id="ff0b5-105">A search folder represents a persistent "always-on" search in a user's mailbox.</span></span> <span data-ttu-id="ff0b5-106">Una carpeta de búsqueda tiene el mismo aspecto y actúa como una carpeta de buzón normal.</span><span class="sxs-lookup"><span data-stu-id="ff0b5-106">A search folder looks and acts like a regular mailbox folder.</span></span> <span data-ttu-id="ff0b5-107">Sin embargo, en lugar de contener elementos, contiene una copia "virtual" de los elementos de las carpetas del ámbito de búsqueda que coinciden con los criterios de búsqueda establecidos en la carpeta.</span><span class="sxs-lookup"><span data-stu-id="ff0b5-107">However, instead of containing items, it contains a "virtual" copy of items from any folders in its search scope that match the search criteria set on the folder.</span></span> <span data-ttu-id="ff0b5-108">Tanto las aplicaciones como los usuarios finales pueden usar las carpetas de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ff0b5-108">Both applications and end-users can use search folders.</span></span> <span data-ttu-id="ff0b5-109">¿Necesita la aplicación realizar la misma búsqueda una y otra vez?</span><span class="sxs-lookup"><span data-stu-id="ff0b5-109">Does your application need to perform the same search over and over?</span></span> <span data-ttu-id="ff0b5-110">Las carpetas de búsqueda son una gran herramienta para esta tarea.</span><span class="sxs-lookup"><span data-stu-id="ff0b5-110">Search folders are a great tool for this task.</span></span> <span data-ttu-id="ff0b5-111">O quizá solo quiera proporcionar a los usuarios la capacidad de tener acceso y administrar las carpetas de búsqueda en el cliente.</span><span class="sxs-lookup"><span data-stu-id="ff0b5-111">Or maybe you just want to give your users the ability to access and manage search folders in your client.</span></span> <span data-ttu-id="ff0b5-112">Independientemente del escenario, la API administrada de EWS y EWS permiten que la aplicación interactúe completamente con las carpetas de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ff0b5-112">Whatever your scenario, the EWS Managed API and EWS enable your application to fully interact with search folders.</span></span>

> [!NOTE] 
> <span data-ttu-id="ff0b5-113">Este artículo solo se aplica al usar Outlook en modo en línea.</span><span class="sxs-lookup"><span data-stu-id="ff0b5-113">This article applies only when using Outlook in online mode.</span></span> <span data-ttu-id="ff0b5-114">Las carpetas de búsqueda no se sincronizan; por lo tanto, las carpetas de búsqueda creadas en modo en línea no aparecerán en el modo en caché.</span><span class="sxs-lookup"><span data-stu-id="ff0b5-114">Search folders do not sync; therefore, search folders created in online mode will not appear in cached mode.</span></span>
  
<span data-ttu-id="ff0b5-115">**Tabla 1. Métodos de API administrada de EWS y operaciones de EWS para trabajar con carpetas de búsqueda**</span><span class="sxs-lookup"><span data-stu-id="ff0b5-115">**Table 1. EWS Managed API methods and EWS operations for working with search folders**</span></span>

|<span data-ttu-id="ff0b5-116">Si quiere...</span><span class="sxs-lookup"><span data-stu-id="ff0b5-116">If you want to…</span></span>|<span data-ttu-id="ff0b5-117">En la API administrada de EWS, use...</span><span class="sxs-lookup"><span data-stu-id="ff0b5-117">In the EWS Managed API, use…</span></span>|<span data-ttu-id="ff0b5-118">En EWS, use...</span><span class="sxs-lookup"><span data-stu-id="ff0b5-118">In EWS, use…</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ff0b5-119">Crear una carpeta de búsqueda</span><span class="sxs-lookup"><span data-stu-id="ff0b5-119">Create a search folder</span></span>  <br/> |[<span data-ttu-id="ff0b5-120">SearchFolder. Save</span><span class="sxs-lookup"><span data-stu-id="ff0b5-120">SearchFolder.Save</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfolder.save%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="ff0b5-121">Operación CreateFolder</span><span class="sxs-lookup"><span data-stu-id="ff0b5-121">CreateFolder operation</span></span>](https://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="ff0b5-122">Obtener una carpeta de búsqueda</span><span class="sxs-lookup"><span data-stu-id="ff0b5-122">Get a search folder</span></span>  <br/> |[<span data-ttu-id="ff0b5-123">SearchFolder. bind</span><span class="sxs-lookup"><span data-stu-id="ff0b5-123">SearchFolder.Bind</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfolder.bind%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="ff0b5-124">Operación GetFolder</span><span class="sxs-lookup"><span data-stu-id="ff0b5-124">GetFolder operation</span></span>](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="ff0b5-125">Actualizar una carpeta de búsqueda</span><span class="sxs-lookup"><span data-stu-id="ff0b5-125">Update a search folder</span></span>  <br/> |[<span data-ttu-id="ff0b5-126">SearchFolder. Update</span><span class="sxs-lookup"><span data-stu-id="ff0b5-126">SearchFolder.Update</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="ff0b5-127">Operación UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="ff0b5-127">UpdateFolder operation</span></span>](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="ff0b5-128">Eliminar una carpeta de búsqueda</span><span class="sxs-lookup"><span data-stu-id="ff0b5-128">Delete a search folder</span></span>  <br/> |[<span data-ttu-id="ff0b5-129">SearchFolder. Delete</span><span class="sxs-lookup"><span data-stu-id="ff0b5-129">SearchFolder.Delete</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.delete%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="ff0b5-130">Operación DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="ff0b5-130">DeleteFolder operation</span></span>](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> |
   
## <a name="core-concepts-to-know-for-working-with-search-folders"></a><span data-ttu-id="ff0b5-131">Conceptos básicos que debe conocer para trabajar con carpetas de búsqueda</span><span class="sxs-lookup"><span data-stu-id="ff0b5-131">Core concepts to know for working with search folders</span></span>
<span data-ttu-id="ff0b5-132"><a name="bk_CoreConcepts"> </a></span><span class="sxs-lookup"><span data-stu-id="ff0b5-132"><a name="bk_CoreConcepts"> </a></span></span>

<span data-ttu-id="ff0b5-133">Antes de empezar a trabajar con carpetas de búsqueda, querrá estar familiarizado con el funcionamiento de los filtros de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ff0b5-133">Before you start working with search folders, you'll want to be familiar with how search filters work.</span></span> <span data-ttu-id="ff0b5-134">Las carpetas de búsqueda dependen de filtros de búsqueda para expresar sus criterios.</span><span class="sxs-lookup"><span data-stu-id="ff0b5-134">Search folders rely on search filters to express their criteria.</span></span> <span data-ttu-id="ff0b5-135">Los filtros de búsqueda para las carpetas de búsqueda se crean de la misma forma que se crean los [filtros de búsqueda para las operaciones de búsqueda](how-to-use-search-filters-with-ews-in-exchange.md) .</span><span class="sxs-lookup"><span data-stu-id="ff0b5-135">Search filters for search folders are constructed in the same way that [search filters for search operations](how-to-use-search-filters-with-ews-in-exchange.md) are constructed.</span></span> 
  
## <a name="create-a-search-folder-by-using-the-ews-managed-api"></a><span data-ttu-id="ff0b5-136">Crear una carpeta de búsqueda mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="ff0b5-136">Create a search folder by using the EWS Managed API</span></span>
<span data-ttu-id="ff0b5-137"><a name="bk_CreateEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="ff0b5-137"><a name="bk_CreateEWSMA"> </a></span></span>

<span data-ttu-id="ff0b5-138">Básicamente, se crea una carpeta de búsqueda mediante la API administrada de EWS del mismo modo que se crea una carpeta normal.</span><span class="sxs-lookup"><span data-stu-id="ff0b5-138">Basically, you create a search folder using the EWS Managed API in the same way that you create a regular folder.</span></span> <span data-ttu-id="ff0b5-139">Sin embargo, en lugar de usar la [clase Folder](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder%28v=exchg.80%29.aspx), use la [clase SearchFolder](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfolder%28v=exchg.80%29.aspx)y establezca la [propiedad SearchParameters](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfolder.searchparameters%28v=exchg.80%29.aspx) para configurar los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ff0b5-139">However, instead of using the [Folder class](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder%28v=exchg.80%29.aspx), you use the [SearchFolder class](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfolder%28v=exchg.80%29.aspx), and set the [SearchParameters property](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfolder.searchparameters%28v=exchg.80%29.aspx) to configure the search criteria.</span></span> 
  
<span data-ttu-id="ff0b5-140">En el siguiente ejemplo, se crea una carpeta de búsqueda para buscar todos los mensajes de la bandeja de entrada y sus subcarpetas enviadas por el administrador del usuario, sadie@contoso.com.</span><span class="sxs-lookup"><span data-stu-id="ff0b5-140">In the following example, a search folder is created to find all messages in the Inbox and its subfolders that were sent by the user's manager, sadie@contoso.com.</span></span> <span data-ttu-id="ff0b5-141">La carpeta se crea como un elemento secundario de la carpeta carpetas de búsqueda en el buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="ff0b5-141">The folder is created as a child of the Search Folders folder in the user's mailbox.</span></span>
  
> [!NOTE]
> <span data-ttu-id="ff0b5-142">Puede crear una carpeta de búsqueda como elemento secundario de cualquier carpeta en el buzón de correo del usuario.</span><span class="sxs-lookup"><span data-stu-id="ff0b5-142">You can create a search folder as a child of any folder in the user's mailbox.</span></span> <span data-ttu-id="ff0b5-143">Sin embargo, si desea que la carpeta recién creada aparezca en las carpetas de búsqueda de Outlook, créela en carpeta de búsqueda de carpetas conocidas mediante el valor **SearchFolders** de la [enumeración WellKnownFolderName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="ff0b5-143">However, if you want the newly created folder to show up under Search Folders in Outlook, create it under the Search Folders well-known folder, using the **SearchFolders** value of the [WellKnownFolderName enumeration](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx).</span></span> 
  
<span data-ttu-id="ff0b5-144">En este ejemplo se supone que el objeto **ExchangeService** se ha inicializado con valores válidos en las propiedades [Credentials](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) y [URL](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="ff0b5-144">This example assumes that the **ExchangeService** object has been initialized with valid values in the [Credentials](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) and [Url](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) properties.</span></span> 
  
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

## <a name="create-a-search-folder-by-using-ews"></a><span data-ttu-id="ff0b5-145">Crear una carpeta de búsqueda con EWS</span><span class="sxs-lookup"><span data-stu-id="ff0b5-145">Create a search folder by using EWS</span></span>
<span data-ttu-id="ff0b5-146"><a name="bk_CreateEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="ff0b5-146"><a name="bk_CreateEWS"> </a></span></span>

<span data-ttu-id="ff0b5-147">Si usa EWS, use la [operación CreateFolder](https://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) con un elemento [SearchFolder](https://msdn.microsoft.com/library/1a7d408b-2e98-4391-8834-085ed6d5757c%28Office.15%29.aspx) para crear una carpeta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ff0b5-147">If you are using EWS, use the [CreateFolder operation](https://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) with a [SearchFolder](https://msdn.microsoft.com/library/1a7d408b-2e98-4391-8834-085ed6d5757c%28Office.15%29.aspx) element to create a search folder.</span></span> <span data-ttu-id="ff0b5-148">En el siguiente ejemplo de solicitud, se crea una carpeta de búsqueda para buscar todos los mensajes de la bandeja de entrada y sus subcarpetas enviadas por el administrador del usuario, sadie@contoso.com.</span><span class="sxs-lookup"><span data-stu-id="ff0b5-148">In the following request example, a search folder is created to find all messages in the Inbox and its subfolders that were sent by the user's manager, sadie@contoso.com.</span></span> <span data-ttu-id="ff0b5-149">La carpeta se crea en la carpeta carpetas de búsqueda del buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="ff0b5-149">The folder is created in the Search Folders folder in the user's mailbox.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ff0b5-150">Puede crear una carpeta de búsqueda como elemento secundario de cualquier carpeta en el buzón de correo del usuario.</span><span class="sxs-lookup"><span data-stu-id="ff0b5-150">You can create a search folder as a child of any folder in the user's mailbox.</span></span> <span data-ttu-id="ff0b5-151">Sin embargo, si desea que la carpeta recién creada aparezca en las carpetas de búsqueda de Outlook, créela en carpeta de búsqueda de carpetas conocidas mediante el valor **SearchFolders** en el atributo **ID** del elemento [DistinguishedFolderId](https://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="ff0b5-151">However, if you want the newly created folder to show up under Search Folders in Outlook, create it under the Search Folders well-known folder, using the **searchfolders** value in the **Id** attribute of the [DistinguishedFolderId](https://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) element.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="ff0b5-152">El servidor responde con un mensaje [CreateFolderResponse](https://msdn.microsoft.com/library/158adecc-491a-47d9-af73-acc2cd3f8566%28Office.15%29.aspx) que incluye un valor [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, que indica que es correcto.</span><span class="sxs-lookup"><span data-stu-id="ff0b5-152">The server responds with a [CreateFolderResponse](https://msdn.microsoft.com/library/158adecc-491a-47d9-af73-acc2cd3f8566%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError**, which indicates success.</span></span>
  
## <a name="get-a-search-folder-by-using-the-ews-managed-api"></a><span data-ttu-id="ff0b5-153">Obtener una carpeta de búsqueda mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="ff0b5-153">Get a search folder by using the EWS Managed API</span></span>
<span data-ttu-id="ff0b5-154"><a name="bk_RetrieveEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="ff0b5-154"><a name="bk_RetrieveEWSMA"> </a></span></span>

<span data-ttu-id="ff0b5-155">Use el método de la API administrada de EWS [ExchangeService. FindFolders](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx) para buscar carpetas de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ff0b5-155">Use the [ExchangeService.FindFolders](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx) EWS Managed API method to find search folders.</span></span> <span data-ttu-id="ff0b5-156">Sin embargo, tenga en cuenta que no puede limitar los resultados para que solo incluyan carpetas de búsqueda; querrá tener esto en cuenta al procesar los resultados.</span><span class="sxs-lookup"><span data-stu-id="ff0b5-156">Note, however, that you can't limit your results to only include search folders; you'll want to keep that in mind when you process the results.</span></span> <span data-ttu-id="ff0b5-157">Utilice el método [SearchFolder. bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfolder.bind%28v=exchg.80%29.aspx) para obtener carpetas de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ff0b5-157">Use the [SearchFolder.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfolder.bind%28v=exchg.80%29.aspx) method to get search folders.</span></span> 
  
<span data-ttu-id="ff0b5-158">En el ejemplo siguiente se buscan las 10 primeras carpetas de la carpeta de carpetas de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ff0b5-158">The following example finds the first 10 folders in the Search Folders folder.</span></span> <span data-ttu-id="ff0b5-159">Realiza una comprobación para determinar si cada una es una carpeta de búsqueda y, si es así, obtiene la carpeta de búsqueda y muestra el número de carpetas de destino que busca.</span><span class="sxs-lookup"><span data-stu-id="ff0b5-159">It checks to determine whether each one is a search folder, and if so, it gets the search folder and displays how many target folders it searches.</span></span>
  
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

## <a name="get-a-search-folder-by-using-ews"></a><span data-ttu-id="ff0b5-160">Obtener una carpeta de búsqueda con EWS</span><span class="sxs-lookup"><span data-stu-id="ff0b5-160">Get a search folder by using EWS</span></span>
<span data-ttu-id="ff0b5-161"><a name="bk_RetrieveEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="ff0b5-161"><a name="bk_RetrieveEWS"> </a></span></span>

<span data-ttu-id="ff0b5-162">Si está usando EWS, use la [operación FindFolder](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) para buscar carpetas de búsqueda y la [operación GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) para obtener las carpetas de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ff0b5-162">If you're using EWS, use the [FindFolder operation](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) to find search folders, and the [GetFolder operation](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) to get search folders.</span></span> <span data-ttu-id="ff0b5-163">Una respuesta de **GetFolder** correcta para una carpeta de búsqueda contendrá un elemento [SearchFolder](https://msdn.microsoft.com/library/1a7d408b-2e98-4391-8834-085ed6d5757c%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="ff0b5-163">A successful **GetFolder** response for a search folder will contain a [SearchFolder](https://msdn.microsoft.com/library/1a7d408b-2e98-4391-8834-085ed6d5757c%28Office.15%29.aspx) element.</span></span> <span data-ttu-id="ff0b5-164">En el siguiente ejemplo de solicitud se buscan las 10 primeras carpetas de la carpeta de carpetas de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ff0b5-164">The following request example finds the first 10 folders in the Search Folders folder.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="ff0b5-165">El servidor devuelve la siguiente respuesta, que muestra una carpeta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ff0b5-165">The server returns the following response, which shows one search folder.</span></span>
  
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
    <m:FindFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="ff0b5-166">El siguiente ejemplo de una solicitud usa el valor del elemento [FolderId](https://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) de la respuesta anterior en una solicitud de operación **GetFolder** para obtener la carpeta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ff0b5-166">The following example of a request uses the value of the [FolderId](https://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) element from the previous response in a **GetFolder** operation request to get the search folder.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="ff0b5-167">El servidor devuelve la siguiente respuesta con todas las propiedades de la primera clase para la carpeta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ff0b5-167">The server returns the following response with all the first-class properties for the search folder.</span></span>
  
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
    <m:GetFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="update-a-search-folder-by-using-the-ews-managed-api"></a><span data-ttu-id="ff0b5-168">Actualizar una carpeta de búsqueda mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="ff0b5-168">Update a search folder by using the EWS Managed API</span></span>
<span data-ttu-id="ff0b5-169"><a name="bk_UpdateEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="ff0b5-169"><a name="bk_UpdateEWSMA"> </a></span></span>

<span data-ttu-id="ff0b5-170">Use el método [Folder. Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) de la API administrada de EWS en un objeto **SearchFolder** para actualizar una carpeta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ff0b5-170">Use the [Folder.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) EWS Managed API method on a **SearchFolder** object to update a search folder.</span></span> <span data-ttu-id="ff0b5-171">En el siguiente ejemplo se actualizan los criterios de búsqueda en una carpeta de búsqueda con el nombre para mostrar "del administrador".</span><span class="sxs-lookup"><span data-stu-id="ff0b5-171">The following example updates the search criteria on a search folder with the display name "From Manager".</span></span> 
  
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

## <a name="update-a-search-folder-by-using-ews"></a><span data-ttu-id="ff0b5-172">Actualizar una carpeta de búsqueda con EWS</span><span class="sxs-lookup"><span data-stu-id="ff0b5-172">Update a search folder by using EWS</span></span>
<span data-ttu-id="ff0b5-173"><a name="bk_UpdateEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="ff0b5-173"><a name="bk_UpdateEWS"> </a></span></span>

<span data-ttu-id="ff0b5-174">Si está usando EWS, use la [operación UpdateFolder](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) con un elemento [SearchFolder](https://msdn.microsoft.com/library/1a7d408b-2e98-4391-8834-085ed6d5757c%28Office.15%29.aspx) para actualizar una carpeta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ff0b5-174">If you're using EWS, use the [UpdateFolder operation](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) with a [SearchFolder](https://msdn.microsoft.com/library/1a7d408b-2e98-4391-8834-085ed6d5757c%28Office.15%29.aspx) element to update a search folder.</span></span> <span data-ttu-id="ff0b5-175">En el siguiente ejemplo de solicitud se actualizan los criterios de búsqueda en la carpeta de búsqueda "desde el administrador".</span><span class="sxs-lookup"><span data-stu-id="ff0b5-175">The following request example updates the search criteria on the "From Manager" search folder.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="ff0b5-176">El servidor responde con un mensaje [UpdateFolderResponse](https://msdn.microsoft.com/library/31f47739-dc9c-46ba-9e3f-cce25dc85e6e%28Office.15%29.aspx) que incluye un valor [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, que indica que es correcto.</span><span class="sxs-lookup"><span data-stu-id="ff0b5-176">The server responds with an [UpdateFolderResponse](https://msdn.microsoft.com/library/31f47739-dc9c-46ba-9e3f-cce25dc85e6e%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError**, which indicates success.</span></span>
  
## <a name="delete-a-search-folder-by-using-the-ews-managed-api"></a><span data-ttu-id="ff0b5-177">Eliminación de una carpeta de búsqueda mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="ff0b5-177">Delete a search folder by using the EWS Managed API</span></span>
<span data-ttu-id="ff0b5-178"><a name="bk_DeleteEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="ff0b5-178"><a name="bk_DeleteEWSMA"> </a></span></span>

<span data-ttu-id="ff0b5-179">Use el método [Folder. Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.delete%28v=exchg.80%29.aspx) de la API administrada de EWS en un objeto **SearchFolder** para eliminar una carpeta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ff0b5-179">Use the [Folder.Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.delete%28v=exchg.80%29.aspx) EWS Managed API method on a **SearchFolder** object to delete a search folder.</span></span> <span data-ttu-id="ff0b5-180">En el siguiente ejemplo se elimina una carpeta de búsqueda con el nombre para mostrar "del administrador".</span><span class="sxs-lookup"><span data-stu-id="ff0b5-180">The following example deletes a search folder with the display name "From Manager".</span></span> <span data-ttu-id="ff0b5-181">La carpeta de búsqueda eliminada se mueve a la carpeta elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="ff0b5-181">The deleted search folder is moved to the Deleted Items folder.</span></span> 
  
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

## <a name="delete-a-search-folder-by-using-ews"></a><span data-ttu-id="ff0b5-182">Eliminación de una carpeta de búsqueda mediante EWS</span><span class="sxs-lookup"><span data-stu-id="ff0b5-182">Delete a search folder by using EWS</span></span>
<span data-ttu-id="ff0b5-183"><a name="bk_DeleteEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="ff0b5-183"><a name="bk_DeleteEWS"> </a></span></span>

<span data-ttu-id="ff0b5-184">Si está usando EWS, use la [operación DeleteFolder](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) para eliminar una carpeta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ff0b5-184">If you're using EWS, use the [DeleteFolder operation](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) to delete a search folder.</span></span> <span data-ttu-id="ff0b5-185">En el siguiente ejemplo se elimina una carpeta de búsqueda y se mueve a la carpeta elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="ff0b5-185">The following example deletes a search folder and moves it to the Deleted Items folder.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="ff0b5-186">El servidor responde con un mensaje [DeleteFolderResponse](https://msdn.microsoft.com/library/27578bda-ef0a-4a33-bccc-2c1bc1735424%28Office.15%29.aspx) que incluye un valor [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, que indica que es correcto.</span><span class="sxs-lookup"><span data-stu-id="ff0b5-186">The server responds with a [DeleteFolderResponse](https://msdn.microsoft.com/library/27578bda-ef0a-4a33-bccc-2c1bc1735424%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError**, which indicates success.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ff0b5-187">Vea también</span><span class="sxs-lookup"><span data-stu-id="ff0b5-187">See also</span></span>

- [<span data-ttu-id="ff0b5-188">Búsqueda y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="ff0b5-188">Search and EWS in Exchange</span></span>](search-and-ews-in-exchange.md)   
- [<span data-ttu-id="ff0b5-189">Usar filtros de búsqueda con EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="ff0b5-189">Use search filters with EWS in Exchange</span></span>](how-to-use-search-filters-with-ews-in-exchange.md)    
- [<span data-ttu-id="ff0b5-190">SearchFolder (clase)</span><span class="sxs-lookup"><span data-stu-id="ff0b5-190">SearchFolder class</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfolder%28v=exchg.80%29.aspx)    
- [<span data-ttu-id="ff0b5-191">Operación CreateFolder</span><span class="sxs-lookup"><span data-stu-id="ff0b5-191">CreateFolder operation</span></span>](https://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx)    
- [<span data-ttu-id="ff0b5-192">Operación FindFolder</span><span class="sxs-lookup"><span data-stu-id="ff0b5-192">FindFolder operation</span></span>](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)   
- [<span data-ttu-id="ff0b5-193">Operación GetFolder</span><span class="sxs-lookup"><span data-stu-id="ff0b5-193">GetFolder operation</span></span>](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx)    
- [<span data-ttu-id="ff0b5-194">Operación UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="ff0b5-194">UpdateFolder operation</span></span>](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx)    
- [<span data-ttu-id="ff0b5-195">Operación DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="ff0b5-195">DeleteFolder operation</span></span>](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx)
    

