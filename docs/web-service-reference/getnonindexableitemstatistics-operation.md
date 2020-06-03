---
title: Operación GetNonIndexableItemStatistics
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ed077877-9d98-4434-b8b6-a4a905e7f7a6
description: Buscar información sobre la operación de EWS de GetNonIndexableItemStatistics.
ms.openlocfilehash: c7d49f9e0d7b4191c7403cb4d1a20e70a96c3882
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44452821"
---
# <a name="getnonindexableitemstatistics-operation"></a><span data-ttu-id="31e60-103">Operación GetNonIndexableItemStatistics</span><span class="sxs-lookup"><span data-stu-id="31e60-103">GetNonIndexableItemStatistics operation</span></span>

<span data-ttu-id="31e60-104">Buscar información sobre la operación de EWS de **GetNonIndexableItemStatistics** .</span><span class="sxs-lookup"><span data-stu-id="31e60-104">Find information about the **GetNonIndexableItemStatistics** EWS operation.</span></span> 
  
<span data-ttu-id="31e60-105">La operación **GetNonIndexableItemStatistics** recupera el recuento de elementos que no se pueden indizar en un buzón.</span><span class="sxs-lookup"><span data-stu-id="31e60-105">The **GetNonIndexableItemStatistics** operation retrieves the count of items that cannot be indexed in a mailbox.</span></span> 
  
<span data-ttu-id="31e60-106">Esta operación se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="31e60-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getnonindexableitemstatistics-operation"></a><span data-ttu-id="31e60-107">Uso de la operación GetNonIndexableItemStatistics</span><span class="sxs-lookup"><span data-stu-id="31e60-107">Using the GetNonIndexableItemStatistics operation</span></span>

<span data-ttu-id="31e60-108">La operación **GetNonIndexableItemStatistics** cuenta los elementos del buzón que no se pueden indizar.</span><span class="sxs-lookup"><span data-stu-id="31e60-108">The **GetNonIndexableItemStatistics** operation counts mailbox items that cannot be indexed.</span></span> <span data-ttu-id="31e60-109">No se busca en los elementos que no se pueden indizar durante una búsqueda de detección.</span><span class="sxs-lookup"><span data-stu-id="31e60-109">Items that cannot be indexed are not searched during a discovery search.</span></span> 
  
### <a name="getnonindexableitemstatistics-operation-soap-headers"></a><span data-ttu-id="31e60-110">Encabezados SOAP de operación GetNonIndexableItemStatistics</span><span class="sxs-lookup"><span data-stu-id="31e60-110">GetNonIndexableItemStatistics operation SOAP headers</span></span>

<span data-ttu-id="31e60-111">La operación **GetNonIndexableItemStatistics** puede usar los encabezados SOAP que se enumeran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="31e60-111">The **GetNonIndexableItemStatistics** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="31e60-112">**Nombre de encabezado**</span><span class="sxs-lookup"><span data-stu-id="31e60-112">**Header name**</span></span>|<span data-ttu-id="31e60-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="31e60-113">**Element**</span></span>|<span data-ttu-id="31e60-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="31e60-114">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="31e60-115">**ManagementRole**</span><span class="sxs-lookup"><span data-stu-id="31e60-115">**ManagementRole**</span></span> <br/> |[<span data-ttu-id="31e60-116">ManagementRole</span><span class="sxs-lookup"><span data-stu-id="31e60-116">ManagementRole</span></span>](managementrole.md) <br/> |<span data-ttu-id="31e60-117">Identifica los roles de servidor que son necesarios para que el autor de la llamada realice la solicitud.</span><span class="sxs-lookup"><span data-stu-id="31e60-117">Identifies the server roles that are necessary in order for the caller to make the request.</span></span> <span data-ttu-id="31e60-118">Este encabezado se aplica a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="31e60-118">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="31e60-119">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="31e60-119">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="31e60-120">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="31e60-120">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="31e60-121">Identifica la versión del esquema para la solicitud de operación.</span><span class="sxs-lookup"><span data-stu-id="31e60-121">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="31e60-122">Este encabezado se aplica a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="31e60-122">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="31e60-123">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="31e60-123">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="31e60-124">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="31e60-124">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="31e60-125">Identifica la versión del servidor que respondió a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="31e60-125">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="31e60-126">Este encabezado se aplica a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="31e60-126">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getnonindexableitemstatistics-operation-request-example-get-the-count-of-items-that-cannot-be-indexed-in-a-mailbox"></a><span data-ttu-id="31e60-127">Ejemplo de solicitud de operación GetNonIndexableItemStatistics: obtener el recuento de elementos que no se pueden indizar en un buzón de correo</span><span class="sxs-lookup"><span data-stu-id="31e60-127">GetNonIndexableItemStatistics operation request example: Get the count of items that cannot be indexed in a mailbox</span></span>

