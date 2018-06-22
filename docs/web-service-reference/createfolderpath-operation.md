---
title: Operación CreateFolderPath
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5a10aa5e-3f25-4ec3-a0b9-284c30918a1f
description: Busque información sobre la EWS CreateFolderPath operación.
ms.openlocfilehash: 22561e5086c144e25d7e04b68ec6674b87c4718d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763935"
---
# <a name="createfolderpath-operation"></a><span data-ttu-id="185fc-103">Operación CreateFolderPath</span><span class="sxs-lookup"><span data-stu-id="185fc-103">CreateFolderPath operation</span></span>

<span data-ttu-id="185fc-104">Obtenga información acerca de la operación de EWS **CreateFolderPath** .</span><span class="sxs-lookup"><span data-stu-id="185fc-104">Find information about the **CreateFolderPath** EWS operation.</span></span> 
  
<span data-ttu-id="185fc-105">La operación **CreateFolderPath** crea una jerarquía de carpetas.</span><span class="sxs-lookup"><span data-stu-id="185fc-105">The **CreateFolderPath** operation creates a folder hierarchy.</span></span> 
  
<span data-ttu-id="185fc-106">Esta operación se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="185fc-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-createfolderpath-operation"></a><span data-ttu-id="185fc-107">Mediante la operación CreateFolderPath</span><span class="sxs-lookup"><span data-stu-id="185fc-107">Using the CreateFolderPath operation</span></span>

<span data-ttu-id="185fc-108">La solicitud de operación **CreateFolderPath** toma una matriz de las carpetas y un identificador de la carpeta primaria y crea una jerarquía de carpetas según el orden de las carpetas en la matriz.</span><span class="sxs-lookup"><span data-stu-id="185fc-108">The **CreateFolderPath** operation request takes an array of folders and a parent folder identifier and creates a folder hierarchy based on the order of the folders in the array.</span></span> 
  
### <a name="createfolderpath-operation-soap-headers"></a><span data-ttu-id="185fc-109">Encabezados SOAP de operación de CreateFolderPath</span><span class="sxs-lookup"><span data-stu-id="185fc-109">CreateFolderPath operation SOAP headers</span></span>

