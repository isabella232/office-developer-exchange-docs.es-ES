---
title: Operación MarkAsJunk
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1f71f04d-56a9-4fee-a4e7-d1034438329e
description: Buscar información sobre la operación de EWS de MarkAsJunk.
ms.openlocfilehash: 25d6b01dfff64c4e45f3382223311219d349c165
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468575"
---
# <a name="markasjunk-operation"></a><span data-ttu-id="4c932-103">Operación MarkAsJunk</span><span class="sxs-lookup"><span data-stu-id="4c932-103">MarkAsJunk operation</span></span>

<span data-ttu-id="4c932-104">Buscar información sobre la operación de EWS de **MarkAsJunk** .</span><span class="sxs-lookup"><span data-stu-id="4c932-104">Find information about the **MarkAsJunk** EWS operation.</span></span> 
  
<span data-ttu-id="4c932-105">La operación **MarkAsJunk** agrega y quita usuarios de la lista de correos electrónicos bloqueados y mueve los mensajes de correo electrónico a la carpeta de correo no deseado.</span><span class="sxs-lookup"><span data-stu-id="4c932-105">The **MarkAsJunk** operation adds and removes users from the blocked email list and moves email messages to the Junk Email folder.</span></span> 
  
<span data-ttu-id="4c932-106">Esta operación se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="4c932-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-markasjunk-operation"></a><span data-ttu-id="4c932-107">Uso de la operación MarkAsJunk</span><span class="sxs-lookup"><span data-stu-id="4c932-107">Using the MarkAsJunk operation</span></span>

<span data-ttu-id="4c932-108">La operación **MarkAsJunk** contiene dos opciones booleanas para indicar si se debe agregar un remitente de correo electrónico a la lista de remitentes bloqueados y si el mensaje de correo electrónico de destino debe moverse a la carpeta de correo electrónico no deseado o a la carpeta Bandeja de entrada predeterminada.</span><span class="sxs-lookup"><span data-stu-id="4c932-108">The **MarkAsJunk** operation contains two Boolean options to indicate whether an email sender should be added to the blocked sender list and whether the target email message should be moved to the default Junk Email folder or the Inbox folder.</span></span> <span data-ttu-id="4c932-109">Las acciones vienen determinadas por los valores de los atributos **IsJunk** y **MoveItem** .</span><span class="sxs-lookup"><span data-stu-id="4c932-109">The actions are determined by the values of the **IsJunk** and **MoveItem** attributes.</span></span> <span data-ttu-id="4c932-110">A continuación se indican las acciones posibles en función de las combinaciones de valores para los atributos **IsJunk** y **MoveItem** :</span><span class="sxs-lookup"><span data-stu-id="4c932-110">The following are the possible actions based on the value combinations for the **IsJunk** and **MoveItem** attributes:</span></span> 
  
- <span data-ttu-id="4c932-111">Si el atributo **IsJunk** se establece en **true**y el atributo **MoveItem** se establece en **true**, el remitente del mensaje de correo electrónico de destino se agrega a la lista de remitentes bloqueados y el mensaje de correo electrónico se mueve a la carpeta de Dmail de correo no deseado.</span><span class="sxs-lookup"><span data-stu-id="4c932-111">If the **IsJunk** attribute is set to **true**, and the **MoveItem** attribute is set to **true**, the sender of the target email message is added to the blocked sender list and the email message is moved to the Junk Dmail folder.</span></span>
    
- <span data-ttu-id="4c932-112">Si el atributo **IsJunk** se establece en **true**y el atributo **MoveItem** se establece en **false**, el remitente del mensaje de correo electrónico de destino se agrega a la lista de remitentes bloqueados y el mensaje de correo electrónico no se mueve de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="4c932-112">If the **IsJunk** attribute is set to **true**, and the **MoveItem** attribute is set to **false**, the sender of the target email message is added to the blocked sender list and the email message is not moved from the folder.</span></span>
    
- <span data-ttu-id="4c932-113">Si el atributo **IsJunk** está establecido en **false**y el atributo **MoveItem** se establece en **true**, el remitente del mensaje de correo electrónico de destino se quita de la lista de remitentes bloqueados y el mensaje de correo electrónico se mueve a la carpeta Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="4c932-113">If the **IsJunk** attribute is set to **false**, and the **MoveItem** attribute is set to **true**, the sender of the target email messageis removed from the blocked sender list and the email message is moved to the Inbox folder.</span></span>
    
- <span data-ttu-id="4c932-114">Si el atributo **IsJunk** está establecido en **false**y el atributo **MoveItem** se establece en **false**, el remitente del mensaje de correo electrónico de destino se quita de la lista de remitentes bloqueados y el mensaje de correo electrónico no se mueve de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="4c932-114">If the **IsJunk** attribute is set to **false**, and the **MoveItem** attribute is set to **false**, the sender of the target email message is removed from the blocked sender list and the email message is not moved from the folder.</span></span>
    
