---
title: Operación SearchMailboxes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8a67c1d8-d021-4e68-aa62-35f7d9c2edc7
description: Busque información sobre la EWS SearchMailboxes operación.
ms.openlocfilehash: 141ea466a24f3cb400a8e0b63e2162c1eae5d7f8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837296"
---
# <a name="searchmailboxes-operation"></a><span data-ttu-id="f8b1a-103">Operación SearchMailboxes</span><span class="sxs-lookup"><span data-stu-id="f8b1a-103">SearchMailboxes operation</span></span>

<span data-ttu-id="f8b1a-104">Obtenga información acerca de la operación de EWS **SearchMailboxes** .</span><span class="sxs-lookup"><span data-stu-id="f8b1a-104">Find information about the **SearchMailboxes** EWS operation.</span></span> 
  
<span data-ttu-id="f8b1a-105">La operación **SearchMailboxes** busca en los buzones de correo para las apariciones de términos en los elementos del buzón.</span><span class="sxs-lookup"><span data-stu-id="f8b1a-105">The **SearchMailboxes** operation searches mailboxes for occurrences of terms in mailbox items.</span></span> 
  
<span data-ttu-id="f8b1a-106">Esta operación se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f8b1a-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-searchmailboxes-operation"></a><span data-ttu-id="f8b1a-107">Mediante la operación SearchMailboxes</span><span class="sxs-lookup"><span data-stu-id="f8b1a-107">Using the SearchMailboxes operation</span></span>

<span data-ttu-id="f8b1a-108">La operación de **SearchMailboxes** puede utilizar muchas de las consultas de búsqueda simultáneas para realizar la búsqueda de detección en varios buzones de correo.</span><span class="sxs-lookup"><span data-stu-id="f8b1a-108">The **SearchMailboxes** operation can use many simultaneous search queries to perform discovery search on multiple mailboxes.</span></span> <span data-ttu-id="f8b1a-109">Los resultados pueden ser cualquier información estadística sobre el número de veces que se producen los términos de búsqueda o una vista previa de los elementos que contienen los términos de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="f8b1a-109">The results can be either statistical information about the number of times search terms occur, or a preview of the items that contain the search terms.</span></span> 
  
### <a name="searchmailboxes-operation-soap-headers"></a><span data-ttu-id="f8b1a-110">Encabezados SOAP de operación de SearchMailboxes</span><span class="sxs-lookup"><span data-stu-id="f8b1a-110">SearchMailboxes operation SOAP headers</span></span>

<span data-ttu-id="f8b1a-111">La operación de **SearchMailboxes** puede utilizar los encabezados SOAP que se enumeran en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="f8b1a-111">The **SearchMailboxes** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="f8b1a-112">**Nombre de encabezado**</span><span class="sxs-lookup"><span data-stu-id="f8b1a-112">**Header name**</span></span>|<span data-ttu-id="f8b1a-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="f8b1a-113">**Element**</span></span>|<span data-ttu-id="f8b1a-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f8b1a-114">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f8b1a-115">**ManagementRole**</span><span class="sxs-lookup"><span data-stu-id="f8b1a-115">**ManagementRole**</span></span> <br/> |[<span data-ttu-id="f8b1a-116">ManagementRole</span><span class="sxs-lookup"><span data-stu-id="f8b1a-116">ManagementRole</span></span>](managementrole.md) <br/> |<span data-ttu-id="f8b1a-117">Identifica las funciones de servidor que son necesarias en orden para el autor de la llamada realizar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f8b1a-117">Identifies the server roles that are necessary in order for the caller to make the request.</span></span> <span data-ttu-id="f8b1a-118">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="f8b1a-118">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="f8b1a-119">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="f8b1a-119">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="f8b1a-120">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="f8b1a-120">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="f8b1a-121">Identifica la versión del esquema para la solicitud de la operación.</span><span class="sxs-lookup"><span data-stu-id="f8b1a-121">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="f8b1a-122">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="f8b1a-122">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="f8b1a-123">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="f8b1a-123">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="f8b1a-124">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="f8b1a-124">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="f8b1a-125">Identifica la versión del servidor que ha respondido a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f8b1a-125">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="f8b1a-126">Este encabezado es aplicable a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="f8b1a-126">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="searchmailboxes-operation-request-example-search-mailboxes-for-number-of-search-term-hits"></a><span data-ttu-id="f8b1a-127">Ejemplo de solicitud de operación de SearchMailboxes: búsqueda de buzones de correo para el número de visitas de términos de búsqueda</span><span class="sxs-lookup"><span data-stu-id="f8b1a-127">SearchMailboxes operation request example: Search mailboxes for number of search term hits</span></span>

