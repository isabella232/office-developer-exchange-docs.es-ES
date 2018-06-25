---
title: Operación PerformReminderAction
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c597bb0e-13b0-422e-9c23-970463e2a5c3
description: Busque información sobre la EWS PerformReminderAction operación.
ms.openlocfilehash: 778fbb508413721f58cfcf9143a5296874e6cd1c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836722"
---
# <a name="performreminderaction-operation"></a><span data-ttu-id="45a54-103">Operación PerformReminderAction</span><span class="sxs-lookup"><span data-stu-id="45a54-103">PerformReminderAction operation</span></span>

<span data-ttu-id="45a54-104">Obtenga información acerca de la operación de EWS **PerformReminderAction** .</span><span class="sxs-lookup"><span data-stu-id="45a54-104">Find information about the **PerformReminderAction** EWS operation.</span></span> 
  
<span data-ttu-id="45a54-105">La operación de Exchange Web Services (EWS) **PerformReminderAction** inicia una acción descartar o posponer en un aviso.</span><span class="sxs-lookup"><span data-stu-id="45a54-105">The **PerformReminderAction** Exchange Web Services (EWS) operation initiates a dismiss or snooze action on a reminder.</span></span> 
  
<span data-ttu-id="45a54-106">Esta operación se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="45a54-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-performreminderaction-operation"></a><span data-ttu-id="45a54-107">Mediante la operación PerformReminderAction</span><span class="sxs-lookup"><span data-stu-id="45a54-107">Using the PerformReminderAction operation</span></span>

