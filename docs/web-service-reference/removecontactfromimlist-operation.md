---
title: Operación RemoveContactFromImList
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 28ec96c3-45af-48ff-9f17-718a527dc0ad
description: Buscar información sobre la operación de EWS de RemoveContactFromImList.
ms.openlocfilehash: 8b3d83a0b53bad169d9f3478540e5087901f3a12
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458470"
---
# <a name="removecontactfromimlist-operation"></a><span data-ttu-id="32a7d-103">Operación RemoveContactFromImList</span><span class="sxs-lookup"><span data-stu-id="32a7d-103">RemoveContactFromImList operation</span></span>

<span data-ttu-id="32a7d-104">Buscar información sobre la operación de EWS de **RemoveContactFromImList** .</span><span class="sxs-lookup"><span data-stu-id="32a7d-104">Find information about the **RemoveContactFromImList** EWS operation.</span></span> 
  
<span data-ttu-id="32a7d-105">La operación **RemoveContactFromImList** elimina contactos de la lista de mensajería instantánea (mi) de Lync cuando Lync usa Exchange para el almacén de contactos.</span><span class="sxs-lookup"><span data-stu-id="32a7d-105">The **RemoveContactFromImList** operation removes contacts from the Lync instant messaging (IM) list when Lync uses Exchange for the contact store.</span></span> 
  
<span data-ttu-id="32a7d-106">Esta operación se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="32a7d-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-removecontactfromimlist-operation"></a><span data-ttu-id="32a7d-107">Uso de la operación RemoveContactFromImList</span><span class="sxs-lookup"><span data-stu-id="32a7d-107">Using the RemoveContactFromImList operation</span></span>

<span data-ttu-id="32a7d-108">La operación **RemoveContactFromImList** acepta un único argumento que identifica un contacto para quitarlo de la lista de contactos de Lync almacenada en un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="32a7d-108">The **RemoveContactFromImList** operation accepts a single argument that identifies a contact to remove from the Lync contact list stored on an Exchange server.</span></span> <span data-ttu-id="32a7d-109">La lista de contactos a los que se dirige esta operación se denomina **contactos de Lync** en Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="32a7d-109">The list of contacts that this operation targets is called **Lync Contacts** in Outlook 2013.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="32a7d-110">No use la [operación DeleteItem](deleteitem-operation.md) para quitar contactos de una lista de contactos.</span><span class="sxs-lookup"><span data-stu-id="32a7d-110">Do not use the [DeleteItem operation](deleteitem-operation.md) to remove contacts from a contact list.</span></span> <span data-ttu-id="32a7d-111">Puede que sea necesario realizar un procesamiento adicional del servidor para admitir la eliminación de un contacto de la lista de **contactos de Lync** .</span><span class="sxs-lookup"><span data-stu-id="32a7d-111">Additional server-side processing might have to occur to support removing a contact from the **Lync Contacts** list.</span></span> <span data-ttu-id="32a7d-112">Tenga en cuenta que la lista de **contactos de Lync** es el equivalente conceptual de la carpeta de buzones de contactos predeterminada de **Lync** .</span><span class="sxs-lookup"><span data-stu-id="32a7d-112">Note that the **Lync Contacts** list is the conceptual equivalent of the default **Lync Contacts** mailbox folder.</span></span> 
  
### <a name="removecontactfromimlist-operation-soap-headers"></a><span data-ttu-id="32a7d-113">Encabezados SOAP de operación RemoveContactFromImList</span><span class="sxs-lookup"><span data-stu-id="32a7d-113">RemoveContactFromImList operation SOAP headers</span></span>

