---
title: Operación SetHoldOnMailboxes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9015a0d8-3495-461b-aa79-797d23169585
description: Busque información sobre la EWS SetHoldOnMailboxes operación.
ms.openlocfilehash: 1091ed14ceb25dfd275499b9db47ae4e41b5f1a0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837412"
---
# <a name="setholdonmailboxes-operation"></a><span data-ttu-id="dfd1e-103">Operación SetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="dfd1e-103">SetHoldOnMailboxes operation</span></span>

<span data-ttu-id="dfd1e-104">Obtenga información acerca de la operación de EWS **SetHoldOnMailboxes** .</span><span class="sxs-lookup"><span data-stu-id="dfd1e-104">Find information about the **SetHoldOnMailboxes** EWS operation.</span></span> 
  
<span data-ttu-id="dfd1e-105">La operación **SetHoldOnMailboxes** establece una directiva de retención de buzón de correo en los buzones de correo.</span><span class="sxs-lookup"><span data-stu-id="dfd1e-105">The **SetHoldOnMailboxes** operation sets a mailbox hold policy on mailboxes.</span></span> 
  
<span data-ttu-id="dfd1e-106">Esta operación se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="dfd1e-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-setholdonmailboxes-operation"></a><span data-ttu-id="dfd1e-107">Mediante la operación SetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="dfd1e-107">Using the SetHoldOnMailboxes operation</span></span>

<span data-ttu-id="dfd1e-108">La operación **SetHoldOnMailboxes** establece una suspensión de buzón de correo en uno o más buzones.</span><span class="sxs-lookup"><span data-stu-id="dfd1e-108">The **SetHoldOnMailboxes** operation sets a mailbox hold on to one or more mailboxes.</span></span> 
  
### <a name="setholdonmailboxes-operation-soap-headers"></a><span data-ttu-id="dfd1e-109">Encabezados SOAP de operación de SetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="dfd1e-109">SetHoldOnMailboxes operation SOAP headers</span></span>

<span data-ttu-id="dfd1e-110">La operación de **SetHoldOnMailboxes** puede utilizar los encabezados SOAP que se enumeran en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="dfd1e-110">The **SetHoldOnMailboxes** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="dfd1e-111">**Nombre de encabezado**</span><span class="sxs-lookup"><span data-stu-id="dfd1e-111">**Header name**</span></span>|<span data-ttu-id="dfd1e-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="dfd1e-112">**Element**</span></span>|<span data-ttu-id="dfd1e-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dfd1e-113">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="dfd1e-114">**ManagementRole**</span><span class="sxs-lookup"><span data-stu-id="dfd1e-114">**ManagementRole**</span></span> <br/> |[<span data-ttu-id="dfd1e-115">ManagementRole</span><span class="sxs-lookup"><span data-stu-id="dfd1e-115">ManagementRole</span></span>](managementrole.md) <br/> |<span data-ttu-id="dfd1e-116">Identifica las funciones de servidor que son necesarias en orden para el autor de la llamada realizar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="dfd1e-116">Identifies the server roles that are necessary in order for the caller to make the request.</span></span> <span data-ttu-id="dfd1e-117">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="dfd1e-117">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="dfd1e-118">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="dfd1e-118">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="dfd1e-119">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="dfd1e-119">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="dfd1e-120">Identifica la versión del esquema para la solicitud de la operación.</span><span class="sxs-lookup"><span data-stu-id="dfd1e-120">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="dfd1e-121">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="dfd1e-121">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="dfd1e-122">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="dfd1e-122">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="dfd1e-123">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="dfd1e-123">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="dfd1e-124">Identifica la versión del servidor que ha respondido a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="dfd1e-124">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="dfd1e-125">Este encabezado es aplicable a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="dfd1e-125">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="setholdonmailboxes-operation-request-example-apply-a-hold-on-a-mailbox"></a><span data-ttu-id="dfd1e-126">Ejemplo de solicitud de operación de SetHoldOnMailboxes: aplicar una suspensión en un buzón de correo</span><span class="sxs-lookup"><span data-stu-id="dfd1e-126">SetHoldOnMailboxes operation request example: Apply a hold on a mailbox</span></span>

