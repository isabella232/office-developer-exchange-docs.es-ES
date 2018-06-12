---
title: Operación ArchiveItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1af216b3-13ea-498e-b4fc-23513755d731
description: Busque información sobre la EWS ArchiveItem operación.
ms.openlocfilehash: 954943acefef8da61e92de5f8857ca023ca4fc9f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763549"
---
# <a name="archiveitem-operation"></a><span data-ttu-id="0b2eb-103">Operación ArchiveItem</span><span class="sxs-lookup"><span data-stu-id="0b2eb-103">ArchiveItem operation</span></span>

<span data-ttu-id="0b2eb-104">Obtenga información acerca de la operación de EWS **ArchiveItem** .</span><span class="sxs-lookup"><span data-stu-id="0b2eb-104">Find information about the **ArchiveItem** EWS operation.</span></span> 
  
<span data-ttu-id="0b2eb-105">La operación de **ArchiveItem** mueve un elemento en el buzón de archivo del usuario de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="0b2eb-105">The **ArchiveItem** operation moves an item into the mailbox user's archive mailbox.</span></span> 
  
<span data-ttu-id="0b2eb-106">Esta operación se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0b2eb-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-archiveitem-operation"></a><span data-ttu-id="0b2eb-107">Mediante la operación ArchiveItem</span><span class="sxs-lookup"><span data-stu-id="0b2eb-107">Using the ArchiveItem operation</span></span>

