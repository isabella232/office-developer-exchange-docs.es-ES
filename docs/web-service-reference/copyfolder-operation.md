---
title: Operación CopyFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CopyFolder
api_type:
- schema
ms.assetid: c7ea0d68-9793-4144-b378-d99536776db9
description: La operación CopyFolder copia carpetas en un buzón.
ms.openlocfilehash: 1f9a7a3f3ede2d3cf8f9d41677d8ce0487266f17
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468897"
---
# <a name="copyfolder-operation"></a><span data-ttu-id="8414f-103">Operación CopyFolder</span><span class="sxs-lookup"><span data-stu-id="8414f-103">CopyFolder operation</span></span>

<span data-ttu-id="8414f-104">La operación CopyFolder copia carpetas en un buzón.</span><span class="sxs-lookup"><span data-stu-id="8414f-104">The CopyFolder operation copies folders in a mailbox.</span></span>
  
## <a name="using-the-copyfolder-operation"></a><span data-ttu-id="8414f-105">Uso de la operación CopyFolder</span><span class="sxs-lookup"><span data-stu-id="8414f-105">Using the CopyFolder operation</span></span>

<span data-ttu-id="8414f-106">La operación CopyFolder es similar a la [operación MoveFolder](movefolder-operation.md).</span><span class="sxs-lookup"><span data-stu-id="8414f-106">The CopyFolder operation is similar to the [MoveFolder operation](movefolder-operation.md).</span></span> <span data-ttu-id="8414f-107">Copia las carpetas identificadas y devuelve el **identificador** y la **changekey** de las carpetas que se han copiado.</span><span class="sxs-lookup"><span data-stu-id="8414f-107">It copies identified folders and returns the **Id** and **ChangeKey** of the copied folders.</span></span> 
  
## <a name="copyfolder-request-example"></a><span data-ttu-id="8414f-108">Ejemplo de solicitud CopyFolder</span><span class="sxs-lookup"><span data-stu-id="8414f-108">CopyFolder request example</span></span>

### <a name="description"></a><span data-ttu-id="8414f-109">Description</span><span class="sxs-lookup"><span data-stu-id="8414f-109">Description</span></span>

<span data-ttu-id="8414f-110">El siguiente ejemplo de una solicitud CopyFolder muestra cómo copiar carpetas en la carpeta Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="8414f-110">The following example of a CopyFolder request shows how to copy folders into the Inbox folder.</span></span>
  
> [!NOTE]
> <span data-ttu-id="8414f-111">El valor del atributo **ID** del elemento [FolderId](folderid.md) se ha abreviado para facilitar su lectura.</span><span class="sxs-lookup"><span data-stu-id="8414f-111">The value of the **Id** attribute of the [FolderId](folderid.md) element has been shortened for readability.</span></span> 
  
### <a name="code"></a><span data-ttu-id="8414f-112">Código</span><span class="sxs-lookup"><span data-stu-id="8414f-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CopyFolder xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ToFolderId>
        <t:DistinguishedFolderId Id="inbox"/>
      </ToFolderId>
      <FolderIds>
        <t:FolderId Id="AS4A=" ChangeKey="fsVU4=="/>
        <t:FolderId Id="AS4AU=" ChangeKey="fsVU4o=="/>
      </FolderIds>
    </CopyFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="8414f-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8414f-113">Comments</span></span>

<span data-ttu-id="8414f-114">Las carpetas pueden identificarse mediante el elemento [DistinguishedFolderId](distinguishedfolderid.md) o el elemento [FolderId](folderid.md) para su uso en los elementos [ToFolderId](tofolderid.md) o [FolderIds](folderids.md) .</span><span class="sxs-lookup"><span data-stu-id="8414f-114">Folders can be identified by either the [DistinguishedFolderId](distinguishedfolderid.md) element or the [FolderId](folderid.md) element for use in either the [ToFolderId](tofolderid.md) or the [FolderIds](folderids.md) elements.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="8414f-115">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="8414f-115">Request elements</span></span>

