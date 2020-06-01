---
title: Operación AddEntityFeedback
manager: luken
ms.date: 4/18/2016
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 00e40197-5794-4268-b937-bd65aa044890
description: La operación AddEntityFeedback devuelve información de error correspondiente a problemas del lado servidor.
ms.openlocfilehash: a1027a0a1ee06cf3e83833b1d84c13d77b07c0b9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458442"
---
# <a name="addentityfeedback-operation"></a><span data-ttu-id="d1b07-103">Operación AddEntityFeedback</span><span class="sxs-lookup"><span data-stu-id="d1b07-103">AddEntityFeedback operation</span></span>

<span data-ttu-id="d1b07-104">La operación **AddEntityFeedback** devuelve información de error correspondiente a problemas del lado servidor.</span><span class="sxs-lookup"><span data-stu-id="d1b07-104">The **AddEntityFeedback** operation returns error information corresponding to server-side issues.</span></span> 
  
<span data-ttu-id="d1b07-105">Esta operación depende del tipo de evento que se está registrando.</span><span class="sxs-lookup"><span data-stu-id="d1b07-105">This operation relies on the type of event being logged.</span></span> <span data-ttu-id="d1b07-106">Uno de los eventos más importantes es **EntityAdded**, que corresponde a una entidad seleccionada.</span><span class="sxs-lookup"><span data-stu-id="d1b07-106">One of the most important events is **EntityAdded**, which corresponds to an entity being selected.</span></span> <span data-ttu-id="d1b07-107">Esta operación es un lote, por lo que se puede usar para registrar lotes de entradas en una sola solicitud.</span><span class="sxs-lookup"><span data-stu-id="d1b07-107">This operation is batch, so it can be used to log batches of entries in a single request.</span></span> 
  
## <a name="findpeople-request-examples"></a><span data-ttu-id="d1b07-108">Ejemplos de solicitudes de FindPeople</span><span class="sxs-lookup"><span data-stu-id="d1b07-108">FindPeople request examples</span></span>

<span data-ttu-id="d1b07-109">La operación **AddEntityFeedback** proporciona un medio para que los clientes registren detalles de interacción con entidades devueltas por el servicio.</span><span class="sxs-lookup"><span data-stu-id="d1b07-109">The **AddEntityFeedback** operation provides a way for clients to log details of interaction with entities returned by the service.</span></span> <span data-ttu-id="d1b07-110">Esto puede usarse como una señal para mejorar la relevancia en segundo plano para cada cliente.</span><span class="sxs-lookup"><span data-stu-id="d1b07-110">This can be used as a signal to improve relevance behind the scenes for each client.</span></span> <span data-ttu-id="d1b07-111">Por ejemplo, los clientes pueden usar esta operación para enviar comentarios sobre entidades de personas devueltas desde **FindPeople**.</span><span class="sxs-lookup"><span data-stu-id="d1b07-111">E.g., Clients can use this operation to provide feedback on people entities returned from **FindPeople**.</span></span>
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
                             xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                             xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="the-request-soap-body-contents"></a><span data-ttu-id="d1b07-112">El contenido del cuerpo SOAP de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d1b07-112">The request SOAP body contents</span></span>

<span data-ttu-id="d1b07-113">La solicitud SOAP contiene un elemento único **EntityFeedbackEntries**.</span><span class="sxs-lookup"><span data-stu-id="d1b07-113">The soap request contains a single element **EntityFeedbackEntries**.</span></span> <span data-ttu-id="d1b07-114">Esto, a su vez, contiene una matriz de objetos **EntityFeedbackEntry** .</span><span class="sxs-lookup"><span data-stu-id="d1b07-114">This in turn contains an array of **EntityFeedbackEntry** objects.</span></span> <span data-ttu-id="d1b07-115">Cada entrada de la matriz puede contener los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="d1b07-115">Each entry in the array can contain the following elements.</span></span> 
  
