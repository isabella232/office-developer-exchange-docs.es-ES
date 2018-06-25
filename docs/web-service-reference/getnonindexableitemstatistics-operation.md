---
title: Operación GetNonIndexableItemStatistics
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ed077877-9d98-4434-b8b6-a4a905e7f7a6
description: Busque información sobre la EWS GetNonIndexableItemStatistics operación.
ms.openlocfilehash: 35c2d3321c6e1a3154c88307d0e875cd6997e7fb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764916"
---
# <a name="getnonindexableitemstatistics-operation"></a><span data-ttu-id="e0ea0-103">Operación GetNonIndexableItemStatistics</span><span class="sxs-lookup"><span data-stu-id="e0ea0-103">GetNonIndexableItemStatistics operation</span></span>

<span data-ttu-id="e0ea0-104">Obtenga información acerca de la operación de EWS **GetNonIndexableItemStatistics** .</span><span class="sxs-lookup"><span data-stu-id="e0ea0-104">Find information about the **GetNonIndexableItemStatistics** EWS operation.</span></span> 
  
<span data-ttu-id="e0ea0-105">La operación **GetNonIndexableItemStatistics** recupera el recuento de elementos que no se pueden indizar en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="e0ea0-105">The **GetNonIndexableItemStatistics** operation retrieves the count of items that cannot be indexed in a mailbox.</span></span> 
  
<span data-ttu-id="e0ea0-106">Esta operación se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e0ea0-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getnonindexableitemstatistics-operation"></a><span data-ttu-id="e0ea0-107">Mediante la operación GetNonIndexableItemStatistics</span><span class="sxs-lookup"><span data-stu-id="e0ea0-107">Using the GetNonIndexableItemStatistics operation</span></span>

<span data-ttu-id="e0ea0-108">La operación de **GetNonIndexableItemStatistics** los recuentos de los elementos del buzón que no se pueden indizar.</span><span class="sxs-lookup"><span data-stu-id="e0ea0-108">The **GetNonIndexableItemStatistics** operation counts mailbox items that cannot be indexed.</span></span> <span data-ttu-id="e0ea0-109">No se buscan los elementos que no se pueden indizar durante una búsqueda de detección.</span><span class="sxs-lookup"><span data-stu-id="e0ea0-109">Items that cannot be indexed are not searched during a discovery search.</span></span> 
  
### <a name="getnonindexableitemstatistics-operation-soap-headers"></a><span data-ttu-id="e0ea0-110">Encabezados SOAP de operación de GetNonIndexableItemStatistics</span><span class="sxs-lookup"><span data-stu-id="e0ea0-110">GetNonIndexableItemStatistics operation SOAP headers</span></span>

<span data-ttu-id="e0ea0-111">La operación de **GetNonIndexableItemStatistics** puede utilizar los encabezados SOAP que se enumeran en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="e0ea0-111">The **GetNonIndexableItemStatistics** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="e0ea0-112">**Nombre de encabezado**</span><span class="sxs-lookup"><span data-stu-id="e0ea0-112">**Header name**</span></span>|<span data-ttu-id="e0ea0-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="e0ea0-113">**Element**</span></span>|<span data-ttu-id="e0ea0-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e0ea0-114">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e0ea0-115">**ManagementRole**</span><span class="sxs-lookup"><span data-stu-id="e0ea0-115">**ManagementRole**</span></span> <br/> |[<span data-ttu-id="e0ea0-116">ManagementRole</span><span class="sxs-lookup"><span data-stu-id="e0ea0-116">ManagementRole</span></span>](managementrole.md) <br/> |<span data-ttu-id="e0ea0-117">Identifica las funciones de servidor que son necesarias en orden para el autor de la llamada realizar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e0ea0-117">Identifies the server roles that are necessary in order for the caller to make the request.</span></span> <span data-ttu-id="e0ea0-118">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="e0ea0-118">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="e0ea0-119">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="e0ea0-119">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="e0ea0-120">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="e0ea0-120">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="e0ea0-121">Identifica la versión del esquema para la solicitud de la operación.</span><span class="sxs-lookup"><span data-stu-id="e0ea0-121">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="e0ea0-122">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="e0ea0-122">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="e0ea0-123">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="e0ea0-123">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="e0ea0-124">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="e0ea0-124">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="e0ea0-125">Identifica la versión del servidor que ha respondido a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e0ea0-125">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="e0ea0-126">Este encabezado es aplicable a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="e0ea0-126">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getnonindexableitemstatistics-operation-request-example-get-the-count-of-items-that-cannot-be-indexed-in-a-mailbox"></a><span data-ttu-id="e0ea0-127">Ejemplo de solicitud de operación de GetNonIndexableItemStatistics: obtener el recuento de elementos que no se pueden indizar en un buzón de correo</span><span class="sxs-lookup"><span data-stu-id="e0ea0-127">GetNonIndexableItemStatistics operation request example: Get the count of items that cannot be indexed in a mailbox</span></span>