<span data-ttu-id="dfd1e-127">El siguiente ejemplo de una solicitud de operación **SetHoldOnMailboxes** muestra cómo aplicar una suspensión en dos buzones.</span><span class="sxs-lookup"><span data-stu-id="dfd1e-127">The following example of a **SetHoldOnMailboxes** operation request shows how to apply a hold on two mailboxes.</span></span> <span data-ttu-id="dfd1e-128">La suspensión de buzón de correo se ha creado mediante el comando [New-MailboxSearch](http://technet.microsoft.com/es-es/library/dd298064.aspx) .</span><span class="sxs-lookup"><span data-stu-id="dfd1e-128">The mailbox hold was created by using the [New-MailboxSearch](http://technet.microsoft.com/es-es/library/dd298064.aspx) command.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:SetHoldOnMailboxes>
         <m:ActionType>Create</m:ActionType>
         <m:HoldId>HoldId2</m:HoldId>
         <m:Query>test</m:Query>
         <m:Mailboxes>
            <t:String>/o=First/ou=Exchange(DLT)/cn=Recipients/cn=1fa441ff5e4749ba43ecc0fd94c21adf-Willi</t:String>
            <t:String>/o=First/ou=Exchange(DLT)/cn=Recipients/cn=aed2346adaa34ffc9f0f339917e8de95-Micha</t:String>
         </m:Mailboxes>
         <m:Language>English</m:Language>
         <m:IncludeNonIndexableItems>false</m:IncludeNonIndexableItems>
         <m:Deduplication>true</m:Deduplication>
      </m:SetHoldOnMailboxes>
   </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="dfd1e-129">La solicitud SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="dfd1e-129">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="dfd1e-130">SetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="dfd1e-130">SetHoldOnMailboxes</span></span>](setholdonmailboxes.md)
    
- [<span data-ttu-id="dfd1e-131">ActionType (HoldActionType)</span><span class="sxs-lookup"><span data-stu-id="dfd1e-131">ActionType (HoldActionType)</span></span>](actiontype-holdactiontype.md)
    
- [<span data-ttu-id="dfd1e-132">HoldId</span><span class="sxs-lookup"><span data-stu-id="dfd1e-132">HoldId</span></span>](holdid.md)
    
- [<span data-ttu-id="dfd1e-133">Consulta</span><span class="sxs-lookup"><span data-stu-id="dfd1e-133">Query</span></span>](query.md)
    
- [<span data-ttu-id="dfd1e-134">Buzones de correo (ArrayOfStringsType)</span><span class="sxs-lookup"><span data-stu-id="dfd1e-134">Mailboxes (ArrayOfStringsType)</span></span>](mailboxes-arrayofstringstype.md)
    
- [<span data-ttu-id="dfd1e-135">String</span><span class="sxs-lookup"><span data-stu-id="dfd1e-135">String</span></span>](string.md)
    
- [<span data-ttu-id="dfd1e-136">Idioma</span><span class="sxs-lookup"><span data-stu-id="dfd1e-136">Language</span></span>](language.md)
    
- [<span data-ttu-id="dfd1e-137">IncludeNonIndexableItems</span><span class="sxs-lookup"><span data-stu-id="dfd1e-137">IncludeNonIndexableItems</span></span>](includenonindexableitems.md)
    
- [<span data-ttu-id="dfd1e-138">Desduplicación</span><span class="sxs-lookup"><span data-stu-id="dfd1e-138">Deduplication</span></span>](deduplication.md)
    
## <a name="successful-setholdonmailboxes-operation-response"></a><span data-ttu-id="dfd1e-139">Respuesta es correcta de operación SetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="dfd1e-139">Successful SetHoldOnMailboxes operation response</span></span>

<span data-ttu-id="dfd1e-140">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación de **SetHoldOnMailboxes** para poner dos buzones en suspensión.</span><span class="sxs-lookup"><span data-stu-id="dfd1e-140">The following example shows a successful response to a **SetHoldOnMailboxes** operation request to put two mailboxes on hold.</span></span> 
  
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
      <SetHoldOnMailboxesResponse ResponseClass="Success" 
                                  xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <MailboxHoldResult>
            <HoldId xmlns="http://schemas.microsoft.com/exchange/services/2006/types">HoldId2</HoldId>
            <Query xmlns="http://schemas.microsoft.com/exchange/services/2006/types">test</Query>
            <MailboxHoldStatuses xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
               <MailboxHoldStatus>
                  <Mailbox>o=First/ou=Exchange(DLT)/cn=Recipients/cn=1fa441ff5e4749ba43ecc0fd94c21adf-Willi</Mailbox>
                  <Status>Pending</Status>
                  <AdditionalInfo/>
               </MailboxHoldStatus>
               <MailboxHoldStatus>
                  <Mailbox>/o=First/ou=Exchange(DLT)/cn=Recipients/cn=aed2346adaa34ffc9f0f339917e8de95-Micha</Mailbox>
                  <Status>Pending</Status>
                  <AdditionalInfo/>
               </MailboxHoldStatus>
            </MailboxHoldStatuses>
         </MailboxHoldResult>
      </SetHoldOnMailboxesResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="dfd1e-141">La respuesta SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="dfd1e-141">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="dfd1e-142">SetHoldOnMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="dfd1e-142">SetHoldOnMailboxesResponse</span></span>](setholdonmailboxesresponse.md)
    
- [<span data-ttu-id="dfd1e-143">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="dfd1e-143">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="dfd1e-144">MailboxHoldResult</span><span class="sxs-lookup"><span data-stu-id="dfd1e-144">MailboxHoldResult</span></span>](mailboxholdresult.md)
    
