---
title: Operación RemoveContactFromImList
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 28ec96c3-45af-48ff-9f17-718a527dc0ad
description: Busque información sobre la EWS RemoveContactFromImList operación.
ms.openlocfilehash: 036b295a84e86ad74c467572cc52fdf6bbae5191
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837080"
---
# <a name="removecontactfromimlist-operation"></a><span data-ttu-id="21362-103">Operación RemoveContactFromImList</span><span class="sxs-lookup"><span data-stu-id="21362-103">RemoveContactFromImList operation</span></span>

<span data-ttu-id="21362-104">Obtenga información acerca de la operación de EWS **RemoveContactFromImList** .</span><span class="sxs-lookup"><span data-stu-id="21362-104">Find information about the **RemoveContactFromImList** EWS operation.</span></span> 
  
<span data-ttu-id="21362-105">La operación **RemoveContactFromImList** quita los contactos de la lista de mensajería instantánea (mi) de Lync cuando Lync usa Exchange para el almacén de contactos.</span><span class="sxs-lookup"><span data-stu-id="21362-105">The **RemoveContactFromImList** operation removes contacts from the Lync instant messaging (IM) list when Lync uses Exchange for the contact store.</span></span> 
  
<span data-ttu-id="21362-106">Esta operación se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="21362-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-removecontactfromimlist-operation"></a><span data-ttu-id="21362-107">Mediante la operación RemoveContactFromImList</span><span class="sxs-lookup"><span data-stu-id="21362-107">Using the RemoveContactFromImList operation</span></span>

<span data-ttu-id="21362-108">La operación de **RemoveContactFromImList** acepta un argumento único que identifica un contacto para quitar de la lista de contactos de Lync almacenada en un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="21362-108">The **RemoveContactFromImList** operation accepts a single argument that identifies a contact to remove from the Lync contact list stored on an Exchange server.</span></span> <span data-ttu-id="21362-109">La lista de contactos que los objetivos de esta operación se denomina **Contactos de Lync** en Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="21362-109">The list of contacts that this operation targets is called **Lync Contacts** in Outlook 2013.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="21362-110">No use la [operación DeleteItem](deleteitem-operation.md) para quitar los contactos de una lista de contactos.</span><span class="sxs-lookup"><span data-stu-id="21362-110">Do not use the [DeleteItem operation](deleteitem-operation.md) to remove contacts from a contact list.</span></span> <span data-ttu-id="21362-111">Procesamiento de servidor adicional que tenga que se producen para admitir la eliminación de un contacto de la lista de **Contactos de Lync** .</span><span class="sxs-lookup"><span data-stu-id="21362-111">Additional server-side processing might have to occur to support removing a contact from the **Lync Contacts** list.</span></span> <span data-ttu-id="21362-112">Tenga en cuenta que la lista de **Contactos de Lync** es el equivalente conceptual de la carpeta de buzón de correo de **Los contactos de Lync** predeterminada.</span><span class="sxs-lookup"><span data-stu-id="21362-112">Note that the **Lync Contacts** list is the conceptual equivalent of the default **Lync Contacts** mailbox folder.</span></span> 
  
### <a name="removecontactfromimlist-operation-soap-headers"></a><span data-ttu-id="21362-113">Encabezados SOAP de operación de RemoveContactFromImList</span><span class="sxs-lookup"><span data-stu-id="21362-113">RemoveContactFromImList operation SOAP headers</span></span>

