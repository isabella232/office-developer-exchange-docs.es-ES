---
title: Operación AddEntityFeedback
manager: luken
ms.date: 4/18/2016
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 00e40197-5794-4268-b937-bd65aa044890
description: La operación AddEntityFeedback devuelve información de error correspondiente a los problemas del servidor.
ms.openlocfilehash: b695806f543827d78aea139ffcbd7e4af58b9fef
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763401"
---
# <a name="addentityfeedback-operation"></a><span data-ttu-id="52141-103">Operación AddEntityFeedback</span><span class="sxs-lookup"><span data-stu-id="52141-103">AddEntityFeedback operation</span></span>

<span data-ttu-id="52141-104">La operación **AddEntityFeedback** devuelve información de error correspondiente a los problemas del servidor.</span><span class="sxs-lookup"><span data-stu-id="52141-104">The **AddEntityFeedback** operation returns error information corresponding to server-side issues.</span></span> 
  
<span data-ttu-id="52141-105">Esta operación se basa en el tipo de evento que se registra.</span><span class="sxs-lookup"><span data-stu-id="52141-105">This operation relies on the type of event being logged.</span></span> <span data-ttu-id="52141-106">Uno de los eventos más importantes es **EntityAdded**, que corresponde a una entidad que se está seleccionada.</span><span class="sxs-lookup"><span data-stu-id="52141-106">One of the most important events is **EntityAdded**, which corresponds to an entity being selected.</span></span> <span data-ttu-id="52141-107">Esta operación es por lotes, por lo que se puede utilizar para registrar los lotes de entradas en una sola solicitud.</span><span class="sxs-lookup"><span data-stu-id="52141-107">This operation is batch, so it can be used to log batches of entries in a single request.</span></span> 
  
## <a name="findpeople-request-examples"></a><span data-ttu-id="52141-108">Ejemplos de solicitudes FindPeople</span><span class="sxs-lookup"><span data-stu-id="52141-108">FindPeople request examples</span></span>

<span data-ttu-id="52141-109">La operación **AddEntityFeedback** proporciona una manera para que los clientes detalles de interacción con las entidades devueltas por el servicio de registro.</span><span class="sxs-lookup"><span data-stu-id="52141-109">The **AddEntityFeedback** operation provides a way for clients to log details of interaction with entities returned by the service.</span></span> <span data-ttu-id="52141-110">Esto puede usarse como una señal para mejorar la relevancia en segundo plano para cada cliente.</span><span class="sxs-lookup"><span data-stu-id="52141-110">This can be used as a signal to improve relevance behind the scenes for each client.</span></span> <span data-ttu-id="52141-111">Por ejemplo, los clientes pueden utilizar esta operación para proporcionar comentarios en las entidades de personas devueltas desde **FindPeople**.</span><span class="sxs-lookup"><span data-stu-id="52141-111">E.g., Clients can use this operation to provide feedback on people entities returned from **FindPeople**.</span></span>
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
                             xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
                             xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:AddEntityFeedback>
            <m:EntityFeedbackEntries>
                  <t:EntityFeedbackEntry>
                        <t:ClientEventTimeUTC> 2015-07-05T22:16:18+00:00</t:ClientEventTimeUTC>
                        <t:ClientEventTimeLocal> 2015-07-05T22:16:18+00:00</t:ClientEventTimeLocal>
                        <t:ClientSessionId>00000000-0000-0000-0000-000000000012</t:ClientSessionId>
                        <t:ClientVersion>15.01.0101.01</t:ClientVersion>
                        <t:ClientId>Web</t:ClientId>
                        <t:TransactionId>123456789</t:TransactionId>
                        <t:EventType>EntityAdded</t:EventType>
                        <t:TargetEntityList>["a","b","c"]</t:TargetEntityList>
                        <t:SourceOfEntityAdded></t:SourceOfEntityAdded>
                        <t:JSONPropertyBag></t:JSONPropertyBag>
                  </t:EntityFeedbackEntry>
                  <t:EntityFeedbackEntry>
                  …
                  </t:EntityFeedbackEntry>
            </m:EntityFeedbackEntries>
      </m:AddEntityFeedback>
   </soap:Body>
</soap:Envelope>

