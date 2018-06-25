---
title: MarkAsJunk Operation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1f71f04d-56a9-4fee-a4e7-d1034438329e
description: Busque información sobre la EWS MarkAsJunk operación.
ms.openlocfilehash: b9d79e6fbec87ce41030b4981f3c16f2f9ce9507
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836353"
---
# <a name="markasjunk-operation"></a><span data-ttu-id="0ea32-103">MarkAsJunk Operation</span><span class="sxs-lookup"><span data-stu-id="0ea32-103">MarkAsJunk operation</span></span>

<span data-ttu-id="0ea32-104">Obtenga información acerca de la operación de EWS **MarkAsJunk** .</span><span class="sxs-lookup"><span data-stu-id="0ea32-104">Find information about the **MarkAsJunk** EWS operation.</span></span> 
  
<span data-ttu-id="0ea32-105">La operación **MarkAsJunk** agrega y quita los usuarios de la lista de correo electrónico bloqueados y mueve mensajes de correo electrónico a la carpeta de correo electrónico no deseado.</span><span class="sxs-lookup"><span data-stu-id="0ea32-105">The **MarkAsJunk** operation adds and removes users from the blocked email list and moves email messages to the Junk Email folder.</span></span> 
  
<span data-ttu-id="0ea32-106">Esta operación se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0ea32-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-markasjunk-operation"></a><span data-ttu-id="0ea32-107">Mediante la operación MarkAsJunk</span><span class="sxs-lookup"><span data-stu-id="0ea32-107">Using the MarkAsJunk operation</span></span>

<span data-ttu-id="0ea32-108">La operación **MarkAsJunk** contiene dos opciones booleanas para indicar si se debe agregar un remitente de correo electrónico a la lista de remitentes bloqueados y si se va a mover el mensaje de correo electrónico de destino para la carpeta de correo electrónico no deseado predeterminada o en la carpeta Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="0ea32-108">The **MarkAsJunk** operation contains two Boolean options to indicate whether an email sender should be added to the blocked sender list and whether the target email message should be moved to the default Junk Email folder or the Inbox folder.</span></span> <span data-ttu-id="0ea32-109">Las acciones están determinadas por los valores de los atributos **IsJunk** y **MoveItem** .</span><span class="sxs-lookup"><span data-stu-id="0ea32-109">The actions are determined by the values of the **IsJunk** and **MoveItem** attributes.</span></span> <span data-ttu-id="0ea32-110">Los siguientes son las posibles acciones en función de las combinaciones de valores para los atributos **IsJunk** y **MoveItem** :</span><span class="sxs-lookup"><span data-stu-id="0ea32-110">The following are the possible actions based on the value combinations for the **IsJunk** and **MoveItem** attributes:</span></span> 
  
- <span data-ttu-id="0ea32-111">Si el atributo **IsJunk** se establece en **true**y el atributo **MoveItem** se establece en **true**, se agrega el remitente del mensaje de correo electrónico de destino a la lista de remitentes bloqueados y el mensaje de correo electrónico se mueve a la carpeta correo no deseado Dmail.</span><span class="sxs-lookup"><span data-stu-id="0ea32-111">If the **IsJunk** attribute is set to **true**, and the **MoveItem** attribute is set to **true**, the sender of the target email message is added to the blocked sender list and the email message is moved to the Junk Dmail folder.</span></span>
    
- <span data-ttu-id="0ea32-112">Si el atributo **IsJunk** se establece en **true**y el atributo **MoveItem** se establece en **false**, se agrega el remitente del mensaje de correo electrónico de destino a la lista de remitentes bloqueados y no se mueve el mensaje de correo electrónico de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="0ea32-112">If the **IsJunk** attribute is set to **true**, and the **MoveItem** attribute is set to **false**, the sender of the target email message is added to the blocked sender list and the email message is not moved from the folder.</span></span>
    
