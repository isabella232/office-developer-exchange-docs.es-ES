---
title: Operación EmptyFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 98161486-e2f2-480f-8d5d-708ba81b208a
description: La operación EmptyFolder vacía carpetas en un buzón. Opcionalmente, esta operación permite eliminar las subcarpetas de la carpeta especificada. Cuando se elimina una subcarpeta, se eliminan la subcarpeta y los mensajes dentro de la subcarpeta.
ms.openlocfilehash: 1913db74d33f1e6750cd158df5870f257d0e7839
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530687"
---
# <a name="emptyfolder-operation"></a><span data-ttu-id="af5ae-105">Operación EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="af5ae-105">EmptyFolder operation</span></span>

<span data-ttu-id="af5ae-106">La operación **EmptyFolder** vacía carpetas en un buzón.</span><span class="sxs-lookup"><span data-stu-id="af5ae-106">The **EmptyFolder** operation empties folders in a mailbox.</span></span> <span data-ttu-id="af5ae-107">Opcionalmente, esta operación permite eliminar las subcarpetas de la carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="af5ae-107">Optionally, this operation enables you to delete the subfolders of the specified folder.</span></span> <span data-ttu-id="af5ae-108">Cuando se elimina una subcarpeta, se eliminan la subcarpeta y los mensajes dentro de la subcarpeta.</span><span class="sxs-lookup"><span data-stu-id="af5ae-108">When a subfolder is deleted, the subfolder and the messages within the subfolder are deleted.</span></span> 
  
## <a name="emptyfolder-request-example"></a><span data-ttu-id="af5ae-109">Ejemplo de solicitud EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="af5ae-109">EmptyFolder request example</span></span>

### <a name="description"></a><span data-ttu-id="af5ae-110">Description</span><span class="sxs-lookup"><span data-stu-id="af5ae-110">Description</span></span>

<span data-ttu-id="af5ae-111">En el siguiente ejemplo de una solicitud de **EmptyFolder** se muestra cómo crear una solicitud para vaciar una carpeta.</span><span class="sxs-lookup"><span data-stu-id="af5ae-111">This following example of an **EmptyFolder** request shows how to form a request to empty a folder.</span></span> <span data-ttu-id="af5ae-112">En este ejemplo se eliminan todas las subcarpetas de la carpeta identificada.</span><span class="sxs-lookup"><span data-stu-id="af5ae-112">This example deletes all subfolders of the identified folder.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="af5ae-113">Los valores de los atributos **ID** y **changekey** del elemento [FolderId](folderid.md) se han abreviado para facilitar su lectura.</span><span class="sxs-lookup"><span data-stu-id="af5ae-113">The values of the **Id** and the **ChangeKey** attributes of the [FolderId](folderid.md) element have been shortened for readability.</span></span> 
  
### <a name="code"></a><span data-ttu-id="af5ae-114">Código</span><span class="sxs-lookup"><span data-stu-id="af5ae-114">Code</span></span>

```XML
<soap:Envelope xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version ="Exchange2010_SP1"/>
    </soap:Header>
    <soap:Body>
      <m:EmptyFolder DeleteType="HardDelete" DeleteSubFolders="true">
        <m:FolderIds>
          <t:FolderId Id="AQMkADhhOGU0"  ChangeKey="AQAAABYAAABsMB" />
        </m:FolderIds>
      </m:EmptyFolder>
    </soap:Body>
</soap:Envelope>

```

### <a name="comments"></a><span data-ttu-id="af5ae-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="af5ae-115">Comments</span></span>

<span data-ttu-id="af5ae-116">En este ejemplo se realiza una eliminación de disco duro en la carpeta.</span><span class="sxs-lookup"><span data-stu-id="af5ae-116">This example performs a hard delete on the folder.</span></span>
  
<span data-ttu-id="af5ae-117">Las carpetas pueden identificarse mediante el elemento [DistinguishedFolderId](distinguishedfolderid.md) o el elemento [FolderId](folderid.md) para su uso en el elemento [FolderIds](folderids.md) .</span><span class="sxs-lookup"><span data-stu-id="af5ae-117">Folders can be identified by either the [DistinguishedFolderId](distinguishedfolderid.md) element or the [FolderId](folderid.md) element for use in the [FolderIds](folderids.md) element.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="af5ae-118">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="af5ae-118">Request elements</span></span>

<span data-ttu-id="af5ae-119">Los siguientes elementos se usan en la solicitud:</span><span class="sxs-lookup"><span data-stu-id="af5ae-119">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="af5ae-120">EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="af5ae-120">EmptyFolder</span></span>](emptyfolder.md)
    
- [<span data-ttu-id="af5ae-121">FolderIds</span><span class="sxs-lookup"><span data-stu-id="af5ae-121">FolderIds</span></span>](folderids.md)
    
- [<span data-ttu-id="af5ae-122">FolderId</span><span class="sxs-lookup"><span data-stu-id="af5ae-122">FolderId</span></span>](folderid.md)
    
