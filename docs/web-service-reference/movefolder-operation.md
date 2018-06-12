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
description: La operación MoveFolder mueve las carpetas de una carpeta especificada y coloca en otra carpeta.
ms.openlocfilehash: 5da6929f11ce9ba74db190db6d799f25974d2192
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836490"
---
# <a name="movefolder-operation"></a><span data-ttu-id="13646-103">Operación MoveFolder</span><span class="sxs-lookup"><span data-stu-id="13646-103">MoveFolder operation</span></span>

<span data-ttu-id="13646-104">La operación MoveFolder mueve las carpetas de una carpeta especificada y coloca en otra carpeta.</span><span class="sxs-lookup"><span data-stu-id="13646-104">The MoveFolder operation moves folders from a specified folder and puts them in another folder.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="13646-105">Notas</span><span class="sxs-lookup"><span data-stu-id="13646-105">Remarks</span></span>

<span data-ttu-id="13646-106">La operación MoveFolder es similar a la operación CopyFolder.</span><span class="sxs-lookup"><span data-stu-id="13646-106">The MoveFolder operation is similar to the CopyFolder operation.</span></span> <span data-ttu-id="13646-107">No se puede mover carpetas distintivos.</span><span class="sxs-lookup"><span data-stu-id="13646-107">You cannot move distinguished folders.</span></span> <span data-ttu-id="13646-108">Puede mover varias carpetas a la vez a la carpeta de destino.</span><span class="sxs-lookup"><span data-stu-id="13646-108">You can move multiple folders at one time to the destination folder.</span></span>
  
## <a name="movefolder-request-example"></a><span data-ttu-id="13646-109">Ejemplo de solicitud MoveFolder</span><span class="sxs-lookup"><span data-stu-id="13646-109">MoveFolder request example</span></span>

### <a name="description"></a><span data-ttu-id="13646-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="13646-110">Description</span></span>

<span data-ttu-id="13646-111">El siguiente ejemplo de una solicitud de MoveFolder muestra cómo formar una solicitud para mover una carpeta identificada por el [FolderId](folderid.md) y poner la carpeta en la carpeta distintivo (DN) de correo electrónico no deseado.</span><span class="sxs-lookup"><span data-stu-id="13646-111">The following example of a MoveFolder request shows how to form a request to move a folder identified by the [FolderId](folderid.md) and put the folder in the Junk E-mail distinguished folder.</span></span> 
  
### <a name="code"></a><span data-ttu-id="13646-112">Código</span><span class="sxs-lookup"><span data-stu-id="13646-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <MoveFolder xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a><span data-ttu-id="13646-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="13646-113">Comments</span></span>

> [!NOTE]
> <span data-ttu-id="13646-114">El valor del atributo ID del elemento [FolderId](folderid.md) se ha acortado para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="13646-114">The value of the ID attribute of the [FolderId](folderid.md) element has been shortened for readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="13646-115">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="13646-115">Request elements</span></span>

<span data-ttu-id="13646-116">Esta solicitud MoveFolder incluye los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="13646-116">This MoveFolder request includes the following elements:</span></span>
  
- [<span data-ttu-id="13646-117">MoveFolder</span><span class="sxs-lookup"><span data-stu-id="13646-117">MoveFolder</span></span>](movefolder.md)
    
- [<span data-ttu-id="13646-118">ToFolderId</span><span class="sxs-lookup"><span data-stu-id="13646-118">ToFolderId</span></span>](tofolderid.md)
    
- [<span data-ttu-id="13646-119">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="13646-119">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="13646-120">FolderIds</span><span class="sxs-lookup"><span data-stu-id="13646-120">FolderIds</span></span>](folderids.md)
    
- [<span data-ttu-id="13646-121">FolderId</span><span class="sxs-lookup"><span data-stu-id="13646-121">FolderId</span></span>](folderid.md)
    
<span data-ttu-id="13646-122">Consulte el esquema para los elementos adicionales que puede usar para realizar una solicitud MoveFolder.</span><span class="sxs-lookup"><span data-stu-id="13646-122">See the schema for additional elements that you can use to form a MoveFolder request.</span></span>
  
> [!NOTE]
> <span data-ttu-id="13646-123">La ubicación predeterminada del esquema se encuentra en el directorio virtual de EWS en el equipo que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="13646-123">The default location of the schema is in the EWS virtual directory on the computer that has the Client Access server role installed.</span></span> 
  
## <a name="successful-movefolder-response-example"></a><span data-ttu-id="13646-124">Ejemplo de respuesta correcta de MoveFolder</span><span class="sxs-lookup"><span data-stu-id="13646-124">Successful MoveFolder response example</span></span>