```

### <a name="the-request-soap-body-contents"></a><span data-ttu-id="52141-112">El contenido del cuerpo de la solicitud SOAP</span><span class="sxs-lookup"><span data-stu-id="52141-112">The request SOAP body contents</span></span>

<span data-ttu-id="52141-113">La solicitud soap contiene un solo elemento **EntityFeedbackEntries**.</span><span class="sxs-lookup"><span data-stu-id="52141-113">The soap request contains a single element **EntityFeedbackEntries**.</span></span> <span data-ttu-id="52141-114">Esto a su vez contiene una matriz de objetos de **EntityFeedbackEntry** .</span><span class="sxs-lookup"><span data-stu-id="52141-114">This in turn contains an array of **EntityFeedbackEntry** objects.</span></span> <span data-ttu-id="52141-115">Cada entrada de la matriz puede contener los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="52141-115">Each entry in the array can contain the following elements.</span></span> 
  
|<span data-ttu-id="52141-116">**Parámetros de la solicitud**</span><span class="sxs-lookup"><span data-stu-id="52141-116">**Request Parameters**</span></span>|<span data-ttu-id="52141-117">**Necesario**</span><span class="sxs-lookup"><span data-stu-id="52141-117">**Required**</span></span>|<span data-ttu-id="52141-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="52141-118">**Description**</span></span>|<span data-ttu-id="52141-119">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="52141-119">**Type**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="52141-120">**ClientEventTimeUtc**</span><span class="sxs-lookup"><span data-stu-id="52141-120">**ClientEventTimeUtc**</span></span> <br/> |<span data-ttu-id="52141-121">Sí</span><span class="sxs-lookup"><span data-stu-id="52141-121">Yes</span></span>  <br/> |<span data-ttu-id="52141-122">La hora UTC se produjo el evento del cliente.</span><span class="sxs-lookup"><span data-stu-id="52141-122">The UTC time the event occurred on the client-side.</span></span>  <br/> |<span data-ttu-id="52141-123">DateTime</span><span class="sxs-lookup"><span data-stu-id="52141-123">DateTime</span></span>  <br/> |
|<span data-ttu-id="52141-124">**ClientEventTimeLocal**</span><span class="sxs-lookup"><span data-stu-id="52141-124">**ClientEventTimeLocal**</span></span> <br/> |<span data-ttu-id="52141-125">Sí</span><span class="sxs-lookup"><span data-stu-id="52141-125">Yes</span></span>  <br/> |<span data-ttu-id="52141-126">La hora local que se produjo el evento en el lado del cliente.</span><span class="sxs-lookup"><span data-stu-id="52141-126">The local time the event occurred on the client side.</span></span>  <br/> |<span data-ttu-id="52141-127">DateTime</span><span class="sxs-lookup"><span data-stu-id="52141-127">DateTime</span></span>  <br/> |
|<span data-ttu-id="52141-128">**ClientId**</span><span class="sxs-lookup"><span data-stu-id="52141-128">**ClientId**</span></span> <br/> |<span data-ttu-id="52141-129">Sí</span><span class="sxs-lookup"><span data-stu-id="52141-129">Yes</span></span>  <br/> |<span data-ttu-id="52141-130">Tipo de cliente (por ejemplo, Outlook, OWA, etcetera).</span><span class="sxs-lookup"><span data-stu-id="52141-130">Type of Client (E.g., Outlook, OWA, etc.).</span></span>  <br/> |<span data-ttu-id="52141-131">ClientIDType (enumeración)</span><span class="sxs-lookup"><span data-stu-id="52141-131">ClientIDType Enumeration</span></span>  <br/> |
|<span data-ttu-id="52141-132">**ClientSessionId**</span><span class="sxs-lookup"><span data-stu-id="52141-132">**ClientSessionId**</span></span> <br/> |<span data-ttu-id="52141-133">Sí</span><span class="sxs-lookup"><span data-stu-id="52141-133">Yes</span></span>  <br/> |<span data-ttu-id="52141-134">GUID que identifica el identificador de sesión.</span><span class="sxs-lookup"><span data-stu-id="52141-134">GUID Identifying the session ID.</span></span> <span data-ttu-id="52141-135">Se genera en el cliente.</span><span class="sxs-lookup"><span data-stu-id="52141-135">Generated on the client.</span></span>  <br/> |<span data-ttu-id="52141-136">GUID</span><span class="sxs-lookup"><span data-stu-id="52141-136">GUID</span></span>  <br/> |
|<span data-ttu-id="52141-137">**ClientVersion**</span><span class="sxs-lookup"><span data-stu-id="52141-137">**ClientVersion**</span></span> <br/> |<span data-ttu-id="52141-138">Sí</span><span class="sxs-lookup"><span data-stu-id="52141-138">Yes</span></span>  <br/> |<span data-ttu-id="52141-139">Versión del cliente (por ejemplo, 15.01.0101.000).</span><span class="sxs-lookup"><span data-stu-id="52141-139">Version of the client (E.g., 15.01.0101.000).</span></span>  <br/> |<span data-ttu-id="52141-140">Cadena</span><span class="sxs-lookup"><span data-stu-id="52141-140">String</span></span>  <br/> |
|<span data-ttu-id="52141-141">**EntityAddSource**</span><span class="sxs-lookup"><span data-stu-id="52141-141">**EntityAddSource**</span></span> <br/> |<span data-ttu-id="52141-142">No</span><span class="sxs-lookup"><span data-stu-id="52141-142">No</span></span>  <br/> |<span data-ttu-id="52141-143">Origen de EntityAded (E.g., EntityRelevanceAPI, tipos, pegados).</span><span class="sxs-lookup"><span data-stu-id="52141-143">Source for EntityAded (E.g., EntityRelevanceAPI, types, pasted).</span></span>  <br/> |<span data-ttu-id="52141-144">EntityAddSource (enumeración)</span><span class="sxs-lookup"><span data-stu-id="52141-144">EntityAddSource Enumeration</span></span>  <br/> |
|<span data-ttu-id="52141-145">**EntrySequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="52141-145">**EntrySequenceNumber**</span></span> <br/> |<span data-ttu-id="52141-146">Sí</span><span class="sxs-lookup"><span data-stu-id="52141-146">Yes</span></span>  <br/> |<span data-ttu-id="52141-147">Un entero incremental por sesión de cliente.</span><span class="sxs-lookup"><span data-stu-id="52141-147">An incremental integer per client session.</span></span> <span data-ttu-id="52141-148">Se usa para detectar la pérdida de datos.</span><span class="sxs-lookup"><span data-stu-id="52141-148">Used for detecting data loss.</span></span>  <br/> |<span data-ttu-id="52141-149">Int</span><span class="sxs-lookup"><span data-stu-id="52141-149">Int</span></span>  <br/> |
|<span data-ttu-id="52141-150">**EventType**</span><span class="sxs-lookup"><span data-stu-id="52141-150">**EventType**</span></span> <br/> |<span data-ttu-id="52141-151">Sí</span><span class="sxs-lookup"><span data-stu-id="52141-151">Yes</span></span>  <br/> |<span data-ttu-id="52141-152">Tipo de evento (E.g., se agrega la entidad, entidad quitado).</span><span class="sxs-lookup"><span data-stu-id="52141-152">Type of event (E.g., Entity Added, Entity Removed).</span></span>  <br/> |<span data-ttu-id="52141-153">Cadena</span><span class="sxs-lookup"><span data-stu-id="52141-153">String</span></span>  <br/> |
|<span data-ttu-id="52141-154">**JSONPropertyBag**</span><span class="sxs-lookup"><span data-stu-id="52141-154">**JSONPropertyBag**</span></span> <br/> |<span data-ttu-id="52141-155">No</span><span class="sxs-lookup"><span data-stu-id="52141-155">No</span></span>  <br/> |<span data-ttu-id="52141-156">Propiedades adicionales asociadas con el evento (blob JSON de pares clave/valor).</span><span class="sxs-lookup"><span data-stu-id="52141-156">Additional properties associated with the event (JSON blob of key/value pairs).</span></span>  <br/> |<span data-ttu-id="52141-157">Blob JSON</span><span class="sxs-lookup"><span data-stu-id="52141-157">JSON Blob</span></span>  <br/> |
|<span data-ttu-id="52141-158">**TargetEntityList**</span><span class="sxs-lookup"><span data-stu-id="52141-158">**TargetEntityList**</span></span> <br/> |<span data-ttu-id="52141-159">No</span><span class="sxs-lookup"><span data-stu-id="52141-159">No</span></span>  <br/> |<span data-ttu-id="52141-160">Lista de las entidades asociadas con el evento.</span><span class="sxs-lookup"><span data-stu-id="52141-160">List of entities associated with the event.</span></span>  <br/> |<span data-ttu-id="52141-161">Cadena JSON</span><span class="sxs-lookup"><span data-stu-id="52141-161">JSON String</span></span>  <br/> |
|<span data-ttu-id="52141-162">**TransactionId**</span><span class="sxs-lookup"><span data-stu-id="52141-162">**TransactionId**</span></span> <br/> |<span data-ttu-id="52141-163">No</span><span class="sxs-lookup"><span data-stu-id="52141-163">No</span></span>  <br/> |<span data-ttu-id="52141-164">Identificador (GUID) correlacionar el identificador en los registros de la consulta.</span><span class="sxs-lookup"><span data-stu-id="52141-164">ID (GUID) correlating the ID in query logs.</span></span>  <br/> |<span data-ttu-id="52141-165">Cadena</span><span class="sxs-lookup"><span data-stu-id="52141-165">String</span></span>  <br/> |
   
### <a name="successful-addentityfeedback-operation-response"></a><span data-ttu-id="52141-166">Respuesta es correcta de operación AddEntityFeedback</span><span class="sxs-lookup"><span data-stu-id="52141-166">Successful AddEntityFeedback operation response</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
    <s:Header>
        <h:ServerVersionInfo MajorVersion="15" 
                                MinorVersion="1" 
                                MajorBuildNumber="228" 
                                MinorBuildNumber="0" 
                                Version="V2_49" 
                                xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                                xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                                xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
    </s:Header>
    <s:Body>
        <AddEntityFeedbackResponse ResponseClass="Success" 
                                                              xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" 
                                                              xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                                                              xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
            <ResponseCode>NoError</ResponseCode>
            <ErrorCount>0</ErrorCount>
            <ErrorDetails />
        </AddEntityFeedbackResponse>
    </s:Body>
</s:Envelope> 

```