|<span data-ttu-id="d1b07-116">**Parámetros de solicitud**</span><span class="sxs-lookup"><span data-stu-id="d1b07-116">**Request Parameters**</span></span>|<span data-ttu-id="d1b07-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="d1b07-117">**Required**</span></span>|<span data-ttu-id="d1b07-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d1b07-118">**Description**</span></span>|<span data-ttu-id="d1b07-119">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="d1b07-119">**Type**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d1b07-120">**ClientEventTimeUtc**</span><span class="sxs-lookup"><span data-stu-id="d1b07-120">**ClientEventTimeUtc**</span></span> <br/> |<span data-ttu-id="d1b07-121">Sí</span><span class="sxs-lookup"><span data-stu-id="d1b07-121">Yes</span></span>  <br/> |<span data-ttu-id="d1b07-122">La hora UTC en que se produjo el evento en el lado cliente.</span><span class="sxs-lookup"><span data-stu-id="d1b07-122">The UTC time the event occurred on the client-side.</span></span>  <br/> |<span data-ttu-id="d1b07-123">DateTime</span><span class="sxs-lookup"><span data-stu-id="d1b07-123">DateTime</span></span>  <br/> |
|<span data-ttu-id="d1b07-124">**ClientEventTimeLocal**</span><span class="sxs-lookup"><span data-stu-id="d1b07-124">**ClientEventTimeLocal**</span></span> <br/> |<span data-ttu-id="d1b07-125">Sí</span><span class="sxs-lookup"><span data-stu-id="d1b07-125">Yes</span></span>  <br/> |<span data-ttu-id="d1b07-126">La hora local en la que se produjo el evento en el lado cliente.</span><span class="sxs-lookup"><span data-stu-id="d1b07-126">The local time the event occurred on the client side.</span></span>  <br/> |<span data-ttu-id="d1b07-127">DateTime</span><span class="sxs-lookup"><span data-stu-id="d1b07-127">DateTime</span></span>  <br/> |
|<span data-ttu-id="d1b07-128">**ClientId**</span><span class="sxs-lookup"><span data-stu-id="d1b07-128">**ClientId**</span></span> <br/> |<span data-ttu-id="d1b07-129">Sí</span><span class="sxs-lookup"><span data-stu-id="d1b07-129">Yes</span></span>  <br/> |<span data-ttu-id="d1b07-130">Tipo de cliente (por ejemplo, Outlook, OWA, etc.).</span><span class="sxs-lookup"><span data-stu-id="d1b07-130">Type of Client (E.g., Outlook, OWA, etc.).</span></span>  <br/> |<span data-ttu-id="d1b07-131">Enumeración ClientIDType</span><span class="sxs-lookup"><span data-stu-id="d1b07-131">ClientIDType Enumeration</span></span>  <br/> |
|<span data-ttu-id="d1b07-132">**ClientSessionId**</span><span class="sxs-lookup"><span data-stu-id="d1b07-132">**ClientSessionId**</span></span> <br/> |<span data-ttu-id="d1b07-133">Sí</span><span class="sxs-lookup"><span data-stu-id="d1b07-133">Yes</span></span>  <br/> |<span data-ttu-id="d1b07-134">GUID que identifica el identificador de sesión.</span><span class="sxs-lookup"><span data-stu-id="d1b07-134">GUID Identifying the session ID.</span></span> <span data-ttu-id="d1b07-135">Se genera en el cliente.</span><span class="sxs-lookup"><span data-stu-id="d1b07-135">Generated on the client.</span></span>  <br/> |<span data-ttu-id="d1b07-136">GUID</span><span class="sxs-lookup"><span data-stu-id="d1b07-136">GUID</span></span>  <br/> |
|<span data-ttu-id="d1b07-137">**ClientVersion**</span><span class="sxs-lookup"><span data-stu-id="d1b07-137">**ClientVersion**</span></span> <br/> |<span data-ttu-id="d1b07-138">Sí</span><span class="sxs-lookup"><span data-stu-id="d1b07-138">Yes</span></span>  <br/> |<span data-ttu-id="d1b07-139">Versión del cliente (por ejemplo, 15.01.0101.000).</span><span class="sxs-lookup"><span data-stu-id="d1b07-139">Version of the client (E.g., 15.01.0101.000).</span></span>  <br/> |<span data-ttu-id="d1b07-140">Cadena</span><span class="sxs-lookup"><span data-stu-id="d1b07-140">String</span></span>  <br/> |
|<span data-ttu-id="d1b07-141">**EntityAddSource**</span><span class="sxs-lookup"><span data-stu-id="d1b07-141">**EntityAddSource**</span></span> <br/> |<span data-ttu-id="d1b07-142">No</span><span class="sxs-lookup"><span data-stu-id="d1b07-142">No</span></span>  <br/> |<span data-ttu-id="d1b07-143">Origen para EntityAded (por ejemplo, EntityRelevanceAPI, Types, pegados).</span><span class="sxs-lookup"><span data-stu-id="d1b07-143">Source for EntityAded (E.g., EntityRelevanceAPI, types, pasted).</span></span>  <br/> |<span data-ttu-id="d1b07-144">Enumeración EntityAddSource</span><span class="sxs-lookup"><span data-stu-id="d1b07-144">EntityAddSource Enumeration</span></span>  <br/> |
|<span data-ttu-id="d1b07-145">**EntrySequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="d1b07-145">**EntrySequenceNumber**</span></span> <br/> |<span data-ttu-id="d1b07-146">Sí</span><span class="sxs-lookup"><span data-stu-id="d1b07-146">Yes</span></span>  <br/> |<span data-ttu-id="d1b07-147">Entero incremental por sesión de cliente.</span><span class="sxs-lookup"><span data-stu-id="d1b07-147">An incremental integer per client session.</span></span> <span data-ttu-id="d1b07-148">Se usa para detectar la pérdida de datos.</span><span class="sxs-lookup"><span data-stu-id="d1b07-148">Used for detecting data loss.</span></span>  <br/> |<span data-ttu-id="d1b07-149">Int</span><span class="sxs-lookup"><span data-stu-id="d1b07-149">Int</span></span>  <br/> |
|<span data-ttu-id="d1b07-150">**EventType**</span><span class="sxs-lookup"><span data-stu-id="d1b07-150">**EventType**</span></span> <br/> |<span data-ttu-id="d1b07-151">Sí</span><span class="sxs-lookup"><span data-stu-id="d1b07-151">Yes</span></span>  <br/> |<span data-ttu-id="d1b07-152">Tipo de evento (por ejemplo, entidad agregada, entidad eliminada).</span><span class="sxs-lookup"><span data-stu-id="d1b07-152">Type of event (E.g., Entity Added, Entity Removed).</span></span>  <br/> |<span data-ttu-id="d1b07-153">Cadena</span><span class="sxs-lookup"><span data-stu-id="d1b07-153">String</span></span>  <br/> |
|<span data-ttu-id="d1b07-154">**JSONPropertyBag**</span><span class="sxs-lookup"><span data-stu-id="d1b07-154">**JSONPropertyBag**</span></span> <br/> |<span data-ttu-id="d1b07-155">No</span><span class="sxs-lookup"><span data-stu-id="d1b07-155">No</span></span>  <br/> |<span data-ttu-id="d1b07-156">Propiedades adicionales asociadas con el evento (objeto binario JSON de pares clave-valor).</span><span class="sxs-lookup"><span data-stu-id="d1b07-156">Additional properties associated with the event (JSON blob of key/value pairs).</span></span>  <br/> |<span data-ttu-id="d1b07-157">BLOB de JSON</span><span class="sxs-lookup"><span data-stu-id="d1b07-157">JSON Blob</span></span>  <br/> |
|<span data-ttu-id="d1b07-158">**TargetEntityList**</span><span class="sxs-lookup"><span data-stu-id="d1b07-158">**TargetEntityList**</span></span> <br/> |<span data-ttu-id="d1b07-159">No</span><span class="sxs-lookup"><span data-stu-id="d1b07-159">No</span></span>  <br/> |<span data-ttu-id="d1b07-160">Lista de entidades asociadas al evento.</span><span class="sxs-lookup"><span data-stu-id="d1b07-160">List of entities associated with the event.</span></span>  <br/> |<span data-ttu-id="d1b07-161">Cadena JSON</span><span class="sxs-lookup"><span data-stu-id="d1b07-161">JSON String</span></span>  <br/> |
|<span data-ttu-id="d1b07-162">**TransactionId**</span><span class="sxs-lookup"><span data-stu-id="d1b07-162">**TransactionId**</span></span> <br/> |<span data-ttu-id="d1b07-163">No</span><span class="sxs-lookup"><span data-stu-id="d1b07-163">No</span></span>  <br/> |<span data-ttu-id="d1b07-164">IDENTIFICADOR (GUID) que correlaciona el identificador en los registros de consulta.</span><span class="sxs-lookup"><span data-stu-id="d1b07-164">ID (GUID) correlating the ID in query logs.</span></span>  <br/> |<span data-ttu-id="d1b07-165">Cadena</span><span class="sxs-lookup"><span data-stu-id="d1b07-165">String</span></span>  <br/> |
   