<span data-ttu-id="185fc-110">La operación de **CreateFolderPath** puede utilizar los encabezados SOAP que se enumeran en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="185fc-110">The **CreateFolderPath** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="185fc-111">**Nombre de encabezado**</span><span class="sxs-lookup"><span data-stu-id="185fc-111">**Header name**</span></span>|<span data-ttu-id="185fc-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="185fc-112">**Element**</span></span>|<span data-ttu-id="185fc-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="185fc-113">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="185fc-114">**Suplantación**</span><span class="sxs-lookup"><span data-stu-id="185fc-114">**Impersonation**</span></span> <br/> |[<span data-ttu-id="185fc-115">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="185fc-115">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="185fc-116">Identifica el usuario que está realizando la suplantación de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="185fc-116">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="185fc-117">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="185fc-117">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="185fc-118">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="185fc-118">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="185fc-119">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="185fc-119">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="185fc-120">Identifica la referencia cultural, como se define en RFC 3066, "Etiquetas para la identificación de idiomas," que se utilizará para acceder al buzón.</span><span class="sxs-lookup"><span data-stu-id="185fc-120">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="185fc-121">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="185fc-121">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="185fc-122">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="185fc-122">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="185fc-123">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="185fc-123">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="185fc-124">Identifica la versión del esquema para la solicitud de la operación.</span><span class="sxs-lookup"><span data-stu-id="185fc-124">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="185fc-125">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="185fc-125">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="185fc-126">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="185fc-126">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="185fc-127">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="185fc-127">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="185fc-128">Identifica la versión del servidor que ha respondido a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="185fc-128">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="185fc-129">Este encabezado es aplicable a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="185fc-129">This header is applicable to a response.</span></span>  <br/> |
|<span data-ttu-id="185fc-130">**TimeZoneContext**</span><span class="sxs-lookup"><span data-stu-id="185fc-130">**TimeZoneContext**</span></span> <br/> |[<span data-ttu-id="185fc-131">TimeZoneContext</span><span class="sxs-lookup"><span data-stu-id="185fc-131">TimeZoneContext</span></span>](timezonecontext.md) <br/> |<span data-ttu-id="185fc-132">Identifica el ámbito de la zona horaria para las propiedades de **fecha y hora** .</span><span class="sxs-lookup"><span data-stu-id="185fc-132">Identifies the time zone scope for **DateTime** properties.</span></span> <span data-ttu-id="185fc-133">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="185fc-133">This header is applicable to a request.</span></span>  <br/> |
   
## <a name="createfolderpath-operation-request-example-create-a-folder-hierarchy"></a><span data-ttu-id="185fc-134">Ejemplo de solicitud de operación de CreateFolderPath: crear una jerarquía de carpetas</span><span class="sxs-lookup"><span data-stu-id="185fc-134">CreateFolderPath operation request example: Create a folder hierarchy</span></span>

<span data-ttu-id="185fc-135">El siguiente ejemplo de una solicitud de operación **CreateFolderPath** muestra cómo crear una jerarquía de carpetas que está tres carpetas profundidad en la carpeta Bandeja de entrada predeterminada.</span><span class="sxs-lookup"><span data-stu-id="185fc-135">The following example of a **CreateFolderPath** operation request shows how to create a folder hierarchy that is three folders deep in the default Inbox folder.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="185fc-136">Todos los identificadores de artículo y cambiar claves en este artículo se han abreviado para conservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="185fc-136">All item identifiers and change keys in this article have been shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
      <t:MailboxCulture>en-US</t:MailboxCulture>
      <t:TimeZoneContext>
         <t:TimeZoneDefinition Id="GMT Standard Time"/>
      </t:TimeZoneContext>
   </soap:Header>
   <soap:Body >
      <m:CreateFolderPath>
         <m:ParentFolderId>
            <t:DistinguishedFolderId Id="inbox"/>
         </m:ParentFolderId>
         <m:RelativeFolderPath>
            <t:Folder>
               <t:DisplayName>MyFirstLevelFolder</t:DisplayName>
            </t:Folder>
            <t:Folder>
               <t:DisplayName>MySecondLevelFolder</t:DisplayName>
            </t:Folder>
            <t:Folder>
               <t:DisplayName>MyThirdLevelFolder</t:DisplayName>
            </t:Folder>
         </m:RelativeFolderPath>
      </m:CreateFolderPath>
   </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="185fc-137">La solicitud SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="185fc-137">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="185fc-138">CreateFolderPath</span><span class="sxs-lookup"><span data-stu-id="185fc-138">CreateFolderPath</span></span>](createfolderpath.md)
    
- [<span data-ttu-id="185fc-139">ID (TargetFolderIdType)</span><span class="sxs-lookup"><span data-stu-id="185fc-139">ParentFolderId (TargetFolderIdType)</span></span>](parentfolderid-targetfolderidtype.md)
    
- [<span data-ttu-id="185fc-140">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="185fc-140">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="185fc-141">RelativeFolderPath</span><span class="sxs-lookup"><span data-stu-id="185fc-141">RelativeFolderPath</span></span>](relativefolderpath.md)
    
- [<span data-ttu-id="185fc-142">Folder</span><span class="sxs-lookup"><span data-stu-id="185fc-142">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="185fc-143">DisplayName (cadena)</span><span class="sxs-lookup"><span data-stu-id="185fc-143">DisplayName (string)</span></span>](displayname-string.md)
    
## <a name="successful-createfolderpath-operation-response"></a><span data-ttu-id="185fc-144">Respuesta es correcta de operación CreateFolderPath</span><span class="sxs-lookup"><span data-stu-id="185fc-144">Successful CreateFolderPath operation response</span></span>