### <a name="description"></a><span data-ttu-id="13646-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="13646-125">Description</span></span>

<span data-ttu-id="13646-126">En el ejemplo siguiente se muestra una respuesta correcta a la solicitud de MoveFolder.</span><span class="sxs-lookup"><span data-stu-id="13646-126">The following example shows a successful response to the MoveFolder request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="13646-127">Código</span><span class="sxs-lookup"><span data-stu-id="13646-127">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <MoveFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a><span data-ttu-id="13646-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="13646-128">Comments</span></span>

> [!NOTE]
> <span data-ttu-id="13646-129">El identificador de la carpeta y la clave de cambio se han abreviado para conservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="13646-129">The folder ID and the change key have been shortened to preserve readability.</span></span> 
  
<span data-ttu-id="13646-130">El ID de carpeta que se devuelve en la respuesta representa la carpeta que se ha movido a la nueva ubicación de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="13646-130">The FolderId that is returned in the response represents the folder that was moved to the new the folder location.</span></span>
  
### <a name="response-elements"></a><span data-ttu-id="13646-131">Elementos de respuesta</span><span class="sxs-lookup"><span data-stu-id="13646-131">Response elements</span></span>

<span data-ttu-id="13646-132">La respuesta MoveFolder incluye los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="13646-132">The MoveFolder response includes the following elements:</span></span>
  
- [<span data-ttu-id="13646-133">MoveFolderResponse</span><span class="sxs-lookup"><span data-stu-id="13646-133">MoveFolderResponse</span></span>](movefolderresponse.md)
    
- [<span data-ttu-id="13646-134">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="13646-134">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="13646-135">MoveFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="13646-135">MoveFolderResponseMessage</span></span>](movefolderresponsemessage.md)
    
- [<span data-ttu-id="13646-136">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="13646-136">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="13646-137">Carpetas</span><span class="sxs-lookup"><span data-stu-id="13646-137">Folders</span></span>](folders-ex15websvcsotherref.md)
    
- [<span data-ttu-id="13646-138">Folder</span><span class="sxs-lookup"><span data-stu-id="13646-138">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="13646-139">FolderId</span><span class="sxs-lookup"><span data-stu-id="13646-139">FolderId</span></span>](folderid.md)
    
## <a name="movefolder-error-response-example"></a><span data-ttu-id="13646-140">Ejemplo de respuesta de MoveFolder Error</span><span class="sxs-lookup"><span data-stu-id="13646-140">MoveFolder Error response example</span></span>

### <a name="description"></a><span data-ttu-id="13646-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="13646-141">Description</span></span>

<span data-ttu-id="13646-142">En el ejemplo siguiente se muestra una respuesta de error que se produce cuando se intenta mover una carpeta distintivo.</span><span class="sxs-lookup"><span data-stu-id="13646-142">The following example shows an error response that occurs when you try to move a distinguished folder.</span></span>
  
### <a name="code"></a><span data-ttu-id="13646-143">Código</span><span class="sxs-lookup"><span data-stu-id="13646-143">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
                 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                 xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <MoveFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="error-response-elements"></a><span data-ttu-id="13646-144">Elementos de respuesta de error</span><span class="sxs-lookup"><span data-stu-id="13646-144">Error response elements</span></span>

<span data-ttu-id="13646-145">La respuesta de error MoveFolder incluye los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="13646-145">The MoveFolder error response includes the following elements:</span></span>
  
- [<span data-ttu-id="13646-146">MoveFolderResponse</span><span class="sxs-lookup"><span data-stu-id="13646-146">MoveFolderResponse</span></span>](movefolderresponse.md)
    
- [<span data-ttu-id="13646-147">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="13646-147">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="13646-148">MoveFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="13646-148">MoveFolderResponseMessage</span></span>](movefolderresponsemessage.md)
    
- [<span data-ttu-id="13646-149">MessageText</span><span class="sxs-lookup"><span data-stu-id="13646-149">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="13646-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="13646-150">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="13646-151">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="13646-151">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="13646-152">Carpetas</span><span class="sxs-lookup"><span data-stu-id="13646-152">Folders</span></span>](folders-ex15websvcsotherref.md)
    
## <a name="see-also"></a><span data-ttu-id="13646-153">Ver también</span><span class="sxs-lookup"><span data-stu-id="13646-153">See also</span></span>



[<span data-ttu-id="13646-154">Operación CopyFolder</span><span class="sxs-lookup"><span data-stu-id="13646-154">CopyFolder operation</span></span>](copyfolder-operation.md)