<span data-ttu-id="f8b1a-128">El siguiente ejemplo de una solicitud de operación **SearchMailboxes** muestra cómo usar las distintas dos consultas para buscar tres buzones diferentes para la información estadística sobre cuántas veces aparece un término en cada buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="f8b1a-128">The following example of a **SearchMailboxes** operation request shows how to use two different queries to search three different mailboxes for statistical information about how many times a term appears in each mailbox.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f8b1a-129">En este ejemplo, el elemento de [consulta](query.md) es intentionaly dejada en blanco.</span><span class="sxs-lookup"><span data-stu-id="f8b1a-129">In this example, the [Query](query.md) element is intentionaly left blank.</span></span> <span data-ttu-id="f8b1a-130">Se muestra cómo una solicitud correcta puede contener las condiciones de error en una base de búsqueda de buzón de correo por.</span><span class="sxs-lookup"><span data-stu-id="f8b1a-130">This shows how a successful request can contain error conditions on a per mailbox search basis.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:SearchMailboxes>
         <m:SearchQueries>
            <t:MailboxQuery>
               <t:Query>Test Item</t:Query>
               <t:MailboxSearchScopes>
                  <t:MailboxSearchScope>
                     <t:Mailbox>/o=First Organization/ou=Exchange Administrative Group (FYDLT)/cn=Recipients/cn=12311a742f0e47e392c8201a60d13ecf-Steve</t:Mailbox>
                     <t:SearchScope>All</t:SearchScope>
                  </t:MailboxSearchScope>
                  <t:MailboxSearchScope>
                     <t:Mailbox>/o=First Organization/ou=Exchange Administrative Group (FYDLT)/cn=Recipients/cn=f00c9f70539844beb52341d8f40c572e-Antho</t:Mailbox>
                     <t:SearchScope>PrimaryOnly</t:SearchScope>
                  </t:MailboxSearchScope>
               </t:MailboxSearchScopes>
            </t:MailboxQuery>
            <t:MailboxQuery>
               <t:Query></t:Query>
               <t:MailboxSearchScopes>
                  <t:MailboxSearchScope>
                     <t:Mailbox>/o=First Organization/ou=Exchange Administrative Group (FYDLT)/cn=Recipients/cn=accba4fd5ddf12214a0e82ce1645f4e-Danie</t:Mailbox>
                     <t:SearchScope>ArchiveOnly</t:SearchScope>
                  </t:MailboxSearchScope>
               </t:MailboxSearchScopes>
            </t:MailboxQuery>
         </m:SearchQueries>
         <m:ResultType>StatisticsOnly</m:ResultType>
      </m:SearchMailboxes>
   </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="f8b1a-131">La solicitud SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="f8b1a-131">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="f8b1a-132">SearchMailboxes</span><span class="sxs-lookup"><span data-stu-id="f8b1a-132">SearchMailboxes</span></span>](searchmailboxes.md)
    
- [<span data-ttu-id="f8b1a-133">SearchQueries</span><span class="sxs-lookup"><span data-stu-id="f8b1a-133">SearchQueries</span></span>](searchqueries.md)
    
- [<span data-ttu-id="f8b1a-134">MailboxQuery</span><span class="sxs-lookup"><span data-stu-id="f8b1a-134">MailboxQuery</span></span>](mailboxquery.md)
    
- [<span data-ttu-id="f8b1a-135">Consulta</span><span class="sxs-lookup"><span data-stu-id="f8b1a-135">Query</span></span>](query.md)
    
- [<span data-ttu-id="f8b1a-136">MailboxSearchScopes</span><span class="sxs-lookup"><span data-stu-id="f8b1a-136">MailboxSearchScopes</span></span>](mailboxsearchscopes.md)
    
- [<span data-ttu-id="f8b1a-137">MailboxSearchScope</span><span class="sxs-lookup"><span data-stu-id="f8b1a-137">MailboxSearchScope</span></span>](mailboxsearchscope.md)
    
- [<span data-ttu-id="f8b1a-138">Buzón de correo (cadena)</span><span class="sxs-lookup"><span data-stu-id="f8b1a-138">Mailbox (string)</span></span>](mailbox-string.md)
    
