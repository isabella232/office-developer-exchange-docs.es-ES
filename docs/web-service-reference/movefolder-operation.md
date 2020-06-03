---
title: Operación MoveFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MoveFolder
api_type:
- schema
ms.assetid: c7233966-6c87-4a14-8156-b1610760176d
description: La operación MoveFolder mueve carpetas de una carpeta especificada y las coloca en otra carpeta.
ms.openlocfilehash: dc572130ca3b2f2b152abbb4a8b68cc6f67790e8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460585"
---
# <a name="movefolder-operation"></a><span data-ttu-id="062a8-103">Operación MoveFolder</span><span class="sxs-lookup"><span data-stu-id="062a8-103">MoveFolder operation</span></span>

<span data-ttu-id="062a8-104">La operación MoveFolder mueve carpetas de una carpeta especificada y las coloca en otra carpeta.</span><span class="sxs-lookup"><span data-stu-id="062a8-104">The MoveFolder operation moves folders from a specified folder and puts them in another folder.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="062a8-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="062a8-105">Remarks</span></span>

<span data-ttu-id="062a8-106">La operación MoveFolder es similar a la operación CopyFolder.</span><span class="sxs-lookup"><span data-stu-id="062a8-106">The MoveFolder operation is similar to the CopyFolder operation.</span></span> <span data-ttu-id="062a8-107">No se pueden mover las carpetas distintivas.</span><span class="sxs-lookup"><span data-stu-id="062a8-107">You cannot move distinguished folders.</span></span> <span data-ttu-id="062a8-108">Puede mover varias carpetas al mismo tiempo a la carpeta de destino.</span><span class="sxs-lookup"><span data-stu-id="062a8-108">You can move multiple folders at one time to the destination folder.</span></span>
  
## <a name="movefolder-request-example"></a><span data-ttu-id="062a8-109">Ejemplo de solicitud MoveFolder</span><span class="sxs-lookup"><span data-stu-id="062a8-109">MoveFolder request example</span></span>

### <a name="description"></a><span data-ttu-id="062a8-110">Description</span><span class="sxs-lookup"><span data-stu-id="062a8-110">Description</span></span>

<span data-ttu-id="062a8-111">En el siguiente ejemplo de una solicitud de MoveFolder se muestra cómo crear una solicitud para mover una carpeta identificada por el [FolderId](folderid.md) y colocar la carpeta en la carpeta completa de correo no deseado.</span><span class="sxs-lookup"><span data-stu-id="062a8-111">The following example of a MoveFolder request shows how to form a request to move a folder identified by the [FolderId](folderid.md) and put the folder in the Junk E-mail distinguished folder.</span></span> 
  
### <a name="code"></a><span data-ttu-id="062a8-112">Código</span><span class="sxs-lookup"><span data-stu-id="062a8-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <MoveFolder xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ToFolderId>
        <t:DistinguishedFolderId Id="junkemail"/>
      </ToFolderId>
      <FolderIds>
        <t:FolderId Id="AScAc"/>
      </FolderIds>
    </MoveFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="062a8-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="062a8-113">Comments</span></span>

> [!NOTE]
> <span data-ttu-id="062a8-114">El valor del atributo ID del elemento [FolderId](folderid.md) se ha abreviado para facilitar su lectura.</span><span class="sxs-lookup"><span data-stu-id="062a8-114">The value of the ID attribute of the [FolderId](folderid.md) element has been shortened for readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="062a8-115">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="062a8-115">Request elements</span></span>

<span data-ttu-id="062a8-116">Esta solicitud de MoveFolder incluye los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="062a8-116">This MoveFolder request includes the following elements:</span></span>
  
- [<span data-ttu-id="062a8-117">MoveFolder</span><span class="sxs-lookup"><span data-stu-id="062a8-117">MoveFolder</span></span>](movefolder.md)
    
- [<span data-ttu-id="062a8-118">ToFolderId</span><span class="sxs-lookup"><span data-stu-id="062a8-118">ToFolderId</span></span>](tofolderid.md)
    
- [<span data-ttu-id="062a8-119">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="062a8-119">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="062a8-120">FolderIds</span><span class="sxs-lookup"><span data-stu-id="062a8-120">FolderIds</span></span>](folderids.md)
    
- [<span data-ttu-id="062a8-121">FolderId</span><span class="sxs-lookup"><span data-stu-id="062a8-121">FolderId</span></span>](folderid.md)
    
<span data-ttu-id="062a8-122">Vea el esquema para ver los elementos adicionales que puede usar para formar una solicitud de MoveFolder.</span><span class="sxs-lookup"><span data-stu-id="062a8-122">See the schema for additional elements that you can use to form a MoveFolder request.</span></span>
  
> [!NOTE]
> <span data-ttu-id="062a8-123">La ubicación predeterminada del esquema está en el directorio virtual de EWS en el equipo que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="062a8-123">The default location of the schema is in the EWS virtual directory on the computer that has the Client Access server role installed.</span></span> 
  
## <a name="successful-movefolder-response-example"></a><span data-ttu-id="062a8-124">Ejemplo de respuesta MoveFolder correcta</span><span class="sxs-lookup"><span data-stu-id="062a8-124">Successful MoveFolder response example</span></span>

