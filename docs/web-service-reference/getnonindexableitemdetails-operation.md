---
title: Operación GetNonIndexableItemDetails
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9279c3ad-f7c8-4bbc-b0a7-2c78416cb39a
description: Busque información sobre la EWS GetNonIndexableItemDetails operación.
ms.openlocfilehash: 6b0c5afd54ac98f89bc6c5199300c20862c6f207
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764915"
---
# <a name="getnonindexableitemdetails-operation"></a><span data-ttu-id="bd0f8-103">Operación GetNonIndexableItemDetails</span><span class="sxs-lookup"><span data-stu-id="bd0f8-103">GetNonIndexableItemDetails operation</span></span>

<span data-ttu-id="bd0f8-104">Obtenga información acerca de la operación de EWS **GetNonIndexableItemDetails** .</span><span class="sxs-lookup"><span data-stu-id="bd0f8-104">Find information about the **GetNonIndexableItemDetails** EWS operation.</span></span> 
  
<span data-ttu-id="bd0f8-105">La operación **GetNonIndexableItemDetails** recupera los detalles acerca de los elementos que no se pueden indizar.</span><span class="sxs-lookup"><span data-stu-id="bd0f8-105">The **GetNonIndexableItemDetails** operation retrieves details about items that cannot be indexed.</span></span> <span data-ttu-id="bd0f8-106">Esto incluye, pero no se limita a, el identificador de elemento, un código de error, una descripción del error, cuando se ha intentado el elemento y obtener información adicional acerca del archivo de índice.</span><span class="sxs-lookup"><span data-stu-id="bd0f8-106">This includes, but is not limited to, the item identifier, an error code, an error description, when an attempt was made to index the item, and additional information about the file.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="bd0f8-107">Aunque el esquema indica que se puede buscar más de un buzón, en la versión inicial de Exchange 2013, el servicio sólo admite obtener detalles de elemento para los elementos de nonindexable de un solo buzón.</span><span class="sxs-lookup"><span data-stu-id="bd0f8-107">Although the schema indicates that more than one mailbox can be searched, in the initial release version of Exchange 2013, the service only supports getting item details for nonindexable items in a single mailbox.</span></span> 
  
<span data-ttu-id="bd0f8-108">Esta operación se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="bd0f8-108">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getnonindexableitemdetails-operation"></a><span data-ttu-id="bd0f8-109">Mediante la operación GetNonIndexableItemDetails</span><span class="sxs-lookup"><span data-stu-id="bd0f8-109">Using the GetNonIndexableItemDetails operation</span></span>

<span data-ttu-id="bd0f8-110">La operación **GetNonIndexableItemDetails** identifica los elementos de buzón de correo que no se pueden indizar y proporciona información acerca de por qué no se pueden indizar los elementos.</span><span class="sxs-lookup"><span data-stu-id="bd0f8-110">The **GetNonIndexableItemDetails** operation identifies mailbox items that cannot be indexed and provides information about why the items cannot be indexed.</span></span> <span data-ttu-id="bd0f8-111">No se buscan los elementos que no se pueden indizar durante una búsqueda de detección.</span><span class="sxs-lookup"><span data-stu-id="bd0f8-111">Items that cannot be indexed are not searched during a discovery search.</span></span> 
  
### <a name="getnonindexableitemdetails-operation-soap-headers"></a><span data-ttu-id="bd0f8-112">Encabezados SOAP de operación de GetNonIndexableItemDetails</span><span class="sxs-lookup"><span data-stu-id="bd0f8-112">GetNonIndexableItemDetails operation SOAP headers</span></span>