- [<span data-ttu-id="f8b1a-139">SearchScope</span><span class="sxs-lookup"><span data-stu-id="f8b1a-139">SearchScope</span></span>](searchscope.md)
    
- [<span data-ttu-id="f8b1a-140">ResultType</span><span class="sxs-lookup"><span data-stu-id="f8b1a-140">ResultType</span></span>](resulttype.md)
    
## <a name="successful-searchmailboxes-operation-response"></a><span data-ttu-id="f8b1a-141">Respuesta es correcta de operación SearchMailboxes</span><span class="sxs-lookup"><span data-stu-id="f8b1a-141">Successful SearchMailboxes operation response</span></span>

<span data-ttu-id="f8b1a-142">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación de **SearchMailboxes** para obtener información estadística sobre el número de veces que se encuentran los términos de búsqueda en los buzones de correo de destino.</span><span class="sxs-lookup"><span data-stu-id="f8b1a-142">The following example shows a successful response to a **SearchMailboxes** operation request to get statistical information about the number of times search terms are found in the target mailboxes.</span></span> <span data-ttu-id="f8b1a-143">La última consulta contiene un elemento vacío de **consulta** , que muestra una búsqueda de buzón de correo con errores.</span><span class="sxs-lookup"><span data-stu-id="f8b1a-143">The last query contains an empty **Query** element, which shows a failed mailbox search.</span></span> 
  
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
      <m:SearchMailboxesResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                                 xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
         <m:ResponseMessages>
            <m:SearchMailboxesResponseMessage ResponseClass="Success">
               <m:ResponseCode>NoError</m:ResponseCode>
               <m:SearchMailboxesResult>
                  <t:SearchQueries>
                     <t:MailboxQuery>
                        <t:Query>Test Item</t:Query>
                        <t:MailboxSearchScopes>
                           <t:MailboxSearchScope>
                              <t:Mailbox>/o=First Organization/ou=Exchange Administrative Group (FYPDLT)/cn=Recipients/cn=35181a94327e392c8201a60d13ecf-Steve</t:Mailbox>
                              <t:SearchScope>All</t:SearchScope>
                           </t:MailboxSearchScope>
                           <t:MailboxSearchScope>
                              <t:Mailbox>/o=First Organization/ou=Exchange Administrative Group (FYPDLT)/cn=Recipients/cn=f00c9f789572-beb04001d8f40c572e-Antho</t:Mailbox>
                              <t:SearchScope>PrimaryOnly</t:SearchScope>
                           </t:MailboxSearchScope>
                        </t:MailboxSearchScopes>
                     </t:MailboxQuery>
                  </t:SearchQueries>
                  <t:ResultType>StatisticsOnly</t:ResultType>
                  <t:ItemCount>2</t:ItemCount>
                  <t:Size>20206</t:Size>
                  <t:PageItemCount>0</t:PageItemCount>
                  <t:PageItemSize>0</t:PageItemSize>
                  <t:KeywordStats>
                     <t:KeywordStat>
                        <t:Keyword>Test Item</t:Keyword>
                        <t:ItemHits>2</t:ItemHits>
                        <t:Size>20206</t:Size>
                     </t:KeywordStat>
                  </t:KeywordStats>
                  <t:FailedMailboxes>
                     <t:FailedMailbox>
                        <t:Mailbox>/o=First Organization/ou=Exchange Administrative Group (FYPDLT)/cn=Recipients/cn=accba4as3df234234a0e82ce1645f4e-Danie</t:Mailbox>
                        <t:ErrorCode>0</t:ErrorCode>
                        <t:ErrorMessage>The search query can't be empty.</t:ErrorMessage>
                        <t:IsArchive>true</t:IsArchive>
                     </t:FailedMailbox>
                  </t:FailedMailboxes>
               </m:SearchMailboxesResult>
            </m:SearchMailboxesResponseMessage>
         </m:ResponseMessages>
      </m:SearchMailboxesResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="f8b1a-144">La respuesta SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="f8b1a-144">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="f8b1a-145">SearchMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="f8b1a-145">SearchMailboxesResponse</span></span>](searchmailboxesresponse.md)
    
- [<span data-ttu-id="f8b1a-146">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="f8b1a-146">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="f8b1a-147">SearchMailboxesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="f8b1a-147">SearchMailboxesResponseMessage</span></span>](searchmailboxesresponsemessage.md)
    
