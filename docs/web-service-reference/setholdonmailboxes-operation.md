---
title: Operación SetHoldOnMailboxes
manager: sethgros
ms.date: 01/24/2020
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9015a0d8-3495-461b-aa79-797d23169585
description: Buscar información sobre la operación de EWS de SetHoldOnMailboxes.
ms.openlocfilehash: 4d79ba9f616974b9415ae9eae23b8f5fdb0ab205
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44448397"
---
# <a name="setholdonmailboxes-operation"></a><span data-ttu-id="e0270-103">Operación SetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="e0270-103">SetHoldOnMailboxes operation</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e0270-104">A partir del 1 de abril de 2020, la operación SetHoldOnMailboxes ya no estará disponible en Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="e0270-104">Starting on April 1, 2020, the SetHoldOnMailboxes operation will no longer be available in Exchange Online.</span></span> <span data-ttu-id="e0270-105">Esta operación no se verá afectada en las versiones locales de Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="e0270-105">This operation won't be affected in on-premises versions of Exchange Server.</span></span> <span data-ttu-id="e0270-106">Para obtener más información, vea [jubilación de las herramientas de eDiscovery heredadas en Exchange Online](https://docs.microsoft.com/microsoft-365/compliance/legacy-ediscovery-retirement#getsearchablemailboxes-setholdonmailboxes-and-getholdonmailboxes-operations-in-the-ews-api).</span><span class="sxs-lookup"><span data-stu-id="e0270-106">For more information, see [Retirement of legacy eDiscovery tools in Exchange Online](https://docs.microsoft.com/microsoft-365/compliance/legacy-ediscovery-retirement#getsearchablemailboxes-setholdonmailboxes-and-getholdonmailboxes-operations-in-the-ews-api).</span></span>

<span data-ttu-id="e0270-107">Buscar información sobre la operación de EWS de **SetHoldOnMailboxes** .</span><span class="sxs-lookup"><span data-stu-id="e0270-107">Find information about the **SetHoldOnMailboxes** EWS operation.</span></span> 
  
<span data-ttu-id="e0270-108">La operación **SetHoldOnMailboxes** establece una directiva de retención de buzones en buzones.</span><span class="sxs-lookup"><span data-stu-id="e0270-108">The **SetHoldOnMailboxes** operation sets a mailbox hold policy on mailboxes.</span></span> 
  
<span data-ttu-id="e0270-109">Esta operación se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e0270-109">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-setholdonmailboxes-operation"></a><span data-ttu-id="e0270-110">Uso de la operación SetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="e0270-110">Using the SetHoldOnMailboxes operation</span></span>

<span data-ttu-id="e0270-111">La operación **SetHoldOnMailboxes** establece una retención de buzón en uno o más buzones.</span><span class="sxs-lookup"><span data-stu-id="e0270-111">The **SetHoldOnMailboxes** operation sets a mailbox hold on to one or more mailboxes.</span></span> 
  
### <a name="setholdonmailboxes-operation-soap-headers"></a><span data-ttu-id="e0270-112">Encabezados SOAP de operación SetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="e0270-112">SetHoldOnMailboxes operation SOAP headers</span></span>

<span data-ttu-id="e0270-113">La operación **SetHoldOnMailboxes** puede usar los encabezados SOAP que se enumeran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="e0270-113">The **SetHoldOnMailboxes** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="e0270-114">**Nombre de encabezado**</span><span class="sxs-lookup"><span data-stu-id="e0270-114">**Header name**</span></span>|<span data-ttu-id="e0270-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e0270-115">**Element**</span></span>|<span data-ttu-id="e0270-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e0270-116">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e0270-117">**ManagementRole**</span><span class="sxs-lookup"><span data-stu-id="e0270-117">**ManagementRole**</span></span> <br/> |[<span data-ttu-id="e0270-118">ManagementRole</span><span class="sxs-lookup"><span data-stu-id="e0270-118">ManagementRole</span></span>](managementrole.md) <br/> |<span data-ttu-id="e0270-119">Identifica los roles de servidor que son necesarios para que el autor de la llamada realice la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e0270-119">Identifies the server roles that are necessary in order for the caller to make the request.</span></span> <span data-ttu-id="e0270-120">Este encabezado se aplica a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="e0270-120">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="e0270-121">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="e0270-121">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="e0270-122">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="e0270-122">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="e0270-123">Identifica la versión del esquema para la solicitud de operación.</span><span class="sxs-lookup"><span data-stu-id="e0270-123">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="e0270-124">Este encabezado se aplica a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="e0270-124">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="e0270-125">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="e0270-125">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="e0270-126">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="e0270-126">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="e0270-127">Identifica la versión del servidor que respondió a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e0270-127">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="e0270-128">Este encabezado se aplica a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="e0270-128">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="setholdonmailboxes-operation-request-example-apply-a-hold-on-a-mailbox"></a><span data-ttu-id="e0270-129">Ejemplo de solicitud de operación SetHoldOnMailboxes: aplicar una retención en un buzón</span><span class="sxs-lookup"><span data-stu-id="e0270-129">SetHoldOnMailboxes operation request example: Apply a hold on a mailbox</span></span>

