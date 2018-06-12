---
title: Operación MarkAllItemsAsRead
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ea5b1cb6-6998-46fb-a99c-a6d3da77591f
description: Busque información sobre la EWS MarkAllItemsAsRead operación.
ms.openlocfilehash: 995a6219f0a3b41bddb0d65c875d981322e1ce78
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836354"
---
# <a name="markallitemsasread-operation"></a><span data-ttu-id="0362a-103">Operación MarkAllItemsAsRead</span><span class="sxs-lookup"><span data-stu-id="0362a-103">MarkAllItemsAsRead operation</span></span>

<span data-ttu-id="0362a-104">Obtenga información acerca de la operación de EWS **MarkAllItemsAsRead** .</span><span class="sxs-lookup"><span data-stu-id="0362a-104">Find information about the **MarkAllItemsAsRead** EWS operation.</span></span> 
  
<span data-ttu-id="0362a-105">La operación **MarkAllItemsAsRead** establece la propiedad [estáleído](isread.md) en todos los elementos, en una o varias carpetas, para indicar que todos los elementos son leídos o no leídos.</span><span class="sxs-lookup"><span data-stu-id="0362a-105">The **MarkAllItemsAsRead** operation sets the [IsRead](isread.md) property on all items, in one or more folders, to indicate that all items are either read or unread.</span></span> 
  
<span data-ttu-id="0362a-106">Esta operación se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0362a-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-markallitemsasread-operation"></a><span data-ttu-id="0362a-107">Mediante la operación MarkAllItemsAsRead</span><span class="sxs-lookup"><span data-stu-id="0362a-107">Using the MarkAllItemsAsRead operation</span></span>

<span data-ttu-id="0362a-108">La operación de **MarkAllItemsAsRead** puede establecer la propiedad [estáleído](isread.md) en todos los elementos en carpetas identificados por el identificador de la carpeta de Exchange Web Services (EWS) o el nombre de la carpeta de Exchange de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="0362a-108">The **MarkAllItemsAsRead** operation can set the [IsRead](isread.md) property on all items in folders identified by either the Exchange Web Services (EWS) folder identifier or the default Exchange folder name.</span></span> <span data-ttu-id="0362a-109">La operación de **MarkAllItemsAsRead** también puede suprimir el envío de confirmaciones de lectura para los elementos marcados como leídos.</span><span class="sxs-lookup"><span data-stu-id="0362a-109">The **MarkAllItemsAsRead** operation can also suppress the sending of read receipts for items marked as read.</span></span> 
  
### <a name="markallitemsasread-operation-soap-headers"></a><span data-ttu-id="0362a-110">Encabezados SOAP de operación de MarkAllItemsAsRead</span><span class="sxs-lookup"><span data-stu-id="0362a-110">MarkAllItemsAsRead operation SOAP headers</span></span>