<span data-ttu-id="0b2eb-108">La operación **ArchiveItem** toma dos argumentos en la solicitud que identifican los elementos que desee mover el buzón de archivo y la carpeta de destino para esos elementos.</span><span class="sxs-lookup"><span data-stu-id="0b2eb-108">The **ArchiveItem** operation takes two arguments in the request that identify the items to move to the archive mailbox and the destination folder for those items.</span></span> <span data-ttu-id="0b2eb-109">Un buzón de archivo debe estar habilitado en orden para esta operación para que funcione.</span><span class="sxs-lookup"><span data-stu-id="0b2eb-109">An archive mailbox must be enabled in order for this operation to work.</span></span> <span data-ttu-id="0b2eb-110">Para obtener información acerca de cómo habilitar un buzón de archivo, vea [Administrar en archivos locales](http://technet.microsoft.com/en-us/library/jj651146.aspx).</span><span class="sxs-lookup"><span data-stu-id="0b2eb-110">For information about how to enable an archive mailbox, see [Manage In-Place Archives](http://technet.microsoft.com/en-us/library/jj651146.aspx).</span></span>
  
### <a name="archiveitem-operation-soap-headers"></a><span data-ttu-id="0b2eb-111">Encabezados SOAP de operación de ArchiveItem</span><span class="sxs-lookup"><span data-stu-id="0b2eb-111">ArchiveItem operation SOAP headers</span></span>

<span data-ttu-id="0b2eb-112">La operación de **ArchiveItem** puede utilizar los encabezados SOAP que se enumeran en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="0b2eb-112">The **ArchiveItem** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="0b2eb-113">**Nombre de encabezado**</span><span class="sxs-lookup"><span data-stu-id="0b2eb-113">**Header name**</span></span>|<span data-ttu-id="0b2eb-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="0b2eb-114">**Element**</span></span>|<span data-ttu-id="0b2eb-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0b2eb-115">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0b2eb-116">**Suplantación**</span><span class="sxs-lookup"><span data-stu-id="0b2eb-116">**Impersonation**</span></span> <br/> |[<span data-ttu-id="0b2eb-117">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="0b2eb-117">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="0b2eb-118">Identifica el usuario que está realizando la suplantación de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="0b2eb-118">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="0b2eb-119">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="0b2eb-119">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="0b2eb-120">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="0b2eb-120">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="0b2eb-121">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="0b2eb-121">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="0b2eb-122">Identifica la referencia cultural, como se define en RFC 3066, **etiquetas para la identificación de idiomas**, que se usará para tener acceso al buzón.</span><span class="sxs-lookup"><span data-stu-id="0b2eb-122">Identifies the culture, as defined in RFC 3066, **Tags for the Identification of Languages**, to be used to access the mailbox.</span></span> <span data-ttu-id="0b2eb-123">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="0b2eb-123">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="0b2eb-124">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="0b2eb-124">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="0b2eb-125">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="0b2eb-125">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="0b2eb-126">Identifica la versión del esquema para la solicitud de la operación.</span><span class="sxs-lookup"><span data-stu-id="0b2eb-126">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="0b2eb-127">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="0b2eb-127">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="0b2eb-128">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="0b2eb-128">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="0b2eb-129">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="0b2eb-129">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="0b2eb-130">Identifica la versión del servidor que ha respondido a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0b2eb-130">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="0b2eb-131">Este encabezado es aplicable a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="0b2eb-131">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="archiveitem-operation-request-example-move-an-item-to-the-archive-inbox-folder"></a><span data-ttu-id="0b2eb-132">Ejemplo de solicitud de operación de ArchiveItem: mover un elemento a la carpeta Bandeja de entrada de archivo</span><span class="sxs-lookup"><span data-stu-id="0b2eb-132">ArchiveItem operation request example: Move an item to the archive inbox folder</span></span>

<span data-ttu-id="0b2eb-133">El siguiente ejemplo de una solicitud de operación **ArchiveItem** muestra cómo mover un elemento a la carpeta Bandeja de entrada de archivo.</span><span class="sxs-lookup"><span data-stu-id="0b2eb-133">The following example of an **ArchiveItem** operation request shows how to move an item to the archive Inbox folder.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="0b2eb-134">Todos los identificadores de artículo y cambiar claves en este artículo se han abreviado para conservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="0b2eb-134">All item identifiers and change keys in this article have been shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013"/>
   </soap:Header>
   <soap:Body>
      <m:ArchiveItem>
         <m:ArchiveSourceFolderId>
            <t:DistinguishedFolderId Id="inbox"/>
         </m:ArchiveSourceFolderId>
         <m:ItemIds>
            <t:ItemId Id="AQMkG5BBwrQAAAxoAAAA=" ChangeKey="CQAAAHCtAAAAAAB7"/>
         </m:ItemIds>
      </m:ArchiveItem>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="0b2eb-135">La solicitud SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="0b2eb-135">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="0b2eb-136">ArchiveItem</span><span class="sxs-lookup"><span data-stu-id="0b2eb-136">ArchiveItem</span></span>](archiveitem.md)    
- [<span data-ttu-id="0b2eb-137">ArchiveSourceFolderId</span><span class="sxs-lookup"><span data-stu-id="0b2eb-137">ArchiveSourceFolderId</span></span>](archivesourcefolderid.md)    
- [<span data-ttu-id="0b2eb-138">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="0b2eb-138">DistinguishedFolderId</span></span>](distinguishedfolderid.md)    
- [<span data-ttu-id="0b2eb-139">ItemId</span><span class="sxs-lookup"><span data-stu-id="0b2eb-139">ItemIds</span></span>](itemids.md)   
- [<span data-ttu-id="0b2eb-140">ItemId</span><span class="sxs-lookup"><span data-stu-id="0b2eb-140">ItemId</span></span>](itemid.md)
    
## <a name="successful-archiveitem-operation-response"></a><span data-ttu-id="0b2eb-141">Respuesta es correcta de operación ArchiveItem</span><span class="sxs-lookup"><span data-stu-id="0b2eb-141">Successful ArchiveItem operation response</span></span>

<span data-ttu-id="0b2eb-142">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación de **ArchiveItem** para mover un elemento a un buzón de archivo.</span><span class="sxs-lookup"><span data-stu-id="0b2eb-142">The following example shows a successful response to an **ArchiveItem** operation request to move an item to an archive mailbox.</span></span> 
  
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
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <m:ArchiveItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                             xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
         <m:ResponseMessages>
            <m:ArchiveItemResponseMessage ResponseClass="Success">
               <m:ResponseCode>NoError</m:ResponseCode>
               <m:Items/>
            </m:ArchiveItemResponseMessage>
         </m:ResponseMessages>
      </m:ArchiveItemResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="0b2eb-143">La respuesta SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="0b2eb-143">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="0b2eb-144">ArchiveItemResponse</span><span class="sxs-lookup"><span data-stu-id="0b2eb-144">ArchiveItemResponse</span></span>](archiveitemresponse.md)    