### <a name="the-response-soap-body-contains-the-following-elements"></a><span data-ttu-id="52141-167">La respuesta SOAP body contiene los siguientes elementos</span><span class="sxs-lookup"><span data-stu-id="52141-167">The response SOAP body contains the following elements</span></span>

#### <a name="errors"></a><span data-ttu-id="52141-168">Errores</span><span class="sxs-lookup"><span data-stu-id="52141-168">Errors</span></span> 
  
<span data-ttu-id="52141-169">La API puede iniciar un lote de entradas de comentarios, se todo lo que se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="52141-169">The API can log a batch of feedback entries, we log all that we can.</span></span> <span data-ttu-id="52141-170">Este campo representa el número de entradas de error que no se han iniciado.</span><span class="sxs-lookup"><span data-stu-id="52141-170">This field represents the number of error entries that were not logged.</span></span>
    
#### <a name="errordetails"></a><span data-ttu-id="52141-171">ErrorDetails</span><span class="sxs-lookup"><span data-stu-id="52141-171">ErrorDetails</span></span>
  
<span data-ttu-id="52141-172">Separa los detalles relativos a los errores anteriores por `;`.</span><span class="sxs-lookup"><span data-stu-id="52141-172">Details pertaining to the errors above separates by `;`.</span></span>
    
