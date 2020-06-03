---
title: Operación CreateManagedFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateManagedFolder
api_type:
- schema
ms.assetid: 60a668a2-b4e9-4db9-ac76-9b181e47b302
description: La operación CreateManagedFolder crea una carpeta administrada en el almacén de Exchange.
ms.openlocfilehash: 779c730b55b9b441644108a6837f9e22d39cc2f4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44444596"
---
# <a name="createmanagedfolder-operation"></a><span data-ttu-id="fbf45-103">Operación CreateManagedFolder</span><span class="sxs-lookup"><span data-stu-id="fbf45-103">CreateManagedFolder operation</span></span>

<span data-ttu-id="fbf45-104">La operación CreateManagedFolder crea una carpeta administrada en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="fbf45-104">The CreateManagedFolder operation creates a managed folder in the Exchange store.</span></span>
  
## <a name="using-the-createmanagedfolder-operation"></a><span data-ttu-id="fbf45-105">Uso de la operación CreateManagedFolder</span><span class="sxs-lookup"><span data-stu-id="fbf45-105">Using the CreateManagedFolder Operation</span></span>

<span data-ttu-id="fbf45-106">La operación CreateManagedFolder agrega una carpeta personalizada administrada al buzón de un usuario.</span><span class="sxs-lookup"><span data-stu-id="fbf45-106">The CreateManagedFolder operation adds a managed custom folder to a user's mailbox.</span></span> <span data-ttu-id="fbf45-107">Puede usar el cmdlet **Get-ManagedFolder** del shell de administración de Exchange para buscar las carpetas administradas que se pueden agregar.</span><span class="sxs-lookup"><span data-stu-id="fbf45-107">You can use the Exchange Management Shell **Get-ManagedFolder** cmdlet to find available managed folders to add.</span></span> <span data-ttu-id="fbf45-108">Aunque este cmdlet devuelve las carpetas personalizadas administradas y las carpetas predeterminadas administradas, solo se pueden agregar carpetas personalizadas administradas.</span><span class="sxs-lookup"><span data-stu-id="fbf45-108">Although this cmdlet returns both managed custom folders and managed default folders, only managed custom folders can be added.</span></span> <span data-ttu-id="fbf45-109">Las carpetas personalizadas administradas se identifican mediante el tipo de carpeta ManagedCustomFolder.</span><span class="sxs-lookup"><span data-stu-id="fbf45-109">Managed custom folders are identified by the ManagedCustomFolder folder type.</span></span> <span data-ttu-id="fbf45-110">El espacio de nombres System. DirectoryServices también incluye tipos que se pueden usar para detectar los nombres de las carpetas administradas disponibles.</span><span class="sxs-lookup"><span data-stu-id="fbf45-110">The System.DirectoryServices namespace also includes types that can be used to discover the names of available managed folders.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="fbf45-111">No puede usar los servicios web Exchange para encontrar los nombres de las carpetas administradas disponibles para agregar a un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="fbf45-111">You cannot use Exchange Web Services to find the names of available managed folders to add to a mailbox.</span></span> 
  
<span data-ttu-id="fbf45-112">Puede usar las operaciones FindFolder y GetFolder para tener acceso a las carpetas administradas.</span><span class="sxs-lookup"><span data-stu-id="fbf45-112">You can use the FindFolder and GetFolder operations to access managed folders.</span></span> <span data-ttu-id="fbf45-113">FindFolder se usa para buscar carpetas en una carpeta principal especificada.</span><span class="sxs-lookup"><span data-stu-id="fbf45-113">FindFolder is used to search for folders in a specified parent folder.</span></span> <span data-ttu-id="fbf45-114">Esto puede usarse para que las carpetas administradas se puedan detectar en una carpeta antes de intentar agregar una carpeta personalizada administrada duplicada al mismo directorio.</span><span class="sxs-lookup"><span data-stu-id="fbf45-114">This can be used so that managed folders can be discovered in a folder before trying to add a duplicate managed custom folder to the same directory.</span></span> <span data-ttu-id="fbf45-115">GetFolder se usa después de la operación FindFolder para obtener más información acerca de una carpeta administrada personalizada.</span><span class="sxs-lookup"><span data-stu-id="fbf45-115">GetFolder is used after the FindFolder operation to get more information about a managed custom folder.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fbf45-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fbf45-116">Remarks</span></span>

