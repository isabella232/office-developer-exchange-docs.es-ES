---
title: Operación CreateFolderPath
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5a10aa5e-3f25-4ec3-a0b9-284c30918a1f
description: Buscar información sobre la operación de EWS de CreateFolderPath.
ms.openlocfilehash: a8d42cbef854d900c5fb6b72c730dd1e2b903aec
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458904"
---
# <a name="createfolderpath-operation"></a><span data-ttu-id="59ddc-103">Operación CreateFolderPath</span><span class="sxs-lookup"><span data-stu-id="59ddc-103">CreateFolderPath operation</span></span>

<span data-ttu-id="59ddc-104">Buscar información sobre la operación de EWS de **CreateFolderPath** .</span><span class="sxs-lookup"><span data-stu-id="59ddc-104">Find information about the **CreateFolderPath** EWS operation.</span></span> 
  
<span data-ttu-id="59ddc-105">La operación **CreateFolderPath** crea una jerarquía de carpetas.</span><span class="sxs-lookup"><span data-stu-id="59ddc-105">The **CreateFolderPath** operation creates a folder hierarchy.</span></span> 
  
<span data-ttu-id="59ddc-106">Esta operación se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="59ddc-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-createfolderpath-operation"></a><span data-ttu-id="59ddc-107">Uso de la operación CreateFolderPath</span><span class="sxs-lookup"><span data-stu-id="59ddc-107">Using the CreateFolderPath operation</span></span>

<span data-ttu-id="59ddc-108">La solicitud de operación **CreateFolderPath** toma una matriz de carpetas y un identificador de carpeta principal y crea una jerarquía de carpetas basada en el orden de las carpetas en la matriz.</span><span class="sxs-lookup"><span data-stu-id="59ddc-108">The **CreateFolderPath** operation request takes an array of folders and a parent folder identifier and creates a folder hierarchy based on the order of the folders in the array.</span></span> 
  
### <a name="createfolderpath-operation-soap-headers"></a><span data-ttu-id="59ddc-109">Encabezados SOAP de operación CreateFolderPath</span><span class="sxs-lookup"><span data-stu-id="59ddc-109">CreateFolderPath operation SOAP headers</span></span>

<span data-ttu-id="59ddc-110">La operación **CreateFolderPath** puede usar los encabezados SOAP que se enumeran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="59ddc-110">The **CreateFolderPath** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="59ddc-111">**Nombre de encabezado**</span><span class="sxs-lookup"><span data-stu-id="59ddc-111">**Header name**</span></span>|<span data-ttu-id="59ddc-112">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="59ddc-112">**Element**</span></span>|<span data-ttu-id="59ddc-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="59ddc-113">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="59ddc-114">**Suplantación**</span><span class="sxs-lookup"><span data-stu-id="59ddc-114">**Impersonation**</span></span> <br/> |[<span data-ttu-id="59ddc-115">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="59ddc-115">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="59ddc-116">Identifica al usuario que está suplantando la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="59ddc-116">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="59ddc-117">Este encabezado se aplica a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="59ddc-117">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="59ddc-118">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="59ddc-118">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="59ddc-119">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="59ddc-119">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="59ddc-120">Identifica la referencia cultural, tal y como se define en RFC 3066, "etiquetas para la identificación de idiomas", que se va a usar para obtener acceso al buzón.</span><span class="sxs-lookup"><span data-stu-id="59ddc-120">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="59ddc-121">Este encabezado se aplica a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="59ddc-121">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="59ddc-122">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="59ddc-122">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="59ddc-123">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="59ddc-123">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="59ddc-124">Identifica la versión del esquema para la solicitud de operación.</span><span class="sxs-lookup"><span data-stu-id="59ddc-124">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="59ddc-125">Este encabezado se aplica a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="59ddc-125">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="59ddc-126">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="59ddc-126">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="59ddc-127">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="59ddc-127">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="59ddc-128">Identifica la versión del servidor que respondió a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="59ddc-128">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="59ddc-129">Este encabezado se aplica a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="59ddc-129">This header is applicable to a response.</span></span>  <br/> |
|<span data-ttu-id="59ddc-130">**TimeZoneContext**</span><span class="sxs-lookup"><span data-stu-id="59ddc-130">**TimeZoneContext**</span></span> <br/> |[<span data-ttu-id="59ddc-131">TimeZoneContext</span><span class="sxs-lookup"><span data-stu-id="59ddc-131">TimeZoneContext</span></span>](timezonecontext.md) <br/> |<span data-ttu-id="59ddc-132">Identifica el ámbito de la zona horaria para las propiedades de **fecha y** hora.</span><span class="sxs-lookup"><span data-stu-id="59ddc-132">Identifies the time zone scope for **DateTime** properties.</span></span> <span data-ttu-id="59ddc-133">Este encabezado se aplica a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="59ddc-133">This header is applicable to a request.</span></span>  <br/> |
   