### <a name="currently-supported-values"></a><span data-ttu-id="52141-173">Valores admitidos actualmente</span><span class="sxs-lookup"><span data-stu-id="52141-173">Currently supported values</span></span>

|<span data-ttu-id="52141-174">**ClientIdType (enumeración)**</span><span class="sxs-lookup"><span data-stu-id="52141-174">**ClientIdType Enumeration**</span></span>|
|:-----|
|<span data-ttu-id="52141-175">Escritorio</span><span class="sxs-lookup"><span data-stu-id="52141-175">Desktop</span></span>  <br/> |
|<span data-ttu-id="52141-176">Exchange</span><span class="sxs-lookup"><span data-stu-id="52141-176">Exchange</span></span>  <br/> |
|<span data-ttu-id="52141-177">IMAP4</span><span class="sxs-lookup"><span data-stu-id="52141-177">IMAP4</span></span>  <br/> |
|<span data-ttu-id="52141-178">Lync</span><span class="sxs-lookup"><span data-stu-id="52141-178">Lync</span></span>  <br/> |
|<span data-ttu-id="52141-179">MacMail</span><span class="sxs-lookup"><span data-stu-id="52141-179">MacMail</span></span>  <br/> |
|<span data-ttu-id="52141-180">MacOutlook</span><span class="sxs-lookup"><span data-stu-id="52141-180">MacOutlook</span></span>  <br/> |
|<span data-ttu-id="52141-181">Móvil</span><span class="sxs-lookup"><span data-stu-id="52141-181">Mobile</span></span>  <br/> |
|<span data-ttu-id="52141-182">Otro</span><span class="sxs-lookup"><span data-stu-id="52141-182">Other</span></span>  <br/> |
|<span data-ttu-id="52141-183">Outlook</span><span class="sxs-lookup"><span data-stu-id="52141-183">Outlook</span></span>  <br/> |
|<span data-ttu-id="52141-184">OutlookService</span><span class="sxs-lookup"><span data-stu-id="52141-184">OutlookService</span></span>  <br/> |
|<span data-ttu-id="52141-185">POP3</span><span class="sxs-lookup"><span data-stu-id="52141-185">POP3</span></span>  <br/> |
|<span data-ttu-id="52141-186">Tableta</span><span class="sxs-lookup"><span data-stu-id="52141-186">Tablet</span></span>  <br/> |
|<span data-ttu-id="52141-187">Web</span><span class="sxs-lookup"><span data-stu-id="52141-187">Web</span></span>  <br/> |
   
