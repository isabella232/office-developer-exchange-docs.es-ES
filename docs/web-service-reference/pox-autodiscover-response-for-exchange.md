---
title: Respuesta de detección automática POX para Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 08c6c5a2-a67a-4141-a8bd-1b5d560b90a7
description: La respuesta de detección automática contiene una respuesta a una solicitud de detección automática que se incluye una lista de direcciones URL que se usan para establecer un enlace con Exchange Web Services (EWS).
ms.openlocfilehash: d9f8a5cc86efaa4dceda7385164872ecc5409252
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836863"
---
# <a name="pox-autodiscover-response-for-exchange"></a><span data-ttu-id="b0a8a-103">Respuesta de detección automática POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="b0a8a-103">POX Autodiscover response for Exchange</span></span>

<span data-ttu-id="b0a8a-104">La respuesta de detección automática contiene una respuesta a una solicitud de detección automática que se incluye una lista de direcciones URL que se usan para establecer un enlace con Exchange Web Services (EWS).</span><span class="sxs-lookup"><span data-stu-id="b0a8a-104">The Autodiscover response contains a response to an Autodiscover request that includes a list of URLs that are used to establish a binding with Exchange Web Services (EWS).</span></span>
  
## <a name="autodiscover-response-example"></a><span data-ttu-id="b0a8a-105">Ejemplo de la respuesta de detección automática</span><span class="sxs-lookup"><span data-stu-id="b0a8a-105">Autodiscover response example</span></span>

### <a name="description"></a><span data-ttu-id="b0a8a-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="b0a8a-106">Description</span></span>

<span data-ttu-id="b0a8a-107">En el ejemplo siguiente se muestra una respuesta correcta de detección automática.</span><span class="sxs-lookup"><span data-stu-id="b0a8a-107">The following example shows a successful Autodiscover response.</span></span>
  
### <a name="code"></a><span data-ttu-id="b0a8a-108">Código</span><span class="sxs-lookup"><span data-stu-id="b0a8a-108">Code</span></span>

```XML
<Autodiscover xmlns="http://schemas.microsoft.com/exchange/autodiscover/responseschema/2006">
  <Response xmlns="http://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a">
    <User>
      <DisplayName>First Last</DisplayName>
      <LegacyDN>/o=contoso/ou=First Administrative Group/cn=Recipients/cn=iuser885646</LegacyDN>
      <DeploymentId>644560b8-a1ce-429c-8ace-23395843f701</DeploymentId>
    </User>
    <Account>
      <AccountType>email</AccountType>
      <Action>settings</Action>
      <Protocol>
        <Type>EXCH</Type>
        <Server>MBX-SERVER.mail.internal.contoso.com</Server>
        <ServerDN>/o=contoso/ou=Exchange Administrative Group (FYDIBOHF23SPDLT)/cn=Configuration/cn=Servers/cn=MBX-SERVER</ServerDN>
        <ServerVersion>72008287</ServerVersion>
        <MdbDN>/o=contoso/ou=Exchange Administrative Group (FYDIBOHF23SPDLT)/cn=Configuration/cn=Servers/cn=MBX-SERVER/cn=Microsoft Private MDB</MdbDN>
        <ASUrl>https://mail.contoso.com/ews/exchange.asmx</ASUrl>
        <OOFUrl>https://mail.contoso.com/ews/exchange.asmx</OOFUrl>
        <UMUrl>https://mail.contoso.com/unifiedmessaging/service.asmx</UMUrl>
        <OABUrl>https://mail.contoso.com/OAB/d29844a9-724e-468c-8820-0f7b345b767b/</OABUrl>
      </Protocol>
      <Protocol>
        <Type>EXPR</Type>
        <Server>Exchange.contoso.com</Server>
        <ASUrl>https://mail.contoso.com/ews/exchange.asmx</ASUrl>
        <OOFUrl>https://mail.contoso.com/ews/exchange.asmx</OOFUrl>
        <UMUrl>https://mail.contoso.com/unifiedmessaging/service.asmx</UMUrl>
        <OABUrl>https://mail.contoso.com/OAB/d29844a9-724e-468c-8820-0f7b345b767b/</OABUrl>
      </Protocol>
      <Protocol>
        <Type>WEB</Type>
        <Internal>
          <OWAUrl AuthenticationMethod="Ntlm, WindowsIntegrated">https://cas-01-server.mail.internal.contoso.com/owa</OWAUrl>
          <OWAUrl AuthenticationMethod="Ntlm, WindowsIntegrated">https://cas-02-server.mail.internal.contoso.com/owa</OWAUrl>
          <OWAUrl AuthenticationMethod="Basic">https://cas-04-server.mail.internal.contoso.com/owa</OWAUrl>
          <OWAUrl AuthenticationMethod="Ntlm, WindowsIntegrated">https://cas-05-server.mail.internal.contoso.com/owa</OWAUrl>
        </Internal>
      </Protocol>
    </Account>
  </Response>
</Autodiscover>
```