<span data-ttu-id="185fc-145">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación de **CreateFolderPath** para crear una carpeta de carpetas de jerarquía de tres profundidad en la carpeta Bandeja de entrada predeterminada.</span><span class="sxs-lookup"><span data-stu-id="185fc-145">The following example shows a successful response to a **CreateFolderPath** operation request to create a folder hierarchy three folders deep in the default Inbox folder.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="526" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <m:CreateFolderPathResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                                  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
         <m:ResponseMessages>
            <m:CreateFolderPathResponseMessage ResponseClass="Success">
               <m:ResponseCode>NoError</m:ResponseCode>
               <m:Folders>
                  <t:Folder>
                     <t:FolderId Id="AAMkADEzOTExYisXAAA=" ChangeKey="AQAAABYAABq6Wxb"/>
                     <t:DisplayName>MyFirstLevelFolder</t:DisplayName>
                     <t:TotalCount>0</t:TotalCount>
                     <t:ChildFolderCount>0</t:ChildFolderCount>
                     <t:UnreadCount>0</t:UnreadCount>
                  </t:Folder>
               </m:Folders>
            </m:CreateFolderPathResponseMessage>
            <m:CreateFolderPathResponseMessage ResponseClass="Success">
               <m:ResponseCode>NoError</m:ResponseCode>
               <m:Folders>
                  <t:Folder>
                     <t:FolderId Id="AAMkADEzOTExm4QrAABqxisYAAA=" ChangeKey="AQAAABYAAAm4QrAABq6Wxg"/>
                     <t:DisplayName>MySecondLevelFolder</t:DisplayName>
                     <t:TotalCount>0</t:TotalCount>
                     <t:ChildFolderCount>0</t:ChildFolderCount>
                     <t:UnreadCount>0</t:UnreadCount>
                  </t:Folder>
               </m:Folders>
            </m:CreateFolderPathResponseMessage>
            <m:CreateFolderPathResponseMessage ResponseClass="Success">
               <m:ResponseCode>NoError</m:ResponseCode>
               <m:Folders>
                  <t:Folder>
                     <t:FolderId Id="AAMkADEzOTAABqxisZAAA=" ChangeKey="AQAAABYAA6Wxl"/>
                     <t:DisplayName>MyThirdLevelFolder</t:DisplayName>
                     <t:TotalCount>0</t:TotalCount>
                     <t:ChildFolderCount>0</t:ChildFolderCount>
                     <t:UnreadCount>0</t:UnreadCount>
                  </t:Folder>
               </m:Folders>
            </m:CreateFolderPathResponseMessage>
         </m:ResponseMessages>
      </m:CreateFolderPathResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="185fc-146">La respuesta SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="185fc-146">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="185fc-147">CreateFolderPathResponse</span><span class="sxs-lookup"><span data-stu-id="185fc-147">CreateFolderPathResponse</span></span>](createfolderpathresponse.md)
    
- [<span data-ttu-id="185fc-148">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="185fc-148">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="185fc-149">CreateFolderPathResponseMessage</span><span class="sxs-lookup"><span data-stu-id="185fc-149">CreateFolderPathResponseMessage</span></span>](createfolderpathresponsemessage.md)
    