<span data-ttu-id="fbf45-117">Para obtener información acerca de cómo configurar la Directiva de administración de registros de mensajes (MRM), consulte [How to Create a Managed Folder Mailbox Policy](https://go.microsoft.com/fwlink/?LinkId=100975).</span><span class="sxs-lookup"><span data-stu-id="fbf45-117">For information about how to set up messaging records management (MRM) policy, see [How to Create a Managed Folder Mailbox Policy](https://go.microsoft.com/fwlink/?LinkId=100975).</span></span>
  
<span data-ttu-id="fbf45-118">Para obtener información acerca de cómo quitar las carpetas personalizadas administradas de un buzón de correo, vea [Remove-ManagedFolder](https://go.microsoft.com/fwlink/?LinkId=100976).</span><span class="sxs-lookup"><span data-stu-id="fbf45-118">For information about how to remove managed custom folders from a mailbox, see [Remove-ManagedFolder](https://go.microsoft.com/fwlink/?LinkId=100976).</span></span>
  
## <a name="createmanagedfolder-request-example"></a><span data-ttu-id="fbf45-119">Ejemplo de solicitud CreateManagedFolder</span><span class="sxs-lookup"><span data-stu-id="fbf45-119">CreateManagedFolder request example</span></span>

### <a name="description"></a><span data-ttu-id="fbf45-120">Description</span><span class="sxs-lookup"><span data-stu-id="fbf45-120">Description</span></span>

<span data-ttu-id="fbf45-121">El siguiente ejemplo de una solicitud de CreateManagedFolder muestra cómo agregar una carpeta administrada llamada test Managed Folder a un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="fbf45-121">The following example of a CreateManagedFolder request shows how to add a managed folder named Test Managed Folder to a mailbox.</span></span>
  
> [!NOTE]
> <span data-ttu-id="fbf45-122">También puede usar acceso delegado para agregar carpetas administradas personalizadas.</span><span class="sxs-lookup"><span data-stu-id="fbf45-122">You can also use delegate access to add managed custom folders.</span></span> 
  
### <a name="code"></a><span data-ttu-id="fbf45-123">Código</span><span class="sxs-lookup"><span data-stu-id="fbf45-123">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateManagedFolder xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <FolderNames>
        <t:FolderName>Test Managed Folder</t:FolderName>
      </FolderNames>
    </CreateManagedFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a><span data-ttu-id="fbf45-124">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="fbf45-124">Request elements</span></span>

<span data-ttu-id="fbf45-125">Los siguientes elementos se usan en la solicitud:</span><span class="sxs-lookup"><span data-stu-id="fbf45-125">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="fbf45-126">CreateManagedFolder</span><span class="sxs-lookup"><span data-stu-id="fbf45-126">CreateManagedFolder</span></span>](createmanagedfolder.md)
    
- [<span data-ttu-id="fbf45-127">FolderNames</span><span class="sxs-lookup"><span data-stu-id="fbf45-127">FolderNames</span></span>](foldernames.md)
    
- [<span data-ttu-id="fbf45-128">FolderName</span><span class="sxs-lookup"><span data-stu-id="fbf45-128">FolderName</span></span>](foldername.md)
    
<span data-ttu-id="fbf45-129">Para buscar otras opciones para el mensaje de solicitud de la operación CreateManagedFolder, explore la jerarquía del esquema.</span><span class="sxs-lookup"><span data-stu-id="fbf45-129">To find other options for the request message of the CreateManagedFolder operation, explore the schema hierarchy.</span></span> <span data-ttu-id="fbf45-130">Empiece en el elemento [CreateManagedFolder](createmanagedfolder.md) .</span><span class="sxs-lookup"><span data-stu-id="fbf45-130">Start at the [CreateManagedFolder](createmanagedfolder.md) element.</span></span> 
  
## <a name="successful-createmanagedfolder-response"></a><span data-ttu-id="fbf45-131">Respuesta CreateManagedFolder correcta</span><span class="sxs-lookup"><span data-stu-id="fbf45-131">Successful CreateManagedFolder Response</span></span>

### <a name="description"></a><span data-ttu-id="fbf45-132">Description</span><span class="sxs-lookup"><span data-stu-id="fbf45-132">Description</span></span>

<span data-ttu-id="fbf45-133">En el ejemplo de código siguiente se muestra una respuesta correcta a una solicitud CreateManagedFolder.</span><span class="sxs-lookup"><span data-stu-id="fbf45-133">The following code example shows a successful response to a CreateManagedFolder request.</span></span>
  
> [!NOTE]
> <span data-ttu-id="fbf45-134">Los valores de atributo **ID** y **changekey** se han abreviado para preservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="fbf45-134">The **Id** and **ChangeKey** attribute values have been shortened to preserve readability.</span></span> 
  
### <a name="code"></a><span data-ttu-id="fbf45-135">Código</span><span class="sxs-lookup"><span data-stu-id="fbf45-135">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="598" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <CreateManagedFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                 xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                                 xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateManagedFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:Folder>
              <t:FolderId Id="AS0AdX=" ChangeKey="AACADA=="/>
            </t:Folder>
          </m:Folders>
        </m:CreateManagedFolderResponseMessage>
      </m:ResponseMessages>
    </CreateManagedFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-response-elements"></a><span data-ttu-id="fbf45-136">Elementos Response correcto</span><span class="sxs-lookup"><span data-stu-id="fbf45-136">Successful response elements</span></span>

<span data-ttu-id="fbf45-137">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="fbf45-137">The following elements are used in the response:</span></span> 
  
- [<span data-ttu-id="fbf45-138">CreateManagedFolderResponse</span><span class="sxs-lookup"><span data-stu-id="fbf45-138">CreateManagedFolderResponse</span></span>](createmanagedfolderresponse.md)
    
- [<span data-ttu-id="fbf45-139">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="fbf45-139">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="fbf45-140">CreateManagedFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="fbf45-140">CreateManagedFolderResponseMessage</span></span>](createmanagedfolderresponsemessage.md)
    
- [<span data-ttu-id="fbf45-141">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="fbf45-141">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="fbf45-142">Folders</span><span class="sxs-lookup"><span data-stu-id="fbf45-142">Folders</span></span>](folders-ex15websvcsotherref.md)
    
- [<span data-ttu-id="fbf45-143">Folder</span><span class="sxs-lookup"><span data-stu-id="fbf45-143">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="fbf45-144">FolderId</span><span class="sxs-lookup"><span data-stu-id="fbf45-144">FolderId</span></span>](folderid.md)
    
<span data-ttu-id="fbf45-145">Para buscar otras opciones de los mensajes de respuesta de la operación CreateManagedFolder, explore la jerarquía del esquema.</span><span class="sxs-lookup"><span data-stu-id="fbf45-145">To find other options for the response messages of the CreateManagedFolder operation, explore the schema hierarchy.</span></span> <span data-ttu-id="fbf45-146">Empiece en el elemento [CreateManagedFolderResponse](createmanagedfolderresponse.md) .</span><span class="sxs-lookup"><span data-stu-id="fbf45-146">Start at the [CreateManagedFolderResponse](createmanagedfolderresponse.md) element.</span></span> 
  
## <a name="createmanagedfolder-error-response"></a><span data-ttu-id="fbf45-147">Respuesta de error de CreateManagedFolder</span><span class="sxs-lookup"><span data-stu-id="fbf45-147">CreateManagedFolder error response</span></span>

### <a name="description"></a><span data-ttu-id="fbf45-148">Description</span><span class="sxs-lookup"><span data-stu-id="fbf45-148">Description</span></span>

<span data-ttu-id="fbf45-149">El siguiente ejemplo de código muestra una respuesta de error a una solicitud CreateManagedFolder.</span><span class="sxs-lookup"><span data-stu-id="fbf45-149">The following code example shows an error response to a CreateManagedFolder request.</span></span>
  
### <a name="code"></a><span data-ttu-id="fbf45-150">Código</span><span class="sxs-lookup"><span data-stu-id="fbf45-150">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="598" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <CreateManagedFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                 xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                                 xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateManagedFolderResponseMessage ResponseClass="Error">
          <m:MessageText>A specified managed folder already exists in the mailbox.</m:MessageText>
          <m:ResponseCode>ErrorManagedFolderAlreadyExists</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:Folders/>
        </m:CreateManagedFolderResponseMessage>
      </m:ResponseMessages>
    </CreateManagedFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a><span data-ttu-id="fbf45-151">Elementos de respuesta de error</span><span class="sxs-lookup"><span data-stu-id="fbf45-151">Error response elements</span></span>

<span data-ttu-id="fbf45-152">Los siguientes elementos se usan en la respuesta de error:</span><span class="sxs-lookup"><span data-stu-id="fbf45-152">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="fbf45-153">CreateManagedFolderResponse</span><span class="sxs-lookup"><span data-stu-id="fbf45-153">CreateManagedFolderResponse</span></span>](createmanagedfolderresponse.md)
    