<span data-ttu-id="e0ea0-128">El siguiente ejemplo de una solicitud de operación **GetNonIndexableItemStatistics** muestra cómo solicitar el recuento de elementos que no se pueden indizar en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="e0ea0-128">The following example of a **GetNonIndexableItemStatistics** operation request shows how to request the count of items that cannot be indexed in a mailbox.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e0ea0-129">Todos los nombres de dominio heredado en este ejemplo se han abreviado para conservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="e0ea0-129">All legacy domain names in this example have be shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:GetNonIndexableItemStatistics>
         <m:Mailboxes>
            <t:LegacyDN>/o=First Organization/ou=Exchange Administrative Group (FYDIDLT)/cn=Recipients/cn=3518cf-Steve</t:LegacyDN>
         </m:Mailboxes>
         <m:SearchArchiveOnly>false</m:SearchArchiveOnly>
      </m:GetNonIndexableItemStatistics>
   </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="e0ea0-130">La solicitud SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="e0ea0-130">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="e0ea0-131">GetNonIndexableItemStatistics</span><span class="sxs-lookup"><span data-stu-id="e0ea0-131">GetNonIndexableItemStatistics</span></span>](getnonindexableitemstatistics.md)
    
- [<span data-ttu-id="e0ea0-132">Buzones de correo (NonEmptyArrayOfLegacyDNsType)</span><span class="sxs-lookup"><span data-stu-id="e0ea0-132">Mailboxes (NonEmptyArrayOfLegacyDNsType)</span></span>](mailboxes-nonemptyarrayoflegacydnstype.md)
    
- [<span data-ttu-id="e0ea0-133">LegacyDN</span><span class="sxs-lookup"><span data-stu-id="e0ea0-133">LegacyDN</span></span>](legacydn.md)
    
- [<span data-ttu-id="e0ea0-134">SearchArchiveOnly</span><span class="sxs-lookup"><span data-stu-id="e0ea0-134">SearchArchiveOnly</span></span>](searcharchiveonly.md)
    
## <a name="successful-getnonindexableitemstatistics-operation-response"></a><span data-ttu-id="e0ea0-135">Respuesta es correcta de operación GetNonIndexableItemStatistics</span><span class="sxs-lookup"><span data-stu-id="e0ea0-135">Successful GetNonIndexableItemStatistics operation response</span></span>

<span data-ttu-id="e0ea0-136">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación de **GetNonIndexableItemStatistics** para obtener el recuento de elementos que no se pueden indizar en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="e0ea0-136">The following example shows a successful response to a **GetNonIndexableItemStatistics** operation request to get the count of items that cannot be indexed in a mailbox.</span></span> 
  
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
      <GetNonIndexableItemStatisticsResponse ResponseClass="Success" 
                                             xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <NonIndexableItemStatistics>
            <NonIndexableItemStatistic xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
               <Mailbox>/o=First Organization/ou=Exchange Administrative Group (FYT)/cn=Recipients/cn=35181acf-Steve</Mailbox>
               <ItemCount>2</ItemCount>
            </NonIndexableItemStatistic>
         </NonIndexableItemStatistics>
      </GetNonIndexableItemStatisticsResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="e0ea0-137">La respuesta SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="e0ea0-137">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="e0ea0-138">GetNonIndexableItemStatisticsResponse</span><span class="sxs-lookup"><span data-stu-id="e0ea0-138">GetNonIndexableItemStatisticsResponse</span></span>](getnonindexableitemstatisticsresponse.md)
    
