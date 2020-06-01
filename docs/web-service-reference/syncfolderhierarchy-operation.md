---
title: Operación SyncFolderHierarchy
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SyncFolderHierarchy
api_type:
- schema
ms.assetid: b31916b1-bc6c-4451-a475-b7c5417f752d
description: La operación SyncFolderHierarchy sincroniza las carpetas entre el equipo que ejecuta Microsoft Exchange Server 2010 y el cliente.
ms.openlocfilehash: 1c7ad2413064161ba54e8a7a30bfcd6f23f218bd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456433"
---
# <a name="syncfolderhierarchy-operation"></a><span data-ttu-id="9f748-103">Operación SyncFolderHierarchy</span><span class="sxs-lookup"><span data-stu-id="9f748-103">SyncFolderHierarchy operation</span></span>

<span data-ttu-id="9f748-104">La operación SyncFolderHierarchy sincroniza las carpetas entre el equipo que ejecuta Microsoft Exchange Server 2010 y el cliente.</span><span class="sxs-lookup"><span data-stu-id="9f748-104">The SyncFolderHierarchy operation synchronizes folders between the computer that is running Microsoft Exchange Server 2010 and the client.</span></span>
  
> [!NOTE]
> <span data-ttu-id="9f748-105">La operación SyncFolderHierarchy no devuelve carpetas cuando las propiedades [UnreadCount](unreadcount.md) o [totalCount](totalcount.md) han cambiado.</span><span class="sxs-lookup"><span data-stu-id="9f748-105">The SyncFolderHierarchy operation does not return folders when the [UnreadCount](unreadcount.md) or [TotalCount](totalcount.md) properties have changed.</span></span> 
  
## <a name="syncfolderhierarchy-request-example"></a><span data-ttu-id="9f748-106">Ejemplo de solicitud SyncFolderHierarchy</span><span class="sxs-lookup"><span data-stu-id="9f748-106">SyncFolderHierarchy request example</span></span>

### <a name="description"></a><span data-ttu-id="9f748-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="9f748-107">Description</span></span>

<span data-ttu-id="9f748-108">En el siguiente ejemplo de una solicitud de SyncFolderHierarchy se muestra cómo sincronizar una jerarquía de carpetas de cliente con el servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="9f748-108">The following example of a SyncFolderHierarchy request shows how to synchronize a client folder hierarchy with the Exchange server.</span></span> <span data-ttu-id="9f748-109">En este ejemplo se muestra una jerarquía de carpetas que ya se ha sincronizado al menos una vez.</span><span class="sxs-lookup"><span data-stu-id="9f748-109">This example shows a folder hierarchy that has already been synchronized at least one time.</span></span> <span data-ttu-id="9f748-110">El elemento [SyncState](syncstate-ex15websvcsotherref.md) no se incluye en la solicitud para el primer intento de sincronizar un cliente con el servidor Exchange.</span><span class="sxs-lookup"><span data-stu-id="9f748-110">The [SyncState](syncstate-ex15websvcsotherref.md) element is not included in the request for the first attempt to synchronize a client with the Exchange server.</span></span> <span data-ttu-id="9f748-111">La primera solicitud devolverá todas las carpetas del buzón.</span><span class="sxs-lookup"><span data-stu-id="9f748-111">The first request will return all the folders in the mailbox.</span></span> <span data-ttu-id="9f748-112">El elemento [SyncState](syncstate-ex15websvcsotherref.md) se devolverá en [SyncFolderHierarchyResponse](syncfolderhierarchyresponse.md).</span><span class="sxs-lookup"><span data-stu-id="9f748-112">The [SyncState](syncstate-ex15websvcsotherref.md) element will be returned in the [SyncFolderHierarchyResponse](syncfolderhierarchyresponse.md).</span></span> <span data-ttu-id="9f748-113">Este elemento se usa para sincronizar el estado de las siguientes solicitudes SyncFolderHierarchy.</span><span class="sxs-lookup"><span data-stu-id="9f748-113">This element is used to synchronize the state for subsequent SyncFolderHierarchy requests.</span></span>
  
### <a name="code"></a><span data-ttu-id="9f748-114">Código</span><span class="sxs-lookup"><span data-stu-id="9f748-114">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <SyncFolderHierarchy  xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <FolderShape>
        <t:BaseShape>AllProperties</t:BaseShape>
      </FolderShape>
      <SyncState>H4sIA=</SyncState>
    </SyncFolderHierarchy>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="9f748-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9f748-115">Comments</span></span>

<span data-ttu-id="9f748-116">Los datos codificados en base64 del elemento [SyncState](syncstate-ex15websvcsotherref.md) se han reducido para preservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="9f748-116">The [SyncState](syncstate-ex15websvcsotherref.md) element base64-encoded data has been shortened to preserve readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="9f748-117">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="9f748-117">Request elements</span></span>

