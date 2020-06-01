---
title: Operación PerformReminderAction
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c597bb0e-13b0-422e-9c23-970463e2a5c3
description: Buscar información sobre la operación de EWS de PerformReminderAction.
ms.openlocfilehash: 4c069d541e9a42167c447a50c405399958d3608d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462293"
---
# <a name="performreminderaction-operation"></a><span data-ttu-id="4fb05-103">Operación PerformReminderAction</span><span class="sxs-lookup"><span data-stu-id="4fb05-103">PerformReminderAction operation</span></span>

<span data-ttu-id="4fb05-104">Buscar información sobre la operación de EWS de **PerformReminderAction** .</span><span class="sxs-lookup"><span data-stu-id="4fb05-104">Find information about the **PerformReminderAction** EWS operation.</span></span> 
  
<span data-ttu-id="4fb05-105">La operación de los servicios web Exchange (EWS) de **PerformReminderAction** inicia una acción de descartar o posponer en un aviso.</span><span class="sxs-lookup"><span data-stu-id="4fb05-105">The **PerformReminderAction** Exchange Web Services (EWS) operation initiates a dismiss or snooze action on a reminder.</span></span> 
  
<span data-ttu-id="4fb05-106">Esta operación se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="4fb05-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-performreminderaction-operation"></a><span data-ttu-id="4fb05-107">Uso de la operación PerformReminderAction</span><span class="sxs-lookup"><span data-stu-id="4fb05-107">Using the PerformReminderAction operation</span></span>