|<span data-ttu-id="52141-188">**EntityAddSource (enumeración)**</span><span class="sxs-lookup"><span data-stu-id="52141-188">**EntityAddSource Enumeration**</span></span>|
|:-----|
|<span data-ttu-id="52141-189">ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="52141-189">ActiveDirectory</span></span>  <br/> |
|<span data-ttu-id="52141-190">EntityRelevanceApi</span><span class="sxs-lookup"><span data-stu-id="52141-190">EntityRelevanceApi</span></span>  <br/> |
|<span data-ttu-id="52141-191">EntityRelevanceApiCache</span><span class="sxs-lookup"><span data-stu-id="52141-191">EntityRelevanceApiCache</span></span>  <br/> |
|<span data-ttu-id="52141-192">ExplicitTyping</span><span class="sxs-lookup"><span data-stu-id="52141-192">ExplicitTyping</span></span>  <br/> |
|<span data-ttu-id="52141-193">LocalCache</span><span class="sxs-lookup"><span data-stu-id="52141-193">LocalCache</span></span>  <br/> |
|<span data-ttu-id="52141-194">LocalCacheAndEntityRelevanceAPI</span><span class="sxs-lookup"><span data-stu-id="52141-194">LocalCacheAndEntityRelevanceAPI</span></span>  <br/> |
|<span data-ttu-id="52141-195">None</span><span class="sxs-lookup"><span data-stu-id="52141-195">None</span></span>  <br/> |
|<span data-ttu-id="52141-196">Otro</span><span class="sxs-lookup"><span data-stu-id="52141-196">Other</span></span>  <br/> |
|<span data-ttu-id="52141-197">Pegar</span><span class="sxs-lookup"><span data-stu-id="52141-197">Paste</span></span>  <br/> |
   
### <a name="addentityfeedback-operation-error-response"></a><span data-ttu-id="52141-198">Respuesta de error de la operación de AddEntityFeedback</span><span class="sxs-lookup"><span data-stu-id="52141-198">AddEntityFeedback operation error response</span></span>

