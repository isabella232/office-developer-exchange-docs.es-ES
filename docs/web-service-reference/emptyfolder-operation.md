---
title: Operación EmptyFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 98161486-e2f2-480f-8d5d-708ba81b208a
description: La operación EmptyFolder vacía carpetas en un buzón de correo. De forma opcional, esta operación le permite eliminar las subcarpetas de la carpeta especificada. Cuando se elimina una subcarpeta, se eliminan la subcarpeta y los mensajes dentro de la subcarpeta.
ms.openlocfilehash: 0192744516c5a6d24b95915452bfcffecc2d92b7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764384"
---
# <a name="emptyfolder-operation"></a><span data-ttu-id="9b797-105">Operación EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="9b797-105">EmptyFolder operation</span></span>

<span data-ttu-id="9b797-106">La operación **EmptyFolder** vacía carpetas en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="9b797-106">The **EmptyFolder** operation empties folders in a mailbox.</span></span> <span data-ttu-id="9b797-107">De forma opcional, esta operación le permite eliminar las subcarpetas de la carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="9b797-107">Optionally, this operation enables you to delete the subfolders of the specified folder.</span></span> <span data-ttu-id="9b797-108">Cuando se elimina una subcarpeta, se eliminan la subcarpeta y los mensajes dentro de la subcarpeta.</span><span class="sxs-lookup"><span data-stu-id="9b797-108">When a subfolder is deleted, the subfolder and the messages within the subfolder are deleted.</span></span> 
  
## <a name="emptyfolder-request-example"></a><span data-ttu-id="9b797-109">Ejemplo de solicitud EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="9b797-109">EmptyFolder request example</span></span>

### <a name="description"></a><span data-ttu-id="9b797-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="9b797-110">Description</span></span>

<span data-ttu-id="9b797-111">El siguiente ejemplo de una solicitud **EmptyFolder** muestra cómo formar una solicitud para vaciar una carpeta.</span><span class="sxs-lookup"><span data-stu-id="9b797-111">This following example of an **EmptyFolder** request shows how to form a request to empty a folder.</span></span> <span data-ttu-id="9b797-112">En este ejemplo se eliminan todas las subcarpetas de la carpeta identificada.</span><span class="sxs-lookup"><span data-stu-id="9b797-112">This example deletes all subfolders of the identified folder.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="9b797-113">Los valores del **identificador** y los atributos **ChangeKey** del elemento [FolderId](folderid.md) se han abreviado para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="9b797-113">The values of the **Id** and the **ChangeKey** attributes of the [FolderId](folderid.md) element have been shortened for readability.</span></span> 
  
### <a name="code"></a><span data-ttu-id="9b797-114">Código</span><span class="sxs-lookup"><span data-stu-id="9b797-114">Code</span></span>

```XML
<soap:Envelope xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a><span data-ttu-id="9b797-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9b797-115">Comments</span></span>

<span data-ttu-id="9b797-116">En este ejemplo se realiza una eliminación de disco duro en la carpeta.</span><span class="sxs-lookup"><span data-stu-id="9b797-116">This example performs a hard delete on the folder.</span></span>
  
<span data-ttu-id="9b797-117">Las carpetas se pueden identificar por el elemento [DistinguishedFolderId](distinguishedfolderid.md) o el elemento [FolderId](folderid.md) para su uso en el elemento [FolderIds](folderids.md) .</span><span class="sxs-lookup"><span data-stu-id="9b797-117">Folders can be identified by either the [DistinguishedFolderId](distinguishedfolderid.md) element or the [FolderId](folderid.md) element for use in the [FolderIds](folderids.md) element.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="9b797-118">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="9b797-118">Request elements</span></span>

<span data-ttu-id="9b797-119">En la solicitud se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="9b797-119">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="9b797-120">EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="9b797-120">EmptyFolder</span></span>](emptyfolder.md)
    
- [<span data-ttu-id="9b797-121">FolderIds</span><span class="sxs-lookup"><span data-stu-id="9b797-121">FolderIds</span></span>](folderids.md)
    
- [<span data-ttu-id="9b797-122">FolderId</span><span class="sxs-lookup"><span data-stu-id="9b797-122">FolderId</span></span>](folderid.md)
    
## <a name="successful-emptyfolder-response"></a><span data-ttu-id="9b797-123">Respuesta es correcta EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="9b797-123">Successful EmptyFolder response</span></span>

### <a name="description"></a><span data-ttu-id="9b797-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="9b797-124">Description</span></span>

<span data-ttu-id="9b797-125">En el ejemplo siguiente se muestra una respuesta correcta a la solicitud **EmptyFolder** .</span><span class="sxs-lookup"><span data-stu-id="9b797-125">The following example shows a successful response to the **EmptyFolder** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="9b797-126">Código</span><span class="sxs-lookup"><span data-stu-id="9b797-126">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="1" 
                         MajorBuildNumber="164" 
                         MinorBuildNumber="0" 
                         Version="Exchange2010_SP1"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:EmptyFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                           xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:EmptyFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:EmptyFolderResponseMessage>
      </m:ResponseMessages>
    </m:EmptyFolderResponse>
  </s:Body>
</s:Envelope>

```