<span data-ttu-id="8414f-116">Los siguientes elementos se usan en la solicitud:</span><span class="sxs-lookup"><span data-stu-id="8414f-116">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="8414f-117">CopyFolder</span><span class="sxs-lookup"><span data-stu-id="8414f-117">CopyFolder</span></span>](copyfolder.md)
    
- [<span data-ttu-id="8414f-118">ToFolderId</span><span class="sxs-lookup"><span data-stu-id="8414f-118">ToFolderId</span></span>](tofolderid.md)
    
- [<span data-ttu-id="8414f-119">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="8414f-119">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="8414f-120">FolderIds</span><span class="sxs-lookup"><span data-stu-id="8414f-120">FolderIds</span></span>](folderids.md)
    
- [<span data-ttu-id="8414f-121">FolderId</span><span class="sxs-lookup"><span data-stu-id="8414f-121">FolderId</span></span>](folderid.md)
    
> [!NOTE]
> <span data-ttu-id="8414f-122">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="8414f-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
<span data-ttu-id="8414f-123">Para buscar otras opciones para el mensaje de solicitud de la operación CopyFolder, explore la jerarquía del esquema.</span><span class="sxs-lookup"><span data-stu-id="8414f-123">To find other options for the request message of the CopyFolder operation, explore the schema hierarchy.</span></span> <span data-ttu-id="8414f-124">Empiece en el elemento [CopyFolder](copyfolder.md) .</span><span class="sxs-lookup"><span data-stu-id="8414f-124">Start at the [CopyFolder](copyfolder.md) element.</span></span> 
  
## <a name="successful-copyfolder-response"></a><span data-ttu-id="8414f-125">Respuesta CopyFolder correcta</span><span class="sxs-lookup"><span data-stu-id="8414f-125">Successful CopyFolder response</span></span>

### <a name="description"></a><span data-ttu-id="8414f-126">Description</span><span class="sxs-lookup"><span data-stu-id="8414f-126">Description</span></span>

<span data-ttu-id="8414f-127">En el ejemplo siguiente se muestra una respuesta correcta a la solicitud CopyFolder.</span><span class="sxs-lookup"><span data-stu-id="8414f-127">The following example shows a successful response to the CopyFolder request.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="8414f-128">El identificador de la carpeta y la clave de cambio se han abreviado para preservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="8414f-128">The folder ID and the change key have been shortened to preserve readability.</span></span> 
  
### <a name="code"></a><span data-ttu-id="8414f-129">Código</span><span class="sxs-lookup"><span data-stu-id="8414f-129">Code</span></span>

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
    <CopyFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CopyFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:Folder>
              <t:FolderId Id="AS4AUn=" ChangeKey="fsVU4o==" />
            </t:Folder>
          </m:Folders>
        </m:CopyFolderResponseMessage>
      </m:ResponseMessages>
    </CopyFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comment"></a><span data-ttu-id="8414f-130">Comentario</span><span class="sxs-lookup"><span data-stu-id="8414f-130">Comment</span></span>

<span data-ttu-id="8414f-131">El elemento [FolderId](folderid.md) que se devuelve en la respuesta representa la carpeta que se copió en la nueva ubicación de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="8414f-131">The [FolderId](folderid.md) element that is returned in the response represents the folder that was copied in the new folder location.</span></span> 
  
### <a name="response-elements"></a><span data-ttu-id="8414f-132">Elementos de respuesta</span><span class="sxs-lookup"><span data-stu-id="8414f-132">Response elements</span></span>

<span data-ttu-id="8414f-133">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="8414f-133">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="8414f-134">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="8414f-134">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="8414f-135">CopyFolderResponse</span><span class="sxs-lookup"><span data-stu-id="8414f-135">CopyFolderResponse</span></span>](copyfolderresponse.md)
    
- [<span data-ttu-id="8414f-136">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="8414f-136">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="8414f-137">CopyFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="8414f-137">CopyFolderResponseMessage</span></span>](copyfolderresponsemessage.md)
    
- [<span data-ttu-id="8414f-138">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="8414f-138">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="8414f-139">Folders</span><span class="sxs-lookup"><span data-stu-id="8414f-139">Folders</span></span>](folders-ex15websvcsotherref.md)
    
