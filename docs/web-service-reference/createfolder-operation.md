---
title: CreateFolder Operation
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
description: La operación CreateFolder crea carpetas, las carpetas de calendario, las carpetas de contactos, tareas de las carpetas y búsqueda carpetas.
ms.openlocfilehash: 97156d4a3747cacbdcf9563d21d93a0aa44c3358
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763932"
---
# <a name="createfolder-operation"></a><span data-ttu-id="32e98-103">CreateFolder Operation</span><span class="sxs-lookup"><span data-stu-id="32e98-103">CreateFolder operation</span></span>

<span data-ttu-id="32e98-104">La operación CreateFolder crea carpetas, las carpetas de calendario, las carpetas de contactos, tareas de las carpetas y búsqueda carpetas.</span><span class="sxs-lookup"><span data-stu-id="32e98-104">The CreateFolder operation creates folders, calendar folders, contacts folders, tasks folders, and search folders.</span></span>
  
## <a name="createfolder-request-example"></a><span data-ttu-id="32e98-105">Ejemplo de solicitud de CreateFolder</span><span class="sxs-lookup"><span data-stu-id="32e98-105">CreateFolder request example</span></span>

### <a name="description"></a><span data-ttu-id="32e98-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="32e98-106">Description</span></span>

<span data-ttu-id="32e98-107">El siguiente ejemplo de una solicitud de CreateFolder muestra cómo formar una solicitud para crear dos nuevas carpetas en la raíz del buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="32e98-107">The following example of a CreateFolder request shows how to form a request to create two new folders in the mailbox root.</span></span>
  
### <a name="code"></a><span data-ttu-id="32e98-108">Código</span><span class="sxs-lookup"><span data-stu-id="32e98-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateFolder xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="request-elements"></a><span data-ttu-id="32e98-109">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="32e98-109">Request elements</span></span>

<span data-ttu-id="32e98-110">En la solicitud se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="32e98-110">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="32e98-111">CreateFolder</span><span class="sxs-lookup"><span data-stu-id="32e98-111">CreateFolder</span></span>](createfolder.md)
    
- [<span data-ttu-id="32e98-112">ID (TargetFolderIdType)</span><span class="sxs-lookup"><span data-stu-id="32e98-112">ParentFolderId (TargetFolderIdType)</span></span>](parentfolderid-targetfolderidtype.md)
    
- [<span data-ttu-id="32e98-113">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="32e98-113">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="32e98-114">Carpetas</span><span class="sxs-lookup"><span data-stu-id="32e98-114">Folders</span></span>](folders-ex15websvcsotherref.md)
    
- [<span data-ttu-id="32e98-115">Folder</span><span class="sxs-lookup"><span data-stu-id="32e98-115">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="32e98-116">DisplayName (cadena)</span><span class="sxs-lookup"><span data-stu-id="32e98-116">DisplayName (string)</span></span>](displayname-string.md)
    
> [!NOTE]
> <span data-ttu-id="32e98-117">El esquema que describe estos elementos se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="32e98-117">The schema that describes these elements is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
<span data-ttu-id="32e98-118">Para buscar otras opciones para el mensaje de solicitud de la operación CreateFolder, explore la jerarquía de esquema.</span><span class="sxs-lookup"><span data-stu-id="32e98-118">To find other options for the request message of the CreateFolder operation, explore the schema hierarchy.</span></span> <span data-ttu-id="32e98-119">Comenzar en el elemento de [CreateFolder](createfolder.md) .</span><span class="sxs-lookup"><span data-stu-id="32e98-119">Start at the [CreateFolder](createfolder.md) element.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="32e98-120">Si crea una carpeta de búsqueda con una restricción mediante el uso de la propiedad **Calendario: organizador** , una llamada de carpeta get subsiguientes devolverá la restricción con la **mensaje: desde** (propiedad) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="32e98-120">If you create a search folder with a restriction by using the **calendar:Organizer** property, a subsequent get folder call will return the restriction with the **message:from** property in its place.</span></span> <span data-ttu-id="32e98-121">Estas dos propiedades se asignan a la misma propiedad MAPI subyacente.</span><span class="sxs-lookup"><span data-stu-id="32e98-121">These two properties map to the same underlying MAPI property.</span></span> 
  
<span data-ttu-id="32e98-122">La operación CreateFolder admite la creación de una clase de carpeta personalizada sólo al crear la carpeta mediante el uso de un elemento de tipo genérico de carpeta y establecer el elemento **FolderClass** .</span><span class="sxs-lookup"><span data-stu-id="32e98-122">The CreateFolder operation supports the creation of a custom folder class only when you create the folder by using a generic folder type element and set the **FolderClass** element.</span></span> 
  
## <a name="successful-createfolder-response-example"></a><span data-ttu-id="32e98-123">Ejemplo de respuesta correcta de CreateFolder</span><span class="sxs-lookup"><span data-stu-id="32e98-123">Successful CreateFolder response example</span></span>

### <a name="description"></a><span data-ttu-id="32e98-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="32e98-124">Description</span></span>

<span data-ttu-id="32e98-125">En el ejemplo siguiente se muestra una respuesta correcta a la solicitud de CreateFolder.</span><span class="sxs-lookup"><span data-stu-id="32e98-125">The following example shows a successful response to the CreateFolder request.</span></span> <span data-ttu-id="32e98-126">En este ejemplo, la respuesta devuelve los identificadores de las carpetas nuevas.</span><span class="sxs-lookup"><span data-stu-id="32e98-126">In this example, the response returns the identifiers of the new folders.</span></span>
  