### <a name="successful-response-elements"></a><span data-ttu-id="9b797-127">Elementos de respuesta correcta</span><span class="sxs-lookup"><span data-stu-id="9b797-127">Successful response elements</span></span>

<span data-ttu-id="9b797-128">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="9b797-128">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="9b797-129">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="9b797-129">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="9b797-130">EmptyFolderResponse</span><span class="sxs-lookup"><span data-stu-id="9b797-130">EmptyFolderResponse</span></span>](emptyfolderresponse.md)
    
- [<span data-ttu-id="9b797-131">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="9b797-131">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="9b797-132">EmptyFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="9b797-132">EmptyFolderResponseMessage</span></span>](emptyfolderresponsemessage.md)
    
- [<span data-ttu-id="9b797-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="9b797-133">ResponseCode</span></span>](responsecode.md)
    
## <a name="emptyfolder-error-response"></a><span data-ttu-id="9b797-134">Respuesta de error EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="9b797-134">EmptyFolder error response</span></span>

### <a name="description"></a><span data-ttu-id="9b797-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="9b797-135">Description</span></span>

<span data-ttu-id="9b797-136">En el ejemplo siguiente se muestra una respuesta de error a una solicitud **Emptyfolder** .</span><span class="sxs-lookup"><span data-stu-id="9b797-136">The following example shows an error response to an **Emptyfolder** request.</span></span> <span data-ttu-id="9b797-137">Se creó el error debido a que la operación intentó vaciar una carpeta que no se encontró en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="9b797-137">The error was created because the operation tried to empty a folder that was not found in the Exchange store.</span></span> 
  
### <a name="code"></a><span data-ttu-id="9b797-138">Código</span><span class="sxs-lookup"><span data-stu-id="9b797-138">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
            MinorVersion="1" 
            MajorBuildNumber="164" 
            MinorBuildNumber="0" 
            Version="Exchange2010_SP1" 
            xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
            xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
            xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
            xmlns:xsd="http://www.w3.org/2001/XMLSchema" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
            xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetFolderResponse 
          xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

### <a name="error-response-elements"></a><span data-ttu-id="9b797-139">Elementos de respuesta de error</span><span class="sxs-lookup"><span data-stu-id="9b797-139">Error response elements</span></span>

<span data-ttu-id="9b797-140">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="9b797-140">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="9b797-141">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="9b797-141">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="9b797-142">GetFolderResponse</span><span class="sxs-lookup"><span data-stu-id="9b797-142">GetFolderResponse</span></span>](getfolderresponse.md)
    
- [<span data-ttu-id="9b797-143">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="9b797-143">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="9b797-144">GetFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="9b797-144">GetFolderResponseMessage</span></span>](getfolderresponsemessage.md)
    
- [<span data-ttu-id="9b797-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="9b797-145">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="9b797-146">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="9b797-146">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="9b797-147">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="9b797-147">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="9b797-148">Carpetas</span><span class="sxs-lookup"><span data-stu-id="9b797-148">Folders</span></span>](folders-ex15websvcsotherref.md)
    
## <a name="see-also"></a><span data-ttu-id="9b797-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="9b797-149">See also</span></span>

- [<span data-ttu-id="9b797-150">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="9b797-150">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

