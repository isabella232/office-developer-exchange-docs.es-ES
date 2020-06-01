---
title: Operación CreateFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateFolder
api_type:
- schema
ms.assetid: 6f6c334c-b190-4e55-8f0a-38f2a018d1b3
description: La operación CreateFolder crea carpetas, carpetas de calendario, carpetas de contactos, carpetas de tareas y carpetas de búsqueda.
ms.openlocfilehash: 125a6d212e5eaf85ace71c048de809f3a05ba9b6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457553"
---
# <a name="createfolder-operation"></a><span data-ttu-id="50359-103">Operación CreateFolder</span><span class="sxs-lookup"><span data-stu-id="50359-103">CreateFolder operation</span></span>

<span data-ttu-id="50359-104">La operación CreateFolder crea carpetas, carpetas de calendario, carpetas de contactos, carpetas de tareas y carpetas de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="50359-104">The CreateFolder operation creates folders, calendar folders, contacts folders, tasks folders, and search folders.</span></span>
  
## <a name="createfolder-request-example"></a><span data-ttu-id="50359-105">Ejemplo de solicitud CreateFolder</span><span class="sxs-lookup"><span data-stu-id="50359-105">CreateFolder request example</span></span>

### <a name="description"></a><span data-ttu-id="50359-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="50359-106">Description</span></span>

<span data-ttu-id="50359-107">El siguiente ejemplo de una solicitud CreateFolder muestra cómo formar una solicitud para crear dos nuevas carpetas en la raíz del buzón.</span><span class="sxs-lookup"><span data-stu-id="50359-107">The following example of a CreateFolder request shows how to form a request to create two new folders in the mailbox root.</span></span>
  
### <a name="code"></a><span data-ttu-id="50359-108">Código</span><span class="sxs-lookup"><span data-stu-id="50359-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateFolder xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ParentFolderId>
        <t:DistinguishedFolderId Id="msgfolderroot"/>
      </ParentFolderId>
      <Folders>
        <t:Folder>
          <t:DisplayName>Folder1</t:DisplayName>
        </t:Folder>
        <t:Folder>
          <t:DisplayName>Folder2</t:DisplayName>
        </t:Folder>
      </Folders>
    </CreateFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a><span data-ttu-id="50359-109">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="50359-109">Request elements</span></span>

<span data-ttu-id="50359-110">Los siguientes elementos se usan en la solicitud:</span><span class="sxs-lookup"><span data-stu-id="50359-110">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="50359-111">CreateFolder</span><span class="sxs-lookup"><span data-stu-id="50359-111">CreateFolder</span></span>](createfolder.md)
    
- [<span data-ttu-id="50359-112">ParentFolderId (TargetFolderIdType)</span><span class="sxs-lookup"><span data-stu-id="50359-112">ParentFolderId (TargetFolderIdType)</span></span>](parentfolderid-targetfolderidtype.md)
    
- [<span data-ttu-id="50359-113">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="50359-113">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="50359-114">Folders</span><span class="sxs-lookup"><span data-stu-id="50359-114">Folders</span></span>](folders-ex15websvcsotherref.md)
    
- [<span data-ttu-id="50359-115">Folder</span><span class="sxs-lookup"><span data-stu-id="50359-115">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="50359-116">DisplayName (cadena)</span><span class="sxs-lookup"><span data-stu-id="50359-116">DisplayName (string)</span></span>](displayname-string.md)
    
> [!NOTE]
> <span data-ttu-id="50359-117">El esquema que describe estos elementos se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="50359-117">The schema that describes these elements is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
<span data-ttu-id="50359-118">Para buscar otras opciones para el mensaje de solicitud de la operación CreateFolder, explore la jerarquía del esquema.</span><span class="sxs-lookup"><span data-stu-id="50359-118">To find other options for the request message of the CreateFolder operation, explore the schema hierarchy.</span></span> <span data-ttu-id="50359-119">Empiece en el elemento [CreateFolder](createfolder.md) .</span><span class="sxs-lookup"><span data-stu-id="50359-119">Start at the [CreateFolder](createfolder.md) element.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="50359-120">Si crea una carpeta de búsqueda con una restricción mediante la propiedad **Calendar: Organizer** , una llamada a la carpeta Get posterior devolverá la restricción con el **mensaje: de** la propiedad en su ubicación.</span><span class="sxs-lookup"><span data-stu-id="50359-120">If you create a search folder with a restriction by using the **calendar:Organizer** property, a subsequent get folder call will return the restriction with the **message:from** property in its place.</span></span> <span data-ttu-id="50359-121">Estas dos propiedades se asignan a la misma propiedad MAPI subyacente.</span><span class="sxs-lookup"><span data-stu-id="50359-121">These two properties map to the same underlying MAPI property.</span></span> 
  