- <span data-ttu-id="0ea32-113">Si el atributo **IsJunk** está establecido en **false**y el **MoveItem** atributo está establecido en **true**, el remitente de la messageis de correo electrónico de destino quitado de la lista de remitentes bloqueados y el mensaje de correo electrónico se mueve a la carpeta Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="0ea32-113">If the **IsJunk** attribute is set to **false**, and the **MoveItem** attribute is set to **true**, the sender of the target email messageis removed from the blocked sender list and the email message is moved to the Inbox folder.</span></span>
    
- <span data-ttu-id="0ea32-114">Si el atributo **IsJunk** está establecido en **false**y el atributo **MoveItem** se establece en **false**, el remitente del mensaje de correo electrónico de destino se quita de la lista de remitentes bloqueados y no se mueve el mensaje de correo electrónico de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="0ea32-114">If the **IsJunk** attribute is set to **false**, and the **MoveItem** attribute is set to **false**, the sender of the target email message is removed from the blocked sender list and the email message is not moved from the folder.</span></span>
    
> [!IMPORTANT]
> <span data-ttu-id="0ea32-115">El contenido de la lista de remitentes bloqueados no es reconocible de EWS.</span><span class="sxs-lookup"><span data-stu-id="0ea32-115">The contents of the blocked sender list are not discoverable from EWS.</span></span> <span data-ttu-id="0ea32-116">Si un remitente se agrega a la lista de remitentes bloqueados, debe conservar una copia de un mensaje de correo electrónico enviado por el remitente bloqueado para desbloquear el remitente en el futuro.</span><span class="sxs-lookup"><span data-stu-id="0ea32-116">If a sender is added to the blocked sender list, you need to keep a copy of an email message sent by the blocked sender to unblock the sender in the future.</span></span> 
  
### <a name="markasjunk-operation-soap-headers"></a><span data-ttu-id="0ea32-117">Encabezados SOAP de operación de MarkAsJunk</span><span class="sxs-lookup"><span data-stu-id="0ea32-117">MarkAsJunk operation SOAP headers</span></span>

<span data-ttu-id="0ea32-118">La operación de **MarkAsJunk** puede utilizar los encabezados SOAP que se enumeran en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="0ea32-118">The **MarkAsJunk** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="0ea32-119">**Nombre de encabezado**</span><span class="sxs-lookup"><span data-stu-id="0ea32-119">**Header name**</span></span>|<span data-ttu-id="0ea32-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="0ea32-120">**Element**</span></span>|<span data-ttu-id="0ea32-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0ea32-121">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0ea32-122">**Suplantación**</span><span class="sxs-lookup"><span data-stu-id="0ea32-122">**Impersonation**</span></span> <br/> |[<span data-ttu-id="0ea32-123">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="0ea32-123">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="0ea32-124">Identifica el usuario que está realizando la suplantación de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="0ea32-124">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="0ea32-125">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="0ea32-125">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="0ea32-126">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="0ea32-126">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="0ea32-127">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="0ea32-127">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="0ea32-128">Identifica la referencia cultural, como se define en RFC 3066, "Etiquetas para la identificación de idiomas," que se utilizará para acceder al buzón.</span><span class="sxs-lookup"><span data-stu-id="0ea32-128">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="0ea32-129">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="0ea32-129">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="0ea32-130">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="0ea32-130">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="0ea32-131">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="0ea32-131">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="0ea32-132">Identifica la versión del esquema para la solicitud de la operación.</span><span class="sxs-lookup"><span data-stu-id="0ea32-132">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="0ea32-133">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="0ea32-133">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="0ea32-134">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="0ea32-134">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="0ea32-135">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="0ea32-135">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="0ea32-136">Identifica la versión del servidor que ha respondido a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0ea32-136">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="0ea32-137">Este encabezado es aplicable a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="0ea32-137">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="markasjunk-operation-request-example-add-a-sender-to-the-blocked-sender-list"></a><span data-ttu-id="0ea32-138">Ejemplo de solicitud de operación de MarkAsJunk: agregar un remitente a la lista de remitentes bloqueados</span><span class="sxs-lookup"><span data-stu-id="0ea32-138">MarkAsJunk operation request example: Add a sender to the blocked sender list</span></span>

<span data-ttu-id="0ea32-139">El siguiente ejemplo de una solicitud de operación **MarkAsJunk** muestra cómo agregar el remitente de un correo electrónico a la lista de remitentes bloqueados y mover el correo electrónico a la carpeta correo electrónico no deseado.</span><span class="sxs-lookup"><span data-stu-id="0ea32-139">The following example of a **MarkAsJunk** operation request shows how to add the sender of an email to the blocked sender list and move the email to the junk mail folder.</span></span> <span data-ttu-id="0ea32-140">La operación **MarkAsJunk** acepta el identificador de mensaje de correo electrónico único para identificar el correo electrónico que se usa para hacer referencia al remitente que se agrega a la lista de remitentes bloqueados.</span><span class="sxs-lookup"><span data-stu-id="0ea32-140">The **MarkAsJunk** operation accepts the unique email message identifier to identify the email that is used to reference the sender that is added to the blocked sender list.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="0ea32-141">Todos los identificadores de artículo y cambiar claves en este artículo se han abreviado para conservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="0ea32-141">All item identifiers and change keys in this article have been shortened to preserve readability.</span></span> 
  
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
        <m:MarkAsJunk IsJunk="true" MoveItem="true">
            <m:ItemIds>
                <t:ItemId Id="AAMkAD=" ChangeKey="CQAAABYA" />
            </m:ItemIds>
        </m:MarkAsJunk>
    </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="0ea32-142">La solicitud SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="0ea32-142">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="0ea32-143">MarkAsJunk</span><span class="sxs-lookup"><span data-stu-id="0ea32-143">MarkAsJunk</span></span>](markasjunk.md)
    