## <a name="createfolderpath-operation-request-example-create-a-folder-hierarchy"></a><span data-ttu-id="59ddc-134">Ejemplo de solicitud de operación CreateFolderPath: crear una jerarquía de carpetas</span><span class="sxs-lookup"><span data-stu-id="59ddc-134">CreateFolderPath operation request example: Create a folder hierarchy</span></span>

<span data-ttu-id="59ddc-135">En el siguiente ejemplo de una solicitud de operación de **CreateFolderPath** , se muestra cómo crear una jerarquía de carpetas que se encuentra en tres carpetas de profundidad en la carpeta Bandeja de entrada predeterminada.</span><span class="sxs-lookup"><span data-stu-id="59ddc-135">The following example of a **CreateFolderPath** operation request shows how to create a folder hierarchy that is three folders deep in the default Inbox folder.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="59ddc-136">Todos los identificadores de elemento y las claves de cambio de este artículo se han reducido para preservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="59ddc-136">All item identifiers and change keys in this article have been shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
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

<span data-ttu-id="59ddc-137">El cuerpo SOAP de la solicitud contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="59ddc-137">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="59ddc-138">CreateFolderPath</span><span class="sxs-lookup"><span data-stu-id="59ddc-138">CreateFolderPath</span></span>](createfolderpath.md)
    
- [<span data-ttu-id="59ddc-139">ParentFolderId (TargetFolderIdType)</span><span class="sxs-lookup"><span data-stu-id="59ddc-139">ParentFolderId (TargetFolderIdType)</span></span>](parentfolderid-targetfolderidtype.md)
    
- [<span data-ttu-id="59ddc-140">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="59ddc-140">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="59ddc-141">RelativeFolderPath</span><span class="sxs-lookup"><span data-stu-id="59ddc-141">RelativeFolderPath</span></span>](relativefolderpath.md)
    
- [<span data-ttu-id="59ddc-142">Folder</span><span class="sxs-lookup"><span data-stu-id="59ddc-142">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="59ddc-143">DisplayName (cadena)</span><span class="sxs-lookup"><span data-stu-id="59ddc-143">DisplayName (string)</span></span>](displayname-string.md)
    
## <a name="successful-createfolderpath-operation-response"></a><span data-ttu-id="59ddc-144">Respuesta de operación CreateFolderPath correcta</span><span class="sxs-lookup"><span data-stu-id="59ddc-144">Successful CreateFolderPath operation response</span></span>

<span data-ttu-id="59ddc-145">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación de **CreateFolderPath** para crear una jerarquía de carpetas con tres carpetas de profundidad en la carpeta Bandeja de entrada predeterminada.</span><span class="sxs-lookup"><span data-stu-id="59ddc-145">The following example shows a successful response to a **CreateFolderPath** operation request to create a folder hierarchy three folders deep in the default Inbox folder.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="526" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <m:CreateFolderPathResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="59ddc-146">El cuerpo SOAP de respuesta contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="59ddc-146">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="59ddc-147">CreateFolderPathResponse</span><span class="sxs-lookup"><span data-stu-id="59ddc-147">CreateFolderPathResponse</span></span>](createfolderpathresponse.md)
    
- [<span data-ttu-id="59ddc-148">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="59ddc-148">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="59ddc-149">CreateFolderPathResponseMessage</span><span class="sxs-lookup"><span data-stu-id="59ddc-149">CreateFolderPathResponseMessage</span></span>](createfolderpathresponsemessage.md)
    