> [!IMPORTANT]
> <span data-ttu-id="4c932-115">El contenido de la lista de remitentes bloqueados no se detecta desde EWS.</span><span class="sxs-lookup"><span data-stu-id="4c932-115">The contents of the blocked sender list are not discoverable from EWS.</span></span> <span data-ttu-id="4c932-116">Si se agrega un remitente a la lista de remitentes bloqueados, debe conservar una copia de un mensaje de correo electrónico enviado por el remitente bloqueado para desbloquear el remitente en el futuro.</span><span class="sxs-lookup"><span data-stu-id="4c932-116">If a sender is added to the blocked sender list, you need to keep a copy of an email message sent by the blocked sender to unblock the sender in the future.</span></span> 
  
### <a name="markasjunk-operation-soap-headers"></a><span data-ttu-id="4c932-117">Encabezados SOAP de operación MarkAsJunk</span><span class="sxs-lookup"><span data-stu-id="4c932-117">MarkAsJunk operation SOAP headers</span></span>

<span data-ttu-id="4c932-118">La operación **MarkAsJunk** puede usar los encabezados SOAP que se enumeran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="4c932-118">The **MarkAsJunk** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="4c932-119">**Nombre de encabezado**</span><span class="sxs-lookup"><span data-stu-id="4c932-119">**Header name**</span></span>|<span data-ttu-id="4c932-120">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="4c932-120">**Element**</span></span>|<span data-ttu-id="4c932-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4c932-121">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4c932-122">**Suplantación**</span><span class="sxs-lookup"><span data-stu-id="4c932-122">**Impersonation**</span></span> <br/> |[<span data-ttu-id="4c932-123">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="4c932-123">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="4c932-124">Identifica al usuario que está suplantando la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="4c932-124">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="4c932-125">Este encabezado se aplica a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="4c932-125">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="4c932-126">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="4c932-126">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="4c932-127">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="4c932-127">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="4c932-128">Identifica la referencia cultural, tal y como se define en RFC 3066, "etiquetas para la identificación de idiomas", que se va a usar para obtener acceso al buzón.</span><span class="sxs-lookup"><span data-stu-id="4c932-128">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="4c932-129">Este encabezado se aplica a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="4c932-129">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="4c932-130">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="4c932-130">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="4c932-131">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="4c932-131">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="4c932-132">Identifica la versión del esquema para la solicitud de operación.</span><span class="sxs-lookup"><span data-stu-id="4c932-132">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="4c932-133">Este encabezado se aplica a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="4c932-133">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="4c932-134">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="4c932-134">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="4c932-135">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="4c932-135">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="4c932-136">Identifica la versión del servidor que respondió a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4c932-136">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="4c932-137">Este encabezado se aplica a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="4c932-137">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="markasjunk-operation-request-example-add-a-sender-to-the-blocked-sender-list"></a><span data-ttu-id="4c932-138">Ejemplo de solicitud de operación MarkAsJunk: agregar un remitente a la lista de remitentes bloqueados</span><span class="sxs-lookup"><span data-stu-id="4c932-138">MarkAsJunk operation request example: Add a sender to the blocked sender list</span></span>

<span data-ttu-id="4c932-139">El siguiente ejemplo de una solicitud de operación de **MarkAsJunk** muestra cómo agregar el remitente de un correo electrónico a la lista de remitentes bloqueados y mover el correo electrónico a la carpeta de correo no deseado.</span><span class="sxs-lookup"><span data-stu-id="4c932-139">The following example of a **MarkAsJunk** operation request shows how to add the sender of an email to the blocked sender list and move the email to the junk mail folder.</span></span> <span data-ttu-id="4c932-140">La operación **MarkAsJunk** acepta el identificador de mensaje de correo electrónico único para identificar el correo electrónico que se usa para hacer referencia al remitente que se agrega a la lista de remitentes bloqueados.</span><span class="sxs-lookup"><span data-stu-id="4c932-140">The **MarkAsJunk** operation accepts the unique email message identifier to identify the email that is used to reference the sender that is added to the blocked sender list.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4c932-141">Todos los identificadores de elemento y las claves de cambio de este artículo se han reducido para preservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="4c932-141">All item identifiers and change keys in this article have been shortened to preserve readability.</span></span> 
  
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
        <m:MarkAsJunk IsJunk="true" MoveItem="true">
            <m:ItemIds>
                <t:ItemId Id="AAMkAD=" ChangeKey="CQAAABYA" />
            </m:ItemIds>
        </m:MarkAsJunk>
    </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="4c932-142">El cuerpo SOAP de la solicitud contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="4c932-142">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="4c932-143">MarkAsJunk</span><span class="sxs-lookup"><span data-stu-id="4c932-143">MarkAsJunk</span></span>](markasjunk.md)
    