### <a name="comments"></a><span data-ttu-id="b0a8a-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b0a8a-109">Comments</span></span>

<span data-ttu-id="b0a8a-110">Para enlazar a servicios Web de Exchange, utilice la dirección URL identificada por el elemento [ASUrl (POX)](asurl-pox.md) .</span><span class="sxs-lookup"><span data-stu-id="b0a8a-110">To bind to Exchange Web Services, use the URL identified by the [ASUrl (POX)](asurl-pox.md) element.</span></span> 
  
### <a name="response-element"></a><span data-ttu-id="b0a8a-111">Elemento Response</span><span class="sxs-lookup"><span data-stu-id="b0a8a-111">Response Element</span></span>

<span data-ttu-id="b0a8a-112">En el cuerpo de la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="b0a8a-112">The following elements are used in the response body:</span></span>
  
- [<span data-ttu-id="b0a8a-113">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="b0a8a-113">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
    
- [<span data-ttu-id="b0a8a-114">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="b0a8a-114">Response (POX)</span></span>](response-pox.md)
    
- [<span data-ttu-id="b0a8a-115">Usuario (POX)</span><span class="sxs-lookup"><span data-stu-id="b0a8a-115">User (POX)</span></span>](user-pox.md)
    
- [<span data-ttu-id="b0a8a-116">DisplayName (POX)</span><span class="sxs-lookup"><span data-stu-id="b0a8a-116">DisplayName (POX)</span></span>](displayname-pox.md)
    
- [<span data-ttu-id="b0a8a-117">LegacyDN (POX)</span><span class="sxs-lookup"><span data-stu-id="b0a8a-117">LegacyDN (POX)</span></span>](legacydn-pox.md)
    
- [<span data-ttu-id="b0a8a-118">DeploymentId (POX)</span><span class="sxs-lookup"><span data-stu-id="b0a8a-118">DeploymentId (POX)</span></span>](deploymentid-pox.md)
    
- [<span data-ttu-id="b0a8a-119">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="b0a8a-119">Account (POX)</span></span>](account-pox.md)
    
- [<span data-ttu-id="b0a8a-120">AccountType (POX)</span><span class="sxs-lookup"><span data-stu-id="b0a8a-120">AccountType (POX)</span></span>](accounttype-pox.md)
    
- [<span data-ttu-id="b0a8a-121">Acción (POX)</span><span class="sxs-lookup"><span data-stu-id="b0a8a-121">Action (POX)</span></span>](action-pox.md)
    
- [<span data-ttu-id="b0a8a-122">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="b0a8a-122">Protocol (POX)</span></span>](protocol-pox.md)
    
- [<span data-ttu-id="b0a8a-123">Tipo (POX)</span><span class="sxs-lookup"><span data-stu-id="b0a8a-123">Type (POX)</span></span>](type-pox.md)
    
- [<span data-ttu-id="b0a8a-124">Servidor (POX)</span><span class="sxs-lookup"><span data-stu-id="b0a8a-124">Server (POX)</span></span>](server-pox.md)
    
- [<span data-ttu-id="b0a8a-125">ServerDN (POX)</span><span class="sxs-lookup"><span data-stu-id="b0a8a-125">ServerDN (POX)</span></span>](serverdn-pox.md)
    
- [<span data-ttu-id="b0a8a-126">ServerVersion (POX)</span><span class="sxs-lookup"><span data-stu-id="b0a8a-126">ServerVersion (POX)</span></span>](serverversion-pox.md)
    
- [<span data-ttu-id="b0a8a-127">MdbDN (POX)</span><span class="sxs-lookup"><span data-stu-id="b0a8a-127">MdbDN (POX)</span></span>](mdbdn-pox.md)
    
- [<span data-ttu-id="b0a8a-128">ASUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="b0a8a-128">ASUrl (POX)</span></span>](asurl-pox.md)
    
- [<span data-ttu-id="b0a8a-129">OOFUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="b0a8a-129">OOFUrl (POX)</span></span>](oofurl-pox.md)
    
- [<span data-ttu-id="b0a8a-130">UMUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="b0a8a-130">UMUrl (POX)</span></span>](umurl-pox.md)
    
- [<span data-ttu-id="b0a8a-131">OABUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="b0a8a-131">OABUrl (POX)</span></span>](oaburl-pox.md)
    
- [<span data-ttu-id="b0a8a-132">Interno (POX)</span><span class="sxs-lookup"><span data-stu-id="b0a8a-132">Internal (POX)</span></span>](internal-pox.md)
    
- [<span data-ttu-id="b0a8a-133">OWAUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="b0a8a-133">OWAUrl (POX)</span></span>](owaurl-pox.md)
    
## <a name="autodiscover-error-response-example"></a><span data-ttu-id="b0a8a-134">Ejemplo de respuesta de Error de detección automática</span><span class="sxs-lookup"><span data-stu-id="b0a8a-134">Autodiscover Error response example</span></span>

### <a name="description"></a><span data-ttu-id="b0a8a-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="b0a8a-135">Description</span></span>

<span data-ttu-id="b0a8a-136">En el ejemplo siguiente se muestra una respuesta de error de detección automática.</span><span class="sxs-lookup"><span data-stu-id="b0a8a-136">The following example shows an Autodiscover error response.</span></span>
  
### <a name="code"></a><span data-ttu-id="b0a8a-137">Código</span><span class="sxs-lookup"><span data-stu-id="b0a8a-137">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<Autodiscover xmlns="http://schemas.microsoft.com/exchange/autodiscover/responseschema/2006">
  <Response xmlns="http://schemas.microsoft.com/exchange/autodiscover/responseschema/2006">
    <Error Time="21:25:04.8897083" Id="4130155072">
      <ErrorCode>600</ErrorCode>
      <Message>Invalid Request</Message>
      <DebugData />
    </Error>
  </Response>
</Autodiscover>
```

### <a name="error-response-element"></a><span data-ttu-id="b0a8a-138">Elemento de respuesta de error</span><span class="sxs-lookup"><span data-stu-id="b0a8a-138">Error response element</span></span>

<span data-ttu-id="b0a8a-139">En el cuerpo de la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="b0a8a-139">The following elements are used in the response body:</span></span>
  
- [<span data-ttu-id="b0a8a-140">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="b0a8a-140">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
    
- [<span data-ttu-id="b0a8a-141">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="b0a8a-141">Response (POX)</span></span>](response-pox.md)
    
- [<span data-ttu-id="b0a8a-142">Error (POX)</span><span class="sxs-lookup"><span data-stu-id="b0a8a-142">Error (POX)</span></span>](error-pox.md)
    
- [<span data-ttu-id="b0a8a-143">ErrorCode (POX)</span><span class="sxs-lookup"><span data-stu-id="b0a8a-143">ErrorCode (POX)</span></span>](errorcode-pox.md)
    
- [<span data-ttu-id="b0a8a-144">Mensaje (POX)</span><span class="sxs-lookup"><span data-stu-id="b0a8a-144">Message (POX)</span></span>](message-pox.md)
    
- [<span data-ttu-id="b0a8a-145">DebugData (POX)</span><span class="sxs-lookup"><span data-stu-id="b0a8a-145">DebugData (POX)</span></span>](debugdata-pox.md)
    
## <a name="see-also"></a><span data-ttu-id="b0a8a-146">Ver también</span><span class="sxs-lookup"><span data-stu-id="b0a8a-146">See also</span></span>

- [<span data-ttu-id="b0a8a-147">Solicitud de detección automática POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="b0a8a-147">POX Autodiscover request for Exchange</span></span>](pox-autodiscover-request-for-exchange.md)
- [<span data-ttu-id="b0a8a-148">Referencia de servicio web POX de detección automática de Exchange</span><span class="sxs-lookup"><span data-stu-id="b0a8a-148">POX Autodiscover web service reference for Exchange</span></span>](pox-autodiscover-web-service-reference-for-exchange.md) 
- [<span data-ttu-id="b0a8a-149">Elementos de Autodiscover XML POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="b0a8a-149">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