- [<span data-ttu-id="0ea32-144">ItemId</span><span class="sxs-lookup"><span data-stu-id="0ea32-144">ItemIds</span></span>](itemids.md)
    
- [<span data-ttu-id="0ea32-145">ItemId</span><span class="sxs-lookup"><span data-stu-id="0ea32-145">ItemId</span></span>](itemid.md)
    
## <a name="successful-markasjunk-operation-response"></a><span data-ttu-id="0ea32-146">Respuesta es correcta de operación MarkAsJunk</span><span class="sxs-lookup"><span data-stu-id="0ea32-146">Successful MarkAsJunk operation response</span></span>

<span data-ttu-id="0ea32-147">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación **MarkAsJunk** para agregar un remitente a la lista de remitentes bloqueados y mover el mensaje de correo electrónico a la carpeta correo electrónico no deseado.</span><span class="sxs-lookup"><span data-stu-id="0ea32-147">The following example shows a successful response to a **MarkAsJunk** operation request to add a sender to the blocked sender list and move the email message to the Junk Email folder.</span></span> 
  
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
        <m:MarkAsJunkResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                              xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
           <m:ResponseMessages>
               <m:MarkAsJunkResponseMessage ResponseClass="Success">
                  <m:ResponseCode>NoError</m:ResponseCode>
                 <m:MovedItemId Id="AAMkAD=" ChangeKey="CQAAABYu" />
               </m:MarkAsJunkResponseMessage>
           </m:ResponseMessages>
        </m:MarkAsJunkResponse>
    </s:Body>