- [<span data-ttu-id="8414f-140">Folder</span><span class="sxs-lookup"><span data-stu-id="8414f-140">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="8414f-141">FolderId</span><span class="sxs-lookup"><span data-stu-id="8414f-141">FolderId</span></span>](folderid.md)
    
<span data-ttu-id="8414f-142">Para buscar otras opciones para el mensaje de respuesta de la operación CopyFolder, explore la jerarquía del esquema.</span><span class="sxs-lookup"><span data-stu-id="8414f-142">To find other options for the response message of the CopyFolder operation, explore the schema hierarchy.</span></span> <span data-ttu-id="8414f-143">Empiece en el elemento [CopyFolderResponse](copyfolderresponse.md) .</span><span class="sxs-lookup"><span data-stu-id="8414f-143">Start at the [CopyFolderResponse](copyfolderresponse.md) element.</span></span> 
  
## <a name="copyfolder-error-response"></a><span data-ttu-id="8414f-144">Respuesta de error de CopyFolder</span><span class="sxs-lookup"><span data-stu-id="8414f-144">CopyFolder error response</span></span>

### <a name="description"></a><span data-ttu-id="8414f-145">Description</span><span class="sxs-lookup"><span data-stu-id="8414f-145">Description</span></span>

<span data-ttu-id="8414f-146">En el ejemplo siguiente se muestra una respuesta de error a una solicitud CopyFolder.</span><span class="sxs-lookup"><span data-stu-id="8414f-146">The following example shows an error response to a CopyFolder request.</span></span> <span data-ttu-id="8414f-147">El error se produjo porque ya existe una carpeta con el mismo nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="8414f-147">The error occurred because a folder with the same display name already exists.</span></span>
  
### <a name="code"></a><span data-ttu-id="8414f-148">Código</span><span class="sxs-lookup"><span data-stu-id="8414f-148">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <CopyFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CopyFolderResponseMessage ResponseClass="Error">
          <m:MessageText>The move or copy operation failed.</m:MessageText>
          <m:ResponseCode>ErrorMoveCopyFailed</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:Folders />
        </m:CopyFolderResponseMessage>
      </m:ResponseMessages>
    </CopyFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a><span data-ttu-id="8414f-149">Elementos de respuesta de error</span><span class="sxs-lookup"><span data-stu-id="8414f-149">Error response elements</span></span>

<span data-ttu-id="8414f-150">Los siguientes elementos se usan en la respuesta de error:</span><span class="sxs-lookup"><span data-stu-id="8414f-150">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="8414f-151">CopyFolderResponse</span><span class="sxs-lookup"><span data-stu-id="8414f-151">CopyFolderResponse</span></span>](copyfolderresponse.md)
    
- [<span data-ttu-id="8414f-152">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="8414f-152">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="8414f-153">CopyFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="8414f-153">CopyFolderResponseMessage</span></span>](copyfolderresponsemessage.md)
    
- [<span data-ttu-id="8414f-154">MessageText</span><span class="sxs-lookup"><span data-stu-id="8414f-154">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="8414f-155">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="8414f-155">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="8414f-156">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="8414f-156">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="8414f-157">Folders</span><span class="sxs-lookup"><span data-stu-id="8414f-157">Folders</span></span>](folders-ex15websvcsotherref.md)
    
<span data-ttu-id="8414f-158">Para buscar otras opciones para el mensaje de respuesta de error de la operación CopyFolder, explore la jerarquía del esquema.</span><span class="sxs-lookup"><span data-stu-id="8414f-158">To find other options for the error response message of the CopyFolder operation, explore the schema hierarchy.</span></span> <span data-ttu-id="8414f-159">Empiece en el elemento [CopyFolderResponse](copyfolderresponse.md) .</span><span class="sxs-lookup"><span data-stu-id="8414f-159">Start at the [CopyFolderResponse](copyfolderresponse.md) element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8414f-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="8414f-160">See also</span></span>

- [<span data-ttu-id="8414f-161">Operación MoveFolder</span><span class="sxs-lookup"><span data-stu-id="8414f-161">MoveFolder operation</span></span>](movefolder-operation.md)
- [<span data-ttu-id="8414f-162">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="8414f-162">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