- [<span data-ttu-id="f8b1a-148">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="f8b1a-148">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="f8b1a-149">SearchMailboxesResult</span><span class="sxs-lookup"><span data-stu-id="f8b1a-149">SearchMailboxesResult</span></span>](searchmailboxesresult.md)
    
- [<span data-ttu-id="f8b1a-150">SearchQueries</span><span class="sxs-lookup"><span data-stu-id="f8b1a-150">SearchQueries</span></span>](searchqueries.md)
    
- [<span data-ttu-id="f8b1a-151">MailboxQuery</span><span class="sxs-lookup"><span data-stu-id="f8b1a-151">MailboxQuery</span></span>](mailboxquery.md)
    
- [<span data-ttu-id="f8b1a-152">Consulta</span><span class="sxs-lookup"><span data-stu-id="f8b1a-152">Query</span></span>](query.md)
    
- [<span data-ttu-id="f8b1a-153">MailboxSearchScopes</span><span class="sxs-lookup"><span data-stu-id="f8b1a-153">MailboxSearchScopes</span></span>](mailboxsearchscopes.md)
    
- [<span data-ttu-id="f8b1a-154">MailboxSearchScope</span><span class="sxs-lookup"><span data-stu-id="f8b1a-154">MailboxSearchScope</span></span>](mailboxsearchscope.md)
    
- [<span data-ttu-id="f8b1a-155">Buzón de correo (cadena)</span><span class="sxs-lookup"><span data-stu-id="f8b1a-155">Mailbox (string)</span></span>](mailbox-string.md)
    
- [<span data-ttu-id="f8b1a-156">SearchScope</span><span class="sxs-lookup"><span data-stu-id="f8b1a-156">SearchScope</span></span>](searchscope.md)
    
- [<span data-ttu-id="f8b1a-157">ResultType</span><span class="sxs-lookup"><span data-stu-id="f8b1a-157">ResultType</span></span>](resulttype.md)
    
- [<span data-ttu-id="f8b1a-158">ItemCount</span><span class="sxs-lookup"><span data-stu-id="f8b1a-158">ItemCount</span></span>](itemcount.md)
    
- [<span data-ttu-id="f8b1a-159">Tamaño (long)</span><span class="sxs-lookup"><span data-stu-id="f8b1a-159">Size (long)</span></span>](size-long.md)
    
- [<span data-ttu-id="f8b1a-160">PageItemCount</span><span class="sxs-lookup"><span data-stu-id="f8b1a-160">PageItemCount</span></span>](pageitemcount.md)
    
- [<span data-ttu-id="f8b1a-161">KeywordStats</span><span class="sxs-lookup"><span data-stu-id="f8b1a-161">KeywordStats</span></span>](keywordstats.md)
    
- [<span data-ttu-id="f8b1a-162">KeywordStat</span><span class="sxs-lookup"><span data-stu-id="f8b1a-162">KeywordStat</span></span>](keywordstat.md)
    
- [<span data-ttu-id="f8b1a-163">Palabra clave</span><span class="sxs-lookup"><span data-stu-id="f8b1a-163">Keyword</span></span>](keyword.md)
    
- [<span data-ttu-id="f8b1a-164">ItemHits</span><span class="sxs-lookup"><span data-stu-id="f8b1a-164">ItemHits</span></span>](itemhits.md)
    
- [<span data-ttu-id="f8b1a-165">FailedMailboxes</span><span class="sxs-lookup"><span data-stu-id="f8b1a-165">FailedMailboxes</span></span>](failedmailboxes.md)
    
- [<span data-ttu-id="f8b1a-166">FailedMailbox</span><span class="sxs-lookup"><span data-stu-id="f8b1a-166">FailedMailbox</span></span>](failedmailbox.md)
    
- [<span data-ttu-id="f8b1a-167">Buzón de correo (cadena)</span><span class="sxs-lookup"><span data-stu-id="f8b1a-167">Mailbox (string)</span></span>](mailbox-string.md)
    
- [<span data-ttu-id="f8b1a-168">ErrorCode (int)</span><span class="sxs-lookup"><span data-stu-id="f8b1a-168">ErrorCode (int)</span></span>](errorcode-int.md)
    
- [<span data-ttu-id="f8b1a-169">ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="f8b1a-169">ErrorMessage</span></span>](errormessage.md)
    
- [<span data-ttu-id="f8b1a-170">IsArchive</span><span class="sxs-lookup"><span data-stu-id="f8b1a-170">IsArchive</span></span>](isarchive.md)
    
