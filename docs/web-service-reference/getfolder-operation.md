---
title: Operación GetFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
api_name:
- GetFolder
api_type:
- schema
ms.assetid: 355bcf93-dc71-4493-b177-622afac5fdb9
description: La operación GetFolder obtiene carpetas del almacén de Exchange.
localization_priority: Priority
ms.openlocfilehash: 9d511f309b9210fd9b5a49ff6c60bc7982992973
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459184"
---
# <a name="getfolder-operation"></a><span data-ttu-id="0ee72-103">Operación GetFolder</span><span class="sxs-lookup"><span data-stu-id="0ee72-103">GetFolder operation</span></span>

<span data-ttu-id="0ee72-104">La operación **GetFolder** obtiene carpetas del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="0ee72-104">The **GetFolder** operation gets folders from the Exchange store.</span></span> 
  
## <a name="getfolder-request-example"></a><span data-ttu-id="0ee72-105">Ejemplo de solicitud GetFolder</span><span class="sxs-lookup"><span data-stu-id="0ee72-105">GetFolder request example</span></span>

### <a name="description"></a><span data-ttu-id="0ee72-106">Description</span><span class="sxs-lookup"><span data-stu-id="0ee72-106">Description</span></span>

<span data-ttu-id="0ee72-107">El siguiente ejemplo de una solicitud **GetFolder** muestra cómo obtener un identificador de carpeta, un nombre para mostrar, el número de elementos de esa carpeta, el número de carpetas secundarias y el número de elementos no leídos de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="0ee72-107">The following example of a **GetFolder** request shows how to obtain a folder identifier, display name, the count of items in that folder, the count of child folders, and the number of unread items in the folder.</span></span> 
  
### <a name="code"></a><span data-ttu-id="0ee72-108">Código</span><span class="sxs-lookup"><span data-stu-id="0ee72-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
   xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetFolder xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

### <a name="request-elements"></a><span data-ttu-id="0ee72-109">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="0ee72-109">Request elements</span></span>

<span data-ttu-id="0ee72-110">Esta solicitud **GetFolder** incluye los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="0ee72-110">This **GetFolder** request includes the following elements:</span></span> 
  
- [<span data-ttu-id="0ee72-111">GetFolder</span><span class="sxs-lookup"><span data-stu-id="0ee72-111">GetFolder</span></span>](getfolder.md)
    
- [<span data-ttu-id="0ee72-112">FolderShape</span><span class="sxs-lookup"><span data-stu-id="0ee72-112">FolderShape</span></span>](foldershape.md)
    
- [<span data-ttu-id="0ee72-113">BaseShape</span><span class="sxs-lookup"><span data-stu-id="0ee72-113">BaseShape</span></span>](baseshape.md)
    
- [<span data-ttu-id="0ee72-114">FolderIds</span><span class="sxs-lookup"><span data-stu-id="0ee72-114">FolderIds</span></span>](folderids.md)
    