<span data-ttu-id="4fb05-108">Puede usar la operación **PerformReminderAction** para descartar o posponer (retrasar) los avisos devueltos por la operación [GetReminders](getreminders-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="4fb05-108">You can use the **PerformReminderAction** operation to dismiss or snooze (delay) reminders returned by the [GetReminders](getreminders-operation.md) operation.</span></span> <span data-ttu-id="4fb05-109">Para posponer un aviso, establezca [ActionType](actiontype-reminderactiontype.md) en **SNOOZE**y establezca el valor de [NewReminderTime](newremindertime.md) en una hora posterior a la [ReminderTime](remindertime.md)actual, de lo contrario el servidor omite el **NewReminderTime** .</span><span class="sxs-lookup"><span data-stu-id="4fb05-109">To snooze a reminder, set the [ActionType](actiontype-reminderactiontype.md) to **Snooze**, and set the [NewReminderTime](newremindertime.md) value to a time later than the current [ReminderTime](remindertime.md), otherwise the **NewReminderTime** is ignored by the server.</span></span> <span data-ttu-id="4fb05-110">Si el aviso es para una ocurrencia de una reunión periódica y se lleva a cabo la acción de **posponer** en el aviso con un **NewReminderTime** que supera el aviso de la siguiente repetición, el aviso se descarta de manera efectiva.</span><span class="sxs-lookup"><span data-stu-id="4fb05-110">If the reminder is for an occurrence of a recurring meeting, and the **Snooze** action is taken on the reminder with a **NewReminderTime** that is past the reminder of the next occurrence, the reminder is effectively dismissed.</span></span> 
  
<span data-ttu-id="4fb05-111">Para descartar un aviso, establezca **ActionType** en **Dismiss**.</span><span class="sxs-lookup"><span data-stu-id="4fb05-111">To dismiss a reminder, set the **ActionType** to **Dismiss**.</span></span> <span data-ttu-id="4fb05-112">Cuando el servidor procesa la solicitud, el servidor cambia el valor [IsReminderSet](isreminderset.md) para el elemento de **true** a **false**.</span><span class="sxs-lookup"><span data-stu-id="4fb05-112">When the server processes the request, the server changes the [IsReminderSet](isreminderset.md) value for the item from **True** to **False**.</span></span>
  
### <a name="performreminderaction-operation-soap-headers"></a><span data-ttu-id="4fb05-113">Encabezados SOAP de operación PerformReminderAction</span><span class="sxs-lookup"><span data-stu-id="4fb05-113">PerformReminderAction operation SOAP headers</span></span>

<span data-ttu-id="4fb05-114">La operación **PerformReminderAction** puede usar los encabezados SOAP que se enumeran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="4fb05-114">The **PerformReminderAction** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="4fb05-115">**Nombre de encabezado**</span><span class="sxs-lookup"><span data-stu-id="4fb05-115">**Header name**</span></span>|<span data-ttu-id="4fb05-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="4fb05-116">**Element**</span></span>|<span data-ttu-id="4fb05-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4fb05-117">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4fb05-118">**Suplantación**</span><span class="sxs-lookup"><span data-stu-id="4fb05-118">**Impersonation**</span></span> <br/> |[<span data-ttu-id="4fb05-119">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="4fb05-119">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="4fb05-120">Identifica al usuario que está suplantando la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="4fb05-120">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="4fb05-121">Este encabezado se aplica a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="4fb05-121">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="4fb05-122">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="4fb05-122">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="4fb05-123">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="4fb05-123">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="4fb05-124">Identifica la referencia cultural, tal y como se define en RFC 3066, "etiquetas para la identificación de idiomas", que se va a usar para obtener acceso al buzón.</span><span class="sxs-lookup"><span data-stu-id="4fb05-124">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="4fb05-125">Este encabezado se aplica a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="4fb05-125">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="4fb05-126">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="4fb05-126">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="4fb05-127">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="4fb05-127">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="4fb05-128">Identifica la versión del esquema para la solicitud de operación.</span><span class="sxs-lookup"><span data-stu-id="4fb05-128">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="4fb05-129">Este encabezado se aplica a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="4fb05-129">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="4fb05-130">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="4fb05-130">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="4fb05-131">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="4fb05-131">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="4fb05-132">Identifica la versión del servidor que respondió a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4fb05-132">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="4fb05-133">Este encabezado se aplica a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="4fb05-133">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="performreminderaction-operation-request-example"></a><span data-ttu-id="4fb05-134">Ejemplo de solicitud de operación PerformReminderAction</span><span class="sxs-lookup"><span data-stu-id="4fb05-134">PerformReminderAction operation request example</span></span>

<span data-ttu-id="4fb05-135">El siguiente ejemplo de una solicitud de operación de **PerformReminderAction** muestra cómo posponer un aviso actual y establecer una nueva hora de aviso.</span><span class="sxs-lookup"><span data-stu-id="4fb05-135">The following example of a **PerformReminderAction** operation request shows how to snooze a current reminder and set a new reminder time.</span></span> <span data-ttu-id="4fb05-136">Tenga en cuenta que debe incluir **changekey** para [Itemid](itemid.md) y **NewReminderTime** debe estar establecido en una hora posterior a la **ReminderTime** devuelta por la operación [GetReminders](getreminders-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="4fb05-136">Note that you need to include the **ChangeKey** for the [ItemId](itemid.md) and the **NewReminderTime** must be set to a time later than the **ReminderTime** returned by the [GetReminders](getreminders-operation.md) operation.</span></span> 
  
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
    <m:PerformReminderAction>
      <m:ReminderItemActions>
        <t:ReminderItemAction>
          <t:ActionType>Snooze</t:ActionType>
          <t:ItemId Id="vwAAAA=="
           ChangeKey="DwAAABQAAACOs0HEMq1WTKpI7sNu5qXNAAAUDA=="/>
          <t:NewReminderTime>2014-04-16T17:00:00Z</t:NewReminderTime>
        </t:ReminderItemAction>
      </m:ReminderItemActions>
    </m:PerformReminderAction>
  </soap:Body>
</soap:Envelope>
```

> [!NOTE]
> <span data-ttu-id="4fb05-137">El valor de **Itemid** se ha abreviado para preservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="4fb05-137">The **ItemId** value has been shortened to preserve readability.</span></span> 
  
<span data-ttu-id="4fb05-138">El cuerpo SOAP de la solicitud contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="4fb05-138">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="4fb05-139">PerformReminderAction</span><span class="sxs-lookup"><span data-stu-id="4fb05-139">PerformReminderAction</span></span>](performreminderaction.md)
    
- [<span data-ttu-id="4fb05-140">ReminderItemActions</span><span class="sxs-lookup"><span data-stu-id="4fb05-140">ReminderItemActions</span></span>](reminderitemactions.md)
    
- [<span data-ttu-id="4fb05-141">ReminderItemAction</span><span class="sxs-lookup"><span data-stu-id="4fb05-141">ReminderItemAction</span></span>](reminderitemaction.md)
    
- [<span data-ttu-id="4fb05-142">ActionType</span><span class="sxs-lookup"><span data-stu-id="4fb05-142">ActionType</span></span>](actiontype-reminderactiontype.md)
    
- [<span data-ttu-id="4fb05-143">ItemId</span><span class="sxs-lookup"><span data-stu-id="4fb05-143">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="4fb05-144">NewReminderTime</span><span class="sxs-lookup"><span data-stu-id="4fb05-144">NewReminderTime</span></span>](newremindertime.md)
    
## <a name="successful-performreminderaction-operation-response"></a><span data-ttu-id="4fb05-145">Respuesta de operación PerformReminderAction correcta</span><span class="sxs-lookup"><span data-stu-id="4fb05-145">Successful PerformReminderAction operation response</span></span>

<span data-ttu-id="4fb05-146">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación de **PerformReminderAction** .</span><span class="sxs-lookup"><span data-stu-id="4fb05-146">The following example shows a successful response to a **PerformReminderAction** operation request.</span></span> <span data-ttu-id="4fb05-147">El elemento **UpdatedItemIds** contiene la **ItemIds** del elemento de calendario actualizado.</span><span class="sxs-lookup"><span data-stu-id="4fb05-147">The **UpdatedItemIds** element contains the **ItemIds** of the updated calendar item.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <ServerVersionInfo MajorVersion="15"
                       MinorVersion="0"
                       MajorBuildNumber="921"
                       MinorBuildNumber="20"
                       Version="V2_10"
                       xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <PerformReminderActionResponse ResponseClass="Success"
                                   xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <UpdatedItemIds>
        <ItemId Id="vwAAAA=="
                ChangeKey="DwAAABYAAAB4to43JyybTYwHLBM1k8MxAAAJKP+S"/>
      </UpdatedItemIds>
    </PerformReminderActionResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="4fb05-148">El cuerpo SOAP de respuesta contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="4fb05-148">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="4fb05-149">PerformReminderActionResponse</span><span class="sxs-lookup"><span data-stu-id="4fb05-149">PerformReminderActionResponse</span></span>](performreminderactionresponse.md)
    
- [<span data-ttu-id="4fb05-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="4fb05-150">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="4fb05-151">UpdatedItemIds</span><span class="sxs-lookup"><span data-stu-id="4fb05-151">UpdatedItemIds</span></span>](updateditemids.md)
    
- [<span data-ttu-id="4fb05-152">ItemId</span><span class="sxs-lookup"><span data-stu-id="4fb05-152">ItemId</span></span>](itemid.md)
    
## <a name="performreminderaction-operation-error-response-example"></a><span data-ttu-id="4fb05-153">Ejemplo de respuesta de error de operación PerformReminderAction</span><span class="sxs-lookup"><span data-stu-id="4fb05-153">PerformReminderAction operation error response example</span></span>

<span data-ttu-id="4fb05-154">En el ejemplo siguiente se muestra una respuesta a una solicitud de operación de **PerformReminderAction** cuando no se ha realizado ningún cambio en el servidor.</span><span class="sxs-lookup"><span data-stu-id="4fb05-154">The following example shows a response to a **PerformReminderAction** operation request when no change was made on the server.</span></span> <span data-ttu-id="4fb05-155">Se trata de una respuesta en la que se ha enviado una solicitud, pero no se ha devuelto ningún **UpdatedItemIds** , lo que significa que no se ha cambiado ningún aviso.</span><span class="sxs-lookup"><span data-stu-id="4fb05-155">This is a response in which a request was sent, but no **UpdatedItemIds** were returned, meaning no reminders were changed.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <ServerVersionInfo MajorVersion="15"
                       MinorVersion="0"
                       MajorBuildNumber="918"
                       MinorBuildNumber="7"
                       Version="V2_10"
                       xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <PerformReminderActionResponse ResponseClass="Success"
                                   xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <UpdatedItemIds />
    </PerformReminderActionResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="4fb05-156">El cuerpo SOAP de respuesta de error contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="4fb05-156">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="4fb05-157">PerformReminderActionResponse</span><span class="sxs-lookup"><span data-stu-id="4fb05-157">PerformReminderActionResponse</span></span>](performreminderactionresponse.md)
    
- [<span data-ttu-id="4fb05-158">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="4fb05-158">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="4fb05-159">UpdatedItemIds</span><span class="sxs-lookup"><span data-stu-id="4fb05-159">UpdatedItemIds</span></span>](updateditemids.md)
    
<span data-ttu-id="4fb05-160">Para obtener los códigos de error adicionales que son genéricos para EWS, consulte [ResponseCode](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="4fb05-160">For additional error codes that are generic to EWS, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4fb05-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="4fb05-161">See also</span></span>


- [<span data-ttu-id="4fb05-162">Operación GetReminders</span><span class="sxs-lookup"><span data-stu-id="4fb05-162">GetReminders operation</span></span>](getreminders-operation.md)
    