<span data-ttu-id="e0270-130">El siguiente ejemplo de una solicitud de operación de **SetHoldOnMailboxes** muestra cómo aplicar una retención en dos buzones.</span><span class="sxs-lookup"><span data-stu-id="e0270-130">The following example of a **SetHoldOnMailboxes** operation request shows how to apply a hold on two mailboxes.</span></span> <span data-ttu-id="e0270-131">La retención de buzones se creó con el comando [New-MailboxSearch](https://technet.microsoft.com/library/dd298064.aspx) .</span><span class="sxs-lookup"><span data-stu-id="e0270-131">The mailbox hold was created by using the [New-MailboxSearch](https://technet.microsoft.com/library/dd298064.aspx) command.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
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

<span data-ttu-id="e0270-132">El cuerpo SOAP de la solicitud contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="e0270-132">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="e0270-133">SetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="e0270-133">SetHoldOnMailboxes</span></span>](setholdonmailboxes.md)
    
- [<span data-ttu-id="e0270-134">ActionType (HoldActionType)</span><span class="sxs-lookup"><span data-stu-id="e0270-134">ActionType (HoldActionType)</span></span>](actiontype-holdactiontype.md)
    
- [<span data-ttu-id="e0270-135">HoldId</span><span class="sxs-lookup"><span data-stu-id="e0270-135">HoldId</span></span>](holdid.md)
    
- [<span data-ttu-id="e0270-136">Query</span><span class="sxs-lookup"><span data-stu-id="e0270-136">Query</span></span>](query.md)
    
- [<span data-ttu-id="e0270-137">Buzones de correo (ArrayOfStringsType)</span><span class="sxs-lookup"><span data-stu-id="e0270-137">Mailboxes (ArrayOfStringsType)</span></span>](mailboxes-arrayofstringstype.md)
    
- [<span data-ttu-id="e0270-138">String</span><span class="sxs-lookup"><span data-stu-id="e0270-138">String</span></span>](string.md)
    
- [<span data-ttu-id="e0270-139">Language</span><span class="sxs-lookup"><span data-stu-id="e0270-139">Language</span></span>](language.md)
    
- [<span data-ttu-id="e0270-140">IncludeNonIndexableItems</span><span class="sxs-lookup"><span data-stu-id="e0270-140">IncludeNonIndexableItems</span></span>](includenonindexableitems.md)
    
- [<span data-ttu-id="e0270-141">Desduplicación</span><span class="sxs-lookup"><span data-stu-id="e0270-141">Deduplication</span></span>](deduplication.md)
    
## <a name="successful-setholdonmailboxes-operation-response"></a><span data-ttu-id="e0270-142">Respuesta de operación SetHoldOnMailboxes correcta</span><span class="sxs-lookup"><span data-stu-id="e0270-142">Successful SetHoldOnMailboxes operation response</span></span>

<span data-ttu-id="e0270-143">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación de **SetHoldOnMailboxes** para poner dos buzones en retención.</span><span class="sxs-lookup"><span data-stu-id="e0270-143">The following example shows a successful response to a **SetHoldOnMailboxes** operation request to put two mailboxes on hold.</span></span> 
  
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
      <SetHoldOnMailboxesResponse ResponseClass="Success" 
                                  xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <MailboxHoldResult>
            <HoldId xmlns="https://schemas.microsoft.com/exchange/services/2006/types">HoldId2</HoldId>
            <Query xmlns="https://schemas.microsoft.com/exchange/services/2006/types">test</Query>
            <MailboxHoldStatuses xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="e0270-144">El cuerpo SOAP de respuesta contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="e0270-144">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="e0270-145">SetHoldOnMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="e0270-145">SetHoldOnMailboxesResponse</span></span>](setholdonmailboxesresponse.md)
    
- [<span data-ttu-id="e0270-146">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="e0270-146">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="e0270-147">MailboxHoldResult</span><span class="sxs-lookup"><span data-stu-id="e0270-147">MailboxHoldResult</span></span>](mailboxholdresult.md)
    