- [<span data-ttu-id="0ee72-115">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="0ee72-115">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
<span data-ttu-id="0ee72-116">Vea el esquema para ver los elementos adicionales que puede usar para formar una solicitud **GetFolder** .</span><span class="sxs-lookup"><span data-stu-id="0ee72-116">See the schema for additional elements that you can use to form a **GetFolder** request.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="0ee72-117">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="0ee72-117">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span> 
  
## <a name="getfolder-response-example"></a><span data-ttu-id="0ee72-118">Ejemplo de respuesta GetFolder</span><span class="sxs-lookup"><span data-stu-id="0ee72-118">GetFolder response example</span></span>

### <a name="description"></a><span data-ttu-id="0ee72-119">Description</span><span class="sxs-lookup"><span data-stu-id="0ee72-119">Description</span></span>

<span data-ttu-id="0ee72-120">El siguiente ejemplo del cuerpo del Protocolo simple de acceso a objetos (SOAP) muestra una respuesta correcta a la solicitud **GetFolder** .</span><span class="sxs-lookup"><span data-stu-id="0ee72-120">The following Simple Object Access Protocol (SOAP) body example shows a successful response to the **GetFolder** request.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="0ee72-121">El identificador de la carpeta y la clave de cambio se han abreviado para preservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="0ee72-121">The folder ID and the change key have been shortened to preserve readability.</span></span> 
  
### <a name="code"></a><span data-ttu-id="0ee72-122">Código</span><span class="sxs-lookup"><span data-stu-id="0ee72-122">Code</span></span>

```XML
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                       xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="response-elements"></a><span data-ttu-id="0ee72-123">Elementos de respuesta</span><span class="sxs-lookup"><span data-stu-id="0ee72-123">Response elements</span></span>

<span data-ttu-id="0ee72-124">Esta respuesta **GetFolder** incluye los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="0ee72-124">This **GetFolder** response includes the following elements:</span></span> 
  
- [<span data-ttu-id="0ee72-125">GetFolderResponse</span><span class="sxs-lookup"><span data-stu-id="0ee72-125">GetFolderResponse</span></span>](getfolderresponse.md)
    
- [<span data-ttu-id="0ee72-126">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="0ee72-126">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="0ee72-127">GetFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="0ee72-127">GetFolderResponseMessage</span></span>](getfolderresponsemessage.md)
    
- [<span data-ttu-id="0ee72-128">Folders</span><span class="sxs-lookup"><span data-stu-id="0ee72-128">Folders</span></span>](folders-ex15websvcsotherref.md)
    
- [<span data-ttu-id="0ee72-129">Folder</span><span class="sxs-lookup"><span data-stu-id="0ee72-129">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="0ee72-130">FolderId</span><span class="sxs-lookup"><span data-stu-id="0ee72-130">FolderId</span></span>](folderid.md)
    
- [<span data-ttu-id="0ee72-131">DisplayName (cadena)</span><span class="sxs-lookup"><span data-stu-id="0ee72-131">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="0ee72-132">TotalCount</span><span class="sxs-lookup"><span data-stu-id="0ee72-132">TotalCount</span></span>](totalcount.md)
    
- [<span data-ttu-id="0ee72-133">ChildFolderCount</span><span class="sxs-lookup"><span data-stu-id="0ee72-133">ChildFolderCount</span></span>](childfoldercount.md)
    
- [<span data-ttu-id="0ee72-134">UnreadCount</span><span class="sxs-lookup"><span data-stu-id="0ee72-134">UnreadCount</span></span>](unreadcount.md)
    
## <a name="getfolder-error-response-example"></a><span data-ttu-id="0ee72-135">Ejemplo de respuesta de error de GetFolder</span><span class="sxs-lookup"><span data-stu-id="0ee72-135">GetFolder Error response example</span></span>

### <a name="description"></a><span data-ttu-id="0ee72-136">Description</span><span class="sxs-lookup"><span data-stu-id="0ee72-136">Description</span></span>

<span data-ttu-id="0ee72-137">El siguiente ejemplo de cuerpo de SOAP muestra una respuesta de error causada por un [FolderId](folderid.md) incorrecto en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0ee72-137">The following SOAP body example shows an error response that is caused by an incorrect [FolderId](folderid.md) in the request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="0ee72-138">Código</span><span class="sxs-lookup"><span data-stu-id="0ee72-138">Code</span></span>

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
    <GetFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                       xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="response-elements"></a><span data-ttu-id="0ee72-139">Elementos de respuesta</span><span class="sxs-lookup"><span data-stu-id="0ee72-139">Response elements</span></span>

<span data-ttu-id="0ee72-140">La respuesta de error **GetFolder** incluye los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="0ee72-140">This **GetFolder** error response includes the following elements:</span></span> 
  
- [<span data-ttu-id="0ee72-141">GetFolderResponse</span><span class="sxs-lookup"><span data-stu-id="0ee72-141">GetFolderResponse</span></span>](getfolderresponse.md)
    
- [<span data-ttu-id="0ee72-142">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="0ee72-142">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="0ee72-143">GetFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="0ee72-143">GetFolderResponseMessage</span></span>](getfolderresponsemessage.md)
    
- [<span data-ttu-id="0ee72-144">MessageText</span><span class="sxs-lookup"><span data-stu-id="0ee72-144">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="0ee72-145">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="0ee72-145">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="0ee72-146">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="0ee72-146">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="0ee72-147">Folders</span><span class="sxs-lookup"><span data-stu-id="0ee72-147">Folders</span></span>](folders-ex15websvcsotherref.md)
    
## <a name="version-differences"></a><span data-ttu-id="0ee72-148">Diferencias de versión</span><span class="sxs-lookup"><span data-stu-id="0ee72-148">Version differences</span></span>

<span data-ttu-id="0ee72-149">Para las aplicaciones dirigidas a Exchange Online, Exchange online como parte de Office 365 o a una versión local de Exchange a partir de Exchange 2013, no se devuelven permisos de carpeta cuando el elemento [BaseShape](baseshape.md) tiene un valor de **AllProperties** en la solicitud de operación [GetFolder](getfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="0ee72-149">For applications that target Exchange Online, Exchange Online as part of Office 365, or an on-premises version of Exchange starting with Exchange 2013, folder permissions are not returned when the [BaseShape](baseshape.md) element has a value of **AllProperties** in the [GetFolder](getfolder-operation.md) operation request.</span></span> <span data-ttu-id="0ee72-150">Para recuperar los permisos de carpeta, agregue el elemento [PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) al elemento [AdditionalProperties](additionalproperties.md) en la solicitud **GetFolder** .</span><span class="sxs-lookup"><span data-stu-id="0ee72-150">To retrieve folder permissions, add the [PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) element to the [AdditionalProperties](additionalproperties.md) element in the **GetFolder** request.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0ee72-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="0ee72-151">See also</span></span>



- [<span data-ttu-id="0ee72-152">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="0ee72-152">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