<span data-ttu-id="bd0f8-113">La operación de **GetNonIndexableItemDetails** puede utilizar los encabezados SOAP que se enumeran en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="bd0f8-113">The **GetNonIndexableItemDetails** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="bd0f8-114">**Nombre de encabezado**</span><span class="sxs-lookup"><span data-stu-id="bd0f8-114">**Header name**</span></span>|<span data-ttu-id="bd0f8-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="bd0f8-115">**Element**</span></span>|<span data-ttu-id="bd0f8-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bd0f8-116">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bd0f8-117">**ManagementRole**</span><span class="sxs-lookup"><span data-stu-id="bd0f8-117">**ManagementRole**</span></span> <br/> |[<span data-ttu-id="bd0f8-118">ManagementRole</span><span class="sxs-lookup"><span data-stu-id="bd0f8-118">ManagementRole</span></span>](managementrole.md) <br/> |<span data-ttu-id="bd0f8-119">Identifica las funciones de servidor que son necesarias en orden para el autor de la llamada realizar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bd0f8-119">Identifies the server roles that are necessary in order for the caller to make the request.</span></span> <span data-ttu-id="bd0f8-120">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="bd0f8-120">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="bd0f8-121">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="bd0f8-121">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="bd0f8-122">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="bd0f8-122">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="bd0f8-123">Identifica la versión del esquema para la solicitud de la operación.</span><span class="sxs-lookup"><span data-stu-id="bd0f8-123">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="bd0f8-124">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="bd0f8-124">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="bd0f8-125">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="bd0f8-125">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="bd0f8-126">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="bd0f8-126">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="bd0f8-127">Identifica la versión del servidor que ha respondido a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bd0f8-127">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="bd0f8-128">Este encabezado es aplicable a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="bd0f8-128">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getnonindexableitemdetails-operation-request-example-get-the-details-of-an-item-that-cannot-be-indexed"></a><span data-ttu-id="bd0f8-129">Ejemplo de solicitud de operación de GetNonIndexableItemDetails: obtener los detalles de un elemento que no se pueden indizar</span><span class="sxs-lookup"><span data-stu-id="bd0f8-129">GetNonIndexableItemDetails operation request example: Get the details of an item that cannot be indexed</span></span>

<span data-ttu-id="bd0f8-130">El siguiente ejemplo de una solicitud de operación **GetNonIndexableItemDetails** muestra cómo solicitar los detalles de los elementos que no se pueden indizar para un solo buzón.</span><span class="sxs-lookup"><span data-stu-id="bd0f8-130">The following example of a **GetNonIndexableItemDetails** operation request shows how to request the details for items that cannot be indexed for a single mailbox.</span></span> <span data-ttu-id="bd0f8-131">La búsqueda se realiza a través de ambos primaria y buzones de archivo.</span><span class="sxs-lookup"><span data-stu-id="bd0f8-131">The search is performed across both primary and archive mailboxes.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="bd0f8-132">Todos los nombres de dominio heredado en este ejemplo se han abreviado para conservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="bd0f8-132">All legacy domain names in this example have be shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:GetNonIndexableItemDetails>
         <m:Mailboxes>
            <t:LegacyDN>/o=First Organization/ou=Exchange Administrative Group (FYT)/cn=Recipients/cn=35-Steve</t:LegacyDN>
         </m:Mailboxes>
         <m:SearchArchiveOnly>false</m:SearchArchiveOnly>
      </m:GetNonIndexableItemDetails>
   </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="bd0f8-133">La solicitud SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="bd0f8-133">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="bd0f8-134">GetNonIndexableItemDetails</span><span class="sxs-lookup"><span data-stu-id="bd0f8-134">GetNonIndexableItemDetails</span></span>](getnonindexableitemdetails.md)
    
- [<span data-ttu-id="bd0f8-135">Buzones de correo (NonEmptyArrayOfLegacyDNsType)</span><span class="sxs-lookup"><span data-stu-id="bd0f8-135">Mailboxes (NonEmptyArrayOfLegacyDNsType)</span></span>](mailboxes-nonemptyarrayoflegacydnstype.md)
    
- [<span data-ttu-id="bd0f8-136">LegacyDN</span><span class="sxs-lookup"><span data-stu-id="bd0f8-136">LegacyDN</span></span>](legacydn.md)
    
- [<span data-ttu-id="bd0f8-137">SearchArchiveOnly</span><span class="sxs-lookup"><span data-stu-id="bd0f8-137">SearchArchiveOnly</span></span>](searcharchiveonly.md)
    
## <a name="successful-getnonindexableitemdetails-operation-response"></a><span data-ttu-id="bd0f8-138">Respuesta es correcta de operación GetNonIndexableItemDetails</span><span class="sxs-lookup"><span data-stu-id="bd0f8-138">Successful GetNonIndexableItemDetails operation response</span></span>

