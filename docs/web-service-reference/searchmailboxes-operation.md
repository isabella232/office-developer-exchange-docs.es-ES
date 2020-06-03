---
title: Operación SearchMailboxes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8a67c1d8-d021-4e68-aa62-35f7d9c2edc7
description: Buscar información sobre la operación de EWS de SearchMailboxes.
ms.openlocfilehash: 9ec7e9dd4ef17f22f236e64ca1fdbeb65e6e56fe
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456777"
---
# <a name="searchmailboxes-operation"></a><span data-ttu-id="8783e-103">Operación SearchMailboxes</span><span class="sxs-lookup"><span data-stu-id="8783e-103">SearchMailboxes operation</span></span>

> [!NOTE]
> <span data-ttu-id="8783e-104">Esta operación está en desuso y Microsoft ya no la admite.</span><span class="sxs-lookup"><span data-stu-id="8783e-104">This operation is deprecated, and no longer supported by Microsoft.</span></span>  <span data-ttu-id="8783e-105">Como reemplazo, use la operación [FindItem](finditem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="8783e-105">As a replacement, please use the [FindItem](finditem-operation.md) operation.</span></span>

<span data-ttu-id="8783e-106">Buscar información sobre la operación de EWS de **SearchMailboxes** .</span><span class="sxs-lookup"><span data-stu-id="8783e-106">Find information about the **SearchMailboxes** EWS operation.</span></span> 
  
<span data-ttu-id="8783e-107">La operación **SearchMailboxes** busca en los buzones las ocurrencias de términos en los elementos del buzón.</span><span class="sxs-lookup"><span data-stu-id="8783e-107">The **SearchMailboxes** operation searches mailboxes for occurrences of terms in mailbox items.</span></span> 
  
<span data-ttu-id="8783e-108">Esta operación se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="8783e-108">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-searchmailboxes-operation"></a><span data-ttu-id="8783e-109">Uso de la operación SearchMailboxes</span><span class="sxs-lookup"><span data-stu-id="8783e-109">Using the SearchMailboxes operation</span></span>

<span data-ttu-id="8783e-110">La operación **SearchMailboxes** puede usar muchas consultas de búsqueda simultáneas para realizar búsquedas de detección en varios buzones.</span><span class="sxs-lookup"><span data-stu-id="8783e-110">The **SearchMailboxes** operation can use many simultaneous search queries to perform discovery search on multiple mailboxes.</span></span> <span data-ttu-id="8783e-111">Los resultados pueden ser tanto información estadística sobre el número de veces que se produzcan los términos de búsqueda, como una vista previa de los elementos que contienen los términos de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="8783e-111">The results can be either statistical information about the number of times search terms occur, or a preview of the items that contain the search terms.</span></span> 
  
### <a name="searchmailboxes-operation-soap-headers"></a><span data-ttu-id="8783e-112">Encabezados SOAP de operación SearchMailboxes</span><span class="sxs-lookup"><span data-stu-id="8783e-112">SearchMailboxes operation SOAP headers</span></span>

<span data-ttu-id="8783e-113">La operación **SearchMailboxes** puede usar los encabezados SOAP que se enumeran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="8783e-113">The **SearchMailboxes** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="8783e-114">**Nombre de encabezado**</span><span class="sxs-lookup"><span data-stu-id="8783e-114">**Header name**</span></span>|<span data-ttu-id="8783e-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="8783e-115">**Element**</span></span>|<span data-ttu-id="8783e-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8783e-116">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8783e-117">**ManagementRole**</span><span class="sxs-lookup"><span data-stu-id="8783e-117">**ManagementRole**</span></span> <br/> |[<span data-ttu-id="8783e-118">ManagementRole</span><span class="sxs-lookup"><span data-stu-id="8783e-118">ManagementRole</span></span>](managementrole.md) <br/> |<span data-ttu-id="8783e-119">Identifica los roles de servidor que son necesarios para que el autor de la llamada realice la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8783e-119">Identifies the server roles that are necessary in order for the caller to make the request.</span></span> <span data-ttu-id="8783e-120">Este encabezado se aplica a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="8783e-120">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="8783e-121">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="8783e-121">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="8783e-122">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="8783e-122">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="8783e-123">Identifica la versión del esquema para la solicitud de operación.</span><span class="sxs-lookup"><span data-stu-id="8783e-123">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="8783e-124">Este encabezado se aplica a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="8783e-124">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="8783e-125">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="8783e-125">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="8783e-126">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="8783e-126">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="8783e-127">Identifica la versión del servidor que respondió a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8783e-127">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="8783e-128">Este encabezado se aplica a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="8783e-128">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="searchmailboxes-operation-request-example-search-mailboxes-for-number-of-search-term-hits"></a><span data-ttu-id="8783e-129">Ejemplo de solicitud de operación SearchMailboxes: buzones de búsqueda para el número de aciertos de términos de búsqueda</span><span class="sxs-lookup"><span data-stu-id="8783e-129">SearchMailboxes operation request example: Search mailboxes for number of search term hits</span></span>

<span data-ttu-id="8783e-130">El siguiente ejemplo de una solicitud de operación de **SearchMailboxes** muestra cómo usar dos consultas diferentes para buscar en tres buzones diferentes para obtener información estadística sobre cuántas veces aparece un término en cada buzón.</span><span class="sxs-lookup"><span data-stu-id="8783e-130">The following example of a **SearchMailboxes** operation request shows how to use two different queries to search three different mailboxes for statistical information about how many times a term appears in each mailbox.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="8783e-131">En este ejemplo, el elemento [query](query.md) se deja en blanco de forma intencionada.</span><span class="sxs-lookup"><span data-stu-id="8783e-131">In this example, the [Query](query.md) element is intentionaly left blank.</span></span> <span data-ttu-id="8783e-132">Esto muestra cómo una solicitud correcta puede contener condiciones de error en cada búsqueda de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="8783e-132">This shows how a successful request can contain error conditions on a per mailbox search basis.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
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

<span data-ttu-id="8783e-133">El cuerpo SOAP de la solicitud contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="8783e-133">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="8783e-134">SearchMailboxes</span><span class="sxs-lookup"><span data-stu-id="8783e-134">SearchMailboxes</span></span>](searchmailboxes.md)
    