- [<span data-ttu-id="4c932-144">ItemIds</span><span class="sxs-lookup"><span data-stu-id="4c932-144">ItemIds</span></span>](itemids.md)
    
- [<span data-ttu-id="4c932-145">ItemId</span><span class="sxs-lookup"><span data-stu-id="4c932-145">ItemId</span></span>](itemid.md)
    
## <a name="successful-markasjunk-operation-response"></a><span data-ttu-id="4c932-146">Respuesta de operación MarkAsJunk correcta</span><span class="sxs-lookup"><span data-stu-id="4c932-146">Successful MarkAsJunk operation response</span></span>

<span data-ttu-id="4c932-147">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación de **MarkAsJunk** para agregar un remitente a la lista de remitentes bloqueados y mover el mensaje de correo electrónico a la carpeta de correo electrónico no deseado.</span><span class="sxs-lookup"><span data-stu-id="4c932-147">The following example shows a successful response to a **MarkAsJunk** operation request to add a sender to the blocked sender list and move the email message to the Junk Email folder.</span></span> 
  
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
        <m:MarkAsJunkResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                              xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="4c932-148">El cuerpo SOAP de respuesta contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="4c932-148">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="4c932-149">MarkAsJunkResponse</span><span class="sxs-lookup"><span data-stu-id="4c932-149">MarkAsJunkResponse</span></span>](markasjunkresponse.md)
    
- [<span data-ttu-id="4c932-150">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="4c932-150">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="4c932-151">MarkAsJunkResponseMessage</span><span class="sxs-lookup"><span data-stu-id="4c932-151">MarkAsJunkResponseMessage</span></span>](markasjunkresponsemessage.md)
    
- [<span data-ttu-id="4c932-152">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="4c932-152">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="4c932-153">MovedItemId</span><span class="sxs-lookup"><span data-stu-id="4c932-153">MovedItemId</span></span>](moveditemid.md)
    
## <a name="markasjunk-operation-request-example-remove-a-sender-from-the-blocked-sender-list"></a><span data-ttu-id="4c932-154">Ejemplo de solicitud de operación MarkAsJunk: quitar un remitente de la lista de remitentes bloqueados</span><span class="sxs-lookup"><span data-stu-id="4c932-154">MarkAsJunk operation request example: Remove a sender from the blocked sender list</span></span>

