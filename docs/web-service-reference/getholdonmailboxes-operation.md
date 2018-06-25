---
title: Operación GetHoldOnMailboxes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9157f329-80b4-4cd0-a158-378064966ae6
description: Busque información sobre la EWS GetHoldOnMailboxes operación.
ms.openlocfilehash: 1d0bc2f9d26e11d8d2710693d67843ad2f339a5d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764864"
---
# <a name="getholdonmailboxes-operation"></a><span data-ttu-id="2f8d3-103">Operación GetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="2f8d3-103">GetHoldOnMailboxes operation</span></span>

<span data-ttu-id="2f8d3-104">Obtenga información acerca de la operación de EWS **GetHoldOnMailboxes** .</span><span class="sxs-lookup"><span data-stu-id="2f8d3-104">Find information about the **GetHoldOnMailboxes** EWS operation.</span></span> 
  
<span data-ttu-id="2f8d3-105">La operación **GetHoldOnMailboxes** obtiene los buzones que se encuentran en una suspensión específica y mantenga el asociado consulta.</span><span class="sxs-lookup"><span data-stu-id="2f8d3-105">The **GetHoldOnMailboxes** operation gets the mailboxes that are under a specific hold and the associated hold query.</span></span> 
  
<span data-ttu-id="2f8d3-106">Esta operación se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="2f8d3-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getholdonmailboxes-operation"></a><span data-ttu-id="2f8d3-107">Mediante la operación GetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="2f8d3-107">Using the GetHoldOnMailboxes operation</span></span>

<span data-ttu-id="2f8d3-108">La operación **GetHoldOnMailboxes** proporciona la información del cliente acerca de los buzones de correo se colocan en una suspensión específica, la información acerca de la consulta de espera asociada con cada suspensión, si procede y la información sobre el estado de espera para cada buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="2f8d3-108">The **GetHoldOnMailboxes** operation gives the client information about which mailboxes are placed under a specific hold, information about the hold query associated with each hold, if applicable, and information about the hold status for each mailbox.</span></span> <span data-ttu-id="2f8d3-109">Para obtener más información acerca de las suspensiones de buzón de correo, incluidas las suspensiones basada en consultas, consulte [Conservación local](http://technet.microsoft.com/en-us/library/ff637980%28v=exchg.150%29) en TechNet.</span><span class="sxs-lookup"><span data-stu-id="2f8d3-109">For more information about mailbox holds, including query-based holds, see [In-Place Hold](http://technet.microsoft.com/en-us/library/ff637980%28v=exchg.150%29) on TechNet.</span></span> 
  
### <a name="getholdonmailboxes-operation-soap-headers"></a><span data-ttu-id="2f8d3-110">Encabezados SOAP de operación de GetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="2f8d3-110">GetHoldOnMailboxes operation SOAP headers</span></span>

<span data-ttu-id="2f8d3-111">La operación de **GetHoldOnMailboxes** puede utilizar los encabezados SOAP que se enumeran en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="2f8d3-111">The **GetHoldOnMailboxes** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="2f8d3-112">**Nombre de encabezado**</span><span class="sxs-lookup"><span data-stu-id="2f8d3-112">**Header name**</span></span>|<span data-ttu-id="2f8d3-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="2f8d3-113">**Element**</span></span>|<span data-ttu-id="2f8d3-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2f8d3-114">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2f8d3-115">**ManagementRole**</span><span class="sxs-lookup"><span data-stu-id="2f8d3-115">**ManagementRole**</span></span> <br/> |[<span data-ttu-id="2f8d3-116">ManagementRole</span><span class="sxs-lookup"><span data-stu-id="2f8d3-116">ManagementRole</span></span>](managementrole.md) <br/> |<span data-ttu-id="2f8d3-117">Identifica las funciones de servidor que son necesarias en orden para el autor de la llamada realizar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2f8d3-117">Identifies the server roles that are necessary in order for the caller to make the request.</span></span> <span data-ttu-id="2f8d3-118">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="2f8d3-118">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="2f8d3-119">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="2f8d3-119">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="2f8d3-120">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="2f8d3-120">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="2f8d3-121">Identifica la versión del esquema para la solicitud de la operación.</span><span class="sxs-lookup"><span data-stu-id="2f8d3-121">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="2f8d3-122">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="2f8d3-122">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="2f8d3-123">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="2f8d3-123">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="2f8d3-124">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="2f8d3-124">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="2f8d3-125">Identifica la versión del servidor que ha respondido a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2f8d3-125">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="2f8d3-126">Este encabezado es aplicable a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="2f8d3-126">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getholdonmailboxes-operation-request-example-get-mailbox-hold-information"></a><span data-ttu-id="2f8d3-127">Ejemplo de solicitud de operación de GetHoldOnMailboxes: obtener información de suspensión de buzón de correo</span><span class="sxs-lookup"><span data-stu-id="2f8d3-127">GetHoldOnMailboxes operation request example: Get mailbox hold information</span></span>

<span data-ttu-id="2f8d3-128">El siguiente ejemplo de una solicitud de operación **GetHoldOnMailboxes** muestra cómo obtener la información de suspensión de buzón de correo para la retención de buzón de correo de HoldId2.</span><span class="sxs-lookup"><span data-stu-id="2f8d3-128">The following example of a **GetHoldOnMailboxes** operation request shows how to get the mailbox hold information for the HoldId2 mailbox hold.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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

<span data-ttu-id="2f8d3-129">La solicitud SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="2f8d3-129">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="2f8d3-130">GetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="2f8d3-130">GetHoldOnMailboxes</span></span>](getholdonmailboxes.md)
    