- [<span data-ttu-id="8783e-135">SearchQueries</span><span class="sxs-lookup"><span data-stu-id="8783e-135">SearchQueries</span></span>](searchqueries.md)
    
- [<span data-ttu-id="8783e-136">MailboxQuery</span><span class="sxs-lookup"><span data-stu-id="8783e-136">MailboxQuery</span></span>](mailboxquery.md)
    
- [<span data-ttu-id="8783e-137">Query</span><span class="sxs-lookup"><span data-stu-id="8783e-137">Query</span></span>](query.md)
    
- [<span data-ttu-id="8783e-138">MailboxSearchScopes</span><span class="sxs-lookup"><span data-stu-id="8783e-138">MailboxSearchScopes</span></span>](mailboxsearchscopes.md)
    
- [<span data-ttu-id="8783e-139">MailboxSearchScope</span><span class="sxs-lookup"><span data-stu-id="8783e-139">MailboxSearchScope</span></span>](mailboxsearchscope.md)
    
- [<span data-ttu-id="8783e-140">Mailbox (cadena)</span><span class="sxs-lookup"><span data-stu-id="8783e-140">Mailbox (string)</span></span>](mailbox-string.md)
    
- [<span data-ttu-id="8783e-141">SearchScope</span><span class="sxs-lookup"><span data-stu-id="8783e-141">SearchScope</span></span>](searchscope.md)
    
- [<span data-ttu-id="8783e-142">ResultType</span><span class="sxs-lookup"><span data-stu-id="8783e-142">ResultType</span></span>](resulttype.md)
    
## <a name="successful-searchmailboxes-operation-response"></a><span data-ttu-id="8783e-143">Respuesta de operación SearchMailboxes correcta</span><span class="sxs-lookup"><span data-stu-id="8783e-143">Successful SearchMailboxes operation response</span></span>