<span data-ttu-id="9f748-118">Los siguientes elementos se usan en la solicitud:</span><span class="sxs-lookup"><span data-stu-id="9f748-118">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="9f748-119">SyncFolderHierarchy</span><span class="sxs-lookup"><span data-stu-id="9f748-119">SyncFolderHierarchy</span></span>](syncfolderhierarchy.md)
    
- [<span data-ttu-id="9f748-120">FolderShape</span><span class="sxs-lookup"><span data-stu-id="9f748-120">FolderShape</span></span>](foldershape.md)
    
- [<span data-ttu-id="9f748-121">BaseShape</span><span class="sxs-lookup"><span data-stu-id="9f748-121">BaseShape</span></span>](baseshape.md)
    
- [<span data-ttu-id="9f748-122">SyncState</span><span class="sxs-lookup"><span data-stu-id="9f748-122">SyncState</span></span>](syncstate-ex15websvcsotherref.md)
    
> [!NOTE]
> <span data-ttu-id="9f748-123">El esquema que describe estos elementos se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="9f748-123">The schema that describes these elements is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="successful-syncfolderhierarchy-response"></a><span data-ttu-id="9f748-124">Respuesta SyncFolderHierarchy correcta</span><span class="sxs-lookup"><span data-stu-id="9f748-124">Successful SyncFolderHierarchy Response</span></span>

### <a name="description"></a><span data-ttu-id="9f748-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="9f748-125">Description</span></span>

<span data-ttu-id="9f748-126">En el ejemplo siguiente se muestra una respuesta correcta a la solicitud SyncFolderHierarchy.</span><span class="sxs-lookup"><span data-stu-id="9f748-126">The following example shows a successful response to the SyncFolderHierarchy request.</span></span> <span data-ttu-id="9f748-127">En este ejemplo, se ha sincronizado una nueva carpeta.</span><span class="sxs-lookup"><span data-stu-id="9f748-127">In this example, a new folder has been synchronized.</span></span>
  
### <a name="code"></a><span data-ttu-id="9f748-128">Código</span><span class="sxs-lookup"><span data-stu-id="9f748-128">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" 
                         MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <SyncFolderHierarchyResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                 xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                                 xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:SyncFolderHierarchyResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:SyncState>H4sIAAA==</m:SyncState>
          <m:IncludesLastFolderInRange>true</m:IncludesLastFolderInRange>
          <m:Changes>
            <t:Create>
              <t:Folder>
                <t:FolderId Id="AQApAHR=" ChangeKey="AQAAABY" />
                <t:ParentFolderId Id="AQApA=" ChangeKey="AQAAAA==" />
                <t:FolderClass>IPF.Note</t:FolderClass>
                <t:DisplayName>NewFolder</t:DisplayName>
                <t:TotalCount>0</t:TotalCount>
                <t:ChildFolderCount>0</t:ChildFolderCount>
                <t:UnreadCount>0</t:UnreadCount>
              </t:Folder>
            </t:Create>
          </m:Changes>
        </m:SyncFolderHierarchyResponseMessage>
      </m:ResponseMessages>
    </SyncFolderHierarchyResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="9f748-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9f748-129">Comments</span></span>

<span data-ttu-id="9f748-130">Los datos con codificación base64 del elemento [SyncState](syncstate-ex15websvcsotherref.md) y los datos del identificador de la carpeta se han reducido para preservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="9f748-130">The [SyncState](syncstate-ex15websvcsotherref.md) element base64-encoded data and the folder identifier data have been shortened to preserve readability.</span></span> 
  
### <a name="successful-response-elements"></a><span data-ttu-id="9f748-131">Elementos Response correcto</span><span class="sxs-lookup"><span data-stu-id="9f748-131">Successful response elements</span></span>

<span data-ttu-id="9f748-132">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="9f748-132">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="9f748-133">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="9f748-133">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="9f748-134">SyncFolderHierarchyResponse</span><span class="sxs-lookup"><span data-stu-id="9f748-134">SyncFolderHierarchyResponse</span></span>](syncfolderhierarchyresponse.md)
    
- [<span data-ttu-id="9f748-135">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="9f748-135">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="9f748-136">SyncFolderHierarchyResponseMessage</span><span class="sxs-lookup"><span data-stu-id="9f748-136">SyncFolderHierarchyResponseMessage</span></span>](syncfolderhierarchyresponsemessage.md)
    
- [<span data-ttu-id="9f748-137">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="9f748-137">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="9f748-138">SyncState</span><span class="sxs-lookup"><span data-stu-id="9f748-138">SyncState</span></span>](syncstate-ex15websvcsotherref.md)
    
- [<span data-ttu-id="9f748-139">IncludesLastFolderInRange</span><span class="sxs-lookup"><span data-stu-id="9f748-139">IncludesLastFolderInRange</span></span>](includeslastfolderinrange.md)
    
- [<span data-ttu-id="9f748-140">Cambios (jerarquía)</span><span class="sxs-lookup"><span data-stu-id="9f748-140">Changes (Hierarchy)</span></span>](changes-hierarchy.md)
    