</s:Envelope>
```

<span data-ttu-id="0ea32-148">La respuesta SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="0ea32-148">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="0ea32-149">MarkAsJunkResponse</span><span class="sxs-lookup"><span data-stu-id="0ea32-149">MarkAsJunkResponse</span></span>](markasjunkresponse.md)
    
- [<span data-ttu-id="0ea32-150">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="0ea32-150">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="0ea32-151">MarkAsJunkResponseMessage</span><span class="sxs-lookup"><span data-stu-id="0ea32-151">MarkAsJunkResponseMessage</span></span>](markasjunkresponsemessage.md)
    
- [<span data-ttu-id="0ea32-152">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="0ea32-152">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="0ea32-153">MovedItemId</span><span class="sxs-lookup"><span data-stu-id="0ea32-153">MovedItemId</span></span>](moveditemid.md)
    
## <a name="markasjunk-operation-request-example-remove-a-sender-from-the-blocked-sender-list"></a><span data-ttu-id="0ea32-154">Ejemplo de solicitud de operación de MarkAsJunk: quitar un remitente de la lista de remitentes bloqueados</span><span class="sxs-lookup"><span data-stu-id="0ea32-154">MarkAsJunk operation request example: Remove a sender from the blocked sender list</span></span>

<span data-ttu-id="0ea32-155">El siguiente ejemplo de una solicitud de operación **MarkAsJunk** muestra cómo quitar el remitente de un mensaje de correo electrónico de la lista de remitentes bloqueados y mover el mensaje de correo electrónico a la carpeta Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="0ea32-155">The following example of a **MarkAsJunk** operation request shows how to remove the sender of an email message from the blocked sender list and move the email message to the Inbox folder.</span></span> <span data-ttu-id="0ea32-156">Debe tener un mensaje de correo electrónico enviado por el remitente bloqueado para quitar el remitente de la lista de remitentes bloqueados.</span><span class="sxs-lookup"><span data-stu-id="0ea32-156">You need to keep an email message sent by the blocked sender to remove the sender from the blocked sender list.</span></span> <span data-ttu-id="0ea32-157">Dirección de correo electrónico del remitente está asociada con los mensajes de correo electrónico que se han enviado por el remitente.</span><span class="sxs-lookup"><span data-stu-id="0ea32-157">The sender's email address is associated with email messages that have been sent by the sender.</span></span> <span data-ttu-id="0ea32-158">Eliminación de un remitente de la lista de remitentes bloqueados no se realizará correctamente si el mensaje de correo electrónico de referencia ya no existe en el buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="0ea32-158">Removing a sender from the blocked sender list will not succeed if the reference email message no longer exists in the user's mailbox.</span></span> <span data-ttu-id="0ea32-159">El identificador de elemento que se utiliza para asociar un mensaje de correo electrónico a su remitente debe asociarse con un elemento que existe en el buzón de Exchange.</span><span class="sxs-lookup"><span data-stu-id="0ea32-159">The item identifier used to associate an email message with its sender must be associated with an item that exists in the Exchange mailbox.</span></span> <span data-ttu-id="0ea32-160">Recomendamos que cree una carpeta oculta para almacenar elementos enviados por remitentes bloqueados anteriormente para que los remitentes se puedan desbloqueados desde la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="0ea32-160">We recommend that you create a hidden folder to store items sent by previously blocked senders so that the senders can be unblocked from the client application.</span></span> <span data-ttu-id="0ea32-161">En caso de que un elemento se ha quitado de los buzones de Exchange, un administrador tiene que usar la consola de administración de Exchange para tener acceso a la lista de remitentes bloqueados para quitar un remitente de la lista.</span><span class="sxs-lookup"><span data-stu-id="0ea32-161">In the event that an item has been removed from the Exchange mailbox, an administrator has to use the Exchange Management Console to access the blocked sender list to remove a sender from the list.</span></span> <span data-ttu-id="0ea32-162">Para obtener información acerca de cómo desbloquear un usuario mediante el uso de la consola de administración de Exchange, consulte [cómo configurar los remitentes seguros y remitentes bloqueados en Office 365](http://support.microsoft.com/kb/2545137).</span><span class="sxs-lookup"><span data-stu-id="0ea32-162">For information about how to unblock a user by using the Exchange Management Console, see [How to configure the safe senders and blocked senders settings in Office 365](http://support.microsoft.com/kb/2545137).</span></span>
  
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
      <m:MarkAsJunk IsJunk="false" MoveItem="true">
        <m:ItemIds>
          <t:ItemId Id="AAMkAD=" ChangeKey="CQAAABYu" />
        </m:ItemIds>
      </m:MarkAsJunk>
    </soap:Body>
 </soap:Envelope>

```