<span data-ttu-id="8783e-144">En el siguiente ejemplo se muestra una respuesta correcta a una solicitud de operación de **SearchMailboxes** para obtener información sobre el número de veces que se encuentran los términos de búsqueda en los buzones de destino.</span><span class="sxs-lookup"><span data-stu-id="8783e-144">The following example shows a successful response to a **SearchMailboxes** operation request to get statistical information about the number of times search terms are found in the target mailboxes.</span></span> <span data-ttu-id="8783e-145">La última consulta contiene un elemento **query** vacío, que muestra una búsqueda de buzón de correo fallida.</span><span class="sxs-lookup"><span data-stu-id="8783e-145">The last query contains an empty **Query** element, which shows a failed mailbox search.</span></span> 
  
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
      <m:SearchMailboxesResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                 xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="8783e-146">El cuerpo SOAP de respuesta contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="8783e-146">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="8783e-147">SearchMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="8783e-147">SearchMailboxesResponse</span></span>](searchmailboxesresponse.md)
    
- [<span data-ttu-id="8783e-148">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="8783e-148">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="8783e-149">SearchMailboxesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="8783e-149">SearchMailboxesResponseMessage</span></span>](searchmailboxesresponsemessage.md)
    
- [<span data-ttu-id="8783e-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="8783e-150">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="8783e-151">SearchMailboxesResult</span><span class="sxs-lookup"><span data-stu-id="8783e-151">SearchMailboxesResult</span></span>](searchmailboxesresult.md)
    
- [<span data-ttu-id="8783e-152">SearchQueries</span><span class="sxs-lookup"><span data-stu-id="8783e-152">SearchQueries</span></span>](searchqueries.md)
    
- [<span data-ttu-id="8783e-153">MailboxQuery</span><span class="sxs-lookup"><span data-stu-id="8783e-153">MailboxQuery</span></span>](mailboxquery.md)
    
- [<span data-ttu-id="8783e-154">Query</span><span class="sxs-lookup"><span data-stu-id="8783e-154">Query</span></span>](query.md)
    
- [<span data-ttu-id="8783e-155">MailboxSearchScopes</span><span class="sxs-lookup"><span data-stu-id="8783e-155">MailboxSearchScopes</span></span>](mailboxsearchscopes.md)
    
- [<span data-ttu-id="8783e-156">MailboxSearchScope</span><span class="sxs-lookup"><span data-stu-id="8783e-156">MailboxSearchScope</span></span>](mailboxsearchscope.md)
    
- [<span data-ttu-id="8783e-157">Mailbox (cadena)</span><span class="sxs-lookup"><span data-stu-id="8783e-157">Mailbox (string)</span></span>](mailbox-string.md)
    
- [<span data-ttu-id="8783e-158">SearchScope</span><span class="sxs-lookup"><span data-stu-id="8783e-158">SearchScope</span></span>](searchscope.md)
    
- [<span data-ttu-id="8783e-159">ResultType</span><span class="sxs-lookup"><span data-stu-id="8783e-159">ResultType</span></span>](resulttype.md)
    
- [<span data-ttu-id="8783e-160">ItemCount</span><span class="sxs-lookup"><span data-stu-id="8783e-160">ItemCount</span></span>](itemcount.md)
    
- [<span data-ttu-id="8783e-161">Tamaño (largo)</span><span class="sxs-lookup"><span data-stu-id="8783e-161">Size (long)</span></span>](size-long.md)
    
- [<span data-ttu-id="8783e-162">PageItemCount</span><span class="sxs-lookup"><span data-stu-id="8783e-162">PageItemCount</span></span>](pageitemcount.md)
    
- [<span data-ttu-id="8783e-163">KeywordStats</span><span class="sxs-lookup"><span data-stu-id="8783e-163">KeywordStats</span></span>](keywordstats.md)
    
- [<span data-ttu-id="8783e-164">KeywordStat</span><span class="sxs-lookup"><span data-stu-id="8783e-164">KeywordStat</span></span>](keywordstat.md)
    
- [<span data-ttu-id="8783e-165">Palabra clave</span><span class="sxs-lookup"><span data-stu-id="8783e-165">Keyword</span></span>](keyword.md)
    
- [<span data-ttu-id="8783e-166">ItemHits</span><span class="sxs-lookup"><span data-stu-id="8783e-166">ItemHits</span></span>](itemhits.md)
    
- [<span data-ttu-id="8783e-167">FailedMailboxes</span><span class="sxs-lookup"><span data-stu-id="8783e-167">FailedMailboxes</span></span>](failedmailboxes.md)
    
- [<span data-ttu-id="8783e-168">FailedMailbox</span><span class="sxs-lookup"><span data-stu-id="8783e-168">FailedMailbox</span></span>](failedmailbox.md)
    
- [<span data-ttu-id="8783e-169">Mailbox (cadena)</span><span class="sxs-lookup"><span data-stu-id="8783e-169">Mailbox (string)</span></span>](mailbox-string.md)
    
- [<span data-ttu-id="8783e-170">ErrorCode (int)</span><span class="sxs-lookup"><span data-stu-id="8783e-170">ErrorCode (int)</span></span>](errorcode-int.md)
    
- [<span data-ttu-id="8783e-171">ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="8783e-171">ErrorMessage</span></span>](errormessage.md)
    
- [<span data-ttu-id="8783e-172">IsArchive</span><span class="sxs-lookup"><span data-stu-id="8783e-172">IsArchive</span></span>](isarchive.md)
    
## <a name="searchmailboxes-operation-error-response"></a><span data-ttu-id="8783e-173">Respuesta de error de operación de SearchMailboxes</span><span class="sxs-lookup"><span data-stu-id="8783e-173">SearchMailboxes operation error response</span></span>

<span data-ttu-id="8783e-174">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **SearchMailboxes** .</span><span class="sxs-lookup"><span data-stu-id="8783e-174">The following example shows an error response to a **SearchMailboxes** operation request.</span></span> <span data-ttu-id="8783e-175">Se trata de una respuesta a una solicitud de búsqueda en un buzón de correo cuando el identificador del buzón de correo es incorrecto.</span><span class="sxs-lookup"><span data-stu-id="8783e-175">This is a response to a request to search a mailbox when the mailbox identifier is incorrect.</span></span> 
  
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
      <m:SearchMailboxesResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                 xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="8783e-176">El cuerpo SOAP de respuesta de error contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="8783e-176">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="8783e-177">SearchMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="8783e-177">SearchMailboxesResponse</span></span>](searchmailboxesresponse.md)
    