### <a name="successful-addentityfeedback-operation-response"></a><span data-ttu-id="d1b07-166">Respuesta de operación AddEntityFeedback correcta</span><span class="sxs-lookup"><span data-stu-id="d1b07-166">Successful AddEntityFeedback operation response</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
    <s:Header>
        <h:ServerVersionInfo MajorVersion="15" 
                                MinorVersion="1" 
                                MajorBuildNumber="228" 
                                MinorBuildNumber="0" 
                                Version="V2_49" 
                                xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                                xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                                xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
    </s:Header>
    <s:Body>
        <AddEntityFeedbackResponse ResponseClass="Success" 
                                                              xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                                              xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                                                              xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
            <ResponseCode>NoError</ResponseCode>
            <ErrorCount>0</ErrorCount>
            <ErrorDetails />
        </AddEntityFeedbackResponse>
    </s:Body>
</s:Envelope> 

```

### <a name="the-response-soap-body-contains-the-following-elements"></a><span data-ttu-id="d1b07-167">El cuerpo SOAP de respuesta contiene los siguientes elementos</span><span class="sxs-lookup"><span data-stu-id="d1b07-167">The response SOAP body contains the following elements</span></span>

#### <a name="errors"></a><span data-ttu-id="d1b07-168">Errores</span><span class="sxs-lookup"><span data-stu-id="d1b07-168">Errors</span></span> 
  
<span data-ttu-id="d1b07-169">La API puede registrar un lote de entradas de comentarios, se registra todo lo que podemos.</span><span class="sxs-lookup"><span data-stu-id="d1b07-169">The API can log a batch of feedback entries, we log all that we can.</span></span> <span data-ttu-id="d1b07-170">Este campo representa el número de entradas de error que no se registraron.</span><span class="sxs-lookup"><span data-stu-id="d1b07-170">This field represents the number of error entries that were not logged.</span></span>
    
#### <a name="errordetails"></a><span data-ttu-id="d1b07-171">ErrorDetails</span><span class="sxs-lookup"><span data-stu-id="d1b07-171">ErrorDetails</span></span>
  
<span data-ttu-id="d1b07-172">Detalles relativos a los errores anteriores separa por `;` .</span><span class="sxs-lookup"><span data-stu-id="d1b07-172">Details pertaining to the errors above separates by `;`.</span></span>
    
### <a name="currently-supported-values"></a><span data-ttu-id="d1b07-173">Valores actualmente admitidos</span><span class="sxs-lookup"><span data-stu-id="d1b07-173">Currently supported values</span></span>

|<span data-ttu-id="d1b07-174">**Enumeración ClientIdType**</span><span class="sxs-lookup"><span data-stu-id="d1b07-174">**ClientIdType Enumeration**</span></span>|
|:-----|
|<span data-ttu-id="d1b07-175">Desktop</span><span class="sxs-lookup"><span data-stu-id="d1b07-175">Desktop</span></span>  <br/> |
|<span data-ttu-id="d1b07-176">Exchange</span><span class="sxs-lookup"><span data-stu-id="d1b07-176">Exchange</span></span>  <br/> |
|<span data-ttu-id="d1b07-177">IMAP4</span><span class="sxs-lookup"><span data-stu-id="d1b07-177">IMAP4</span></span>  <br/> |
|<span data-ttu-id="d1b07-178">2015</span><span class="sxs-lookup"><span data-stu-id="d1b07-178">Lync</span></span>  <br/> |
|<span data-ttu-id="d1b07-179">MacMail</span><span class="sxs-lookup"><span data-stu-id="d1b07-179">MacMail</span></span>  <br/> |
|<span data-ttu-id="d1b07-180">MacOutlook</span><span class="sxs-lookup"><span data-stu-id="d1b07-180">MacOutlook</span></span>  <br/> |
|<span data-ttu-id="d1b07-181">Mobile</span><span class="sxs-lookup"><span data-stu-id="d1b07-181">Mobile</span></span>  <br/> |
|<span data-ttu-id="d1b07-182">Otros</span><span class="sxs-lookup"><span data-stu-id="d1b07-182">Other</span></span>  <br/> |
|<span data-ttu-id="d1b07-183">Outlook</span><span class="sxs-lookup"><span data-stu-id="d1b07-183">Outlook</span></span>  <br/> |
|<span data-ttu-id="d1b07-184">OutlookService</span><span class="sxs-lookup"><span data-stu-id="d1b07-184">OutlookService</span></span>  <br/> |
|<span data-ttu-id="d1b07-185">POP3</span><span class="sxs-lookup"><span data-stu-id="d1b07-185">POP3</span></span>  <br/> |
|<span data-ttu-id="d1b07-186">Tablet</span><span class="sxs-lookup"><span data-stu-id="d1b07-186">Tablet</span></span>  <br/> |
|<span data-ttu-id="d1b07-187">Web</span><span class="sxs-lookup"><span data-stu-id="d1b07-187">Web</span></span>  <br/> |
   
|<span data-ttu-id="d1b07-188">**Enumeración EntityAddSource**</span><span class="sxs-lookup"><span data-stu-id="d1b07-188">**EntityAddSource Enumeration**</span></span>|
|:-----|
|<span data-ttu-id="d1b07-189">Directory</span><span class="sxs-lookup"><span data-stu-id="d1b07-189">ActiveDirectory</span></span>  <br/> |
|<span data-ttu-id="d1b07-190">EntityRelevanceApi</span><span class="sxs-lookup"><span data-stu-id="d1b07-190">EntityRelevanceApi</span></span>  <br/> |
|<span data-ttu-id="d1b07-191">EntityRelevanceApiCache</span><span class="sxs-lookup"><span data-stu-id="d1b07-191">EntityRelevanceApiCache</span></span>  <br/> |
|<span data-ttu-id="d1b07-192">ExplicitTyping</span><span class="sxs-lookup"><span data-stu-id="d1b07-192">ExplicitTyping</span></span>  <br/> |
|<span data-ttu-id="d1b07-193">LocalCache</span><span class="sxs-lookup"><span data-stu-id="d1b07-193">LocalCache</span></span>  <br/> |
|<span data-ttu-id="d1b07-194">LocalCacheAndEntityRelevanceAPI</span><span class="sxs-lookup"><span data-stu-id="d1b07-194">LocalCacheAndEntityRelevanceAPI</span></span>  <br/> |
|<span data-ttu-id="d1b07-195">Ninguno</span><span class="sxs-lookup"><span data-stu-id="d1b07-195">None</span></span>  <br/> |
|<span data-ttu-id="d1b07-196">Otros</span><span class="sxs-lookup"><span data-stu-id="d1b07-196">Other</span></span>  <br/> |
|<span data-ttu-id="d1b07-197">Paste</span><span class="sxs-lookup"><span data-stu-id="d1b07-197">Paste</span></span>  <br/> |
   
### <a name="addentityfeedback-operation-error-response"></a><span data-ttu-id="d1b07-198">Respuesta de error de operación de AddEntityFeedback</span><span class="sxs-lookup"><span data-stu-id="d1b07-198">AddEntityFeedback operation error response</span></span>

<span data-ttu-id="d1b07-199">Para los códigos de error que son genéricos para EWS, vea [ResponseCode](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="d1b07-199">For error codes that are generic to EWS, see [ResponseCode](responsecode.md).</span></span>
  
### <a name="example-of-addentityfeedback-in-conjunction-with-findpeople"></a><span data-ttu-id="d1b07-200">Ejemplo de AddEntityFeedback en combinación con FindPeople</span><span class="sxs-lookup"><span data-stu-id="d1b07-200">Example of AddEntityFeedback in conjunction with FindPeople</span></span>

#### <a name="findpeople-request"></a><span data-ttu-id="d1b07-201">Solicitud FindPeople</span><span class="sxs-lookup"><span data-stu-id="d1b07-201">FindPeople request</span></span>
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
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

#### <a name="findpeople-response"></a><span data-ttu-id="d1b07-202">Respuesta FindPeople</span><span class="sxs-lookup"><span data-stu-id="d1b07-202">FindPeople response</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
    <s:Header>
        <h:ServerVersionInfo MajorVersion="15" MinorVersion="1" MajorBuildNumber="302" MinorBuildNumber="0" Version="V2_68" xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
    </s:Header>
    <s:Body>
        <FindPeopleResponse ResponseClass="Success" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
            <ResponseCode>NoError</ResponseCode>
            <People>
                <Persona xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
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

#### <a name="addentityfeedback-request"></a><span data-ttu-id="d1b07-203">Solicitud AddEntityFeedback</span><span class="sxs-lookup"><span data-stu-id="d1b07-203">AddEntityFeedback request</span></span>

```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
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
> <span data-ttu-id="d1b07-204">Mediante FindPeople Response ID Transaction como el identificador de transacción de solicitud AddEntityFeedback.</span><span class="sxs-lookup"><span data-stu-id="d1b07-204">Using FindPeople response transaction ID as the AddEntityFeedback request transaction ID.</span></span> 
  
#### <a name="addentityfeedback-response"></a><span data-ttu-id="d1b07-205">Respuesta AddEntityFeedback</span><span class="sxs-lookup"><span data-stu-id="d1b07-205">AddEntityFeedback response</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
    <s:Header>
        <h:ServerVersionInfo MajorVersion="15" MinorVersion="1" MajorBuildNumber="302" MinorBuildNumber="0" Version="V2_68" xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
    </s:Header>
    <s:Body>
        <AddEntityFeedbackResponse ResponseClass="Success" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
            <ResponseCode>NoError</ResponseCode>
            <ErrorCount>0</ErrorCount>
            <ErrorDetails />
        </AddEntityFeedbackResponse>
    </s:Body>
</s:Envelope>

```