<span data-ttu-id="bd0f8-139">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación de **GetNonIndexableItemDetails** para obtener los elementos que no se pueden indizar para un solo buzón.</span><span class="sxs-lookup"><span data-stu-id="bd0f8-139">The following example shows a successful response to a **GetNonIndexableItemDetails** operation request to get items that cannot be indexed for a single mailbox.</span></span> <span data-ttu-id="bd0f8-140">El elemento en este ejemplo que no se pueden indizar es el archivo binaryfile.abc, que es un formato desconocido.</span><span class="sxs-lookup"><span data-stu-id="bd0f8-140">The item in this example that cannot be indexed is the binaryfile.abc file, which is of an unknown format.</span></span> 
  
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
      <GetNonIndexableItemDetailsResponse ResponseClass="Success" 
                                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <NonIndexableItemDetailsResult>
            <Items xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
               <NonIndexableItemDetail>
                  <ItemId Id="AQMkAGVmNDAyOQAAAY2fUAAAAA==" ChangeKey="CQAAAA=="/>
                  <ErrorCode>DocumentParserFailure</ErrorCode>
                  <ErrorDescription>The document parser encountered a processing error.</ErrorDescription>
                  <IsPartiallyIndexed>false</IsPartiallyIndexed>
                  <IsPermanentFailure>true</IsPermanentFailure>
                  <SortValue>502511175756</SortValue>
                  <AttemptCount>0</AttemptCount>
                  <LastAttemptTime>2012-11-15T01:56:11Z</LastAttemptTime>
                  <AdditionalInfo> 301002 Error parsing document 'exchange://localhost/Attachment/d987b1f4-9aa7-42b3-aa8c-9515a35dfa1a/1f3047d4-c287-41e4-910c-feb70c1a59f0/ef402830-3d33-4a0d-a4e9-d8576900060d/85b83861-0026-418f-8464-be2036696333/502511175756.0/binaryfile.abc'. Document has an undetectable format and will not be parsed.</AdditionalInfo>
               </NonIndexableItemDetail>
            </Items>
         </NonIndexableItemDetailsResult>
      </GetNonIndexableItemDetailsResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="bd0f8-141">La respuesta SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="bd0f8-141">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="bd0f8-142">GetNonIndexableItemDetailsResponse</span><span class="sxs-lookup"><span data-stu-id="bd0f8-142">GetNonIndexableItemDetailsResponse</span></span>](getnonindexableitemdetailsresponse.md)
    
- [<span data-ttu-id="bd0f8-143">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="bd0f8-143">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="bd0f8-144">NonIndexableItemDetailsResult</span><span class="sxs-lookup"><span data-stu-id="bd0f8-144">NonIndexableItemDetailsResult</span></span>](nonindexableitemdetailsresult.md)
    
- [<span data-ttu-id="bd0f8-145">NonIndexableItemDetail</span><span class="sxs-lookup"><span data-stu-id="bd0f8-145">NonIndexableItemDetail</span></span>](nonindexableitemdetail.md)
    
- [<span data-ttu-id="bd0f8-146">ItemId</span><span class="sxs-lookup"><span data-stu-id="bd0f8-146">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="bd0f8-147">ErrorCode (ItemIndexErrorType)</span><span class="sxs-lookup"><span data-stu-id="bd0f8-147">ErrorCode (ItemIndexErrorType)</span></span>](errorcode-itemindexerrortype.md)
    
- [<span data-ttu-id="bd0f8-148">ErrorDescription</span><span class="sxs-lookup"><span data-stu-id="bd0f8-148">ErrorDescription</span></span>](errordescription.md)
    
- [<span data-ttu-id="bd0f8-149">IsPartiallyIndexed</span><span class="sxs-lookup"><span data-stu-id="bd0f8-149">IsPartiallyIndexed</span></span>](ispartiallyindexed.md)
    
- [<span data-ttu-id="bd0f8-150">IsPermanentFailure</span><span class="sxs-lookup"><span data-stu-id="bd0f8-150">IsPermanentFailure</span></span>](ispermanentfailure.md)
    