- [<span data-ttu-id="8783e-178">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="8783e-178">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="8783e-179">SearchMailboxesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="8783e-179">SearchMailboxesResponseMessage</span></span>](searchmailboxesresponsemessage.md)
    
- [<span data-ttu-id="8783e-180">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="8783e-180">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="8783e-181">SearchMailboxesResult</span><span class="sxs-lookup"><span data-stu-id="8783e-181">SearchMailboxesResult</span></span>](searchmailboxesresult.md)
    
- [<span data-ttu-id="8783e-182">SearchQueries</span><span class="sxs-lookup"><span data-stu-id="8783e-182">SearchQueries</span></span>](searchqueries.md)
    
- [<span data-ttu-id="8783e-183">MailboxQuery</span><span class="sxs-lookup"><span data-stu-id="8783e-183">MailboxQuery</span></span>](mailboxquery.md)
    
- [<span data-ttu-id="8783e-184">Query</span><span class="sxs-lookup"><span data-stu-id="8783e-184">Query</span></span>](query.md)
    
- [<span data-ttu-id="8783e-185">MailboxSearchScopes</span><span class="sxs-lookup"><span data-stu-id="8783e-185">MailboxSearchScopes</span></span>](mailboxsearchscopes.md)
    
- [<span data-ttu-id="8783e-186">MailboxSearchScope</span><span class="sxs-lookup"><span data-stu-id="8783e-186">MailboxSearchScope</span></span>](mailboxsearchscope.md)
    