### <a name="description"></a><span data-ttu-id="062a8-125">Description</span><span class="sxs-lookup"><span data-stu-id="062a8-125">Description</span></span>

<span data-ttu-id="062a8-126">En el ejemplo siguiente se muestra una respuesta correcta a la solicitud MoveFolder.</span><span class="sxs-lookup"><span data-stu-id="062a8-126">The following example shows a successful response to the MoveFolder request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="062a8-127">Código</span><span class="sxs-lookup"><span data-stu-id="062a8-127">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <MoveFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:MoveFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:Folder>
              <t:FolderId Id="AAAlAFV" ChangeKey="AQAAAB" />
            </t:Folder>
          </m:Folders>
        </m:MoveFolderResponseMessage>
      </m:ResponseMessages>
    </MoveFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="062a8-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="062a8-128">Comments</span></span>

> [!NOTE]
> <span data-ttu-id="062a8-129">El identificador de la carpeta y la clave de cambio se han abreviado para preservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="062a8-129">The folder ID and the change key have been shortened to preserve readability.</span></span> 
  
<span data-ttu-id="062a8-130">La FolderId que se devuelve en la respuesta representa la carpeta que se movió a la nueva ubicación de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="062a8-130">The FolderId that is returned in the response represents the folder that was moved to the new the folder location.</span></span>
  
### <a name="response-elements"></a><span data-ttu-id="062a8-131">Elementos de respuesta</span><span class="sxs-lookup"><span data-stu-id="062a8-131">Response elements</span></span>

<span data-ttu-id="062a8-132">La respuesta MoveFolder incluye los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="062a8-132">The MoveFolder response includes the following elements:</span></span>
  
- [<span data-ttu-id="062a8-133">MoveFolderResponse</span><span class="sxs-lookup"><span data-stu-id="062a8-133">MoveFolderResponse</span></span>](movefolderresponse.md)
    
- [<span data-ttu-id="062a8-134">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="062a8-134">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="062a8-135">MoveFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="062a8-135">MoveFolderResponseMessage</span></span>](movefolderresponsemessage.md)
    
- [<span data-ttu-id="062a8-136">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="062a8-136">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="062a8-137">Folders</span><span class="sxs-lookup"><span data-stu-id="062a8-137">Folders</span></span>](folders-ex15websvcsotherref.md)
    
- [<span data-ttu-id="062a8-138">Folder</span><span class="sxs-lookup"><span data-stu-id="062a8-138">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="062a8-139">FolderId</span><span class="sxs-lookup"><span data-stu-id="062a8-139">FolderId</span></span>](folderid.md)
    
## <a name="movefolder-error-response-example"></a><span data-ttu-id="062a8-140">Ejemplo de respuesta de error MoveFolder</span><span class="sxs-lookup"><span data-stu-id="062a8-140">MoveFolder Error response example</span></span>

### <a name="description"></a><span data-ttu-id="062a8-141">Description</span><span class="sxs-lookup"><span data-stu-id="062a8-141">Description</span></span>

<span data-ttu-id="062a8-142">En el ejemplo siguiente se muestra una respuesta de error que se produce al intentar mover una carpeta distintiva.</span><span class="sxs-lookup"><span data-stu-id="062a8-142">The following example shows an error response that occurs when you try to move a distinguished folder.</span></span>
  
### <a name="code"></a><span data-ttu-id="062a8-143">Código</span><span class="sxs-lookup"><span data-stu-id="062a8-143">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
                 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                 xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <MoveFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:MoveFolderResponseMessage ResponseClass="Error">
          <m:MessageText>Cannot move distinguished folder.</m:MessageText>
          <m:ResponseCode>ErrorMoveDistinguishedFolder</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:Folders />
        </m:MoveFolderResponseMessage>
      </m:ResponseMessages>
    </MoveFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a><span data-ttu-id="062a8-144">Elementos de respuesta de error</span><span class="sxs-lookup"><span data-stu-id="062a8-144">Error response elements</span></span>

<span data-ttu-id="062a8-145">La respuesta de error MoveFolder incluye los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="062a8-145">The MoveFolder error response includes the following elements:</span></span>
  
- [<span data-ttu-id="062a8-146">MoveFolderResponse</span><span class="sxs-lookup"><span data-stu-id="062a8-146">MoveFolderResponse</span></span>](movefolderresponse.md)
    
- [<span data-ttu-id="062a8-147">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="062a8-147">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="062a8-148">MoveFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="062a8-148">MoveFolderResponseMessage</span></span>](movefolderresponsemessage.md)
    
- [<span data-ttu-id="062a8-149">MessageText</span><span class="sxs-lookup"><span data-stu-id="062a8-149">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="062a8-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="062a8-150">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="062a8-151">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="062a8-151">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="062a8-152">Folders</span><span class="sxs-lookup"><span data-stu-id="062a8-152">Folders</span></span>](folders-ex15websvcsotherref.md)
    
## <a name="see-also"></a><span data-ttu-id="062a8-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="062a8-153">See also</span></span>



[<span data-ttu-id="062a8-154">Operación CopyFolder</span><span class="sxs-lookup"><span data-stu-id="062a8-154">CopyFolder operation</span></span>](copyfolder-operation.md)