<span data-ttu-id="50359-122">La operación CreateFolder admite la creación de una clase de carpeta personalizada solo cuando se crea la carpeta mediante un elemento de tipo Folder genérico y se establece el elemento **FolderClass** .</span><span class="sxs-lookup"><span data-stu-id="50359-122">The CreateFolder operation supports the creation of a custom folder class only when you create the folder by using a generic folder type element and set the **FolderClass** element.</span></span> 
  
## <a name="successful-createfolder-response-example"></a><span data-ttu-id="50359-123">Ejemplo de respuesta CreateFolder correcta</span><span class="sxs-lookup"><span data-stu-id="50359-123">Successful CreateFolder response example</span></span>

### <a name="description"></a><span data-ttu-id="50359-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="50359-124">Description</span></span>

<span data-ttu-id="50359-125">En el ejemplo siguiente se muestra una respuesta correcta a la solicitud CreateFolder.</span><span class="sxs-lookup"><span data-stu-id="50359-125">The following example shows a successful response to the CreateFolder request.</span></span> <span data-ttu-id="50359-126">En este ejemplo, la respuesta devuelve los identificadores de las nuevas carpetas.</span><span class="sxs-lookup"><span data-stu-id="50359-126">In this example, the response returns the identifiers of the new folders.</span></span>
  
> [!NOTE]
> <span data-ttu-id="50359-127">El identificador de la carpeta y la clave de cambio se han abreviado para preservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="50359-127">The folder ID and the change key have been shortened to preserve readability.</span></span> 
  
### <a name="code"></a><span data-ttu-id="50359-128">Código</span><span class="sxs-lookup"><span data-stu-id="50359-128">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <CreateFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:Folder>
              <t:FolderId Id="AS4AUn==" />
            </t:Folder>
          </m:Folders>
        </m:CreateFolderResponseMessage>
        <m:CreateFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:Folder>
              <t:FolderId Id="AS4AUn==" />
            </t:Folder>
          </m:Folders>
        </m:CreateFolderResponseMessage>
      </m:ResponseMessages>
    </CreateFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-response-elements"></a><span data-ttu-id="50359-129">Elementos Response correcto</span><span class="sxs-lookup"><span data-stu-id="50359-129">Successful response elements</span></span>

<span data-ttu-id="50359-130">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="50359-130">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="50359-131">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="50359-131">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="50359-132">CreateFolderResponse</span><span class="sxs-lookup"><span data-stu-id="50359-132">CreateFolderResponse</span></span>](createfolderresponse.md)
    
- [<span data-ttu-id="50359-133">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="50359-133">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="50359-134">CreateFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="50359-134">CreateFolderResponseMessage</span></span>](createfolderresponsemessage.md)
    
- [<span data-ttu-id="50359-135">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="50359-135">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="50359-136">Folders</span><span class="sxs-lookup"><span data-stu-id="50359-136">Folders</span></span>](folders-ex15websvcsotherref.md)
    
- [<span data-ttu-id="50359-137">Folder</span><span class="sxs-lookup"><span data-stu-id="50359-137">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="50359-138">FolderId</span><span class="sxs-lookup"><span data-stu-id="50359-138">FolderId</span></span>](folderid.md)
    