<span data-ttu-id="31e60-128">El siguiente ejemplo de una solicitud de operación de **GetNonIndexableItemStatistics** muestra cómo solicitar el recuento de elementos que no se pueden indizar en un buzón.</span><span class="sxs-lookup"><span data-stu-id="31e60-128">The following example of a **GetNonIndexableItemStatistics** operation request shows how to request the count of items that cannot be indexed in a mailbox.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="31e60-129">Todos los nombres de dominio heredados en este ejemplo se acortan para preservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="31e60-129">All legacy domain names in this example have be shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
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

<span data-ttu-id="31e60-130">El cuerpo SOAP de la solicitud contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="31e60-130">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="31e60-131">GetNonIndexableItemStatistics</span><span class="sxs-lookup"><span data-stu-id="31e60-131">GetNonIndexableItemStatistics</span></span>](getnonindexableitemstatistics.md)
    
- [<span data-ttu-id="31e60-132">Buzones de correo (NonEmptyArrayOfLegacyDNsType)</span><span class="sxs-lookup"><span data-stu-id="31e60-132">Mailboxes (NonEmptyArrayOfLegacyDNsType)</span></span>](mailboxes-nonemptyarrayoflegacydnstype.md)
    
- [<span data-ttu-id="31e60-133">LegacyDN</span><span class="sxs-lookup"><span data-stu-id="31e60-133">LegacyDN</span></span>](legacydn.md)
    
- [<span data-ttu-id="31e60-134">SearchArchiveOnly</span><span class="sxs-lookup"><span data-stu-id="31e60-134">SearchArchiveOnly</span></span>](searcharchiveonly.md)
    
## <a name="successful-getnonindexableitemstatistics-operation-response"></a><span data-ttu-id="31e60-135">Respuesta de operación GetNonIndexableItemStatistics correcta</span><span class="sxs-lookup"><span data-stu-id="31e60-135">Successful GetNonIndexableItemStatistics operation response</span></span>

<span data-ttu-id="31e60-136">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación **GetNonIndexableItemStatistics** para obtener el recuento de elementos que no se pueden indizar en un buzón.</span><span class="sxs-lookup"><span data-stu-id="31e60-136">The following example shows a successful response to a **GetNonIndexableItemStatistics** operation request to get the count of items that cannot be indexed in a mailbox.</span></span> 
  
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
      <GetNonIndexableItemStatisticsResponse ResponseClass="Success" 
                                             xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <NonIndexableItemStatistics>
            <NonIndexableItemStatistic xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <Mailbox>/o=First Organization/ou=Exchange Administrative Group (FYT)/cn=Recipients/cn=35181acf-Steve</Mailbox>
               <ItemCount>2</ItemCount>
            </NonIndexableItemStatistic>
         </NonIndexableItemStatistics>
      </GetNonIndexableItemStatisticsResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="31e60-137">El cuerpo SOAP de respuesta contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="31e60-137">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="31e60-138">GetNonIndexableItemStatisticsResponse</span><span class="sxs-lookup"><span data-stu-id="31e60-138">GetNonIndexableItemStatisticsResponse</span></span>](getnonindexableitemstatisticsresponse.md)
    