- [<span data-ttu-id="fbf45-154">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="fbf45-154">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="fbf45-155">CreateManagedFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="fbf45-155">CreateManagedFolderResponseMessage</span></span>](createmanagedfolderresponsemessage.md)
    
- [<span data-ttu-id="fbf45-156">MessageText</span><span class="sxs-lookup"><span data-stu-id="fbf45-156">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="fbf45-157">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="fbf45-157">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="fbf45-158">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="fbf45-158">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="fbf45-159">Folders</span><span class="sxs-lookup"><span data-stu-id="fbf45-159">Folders</span></span>](folders-ex15websvcsotherref.md)
    
## <a name="see-also"></a><span data-ttu-id="fbf45-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="fbf45-160">See also</span></span>



[<span data-ttu-id="fbf45-161">Operación GetFolder</span><span class="sxs-lookup"><span data-stu-id="fbf45-161">GetFolder operation</span></span>](getfolder-operation.md)
  
[<span data-ttu-id="fbf45-162">Operación FindFolder</span><span class="sxs-lookup"><span data-stu-id="fbf45-162">FindFolder operation</span></span>](findfolder-operation.md)


[<span data-ttu-id="fbf45-163">Buscar carpetas</span><span class="sxs-lookup"><span data-stu-id="fbf45-163">Finding Folders</span></span>](https://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)
  
[<span data-ttu-id="fbf45-164">Adición de carpetas administradas</span><span class="sxs-lookup"><span data-stu-id="fbf45-164">Adding Managed Folders</span></span>](https://msdn.microsoft.com/library/846658c6-7043-40fb-8439-19f97c2a967f%28Office.15%29.aspx)

