---
title: Operación GetHoldOnMailboxes
manager: sethgros
ms.date: 01/24/2020
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9157f329-80b4-4cd0-a158-378064966ae6
description: Buscar información sobre la operación de EWS de GetHoldOnMailboxes.
ms.openlocfilehash: 867f38be87e60af8708eeb0b9d0e3ac8eee6ff64
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457735"
---
# <a name="getholdonmailboxes-operation"></a><span data-ttu-id="af10f-103">Operación GetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="af10f-103">GetHoldOnMailboxes operation</span></span>

> [!IMPORTANT]
> <span data-ttu-id="af10f-104">A partir del 1 de abril de 2020, la operación GetHoldOnMailboxes ya no estará disponible en Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="af10f-104">Starting on April 1, 2020, the GetHoldOnMailboxes operation will no longer be available in Exchange Online.</span></span> <span data-ttu-id="af10f-105">Esta operación no se verá afectada en las versiones locales de Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="af10f-105">This operation won't be affected in on-premises versions of Exchange Server.</span></span> <span data-ttu-id="af10f-106">Para obtener más información, vea [jubilación de las herramientas de eDiscovery heredadas en Exchange Online](https://docs.microsoft.com/microsoft-365/compliance/legacy-ediscovery-retirement#getsearchablemailboxes-setholdonmailboxes-and-getholdonmailboxes-operations-in-the-ews-api).</span><span class="sxs-lookup"><span data-stu-id="af10f-106">For more information, see [Retirement of legacy eDiscovery tools in Exchange Online](https://docs.microsoft.com/microsoft-365/compliance/legacy-ediscovery-retirement#getsearchablemailboxes-setholdonmailboxes-and-getholdonmailboxes-operations-in-the-ews-api).</span></span>

<span data-ttu-id="af10f-107">Buscar información sobre la operación de EWS de **GetHoldOnMailboxes** .</span><span class="sxs-lookup"><span data-stu-id="af10f-107">Find information about the **GetHoldOnMailboxes** EWS operation.</span></span> 
  
<span data-ttu-id="af10f-108">La operación **GetHoldOnMailboxes** obtiene los buzones que están en una suspensión específica y la consulta de retención asociada.</span><span class="sxs-lookup"><span data-stu-id="af10f-108">The **GetHoldOnMailboxes** operation gets the mailboxes that are under a specific hold and the associated hold query.</span></span> 
  
<span data-ttu-id="af10f-109">Esta operación se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="af10f-109">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getholdonmailboxes-operation"></a><span data-ttu-id="af10f-110">Uso de la operación GetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="af10f-110">Using the GetHoldOnMailboxes operation</span></span>

