---
title: Operación MarkAllItemsAsRead
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ea5b1cb6-6998-46fb-a99c-a6d3da77591f
description: Buscar información sobre la operación de EWS de MarkAllItemsAsRead.
ms.openlocfilehash: aeeacea1cd5eed723f93027dd1ef75b34605fdfd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530533"
---
# <a name="markallitemsasread-operation"></a><span data-ttu-id="86a76-103">Operación MarkAllItemsAsRead</span><span class="sxs-lookup"><span data-stu-id="86a76-103">MarkAllItemsAsRead operation</span></span>

<span data-ttu-id="86a76-104">Buscar información sobre la operación de EWS de **MarkAllItemsAsRead** .</span><span class="sxs-lookup"><span data-stu-id="86a76-104">Find information about the **MarkAllItemsAsRead** EWS operation.</span></span> 
  
<span data-ttu-id="86a76-105">La operación **MarkAllItemsAsRead** establece la propiedad [IsRead](isread.md) en todos los elementos de una o varias carpetas para indicar que todos los elementos son leídos o no leídos.</span><span class="sxs-lookup"><span data-stu-id="86a76-105">The **MarkAllItemsAsRead** operation sets the [IsRead](isread.md) property on all items, in one or more folders, to indicate that all items are either read or unread.</span></span> 
  
<span data-ttu-id="86a76-106">Esta operación se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="86a76-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-markallitemsasread-operation"></a><span data-ttu-id="86a76-107">Uso de la operación MarkAllItemsAsRead</span><span class="sxs-lookup"><span data-stu-id="86a76-107">Using the MarkAllItemsAsRead operation</span></span>

<span data-ttu-id="86a76-108">La operación **MarkAllItemsAsRead** puede establecer la propiedad [IsRead](isread.md) en todos los elementos de las carpetas identificadas por el identificador de la carpeta de servicios web Exchange (EWS) o el nombre de la carpeta de Exchange predeterminada.</span><span class="sxs-lookup"><span data-stu-id="86a76-108">The **MarkAllItemsAsRead** operation can set the [IsRead](isread.md) property on all items in folders identified by either the Exchange Web Services (EWS) folder identifier or the default Exchange folder name.</span></span> <span data-ttu-id="86a76-109">La operación **MarkAllItemsAsRead** también puede suprimir el envío de confirmaciones de lectura para los elementos marcados como leídos.</span><span class="sxs-lookup"><span data-stu-id="86a76-109">The **MarkAllItemsAsRead** operation can also suppress the sending of read receipts for items marked as read.</span></span> 
  
### <a name="markallitemsasread-operation-soap-headers"></a><span data-ttu-id="86a76-110">Encabezados SOAP de operación MarkAllItemsAsRead</span><span class="sxs-lookup"><span data-stu-id="86a76-110">MarkAllItemsAsRead operation SOAP headers</span></span>