- [<span data-ttu-id="31e60-139">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="31e60-139">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="31e60-140">NonIndexableItemStatistics</span><span class="sxs-lookup"><span data-stu-id="31e60-140">NonIndexableItemStatistics</span></span>](nonindexableitemstatistics.md)
    
- [<span data-ttu-id="31e60-141">NonIndexableItemStatistic</span><span class="sxs-lookup"><span data-stu-id="31e60-141">NonIndexableItemStatistic</span></span>](nonindexableitemstatistic.md)
    
- [<span data-ttu-id="31e60-142">Mailbox (cadena)</span><span class="sxs-lookup"><span data-stu-id="31e60-142">Mailbox (string)</span></span>](mailbox-string.md)
    
- [<span data-ttu-id="31e60-143">ItemCount</span><span class="sxs-lookup"><span data-stu-id="31e60-143">ItemCount</span></span>](itemcount.md)
    
## <a name="getnonindexableitemstatistics-operation-error-response"></a><span data-ttu-id="31e60-144">Respuesta de error de operación de GetNonIndexableItemStatistics</span><span class="sxs-lookup"><span data-stu-id="31e60-144">GetNonIndexableItemStatistics operation error response</span></span>

<span data-ttu-id="31e60-145">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **GetNonIndexableItemStatistics** .</span><span class="sxs-lookup"><span data-stu-id="31e60-145">The following example shows an error response to a **GetNonIndexableItemStatistics** operation request.</span></span> <span data-ttu-id="31e60-146">Se trata de una respuesta a una solicitud para obtener el recuento de elementos que no se pueden indizar desde más de un buzón.</span><span class="sxs-lookup"><span data-stu-id="31e60-146">This is a response to a request to get the count of items that cannot be indexed from more than one mailbox.</span></span> 
  
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
      <GetNonIndexableItemStatisticsResponse ResponseClass="Error" 
                                             xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>Multiple mailboxes is currently not supported, only single mailbox is supported.</MessageText>
         <ResponseCode>ErrorInvalidArgument</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </GetNonIndexableItemStatisticsResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="31e60-147">El cuerpo SOAP de respuesta de error contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="31e60-147">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="31e60-148">GetNonIndexableItemStatisticsResponse</span><span class="sxs-lookup"><span data-stu-id="31e60-148">GetNonIndexableItemStatisticsResponse</span></span>](getnonindexableitemstatisticsresponse.md)
    
- [<span data-ttu-id="31e60-149">MessageText</span><span class="sxs-lookup"><span data-stu-id="31e60-149">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="31e60-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="31e60-150">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="31e60-151">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="31e60-151">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="31e60-152">Para obtener los códigos de error adicionales que son genéricos para EWS y específicos de esta operación, vea [ResponseCode](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="31e60-152">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="31e60-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="31e60-153">See also</span></span>

- [<span data-ttu-id="31e60-154">Operaciones de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="31e60-154">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="31e60-155">Operación GetSearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="31e60-155">GetSearchableMailboxes operation</span></span>](getsearchablemailboxes-operation.md)
    
- [<span data-ttu-id="31e60-156">Operación SearchMailboxes</span><span class="sxs-lookup"><span data-stu-id="31e60-156">SearchMailboxes operation</span></span>](searchmailboxes-operation.md)
    
- [<span data-ttu-id="31e60-157">Operación GetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="31e60-157">GetHoldOnMailboxes operation</span></span>](getholdonmailboxes-operation.md)
    
- [<span data-ttu-id="31e60-158">Operación SetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="31e60-158">SetHoldOnMailboxes operation</span></span>](setholdonmailboxes-operation.md)
    
- [<span data-ttu-id="31e60-159">Operación GetDiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="31e60-159">GetDiscoverySearchConfiguration operation</span></span>](getdiscoverysearchconfiguration-operation.md)
    
- [<span data-ttu-id="31e60-160">Operación GetNonIndexableItemDetails</span><span class="sxs-lookup"><span data-stu-id="31e60-160">GetNonIndexableItemDetails operation</span></span>](getnonindexableitemdetails-operation.md)
    