- [<span data-ttu-id="0b2eb-145">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="0b2eb-145">ResponseMessages</span></span>](responsemessages.md)   
- [<span data-ttu-id="0b2eb-146">ArchiveItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="0b2eb-146">ArchiveItemResponseMessage</span></span>](archiveitemresponsemessage.md)    
- [<span data-ttu-id="0b2eb-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="0b2eb-147">ResponseCode</span></span>](responsecode.md)    
- [<span data-ttu-id="0b2eb-148">Items</span><span class="sxs-lookup"><span data-stu-id="0b2eb-148">Items</span></span>](items.md)
    
## <a name="archiveitem-operation-error-response"></a><span data-ttu-id="0b2eb-149">Respuesta de error de la operación de ArchiveItem</span><span class="sxs-lookup"><span data-stu-id="0b2eb-149">ArchiveItem operation error response</span></span>

<span data-ttu-id="0b2eb-150">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **ArchiveItem** .</span><span class="sxs-lookup"><span data-stu-id="0b2eb-150">The following example shows an error response to an **ArchiveItem** operation request.</span></span> <span data-ttu-id="0b2eb-151">Esta es una respuesta a una solicitud válida para archivar un elemento cuando un buzón de archivo no está habilitado para un usuario.</span><span class="sxs-lookup"><span data-stu-id="0b2eb-151">This is a response to a valid request to archive an item when an archive mailbox is not enabled for a user.</span></span> 
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="8" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <m:ArchiveItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                             xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
         <m:ResponseMessages>
            <m:ArchiveItemResponseMessage ResponseClass="Error">
               <m:MessageText>Archive mailbox is not enabled for this user.</m:MessageText>
               <m:ResponseCode>ErrorInvalidOperation</m:ResponseCode>
               <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
               <m:Items/>
            </m:ArchiveItemResponseMessage>
         </m:ResponseMessages>
      </m:ArchiveItemResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="0b2eb-152">La respuesta de error SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="0b2eb-152">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="0b2eb-153">ArchiveItemResponse</span><span class="sxs-lookup"><span data-stu-id="0b2eb-153">ArchiveItemResponse</span></span>](archiveitemresponse.md)    
- [<span data-ttu-id="0b2eb-154">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="0b2eb-154">ResponseMessages</span></span>](responsemessages.md)    
- [<span data-ttu-id="0b2eb-155">ArchiveItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="0b2eb-155">ArchiveItemResponseMessage</span></span>](archiveitemresponsemessage.md)    
- [<span data-ttu-id="0b2eb-156">MessageText</span><span class="sxs-lookup"><span data-stu-id="0b2eb-156">MessageText</span></span>](messagetext.md)    
- [<span data-ttu-id="0b2eb-157">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="0b2eb-157">ResponseCode</span></span>](responsecode.md)    
- [<span data-ttu-id="0b2eb-158">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="0b2eb-158">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)    
- [<span data-ttu-id="0b2eb-159">Items</span><span class="sxs-lookup"><span data-stu-id="0b2eb-159">Items</span></span>](items.md)
    
<span data-ttu-id="0b2eb-160">Para códigos de error adicionales que son genéricos para EWS y específicos de esta operación, vea [ResponseCode](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="0b2eb-160">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0b2eb-161">Ver también</span><span class="sxs-lookup"><span data-stu-id="0b2eb-161">See also</span></span>

- [<span data-ttu-id="0b2eb-162">Operaciones de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="0b2eb-162">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md) 
- [<span data-ttu-id="0b2eb-163">Archivado en EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="0b2eb-163">Archiving in EWS in Exchange</span></span>](http://msdn.microsoft.com/library/78ae179b-ae4f-4f64-911a-e0c70e0fa314%28Office.15%29.aspx)
    