- [<span data-ttu-id="bd0f8-151">SortValue</span><span class="sxs-lookup"><span data-stu-id="bd0f8-151">SortValue</span></span>](sortvalue.md)
    
- [<span data-ttu-id="bd0f8-152">AttemptCount</span><span class="sxs-lookup"><span data-stu-id="bd0f8-152">AttemptCount</span></span>](attemptcount.md)
    
- [<span data-ttu-id="bd0f8-153">LastAttemptTime</span><span class="sxs-lookup"><span data-stu-id="bd0f8-153">LastAttemptTime</span></span>](lastattempttime.md)
    
- [<span data-ttu-id="bd0f8-154">AdditionalInfo</span><span class="sxs-lookup"><span data-stu-id="bd0f8-154">AdditionalInfo</span></span>](additionalinfo.md)
    
## <a name="getnonindexableitemdetails-operation-error-response"></a><span data-ttu-id="bd0f8-155">Respuesta de error de la operación de GetNonIndexableItemDetails</span><span class="sxs-lookup"><span data-stu-id="bd0f8-155">GetNonIndexableItemDetails operation error response</span></span>

<span data-ttu-id="bd0f8-156">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **GetNonIndexableItemDetails** .</span><span class="sxs-lookup"><span data-stu-id="bd0f8-156">The following example shows an error response to a **GetNonIndexableItemDetails** operation request.</span></span> <span data-ttu-id="bd0f8-157">Esta es una respuesta a una solicitud para obtener detalles de elemento para los elementos que no se pueden indizar desde más de un buzón.</span><span class="sxs-lookup"><span data-stu-id="bd0f8-157">This is a response to a request to get item details for items that cannot be indexed from more than one mailbox.</span></span> 
  
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
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetNonIndexableItemDetailsResponse ResponseClass="Error" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>Multiple mailboxes is currently not supported, only single mailbox is supported.</MessageText>
         <ResponseCode>ErrorInvalidArgument</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </GetNonIndexableItemDetailsResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="bd0f8-158">La respuesta de error SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="bd0f8-158">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="bd0f8-159">GetNonIndexableItemDetailsResponse</span><span class="sxs-lookup"><span data-stu-id="bd0f8-159">GetNonIndexableItemDetailsResponse</span></span>](getnonindexableitemdetailsresponse.md)
    
- [<span data-ttu-id="bd0f8-160">MessageText</span><span class="sxs-lookup"><span data-stu-id="bd0f8-160">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="bd0f8-161">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="bd0f8-161">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="bd0f8-162">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="bd0f8-162">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="bd0f8-163">Para códigos de error adicionales que son genéricos para EWS y específicos de esta operación, vea [ResponseCode](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="bd0f8-163">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bd0f8-164">Ver también</span><span class="sxs-lookup"><span data-stu-id="bd0f8-164">See also</span></span>

- [<span data-ttu-id="bd0f8-165">Operaciones de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="bd0f8-165">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="bd0f8-166">Operación GetSearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="bd0f8-166">GetSearchableMailboxes operation</span></span>](getsearchablemailboxes-operation.md)
    
- [<span data-ttu-id="bd0f8-167">Operación SearchMailboxes</span><span class="sxs-lookup"><span data-stu-id="bd0f8-167">SearchMailboxes operation</span></span>](searchmailboxes-operation.md)
    
- [<span data-ttu-id="bd0f8-168">Operación GetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="bd0f8-168">GetHoldOnMailboxes operation</span></span>](getholdonmailboxes-operation.md)
    
- [<span data-ttu-id="bd0f8-169">Operación SetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="bd0f8-169">SetHoldOnMailboxes operation</span></span>](setholdonmailboxes-operation.md)
    
- [<span data-ttu-id="bd0f8-170">Operación GetDiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="bd0f8-170">GetDiscoverySearchConfiguration operation</span></span>](getdiscoverysearchconfiguration-operation.md)
    
- [<span data-ttu-id="bd0f8-171">Operación GetNonIndexableItemStatistics</span><span class="sxs-lookup"><span data-stu-id="bd0f8-171">GetNonIndexableItemStatistics operation</span></span>](getnonindexableitemstatistics-operation.md)
    

