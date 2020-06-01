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
ms.lasthandoff: 06/01/2020
ms.locfileid: "44468897"
---
# <a name="copyfolder-operation"></a><span data-ttu-id="61f49-103">Operación CopyFolder</span><span class="sxs-lookup"><span data-stu-id="61f49-103">CopyFolder operation</span></span>

<span data-ttu-id="61f49-104">La operación CopyFolder copia carpetas en un buzón.</span><span class="sxs-lookup"><span data-stu-id="61f49-104">The CopyFolder operation copies folders in a mailbox.</span></span>
  
## <a name="using-the-copyfolder-operation"></a><span data-ttu-id="61f49-105">Uso de la operación CopyFolder</span><span class="sxs-lookup"><span data-stu-id="61f49-105">Using the CopyFolder operation</span></span>

<span data-ttu-id="61f49-106">La operación CopyFolder es similar a la [operación MoveFolder](movefolder-operation.md).</span><span class="sxs-lookup"><span data-stu-id="61f49-106">The CopyFolder operation is similar to the [MoveFolder operation](movefolder-operation.md).</span></span> <span data-ttu-id="61f49-107">Copia las carpetas identificadas y devuelve el **identificador** y la **changekey** de las carpetas que se han copiado.</span><span class="sxs-lookup"><span data-stu-id="61f49-107">It copies identified folders and returns the **Id** and **ChangeKey** of the copied folders.</span></span> 
  
## <a name="copyfolder-request-example"></a><span data-ttu-id="61f49-108">Ejemplo de solicitud CopyFolder</span><span class="sxs-lookup"><span data-stu-id="61f49-108">CopyFolder request example</span></span>

### <a name="description"></a><span data-ttu-id="61f49-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="61f49-109">Description</span></span>

<span data-ttu-id="61f49-110">El siguiente ejemplo de una solicitud CopyFolder muestra cómo copiar carpetas en la carpeta Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="61f49-110">The following example of a CopyFolder request shows how to copy folders into the Inbox folder.</span></span>
  
> [!NOTE]
> <span data-ttu-id="61f49-111">El valor del atributo **ID** del elemento [FolderId](folderid.md) se ha abreviado para facilitar su lectura.</span><span class="sxs-lookup"><span data-stu-id="61f49-111">The value of the **Id** attribute of the [FolderId](folderid.md) element has been shortened for readability.</span></span> 
  
### <a name="code"></a><span data-ttu-id="61f49-112">Código</span><span class="sxs-lookup"><span data-stu-id="61f49-112">Code</span></span>

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

### <a name="comments"></a><span data-ttu-id="61f49-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="61f49-113">Comments</span></span>

<span data-ttu-id="61f49-114">Las carpetas pueden identificarse mediante el elemento [DistinguishedFolderId](distinguishedfolderid.md) o el elemento [FolderId](folderid.md) para su uso en los elementos [ToFolderId](tofolderid.md) o [FolderIds](folderids.md) .</span><span class="sxs-lookup"><span data-stu-id="61f49-114">Folders can be identified by either the [DistinguishedFolderId](distinguishedfolderid.md) element or the [FolderId](folderid.md) element for use in either the [ToFolderId](tofolderid.md) or the [FolderIds](folderids.md) elements.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="61f49-115">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="61f49-115">Request elements</span></span>

<span data-ttu-id="61f49-116">Los siguientes elementos se usan en la solicitud:</span><span class="sxs-lookup"><span data-stu-id="61f49-116">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="61f49-117">CopyFolder</span><span class="sxs-lookup"><span data-stu-id="61f49-117">CopyFolder</span></span>](copyfolder.md)
    
- [<span data-ttu-id="61f49-118">ToFolderId</span><span class="sxs-lookup"><span data-stu-id="61f49-118">ToFolderId</span></span>](tofolderid.md)
    
- [<span data-ttu-id="61f49-119">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="61f49-119">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="61f49-120">FolderIds</span><span class="sxs-lookup"><span data-stu-id="61f49-120">FolderIds</span></span>](folderids.md)
    
- [<span data-ttu-id="61f49-121">FolderId</span><span class="sxs-lookup"><span data-stu-id="61f49-121">FolderId</span></span>](folderid.md)
    
> [!NOTE]
> <span data-ttu-id="61f49-122">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="61f49-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
<span data-ttu-id="61f49-123">Para buscar otras opciones para el mensaje de solicitud de la operación CopyFolder, explore la jerarquía del esquema.</span><span class="sxs-lookup"><span data-stu-id="61f49-123">To find other options for the request message of the CopyFolder operation, explore the schema hierarchy.</span></span> <span data-ttu-id="61f49-124">Empiece en el elemento [CopyFolder](copyfolder.md) .</span><span class="sxs-lookup"><span data-stu-id="61f49-124">Start at the [CopyFolder](copyfolder.md) element.</span></span> 
  
## <a name="successful-copyfolder-response"></a><span data-ttu-id="61f49-125">Respuesta CopyFolder correcta</span><span class="sxs-lookup"><span data-stu-id="61f49-125">Successful CopyFolder response</span></span>

### <a name="description"></a><span data-ttu-id="61f49-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="61f49-126">Description</span></span>

<span data-ttu-id="61f49-127">En el ejemplo siguiente se muestra una respuesta correcta a la solicitud CopyFolder.</span><span class="sxs-lookup"><span data-stu-id="61f49-127">The following example shows a successful response to the CopyFolder request.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="61f49-128">El identificador de la carpeta y la clave de cambio se han abreviado para preservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="61f49-128">The folder ID and the change key have been shortened to preserve readability.</span></span> 
  