- [<span data-ttu-id="185fc-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="185fc-150">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="185fc-151">Carpetas</span><span class="sxs-lookup"><span data-stu-id="185fc-151">Folders</span></span>](folders-ex15websvcsotherref.md)
    
- [<span data-ttu-id="185fc-152">Folder</span><span class="sxs-lookup"><span data-stu-id="185fc-152">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="185fc-153">FolderId</span><span class="sxs-lookup"><span data-stu-id="185fc-153">FolderId</span></span>](folderid.md)
    
- [<span data-ttu-id="185fc-154">DisplayName (cadena)</span><span class="sxs-lookup"><span data-stu-id="185fc-154">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="185fc-155">TotalCount</span><span class="sxs-lookup"><span data-stu-id="185fc-155">TotalCount</span></span>](totalcount.md)
    
- [<span data-ttu-id="185fc-156">ChildFolderCount</span><span class="sxs-lookup"><span data-stu-id="185fc-156">ChildFolderCount</span></span>](childfoldercount.md)
    
- [<span data-ttu-id="185fc-157">UnreadCount</span><span class="sxs-lookup"><span data-stu-id="185fc-157">UnreadCount</span></span>](unreadcount.md)
    
## <a name="createfolderpath-operation-error-response"></a><span data-ttu-id="185fc-158">Respuesta de error de la operación de CreateFolderPath</span><span class="sxs-lookup"><span data-stu-id="185fc-158">CreateFolderPath operation error response</span></span>

<span data-ttu-id="185fc-159">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **CreateFolderPath** .</span><span class="sxs-lookup"><span data-stu-id="185fc-159">The following example shows an error response to a **CreateFolderPath** operation request.</span></span> <span data-ttu-id="185fc-160">Esta es una respuesta a una solicitud para crear dos carpetas, la primera de las cuales no tiene una propiedad de nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="185fc-160">This is a response to a request to create two folders, the first of which does not have a display name property set.</span></span> <span data-ttu-id="185fc-161">No se puede crear la primera carpeta de la jerarquía sin una propiedad de nombre para mostrar y la segunda carpeta no se puede crear porque no se creó la carpeta principal de la jerarquía.</span><span class="sxs-lookup"><span data-stu-id="185fc-161">The first folder in the hierarchy cannot be created without a display name property, and the second folder cannot be created because the parent folder in the hierarchy was not created.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="14" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <m:CreateFolderPathResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                                  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
         <m:ResponseMessages>
            <m:CreateFolderPathResponseMessage ResponseClass="Error">
               <m:MessageText>The folder save operation failed due to invalid property values.</m:MessageText>
               <m:ResponseCode>ErrorFolderSavePropertyError</m:ResponseCode>
               <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
               <m:MessageXml>
                  <t:FieldURI FieldURI="folder:DisplayName"/>
               </m:MessageXml>
               <m:Folders/>
            </m:CreateFolderPathResponseMessage>
            <m:CreateFolderPathResponseMessage ResponseClass="Error">
               <m:MessageText>The specified parent folder could not be found.</m:MessageText>
               <m:ResponseCode>ErrorParentFolderNotFound</m:ResponseCode>
               <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
               <m:Folders/>
            </m:CreateFolderPathResponseMessage>
         </m:ResponseMessages>
      </m:CreateFolderPathResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="185fc-162">La respuesta de error SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="185fc-162">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="185fc-163">CreateFolderPathResponse</span><span class="sxs-lookup"><span data-stu-id="185fc-163">CreateFolderPathResponse</span></span>](createfolderpathresponse.md)
    
- [<span data-ttu-id="185fc-164">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="185fc-164">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="185fc-165">CreateFolderPathResponseMessage</span><span class="sxs-lookup"><span data-stu-id="185fc-165">CreateFolderPathResponseMessage</span></span>](createfolderpathresponsemessage.md)
    
- [<span data-ttu-id="185fc-166">MessageText</span><span class="sxs-lookup"><span data-stu-id="185fc-166">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="185fc-167">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="185fc-167">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="185fc-168">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="185fc-168">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="185fc-169">MessageXml</span><span class="sxs-lookup"><span data-stu-id="185fc-169">MessageXml</span></span>](messagexml.md)
    
- [<span data-ttu-id="185fc-170">FieldURI</span><span class="sxs-lookup"><span data-stu-id="185fc-170">FieldURI</span></span>](fielduri.md)
    
- [<span data-ttu-id="185fc-171">Carpetas</span><span class="sxs-lookup"><span data-stu-id="185fc-171">Folders</span></span>](folders-ex15websvcsotherref.md)
    
<span data-ttu-id="185fc-172">Para códigos de error adicionales que son genéricos para EWS y específicos de esta operación, vea [ResponseCode](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="185fc-172">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="185fc-173">Ver también</span><span class="sxs-lookup"><span data-stu-id="185fc-173">See also</span></span>

- [<span data-ttu-id="185fc-174">Operaciones de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="185fc-174">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="185fc-175">Operación FindFolder</span><span class="sxs-lookup"><span data-stu-id="185fc-175">FindFolder operation</span></span>](findfolder-operation.md)
    