- [<span data-ttu-id="9f748-141">Crear (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="9f748-141">Create (FolderSync)</span></span>](create-foldersync.md)
    
- [<span data-ttu-id="9f748-142">Folder</span><span class="sxs-lookup"><span data-stu-id="9f748-142">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="9f748-143">FolderId</span><span class="sxs-lookup"><span data-stu-id="9f748-143">FolderId</span></span>](folderid.md)
    
- [<span data-ttu-id="9f748-144">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="9f748-144">ParentFolderId</span></span>](parentfolderid.md)
    
- [<span data-ttu-id="9f748-145">FolderClass</span><span class="sxs-lookup"><span data-stu-id="9f748-145">FolderClass</span></span>](folderclass.md)
    
- [<span data-ttu-id="9f748-146">DisplayName (cadena)</span><span class="sxs-lookup"><span data-stu-id="9f748-146">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="9f748-147">TotalCount</span><span class="sxs-lookup"><span data-stu-id="9f748-147">TotalCount</span></span>](totalcount.md)
    
- [<span data-ttu-id="9f748-148">ChildFolderCount</span><span class="sxs-lookup"><span data-stu-id="9f748-148">ChildFolderCount</span></span>](childfoldercount.md)
    
- [<span data-ttu-id="9f748-149">UnreadCount</span><span class="sxs-lookup"><span data-stu-id="9f748-149">UnreadCount</span></span>](unreadcount.md)
    
## <a name="syncfolderhierarchy-error-response"></a><span data-ttu-id="9f748-150">Respuesta de error de SyncFolderHierarchy</span><span class="sxs-lookup"><span data-stu-id="9f748-150">SyncFolderHierarchy error response</span></span>

### <a name="description"></a><span data-ttu-id="9f748-151">Descripción</span><span class="sxs-lookup"><span data-stu-id="9f748-151">Description</span></span>

<span data-ttu-id="9f748-152">En el ejemplo siguiente se muestra una respuesta de error a una solicitud SyncFolderHierarchy.</span><span class="sxs-lookup"><span data-stu-id="9f748-152">The following example shows an error response to a SyncFolderHierarchy request.</span></span> <span data-ttu-id="9f748-153">Este error se debió a un SyncState no válido.</span><span class="sxs-lookup"><span data-stu-id="9f748-153">This error was caused by an invalid SyncState.</span></span>
  
### <a name="code"></a><span data-ttu-id="9f748-154">Código</span><span class="sxs-lookup"><span data-stu-id="9f748-154">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" 
                         MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <SyncFolderHierarchyResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                 xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                                 xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:SyncFolderHierarchyResponseMessage ResponseClass="Error">
          <m:MessageText>Synchronization state data is corrupted or otherwise invalid.</m:MessageText>
          <m:ResponseCode>ErrorInvalidSyncStateData</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:SyncState />
          <m:IncludesLastFolderInRange>true</m:IncludesLastFolderInRange>
        </m:SyncFolderHierarchyResponseMessage>
      </m:ResponseMessages>
    </SyncFolderHierarchyResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a><span data-ttu-id="9f748-155">Elementos de respuesta de error</span><span class="sxs-lookup"><span data-stu-id="9f748-155">Error response elements</span></span>

<span data-ttu-id="9f748-156">Los siguientes elementos se usan en la respuesta de error:</span><span class="sxs-lookup"><span data-stu-id="9f748-156">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="9f748-157">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="9f748-157">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="9f748-158">SyncFolderHierarchyResponse</span><span class="sxs-lookup"><span data-stu-id="9f748-158">SyncFolderHierarchyResponse</span></span>](syncfolderhierarchyresponse.md)
    
- [<span data-ttu-id="9f748-159">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="9f748-159">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="9f748-160">SyncFolderHierarchyResponseMessage</span><span class="sxs-lookup"><span data-stu-id="9f748-160">SyncFolderHierarchyResponseMessage</span></span>](syncfolderhierarchyresponsemessage.md)
    
- [<span data-ttu-id="9f748-161">MessageText</span><span class="sxs-lookup"><span data-stu-id="9f748-161">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="9f748-162">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="9f748-162">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="9f748-163">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="9f748-163">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="9f748-164">SyncState</span><span class="sxs-lookup"><span data-stu-id="9f748-164">SyncState</span></span>](syncstate-ex15websvcsotherref.md)
    
- [<span data-ttu-id="9f748-165">IncludesLastFolderInRange</span><span class="sxs-lookup"><span data-stu-id="9f748-165">IncludesLastFolderInRange</span></span>](includeslastfolderinrange.md)
    
## <a name="see-also"></a><span data-ttu-id="9f748-166">Vea también</span><span class="sxs-lookup"><span data-stu-id="9f748-166">See also</span></span>



- [<span data-ttu-id="9f748-167">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="9f748-167">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