<span data-ttu-id="4c932-155">El siguiente ejemplo de una solicitud de operación de **MarkAsJunk** muestra cómo quitar el remitente de un mensaje de correo electrónico de la lista de remitentes bloqueados y mover el mensaje de correo electrónico a la carpeta Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="4c932-155">The following example of a **MarkAsJunk** operation request shows how to remove the sender of an email message from the blocked sender list and move the email message to the Inbox folder.</span></span> <span data-ttu-id="4c932-156">Debe conservar un mensaje de correo electrónico enviado por el remitente bloqueado para quitar el remitente de la lista de remitentes bloqueados.</span><span class="sxs-lookup"><span data-stu-id="4c932-156">You need to keep an email message sent by the blocked sender to remove the sender from the blocked sender list.</span></span> <span data-ttu-id="4c932-157">La dirección de correo electrónico del remitente está asociada con los mensajes de correo electrónico enviados por el remitente.</span><span class="sxs-lookup"><span data-stu-id="4c932-157">The sender's email address is associated with email messages that have been sent by the sender.</span></span> <span data-ttu-id="4c932-158">Si se quita un remitente de la lista de remitentes bloqueados, no se realizará correctamente si el mensaje de correo de referencia ya no existe en el buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="4c932-158">Removing a sender from the blocked sender list will not succeed if the reference email message no longer exists in the user's mailbox.</span></span> <span data-ttu-id="4c932-159">El identificador del elemento que se usa para asociar un mensaje de correo electrónico con su remitente debe estar asociado con un elemento que exista en el buzón de Exchange.</span><span class="sxs-lookup"><span data-stu-id="4c932-159">The item identifier used to associate an email message with its sender must be associated with an item that exists in the Exchange mailbox.</span></span> <span data-ttu-id="4c932-160">Le recomendamos que cree una carpeta oculta para almacenar los elementos enviados por los remitentes previamente bloqueados para que los remitentes se puedan desbloquear desde la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="4c932-160">We recommend that you create a hidden folder to store items sent by previously blocked senders so that the senders can be unblocked from the client application.</span></span> <span data-ttu-id="4c932-161">En el caso de que se haya quitado un elemento del buzón de Exchange, un administrador tiene que usar la consola de administración de Exchange para tener acceso a la lista de remitentes bloqueados y quitar un remitente de la lista.</span><span class="sxs-lookup"><span data-stu-id="4c932-161">In the event that an item has been removed from the Exchange mailbox, an administrator has to use the Exchange Management Console to access the blocked sender list to remove a sender from the list.</span></span> <span data-ttu-id="4c932-162">Para obtener información acerca de cómo desbloquear un usuario mediante la consola de administración de Exchange, consulte [How to Configure The Safe Senders and blocked Senders Settings in Office 365](https://support.microsoft.com/kb/2545137).</span><span class="sxs-lookup"><span data-stu-id="4c932-162">For information about how to unblock a user by using the Exchange Management Console, see [How to configure the safe senders and blocked senders settings in Office 365](https://support.microsoft.com/kb/2545137).</span></span>
  
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
      <m:MarkAsJunk IsJunk="false" MoveItem="true">
        <m:ItemIds>
          <t:ItemId Id="AAMkAD=" ChangeKey="CQAAABYu" />
        </m:ItemIds>
      </m:MarkAsJunk>
    </soap:Body>
 </soap:Envelope>

```

<span data-ttu-id="4c932-163">Una respuesta correcta para quitar un remitente de la lista de remitentes bloqueados es la misma que la respuesta para agregar un remitente a la lista de remitentes bloqueados.</span><span class="sxs-lookup"><span data-stu-id="4c932-163">A successful response for removing a sender from the blocked sender list is the same as the response for adding a sender to the blocked sender list.</span></span>
  
<span data-ttu-id="4c932-164">El cuerpo SOAP de la solicitud contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="4c932-164">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="4c932-165">MarkAsJunk</span><span class="sxs-lookup"><span data-stu-id="4c932-165">MarkAsJunk</span></span>](markasjunk.md)
    
- [<span data-ttu-id="4c932-166">ItemIds</span><span class="sxs-lookup"><span data-stu-id="4c932-166">ItemIds</span></span>](itemids.md)
    
- [<span data-ttu-id="4c932-167">ItemId</span><span class="sxs-lookup"><span data-stu-id="4c932-167">ItemId</span></span>](itemid.md)
    
## <a name="markasjunk-operation-error-response"></a><span data-ttu-id="4c932-168">Respuesta de error de operación de MarkAsJunk</span><span class="sxs-lookup"><span data-stu-id="4c932-168">MarkAsJunk operation error response</span></span>

<span data-ttu-id="4c932-169">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **MarkAsJunk** .</span><span class="sxs-lookup"><span data-stu-id="4c932-169">The following example shows an error response to a **MarkAsJunk** operation request.</span></span> <span data-ttu-id="4c932-170">Se trata de una respuesta a una solicitud de adición o eliminación de un remitente de la lista de remitentes bloqueados cuando el mensaje de correo electrónico especificado por el identificador de elemento ya no existe en el buzón.</span><span class="sxs-lookup"><span data-stu-id="4c932-170">This is a response to a request to add or remove a sender from the blocked sender list when the email message specified by the item identifier no longer exists in the mailbox.</span></span> 
  
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
    <m:MarkAsJunkResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="4c932-171">El cuerpo SOAP de respuesta de error contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="4c932-171">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="4c932-172">MarkAsJunkResponse</span><span class="sxs-lookup"><span data-stu-id="4c932-172">MarkAsJunkResponse</span></span>](markasjunkresponse.md)
    
- [<span data-ttu-id="4c932-173">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="4c932-173">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="4c932-174">MarkAsJunkResponseMessage</span><span class="sxs-lookup"><span data-stu-id="4c932-174">MarkAsJunkResponseMessage</span></span>](markasjunkresponsemessage.md)
    
- [<span data-ttu-id="4c932-175">MessageText</span><span class="sxs-lookup"><span data-stu-id="4c932-175">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="4c932-176">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="4c932-176">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="4c932-177">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="4c932-177">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="4c932-178">Vea también</span><span class="sxs-lookup"><span data-stu-id="4c932-178">See also</span></span>

- [<span data-ttu-id="4c932-179">Operaciones de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="4c932-179">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- <span data-ttu-id="4c932-180">[GetItem Operation](getitem-operation.md) GetItem Operation</span><span class="sxs-lookup"><span data-stu-id="4c932-180">[GetItem operation](getitem-operation.md) GetItem operation</span></span> 
    
- [<span data-ttu-id="4c932-181">Operación FindItem</span><span class="sxs-lookup"><span data-stu-id="4c932-181">FindItem operation</span></span>](finditem-operation.md)
    

