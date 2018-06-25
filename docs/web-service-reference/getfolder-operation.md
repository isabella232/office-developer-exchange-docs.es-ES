---
title: GetFolder Operation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetFolder
api_type:
- schema
ms.assetid: 355bcf93-dc71-4493-b177-622afac5fdb9
description: La operación GetFolder Obtiene las carpetas del almacén de Exchange.
ms.openlocfilehash: 1d2806e4febb6059b8a866d585bc70f49befbdef
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764858"
---
# <a name="getfolder-operation"></a><span data-ttu-id="ddcaa-103">GetFolder Operation</span><span class="sxs-lookup"><span data-stu-id="ddcaa-103">GetFolder operation</span></span>

<span data-ttu-id="ddcaa-104">La operación **GetFolder** Obtiene las carpetas del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ddcaa-104">The **GetFolder** operation gets folders from the Exchange store.</span></span> 
  
## <a name="getfolder-request-example"></a><span data-ttu-id="ddcaa-105">Ejemplo de solicitud GetFolder</span><span class="sxs-lookup"><span data-stu-id="ddcaa-105">GetFolder request example</span></span>

### <a name="description"></a><span data-ttu-id="ddcaa-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="ddcaa-106">Description</span></span>

<span data-ttu-id="ddcaa-107">El siguiente ejemplo de una solicitud de **GetFolder** muestra cómo obtener un identificador de carpeta, Mostrar nombre, el recuento de elementos en dicha carpeta, el número de carpetas secundarias y el número de elementos no leídos en la carpeta.</span><span class="sxs-lookup"><span data-stu-id="ddcaa-107">The following example of a **GetFolder** request shows how to obtain a folder identifier, display name, the count of items in that folder, the count of child folders, and the number of unread items in the folder.</span></span> 
  
### <a name="code"></a><span data-ttu-id="ddcaa-108">Código</span><span class="sxs-lookup"><span data-stu-id="ddcaa-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
   xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetFolder xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <FolderShape>
        <t:BaseShape>Default</t:BaseShape>
      </FolderShape>
      <FolderIds>
        <t:DistinguishedFolderId Id="inbox"/>
      </FolderIds>
    </GetFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a><span data-ttu-id="ddcaa-109">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="ddcaa-109">Request elements</span></span>

<span data-ttu-id="ddcaa-110">Esta solicitud **GetFolder** incluye los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="ddcaa-110">This **GetFolder** request includes the following elements:</span></span> 
  
- [<span data-ttu-id="ddcaa-111">GetFolder</span><span class="sxs-lookup"><span data-stu-id="ddcaa-111">GetFolder</span></span>](getfolder.md)
    
- [<span data-ttu-id="ddcaa-112">FolderShape</span><span class="sxs-lookup"><span data-stu-id="ddcaa-112">FolderShape</span></span>](foldershape.md)
    
- [<span data-ttu-id="ddcaa-113">BaseShape</span><span class="sxs-lookup"><span data-stu-id="ddcaa-113">BaseShape</span></span>](baseshape.md)
    
- [<span data-ttu-id="ddcaa-114">FolderIds</span><span class="sxs-lookup"><span data-stu-id="ddcaa-114">FolderIds</span></span>](folderids.md)
    
