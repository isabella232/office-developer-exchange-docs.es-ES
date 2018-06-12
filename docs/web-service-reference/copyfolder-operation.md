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
description: La operación CopyFolder copia las carpetas en un buzón de correo.
ms.openlocfilehash: a83444ff0927a3c8fe075c79d44d02357a737773
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763893"
---
# <a name="copyfolder-operation"></a><span data-ttu-id="03e51-103">Operación CopyFolder</span><span class="sxs-lookup"><span data-stu-id="03e51-103">CopyFolder operation</span></span>

<span data-ttu-id="03e51-104">La operación CopyFolder copia las carpetas en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="03e51-104">The CopyFolder operation copies folders in a mailbox.</span></span>
  
## <a name="using-the-copyfolder-operation"></a><span data-ttu-id="03e51-105">Mediante la operación CopyFolder</span><span class="sxs-lookup"><span data-stu-id="03e51-105">Using the CopyFolder operation</span></span>

<span data-ttu-id="03e51-106">La operación CopyFolder es similar a la [operación MoveFolder](movefolder-operation.md).</span><span class="sxs-lookup"><span data-stu-id="03e51-106">The CopyFolder operation is similar to the [MoveFolder operation](movefolder-operation.md).</span></span> <span data-ttu-id="03e51-107">Copia carpetas identificadas y devuelve el **identificador** y **ChangeKey** de las carpetas copiadas.</span><span class="sxs-lookup"><span data-stu-id="03e51-107">It copies identified folders and returns the **Id** and **ChangeKey** of the copied folders.</span></span> 
  
## <a name="copyfolder-request-example"></a><span data-ttu-id="03e51-108">Ejemplo de solicitud CopyFolder</span><span class="sxs-lookup"><span data-stu-id="03e51-108">CopyFolder request example</span></span>

### <a name="description"></a><span data-ttu-id="03e51-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="03e51-109">Description</span></span>

<span data-ttu-id="03e51-110">El siguiente ejemplo de una solicitud de CopyFolder muestra cómo copiar carpetas en la carpeta Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="03e51-110">The following example of a CopyFolder request shows how to copy folders into the Inbox folder.</span></span>
  
> [!NOTE]
> <span data-ttu-id="03e51-111">El valor del atributo **Id** del elemento [FolderId](folderid.md) se ha acortado para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="03e51-111">The value of the **Id** attribute of the [FolderId](folderid.md) element has been shortened for readability.</span></span> 
  
### <a name="code"></a><span data-ttu-id="03e51-112">Código</span><span class="sxs-lookup"><span data-stu-id="03e51-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CopyFolder xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a><span data-ttu-id="03e51-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="03e51-113">Comments</span></span>

<span data-ttu-id="03e51-114">Las carpetas se pueden identificar por el elemento [DistinguishedFolderId](distinguishedfolderid.md) o el elemento [FolderId](folderid.md) para su uso en ya sea el [ToFolderId](tofolderid.md) o los elementos de [FolderIds](folderids.md) .</span><span class="sxs-lookup"><span data-stu-id="03e51-114">Folders can be identified by either the [DistinguishedFolderId](distinguishedfolderid.md) element or the [FolderId](folderid.md) element for use in either the [ToFolderId](tofolderid.md) or the [FolderIds](folderids.md) elements.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="03e51-115">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="03e51-115">Request elements</span></span>

<span data-ttu-id="03e51-116">En la solicitud se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="03e51-116">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="03e51-117">CopyFolder</span><span class="sxs-lookup"><span data-stu-id="03e51-117">CopyFolder</span></span>](copyfolder.md)
    
- [<span data-ttu-id="03e51-118">ToFolderId</span><span class="sxs-lookup"><span data-stu-id="03e51-118">ToFolderId</span></span>](tofolderid.md)
    
- [<span data-ttu-id="03e51-119">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="03e51-119">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="03e51-120">FolderIds</span><span class="sxs-lookup"><span data-stu-id="03e51-120">FolderIds</span></span>](folderids.md)
    
- [<span data-ttu-id="03e51-121">FolderId</span><span class="sxs-lookup"><span data-stu-id="03e51-121">FolderId</span></span>](folderid.md)
    
> [!NOTE]
> <span data-ttu-id="03e51-122">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="03e51-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
<span data-ttu-id="03e51-123">Para buscar otras opciones para el mensaje de solicitud de la operación CopyFolder, explore la jerarquía de esquema.</span><span class="sxs-lookup"><span data-stu-id="03e51-123">To find other options for the request message of the CopyFolder operation, explore the schema hierarchy.</span></span> <span data-ttu-id="03e51-124">Comenzar en el elemento de [CopyFolder](copyfolder.md) .</span><span class="sxs-lookup"><span data-stu-id="03e51-124">Start at the [CopyFolder](copyfolder.md) element.</span></span> 
  
## <a name="successful-copyfolder-response"></a><span data-ttu-id="03e51-125">Respuesta es correcta CopyFolder</span><span class="sxs-lookup"><span data-stu-id="03e51-125">Successful CopyFolder response</span></span>

### <a name="description"></a><span data-ttu-id="03e51-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="03e51-126">Description</span></span>

<span data-ttu-id="03e51-127">En el ejemplo siguiente se muestra una respuesta correcta a la solicitud de CopyFolder.</span><span class="sxs-lookup"><span data-stu-id="03e51-127">The following example shows a successful response to the CopyFolder request.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="03e51-128">El identificador de la carpeta y la clave de cambio se han abreviado para conservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="03e51-128">The folder ID and the change key have been shortened to preserve readability.</span></span> 
  