<span data-ttu-id="45a54-108">Puede usar la operación **PerformReminderAction** para descartar o posponer avisos (retraso) devueltos por la operación [GetReminders](getreminders-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="45a54-108">You can use the **PerformReminderAction** operation to dismiss or snooze (delay) reminders returned by the [GetReminders](getreminders-operation.md) operation.</span></span> <span data-ttu-id="45a54-109">Para posponer un aviso, establezca el [ActionType](actiontype-reminderactiontype.md) para **Posponer**y establezca el valor de [NewReminderTime](newremindertime.md) en un momento posterior a la actual [ReminderTime](remindertime.md), en caso contrario, el **NewReminderTime** se omite el servidor.</span><span class="sxs-lookup"><span data-stu-id="45a54-109">To snooze a reminder, set the [ActionType](actiontype-reminderactiontype.md) to **Snooze**, and set the [NewReminderTime](newremindertime.md) value to a time later than the current [ReminderTime](remindertime.md), otherwise the **NewReminderTime** is ignored by the server.</span></span> <span data-ttu-id="45a54-110">Si el aviso es para una aparición de una reunión periódica, y se realiza la acción **Posponer** en el aviso con un **NewReminderTime** que está más allá del aviso de la siguiente aparición, eficazmente se omite el aviso.</span><span class="sxs-lookup"><span data-stu-id="45a54-110">If the reminder is for an occurrence of a recurring meeting, and the **Snooze** action is taken on the reminder with a **NewReminderTime** that is past the reminder of the next occurrence, the reminder is effectively dismissed.</span></span> 
  
<span data-ttu-id="45a54-111">Para descartar un aviso, establezca el **ActionType** en **Descartar**.</span><span class="sxs-lookup"><span data-stu-id="45a54-111">To dismiss a reminder, set the **ActionType** to **Dismiss**.</span></span> <span data-ttu-id="45a54-112">Cuando el servidor procesa la solicitud, el servidor cambia el valor de [IsReminderSet](isreminderset.md) para el elemento de **True** a **False**.</span><span class="sxs-lookup"><span data-stu-id="45a54-112">When the server processes the request, the server changes the [IsReminderSet](isreminderset.md) value for the item from **True** to **False**.</span></span>
  
### <a name="performreminderaction-operation-soap-headers"></a><span data-ttu-id="45a54-113">Encabezados SOAP de operación de PerformReminderAction</span><span class="sxs-lookup"><span data-stu-id="45a54-113">PerformReminderAction operation SOAP headers</span></span>

<span data-ttu-id="45a54-114">La operación de **PerformReminderAction** puede utilizar los encabezados SOAP que se enumeran en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="45a54-114">The **PerformReminderAction** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="45a54-115">**Nombre de encabezado**</span><span class="sxs-lookup"><span data-stu-id="45a54-115">**Header name**</span></span>|<span data-ttu-id="45a54-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="45a54-116">**Element**</span></span>|<span data-ttu-id="45a54-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="45a54-117">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="45a54-118">**Suplantación**</span><span class="sxs-lookup"><span data-stu-id="45a54-118">**Impersonation**</span></span> <br/> |[<span data-ttu-id="45a54-119">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="45a54-119">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="45a54-120">Identifica el usuario que está realizando la suplantación de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="45a54-120">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="45a54-121">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="45a54-121">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="45a54-122">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="45a54-122">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="45a54-123">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="45a54-123">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="45a54-124">Identifica la referencia cultural, como se define en RFC 3066, "Etiquetas para la identificación de idiomas," que se utilizará para acceder al buzón.</span><span class="sxs-lookup"><span data-stu-id="45a54-124">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="45a54-125">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="45a54-125">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="45a54-126">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="45a54-126">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="45a54-127">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="45a54-127">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="45a54-128">Identifica la versión del esquema para la solicitud de la operación.</span><span class="sxs-lookup"><span data-stu-id="45a54-128">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="45a54-129">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="45a54-129">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="45a54-130">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="45a54-130">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="45a54-131">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="45a54-131">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="45a54-132">Identifica la versión del servidor que ha respondido a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="45a54-132">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="45a54-133">Este encabezado es aplicable a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="45a54-133">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="performreminderaction-operation-request-example"></a><span data-ttu-id="45a54-134">Ejemplo de solicitud de operación de PerformReminderAction</span><span class="sxs-lookup"><span data-stu-id="45a54-134">PerformReminderAction operation request example</span></span>

<span data-ttu-id="45a54-135">El siguiente ejemplo de una solicitud de operación **PerformReminderAction** muestra cómo aplazar un aviso actual y establecer una hora de aviso de nuevo.</span><span class="sxs-lookup"><span data-stu-id="45a54-135">The following example of a **PerformReminderAction** operation request shows how to snooze a current reminder and set a new reminder time.</span></span> <span data-ttu-id="45a54-136">Tenga en cuenta que debe incluir el **ChangeKey** para el [ItemId](itemid.md) y la **NewReminderTime** se debe establecer en una hora posterior a la **ReminderTime** devuelto por la operación [GetReminders](getreminders-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="45a54-136">Note that you need to include the **ChangeKey** for the [ItemId](itemid.md) and the **NewReminderTime** must be set to a time later than the **ReminderTime** returned by the [GetReminders](getreminders-operation.md) operation.</span></span> 
  
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
> <span data-ttu-id="45a54-137">Se ha reducido el valor **ItemId** para conservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="45a54-137">The **ItemId** value has been shortened to preserve readability.</span></span> 
  
<span data-ttu-id="45a54-138">La solicitud SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="45a54-138">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="45a54-139">PerformReminderAction</span><span class="sxs-lookup"><span data-stu-id="45a54-139">PerformReminderAction</span></span>](performreminderaction.md)
    
- [<span data-ttu-id="45a54-140">ReminderItemActions</span><span class="sxs-lookup"><span data-stu-id="45a54-140">ReminderItemActions</span></span>](reminderitemactions.md)
    
- [<span data-ttu-id="45a54-141">ReminderItemAction</span><span class="sxs-lookup"><span data-stu-id="45a54-141">ReminderItemAction</span></span>](reminderitemaction.md)
    
- [<span data-ttu-id="45a54-142">ActionType</span><span class="sxs-lookup"><span data-stu-id="45a54-142">ActionType</span></span>](actiontype-reminderactiontype.md)
    
- [<span data-ttu-id="45a54-143">ItemId</span><span class="sxs-lookup"><span data-stu-id="45a54-143">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="45a54-144">NewReminderTime</span><span class="sxs-lookup"><span data-stu-id="45a54-144">NewReminderTime</span></span>](newremindertime.md)
    
## <a name="successful-performreminderaction-operation-response"></a><span data-ttu-id="45a54-145">Respuesta es correcta de operación PerformReminderAction</span><span class="sxs-lookup"><span data-stu-id="45a54-145">Successful PerformReminderAction operation response</span></span>

<span data-ttu-id="45a54-146">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación **PerformReminderAction** .</span><span class="sxs-lookup"><span data-stu-id="45a54-146">The following example shows a successful response to a **PerformReminderAction** operation request.</span></span> <span data-ttu-id="45a54-147">El elemento **UpdatedItemIds** contiene el **ItemID** del elemento de calendario actualizados.</span><span class="sxs-lookup"><span data-stu-id="45a54-147">The **UpdatedItemIds** element contains the **ItemIds** of the updated calendar item.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <ServerVersionInfo MajorVersion="15"
                       MinorVersion="0"
                       MajorBuildNumber="921"
                       MinorBuildNumber="20"
                       Version="V2_10"
                       xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <PerformReminderActionResponse ResponseClass="Success"
                                   xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <UpdatedItemIds>
        <ItemId Id="vwAAAA=="
                ChangeKey="DwAAABYAAAB4to43JyybTYwHLBM1k8MxAAAJKP+S"/>
      </UpdatedItemIds>
    </PerformReminderActionResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="45a54-148">La respuesta SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="45a54-148">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="45a54-149">PerformReminderActionResponse</span><span class="sxs-lookup"><span data-stu-id="45a54-149">PerformReminderActionResponse</span></span>](performreminderactionresponse.md)
    
- [<span data-ttu-id="45a54-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="45a54-150">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="45a54-151">UpdatedItemIds</span><span class="sxs-lookup"><span data-stu-id="45a54-151">UpdatedItemIds</span></span>](updateditemids.md)
    
- [<span data-ttu-id="45a54-152">ItemId</span><span class="sxs-lookup"><span data-stu-id="45a54-152">ItemId</span></span>](itemid.md)
    
## <a name="performreminderaction-operation-error-response-example"></a><span data-ttu-id="45a54-153">Ejemplo de respuesta de error de operación de PerformReminderAction</span><span class="sxs-lookup"><span data-stu-id="45a54-153">PerformReminderAction operation error response example</span></span>

<span data-ttu-id="45a54-154">En el ejemplo siguiente se muestra una respuesta a una solicitud de operación **PerformReminderAction** cuando se realizó ningún cambio en el servidor.</span><span class="sxs-lookup"><span data-stu-id="45a54-154">The following example shows a response to a **PerformReminderAction** operation request when no change was made on the server.</span></span> <span data-ttu-id="45a54-155">Esta es una respuesta en el que se envió una solicitud, pero se han devuelto no **UpdatedItemIds** , lo que significa que no hay avisos se han cambiado.</span><span class="sxs-lookup"><span data-stu-id="45a54-155">This is a response in which a request was sent, but no **UpdatedItemIds** were returned, meaning no reminders were changed.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <ServerVersionInfo MajorVersion="15"
                       MinorVersion="0"
                       MajorBuildNumber="918"
                       MinorBuildNumber="7"
                       Version="V2_10"
                       xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <PerformReminderActionResponse ResponseClass="Success"
                                   xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <UpdatedItemIds />
    </PerformReminderActionResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="45a54-156">La respuesta de error SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="45a54-156">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="45a54-157">PerformReminderActionResponse</span><span class="sxs-lookup"><span data-stu-id="45a54-157">PerformReminderActionResponse</span></span>](performreminderactionresponse.md)
    
- [<span data-ttu-id="45a54-158">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="45a54-158">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="45a54-159">UpdatedItemIds</span><span class="sxs-lookup"><span data-stu-id="45a54-159">UpdatedItemIds</span></span>](updateditemids.md)
    
<span data-ttu-id="45a54-160">Para códigos de error adicionales que son genéricos de EWS, consulte [ResponseCode](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="45a54-160">For additional error codes that are generic to EWS, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="45a54-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="45a54-161">See also</span></span>


- [<span data-ttu-id="45a54-162">Operación GetReminders</span><span class="sxs-lookup"><span data-stu-id="45a54-162">GetReminders operation</span></span>](getreminders-operation.md)
    