- [<span data-ttu-id="dfd1e-145">HoldId</span><span class="sxs-lookup"><span data-stu-id="dfd1e-145">HoldId</span></span>](holdid.md)
    
- [<span data-ttu-id="dfd1e-146">Consulta</span><span class="sxs-lookup"><span data-stu-id="dfd1e-146">Query</span></span>](query.md)
    
- [<span data-ttu-id="dfd1e-147">MailboxHoldStatuses</span><span class="sxs-lookup"><span data-stu-id="dfd1e-147">MailboxHoldStatuses</span></span>](mailboxholdstatuses.md)
    
- [<span data-ttu-id="dfd1e-148">MailboxHoldStatus</span><span class="sxs-lookup"><span data-stu-id="dfd1e-148">MailboxHoldStatus</span></span>](mailboxholdstatus.md)
    
- [<span data-ttu-id="dfd1e-149">Buzón de correo (cadena)</span><span class="sxs-lookup"><span data-stu-id="dfd1e-149">Mailbox (string)</span></span>](mailbox-string.md)
    
- [<span data-ttu-id="dfd1e-150">Estado (HoldStatusType)</span><span class="sxs-lookup"><span data-stu-id="dfd1e-150">Status (HoldStatusType)</span></span>](status-holdstatustype.md)
    
- [<span data-ttu-id="dfd1e-151">AdditionalInfo</span><span class="sxs-lookup"><span data-stu-id="dfd1e-151">AdditionalInfo</span></span>](additionalinfo.md)
    
## <a name="setholdonmailboxes-operation-error-response"></a><span data-ttu-id="dfd1e-152">Respuesta de error de la operación de SetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="dfd1e-152">SetHoldOnMailboxes operation error response</span></span>

<span data-ttu-id="dfd1e-153">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **SetHoldOnMailboxes** .</span><span class="sxs-lookup"><span data-stu-id="dfd1e-153">The following example shows an error response to a **SetHoldOnMailboxes** operation request.</span></span> <span data-ttu-id="dfd1e-154">Esta es una respuesta a una solicitud que contiene un identificador de buzón de correo especificado incorrectamente.</span><span class="sxs-lookup"><span data-stu-id="dfd1e-154">This is a response to a request that contains an incorrectly specified mailbox identifier.</span></span> 
  
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
      <SetHoldOnMailboxesResponse ResponseClass="Error" 
                                  xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>No mailbox is specified for hold operation. If specified in the request, then it could be the object does not exist in AD or is a Distribution Group.</MessageText>
         <ResponseCode>ErrorInvalidOperation</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </SetHoldOnMailboxesResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="dfd1e-155">La respuesta de error SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="dfd1e-155">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="dfd1e-156">SetHoldOnMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="dfd1e-156">SetHoldOnMailboxesResponse</span></span>](setholdonmailboxesresponse.md)
    
- [<span data-ttu-id="dfd1e-157">MessageText</span><span class="sxs-lookup"><span data-stu-id="dfd1e-157">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="dfd1e-158">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="dfd1e-158">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="dfd1e-159">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="dfd1e-159">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="dfd1e-160">Para códigos de error adicionales que son genéricos para EWS y específicos de esta operación, vea [ResponseCode](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="dfd1e-160">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="dfd1e-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="dfd1e-161">See also</span></span>

- [<span data-ttu-id="dfd1e-162">Operaciones de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="dfd1e-162">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="dfd1e-163">Operación GetSearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="dfd1e-163">GetSearchableMailboxes operation</span></span>](getsearchablemailboxes-operation.md)
    
- [<span data-ttu-id="dfd1e-164">Operación SearchMailboxes</span><span class="sxs-lookup"><span data-stu-id="dfd1e-164">SearchMailboxes operation</span></span>](searchmailboxes-operation.md)
    
- [<span data-ttu-id="dfd1e-165">Operación GetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="dfd1e-165">GetHoldOnMailboxes operation</span></span>](getholdonmailboxes-operation.md)
    
- [<span data-ttu-id="dfd1e-166">Operación GetDiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="dfd1e-166">GetDiscoverySearchConfiguration operation</span></span>](getdiscoverysearchconfiguration-operation.md)
    
- [<span data-ttu-id="dfd1e-167">Operación GetNonIndexableItemDetails</span><span class="sxs-lookup"><span data-stu-id="dfd1e-167">GetNonIndexableItemDetails operation</span></span>](getnonindexableitemdetails-operation.md)
    
- [<span data-ttu-id="dfd1e-168">Operación GetNonIndexableItemStatistics</span><span class="sxs-lookup"><span data-stu-id="dfd1e-168">GetNonIndexableItemStatistics operation</span></span>](getnonindexableitemstatistics-operation.md)
    