<span data-ttu-id="86a76-111">La operación **MarkAllItemsAsRead** puede usar los encabezados SOAP que se enumeran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="86a76-111">The **MarkAllItemsAsRead** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="86a76-112">**Nombre de encabezado**</span><span class="sxs-lookup"><span data-stu-id="86a76-112">**Header name**</span></span>|<span data-ttu-id="86a76-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="86a76-113">**Element**</span></span>|<span data-ttu-id="86a76-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="86a76-114">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="86a76-115">**Suplantación**</span><span class="sxs-lookup"><span data-stu-id="86a76-115">**Impersonation**</span></span> <br/> |[<span data-ttu-id="86a76-116">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="86a76-116">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="86a76-117">Identifica al usuario que está suplantando la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="86a76-117">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="86a76-118">Este encabezado se aplica a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="86a76-118">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="86a76-119">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="86a76-119">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="86a76-120">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="86a76-120">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="86a76-121">Identifica la referencia cultural, tal y como se define en RFC 3066, "etiquetas para la identificación de idiomas", que se va a usar para obtener acceso al buzón.</span><span class="sxs-lookup"><span data-stu-id="86a76-121">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="86a76-122">Este encabezado se aplica a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="86a76-122">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="86a76-123">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="86a76-123">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="86a76-124">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="86a76-124">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="86a76-125">Identifica la versión del esquema para la solicitud de operación.</span><span class="sxs-lookup"><span data-stu-id="86a76-125">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="86a76-126">Este encabezado se aplica a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="86a76-126">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="86a76-127">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="86a76-127">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="86a76-128">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="86a76-128">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="86a76-129">Identifica la versión del servidor que respondió a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="86a76-129">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="86a76-130">Este encabezado se aplica a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="86a76-130">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="markallitemsasread-operation-request-example-mark-all-items-in-a-folder-as-read"></a><span data-ttu-id="86a76-131">Ejemplo de solicitud de operación MarkAllItemsAsRead: marcar todos los elementos de una carpeta como leídos</span><span class="sxs-lookup"><span data-stu-id="86a76-131">MarkAllItemsAsRead operation request example: Mark all items in a folder as read</span></span>

<span data-ttu-id="86a76-132">El siguiente ejemplo de una solicitud de operación de **MarkAllItemsAsRead** muestra cómo establecer la propiedad [IsRead](isread.md) , que también se denomina marca de lectura, en **true** en todos los elementos de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="86a76-132">The following example of a **MarkAllItemsAsRead** operation request shows how to set the [IsRead](isread.md) property, which is also called the read flag, to **true** on all items in a folder.</span></span> <span data-ttu-id="86a76-133">En este ejemplo también se muestra que no se envían confirmaciones de lectura en respuesta a las solicitudes de confirmación de lectura.</span><span class="sxs-lookup"><span data-stu-id="86a76-133">This example also shows that read receipts are not sent in response to any read receipt requests.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="86a76-134">Todos los identificadores de elemento y las claves de cambio de este artículo se han reducido para preservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="86a76-134">All item identifiers and change keys in this article have been shortened to preserve readability.</span></span> <span data-ttu-id="86a76-135">Las claves de cambio no son necesarias para esta operación.</span><span class="sxs-lookup"><span data-stu-id="86a76-135">Change keys are not required for this operation.</span></span> 
  
```XML
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
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

<span data-ttu-id="86a76-136">El cuerpo SOAP de la solicitud contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="86a76-136">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="86a76-137">MarkAllItemsAsRead</span><span class="sxs-lookup"><span data-stu-id="86a76-137">MarkAllItemsAsRead</span></span>](markallitemsasread.md)
    
- [<span data-ttu-id="86a76-138">ReadFlag</span><span class="sxs-lookup"><span data-stu-id="86a76-138">ReadFlag</span></span>](readflag.md)
    
- [<span data-ttu-id="86a76-139">SuppressReadReceipts</span><span class="sxs-lookup"><span data-stu-id="86a76-139">SuppressReadReceipts</span></span>](suppressreadreceipts.md)
    
- [<span data-ttu-id="86a76-140">FolderIds</span><span class="sxs-lookup"><span data-stu-id="86a76-140">FolderIds</span></span>](folderids.md)
    
- [<span data-ttu-id="86a76-141">FolderId</span><span class="sxs-lookup"><span data-stu-id="86a76-141">FolderId</span></span>](folderid.md)
    
## <a name="successful-markallitemsasread-operation-response"></a><span data-ttu-id="86a76-142">Respuesta de operación MarkAllItemsAsRead correcta</span><span class="sxs-lookup"><span data-stu-id="86a76-142">Successful MarkAllItemsAsRead operation response</span></span>

<span data-ttu-id="86a76-143">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación **MarkAllItemsAsRead** para marcar todos los elementos de una carpeta como leídos.</span><span class="sxs-lookup"><span data-stu-id="86a76-143">The following example shows a successful response to a **MarkAllItemsAsRead** operation request to mark all items in a folder as read.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="545" 
                           MinorBuildNumber="11" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <m:MarkAllItemsAsReadResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
         <m:ResponseMessages>
            <m:MarkAllItemsAsReadResponseMessage ResponseClass="Success">
               <m:ResponseCode>NoError</m:ResponseCode>
            </m:MarkAllItemsAsReadResponseMessage>
         </m:ResponseMessages>
      </m:MarkAllItemsAsReadResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="86a76-144">El cuerpo SOAP de respuesta contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="86a76-144">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="86a76-145">MarkAllItemsAsReadResponse</span><span class="sxs-lookup"><span data-stu-id="86a76-145">MarkAllItemsAsReadResponse</span></span>](markallitemsasreadresponse.md)
    
- [<span data-ttu-id="86a76-146">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="86a76-146">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="86a76-147">MarkAllItemsAsReadResponseMessage</span><span class="sxs-lookup"><span data-stu-id="86a76-147">MarkAllItemsAsReadResponseMessage</span></span>](markallitemsasreadresponsemessage.md)
    
- [<span data-ttu-id="86a76-148">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="86a76-148">ResponseCode</span></span>](responsecode.md)
    
## <a name="markallitemsasread-operation-request-example-mark-all-items-in-a-folder-as-unread"></a><span data-ttu-id="86a76-149">Ejemplo de solicitud de operación MarkAllItemsAsRead: marcar todos los elementos de una carpeta como no leídos</span><span class="sxs-lookup"><span data-stu-id="86a76-149">MarkAllItemsAsRead operation request example: Mark all items in a folder as unread</span></span>

<span data-ttu-id="86a76-150">El siguiente ejemplo de una solicitud de operación de **MarkAllItemsAsRead** muestra cómo establecer la propiedad [IsRead](isread.md) en **false** en todos los elementos de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="86a76-150">The following example of a **MarkAllItemsAsRead** operation request shows how to set the [IsRead](isread.md) property to **false** on all items in a folder.</span></span> <span data-ttu-id="86a76-151">En este ejemplo también se muestra que no se envían confirmaciones de lectura en respuesta a las solicitudes de confirmación de lectura.</span><span class="sxs-lookup"><span data-stu-id="86a76-151">This example also shows that read receipts are not sent in response to any read receipt requests.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
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

<span data-ttu-id="86a76-152">Una respuesta correcta a una solicitud para marcar todos los elementos como leídos es la misma que la respuesta a una solicitud para marcar todos los elementos como no leídos.</span><span class="sxs-lookup"><span data-stu-id="86a76-152">A successful response to a request to mark all items as read is the same as the response to a request to mark all items as unread.</span></span>
  
<span data-ttu-id="86a76-153">El cuerpo SOAP de la solicitud contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="86a76-153">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="86a76-154">MarkAllItemsAsRead</span><span class="sxs-lookup"><span data-stu-id="86a76-154">MarkAllItemsAsRead</span></span>](markallitemsasread.md)
    
- [<span data-ttu-id="86a76-155">ReadFlag</span><span class="sxs-lookup"><span data-stu-id="86a76-155">ReadFlag</span></span>](readflag.md)
    
- [<span data-ttu-id="86a76-156">SuppressReadReceipts</span><span class="sxs-lookup"><span data-stu-id="86a76-156">SuppressReadReceipts</span></span>](suppressreadreceipts.md)
    
- [<span data-ttu-id="86a76-157">FolderIds</span><span class="sxs-lookup"><span data-stu-id="86a76-157">FolderIds</span></span>](folderids.md)
    
- [<span data-ttu-id="86a76-158">FolderId</span><span class="sxs-lookup"><span data-stu-id="86a76-158">FolderId</span></span>](folderid.md)
    
## <a name="markallitemsasread-operation-error-response"></a><span data-ttu-id="86a76-159">Respuesta de error de operación de MarkAllItemsAsRead</span><span class="sxs-lookup"><span data-stu-id="86a76-159">MarkAllItemsAsRead operation error response</span></span>

<span data-ttu-id="86a76-160">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **MarkAllItemsAsRead** para marcar todos los elementos de una carpeta como leídos o no leídos cuando la carpeta no existe en el buzón.</span><span class="sxs-lookup"><span data-stu-id="86a76-160">The following example shows an error response to a **MarkAllItemsAsRead** operation request to mark all items in a folder as read or unread when the folder does not exist in the mailbox.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="545" 
                           MinorBuildNumber="11" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <m:MarkAllItemsAsReadResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="86a76-161">El cuerpo SOAP de respuesta de error contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="86a76-161">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="86a76-162">MarkAllItemsAsReadResponse</span><span class="sxs-lookup"><span data-stu-id="86a76-162">MarkAllItemsAsReadResponse</span></span>](markallitemsasreadresponse.md)
    
- [<span data-ttu-id="86a76-163">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="86a76-163">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="86a76-164">MarkAllItemsAsReadResponseMessage</span><span class="sxs-lookup"><span data-stu-id="86a76-164">MarkAllItemsAsReadResponseMessage</span></span>](markallitemsasreadresponsemessage.md)
    
- [<span data-ttu-id="86a76-165">MessageText</span><span class="sxs-lookup"><span data-stu-id="86a76-165">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="86a76-166">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="86a76-166">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="86a76-167">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="86a76-167">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="86a76-168">Vea también</span><span class="sxs-lookup"><span data-stu-id="86a76-168">See also</span></span>

- [<span data-ttu-id="86a76-169">Operaciones de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="86a76-169">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="86a76-170">Operación FindFolder</span><span class="sxs-lookup"><span data-stu-id="86a76-170">FindFolder operation</span></span>](findfolder-operation.md)
    