<span data-ttu-id="32a7d-114">La operación **RemoveContactFromImList** puede usar los encabezados SOAP que se enumeran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="32a7d-114">The **RemoveContactFromImList** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="32a7d-115">**Nombre de encabezado**</span><span class="sxs-lookup"><span data-stu-id="32a7d-115">**Header name**</span></span>|<span data-ttu-id="32a7d-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="32a7d-116">**Element**</span></span>|<span data-ttu-id="32a7d-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="32a7d-117">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="32a7d-118">**Suplantación**</span><span class="sxs-lookup"><span data-stu-id="32a7d-118">**Impersonation**</span></span> <br/> |[<span data-ttu-id="32a7d-119">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="32a7d-119">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="32a7d-120">Identifica al usuario que está suplantando la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="32a7d-120">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="32a7d-121">Este encabezado se aplica a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="32a7d-121">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="32a7d-122">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="32a7d-122">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="32a7d-123">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="32a7d-123">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="32a7d-124">Identifica la referencia cultural, tal y como se define en RFC 3066, "etiquetas para la identificación de idiomas", que se va a usar para obtener acceso al buzón.</span><span class="sxs-lookup"><span data-stu-id="32a7d-124">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="32a7d-125">Este encabezado se aplica a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="32a7d-125">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="32a7d-126">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="32a7d-126">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="32a7d-127">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="32a7d-127">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="32a7d-128">Identifica la versión del esquema para la solicitud de operación.</span><span class="sxs-lookup"><span data-stu-id="32a7d-128">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="32a7d-129">Este encabezado se aplica a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="32a7d-129">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="32a7d-130">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="32a7d-130">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="32a7d-131">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="32a7d-131">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="32a7d-132">Identifica la versión del servidor que respondió a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="32a7d-132">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="32a7d-133">Este encabezado se aplica a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="32a7d-133">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="removecontactfromimlist-operation-request-example-remove-a-contact-from-the-lync-contacts-list"></a><span data-ttu-id="32a7d-134">Ejemplo de solicitud de operación RemoveContactFromImList: quitar un contacto de la lista de contactos de Lync</span><span class="sxs-lookup"><span data-stu-id="32a7d-134">RemoveContactFromImList operation request example: Remove a contact from the Lync Contacts list</span></span>

<span data-ttu-id="32a7d-135">El siguiente ejemplo de una solicitud de operación de **RemoveContactFromImList** muestra cómo quitar un contacto de la lista de **contactos de Lync** .</span><span class="sxs-lookup"><span data-stu-id="32a7d-135">The following example of a **RemoveContactFromImList** operation request shows how to remove a contact from the **Lync Contacts** list.</span></span> <span data-ttu-id="32a7d-136">La operación **RemoveContactFromImList** acepta un único identificador de contacto único para identificar el contacto que se ha quitado de la lista de **contactos de Lync** .</span><span class="sxs-lookup"><span data-stu-id="32a7d-136">The **RemoveContactFromImList** operation accepts a single unique contact identifier to identify the contact that is removed from the **Lync Contacts** list.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="32a7d-137">Todos los identificadores de elemento y las claves de cambio de este artículo se han reducido para preservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="32a7d-137">All item identifiers and change keys in this article have been shortened to preserve readability.</span></span> 
  
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
      <m:RemoveContactFromImList>
         <m:ContactId Id=""/>
      </m:RemoveContactFromImList>
   </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="32a7d-138">Los siguientes elementos se usan en el cuerpo SOAP de la solicitud:</span><span class="sxs-lookup"><span data-stu-id="32a7d-138">The following elements are used in the request SOAP body:</span></span>
  
- [<span data-ttu-id="32a7d-139">RemoveContactFromImList</span><span class="sxs-lookup"><span data-stu-id="32a7d-139">RemoveContactFromImList</span></span>](removecontactfromimlist.md)
    
- [<span data-ttu-id="32a7d-140">Contacto</span><span class="sxs-lookup"><span data-stu-id="32a7d-140">ContactId</span></span>](contactid.md)
    
## <a name="successful-removecontactfromimlist-operation-response"></a><span data-ttu-id="32a7d-141">Respuesta de operación RemoveContactFromImList correcta</span><span class="sxs-lookup"><span data-stu-id="32a7d-141">Successful RemoveContactFromImList operation response</span></span>

<span data-ttu-id="32a7d-142">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación de **RemoveContactFromImList** para quitar un contacto de la lista de **contactos de Lync** .</span><span class="sxs-lookup"><span data-stu-id="32a7d-142">The following example shows a successful response to a **RemoveContactFromImList** operation request to remove a contact from the **Lync Contacts** list.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="8" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <RemoveContactFromImListResponse ResponseClass="Success" 
                                       xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
      </RemoveContactFromImListResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="32a7d-143">Los siguientes elementos se usan en el cuerpo SOAP de la respuesta:</span><span class="sxs-lookup"><span data-stu-id="32a7d-143">The following elements are used in the response SOAP body:</span></span>
  
- [<span data-ttu-id="32a7d-144">RemoveContactFromImListResponse</span><span class="sxs-lookup"><span data-stu-id="32a7d-144">RemoveContactFromImListResponse</span></span>](removecontactfromimlistresponse.md)
    
- [<span data-ttu-id="32a7d-145">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="32a7d-145">ResponseCode</span></span>](responsecode.md)
    
## <a name="removecontactfromimlist-operation-error-response"></a><span data-ttu-id="32a7d-146">Respuesta de error de operación de RemoveContactFromImList</span><span class="sxs-lookup"><span data-stu-id="32a7d-146">RemoveContactFromImList operation error response</span></span>

<span data-ttu-id="32a7d-147">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **RemoveContactFromImList** .</span><span class="sxs-lookup"><span data-stu-id="32a7d-147">The following example shows an error response to a **RemoveContactFromImList** operation request.</span></span> <span data-ttu-id="32a7d-148">Se trata de una respuesta a una solicitud para quitar un contacto de la lista de **contactos de Lync** cuando el contacto ya no existe en la lista.</span><span class="sxs-lookup"><span data-stu-id="32a7d-148">This is a response to a request to remove a contact from the **Lync Contacts** list when the contact no longer exists in the list.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="8" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <RemoveContactFromImListResponse ResponseClass="Error" 
                                       xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>The specified object was not found in the store.</MessageText>
         <ResponseCode>ErrorItemNotFound</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </RemoveContactFromImListResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="32a7d-149">Los siguientes elementos se usan en el cuerpo SOAP de respuesta de error:</span><span class="sxs-lookup"><span data-stu-id="32a7d-149">The following elements are used in the error response SOAP body:</span></span>
  
- [<span data-ttu-id="32a7d-150">RemoveContactFromImListResponse</span><span class="sxs-lookup"><span data-stu-id="32a7d-150">RemoveContactFromImListResponse</span></span>](removecontactfromimlistresponse.md)
    
- [<span data-ttu-id="32a7d-151">MessageText</span><span class="sxs-lookup"><span data-stu-id="32a7d-151">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="32a7d-152">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="32a7d-152">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="32a7d-153">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="32a7d-153">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="32a7d-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="32a7d-154">See also</span></span>

- [<span data-ttu-id="32a7d-155">Operaciones de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="32a7d-155">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="32a7d-156">Operación GetImItemList</span><span class="sxs-lookup"><span data-stu-id="32a7d-156">GetImItemList operation</span></span>](getimitemlist-operation.md)
    