- [<span data-ttu-id="2f8d3-131">HoldId</span><span class="sxs-lookup"><span data-stu-id="2f8d3-131">HoldId</span></span>](holdid.md)
    
## <a name="successful-getholdonmailboxes-operation-response"></a><span data-ttu-id="2f8d3-132">Respuesta es correcta de operación GetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="2f8d3-132">Successful GetHoldOnMailboxes operation response</span></span>

<span data-ttu-id="2f8d3-133">El ejemplo siguiente se muestra una respuesta correcta a una operación **GetHoldOnMailboxes** solicitud para obtener el buzón de correo contiene información para la retención de buzón de correo de HoldId2.</span><span class="sxs-lookup"><span data-stu-id="2f8d3-133">The following example shows a successful response to a **GetHoldOnMailboxes** operation request to get the mailbox hold information for the HoldId2 mailbox hold.</span></span> 
  
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
      <GetHoldOnMailboxesResponse ResponseClass="Success" 
                                  xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <MailboxHoldResult>
            <HoldId xmlns="http://schemas.microsoft.com/exchange/services/2006/types">HoldId2</HoldId>
            <Query xmlns="http://schemas.microsoft.com/exchange/services/2006/types">test</Query>
            <MailboxHoldStatuses xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="2f8d3-134">La respuesta SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="2f8d3-134">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="2f8d3-135">GetHoldOnMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="2f8d3-135">GetHoldOnMailboxesResponse</span></span>](getholdonmailboxesresponse.md)
    
- [<span data-ttu-id="2f8d3-136">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="2f8d3-136">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="2f8d3-137">MailboxHoldResult</span><span class="sxs-lookup"><span data-stu-id="2f8d3-137">MailboxHoldResult</span></span>](mailboxholdresult.md)
    
- [<span data-ttu-id="2f8d3-138">HoldId</span><span class="sxs-lookup"><span data-stu-id="2f8d3-138">HoldId</span></span>](holdid.md)
    
- [<span data-ttu-id="2f8d3-139">Consulta</span><span class="sxs-lookup"><span data-stu-id="2f8d3-139">Query</span></span>](query.md)
    
- [<span data-ttu-id="2f8d3-140">MailboxHoldStatuses</span><span class="sxs-lookup"><span data-stu-id="2f8d3-140">MailboxHoldStatuses</span></span>](mailboxholdstatuses.md)
    