- [<span data-ttu-id="e0ea0-139">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="e0ea0-139">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="e0ea0-140">NonIndexableItemStatistics</span><span class="sxs-lookup"><span data-stu-id="e0ea0-140">NonIndexableItemStatistics</span></span>](nonindexableitemstatistics.md)
    
- [<span data-ttu-id="e0ea0-141">NonIndexableItemStatistic</span><span class="sxs-lookup"><span data-stu-id="e0ea0-141">NonIndexableItemStatistic</span></span>](nonindexableitemstatistic.md)
    
- [<span data-ttu-id="e0ea0-142">Buzón de correo (cadena)</span><span class="sxs-lookup"><span data-stu-id="e0ea0-142">Mailbox (string)</span></span>](mailbox-string.md)
    
- [<span data-ttu-id="e0ea0-143">ItemCount</span><span class="sxs-lookup"><span data-stu-id="e0ea0-143">ItemCount</span></span>](itemcount.md)
    
## <a name="getnonindexableitemstatistics-operation-error-response"></a><span data-ttu-id="e0ea0-144">Respuesta de error de la operación de GetNonIndexableItemStatistics</span><span class="sxs-lookup"><span data-stu-id="e0ea0-144">GetNonIndexableItemStatistics operation error response</span></span>

<span data-ttu-id="e0ea0-145">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **GetNonIndexableItemStatistics** .</span><span class="sxs-lookup"><span data-stu-id="e0ea0-145">The following example shows an error response to a **GetNonIndexableItemStatistics** operation request.</span></span> <span data-ttu-id="e0ea0-146">Esta es una respuesta a una solicitud para obtener el recuento de elementos que no se pueden indizar desde más de un buzón.</span><span class="sxs-lookup"><span data-stu-id="e0ea0-146">This is a response to a request to get the count of items that cannot be indexed from more than one mailbox.</span></span> 
  
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
      <GetNonIndexableItemStatisticsResponse ResponseClass="Error" 
                                             xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>Multiple mailboxes is currently not supported, only single mailbox is supported.</MessageText>
         <ResponseCode>ErrorInvalidArgument</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </GetNonIndexableItemStatisticsResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="e0ea0-147">La respuesta de error SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="e0ea0-147">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="e0ea0-148">GetNonIndexableItemStatisticsResponse</span><span class="sxs-lookup"><span data-stu-id="e0ea0-148">GetNonIndexableItemStatisticsResponse</span></span>](getnonindexableitemstatisticsresponse.md)
    
- [<span data-ttu-id="e0ea0-149">MessageText</span><span class="sxs-lookup"><span data-stu-id="e0ea0-149">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="e0ea0-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="e0ea0-150">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="e0ea0-151">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="e0ea0-151">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="e0ea0-152">Para códigos de error adicionales que son genéricos para EWS y específicos de esta operación, vea [ResponseCode](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="e0ea0-152">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e0ea0-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="e0ea0-153">See also</span></span>

- [<span data-ttu-id="e0ea0-154">Operaciones de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="e0ea0-154">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="e0ea0-155">Operación GetSearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="e0ea0-155">GetSearchableMailboxes operation</span></span>](getsearchablemailboxes-operation.md)
    
- [<span data-ttu-id="e0ea0-156">Operación SearchMailboxes</span><span class="sxs-lookup"><span data-stu-id="e0ea0-156">SearchMailboxes operation</span></span>](searchmailboxes-operation.md)
    
- [<span data-ttu-id="e0ea0-157">Operación GetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="e0ea0-157">GetHoldOnMailboxes operation</span></span>](getholdonmailboxes-operation.md)
    
- [<span data-ttu-id="e0ea0-158">Operación SetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="e0ea0-158">SetHoldOnMailboxes operation</span></span>](setholdonmailboxes-operation.md)
    
- [<span data-ttu-id="e0ea0-159">Operación GetDiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e0ea0-159">GetDiscoverySearchConfiguration operation</span></span>](getdiscoverysearchconfiguration-operation.md)
    
- [<span data-ttu-id="e0ea0-160">Operación GetNonIndexableItemDetails</span><span class="sxs-lookup"><span data-stu-id="e0ea0-160">GetNonIndexableItemDetails operation</span></span>](getnonindexableitemdetails-operation.md)
    