### <a name="code"></a><span data-ttu-id="61f49-129">Código</span><span class="sxs-lookup"><span data-stu-id="61f49-129">Code</span></span>

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

### <a name="comment"></a><span data-ttu-id="61f49-130">Comentario</span><span class="sxs-lookup"><span data-stu-id="61f49-130">Comment</span></span>

<span data-ttu-id="61f49-131">El elemento [FolderId](folderid.md) que se devuelve en la respuesta representa la carpeta que se copió en la nueva ubicación de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="61f49-131">The [FolderId](folderid.md) element that is returned in the response represents the folder that was copied in the new folder location.</span></span> 
  
### <a name="response-elements"></a><span data-ttu-id="61f49-132">Elementos de respuesta</span><span class="sxs-lookup"><span data-stu-id="61f49-132">Response elements</span></span>

<span data-ttu-id="61f49-133">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="61f49-133">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="61f49-134">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="61f49-134">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="61f49-135">CopyFolderResponse</span><span class="sxs-lookup"><span data-stu-id="61f49-135">CopyFolderResponse</span></span>](copyfolderresponse.md)
    
- [<span data-ttu-id="61f49-136">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="61f49-136">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="61f49-137">CopyFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="61f49-137">CopyFolderResponseMessage</span></span>](copyfolderresponsemessage.md)
    
- [<span data-ttu-id="61f49-138">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="61f49-138">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="61f49-139">Folders</span><span class="sxs-lookup"><span data-stu-id="61f49-139">Folders</span></span>](folders-ex15websvcsotherref.md)
    
- [<span data-ttu-id="61f49-140">Folder</span><span class="sxs-lookup"><span data-stu-id="61f49-140">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="61f49-141">FolderId</span><span class="sxs-lookup"><span data-stu-id="61f49-141">FolderId</span></span>](folderid.md)
    
<span data-ttu-id="61f49-142">Para buscar otras opciones para el mensaje de respuesta de la operación CopyFolder, explore la jerarquía del esquema.</span><span class="sxs-lookup"><span data-stu-id="61f49-142">To find other options for the response message of the CopyFolder operation, explore the schema hierarchy.</span></span> <span data-ttu-id="61f49-143">Empiece en el elemento [CopyFolderResponse](copyfolderresponse.md) .</span><span class="sxs-lookup"><span data-stu-id="61f49-143">Start at the [CopyFolderResponse](copyfolderresponse.md) element.</span></span> 
  
## <a name="copyfolder-error-response"></a><span data-ttu-id="61f49-144">Respuesta de error de CopyFolder</span><span class="sxs-lookup"><span data-stu-id="61f49-144">CopyFolder error response</span></span>

### <a name="description"></a><span data-ttu-id="61f49-145">Descripción</span><span class="sxs-lookup"><span data-stu-id="61f49-145">Description</span></span>

<span data-ttu-id="61f49-146">En el ejemplo siguiente se muestra una respuesta de error a una solicitud CopyFolder.</span><span class="sxs-lookup"><span data-stu-id="61f49-146">The following example shows an error response to a CopyFolder request.</span></span> <span data-ttu-id="61f49-147">El error se produjo porque ya existe una carpeta con el mismo nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="61f49-147">The error occurred because a folder with the same display name already exists.</span></span>
  
### <a name="code"></a><span data-ttu-id="61f49-148">Código</span><span class="sxs-lookup"><span data-stu-id="61f49-148">Code</span></span>

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

### <a name="error-response-elements"></a><span data-ttu-id="61f49-149">Elementos de respuesta de error</span><span class="sxs-lookup"><span data-stu-id="61f49-149">Error response elements</span></span>

<span data-ttu-id="61f49-150">Los siguientes elementos se usan en la respuesta de error:</span><span class="sxs-lookup"><span data-stu-id="61f49-150">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="61f49-151">CopyFolderResponse</span><span class="sxs-lookup"><span data-stu-id="61f49-151">CopyFolderResponse</span></span>](copyfolderresponse.md)
    
- [<span data-ttu-id="61f49-152">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="61f49-152">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="61f49-153">CopyFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="61f49-153">CopyFolderResponseMessage</span></span>](copyfolderresponsemessage.md)
    
- [<span data-ttu-id="61f49-154">MessageText</span><span class="sxs-lookup"><span data-stu-id="61f49-154">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="61f49-155">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="61f49-155">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="61f49-156">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="61f49-156">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="61f49-157">Folders</span><span class="sxs-lookup"><span data-stu-id="61f49-157">Folders</span></span>](folders-ex15websvcsotherref.md)
    
<span data-ttu-id="61f49-158">Para buscar otras opciones para el mensaje de respuesta de error de la operación CopyFolder, explore la jerarquía del esquema.</span><span class="sxs-lookup"><span data-stu-id="61f49-158">To find other options for the error response message of the CopyFolder operation, explore the schema hierarchy.</span></span> <span data-ttu-id="61f49-159">Empiece en el elemento [CopyFolderResponse](copyfolderresponse.md) .</span><span class="sxs-lookup"><span data-stu-id="61f49-159">Start at the [CopyFolderResponse](copyfolderresponse.md) element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="61f49-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="61f49-160">See also</span></span>

- [<span data-ttu-id="61f49-161">Operación MoveFolder</span><span class="sxs-lookup"><span data-stu-id="61f49-161">MoveFolder operation</span></span>](movefolder-operation.md)
- [<span data-ttu-id="61f49-162">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="61f49-162">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