- [<span data-ttu-id="59ddc-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="59ddc-150">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="59ddc-151">Folders</span><span class="sxs-lookup"><span data-stu-id="59ddc-151">Folders</span></span>](folders-ex15websvcsotherref.md)
    
- [<span data-ttu-id="59ddc-152">Folder</span><span class="sxs-lookup"><span data-stu-id="59ddc-152">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="59ddc-153">FolderId</span><span class="sxs-lookup"><span data-stu-id="59ddc-153">FolderId</span></span>](folderid.md)
    
- [<span data-ttu-id="59ddc-154">DisplayName (cadena)</span><span class="sxs-lookup"><span data-stu-id="59ddc-154">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="59ddc-155">TotalCount</span><span class="sxs-lookup"><span data-stu-id="59ddc-155">TotalCount</span></span>](totalcount.md)
    
- [<span data-ttu-id="59ddc-156">ChildFolderCount</span><span class="sxs-lookup"><span data-stu-id="59ddc-156">ChildFolderCount</span></span>](childfoldercount.md)
    
- [<span data-ttu-id="59ddc-157">UnreadCount</span><span class="sxs-lookup"><span data-stu-id="59ddc-157">UnreadCount</span></span>](unreadcount.md)
    
## <a name="createfolderpath-operation-error-response"></a><span data-ttu-id="59ddc-158">Respuesta de error de operación de CreateFolderPath</span><span class="sxs-lookup"><span data-stu-id="59ddc-158">CreateFolderPath operation error response</span></span>

<span data-ttu-id="59ddc-159">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **CreateFolderPath** .</span><span class="sxs-lookup"><span data-stu-id="59ddc-159">The following example shows an error response to a **CreateFolderPath** operation request.</span></span> <span data-ttu-id="59ddc-160">Se trata de una respuesta a una solicitud para crear dos carpetas, la primera de las cuales no tiene establecida la propiedad nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="59ddc-160">This is a response to a request to create two folders, the first of which does not have a display name property set.</span></span> <span data-ttu-id="59ddc-161">No se puede crear la primera carpeta de la jerarquía sin una propiedad de nombre para mostrar y no se puede crear la segunda carpeta porque no se ha creado la carpeta principal en la jerarquía.</span><span class="sxs-lookup"><span data-stu-id="59ddc-161">The first folder in the hierarchy cannot be created without a display name property, and the second folder cannot be created because the parent folder in the hierarchy was not created.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="14" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <m:CreateFolderPathResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="59ddc-162">El cuerpo SOAP de respuesta de error contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="59ddc-162">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="59ddc-163">CreateFolderPathResponse</span><span class="sxs-lookup"><span data-stu-id="59ddc-163">CreateFolderPathResponse</span></span>](createfolderpathresponse.md)
    
- [<span data-ttu-id="59ddc-164">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="59ddc-164">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="59ddc-165">CreateFolderPathResponseMessage</span><span class="sxs-lookup"><span data-stu-id="59ddc-165">CreateFolderPathResponseMessage</span></span>](createfolderpathresponsemessage.md)
    
- [<span data-ttu-id="59ddc-166">MessageText</span><span class="sxs-lookup"><span data-stu-id="59ddc-166">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="59ddc-167">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="59ddc-167">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="59ddc-168">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="59ddc-168">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="59ddc-169">MessageXml</span><span class="sxs-lookup"><span data-stu-id="59ddc-169">MessageXml</span></span>](messagexml.md)
    
- [<span data-ttu-id="59ddc-170">FieldURI</span><span class="sxs-lookup"><span data-stu-id="59ddc-170">FieldURI</span></span>](fielduri.md)
    
- [<span data-ttu-id="59ddc-171">Folders</span><span class="sxs-lookup"><span data-stu-id="59ddc-171">Folders</span></span>](folders-ex15websvcsotherref.md)
    
<span data-ttu-id="59ddc-172">Para obtener los códigos de error adicionales que son genéricos para EWS y específicos de esta operación, vea [ResponseCode](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="59ddc-172">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="59ddc-173">Vea también</span><span class="sxs-lookup"><span data-stu-id="59ddc-173">See also</span></span>

- [<span data-ttu-id="59ddc-174">Operaciones de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="59ddc-174">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="59ddc-175">Operación FindFolder</span><span class="sxs-lookup"><span data-stu-id="59ddc-175">FindFolder operation</span></span>](findfolder-operation.md)
    