<span data-ttu-id="0362a-111">La operación de **MarkAllItemsAsRead** puede utilizar los encabezados SOAP que se enumeran en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="0362a-111">The **MarkAllItemsAsRead** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="0362a-112">**Nombre de encabezado**</span><span class="sxs-lookup"><span data-stu-id="0362a-112">**Header name**</span></span>|<span data-ttu-id="0362a-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="0362a-113">**Element**</span></span>|<span data-ttu-id="0362a-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0362a-114">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0362a-115">**Suplantación**</span><span class="sxs-lookup"><span data-stu-id="0362a-115">**Impersonation**</span></span> <br/> |[<span data-ttu-id="0362a-116">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="0362a-116">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="0362a-117">Identifica el usuario que está realizando la suplantación de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="0362a-117">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="0362a-118">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="0362a-118">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="0362a-119">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="0362a-119">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="0362a-120">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="0362a-120">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="0362a-121">Identifica la referencia cultural, como se define en RFC 3066, "Etiquetas para la identificación de idiomas," que se utilizará para acceder al buzón.</span><span class="sxs-lookup"><span data-stu-id="0362a-121">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="0362a-122">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="0362a-122">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="0362a-123">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="0362a-123">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="0362a-124">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="0362a-124">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="0362a-125">Identifica la versión del esquema para la solicitud de la operación.</span><span class="sxs-lookup"><span data-stu-id="0362a-125">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="0362a-126">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="0362a-126">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="0362a-127">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="0362a-127">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="0362a-128">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="0362a-128">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="0362a-129">Identifica la versión del servidor que ha respondido a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0362a-129">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="0362a-130">Este encabezado es aplicable a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="0362a-130">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="markallitemsasread-operation-request-example-mark-all-items-in-a-folder-as-read"></a><span data-ttu-id="0362a-131">Ejemplo de solicitud de operación de MarkAllItemsAsRead: marcar todos los elementos de una carpeta como leídos</span><span class="sxs-lookup"><span data-stu-id="0362a-131">MarkAllItemsAsRead operation request example: Mark all items in a folder as read</span></span>

<span data-ttu-id="0362a-132">El siguiente ejemplo de una solicitud de operación **MarkAllItemsAsRead** muestra cómo establecer la propiedad [estáleído](isread.md) , que también se llama a la marca de lectura, en **true** en todos los elementos de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="0362a-132">The following example of a **MarkAllItemsAsRead** operation request shows how to set the [IsRead](isread.md) property, which is also called the read flag, to **true** on all items in a folder.</span></span> <span data-ttu-id="0362a-133">En este ejemplo se muestra también que se leen confirmaciones no se envían en respuesta a las solicitudes de confirmación de lectura.</span><span class="sxs-lookup"><span data-stu-id="0362a-133">This example also shows that read receipts are not sent in response to any read receipt requests.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="0362a-134">Todos los identificadores de artículo y cambiar claves en este artículo se han abreviado para conservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="0362a-134">All item identifiers and change keys in this article have been shortened to preserve readability.</span></span> <span data-ttu-id="0362a-135">Cambiar claves no son necesarias para esta operación.</span><span class="sxs-lookup"><span data-stu-id="0362a-135">Change keys are not required for this operation.</span></span> 
  
```XML
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body>
      <m:MarkAllItemsAsRead>
         <m:ReadFlag>true</m:ReadFlag>
         <m:SuppressReadReceipts>true</m:SuppressReadReceipts>
         <m:FolderIds>
            <t:FolderId Id="AAMkADEzOTExYZRAAA=" 
                        ChangeKey="AQAAAAA3vA==" />
         </m:FolderIds>
      </m:MarkAllItemsAsRead>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="0362a-136">La solicitud SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="0362a-136">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="0362a-137">MarkAllItemsAsRead</span><span class="sxs-lookup"><span data-stu-id="0362a-137">MarkAllItemsAsRead</span></span>](markallitemsasread.md)
    
- [<span data-ttu-id="0362a-138">ReadFlag</span><span class="sxs-lookup"><span data-stu-id="0362a-138">ReadFlag</span></span>](readflag.md)
    
- [<span data-ttu-id="0362a-139">SuppressReadReceipts</span><span class="sxs-lookup"><span data-stu-id="0362a-139">SuppressReadReceipts</span></span>](suppressreadreceipts.md)
    
- [<span data-ttu-id="0362a-140">FolderIds</span><span class="sxs-lookup"><span data-stu-id="0362a-140">FolderIds</span></span>](folderids.md)
    
- [<span data-ttu-id="0362a-141">FolderId</span><span class="sxs-lookup"><span data-stu-id="0362a-141">FolderId</span></span>](folderid.md)
    
## <a name="successful-markallitemsasread-operation-response"></a><span data-ttu-id="0362a-142">Respuesta es correcta de operación MarkAllItemsAsRead</span><span class="sxs-lookup"><span data-stu-id="0362a-142">Successful MarkAllItemsAsRead operation response</span></span>

<span data-ttu-id="0362a-143">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación de **MarkAllItemsAsRead** para marcar todos los elementos de una carpeta como leídos.</span><span class="sxs-lookup"><span data-stu-id="0362a-143">The following example shows a successful response to a **MarkAllItemsAsRead** operation request to mark all items in a folder as read.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="545" 
                           MinorBuildNumber="11" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <m:MarkAllItemsAsReadResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                                    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
         <m:ResponseMessages>
            <m:MarkAllItemsAsReadResponseMessage ResponseClass="Success">
               <m:ResponseCode>NoError</m:ResponseCode>
            </m:MarkAllItemsAsReadResponseMessage>
         </m:ResponseMessages>
      </m:MarkAllItemsAsReadResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="0362a-144">La respuesta SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="0362a-144">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="0362a-145">MarkAllItemsAsReadResponse</span><span class="sxs-lookup"><span data-stu-id="0362a-145">MarkAllItemsAsReadResponse</span></span>](markallitemsasreadresponse.md)
    
- [<span data-ttu-id="0362a-146">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="0362a-146">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="0362a-147">MarkAllItemsAsReadResponseMessage</span><span class="sxs-lookup"><span data-stu-id="0362a-147">MarkAllItemsAsReadResponseMessage</span></span>](markallitemsasreadresponsemessage.md)
    
- [<span data-ttu-id="0362a-148">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="0362a-148">ResponseCode</span></span>](responsecode.md)
    
## <a name="markallitemsasread-operation-request-example-mark-all-items-in-a-folder-as-unread"></a><span data-ttu-id="0362a-149">Ejemplo de solicitud de operación de MarkAllItemsAsRead: marcar todos los elementos de una carpeta como no leídos</span><span class="sxs-lookup"><span data-stu-id="0362a-149">MarkAllItemsAsRead operation request example: Mark all items in a folder as unread</span></span>

<span data-ttu-id="0362a-150">El siguiente ejemplo de una solicitud de operación **MarkAllItemsAsRead** muestra cómo establecer la propiedad [estáleído](isread.md) en **false** en todos los elementos de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="0362a-150">The following example of a **MarkAllItemsAsRead** operation request shows how to set the [IsRead](isread.md) property to **false** on all items in a folder.</span></span> <span data-ttu-id="0362a-151">En este ejemplo se muestra también que se leen confirmaciones no se envían en respuesta a las solicitudes de confirmación de lectura.</span><span class="sxs-lookup"><span data-stu-id="0362a-151">This example also shows that read receipts are not sent in response to any read receipt requests.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body>
      <m:MarkAllItemsAsRead>
         <m:ReadFlag>false</m:ReadFlag>
         <m:SuppressReadReceipts>true</m:SuppressReadReceipts>
         <m:FolderIds>
            <t:FolderId Id="AAMkADEzOTExYZRAAA=" 
                        ChangeKey="AQAAAAA3vA==" />
         </m:FolderIds>
      </m:MarkAllItemsAsRead>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="0362a-152">Una respuesta correcta a una solicitud para marcar todos los elementos como leídos es el mismo que la respuesta a una solicitud para marcar todos los elementos como no leídos.</span><span class="sxs-lookup"><span data-stu-id="0362a-152">A successful response to a request to mark all items as read is the same as the response to a request to mark all items as unread.</span></span>
  
<span data-ttu-id="0362a-153">La solicitud SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="0362a-153">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="0362a-154">MarkAllItemsAsRead</span><span class="sxs-lookup"><span data-stu-id="0362a-154">MarkAllItemsAsRead</span></span>](markallitemsasread.md)
    
- [<span data-ttu-id="0362a-155">ReadFlag</span><span class="sxs-lookup"><span data-stu-id="0362a-155">ReadFlag</span></span>](readflag.md)
    
- [<span data-ttu-id="0362a-156">SuppressReadReceipts</span><span class="sxs-lookup"><span data-stu-id="0362a-156">SuppressReadReceipts</span></span>](suppressreadreceipts.md)
    
- [<span data-ttu-id="0362a-157">FolderIds</span><span class="sxs-lookup"><span data-stu-id="0362a-157">FolderIds</span></span>](folderids.md)
    
- [<span data-ttu-id="0362a-158">FolderId</span><span class="sxs-lookup"><span data-stu-id="0362a-158">FolderId</span></span>](folderid.md)
    
## <a name="markallitemsasread-operation-error-response"></a><span data-ttu-id="0362a-159">Respuesta de error de la operación de MarkAllItemsAsRead</span><span class="sxs-lookup"><span data-stu-id="0362a-159">MarkAllItemsAsRead operation error response</span></span>

<span data-ttu-id="0362a-160">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación de **MarkAllItemsAsRead** para marcar todos los elementos de una carpeta como leídos o no leídos cuando la carpeta no existe en el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="0362a-160">The following example shows an error response to a **MarkAllItemsAsRead** operation request to mark all items in a folder as read or unread when the folder does not exist in the mailbox.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="545" 
                           MinorBuildNumber="11" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <m:MarkAllItemsAsReadResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                                    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
         <m:ResponseMessages>
            <m:MarkAllItemsAsReadResponseMessage ResponseClass="Error">
               <m:MessageText>The specified object was not found in the store.</m:MessageText>
               <m:ResponseCode>ErrorItemNotFound</m:ResponseCode>
               <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
            </m:MarkAllItemsAsReadResponseMessage>
         </m:ResponseMessages>
      </m:MarkAllItemsAsReadResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="0362a-161">La respuesta de error SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="0362a-161">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="0362a-162">MarkAllItemsAsReadResponse</span><span class="sxs-lookup"><span data-stu-id="0362a-162">MarkAllItemsAsReadResponse</span></span>](markallitemsasreadresponse.md)
    
- [<span data-ttu-id="0362a-163">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="0362a-163">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="0362a-164">MarkAllItemsAsReadResponseMessage</span><span class="sxs-lookup"><span data-stu-id="0362a-164">MarkAllItemsAsReadResponseMessage</span></span>](markallitemsasreadresponsemessage.md)
    
- [<span data-ttu-id="0362a-165">MessageText</span><span class="sxs-lookup"><span data-stu-id="0362a-165">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="0362a-166">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="0362a-166">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="0362a-167">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="0362a-167">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="0362a-168">Ver también</span><span class="sxs-lookup"><span data-stu-id="0362a-168">See also</span></span>

- [<span data-ttu-id="0362a-169">Operaciones de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="0362a-169">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="0362a-170">Operación FindFolder</span><span class="sxs-lookup"><span data-stu-id="0362a-170">FindFolder operation</span></span>](findfolder-operation.md)
    