<span data-ttu-id="52141-199">Para los códigos de error que son genéricos de EWS, consulte [ResponseCode](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="52141-199">For error codes that are generic to EWS, see [ResponseCode](responsecode.md).</span></span>
  
### <a name="example-of-addentityfeedback-in-conjunction-with-findpeople"></a><span data-ttu-id="52141-200">Ejemplo de AddEntityFeedback junto con FindPeople</span><span class="sxs-lookup"><span data-stu-id="52141-200">Example of AddEntityFeedback in conjunction with FindPeople</span></span>

#### <a name="findpeople-request"></a><span data-ttu-id="52141-201">Solicitud de FindPeople</span><span class="sxs-lookup"><span data-stu-id="52141-201">FindPeople request</span></span>
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
<soap:Body >
    <m:FindPeople>
      <m:IndexedPageItemView BasePoint="Beginning" MaxEntriesReturned="100" Offset="0"/>
      <m:QueryString>user1</m:QueryString>
      <m:SearchPeopleSuggestionIndex>true</m:SearchPeopleSuggestionIndex>
    </m:FindPeople>
  </soap:Body>
</soap:Envelope>    
    
```

#### <a name="findpeople-response"></a><span data-ttu-id="52141-202">Respuesta de FindPeople</span><span class="sxs-lookup"><span data-stu-id="52141-202">FindPeople response</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
    <s:Header>
        <h:ServerVersionInfo MajorVersion="15" MinorVersion="1" MajorBuildNumber="302" MinorBuildNumber="0" Version="V2_68" xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
    </s:Header>
    <s:Body>
        <FindPeopleResponse ResponseClass="Success" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
            <ResponseCode>NoError</ResponseCode>
            <People>
                <Persona xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
                    <PersonaId Id="AAUQAFjZ4UxX8SZCqSPFsmh0cSo=" />
                    <PersonaType>Person</PersonaType>
                    <CreationTime>2015-10-02T23:25:42</CreationTime>
                    <DisplayName>user2</DisplayName>
…
                  </Persona>
            </People>
            <TotalNumberOfPeopleInView>0</TotalNumberOfPeopleInView>
            <FirstMatchingRowIndex>0</FirstMatchingRowIndex>
            <FirstLoadedRowIndex>0</FirstLoadedRowIndex>
            <TransactionId>b56ad16e-5d5a-4574-90f8-b8dd57382be6</TransactionId>
        </FindPeopleResponse>
    </s:Body>
</s:Envelope>

```

#### <a name="addentityfeedback-request"></a><span data-ttu-id="52141-203">Solicitud de AddEntityFeedback</span><span class="sxs-lookup"><span data-stu-id="52141-203">AddEntityFeedback request</span></span>

```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:AddEntityFeedback>
<m:EntityFeedbackEntries>
<t:EntityFeedbackEntry>
         <t:ClientEventTimeUtc>2015-07-05T22:16:18+00:00</t:ClientEventTimeUtc>
         <t:ClientEventTimeLocal>2015-07-05T22:16:18+00:00</t:ClientEventTimeLocal>
         <t:ClientSessionId>00000000-0000-0000-0000-000000000012</t:ClientSessionId>
         <t:ClientVersion>15.01.0101.01</t:ClientVersion>
         <t:ClientId>Web</t:ClientId>
         <t:TransactionId>b56ad16e-5d5a-4574-90f8-b8dd57382be6</t:TransactionId>
         <t:EventType>EntityAdded</t:EventType>
         <t:TargetEntityList>["user1@ms7.com"]</t:TargetEntityList>
         <t:SourceOfEntityAdded>EntityRelevanceApi</t:SourceOfEntityAdded>
         <t:JSONPropertyBag></t:JSONPropertyBag>
</t:EntityFeedbackEntry>
</m:EntityFeedbackEntries>
      </m:AddEntityFeedback>
   </soap:Body>
</soap:Envelope>

```

> [!NOTE]
> <span data-ttu-id="52141-204">Uso de FindPeople respuesta transacciones ID como la transacción de solicitud de AddEntityFeedback Id.</span><span class="sxs-lookup"><span data-stu-id="52141-204">Using FindPeople response transaction ID as the AddEntityFeedback request transaction ID.</span></span> 
  
#### <a name="addentityfeedback-response"></a><span data-ttu-id="52141-205">Respuesta de AddEntityFeedback</span><span class="sxs-lookup"><span data-stu-id="52141-205">AddEntityFeedback response</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
    <s:Header>
        <h:ServerVersionInfo MajorVersion="15" MinorVersion="1" MajorBuildNumber="302" MinorBuildNumber="0" Version="V2_68" xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
    </s:Header>
    <s:Body>
        <AddEntityFeedbackResponse ResponseClass="Success" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
            <ResponseCode>NoError</ResponseCode>
            <ErrorCount>0</ErrorCount>
            <ErrorDetails />
        </AddEntityFeedbackResponse>
    </s:Body>
</s:Envelope>

```