## <a name="searchmailboxes-operation-error-response"></a><span data-ttu-id="f8b1a-171">Respuesta de error de la operación de SearchMailboxes</span><span class="sxs-lookup"><span data-stu-id="f8b1a-171">SearchMailboxes operation error response</span></span>

<span data-ttu-id="f8b1a-172">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **SearchMailboxes** .</span><span class="sxs-lookup"><span data-stu-id="f8b1a-172">The following example shows an error response to a **SearchMailboxes** operation request.</span></span> <span data-ttu-id="f8b1a-173">Esta es una respuesta a una solicitud para buscar un buzón de correo cuando el identificador de buzón de correo es incorrecto.</span><span class="sxs-lookup"><span data-stu-id="f8b1a-173">This is a response to a request to search a mailbox when the mailbox identifier is incorrect.</span></span> 
  
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
      <m:SearchMailboxesResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                                 xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
         <m:ResponseMessages>
            <m:SearchMailboxesResponseMessage ResponseClass="Error">
               <m:MessageText>No mailbox is specified for search operation. If specified in the request, 
               then it could be due to permission issue.</m:MessageText>
               <m:ResponseCode>ErrorInvalidOperation</m:ResponseCode>
               <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
               <m:SearchMailboxesResult>
                  <t:SearchQueries>
                     <t:MailboxQuery>
                        <t:Query>subject:Test Item</t:Query>
                        <t:MailboxSearchScopes>
                           <t:MailboxSearchScope>
                              <t:Mailbox>sbrown@contoso.com</t:Mailbox>
                              <t:SearchScope>All</t:SearchScope>
                           </t:MailboxSearchScope>
                        </t:MailboxSearchScopes>
                     </t:MailboxQuery>
                  </t:SearchQueries>
                  <t:ResultType>StatisticsOnly</t:ResultType>
                  <t:ItemCount>0</t:ItemCount>
                  <t:Size>0</t:Size>
                  <t:PageItemCount>0</t:PageItemCount>
                  <t:PageItemSize>0</t:PageItemSize>
                  <t:FailedMailboxes>
                     <t:FailedMailbox>
                        <t:Mailbox>sbrown@contoso.com</t:Mailbox>
                        <t:ErrorCode>0</t:ErrorCode>
                        <t:ErrorMessage>No mailbox is specified for search operation. If specified in the request, 
                        then it could be due to permission issue.</t:ErrorMessage>
                        <t:IsArchive>false</t:IsArchive>
                     </t:FailedMailbox>
                  </t:FailedMailboxes>
               </m:SearchMailboxesResult>
            </m:SearchMailboxesResponseMessage>
         </m:ResponseMessages>
      </m:SearchMailboxesResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="f8b1a-174">La respuesta de error SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="f8b1a-174">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="f8b1a-175">SearchMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="f8b1a-175">SearchMailboxesResponse</span></span>](searchmailboxesresponse.md)
    
- [<span data-ttu-id="f8b1a-176">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="f8b1a-176">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="f8b1a-177">SearchMailboxesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="f8b1a-177">SearchMailboxesResponseMessage</span></span>](searchmailboxesresponsemessage.md)
    
- [<span data-ttu-id="f8b1a-178">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="f8b1a-178">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="f8b1a-179">SearchMailboxesResult</span><span class="sxs-lookup"><span data-stu-id="f8b1a-179">SearchMailboxesResult</span></span>](searchmailboxesresult.md)
    
- [<span data-ttu-id="f8b1a-180">SearchQueries</span><span class="sxs-lookup"><span data-stu-id="f8b1a-180">SearchQueries</span></span>](searchqueries.md)
    
- [<span data-ttu-id="f8b1a-181">MailboxQuery</span><span class="sxs-lookup"><span data-stu-id="f8b1a-181">MailboxQuery</span></span>](mailboxquery.md)
    
- [<span data-ttu-id="f8b1a-182">Consulta</span><span class="sxs-lookup"><span data-stu-id="f8b1a-182">Query</span></span>](query.md)
    
- [<span data-ttu-id="f8b1a-183">MailboxSearchScopes</span><span class="sxs-lookup"><span data-stu-id="f8b1a-183">MailboxSearchScopes</span></span>](mailboxsearchscopes.md)
    