> [!NOTE]
> <span data-ttu-id="32e98-127">El identificador de la carpeta y la clave de cambio se han abreviado para conservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="32e98-127">The folder ID and the change key have been shortened to preserve readability.</span></span> 
  
### <a name="code"></a><span data-ttu-id="32e98-128">Código</span><span class="sxs-lookup"><span data-stu-id="32e98-128">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <CreateFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="successful-response-elements"></a><span data-ttu-id="32e98-129">Elementos de respuesta correcta</span><span class="sxs-lookup"><span data-stu-id="32e98-129">Successful response elements</span></span>

<span data-ttu-id="32e98-130">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="32e98-130">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="32e98-131">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="32e98-131">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="32e98-132">CreateFolderResponse</span><span class="sxs-lookup"><span data-stu-id="32e98-132">CreateFolderResponse</span></span>](createfolderresponse.md)
    
- [<span data-ttu-id="32e98-133">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="32e98-133">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="32e98-134">CreateFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="32e98-134">CreateFolderResponseMessage</span></span>](createfolderresponsemessage.md)
    
- [<span data-ttu-id="32e98-135">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="32e98-135">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="32e98-136">Carpetas</span><span class="sxs-lookup"><span data-stu-id="32e98-136">Folders</span></span>](folders-ex15websvcsotherref.md)
    
- [<span data-ttu-id="32e98-137">Folder</span><span class="sxs-lookup"><span data-stu-id="32e98-137">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="32e98-138">FolderId</span><span class="sxs-lookup"><span data-stu-id="32e98-138">FolderId</span></span>](folderid.md)
    
<span data-ttu-id="32e98-139">Para buscar otras opciones para el mensaje de respuesta de la operación CreateFolder, explore la jerarquía de esquema.</span><span class="sxs-lookup"><span data-stu-id="32e98-139">To find other options for the response message of the CreateFolder operation, explore the schema hierarchy.</span></span> <span data-ttu-id="32e98-140">Comenzar en el elemento de [CreateFolderResponse](createfolderresponse.md) .</span><span class="sxs-lookup"><span data-stu-id="32e98-140">Start at the [CreateFolderResponse](createfolderresponse.md) element.</span></span> 
  
## <a name="createfolder-error-response"></a><span data-ttu-id="32e98-141">Respuesta de error CreateFolder</span><span class="sxs-lookup"><span data-stu-id="32e98-141">CreateFolder error response</span></span>

### <a name="description"></a><span data-ttu-id="32e98-142">Descripción</span><span class="sxs-lookup"><span data-stu-id="32e98-142">Description</span></span>

<span data-ttu-id="32e98-143">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de CreateFolder.</span><span class="sxs-lookup"><span data-stu-id="32e98-143">The following example shows an error response to a CreateFolder request.</span></span>
  
### <a name="code"></a><span data-ttu-id="32e98-144">Código</span><span class="sxs-lookup"><span data-stu-id="32e98-144">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <CreateFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="error-response-elements"></a><span data-ttu-id="32e98-145">Elementos de respuesta de error</span><span class="sxs-lookup"><span data-stu-id="32e98-145">Error response elements</span></span>

<span data-ttu-id="32e98-146">En la respuesta de error, se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="32e98-146">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="32e98-147">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="32e98-147">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="32e98-148">CreateFolderResponse</span><span class="sxs-lookup"><span data-stu-id="32e98-148">CreateFolderResponse</span></span>](createfolderresponse.md)
    
- [<span data-ttu-id="32e98-149">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="32e98-149">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="32e98-150">CreateFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="32e98-150">CreateFolderResponseMessage</span></span>](createfolderresponsemessage.md)
    
- [<span data-ttu-id="32e98-151">MessageText</span><span class="sxs-lookup"><span data-stu-id="32e98-151">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="32e98-152">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="32e98-152">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="32e98-153">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="32e98-153">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="32e98-154">Carpetas</span><span class="sxs-lookup"><span data-stu-id="32e98-154">Folders</span></span>](folders-ex15websvcsotherref.md)
    
<span data-ttu-id="32e98-155">Para buscar otras opciones para el mensaje de respuesta de error de la operación CreateFolder, explore la jerarquía de esquema.</span><span class="sxs-lookup"><span data-stu-id="32e98-155">To find other options for the error response message of the CreateFolder operation, explore the schema hierarchy.</span></span> <span data-ttu-id="32e98-156">Comenzar en el elemento de [CreateFolderResponse](createfolderresponse.md) .</span><span class="sxs-lookup"><span data-stu-id="32e98-156">Start at the [CreateFolderResponse](createfolderresponse.md) element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="32e98-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="32e98-157">See also</span></span>



[<span data-ttu-id="32e98-158">Operación FindItem</span><span class="sxs-lookup"><span data-stu-id="32e98-158">FindItem operation</span></span>](finditem-operation.md)
  
[<span data-ttu-id="32e98-159">Operación FindFolder</span><span class="sxs-lookup"><span data-stu-id="32e98-159">FindFolder operation</span></span>](findfolder-operation.md)
  
 <span data-ttu-id="32e98-160">**CreateFolderType**</span><span class="sxs-lookup"><span data-stu-id="32e98-160">**CreateFolderType**</span></span>


- [<span data-ttu-id="32e98-161">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="32e98-161">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="32e98-162">Creación de carpetas (servicios Web de Exchange)</span><span class="sxs-lookup"><span data-stu-id="32e98-162">Creating Folders (Exchange Web Services)</span></span>](http://msdn.microsoft.com/library/3b15b0ec-8691-45ed-9a24-a91ff732d6cf%28Office.15%29.aspx)