- [<span data-ttu-id="ddcaa-115">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="ddcaa-115">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
<span data-ttu-id="ddcaa-116">Consulte el esquema para los elementos adicionales que puede usar para realizar una solicitud **GetFolder** .</span><span class="sxs-lookup"><span data-stu-id="ddcaa-116">See the schema for additional elements that you can use to form a **GetFolder** request.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ddcaa-117">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="ddcaa-117">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span> 
  
## <a name="getfolder-response-example"></a><span data-ttu-id="ddcaa-118">Ejemplo de respuesta GetFolder</span><span class="sxs-lookup"><span data-stu-id="ddcaa-118">GetFolder response example</span></span>

### <a name="description"></a><span data-ttu-id="ddcaa-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="ddcaa-119">Description</span></span>

<span data-ttu-id="ddcaa-120">El siguiente ejemplo de cuerpo de SOAP Simple Object Access Protocol () muestra una respuesta correcta a la solicitud de **GetFolder** .</span><span class="sxs-lookup"><span data-stu-id="ddcaa-120">The following Simple Object Access Protocol (SOAP) body example shows a successful response to the **GetFolder** request.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ddcaa-121">El identificador de la carpeta y la clave de cambio se han abreviado para conservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="ddcaa-121">The folder ID and the change key have been shortened to preserve readability.</span></span> 
  
### <a name="code"></a><span data-ttu-id="ddcaa-122">Código</span><span class="sxs-lookup"><span data-stu-id="ddcaa-122">Code</span></span>

```XML
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                       xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:GetFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:Folder>
              <t:FolderId Id="AQApA=" ChangeKey="AQAAAB" />
              <t:DisplayName>Inbox</t:DisplayName>
              <t:TotalCount>2</t:TotalCount>
              <t:ChildFolderCount>0</t:ChildFolderCount>
              <t:UnreadCount>2</t:UnreadCount>
            </t:Folder>
          </m:Folders>
        </m:GetFolderResponseMessage>
      </m:ResponseMessages>
    </GetFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="response-elements"></a><span data-ttu-id="ddcaa-123">Elementos de respuesta</span><span class="sxs-lookup"><span data-stu-id="ddcaa-123">Response elements</span></span>

<span data-ttu-id="ddcaa-124">Esta respuesta **GetFolder** incluye los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="ddcaa-124">This **GetFolder** response includes the following elements:</span></span> 
  
- [<span data-ttu-id="ddcaa-125">GetFolderResponse</span><span class="sxs-lookup"><span data-stu-id="ddcaa-125">GetFolderResponse</span></span>](getfolderresponse.md)
    
- [<span data-ttu-id="ddcaa-126">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="ddcaa-126">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="ddcaa-127">GetFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="ddcaa-127">GetFolderResponseMessage</span></span>](getfolderresponsemessage.md)
    
- [<span data-ttu-id="ddcaa-128">Carpetas</span><span class="sxs-lookup"><span data-stu-id="ddcaa-128">Folders</span></span>](folders-ex15websvcsotherref.md)
    
- [<span data-ttu-id="ddcaa-129">Folder</span><span class="sxs-lookup"><span data-stu-id="ddcaa-129">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="ddcaa-130">FolderId</span><span class="sxs-lookup"><span data-stu-id="ddcaa-130">FolderId</span></span>](folderid.md)
    
- [<span data-ttu-id="ddcaa-131">DisplayName (cadena)</span><span class="sxs-lookup"><span data-stu-id="ddcaa-131">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="ddcaa-132">TotalCount</span><span class="sxs-lookup"><span data-stu-id="ddcaa-132">TotalCount</span></span>](totalcount.md)
    
- [<span data-ttu-id="ddcaa-133">ChildFolderCount</span><span class="sxs-lookup"><span data-stu-id="ddcaa-133">ChildFolderCount</span></span>](childfoldercount.md)
    
- [<span data-ttu-id="ddcaa-134">UnreadCount</span><span class="sxs-lookup"><span data-stu-id="ddcaa-134">UnreadCount</span></span>](unreadcount.md)
    
## <a name="getfolder-error-response-example"></a><span data-ttu-id="ddcaa-135">Ejemplo de respuesta de GetFolder Error</span><span class="sxs-lookup"><span data-stu-id="ddcaa-135">GetFolder Error response example</span></span>

### <a name="description"></a><span data-ttu-id="ddcaa-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="ddcaa-136">Description</span></span>

<span data-ttu-id="ddcaa-137">El siguiente ejemplo de cuerpo SOAP muestra una respuesta de error que está causada por un incorrecta [FolderId](folderid.md) en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ddcaa-137">The following SOAP body example shows an error response that is caused by an incorrect [FolderId](folderid.md) in the request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="ddcaa-138">Código</span><span class="sxs-lookup"><span data-stu-id="ddcaa-138">Code</span></span>

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
    <GetFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                       xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:GetFolderResponseMessage ResponseClass="Error">
          <m:MessageText>Id is malformed.</m:MessageText>
          <m:ResponseCode>ErrorInvalidIdMalformed</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:Folders />
        </m:GetFolderResponseMessage>
      </m:ResponseMessages>
    </GetFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="response-elements"></a><span data-ttu-id="ddcaa-139">Elementos de respuesta</span><span class="sxs-lookup"><span data-stu-id="ddcaa-139">Response elements</span></span>

<span data-ttu-id="ddcaa-140">Esta respuesta de error **GetFolder** incluye los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="ddcaa-140">This **GetFolder** error response includes the following elements:</span></span> 
  
- [<span data-ttu-id="ddcaa-141">GetFolderResponse</span><span class="sxs-lookup"><span data-stu-id="ddcaa-141">GetFolderResponse</span></span>](getfolderresponse.md)
    
- [<span data-ttu-id="ddcaa-142">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="ddcaa-142">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="ddcaa-143">GetFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="ddcaa-143">GetFolderResponseMessage</span></span>](getfolderresponsemessage.md)
    
- [<span data-ttu-id="ddcaa-144">MessageText</span><span class="sxs-lookup"><span data-stu-id="ddcaa-144">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="ddcaa-145">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="ddcaa-145">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="ddcaa-146">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="ddcaa-146">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="ddcaa-147">Carpetas</span><span class="sxs-lookup"><span data-stu-id="ddcaa-147">Folders</span></span>](folders-ex15websvcsotherref.md)
    
## <a name="version-differences"></a><span data-ttu-id="ddcaa-148">Diferencias de versión</span><span class="sxs-lookup"><span data-stu-id="ddcaa-148">Version differences</span></span>

<span data-ttu-id="ddcaa-149">Para las aplicaciones de ese destino Exchange Online, Exchange Online como parte de Office 365 o una versión local de Exchange a partir de Exchange 2013, los permisos de carpetas no se devuelven cuando el elemento [BaseShape](baseshape.md) tiene un valor de **AllProperties** en la solicitud de operación [GetFolder](getfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="ddcaa-149">For applications that target Exchange Online, Exchange Online as part of Office 365, or an on-premises version of Exchange starting with Exchange 2013, folder permissions are not returned when the [BaseShape](baseshape.md) element has a value of **AllProperties** in the [GetFolder](getfolder-operation.md) operation request.</span></span> <span data-ttu-id="ddcaa-150">Para recuperar los permisos de carpeta, agregue el elemento [PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) al elemento [AdditionalProperties](additionalproperties.md) en la solicitud de **GetFolder** .</span><span class="sxs-lookup"><span data-stu-id="ddcaa-150">To retrieve folder permissions, add the [PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) element to the [AdditionalProperties](additionalproperties.md) element in the **GetFolder** request.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ddcaa-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="ddcaa-151">See also</span></span>



- [<span data-ttu-id="ddcaa-152">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="ddcaa-152">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