- [<span data-ttu-id="2f8d3-141">MailboxHoldStatus</span><span class="sxs-lookup"><span data-stu-id="2f8d3-141">MailboxHoldStatus</span></span>](mailboxholdstatus.md)
    
- [<span data-ttu-id="2f8d3-142">Buzón de correo (cadena)</span><span class="sxs-lookup"><span data-stu-id="2f8d3-142">Mailbox (string)</span></span>](mailbox-string.md)
    
- [<span data-ttu-id="2f8d3-143">Estado (HoldStatusType)</span><span class="sxs-lookup"><span data-stu-id="2f8d3-143">Status (HoldStatusType)</span></span>](status-holdstatustype.md)
    
- [<span data-ttu-id="2f8d3-144">AdditionalInfo</span><span class="sxs-lookup"><span data-stu-id="2f8d3-144">AdditionalInfo</span></span>](additionalinfo.md)
    
## <a name="getholdonmailboxes-operation-error-response"></a><span data-ttu-id="2f8d3-145">Respuesta de error de la operación de GetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="2f8d3-145">GetHoldOnMailboxes operation error response</span></span>

<span data-ttu-id="2f8d3-146">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **GetHoldOnMailboxes** .</span><span class="sxs-lookup"><span data-stu-id="2f8d3-146">The following example shows an error response to a **GetHoldOnMailboxes** operation request.</span></span> <span data-ttu-id="2f8d3-147">Esta es una respuesta a una solicitud para obtener una suspensión a la que se ha eliminado.</span><span class="sxs-lookup"><span data-stu-id="2f8d3-147">This is a response to a request to get a hold that has been deleted.</span></span> 
  
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
      <GetHoldOnMailboxesResponse ResponseClass="Error" 
                                  xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>The specific query-based hold is not found.</MessageText>
         <ResponseCode>ErrorMailboxHoldNotFound</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </GetHoldOnMailboxesResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="2f8d3-148">La respuesta de error SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="2f8d3-148">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="2f8d3-149">GetHoldOnMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="2f8d3-149">GetHoldOnMailboxesResponse</span></span>](getholdonmailboxesresponse.md)
    
- [<span data-ttu-id="2f8d3-150">MessageText</span><span class="sxs-lookup"><span data-stu-id="2f8d3-150">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="2f8d3-151">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="2f8d3-151">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="2f8d3-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="2f8d3-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="2f8d3-153">Para códigos de error adicionales que son genéricos para EWS y específicos de esta operación, vea [ResponseCode](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="2f8d3-153">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2f8d3-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="2f8d3-154">See also</span></span>

- [<span data-ttu-id="2f8d3-155">Operaciones de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="2f8d3-155">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="2f8d3-156">Operación GetSearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="2f8d3-156">GetSearchableMailboxes operation</span></span>](getsearchablemailboxes-operation.md)
    
- [<span data-ttu-id="2f8d3-157">Operación SearchMailboxes</span><span class="sxs-lookup"><span data-stu-id="2f8d3-157">SearchMailboxes operation</span></span>](searchmailboxes-operation.md)
    
- [<span data-ttu-id="2f8d3-158">Operación SetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="2f8d3-158">SetHoldOnMailboxes operation</span></span>](setholdonmailboxes-operation.md)
    
- [<span data-ttu-id="2f8d3-159">Operación GetDiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="2f8d3-159">GetDiscoverySearchConfiguration operation</span></span>](getdiscoverysearchconfiguration-operation.md)
    
- [<span data-ttu-id="2f8d3-160">Operación GetNonIndexableItemDetails</span><span class="sxs-lookup"><span data-stu-id="2f8d3-160">GetNonIndexableItemDetails operation</span></span>](getnonindexableitemdetails-operation.md)
    
- [<span data-ttu-id="2f8d3-161">Operación GetNonIndexableItemStatistics</span><span class="sxs-lookup"><span data-stu-id="2f8d3-161">GetNonIndexableItemStatistics operation</span></span>](getnonindexableitemstatistics-operation.md)
    

