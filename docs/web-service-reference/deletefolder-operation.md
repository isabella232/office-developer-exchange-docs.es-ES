---
title: Operación DeleteFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteFolder
api_type:
- schema
ms.assetid: b0f92682-4895-4bcf-a4a1-e4c2e8403979
description: La operación DeleteFolder elimina carpetas de un buzón.
ms.openlocfilehash: e9bb9199027c2af2cbbb664ef7ad4fa70b7ef718
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455747"
---
# <a name="deletefolder-operation"></a><span data-ttu-id="7b5f5-103">Operación DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="7b5f5-103">DeleteFolder operation</span></span>

<span data-ttu-id="7b5f5-104">La operación **DeleteFolder** elimina carpetas de un buzón.</span><span class="sxs-lookup"><span data-stu-id="7b5f5-104">The **DeleteFolder** operation deletes folders from a mailbox.</span></span> 
  
## <a name="deletefolder-request-example"></a><span data-ttu-id="7b5f5-105">Ejemplo de solicitud DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="7b5f5-105">DeleteFolder request example</span></span>

### <a name="description"></a><span data-ttu-id="7b5f5-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="7b5f5-106">Description</span></span>

<span data-ttu-id="7b5f5-107">En el siguiente ejemplo de una solicitud de **DeleteFolder** se muestra cómo crear una solicitud para eliminar una carpeta.</span><span class="sxs-lookup"><span data-stu-id="7b5f5-107">This following example of a **DeleteFolder** request shows how to form a request to delete a folder.</span></span> 
  
### <a name="code"></a><span data-ttu-id="7b5f5-108">Código</span><span class="sxs-lookup"><span data-stu-id="7b5f5-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <DeleteFolder xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                  DeleteType="HardDelete" >
      <FolderIds>
        <t:FolderId Id="AS4AUnVz=" />
      </FolderIds>
    </DeleteFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="7b5f5-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7b5f5-109">Comments</span></span>

<span data-ttu-id="7b5f5-110">En este ejemplo se realiza una eliminación de disco duro en la carpeta.</span><span class="sxs-lookup"><span data-stu-id="7b5f5-110">This example performs a hard delete on the folder.</span></span>
  
> [!NOTE]
> <span data-ttu-id="7b5f5-111">El identificador de la carpeta se ha abreviado para preservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="7b5f5-111">The folder ID has been shortened to preserve readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="7b5f5-112">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="7b5f5-112">Request elements</span></span>

<span data-ttu-id="7b5f5-113">Los siguientes elementos se usan en la solicitud:</span><span class="sxs-lookup"><span data-stu-id="7b5f5-113">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="7b5f5-114">DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="7b5f5-114">DeleteFolder</span></span>](deletefolder.md)
    
- [<span data-ttu-id="7b5f5-115">FolderIds</span><span class="sxs-lookup"><span data-stu-id="7b5f5-115">FolderIds</span></span>](folderids.md)
    
- [<span data-ttu-id="7b5f5-116">FolderId</span><span class="sxs-lookup"><span data-stu-id="7b5f5-116">FolderId</span></span>](folderid.md)
    
> [!NOTE]
> <span data-ttu-id="7b5f5-117">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="7b5f5-117">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span> 
  
<span data-ttu-id="7b5f5-118">Para buscar otras opciones para el mensaje de solicitud de la operación **DeleteFolder** , explore la jerarquía del esquema.</span><span class="sxs-lookup"><span data-stu-id="7b5f5-118">To find other options for the request message of the **DeleteFolder** operation, explore the schema hierarchy.</span></span> <span data-ttu-id="7b5f5-119">Empiece en el elemento [DeleteFolder](deletefolder.md) .</span><span class="sxs-lookup"><span data-stu-id="7b5f5-119">Start at the [DeleteFolder](deletefolder.md) element.</span></span> 
  
## <a name="successful-deletefolder-response"></a><span data-ttu-id="7b5f5-120">Respuesta DeleteFolder correcta</span><span class="sxs-lookup"><span data-stu-id="7b5f5-120">Successful DeleteFolder response</span></span>

### <a name="description"></a><span data-ttu-id="7b5f5-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="7b5f5-121">Description</span></span>

<span data-ttu-id="7b5f5-122">En el ejemplo siguiente se muestra una respuesta correcta a la solicitud **DeleteFolder** .</span><span class="sxs-lookup"><span data-stu-id="7b5f5-122">The following example shows a successful response to the **DeleteFolder** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="7b5f5-123">Código</span><span class="sxs-lookup"><span data-stu-id="7b5f5-123">Code</span></span>

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
    <DeleteFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:DeleteFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:DeleteFolderResponseMessage>
      </m:ResponseMessages>
    </DeleteFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="response-elements"></a><span data-ttu-id="7b5f5-124">Elementos de respuesta</span><span class="sxs-lookup"><span data-stu-id="7b5f5-124">Response elements</span></span>