- [<span data-ttu-id="8783e-187">Mailbox (cadena)</span><span class="sxs-lookup"><span data-stu-id="8783e-187">Mailbox (string)</span></span>](mailbox-string.md)
    
- [<span data-ttu-id="8783e-188">SearchScope</span><span class="sxs-lookup"><span data-stu-id="8783e-188">SearchScope</span></span>](searchscope.md)
    
- [<span data-ttu-id="8783e-189">ResultType</span><span class="sxs-lookup"><span data-stu-id="8783e-189">ResultType</span></span>](resulttype.md)
    
- [<span data-ttu-id="8783e-190">ItemCount</span><span class="sxs-lookup"><span data-stu-id="8783e-190">ItemCount</span></span>](itemcount.md)
    
- [<span data-ttu-id="8783e-191">Tamaño (largo)</span><span class="sxs-lookup"><span data-stu-id="8783e-191">Size (long)</span></span>](size-long.md)
    
- [<span data-ttu-id="8783e-192">PageItemCount</span><span class="sxs-lookup"><span data-stu-id="8783e-192">PageItemCount</span></span>](pageitemcount.md)
    
- [<span data-ttu-id="8783e-193">PageItemSize</span><span class="sxs-lookup"><span data-stu-id="8783e-193">PageItemSize</span></span>](pageitemsize.md)
    
- [<span data-ttu-id="8783e-194">FailedMailboxes</span><span class="sxs-lookup"><span data-stu-id="8783e-194">FailedMailboxes</span></span>](failedmailboxes.md)
    
- [<span data-ttu-id="8783e-195">FailedMailbox</span><span class="sxs-lookup"><span data-stu-id="8783e-195">FailedMailbox</span></span>](failedmailbox.md)
    
- [<span data-ttu-id="8783e-196">Mailbox (cadena)</span><span class="sxs-lookup"><span data-stu-id="8783e-196">Mailbox (string)</span></span>](mailbox-string.md)
    
- [<span data-ttu-id="8783e-197">ErrorCode (int)</span><span class="sxs-lookup"><span data-stu-id="8783e-197">ErrorCode (int)</span></span>](errorcode-int.md)
    
- [<span data-ttu-id="8783e-198">ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="8783e-198">ErrorMessage</span></span>](errormessage.md)
    
- [<span data-ttu-id="8783e-199">IsArchive</span><span class="sxs-lookup"><span data-stu-id="8783e-199">IsArchive</span></span>](isarchive.md)
    
<span data-ttu-id="8783e-200">Para obtener los códigos de error adicionales que son genéricos para EWS y específicos de esta operación, vea [ResponseCode](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="8783e-200">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8783e-201">Vea también</span><span class="sxs-lookup"><span data-stu-id="8783e-201">See also</span></span>

- [<span data-ttu-id="8783e-202">Operaciones de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="8783e-202">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="8783e-203">Operación GetSearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="8783e-203">GetSearchableMailboxes operation</span></span>](getsearchablemailboxes-operation.md)
    
- [<span data-ttu-id="8783e-204">Operación SetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="8783e-204">SetHoldOnMailboxes operation</span></span>](setholdonmailboxes-operation.md)
    
- [<span data-ttu-id="8783e-205">Operación GetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="8783e-205">GetHoldOnMailboxes operation</span></span>](getholdonmailboxes-operation.md)
    
- [<span data-ttu-id="8783e-206">Operación GetDiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="8783e-206">GetDiscoverySearchConfiguration operation</span></span>](getdiscoverysearchconfiguration-operation.md)
    
- [<span data-ttu-id="8783e-207">Operación GetNonIndexableItemDetails</span><span class="sxs-lookup"><span data-stu-id="8783e-207">GetNonIndexableItemDetails operation</span></span>](getnonindexableitemdetails-operation.md)
    
- [<span data-ttu-id="8783e-208">Operación GetNonIndexableItemStatistics</span><span class="sxs-lookup"><span data-stu-id="8783e-208">GetNonIndexableItemStatistics operation</span></span>](getnonindexableitemstatistics-operation.md)
    