<span data-ttu-id="0ea32-163">Una respuesta correcta para quitar un remitente de la lista de remitentes bloqueados es el mismo que la respuesta para agregar un remitente a la lista de remitentes bloqueados.</span><span class="sxs-lookup"><span data-stu-id="0ea32-163">A successful response for removing a sender from the blocked sender list is the same as the response for adding a sender to the blocked sender list.</span></span>
  
<span data-ttu-id="0ea32-164">La solicitud SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="0ea32-164">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="0ea32-165">MarkAsJunk</span><span class="sxs-lookup"><span data-stu-id="0ea32-165">MarkAsJunk</span></span>](markasjunk.md)
    
- [<span data-ttu-id="0ea32-166">ItemId</span><span class="sxs-lookup"><span data-stu-id="0ea32-166">ItemIds</span></span>](itemids.md)
    
- [<span data-ttu-id="0ea32-167">ItemId</span><span class="sxs-lookup"><span data-stu-id="0ea32-167">ItemId</span></span>](itemid.md)
    
## <a name="markasjunk-operation-error-response"></a><span data-ttu-id="0ea32-168">Respuesta de error de la operación de MarkAsJunk</span><span class="sxs-lookup"><span data-stu-id="0ea32-168">MarkAsJunk operation error response</span></span>

<span data-ttu-id="0ea32-169">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **MarkAsJunk** .</span><span class="sxs-lookup"><span data-stu-id="0ea32-169">The following example shows an error response to a **MarkAsJunk** operation request.</span></span> <span data-ttu-id="0ea32-170">Esta es una respuesta a una solicitud para agregar o quitar un remitente de la lista de remitentes bloqueados cuando el mensaje de correo electrónico especificado por el identificador del elemento ya no existe en el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="0ea32-170">This is a response to a request to add or remove a sender from the blocked sender list when the email message specified by the item identifier no longer exists in the mailbox.</span></span> 
  
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
    <m:MarkAsJunkResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:MarkAsJunkResponseMessage ResponseClass="Error">
          <m:MessageText>The specified object was not found in the store.</m:MessageText>
          <m:ResponseCode>ErrorItemNotFound</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:MarkAsJunkResponseMessage>
      </m:ResponseMessages>
    </m:MarkAsJunkResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="0ea32-171">La respuesta de error SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="0ea32-171">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="0ea32-172">MarkAsJunkResponse</span><span class="sxs-lookup"><span data-stu-id="0ea32-172">MarkAsJunkResponse</span></span>](markasjunkresponse.md)
    
- [<span data-ttu-id="0ea32-173">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="0ea32-173">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="0ea32-174">MarkAsJunkResponseMessage</span><span class="sxs-lookup"><span data-stu-id="0ea32-174">MarkAsJunkResponseMessage</span></span>](markasjunkresponsemessage.md)
    
- [<span data-ttu-id="0ea32-175">MessageText</span><span class="sxs-lookup"><span data-stu-id="0ea32-175">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="0ea32-176">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="0ea32-176">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="0ea32-177">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="0ea32-177">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="0ea32-178">Vea también</span><span class="sxs-lookup"><span data-stu-id="0ea32-178">See also</span></span>

- [<span data-ttu-id="0ea32-179">Operaciones de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="0ea32-179">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- <span data-ttu-id="0ea32-180">[GetItem operation](getitem-operation.md) Operación GetItem</span><span class="sxs-lookup"><span data-stu-id="0ea32-180">[GetItem operation](getitem-operation.md) GetItem operation</span></span> 
    
- [<span data-ttu-id="0ea32-181">Operación FindItem</span><span class="sxs-lookup"><span data-stu-id="0ea32-181">FindItem operation</span></span>](finditem-operation.md)
    