## <a name="successful-emptyfolder-response"></a><span data-ttu-id="af5ae-123">Respuesta EmptyFolder correcta</span><span class="sxs-lookup"><span data-stu-id="af5ae-123">Successful EmptyFolder response</span></span>

### <a name="description"></a><span data-ttu-id="af5ae-124">Description</span><span class="sxs-lookup"><span data-stu-id="af5ae-124">Description</span></span>

<span data-ttu-id="af5ae-125">En el ejemplo siguiente se muestra una respuesta correcta a la solicitud **EmptyFolder** .</span><span class="sxs-lookup"><span data-stu-id="af5ae-125">The following example shows a successful response to the **EmptyFolder** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="af5ae-126">Código</span><span class="sxs-lookup"><span data-stu-id="af5ae-126">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="1" 
                         MajorBuildNumber="164" 
                         MinorBuildNumber="0" 
                         Version="Exchange2010_SP1"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:EmptyFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                           xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:EmptyFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:EmptyFolderResponseMessage>
      </m:ResponseMessages>
    </m:EmptyFolderResponse>
  </s:Body>
</s:Envelope>

```

### <a name="successful-response-elements"></a><span data-ttu-id="af5ae-127">Elementos Response correcto</span><span class="sxs-lookup"><span data-stu-id="af5ae-127">Successful response elements</span></span>

<span data-ttu-id="af5ae-128">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="af5ae-128">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="af5ae-129">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="af5ae-129">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="af5ae-130">EmptyFolderResponse</span><span class="sxs-lookup"><span data-stu-id="af5ae-130">EmptyFolderResponse</span></span>](emptyfolderresponse.md)
    
- [<span data-ttu-id="af5ae-131">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="af5ae-131">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="af5ae-132">EmptyFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="af5ae-132">EmptyFolderResponseMessage</span></span>](emptyfolderresponsemessage.md)
    
- [<span data-ttu-id="af5ae-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="af5ae-133">ResponseCode</span></span>](responsecode.md)
    
## <a name="emptyfolder-error-response"></a><span data-ttu-id="af5ae-134">Respuesta de error de EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="af5ae-134">EmptyFolder error response</span></span>

### <a name="description"></a><span data-ttu-id="af5ae-135">Description</span><span class="sxs-lookup"><span data-stu-id="af5ae-135">Description</span></span>

<span data-ttu-id="af5ae-136">En el ejemplo siguiente se muestra una respuesta de error a una solicitud **Emptyfolder** .</span><span class="sxs-lookup"><span data-stu-id="af5ae-136">The following example shows an error response to an **Emptyfolder** request.</span></span> <span data-ttu-id="af5ae-137">El error se creó porque la operación intentó vaciar una carpeta que no se encontró en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="af5ae-137">The error was created because the operation tried to empty a folder that was not found in the Exchange store.</span></span> 
  
### <a name="code"></a><span data-ttu-id="af5ae-138">Código</span><span class="sxs-lookup"><span data-stu-id="af5ae-138">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
            MinorVersion="1" 
            MajorBuildNumber="164" 
            MinorBuildNumber="0" 
            Version="Exchange2010_SP1" 
            xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
            xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
            xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
            xmlns:xsd="http://www.w3.org/2001/XMLSchema" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
            xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetFolderResponse 
          xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetFolderResponseMessage ResponseClass="Error">
          <m:MessageText>Id is malformed.</m:MessageText>
          <m:ResponseCode>ErrorInvalidIdMalformed</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:Folders />
        </m:GetFolderResponseMessage>
      </m:ResponseMessages>
    </m:GetFolderResponse>
  </s:Body>
</s:Envelope>
```

### <a name="error-response-elements"></a><span data-ttu-id="af5ae-139">Elementos de respuesta de error</span><span class="sxs-lookup"><span data-stu-id="af5ae-139">Error response elements</span></span>

<span data-ttu-id="af5ae-140">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="af5ae-140">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="af5ae-141">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="af5ae-141">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="af5ae-142">GetFolderResponse</span><span class="sxs-lookup"><span data-stu-id="af5ae-142">GetFolderResponse</span></span>](getfolderresponse.md)
    
- [<span data-ttu-id="af5ae-143">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="af5ae-143">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="af5ae-144">GetFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="af5ae-144">GetFolderResponseMessage</span></span>](getfolderresponsemessage.md)
    
- [<span data-ttu-id="af5ae-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="af5ae-145">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="af5ae-146">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="af5ae-146">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="af5ae-147">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="af5ae-147">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="af5ae-148">Folders</span><span class="sxs-lookup"><span data-stu-id="af5ae-148">Folders</span></span>](folders-ex15websvcsotherref.md)
    
## <a name="see-also"></a><span data-ttu-id="af5ae-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="af5ae-149">See also</span></span>

- [<span data-ttu-id="af5ae-150">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="af5ae-150">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