- [<span data-ttu-id="e0270-148">HoldId</span><span class="sxs-lookup"><span data-stu-id="e0270-148">HoldId</span></span>](holdid.md)
    
- [<span data-ttu-id="e0270-149">Query</span><span class="sxs-lookup"><span data-stu-id="e0270-149">Query</span></span>](query.md)
    
- [<span data-ttu-id="e0270-150">MailboxHoldStatuses</span><span class="sxs-lookup"><span data-stu-id="e0270-150">MailboxHoldStatuses</span></span>](mailboxholdstatuses.md)
    
- [<span data-ttu-id="e0270-151">MailboxHoldStatus</span><span class="sxs-lookup"><span data-stu-id="e0270-151">MailboxHoldStatus</span></span>](mailboxholdstatus.md)
    
- [<span data-ttu-id="e0270-152">Mailbox (cadena)</span><span class="sxs-lookup"><span data-stu-id="e0270-152">Mailbox (string)</span></span>](mailbox-string.md)
    
- [<span data-ttu-id="e0270-153">Estado (HoldStatusType)</span><span class="sxs-lookup"><span data-stu-id="e0270-153">Status (HoldStatusType)</span></span>](status-holdstatustype.md)
    
- [<span data-ttu-id="e0270-154">AdditionalInfo</span><span class="sxs-lookup"><span data-stu-id="e0270-154">AdditionalInfo</span></span>](additionalinfo.md)
    
## <a name="setholdonmailboxes-operation-error-response"></a><span data-ttu-id="e0270-155">Respuesta de error de operación de SetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="e0270-155">SetHoldOnMailboxes operation error response</span></span>

<span data-ttu-id="e0270-156">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **SetHoldOnMailboxes** .</span><span class="sxs-lookup"><span data-stu-id="e0270-156">The following example shows an error response to a **SetHoldOnMailboxes** operation request.</span></span> <span data-ttu-id="e0270-157">Se trata de una respuesta a una solicitud que contiene un identificador de buzón de correo especificado incorrectamente.</span><span class="sxs-lookup"><span data-stu-id="e0270-157">This is a response to a request that contains an incorrectly specified mailbox identifier.</span></span> 
  
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
      <SetHoldOnMailboxesResponse ResponseClass="Error" 
                                  xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>No mailbox is specified for hold operation. If specified in the request, then it could be the object does not exist in AD or is a Distribution Group.</MessageText>
         <ResponseCode>ErrorInvalidOperation</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </SetHoldOnMailboxesResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="e0270-158">El cuerpo SOAP de respuesta de error contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="e0270-158">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="e0270-159">SetHoldOnMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="e0270-159">SetHoldOnMailboxesResponse</span></span>](setholdonmailboxesresponse.md)
    
- [<span data-ttu-id="e0270-160">MessageText</span><span class="sxs-lookup"><span data-stu-id="e0270-160">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="e0270-161">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="e0270-161">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="e0270-162">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="e0270-162">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="e0270-163">Para obtener los códigos de error adicionales que son genéricos para EWS y específicos de esta operación, vea [ResponseCode](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="e0270-163">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e0270-164">Vea también</span><span class="sxs-lookup"><span data-stu-id="e0270-164">See also</span></span>

- [<span data-ttu-id="e0270-165">Operaciones de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="e0270-165">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="e0270-166">Operación GetSearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="e0270-166">GetSearchableMailboxes operation</span></span>](getsearchablemailboxes-operation.md)
    
- [<span data-ttu-id="e0270-167">Operación SearchMailboxes</span><span class="sxs-lookup"><span data-stu-id="e0270-167">SearchMailboxes operation</span></span>](searchmailboxes-operation.md)
    
- [<span data-ttu-id="e0270-168">Operación GetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="e0270-168">GetHoldOnMailboxes operation</span></span>](getholdonmailboxes-operation.md)
    
- [<span data-ttu-id="e0270-169">Operación GetDiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e0270-169">GetDiscoverySearchConfiguration operation</span></span>](getdiscoverysearchconfiguration-operation.md)
    
- [<span data-ttu-id="e0270-170">Operación GetNonIndexableItemDetails</span><span class="sxs-lookup"><span data-stu-id="e0270-170">GetNonIndexableItemDetails operation</span></span>](getnonindexableitemdetails-operation.md)
    
- [<span data-ttu-id="e0270-171">Operación GetNonIndexableItemStatistics</span><span class="sxs-lookup"><span data-stu-id="e0270-171">GetNonIndexableItemStatistics operation</span></span>](getnonindexableitemstatistics-operation.md)
    