<span data-ttu-id="21362-114">La operación de **RemoveContactFromImList** puede utilizar los encabezados SOAP que se enumeran en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="21362-114">The **RemoveContactFromImList** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="21362-115">**Nombre de encabezado**</span><span class="sxs-lookup"><span data-stu-id="21362-115">**Header name**</span></span>|<span data-ttu-id="21362-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="21362-116">**Element**</span></span>|<span data-ttu-id="21362-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="21362-117">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="21362-118">**Suplantación**</span><span class="sxs-lookup"><span data-stu-id="21362-118">**Impersonation**</span></span> <br/> |[<span data-ttu-id="21362-119">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="21362-119">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="21362-120">Identifica el usuario que está realizando la suplantación de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="21362-120">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="21362-121">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="21362-121">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="21362-122">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="21362-122">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="21362-123">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="21362-123">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="21362-124">Identifica la referencia cultural, como se define en RFC 3066, "Etiquetas para la identificación de idiomas," que se utilizará para acceder al buzón.</span><span class="sxs-lookup"><span data-stu-id="21362-124">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="21362-125">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="21362-125">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="21362-126">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="21362-126">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="21362-127">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="21362-127">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="21362-128">Identifica la versión del esquema para la solicitud de la operación.</span><span class="sxs-lookup"><span data-stu-id="21362-128">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="21362-129">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="21362-129">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="21362-130">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="21362-130">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="21362-131">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="21362-131">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="21362-132">Identifica la versión del servidor que ha respondido a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="21362-132">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="21362-133">Este encabezado es aplicable a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="21362-133">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="removecontactfromimlist-operation-request-example-remove-a-contact-from-the-lync-contacts-list"></a><span data-ttu-id="21362-134">Ejemplo de solicitud de operación de RemoveContactFromImList: quitar un contacto de la lista de contactos de Lync</span><span class="sxs-lookup"><span data-stu-id="21362-134">RemoveContactFromImList operation request example: Remove a contact from the Lync Contacts list</span></span>

<span data-ttu-id="21362-135">El siguiente ejemplo de una solicitud de operación **RemoveContactFromImList** muestra cómo quitar un contacto de la lista de **Contactos de Lync** .</span><span class="sxs-lookup"><span data-stu-id="21362-135">The following example of a **RemoveContactFromImList** operation request shows how to remove a contact from the **Lync Contacts** list.</span></span> <span data-ttu-id="21362-136">La operación de **RemoveContactFromImList** acepta un único identificador de contacto único para identificar el contacto al que se ha quitado de la lista de **Contactos de Lync** .</span><span class="sxs-lookup"><span data-stu-id="21362-136">The **RemoveContactFromImList** operation accepts a single unique contact identifier to identify the contact that is removed from the **Lync Contacts** list.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="21362-137">Todos los identificadores de artículo y cambiar claves en este artículo se han abreviado para conservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="21362-137">All item identifiers and change keys in this article have been shortened to preserve readability.</span></span> 
  
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
      <m:RemoveContactFromImList>
         <m:ContactId Id=""/>
      </m:RemoveContactFromImList>
   </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="21362-138">En la solicitud SOAP body, se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="21362-138">The following elements are used in the request SOAP body:</span></span>
  
- [<span data-ttu-id="21362-139">RemoveContactFromImList</span><span class="sxs-lookup"><span data-stu-id="21362-139">RemoveContactFromImList</span></span>](removecontactfromimlist.md)
    
- [<span data-ttu-id="21362-140">ID de contacto</span><span class="sxs-lookup"><span data-stu-id="21362-140">ContactId</span></span>](contactid.md)
    
## <a name="successful-removecontactfromimlist-operation-response"></a><span data-ttu-id="21362-141">Respuesta es correcta de operación RemoveContactFromImList</span><span class="sxs-lookup"><span data-stu-id="21362-141">Successful RemoveContactFromImList operation response</span></span>

<span data-ttu-id="21362-142">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación de **RemoveContactFromImList** para quitar un contacto de la lista de **Contactos de Lync** .</span><span class="sxs-lookup"><span data-stu-id="21362-142">The following example shows a successful response to a **RemoveContactFromImList** operation request to remove a contact from the **Lync Contacts** list.</span></span> 
  
```XML
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
      <RemoveContactFromImListResponse ResponseClass="Success" 
                                       xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
      </RemoveContactFromImListResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="21362-143">En la respuesta SOAP body, se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="21362-143">The following elements are used in the response SOAP body:</span></span>
  
- [<span data-ttu-id="21362-144">RemoveContactFromImListResponse</span><span class="sxs-lookup"><span data-stu-id="21362-144">RemoveContactFromImListResponse</span></span>](removecontactfromimlistresponse.md)
    
- [<span data-ttu-id="21362-145">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="21362-145">ResponseCode</span></span>](responsecode.md)
    
## <a name="removecontactfromimlist-operation-error-response"></a><span data-ttu-id="21362-146">Respuesta de error de la operación de RemoveContactFromImList</span><span class="sxs-lookup"><span data-stu-id="21362-146">RemoveContactFromImList operation error response</span></span>

<span data-ttu-id="21362-147">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **RemoveContactFromImList** .</span><span class="sxs-lookup"><span data-stu-id="21362-147">The following example shows an error response to a **RemoveContactFromImList** operation request.</span></span> <span data-ttu-id="21362-148">Esta es una respuesta a una solicitud para quitar un contacto de la lista de **Contactos de Lync** cuando el contacto ya no existe en la lista.</span><span class="sxs-lookup"><span data-stu-id="21362-148">This is a response to a request to remove a contact from the **Lync Contacts** list when the contact no longer exists in the list.</span></span> 
  
```XML
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
      <RemoveContactFromImListResponse ResponseClass="Error" 
                                       xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>The specified object was not found in the store.</MessageText>
         <ResponseCode>ErrorItemNotFound</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </RemoveContactFromImListResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="21362-149">En el cuerpo del mensaje SOAP de respuesta de error se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="21362-149">The following elements are used in the error response SOAP body:</span></span>
  
- [<span data-ttu-id="21362-150">RemoveContactFromImListResponse</span><span class="sxs-lookup"><span data-stu-id="21362-150">RemoveContactFromImListResponse</span></span>](removecontactfromimlistresponse.md)
    
- [<span data-ttu-id="21362-151">MessageText</span><span class="sxs-lookup"><span data-stu-id="21362-151">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="21362-152">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="21362-152">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="21362-153">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="21362-153">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="21362-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="21362-154">See also</span></span>

- [<span data-ttu-id="21362-155">Operaciones de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="21362-155">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="21362-156">Operación GetImItemList</span><span class="sxs-lookup"><span data-stu-id="21362-156">GetImItemList operation</span></span>](getimitemlist-operation.md)
    