- [<span data-ttu-id="f8b1a-184">MailboxSearchScope</span><span class="sxs-lookup"><span data-stu-id="f8b1a-184">MailboxSearchScope</span></span>](mailboxsearchscope.md)
    
- [<span data-ttu-id="f8b1a-185">Buzón de correo (cadena)</span><span class="sxs-lookup"><span data-stu-id="f8b1a-185">Mailbox (string)</span></span>](mailbox-string.md)
    
- [<span data-ttu-id="f8b1a-186">SearchScope</span><span class="sxs-lookup"><span data-stu-id="f8b1a-186">SearchScope</span></span>](searchscope.md)
    
- [<span data-ttu-id="f8b1a-187">ResultType</span><span class="sxs-lookup"><span data-stu-id="f8b1a-187">ResultType</span></span>](resulttype.md)
    
- [<span data-ttu-id="f8b1a-188">ItemCount</span><span class="sxs-lookup"><span data-stu-id="f8b1a-188">ItemCount</span></span>](itemcount.md)
    
- [<span data-ttu-id="f8b1a-189">Tamaño (long)</span><span class="sxs-lookup"><span data-stu-id="f8b1a-189">Size (long)</span></span>](size-long.md)
    
- [<span data-ttu-id="f8b1a-190">PageItemCount</span><span class="sxs-lookup"><span data-stu-id="f8b1a-190">PageItemCount</span></span>](pageitemcount.md)
    
- [<span data-ttu-id="f8b1a-191">PageItemSize</span><span class="sxs-lookup"><span data-stu-id="f8b1a-191">PageItemSize</span></span>](pageitemsize.md)
    
- [<span data-ttu-id="f8b1a-192">FailedMailboxes</span><span class="sxs-lookup"><span data-stu-id="f8b1a-192">FailedMailboxes</span></span>](failedmailboxes.md)
    
- [<span data-ttu-id="f8b1a-193">FailedMailbox</span><span class="sxs-lookup"><span data-stu-id="f8b1a-193">FailedMailbox</span></span>](failedmailbox.md)
    
- [<span data-ttu-id="f8b1a-194">Buzón de correo (cadena)</span><span class="sxs-lookup"><span data-stu-id="f8b1a-194">Mailbox (string)</span></span>](mailbox-string.md)
    
- [<span data-ttu-id="f8b1a-195">ErrorCode (int)</span><span class="sxs-lookup"><span data-stu-id="f8b1a-195">ErrorCode (int)</span></span>](errorcode-int.md)
    
- [<span data-ttu-id="f8b1a-196">ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="f8b1a-196">ErrorMessage</span></span>](errormessage.md)
    
- [<span data-ttu-id="f8b1a-197">IsArchive</span><span class="sxs-lookup"><span data-stu-id="f8b1a-197">IsArchive</span></span>](isarchive.md)
    
<span data-ttu-id="f8b1a-198">Para códigos de error adicionales que son genéricos para EWS y específicos de esta operación, vea [ResponseCode](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="f8b1a-198">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f8b1a-199">Ver también</span><span class="sxs-lookup"><span data-stu-id="f8b1a-199">See also</span></span>

- [<span data-ttu-id="f8b1a-200">Operaciones de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="f8b1a-200">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="f8b1a-201">Operación GetSearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="f8b1a-201">GetSearchableMailboxes operation</span></span>](getsearchablemailboxes-operation.md)
    
- [<span data-ttu-id="f8b1a-202">Operación SetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="f8b1a-202">SetHoldOnMailboxes operation</span></span>](setholdonmailboxes-operation.md)
    
- [<span data-ttu-id="f8b1a-203">Operación GetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="f8b1a-203">GetHoldOnMailboxes operation</span></span>](getholdonmailboxes-operation.md)
    
- [<span data-ttu-id="f8b1a-204">Operación GetDiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="f8b1a-204">GetDiscoverySearchConfiguration operation</span></span>](getdiscoverysearchconfiguration-operation.md)
    
- [<span data-ttu-id="f8b1a-205">Operación GetNonIndexableItemDetails</span><span class="sxs-lookup"><span data-stu-id="f8b1a-205">GetNonIndexableItemDetails operation</span></span>](getnonindexableitemdetails-operation.md)
    
- [<span data-ttu-id="f8b1a-206">Operación GetNonIndexableItemStatistics</span><span class="sxs-lookup"><span data-stu-id="f8b1a-206">GetNonIndexableItemStatistics operation</span></span>](getnonindexableitemstatistics-operation.md)
    