<span data-ttu-id="af10f-111">La operación **GetHoldOnMailboxes** proporciona a la información de cliente los buzones que se colocan en una suspensión específica, información sobre la consulta de espera asociada a cada suspensión, si procede, e información sobre el estado de conservación de cada buzón.</span><span class="sxs-lookup"><span data-stu-id="af10f-111">The **GetHoldOnMailboxes** operation gives the client information about which mailboxes are placed under a specific hold, information about the hold query associated with each hold, if applicable, and information about the hold status for each mailbox.</span></span> <span data-ttu-id="af10f-112">Para obtener más información acerca de las suspensiones de buzones, incluidas las suspensiones basadas en consultas, vea [in-Place Hold](https://technet.microsoft.com/library/ff637980%28v=exchg.150%29) en TechNet.</span><span class="sxs-lookup"><span data-stu-id="af10f-112">For more information about mailbox holds, including query-based holds, see [In-Place Hold](https://technet.microsoft.com/library/ff637980%28v=exchg.150%29) on TechNet.</span></span> 
  
### <a name="getholdonmailboxes-operation-soap-headers"></a><span data-ttu-id="af10f-113">Encabezados SOAP de operación GetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="af10f-113">GetHoldOnMailboxes operation SOAP headers</span></span>

<span data-ttu-id="af10f-114">La operación **GetHoldOnMailboxes** puede usar los encabezados SOAP que se enumeran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="af10f-114">The **GetHoldOnMailboxes** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="af10f-115">**Nombre de encabezado**</span><span class="sxs-lookup"><span data-stu-id="af10f-115">**Header name**</span></span>|<span data-ttu-id="af10f-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="af10f-116">**Element**</span></span>|<span data-ttu-id="af10f-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="af10f-117">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="af10f-118">**ManagementRole**</span><span class="sxs-lookup"><span data-stu-id="af10f-118">**ManagementRole**</span></span> <br/> |[<span data-ttu-id="af10f-119">ManagementRole</span><span class="sxs-lookup"><span data-stu-id="af10f-119">ManagementRole</span></span>](managementrole.md) <br/> |<span data-ttu-id="af10f-120">Identifica los roles de servidor que son necesarios para que el autor de la llamada realice la solicitud.</span><span class="sxs-lookup"><span data-stu-id="af10f-120">Identifies the server roles that are necessary in order for the caller to make the request.</span></span> <span data-ttu-id="af10f-121">Este encabezado se aplica a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="af10f-121">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="af10f-122">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="af10f-122">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="af10f-123">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="af10f-123">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="af10f-124">Identifica la versión del esquema para la solicitud de operación.</span><span class="sxs-lookup"><span data-stu-id="af10f-124">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="af10f-125">Este encabezado se aplica a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="af10f-125">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="af10f-126">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="af10f-126">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="af10f-127">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="af10f-127">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="af10f-128">Identifica la versión del servidor que respondió a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="af10f-128">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="af10f-129">Este encabezado se aplica a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="af10f-129">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getholdonmailboxes-operation-request-example-get-mailbox-hold-information"></a><span data-ttu-id="af10f-130">Ejemplo de solicitud de operación GetHoldOnMailboxes: obtener información de retención de buzón</span><span class="sxs-lookup"><span data-stu-id="af10f-130">GetHoldOnMailboxes operation request example: Get mailbox hold information</span></span>

<span data-ttu-id="af10f-131">El siguiente ejemplo de una solicitud de operación de **GetHoldOnMailboxes** muestra cómo obtener la información de retención de buzones para la retención de buzones de HoldId2.</span><span class="sxs-lookup"><span data-stu-id="af10f-131">The following example of a **GetHoldOnMailboxes** operation request shows how to get the mailbox hold information for the HoldId2 mailbox hold.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:GetHoldOnMailboxes>
         <m:HoldId>HoldId2</m:HoldId>
      </m:GetHoldOnMailboxes>
   </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="af10f-132">El cuerpo SOAP de la solicitud contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="af10f-132">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="af10f-133">GetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="af10f-133">GetHoldOnMailboxes</span></span>](getholdonmailboxes.md)
    
- [<span data-ttu-id="af10f-134">HoldId</span><span class="sxs-lookup"><span data-stu-id="af10f-134">HoldId</span></span>](holdid.md)
    
## <a name="successful-getholdonmailboxes-operation-response"></a><span data-ttu-id="af10f-135">Respuesta de operación GetHoldOnMailboxes correcta</span><span class="sxs-lookup"><span data-stu-id="af10f-135">Successful GetHoldOnMailboxes operation response</span></span>

<span data-ttu-id="af10f-136">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación de **GetHoldOnMailboxes** para obtener la información de retención de buzones para la retención de buzones de HoldId2.</span><span class="sxs-lookup"><span data-stu-id="af10f-136">The following example shows a successful response to a **GetHoldOnMailboxes** operation request to get the mailbox hold information for the HoldId2 mailbox hold.</span></span> 
  
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
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetHoldOnMailboxesResponse ResponseClass="Success" 
                                  xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <MailboxHoldResult>
            <HoldId xmlns="https://schemas.microsoft.com/exchange/services/2006/types">HoldId2</HoldId>
            <Query xmlns="https://schemas.microsoft.com/exchange/services/2006/types">test</Query>
            <MailboxHoldStatuses xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <MailboxHoldStatus>
                  <Mailbox>/o=First Organization/ou=Exchange Administrative Group (FYDIBPDLT)/cn=Recipients/cn=ecc0fd98c2cadf-Willi</Mailbox>
                  <Status>OnHold</Status>
                  <AdditionalInfo/>
               </MailboxHoldStatus>
               <MailboxHoldStatus>
                  <Mailbox>/o=First Organization/ou=Exchange Administrative Group (FYDIBPDLT)/cn=Recipients/cn=dasdat341q8de95-Micha</Mailbox>
                  <Status>OnHold</Status>
                  <AdditionalInfo/>
               </MailboxHoldStatus>
            </MailboxHoldStatuses>
         </MailboxHoldResult>
      </GetHoldOnMailboxesResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="af10f-137">El cuerpo SOAP de respuesta contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="af10f-137">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="af10f-138">GetHoldOnMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="af10f-138">GetHoldOnMailboxesResponse</span></span>](getholdonmailboxesresponse.md)
    