<span data-ttu-id="7b5f5-125">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="7b5f5-125">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="7b5f5-126">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="7b5f5-126">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="7b5f5-127">DeleteFolderResponse</span><span class="sxs-lookup"><span data-stu-id="7b5f5-127">DeleteFolderResponse</span></span>](deletefolderresponse.md)
    
- [<span data-ttu-id="7b5f5-128">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="7b5f5-128">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="7b5f5-129">DeleteFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="7b5f5-129">DeleteFolderResponseMessage</span></span>](deletefolderresponsemessage.md)
    
- [<span data-ttu-id="7b5f5-130">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="7b5f5-130">ResponseCode</span></span>](responsecode.md)
    
<span data-ttu-id="7b5f5-131">Para buscar otras opciones para el mensaje de respuesta de la operación **DeleteFolder** , explore la jerarquía del esquema.</span><span class="sxs-lookup"><span data-stu-id="7b5f5-131">To find other options for the response message of the **DeleteFolder** operation, explore the schema hierarchy.</span></span> <span data-ttu-id="7b5f5-132">Empiece en el elemento [DeleteFolderResponse](deletefolderresponse.md) .</span><span class="sxs-lookup"><span data-stu-id="7b5f5-132">Start at the [DeleteFolderResponse](deletefolderresponse.md) element.</span></span> 
  
## <a name="deletefolder-error-response"></a><span data-ttu-id="7b5f5-133">Respuesta de error de DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="7b5f5-133">DeleteFolder error response</span></span>

### <a name="description"></a><span data-ttu-id="7b5f5-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="7b5f5-134">Description</span></span>

<span data-ttu-id="7b5f5-135">En el ejemplo siguiente se muestra una respuesta de error a una solicitud **DeleteFolder** .</span><span class="sxs-lookup"><span data-stu-id="7b5f5-135">The following example shows an error response to a **DeleteFolder** request.</span></span> <span data-ttu-id="7b5f5-136">El error se ha producido por una solicitud para eliminar una carpeta que no estaba presente en el buzón.</span><span class="sxs-lookup"><span data-stu-id="7b5f5-136">The error was caused by a request to delete a folder that was not present in the mailbox.</span></span> 
  
### <a name="code"></a><span data-ttu-id="7b5f5-137">Código</span><span class="sxs-lookup"><span data-stu-id="7b5f5-137">Code</span></span>

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
    <DeleteFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:DeleteFolderResponseMessage ResponseClass="Error">
          <m:MessageText>The specified object was not found in the store.</m:MessageText>
          <m:ResponseCode>ErrorItemNotFound</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:DeleteFolderResponseMessage>
      </m:ResponseMessages>
    </DeleteFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="7b5f5-138">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7b5f5-138">Comments</span></span>

<span data-ttu-id="7b5f5-139">La operación **DeleteFolder** no se puede usar en carpetas completas.</span><span class="sxs-lookup"><span data-stu-id="7b5f5-139">The **DeleteFolder** operation cannot be used on distinguished folders.</span></span> 
  
### <a name="error-response-elements"></a><span data-ttu-id="7b5f5-140">Elementos de respuesta de error</span><span class="sxs-lookup"><span data-stu-id="7b5f5-140">Error response elements</span></span>

<span data-ttu-id="7b5f5-141">Los siguientes elementos se usan en la respuesta de error:</span><span class="sxs-lookup"><span data-stu-id="7b5f5-141">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="7b5f5-142">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="7b5f5-142">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="7b5f5-143">DeleteFolderResponse</span><span class="sxs-lookup"><span data-stu-id="7b5f5-143">DeleteFolderResponse</span></span>](deletefolderresponse.md)
    
- [<span data-ttu-id="7b5f5-144">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="7b5f5-144">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="7b5f5-145">DeleteFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="7b5f5-145">DeleteFolderResponseMessage</span></span>](deletefolderresponsemessage.md)
    
- [<span data-ttu-id="7b5f5-146">MessageText</span><span class="sxs-lookup"><span data-stu-id="7b5f5-146">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="7b5f5-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="7b5f5-147">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="7b5f5-148">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="7b5f5-148">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="7b5f5-149">Para buscar otras opciones para el mensaje de respuesta de error de la operación **DeleteFolder** , explore la jerarquía del esquema.</span><span class="sxs-lookup"><span data-stu-id="7b5f5-149">To find other options for the error response message of the **DeleteFolder** operation, explore the schema hierarchy.</span></span> <span data-ttu-id="7b5f5-150">Empiece en el elemento [DeleteFolderResponse](deletefolderresponse.md) .</span><span class="sxs-lookup"><span data-stu-id="7b5f5-150">Start at the [DeleteFolderResponse](deletefolderresponse.md) element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7b5f5-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="7b5f5-151">See also</span></span>

- [<span data-ttu-id="7b5f5-152">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="7b5f5-152">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="7b5f5-153">Eliminar carpetas</span><span class="sxs-lookup"><span data-stu-id="7b5f5-153">Deleting Folders</span></span>](https://msdn.microsoft.com/library/1958add5-5071-4239-adb2-40f7a7d74aee%28Office.15%29.aspx)