### <a name="code"></a><span data-ttu-id="03e51-129">Código</span><span class="sxs-lookup"><span data-stu-id="03e51-129">Code</span></span>

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
    <CopyFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comment"></a><span data-ttu-id="03e51-130">Comment</span><span class="sxs-lookup"><span data-stu-id="03e51-130">Comment</span></span>

<span data-ttu-id="03e51-131">El elemento [FolderId](folderid.md) que se devuelve en la respuesta que representa la carpeta que se ha copiado en la nueva ubicación de carpeta.</span><span class="sxs-lookup"><span data-stu-id="03e51-131">The [FolderId](folderid.md) element that is returned in the response represents the folder that was copied in the new folder location.</span></span> 
  
### <a name="response-elements"></a><span data-ttu-id="03e51-132">Elementos de respuesta</span><span class="sxs-lookup"><span data-stu-id="03e51-132">Response elements</span></span>

<span data-ttu-id="03e51-133">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="03e51-133">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="03e51-134">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="03e51-134">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="03e51-135">CopyFolderResponse</span><span class="sxs-lookup"><span data-stu-id="03e51-135">CopyFolderResponse</span></span>](copyfolderresponse.md)
    
- [<span data-ttu-id="03e51-136">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="03e51-136">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="03e51-137">CopyFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="03e51-137">CopyFolderResponseMessage</span></span>](copyfolderresponsemessage.md)
    
- [<span data-ttu-id="03e51-138">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="03e51-138">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="03e51-139">Carpetas</span><span class="sxs-lookup"><span data-stu-id="03e51-139">Folders</span></span>](folders-ex15websvcsotherref.md)
    
- [<span data-ttu-id="03e51-140">Folder</span><span class="sxs-lookup"><span data-stu-id="03e51-140">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="03e51-141">FolderId</span><span class="sxs-lookup"><span data-stu-id="03e51-141">FolderId</span></span>](folderid.md)
    
<span data-ttu-id="03e51-142">Para buscar otras opciones para el mensaje de respuesta de la operación CopyFolder, explore la jerarquía de esquema.</span><span class="sxs-lookup"><span data-stu-id="03e51-142">To find other options for the response message of the CopyFolder operation, explore the schema hierarchy.</span></span> <span data-ttu-id="03e51-143">Comenzar en el elemento de [CopyFolderResponse](copyfolderresponse.md) .</span><span class="sxs-lookup"><span data-stu-id="03e51-143">Start at the [CopyFolderResponse](copyfolderresponse.md) element.</span></span> 
  
## <a name="copyfolder-error-response"></a><span data-ttu-id="03e51-144">Respuesta de error CopyFolder</span><span class="sxs-lookup"><span data-stu-id="03e51-144">CopyFolder error response</span></span>

### <a name="description"></a><span data-ttu-id="03e51-145">Descripción</span><span class="sxs-lookup"><span data-stu-id="03e51-145">Description</span></span>

<span data-ttu-id="03e51-146">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de CopyFolder.</span><span class="sxs-lookup"><span data-stu-id="03e51-146">The following example shows an error response to a CopyFolder request.</span></span> <span data-ttu-id="03e51-147">Se produjo el error debido a que ya existe una carpeta con el mismo nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="03e51-147">The error occurred because a folder with the same display name already exists.</span></span>
  
### <a name="code"></a><span data-ttu-id="03e51-148">Código</span><span class="sxs-lookup"><span data-stu-id="03e51-148">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <CopyFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="error-response-elements"></a><span data-ttu-id="03e51-149">Elementos de respuesta de error</span><span class="sxs-lookup"><span data-stu-id="03e51-149">Error response elements</span></span>

<span data-ttu-id="03e51-150">En la respuesta de error, se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="03e51-150">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="03e51-151">CopyFolderResponse</span><span class="sxs-lookup"><span data-stu-id="03e51-151">CopyFolderResponse</span></span>](copyfolderresponse.md)
    
- [<span data-ttu-id="03e51-152">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="03e51-152">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="03e51-153">CopyFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="03e51-153">CopyFolderResponseMessage</span></span>](copyfolderresponsemessage.md)
    
- [<span data-ttu-id="03e51-154">MessageText</span><span class="sxs-lookup"><span data-stu-id="03e51-154">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="03e51-155">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="03e51-155">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="03e51-156">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="03e51-156">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="03e51-157">Carpetas</span><span class="sxs-lookup"><span data-stu-id="03e51-157">Folders</span></span>](folders-ex15websvcsotherref.md)
    
<span data-ttu-id="03e51-158">Para buscar otras opciones para el mensaje de respuesta de error de la operación CopyFolder, explore la jerarquía de esquema.</span><span class="sxs-lookup"><span data-stu-id="03e51-158">To find other options for the error response message of the CopyFolder operation, explore the schema hierarchy.</span></span> <span data-ttu-id="03e51-159">Comenzar en el elemento de [CopyFolderResponse](copyfolderresponse.md) .</span><span class="sxs-lookup"><span data-stu-id="03e51-159">Start at the [CopyFolderResponse](copyfolderresponse.md) element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="03e51-160">Ver también</span><span class="sxs-lookup"><span data-stu-id="03e51-160">See also</span></span>

- [<span data-ttu-id="03e51-161">Operación MoveFolder</span><span class="sxs-lookup"><span data-stu-id="03e51-161">MoveFolder operation</span></span>](movefolder-operation.md)
- [<span data-ttu-id="03e51-162">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="03e51-162">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

