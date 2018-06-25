---
title: Trabajar con carpetas mediante EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4b3eb746-74c4-42a0-aa2c-742c147f1871
description: Obtenga información sobre cómo crear, obtener, actualizar y eliminar carpetas mediante la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: a9a9e5974b2751268f37a1c9faacce43a333bcdb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763207"
---
# <a name="work-with-folders-by-using-ews-in-exchange"></a><span data-ttu-id="b170e-103">Trabajar con carpetas mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="b170e-103">Work with folders by using EWS in Exchange</span></span>

<span data-ttu-id="b170e-104">Obtenga información sobre cómo crear, obtener, actualizar y eliminar carpetas mediante la API administrada de EWS o EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="b170e-104">Learn how to create, get, update, and delete folders by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="b170e-105">EWS en Exchange utiliza carpetas para estructurar y organizar los buzones de correo.</span><span class="sxs-lookup"><span data-stu-id="b170e-105">EWS in Exchange uses folders to structure and organize mailboxes.</span></span> <span data-ttu-id="b170e-106">Puede crear nuevos, obtener, actualizar y eliminar carpetas mediante el uso de la API administrada de EWS o EWS.</span><span class="sxs-lookup"><span data-stu-id="b170e-106">You can create new, get, update, and delete folders by using the EWS Managed API or EWS.</span></span> <span data-ttu-id="b170e-107">Cada uno de los métodos o las operaciones que aparecen en la siguiente tabla se realiza en un objeto [Folder](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder%28v=exchg.80%29.aspx) , un tipo de [carpeta](http://msdn.microsoft.com/library/812948d8-c7db-45ce-bb3a-77233a53a974%28Office.15%29.aspx) o [uno de los tipos o clases derivadas de carpeta](folders-and-items-in-ews-in-exchange.md#bk_folders).</span><span class="sxs-lookup"><span data-stu-id="b170e-107">Each of the methods or operations listed in the following table is performed on a [Folder](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder%28v=exchg.80%29.aspx) object, a [Folder](http://msdn.microsoft.com/library/812948d8-c7db-45ce-bb3a-77233a53a974%28Office.15%29.aspx) type, or [one of the derived folder classes or types](folders-and-items-in-ews-in-exchange.md#bk_folders).</span></span>
  
<span data-ttu-id="b170e-108">**La tabla 1. Métodos de las operaciones y para crear, obtener, actualizar y eliminar carpetas**</span><span class="sxs-lookup"><span data-stu-id="b170e-108">**Table 1. Methods and operations for creating, getting, updating and deleting folders**</span></span>

|<span data-ttu-id="b170e-109">**Con el fin...**</span><span class="sxs-lookup"><span data-stu-id="b170e-109">**In order to…**</span></span>|<span data-ttu-id="b170e-110">**Método de la API administrada de EWS**</span><span class="sxs-lookup"><span data-stu-id="b170e-110">**EWS Managed API method**</span></span>|<span data-ttu-id="b170e-111">**Operación de EWS**</span><span class="sxs-lookup"><span data-stu-id="b170e-111">**EWS operation**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b170e-112">Cree una carpeta</span><span class="sxs-lookup"><span data-stu-id="b170e-112">Create a folder</span></span>  <br/> |[<span data-ttu-id="b170e-113">Folder.Save</span><span class="sxs-lookup"><span data-stu-id="b170e-113">Folder.Save</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.save%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="b170e-114">CreateFolder</span><span class="sxs-lookup"><span data-stu-id="b170e-114">CreateFolder</span></span>](http://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="b170e-115">Crear una jerarquía de carpetas</span><span class="sxs-lookup"><span data-stu-id="b170e-115">Create a folder hierarchy</span></span>  <br/> |<span data-ttu-id="b170e-116">No disponible</span><span class="sxs-lookup"><span data-stu-id="b170e-116">Not available</span></span>  <br/> |[<span data-ttu-id="b170e-117">CreateFolderPath</span><span class="sxs-lookup"><span data-stu-id="b170e-117">CreateFolderPath</span></span>](http://msdn.microsoft.com/library/5a10aa5e-3f25-4ec3-a0b9-284c30918a1f%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="b170e-118">Obtener una carpeta</span><span class="sxs-lookup"><span data-stu-id="b170e-118">Get a folder</span></span>  <br/> |[<span data-ttu-id="b170e-119">Folder.Bind</span><span class="sxs-lookup"><span data-stu-id="b170e-119">Folder.Bind</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="b170e-120">GetFolder</span><span class="sxs-lookup"><span data-stu-id="b170e-120">GetFolder</span></span>](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="b170e-121">Obtener una jerarquía de carpetas</span><span class="sxs-lookup"><span data-stu-id="b170e-121">Get a folder hierarchy</span></span>  <br/> |[<span data-ttu-id="b170e-122">Folder.FindFolders</span><span class="sxs-lookup"><span data-stu-id="b170e-122">Folder.FindFolders</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="b170e-123">FindFolder</span><span class="sxs-lookup"><span data-stu-id="b170e-123">FindFolder</span></span>](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="b170e-124">Actualización de una carpeta</span><span class="sxs-lookup"><span data-stu-id="b170e-124">Update a folder</span></span>  <br/> |[<span data-ttu-id="b170e-125">Folder.Update</span><span class="sxs-lookup"><span data-stu-id="b170e-125">Folder.Update</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="b170e-126">UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="b170e-126">UpdateFolder</span></span>](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="b170e-127">Eliminar una carpeta</span><span class="sxs-lookup"><span data-stu-id="b170e-127">Delete a folder</span></span>  <br/> |[<span data-ttu-id="b170e-128">Folder.Delete</span><span class="sxs-lookup"><span data-stu-id="b170e-128">Folder.Delete</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.delete%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="b170e-129">DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="b170e-129">DeleteFolder</span></span>](http://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> |

<span data-ttu-id="b170e-130"><a name="bk_createfolderewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="b170e-130"></span></span>

## <a name="create-a-folder-by-using-the-ews-managed-api"></a><span data-ttu-id="b170e-131">Cree una carpeta mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="b170e-131">Create a folder by using the EWS Managed API</span></span>

<span data-ttu-id="b170e-132">En el ejemplo de código siguiente se muestra cómo usar la clase de [carpeta](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder%28v=exchg.80%29.aspx) para crear una nueva carpeta genérica con un [DisplayName](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.displayname%28v=exchg.80%29.aspx) de "Carpeta personalizada" y un valor de la propiedad [FolderClass](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.folderclass%28v=exchg.80%29.aspx) de IPF. Tenga en cuenta.</span><span class="sxs-lookup"><span data-stu-id="b170e-132">The following code example shows how to use the [Folder](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder%28v=exchg.80%29.aspx) class to create a new generic folder with a [DisplayName](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.displayname%28v=exchg.80%29.aspx) of "Custom Folder" and a [FolderClass](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.folderclass%28v=exchg.80%29.aspx) property value of IPF.Note.</span></span> <span data-ttu-id="b170e-133">El método [Folder.Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.save%28v=exchg.80%29.aspx) guarda la carpeta como una carpeta secundaria de la carpeta Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="b170e-133">The [Folder.Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.save%28v=exchg.80%29.aspx) method saves the folder as a child folder of the Inbox folder.</span></span> 
  
<span data-ttu-id="b170e-134">Estos ejemplos supone que **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que se ha autenticado el usuario a un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="b170e-134">These examples assume that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
// Create a custom folder.
Folder folder = new Folder(service);
folder.DisplayName = "Custom Folder";
folder.FolderClass = "IPF.Note";
// Save the folder as a child folder of the Inbox.
folder.Save(WellKnownFolderName.Inbox);
```

<span data-ttu-id="b170e-135">Para crear un tipo diferente de carpeta, como [CalendarFolder](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.calendarfolder%28v=exchg.80%29.aspx), [ContactsFolder](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.contactsfolder%28v=exchg.80%29.aspx), [SearchFolder](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfolder%28v=exchg.80%29.aspx)o [TasksFolder](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.tasksfolder%28v=exchg.80%29.aspx), cree una nueva instancia de la clase específica (en lugar de la clase genérica de **carpeta** ) y no se establece la Propiedad **FolderClass** .</span><span class="sxs-lookup"><span data-stu-id="b170e-135">To create a different type of folder, such as a [CalendarFolder](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.calendarfolder%28v=exchg.80%29.aspx), [ContactsFolder](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.contactsfolder%28v=exchg.80%29.aspx), [SearchFolder](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfolder%28v=exchg.80%29.aspx), or [TasksFolder](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.tasksfolder%28v=exchg.80%29.aspx), create a new instance of the specific class (instead of the generic **Folder** class) and do not set the **FolderClass** property.</span></span> <span data-ttu-id="b170e-136">Por ejemplo, en el ejemplo de código siguiente se muestra cómo crear un nuevo [TasksFolder](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.tasksfolder%28v=exchg.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="b170e-136">For example, the following code example shows how to create a new [TasksFolder](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.tasksfolder%28v=exchg.80%29.aspx).</span></span>
  
```cs
// Create a custom Tasks folder.
TasksFolder folder = new TasksFolder(service);
folder.DisplayName = "Custom Tasks";
// Save the folder as a child folder in the Inbox folder.
// This method call results in a CreateFolder call to EWS.
folder.Save(WellKnownFolderName.Inbox);
```

<span data-ttu-id="b170e-137">Si se intenta crear una instancia de una clase específica y también define la propiedad **FolderClass** , se produce el error [ErrorNoFolderClassOverride](http://msdn.microsoft.com/en-us/library/exchangewebservices.responsecodetype%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b170e-137">If you try to create an instance of a specific class and also set the **FolderClass** property, the [ErrorNoFolderClassOverride](http://msdn.microsoft.com/en-us/library/exchangewebservices.responsecodetype%28v=exchg.80%29.aspx) error is thrown.</span></span> 
  
<span data-ttu-id="b170e-138">Tenga en cuenta que no se puede procesar por lotes la creación de varias carpetas en una única llamada al método mediante el uso de la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="b170e-138">Note that you cannot batch the creation of multiple folders in a single method call by using the EWS Managed API.</span></span>
  
## <a name="create-a-folder-by-using-ews"></a><span data-ttu-id="b170e-139">Cree una carpeta mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="b170e-139">Create a folder by using EWS</span></span>
<span data-ttu-id="b170e-140"><a name="bk_createfolderews"> </a></span><span class="sxs-lookup"><span data-stu-id="b170e-140"></span></span>

<span data-ttu-id="b170e-141">Puede crear una sola carpeta o varias de las carpetas mediante el uso de EWS.</span><span class="sxs-lookup"><span data-stu-id="b170e-141">You can create a single folder or multiple of folders by using EWS.</span></span>
  
<span data-ttu-id="b170e-142">Para crear una sola carpeta, enviar un mensaje de solicitud de operación [CreateFolder](http://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b170e-142">To create a single folder, send a [CreateFolder](http://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) operation request message.</span></span> <span data-ttu-id="b170e-143">La solicitud de operación **CreateFolder** indica que la carpeta principal es la Bandeja de entrada, el [DisplayName](http://msdn.microsoft.com/library/e7efbbe1-6629-4d11-bed1-ed899e3f9d77%28Office.15%29.aspx) es "Carpeta personalizada" y el valor del elemento [FolderClass](http://msdn.microsoft.com/library/0041d135-2869-4612-89a5-d1aa86aa1093%28Office.15%29.aspx) es IPF. Tenga en cuenta.</span><span class="sxs-lookup"><span data-stu-id="b170e-143">The **CreateFolder** operation request indicates that the parent folder is the Inbox, the [DisplayName](http://msdn.microsoft.com/library/e7efbbe1-6629-4d11-bed1-ed899e3f9d77%28Office.15%29.aspx) is "Custom Folder", and the [FolderClass](http://msdn.microsoft.com/library/0041d135-2869-4612-89a5-d1aa86aa1093%28Office.15%29.aspx) element value is IPF.Note.</span></span> 
  
<span data-ttu-id="b170e-144">También es la solicitud XML que la API administrada de EWS envía al crear una nueva carpeta y llame al método [Folder.Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.save%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b170e-144">This is also the XML request that the EWS Managed API sends when you create a new folder and call the [Folder.Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.save%28v=exchg.80%29.aspx) method.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:CreateFolder>
      <m:ParentFolderId>
        <t:DistinguishedFolderId Id="inbox" />
      </m:ParentFolderId>
      <m:Folders>
        <t:Folder>
          <t:FolderClass>IPF.Note</t:FolderClass>
          <t:DisplayName>Custom Folder</t:DisplayName>
        </t:Folder>
      </m:Folders>
    </m:CreateFolder>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="b170e-145">El servidor responde a la solicitud de **CreateFolder** con un mensaje de [CreateFolderResponse](http://msdn.microsoft.com/library/158adecc-491a-47d9-af73-acc2cd3f8566%28Office.15%29.aspx) que incluye un valor [ResponseCode](http://msdn.microsoft.com/en-us/library/aa580757%28v=exchg.150%29.aspx) **NoError**, lo que indica que la carpeta se creó correctamente y el [FolderId](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) de el mensaje recién creado.</span><span class="sxs-lookup"><span data-stu-id="b170e-145">The server responds to the **CreateFolder** request with a [CreateFolderResponse](http://msdn.microsoft.com/library/158adecc-491a-47d9-af73-acc2cd3f8566%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/en-us/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, which indicates that the folder was created successfully, and the [FolderId](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) of the newly created message.</span></span> 
  
<span data-ttu-id="b170e-146">Para crear varias carpetas, incluir varios elementos de [carpeta](http://msdn.microsoft.com/library/812948d8-c7db-45ce-bb3a-77233a53a974%28Office.15%29.aspx) en el mensaje de solicitud de la operación de **CreateFolder** .</span><span class="sxs-lookup"><span data-stu-id="b170e-146">To create multiple folders, include multiple [Folder](http://msdn.microsoft.com/library/812948d8-c7db-45ce-bb3a-77233a53a974%28Office.15%29.aspx) elements in the **CreateFolder** operation request message.</span></span> <span data-ttu-id="b170e-147">Las nuevas carpetas deben estar en la misma carpeta primaria.</span><span class="sxs-lookup"><span data-stu-id="b170e-147">All the new folders must be in the same parent folder.</span></span> 
  
## <a name="create-a-folder-hierarchy-by-using-ews"></a><span data-ttu-id="b170e-148">Crear una jerarquía de carpetas mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="b170e-148">Create a folder hierarchy by using EWS</span></span>
<span data-ttu-id="b170e-149"><a name="bk_createfolderhierarchy"> </a></span><span class="sxs-lookup"><span data-stu-id="b170e-149"></span></span>

<span data-ttu-id="b170e-150">Puede crear una jerarquía de carpetas en una sola llamada mediante la operación de EWS [CreateFolderPath](http://msdn.microsoft.com/library/5a10aa5e-3f25-4ec3-a0b9-284c30918a1f%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b170e-150">You can create a folder hierarchy in a single call by using the EWS [CreateFolderPath](http://msdn.microsoft.com/library/5a10aa5e-3f25-4ec3-a0b9-284c30918a1f%28Office.15%29.aspx) operation.</span></span> <span data-ttu-id="b170e-151">La misma funcionalidad no está disponible en la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="b170e-151">The same functionality is not available in the EWS Managed API.</span></span> <span data-ttu-id="b170e-152">En su lugar, si está utilizando la API administrada de EWS, puede crear carpetas de uno a uno, tal como se muestra en [crear una carpeta mediante el uso de EWS](#bk_createfolderews).</span><span class="sxs-lookup"><span data-stu-id="b170e-152">Instead, if you are using the EWS Managed API, you can create folders one by one, as shown in [Create a folder by using EWS](#bk_createfolderews).</span></span>
  
> [!NOTE]
> <span data-ttu-id="b170e-153">La API administrada de EWS no implementa esta funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="b170e-153">The EWS Managed API does not implement this functionality.</span></span> 
  
## <a name="get-a-folder-by-using-the-ews-managed-api"></a><span data-ttu-id="b170e-154">Obtener una carpeta mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="b170e-154">Get a folder by using the EWS Managed API</span></span>
<span data-ttu-id="b170e-155"><a name="bk_getfolderewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="b170e-155"></span></span>

<span data-ttu-id="b170e-156">En el ejemplo de código siguiente se muestra cómo utilizar el método [Folder.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) para obtener la carpeta Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="b170e-156">The following code example shows how to use the [Folder.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) method to get the Inbox folder.</span></span> <span data-ttu-id="b170e-157">Como procedimiento recomendado, limite las propiedades devueltas a sólo los necesarios para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b170e-157">As a best practice, limit the properties returned to only those required for your application.</span></span> <span data-ttu-id="b170e-158">En este ejemplo se limita las propiedades devueltos para incluir sólo la propiedad [Id](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.id%28v=exchg.80%29.aspx) mediante la creación de un objeto [PropertySet](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.propertyset%28v=exchg.80%29.aspx) y aplicar el valor de [IdOnly](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.basepropertyset%28v=exchg.80%29.aspx) a la propiedad [BasePropertySet](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.propertyset.basepropertyset%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b170e-158">This example limits the return properties to only include the [Id](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.id%28v=exchg.80%29.aspx) property by creating a [PropertySet](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.propertyset%28v=exchg.80%29.aspx) object and applying the [IdOnly](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.basepropertyset%28v=exchg.80%29.aspx) value to the [BasePropertySet](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.propertyset.basepropertyset%28v=exchg.80%29.aspx) property.</span></span> 
  
<span data-ttu-id="b170e-159">En este ejemplo se da por supuesto que **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que se ha autenticado el usuario a un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="b170e-159">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
// As a best practice, limit the properties returned to only those that are required.
// In this scenario, you only need the FolderId.
PropertySet propSet = new PropertySet(BasePropertySet.IdOnly);
// Bind to an existing folder and get only the properties specified in the PropertySet.
// This method call results in a GetFolder call to EWS.
Folder rootfolder = Folder.Bind(service, WellKnownFolderName.Inbox, propSet);
```

<span data-ttu-id="b170e-160">Si necesita devolver propiedades adicionales, agregar las propiedades de la clase [FolderSchema](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderschema%28v=exchg.80%29.aspx) a la **PropertySet**o use uno de los sobrecargados [enlazar](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) métodos que devuelve todas las propiedades de primera clases.</span><span class="sxs-lookup"><span data-stu-id="b170e-160">If you need to return additional properties, add properties from the [FolderSchema](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderschema%28v=exchg.80%29.aspx) class to the **PropertySet**, or use one of the overloaded [Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) methods that returns all first class properties.</span></span> 
  
<span data-ttu-id="b170e-161">Tenga en cuenta que no se puede obtener varias carpetas a la vez mediante el uso de la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="b170e-161">Note that you cannot get multiple folders at one time by using the EWS Managed API.</span></span> <span data-ttu-id="b170e-162">Se debe llamar al método **enlazar** en cada carpeta por separado.</span><span class="sxs-lookup"><span data-stu-id="b170e-162">You have to call the **Bind** method on each folder separately.</span></span> 
  
## <a name="get-a-folder-by-using-ews"></a><span data-ttu-id="b170e-163">Obtener una carpeta mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="b170e-163">Get a folder by using EWS</span></span>
<span data-ttu-id="b170e-164"><a name="bk_getfolderews"> </a></span><span class="sxs-lookup"><span data-stu-id="b170e-164"></span></span>

<span data-ttu-id="b170e-165">Puede obtener una sola carpeta o en varias carpetas mediante el uso de EWS.</span><span class="sxs-lookup"><span data-stu-id="b170e-165">You can get a single folder or multiple folders by using EWS.</span></span>
  
<span data-ttu-id="b170e-166">Para obtener una sola carpeta, envíe un mensaje de solicitud de operación [GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) para el servidor.</span><span class="sxs-lookup"><span data-stu-id="b170e-166">To get a single folder, send a [GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) operation request message to the server.</span></span> <span data-ttu-id="b170e-167">En el siguiente ejemplo, se establece el [BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) a **IdOnly**, se devuelve sólo el [FolderId](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) de la carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="b170e-167">In the following example, the [BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) is set to **IdOnly**, so only the [FolderId](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) of the specified folder is returned.</span></span> <span data-ttu-id="b170e-168">El elemento [FolderIds](http://msdn.microsoft.com/library/3ff9d15a-7220-4785-ae6b-583a7eb82005%28Office.15%29.aspx) indica que la carpeta que se va a recuperar es la carpeta Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="b170e-168">The [FolderIds](http://msdn.microsoft.com/library/3ff9d15a-7220-4785-ae6b-583a7eb82005%28Office.15%29.aspx) element indicates that the folder to retrieve is the Inbox folder.</span></span> 
  
<span data-ttu-id="b170e-169">También es la solicitud XML que la API administrada de EWS envía al enlazar a una carpeta mediante el método [Folder.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b170e-169">This is also the XML request that the EWS Managed API sends when you bind to a folder by using the [Folder.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) method.</span></span> 
  
<span data-ttu-id="b170e-170">Para obtener varias carpetas, incluir varios elementos [FolderIds](http://msdn.microsoft.com/library/812948d8-c7db-45ce-bb3a-77233a53a974%28Office.15%29.aspx) en el mensaje de solicitud de operación **GetFolder** .</span><span class="sxs-lookup"><span data-stu-id="b170e-170">To get multiple folders, include multiple [FolderIds](http://msdn.microsoft.com/library/812948d8-c7db-45ce-bb3a-77233a53a974%28Office.15%29.aspx) elements in the **GetFolder** operation request message.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:GetFolder>
      <m:FolderShape>
        <t:BaseShape>IdOnly</t:BaseShape>
      </m:FolderShape>
      <m:FolderIds>
        <t:DistinguishedFolderId Id="inbox" />
      </m:FolderIds>
    </m:GetFolder>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="b170e-171">En el ejemplo de XML siguiente se muestra el mensaje de [GetFolderResponse](http://msdn.microsoft.com/library/47abeec8-78dd-4297-8525-099174ec880d%28Office.15%29.aspx) que se envía desde el servidor al cliente en respuesta a la solicitud de operación **GetFolder** .</span><span class="sxs-lookup"><span data-stu-id="b170e-171">The following XML example shows the [GetFolderResponse](http://msdn.microsoft.com/library/47abeec8-78dd-4297-8525-099174ec880d%28Office.15%29.aspx) message that is sent from the server to the client in response to the **GetFolder** operation request.</span></span> <span data-ttu-id="b170e-172">Sólo contiene el valor de [ID carpeta](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) de la carpeta Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="b170e-172">It only contains the [FolderId](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) value of the Inbox folder.</span></span> <span data-ttu-id="b170e-173">Los valores de algunos elementos y atributos se han abreviado para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="b170e-173">The values of some attributes and elements have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="800"
                         MinorBuildNumber="16"
                         Version="V2_6"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:Folder>
              <t:FolderId Id="AAAENAAA=" ChangeKey="AQAAABYAAAAPxolXAHv3TaHUnjW8wWqXAAAEkbCr"/>
            </t:Folder>
          </m:Folders>
        </m:GetFolderResponseMessage>
      </m:ResponseMessages>
    </m:GetFolderResponse>
  </s:Body>
</s:Envelope>
```

## <a name="get-a-folder-hierarchy-by-using-the-ews-managed-api"></a><span data-ttu-id="b170e-174">Obtener una jerarquía de carpetas mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="b170e-174">Get a folder hierarchy by using the EWS Managed API</span></span>
<span data-ttu-id="b170e-175"><a name="bk_getfolderhierarchyewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="b170e-175"></span></span>

<span data-ttu-id="b170e-176">En el ejemplo de código siguiente se muestra cómo recuperar las subcarpetas de una carpeta raíz especificada.</span><span class="sxs-lookup"><span data-stu-id="b170e-176">The following code example shows how to retrieve the subfolders for a specified root folder.</span></span> <span data-ttu-id="b170e-177">En este ejemplo se recuperan las subcarpetas de la carpeta **MsgFolderRoot** , que es la raíz del subárbol IPM (donde las carpetas del buzón y los elementos se almacenan).</span><span class="sxs-lookup"><span data-stu-id="b170e-177">This example retrieves the subfolders of the **MsgFolderRoot** folder, which is the root of the IPM Subtree (where your mailbox folders and items are stored).</span></span> 
  
<span data-ttu-id="b170e-178">En este ejemplo, se crea un objeto de clase [FolderView](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderview%28v=exchg.80%29.aspx) para limitar los resultados de la respuesta del método [Folder.FindFolders](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b170e-178">In this example, a [FolderView](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderview%28v=exchg.80%29.aspx) class object is created to limit the results of the [Folder.FindFolders](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx) method response.</span></span> <span data-ttu-id="b170e-179">En este escenario limita las propiedades para volver a lo siguiente: [Id](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.id%28v=exchg.80%29.aspx), [DisplayName](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.displayname%28v=exchg.80%29.aspx)y la propiedad extendida que indica si la carpeta es una carpeta oculta.</span><span class="sxs-lookup"><span data-stu-id="b170e-179">This scenario limits the properties to return to the following: [Id](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.id%28v=exchg.80%29.aspx), [DisplayName](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.displayname%28v=exchg.80%29.aspx), and the extended property that indicates whether the folder is a hidden folder.</span></span> <span data-ttu-id="b170e-180">Establezca el valor de [FolderView.Traversal](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderview.traversal%28v=EXCHG.80%29.aspx) en profunda para realizar una búsqueda recursiva de modo que el servidor recupera las subcarpetas y establece la carpeta raíz en **MsgFolderRoot**, para que el servidor devuelve todas las carpetas del usuario (y el servidor no devuelve carpetas del sistema en el subárbol no IPM).</span><span class="sxs-lookup"><span data-stu-id="b170e-180">Set the [FolderView.Traversal](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderview.traversal%28v=EXCHG.80%29.aspx) value to Deep to perform a recursive search so that the server retrieves the subfolders, and set the root folder to **MsgFolderRoot**, so that the server returns all the user's folders (and the server does not return system folders in the Non-IPM Subtree).</span></span>
  
<span data-ttu-id="b170e-181">En este ejemplo se da por supuesto que **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que se ha autenticado el usuario a un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="b170e-181">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
```XML
// Create a new folder view, and pass in the maximum number of folders to return.
FolderView view = new FolderView(folderViewSize);
// Create an extended property definition for the PR_ATTR_HIDDEN property,
// so that your results will indicate whether the folder is a hidden folder.
ExtendedPropertyDefinition isHiddenProp = new ExtendedPropertyDefinition(0x10f4, MapiPropertyType.Boolean);
// As a best practice, limit the properties returned to only those required.
// In this case, return the folder ID, DisplayName, and the value of the isHiddenProp
// extended property.
view.PropertySet = new PropertySet(BasePropertySet.IdOnly, FolderSchema.DisplayName, isHiddenProp);
// Indicate a Traversal value of Deep, so that all subfolders are retrieved.
view.Traversal = FolderTraversal.Deep;
// Call FindFolders to retrieve the folder hierarchy, starting with the MsgFolderRoot folder.
// This method call results in a FindFolder call to EWS.
FindFoldersResults findFolderResults = service.FindFolders(WellKnownFolderName.MsgFolderRoot, view);
```

## <a name="get-a-folder-hierarchy-by-using-ews"></a><span data-ttu-id="b170e-182">Obtener una jerarquía de carpetas mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="b170e-182">Get a folder hierarchy by using EWS</span></span>
<span data-ttu-id="b170e-183"><a name="bk_getfolderhierarchyews"> </a></span><span class="sxs-lookup"><span data-stu-id="b170e-183"></span></span>

<span data-ttu-id="b170e-184">Los siguientes ejemplos XML muestran cómo usar la operación [FindFolder](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) para recuperar una jerarquía de carpetas mediante el uso de EWS.</span><span class="sxs-lookup"><span data-stu-id="b170e-184">The following XML examples show how to use the [FindFolder](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) operation to retrieve a folder hierarchy by using EWS.</span></span> <span data-ttu-id="b170e-185">En este ejemplo se recupera la carpeta **msgfolderroot** , que es la raíz del subárbol IPM y todas sus subcarpetas.</span><span class="sxs-lookup"><span data-stu-id="b170e-185">This example retrieves the **msgfolderroot** folder, which is the root of the IPM Subtree, and all its subfolders.</span></span> <span data-ttu-id="b170e-186">El **cruce seguro del** atributo se establece en **profundidad** para que el servidor realiza una búsqueda recursiva de la jerarquía de carpetas y devuelve sólo las carpetas y subcarpetas en la raíz especificada en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b170e-186">The **Traversal** attribute is set to **Deep** so that the server performs a recursive search of the folder hierarchy and only returns folders and subfolders under the specified root in the response.</span></span> <span data-ttu-id="b170e-187">En este ejemplo, se establece el elemento de [BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) a **IdOnly** para que el servidor devuelve sólo el elemento de [FolderId](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b170e-187">In this example, the [BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) element is set to **IdOnly** so that the server only returns the [FolderId](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) element.</span></span> <span data-ttu-id="b170e-188">Para que el resultado sea más fácil comprender, incluya el elemento **DisplayName** en los resultados mediante la inclusión en el elemento [AdditionalProperties](http://msdn.microsoft.com/library/7a269aed-dcfd-4c3e-9e14-094e53828101%28Office.15%29.aspx) en la solicitud, junto con el valor de **ExtendedFieldURI** para el **PR_ATTR_HIDDEN** propiedad, para que sepan si las carpetas son las carpetas ocultas.</span><span class="sxs-lookup"><span data-stu-id="b170e-188">To make the output easier to understand, include the **DisplayName** element in your results by including it in the [AdditionalProperties](http://msdn.microsoft.com/library/7a269aed-dcfd-4c3e-9e14-094e53828101%28Office.15%29.aspx) element in the request, along with the **ExtendedFieldURI** value for the **PR_ATTR_HIDDEN** property, so that you know whether the folders are hidden folders.</span></span> 
  
<span data-ttu-id="b170e-189">También es la solicitud XML que la API administrada de EWS envía cuando se llama al método [FindFolders](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b170e-189">This is also the XML request that the EWS Managed API sends when you call the [FindFolders](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx) method.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:FindFolder Traversal="Deep">
      <m:FolderShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="folder:DisplayName" />
          <t:ExtendedFieldURI PropertyTag="4340"
                              PropertyType="Boolean" />
        </t:AdditionalProperties>
      </m:FolderShape>
      <m:IndexedPageFolderView MaxEntriesReturned="100"
                               Offset="0"
                               BasePoint="Beginning" />
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="msgfolderroot" />
      </m:ParentFolderIds>
    </m:FindFolder>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="b170e-190">En el ejemplo de XML siguiente se muestra el mensaje de [FindFolderResponse](http://msdn.microsoft.com/library/f5dd813c-9698-4a39-8fca-3a825df365ed%28Office.15%29.aspx) que se envía desde el servidor al cliente en respuesta a la solicitud de operación **FindFolder** .</span><span class="sxs-lookup"><span data-stu-id="b170e-190">The following XML example shows the [FindFolderResponse](http://msdn.microsoft.com/library/f5dd813c-9698-4a39-8fca-3a825df365ed%28Office.15%29.aspx) message that is sent from the server to the client in response to the **FindFolder** operation request.</span></span> <span data-ttu-id="b170e-191">Contiene sólo el [FolderId](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx), [DisplayName](http://msdn.microsoft.com/library/e7efbbe1-6629-4d11-bed1-ed899e3f9d77%28Office.15%29.aspx), y el valor de la **PR_ATTR_HIDDEN** extendidas (propiedad) para todas las subcarpetas bajo la carpeta **msgrootfolder** .</span><span class="sxs-lookup"><span data-stu-id="b170e-191">It contains only the [FolderId](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx), the [DisplayName](http://msdn.microsoft.com/library/e7efbbe1-6629-4d11-bed1-ed899e3f9d77%28Office.15%29.aspx), and the value of the **PR_ATTR_HIDDEN** extended property for all the subfolders under the **msgrootfolder** folder.</span></span> <span data-ttu-id="b170e-192">Si el elemento [Value](http://msdn.microsoft.com/library/9a30cadd-909e-41b1-b4e9-291643dd89c6%28Office.15%29.aspx) se establece en true, la carpeta debería estar oculto en la vista de cliente.</span><span class="sxs-lookup"><span data-stu-id="b170e-192">If the [Value](http://msdn.microsoft.com/library/9a30cadd-909e-41b1-b4e9-291643dd89c6%28Office.15%29.aspx) element is set to true, the folder should be hidden in the client view.</span></span> 
  
<span data-ttu-id="b170e-193">También es la respuesta XML que la API administrada de EWS envía al obtener varias carpetas mediante el método [FindFolder](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b170e-193">This is also the XML response that the EWS Managed API sends when you get multiple folders by using the [FindFolder](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx) method.</span></span> <span data-ttu-id="b170e-194">Los valores de algunos elementos y atributos se han abreviado para mejorar la legibilidad y algunas carpetas no se han incluido por razones de brevedad.</span><span class="sxs-lookup"><span data-stu-id="b170e-194">The values of some attributes and elements have been shortened for readability, and some folders have not been included for brevity.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?><s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="815"
                         MinorBuildNumber="6"
                         Version="V2_7"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="16"
                        TotalItemsInView="16"
                        IncludesLastItemInRange="true">
            <t:Folders>
              <t:CalendarFolder>
                <t:FolderId Id="AAAEOAAA="
                            ChangeKey="AgAAABYAAAAPxolXAHv3TaHUnjW8wWqXAAAAAAA3"/>
                <t:DisplayName>Calendar</t:DisplayName>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertyTag="0x10f4"
                                      PropertyType="Boolean"/>
                  <t:Value>false</t:Value>
                </t:ExtendedProperty>
              </t:CalendarFolder>
              <t:ContactsFolder>
                <t:FolderId Id="AAAEPAAA="
                            ChangeKey="AwAAABYAAAAPxolXAHv3TaHUnjW8wWqXAAAAAAA4"/>
                <t:DisplayName>Contacts</t:DisplayName>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertyTag="0x10f4"
                                      PropertyType="Boolean"/>
                  <t:Value>false</t:Value>
                </t:ExtendedProperty>
              </t:ContactsFolder>
              <t:ContactsFolder>
                <t:FolderId Id="AAAUKAAA="
                            ChangeKey="AwAAABYAAAAPxolXAHv3TaHUnjW8wWqXAAAAAAS5"/>
                <t:DisplayName>Recipient Cache</t:DisplayName>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertyTag="0x10f4"
                                      PropertyType="Boolean"/>
                  <t:Value>true</t:Value>
                </t:ExtendedProperty>
              </t:ContactsFolder>
              <t:Folder>
                <t:FolderId Id="AAAUJAAA="
                            ChangeKey="AQAAABYAAAAPxolXAHv3TaHUnjW8wWqXAAAAAASx"/>
                <t:DisplayName>Conversation Action Settings</t:DisplayName>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertyTag="0x10f4"
                                      PropertyType="Boolean"/>
                  <t:Value>true</t:Value>
                </t:ExtendedProperty>
              </t:Folder>
…
            </t:Folders>
          </m:RootFolder>
        </m:FindFolderResponseMessage>
      </m:ResponseMessages>
    </m:FindFolderResponse>
  </s:Body>
</s:Envelope>
```

## <a name="update-a-folder-by-using-the-ews-managed-api"></a><span data-ttu-id="b170e-195">Actualizar una carpeta mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="b170e-195">Update a folder by using the EWS Managed API</span></span>
<span data-ttu-id="b170e-196"><a name="bk_updatefolderewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="b170e-196"></span></span>

<span data-ttu-id="b170e-197">En el ejemplo de código siguiente se muestra cómo actualizar el nombre para mostrar de una carpeta mediante el uso de la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="b170e-197">The following code example shows how to update the display name of a folder by using the EWS Managed API.</span></span>
  
<span data-ttu-id="b170e-198">En primer lugar, cree un [PropertySet](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.propertyset%28v=exchg.80%29.aspx) para limitar el número de propiedades que el servidor devuelve en la respuesta de [Folder.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b170e-198">First, create a [PropertySet](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.propertyset%28v=exchg.80%29.aspx) to limit the number of properties that the server returns in the [Folder.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) response.</span></span> <span data-ttu-id="b170e-199">Se recomienda que use la **IdOnly** **BasePropertySet** para reducir las llamadas a la base de datos de Exchange.</span><span class="sxs-lookup"><span data-stu-id="b170e-199">We recommend that you use the **IdOnly** **BasePropertySet** to reduce calls to the Exchange database.</span></span> <span data-ttu-id="b170e-200">A continuación, utilice el método **Bind** para enlazar a la carpeta que se debe actualizar.</span><span class="sxs-lookup"><span data-stu-id="b170e-200">Next, use the **Bind** method to bind to the folder to update.</span></span> <span data-ttu-id="b170e-201">A continuación, actualice la propiedad [DisplayName](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.displayname%28v=exchg.80%29.aspx) y utilice el método [Folder.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) para guardar los cambios.</span><span class="sxs-lookup"><span data-stu-id="b170e-201">Then, update the [DisplayName](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.displayname%28v=exchg.80%29.aspx) property, and use the [Folder.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) method to save the changes.</span></span> 
  
<span data-ttu-id="b170e-202">En este ejemplo, se da por sentada ese **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que se ha autenticado el usuario a un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="b170e-202">In this example, we assume that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> <span data-ttu-id="b170e-203">La variable local *folderId* es el [identificador](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.id%28v=exchg.80%29.aspx) de la carpeta que se debe actualizar.</span><span class="sxs-lookup"><span data-stu-id="b170e-203">The local variable  *folderId*  is the [Id](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.id%28v=exchg.80%29.aspx) of the folder to update.</span></span> 
  
```cs
// As a best practice, only include the ID value in the PropertySet.
PropertySet propertySet = new PropertySet(BasePropertySet.IdOnly);
// Bind to an existing folder and get the FolderId.
// This method call results in a GetFolder call to EWS.
Folder folder = Folder.Bind(service, folderId, propertySet);
// Update the display name of the folder.
folder.DisplayName = "Updated folder name";
// Save the updates.
// This method call results in an UpdateFolder call to EWS.
folder.Update();

```

## <a name="update-a-folder-by-using-ews"></a><span data-ttu-id="b170e-204">Actualizar una carpeta mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="b170e-204">Update a folder by using EWS</span></span>
<span data-ttu-id="b170e-205"><a name="bk_updatefolderews"> </a></span><span class="sxs-lookup"><span data-stu-id="b170e-205"></span></span>

<span data-ttu-id="b170e-206">Los siguientes ejemplos XML muestran cómo actualizar el nombre para mostrar de una carpeta mediante el uso de EWS.</span><span class="sxs-lookup"><span data-stu-id="b170e-206">The following XML examples show how to update the display name of a folder by using EWS.</span></span>
  
<span data-ttu-id="b170e-207">En primer lugar, enviar un mensaje de solicitud de operación [GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) para obtener la carpeta que se va a actualizar, como se muestra en [obtener una jerarquía de carpetas mediante el uso de EWS](#bk_getfolderhierarchyews).</span><span class="sxs-lookup"><span data-stu-id="b170e-207">First, send a [GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) operation request message to get the folder to update, as shown in [Get a folder hierarchy by using EWS](#bk_getfolderhierarchyews).</span></span>
  
<span data-ttu-id="b170e-208">A continuación, enviar un mensaje de solicitud de operación de [UpdateFolder](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) al servidor para actualizar una carpeta.</span><span class="sxs-lookup"><span data-stu-id="b170e-208">Next, send an [UpdateFolder](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) operation request message to the server to update a folder.</span></span> <span data-ttu-id="b170e-209">La solicitud de operación **UpdateFolder** actualiza el [DisplayName](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) a "Actualiza carpeta personalizada".</span><span class="sxs-lookup"><span data-stu-id="b170e-209">The **UpdateFolder** operation request updates the [DisplayName](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) to "Updated Custom Folder".</span></span> 
  
<span data-ttu-id="b170e-210">También es la solicitud XML que la API administrada de EWS envía al actualizar una carpeta mediante el método [Folder.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b170e-210">This is also the XML request that the EWS Managed API sends when you update a folder by using the [Folder.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) method.</span></span> <span data-ttu-id="b170e-211">Los valores de algunos elementos y atributos se han abreviado para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="b170e-211">The values of some attributes and elements have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:UpdateFolder>
      <m:FolderChanges>
        <t:FolderChange>
          <t:FolderId Id="OrV9ZAAA=" ChangeKey="AQAAABYAAABVzRdyy/cHS4XTC9itCRdUAAAOrXWb" />
          <t:Updates>
            <t:SetFolderField>
              <t:FieldURI FieldURI="folder:DisplayName" />
              <t:Folder>
                <t:DisplayName>Updated Custom Folder</t:DisplayName>
              </t:Folder>
            </t:SetFolderField>
          </t:Updates>
        </t:FolderChange>
      </m:FolderChanges>
    </m:UpdateFolder>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="b170e-212">El servidor responde a la solicitud de **UpdateFolder** con un mensaje de [UpdateFolderResponse](http://msdn.microsoft.com/library/31f47739-dc9c-46ba-9e3f-cce25dc85e6e%28Office.15%29.aspx) que incluye el valor [ResponseCode](http://msdn.microsoft.com/en-us/library/aa580757%28v=exchg.150%29.aspx) **NoError**y el [ID carpeta](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) de la carpeta que se ha actualizado con un **actualizado ChangeKey** valor de atributo.</span><span class="sxs-lookup"><span data-stu-id="b170e-212">The server responds to the **UpdateFolder** request with a [UpdateFolderResponse](http://msdn.microsoft.com/library/31f47739-dc9c-46ba-9e3f-cce25dc85e6e%28Office.15%29.aspx) message that includes the a [ResponseCode](http://msdn.microsoft.com/en-us/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, and the [FolderId](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) of the folder that was updated with an updated **ChangeKey** attribute value.</span></span> 
  
## <a name="delete-a-folder-by-using-the-ews-managed-api"></a><span data-ttu-id="b170e-213">Eliminar una carpeta mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="b170e-213">Delete a folder by using the EWS Managed API</span></span>
<span data-ttu-id="b170e-214"><a name="bk_deletefolderewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="b170e-214"></span></span>

<span data-ttu-id="b170e-215">En este artículo se proporciona un ejemplo básico que muestra cómo eliminar una carpeta mediante el uso de la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="b170e-215">This article provides a basic example that shows you how to delete a folder by using the EWS Managed API.</span></span> <span data-ttu-id="b170e-216">Para obtener más información acerca de cómo eliminar las carpetas, vea [Eliminar elementos mediante el uso de EWS en Exchange](deleting-items-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="b170e-216">For more details about deleting folders, see [Deleting items by using EWS in Exchange](deleting-items-by-using-ews-in-exchange.md).</span></span>
  
<span data-ttu-id="b170e-217">Para eliminar una carpeta mediante el uso de la API administrada de EWS, en primer lugar, use el método [Folder.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) para enlazar con el objeto de servicio a la carpeta para eliminar.</span><span class="sxs-lookup"><span data-stu-id="b170e-217">To delete a folder by using the EWS Managed API, first, use the [Folder.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) method to bind to the service object to the folder to delete.</span></span> <span data-ttu-id="b170e-218">A continuación, use el método [Folder.Delete](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.delete%28v=exchg.80%29.aspx) para eliminar la carpeta mediante el modo de eliminación de [HardDelete](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.deletemode%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b170e-218">Next, use the [Folder.Delete](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.delete%28v=exchg.80%29.aspx) method to delete the folder by using the [HardDelete](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.deletemode%28v=exchg.80%29.aspx) deletion mode.</span></span> 
  
<span data-ttu-id="b170e-219">En este ejemplo se da por supuesto que **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que se ha autenticado el usuario a un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="b170e-219">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> <span data-ttu-id="b170e-220">La variable local *folderId* es el [identificador](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.id%28v=exchg.80%29.aspx) de la carpeta para eliminar.</span><span class="sxs-lookup"><span data-stu-id="b170e-220">The local variable  *folderId*  is the [Id](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.id%28v=exchg.80%29.aspx) of the folder to delete.</span></span> 
  
```cs
// Bind to an existing folder and get all its properties.
// This method call results in a GetFolder call to EWS.
Folder folder = Folder.Bind(service, folderId);
// HardDelete the folder.
// This method call results in a DeleteFolder call to EWS.
folder.Delete(DeleteMode.HardDelete);
```

## <a name="delete-a-folder-by-using-ews"></a><span data-ttu-id="b170e-221">Eliminar una carpeta mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="b170e-221">Delete a folder by using EWS</span></span>
<span data-ttu-id="b170e-222"><a name="bk_deletefolderews"> </a></span><span class="sxs-lookup"><span data-stu-id="b170e-222"></span></span>

<span data-ttu-id="b170e-223">En este artículo se proporciona un ejemplo XML básico que muestra cómo eliminar una carpeta mediante el uso de EWS.</span><span class="sxs-lookup"><span data-stu-id="b170e-223">This article provides a basic XML example that shows you how to delete a folder by using EWS.</span></span> <span data-ttu-id="b170e-224">Para obtener más información acerca de cómo eliminar las carpetas, vea [Eliminar elementos mediante el uso de EWS en Exchange](deleting-items-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="b170e-224">For more details about deleting folders, see [Deleting items by using EWS in Exchange](deleting-items-by-using-ews-in-exchange.md).</span></span>
  
<span data-ttu-id="b170e-225">Para eliminar una carpeta mediante el uso de EWS, en primer lugar, enviar un mensaje de solicitud de operación [GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) para obtener la carpeta que se va a actualizar tal y como se muestra en [obtener una carpeta mediante el uso de EWS](#bk_getfolderews).</span><span class="sxs-lookup"><span data-stu-id="b170e-225">To delete a folder by using EWS, first, send a [GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) operation request message to get the folder to update as shown in [Get a folder by using EWS](#bk_getfolderews).</span></span> 
  
<span data-ttu-id="b170e-226">A continuación, enviar un mensaje de solicitud de operación [DeleteFolder](http://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) al servidor para eliminar la carpeta.</span><span class="sxs-lookup"><span data-stu-id="b170e-226">Next, send a [DeleteFolder](http://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) operation request message to the server to delete the folder.</span></span> <span data-ttu-id="b170e-227">La solicitud de operación **DeleteFolder** indica que el **DeleteType** es **HardDelete** e incluye el [ID carpeta](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) de la carpeta para eliminar.</span><span class="sxs-lookup"><span data-stu-id="b170e-227">The **DeleteFolder** operation request indicates that the **DeleteType** is **HardDelete** and it includes the [FolderId](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) of the folder to delete.</span></span> 
  
<span data-ttu-id="b170e-228">También es la solicitud XML que la API administrada de EWS envía al eliminar una carpeta mediante el método [Folder.Delete](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.delete%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b170e-228">This is also the XML request that the EWS Managed API sends when you delete a folder by using the [Folder.Delete](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.delete%28v=exchg.80%29.aspx) method.</span></span> <span data-ttu-id="b170e-229">Los valores de algunos elementos y atributos se han abreviado para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="b170e-229">The values of some attributes and elements have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:DeleteFolder DeleteType="HardDelete">
      <m:FolderIds>
        <t:FolderId Id="OrV9ZAAA=" ChangeKey="AQAAABYAAABVzRdyy/cHS4XTC9itCRdUAAAOrXWf" />
      </m:FolderIds>
    </m:DeleteFolder>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="b170e-230">El servidor responde a la solicitud de **DeleteFolder** con un mensaje de [DeleteFolderResponse](http://msdn.microsoft.com/library/27578bda-ef0a-4a33-bccc-2c1bc1735424%28Office.15%29.aspx) que incluye el valor [ResponseCode](http://msdn.microsoft.com/en-us/library/aa580757%28v=exchg.150%29.aspx) **NoError**, que indica que la eliminación de la carpeta se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="b170e-230">The server responds to the **DeleteFolder** request with a [DeleteFolderResponse](http://msdn.microsoft.com/library/27578bda-ef0a-4a33-bccc-2c1bc1735424%28Office.15%29.aspx) message that includes the a [ResponseCode](http://msdn.microsoft.com/en-us/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, which indicates that the folder deletion was successful.</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="b170e-231">Siguientes pasos</span><span class="sxs-lookup"><span data-stu-id="b170e-231">Next steps</span></span>
<span data-ttu-id="b170e-232"><a name="bk_nextsteps"> </a></span><span class="sxs-lookup"><span data-stu-id="b170e-232"></span></span>

<span data-ttu-id="b170e-233">Después de recuperar las carpetas en el servidor, o realizado cambios en las carpetas, es posible que desee [sincronizar la jerarquía de carpetas](how-to-synchronize-folders-by-using-ews-in-exchange.md) o [suscribirse a las notificaciones sobre cambios de carpeta](notification-subscriptions-mailbox-events-and-ews-in-exchange.md) en el servidor.</span><span class="sxs-lookup"><span data-stu-id="b170e-233">After you have retrieved the folders on the server, or made changes to folders, you might want to [synchronize your folder hierarchy](how-to-synchronize-folders-by-using-ews-in-exchange.md) or [subscribe to notifications about folder changes](notification-subscriptions-mailbox-events-and-ews-in-exchange.md) on the server.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b170e-234">Vea también</span><span class="sxs-lookup"><span data-stu-id="b170e-234">See also</span></span>

- [<span data-ttu-id="b170e-235">Las carpetas y elementos de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="b170e-235">Folders and items in EWS in Exchange</span></span>](folders-and-items-in-ews-in-exchange.md)   
- [<span data-ttu-id="b170e-236">Trabajar con los elementos del buzón de Exchange mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="b170e-236">Work with Exchange mailbox items by using EWS in Exchange</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md)    
- [<span data-ttu-id="b170e-237">Eliminación de elementos con EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="b170e-237">Deleting items by using EWS in Exchange</span></span>](deleting-items-by-using-ews-in-exchange.md)   
- [<span data-ttu-id="b170e-238">Desarrollo de clientes de servicios web de Exchange</span><span class="sxs-lookup"><span data-stu-id="b170e-238">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)
    