- [<span data-ttu-id="af10f-139">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="af10f-139">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="af10f-140">MailboxHoldResult</span><span class="sxs-lookup"><span data-stu-id="af10f-140">MailboxHoldResult</span></span>](mailboxholdresult.md)
    
- [<span data-ttu-id="af10f-141">HoldId</span><span class="sxs-lookup"><span data-stu-id="af10f-141">HoldId</span></span>](holdid.md)
    
- [<span data-ttu-id="af10f-142">Query</span><span class="sxs-lookup"><span data-stu-id="af10f-142">Query</span></span>](query.md)
    
- [<span data-ttu-id="af10f-143">MailboxHoldStatuses</span><span class="sxs-lookup"><span data-stu-id="af10f-143">MailboxHoldStatuses</span></span>](mailboxholdstatuses.md)
    
- [<span data-ttu-id="af10f-144">MailboxHoldStatus</span><span class="sxs-lookup"><span data-stu-id="af10f-144">MailboxHoldStatus</span></span>](mailboxholdstatus.md)
    
- [<span data-ttu-id="af10f-145">Mailbox (cadena)</span><span class="sxs-lookup"><span data-stu-id="af10f-145">Mailbox (string)</span></span>](mailbox-string.md)
    
- [<span data-ttu-id="af10f-146">Estado (HoldStatusType)</span><span class="sxs-lookup"><span data-stu-id="af10f-146">Status (HoldStatusType)</span></span>](status-holdstatustype.md)
    
- [<span data-ttu-id="af10f-147">AdditionalInfo</span><span class="sxs-lookup"><span data-stu-id="af10f-147">AdditionalInfo</span></span>](additionalinfo.md)
    
## <a name="getholdonmailboxes-operation-error-response"></a><span data-ttu-id="af10f-148">Respuesta de error de operación de GetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="af10f-148">GetHoldOnMailboxes operation error response</span></span>

<span data-ttu-id="af10f-149">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **GetHoldOnMailboxes** .</span><span class="sxs-lookup"><span data-stu-id="af10f-149">The following example shows an error response to a **GetHoldOnMailboxes** operation request.</span></span> <span data-ttu-id="af10f-150">Se trata de una respuesta a una solicitud para obtener una retención que se ha eliminado.</span><span class="sxs-lookup"><span data-stu-id="af10f-150">This is a response to a request to get a hold that has been deleted.</span></span> 
  
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
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetHoldOnMailboxesResponse ResponseClass="Error" 
                                  xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>The specific query-based hold is not found.</MessageText>
         <ResponseCode>ErrorMailboxHoldNotFound</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </GetHoldOnMailboxesResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="af10f-151">El cuerpo SOAP de respuesta de error contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="af10f-151">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="af10f-152">GetHoldOnMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="af10f-152">GetHoldOnMailboxesResponse</span></span>](getholdonmailboxesresponse.md)
    
- [<span data-ttu-id="af10f-153">MessageText</span><span class="sxs-lookup"><span data-stu-id="af10f-153">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="af10f-154">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="af10f-154">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="af10f-155">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="af10f-155">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="af10f-156">Para obtener los códigos de error adicionales que son genéricos para EWS y específicos de esta operación, vea [ResponseCode](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="af10f-156">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="af10f-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="af10f-157">See also</span></span>

- [<span data-ttu-id="af10f-158">Operaciones de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="af10f-158">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="af10f-159">Operación GetSearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="af10f-159">GetSearchableMailboxes operation</span></span>](getsearchablemailboxes-operation.md)
    
- [<span data-ttu-id="af10f-160">Operación SearchMailboxes</span><span class="sxs-lookup"><span data-stu-id="af10f-160">SearchMailboxes operation</span></span>](searchmailboxes-operation.md)
    
- [<span data-ttu-id="af10f-161">Operación SetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="af10f-161">SetHoldOnMailboxes operation</span></span>](setholdonmailboxes-operation.md)
    
- [<span data-ttu-id="af10f-162">Operación GetDiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="af10f-162">GetDiscoverySearchConfiguration operation</span></span>](getdiscoverysearchconfiguration-operation.md)
    
- [<span data-ttu-id="af10f-163">Operación GetNonIndexableItemDetails</span><span class="sxs-lookup"><span data-stu-id="af10f-163">GetNonIndexableItemDetails operation</span></span>](getnonindexableitemdetails-operation.md)
    
- [<span data-ttu-id="af10f-164">Operación GetNonIndexableItemStatistics</span><span class="sxs-lookup"><span data-stu-id="af10f-164">GetNonIndexableItemStatistics operation</span></span>](getnonindexableitemstatistics-operation.md)
    