<span data-ttu-id="50359-139">Para buscar otras opciones para el mensaje de respuesta de la operación CreateFolder, explore la jerarquía del esquema.</span><span class="sxs-lookup"><span data-stu-id="50359-139">To find other options for the response message of the CreateFolder operation, explore the schema hierarchy.</span></span> <span data-ttu-id="50359-140">Empiece en el elemento [CreateFolderResponse](createfolderresponse.md) .</span><span class="sxs-lookup"><span data-stu-id="50359-140">Start at the [CreateFolderResponse](createfolderresponse.md) element.</span></span> 
  
## <a name="createfolder-error-response"></a><span data-ttu-id="50359-141">Respuesta de error CreateFolder</span><span class="sxs-lookup"><span data-stu-id="50359-141">CreateFolder error response</span></span>

### <a name="description"></a><span data-ttu-id="50359-142">Descripción</span><span class="sxs-lookup"><span data-stu-id="50359-142">Description</span></span>

<span data-ttu-id="50359-143">En el ejemplo siguiente se muestra una respuesta de error a una solicitud CreateFolder.</span><span class="sxs-lookup"><span data-stu-id="50359-143">The following example shows an error response to a CreateFolder request.</span></span>
  
### <a name="code"></a><span data-ttu-id="50359-144">Código</span><span class="sxs-lookup"><span data-stu-id="50359-144">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <CreateFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateFolderResponseMessage ResponseClass="Error">
          <m:MessageText>A folder with the specified name already exists.</m:MessageText>
          <m:ResponseCode>ErrorFolderExists</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:Folders />
        </m:CreateFolderResponseMessage>
      </m:ResponseMessages>
    </CreateFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a><span data-ttu-id="50359-145">Elementos de respuesta de error</span><span class="sxs-lookup"><span data-stu-id="50359-145">Error response elements</span></span>

<span data-ttu-id="50359-146">Los siguientes elementos se usan en la respuesta de error:</span><span class="sxs-lookup"><span data-stu-id="50359-146">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="50359-147">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="50359-147">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="50359-148">CreateFolderResponse</span><span class="sxs-lookup"><span data-stu-id="50359-148">CreateFolderResponse</span></span>](createfolderresponse.md)
    
- [<span data-ttu-id="50359-149">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="50359-149">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="50359-150">CreateFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="50359-150">CreateFolderResponseMessage</span></span>](createfolderresponsemessage.md)
    
- [<span data-ttu-id="50359-151">MessageText</span><span class="sxs-lookup"><span data-stu-id="50359-151">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="50359-152">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="50359-152">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="50359-153">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="50359-153">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="50359-154">Folders</span><span class="sxs-lookup"><span data-stu-id="50359-154">Folders</span></span>](folders-ex15websvcsotherref.md)
    
<span data-ttu-id="50359-155">Para buscar otras opciones para el mensaje de respuesta de error de la operación CreateFolder, explore la jerarquía del esquema.</span><span class="sxs-lookup"><span data-stu-id="50359-155">To find other options for the error response message of the CreateFolder operation, explore the schema hierarchy.</span></span> <span data-ttu-id="50359-156">Empiece en el elemento [CreateFolderResponse](createfolderresponse.md) .</span><span class="sxs-lookup"><span data-stu-id="50359-156">Start at the [CreateFolderResponse](createfolderresponse.md) element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="50359-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="50359-157">See also</span></span>



[<span data-ttu-id="50359-158">Operación FindItem</span><span class="sxs-lookup"><span data-stu-id="50359-158">FindItem operation</span></span>](finditem-operation.md)
  
[<span data-ttu-id="50359-159">Operación FindFolder</span><span class="sxs-lookup"><span data-stu-id="50359-159">FindFolder operation</span></span>](findfolder-operation.md)
  
 <span data-ttu-id="50359-160">**CreateFolderType**</span><span class="sxs-lookup"><span data-stu-id="50359-160">**CreateFolderType**</span></span>


- [<span data-ttu-id="50359-161">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="50359-161">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="50359-162">Creación de carpetas (servicios Web de Exchange)</span><span class="sxs-lookup"><span data-stu-id="50359-162">Creating Folders (Exchange Web Services)</span></span>](https://msdn.microsoft.com/library/3b15b0ec-8691-45ed-9a24-a91ff732d6cf%28Office.15%29.aspx)

