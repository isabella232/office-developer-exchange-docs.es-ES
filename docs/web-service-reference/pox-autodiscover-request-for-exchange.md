---
title: Solicitud de detección automática POX para Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 75671b1d-f35b-497b-8d8c-706f3f2535fd
description: La solicitud de detección automática contiene una consulta para la configuración de acceso de cliente de un usuario.
ms.openlocfilehash: 48d6c30946e75936ed93a6f4507d8a8d3ae47d40
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836865"
---
# <a name="pox-autodiscover-request-for-exchange"></a><span data-ttu-id="86909-103">Solicitud de detección automática POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="86909-103">POX Autodiscover request for Exchange</span></span>

<span data-ttu-id="86909-104">La solicitud de detección automática contiene una consulta para la configuración de acceso de cliente de un usuario.</span><span class="sxs-lookup"><span data-stu-id="86909-104">The Autodiscover request contains a query for a user's client access configuration.</span></span>
  
## <a name="autodiscover-request-example"></a><span data-ttu-id="86909-105">Ejemplo de solicitud de detección automática</span><span class="sxs-lookup"><span data-stu-id="86909-105">Autodiscover request example</span></span>

### <a name="description"></a><span data-ttu-id="86909-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="86909-106">Description</span></span>

<span data-ttu-id="86909-107">En el ejemplo de XML siguiente se muestra un cuerpo de la solicitud de detección automática.</span><span class="sxs-lookup"><span data-stu-id="86909-107">The following XML example shows an Autodiscover request body.</span></span>
  
### <a name="code"></a><span data-ttu-id="86909-108">Código</span><span class="sxs-lookup"><span data-stu-id="86909-108">Code</span></span>

```XML
<Autodiscover xmlns="http://schemas.microsoft.com/exchange/autodiscover/outlook/requestschema/2006">
   <Request>
     <EMailAddress>user@contoso.com</EMailAddress>
     <AcceptableResponseSchema>http://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a</AcceptableResponseSchema>
   </Request>
 </Autodiscover>
```

### <a name="request-headers"></a><span data-ttu-id="86909-109">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="86909-109">Request Headers</span></span>

<span data-ttu-id="86909-110">Los encabezados HTTP siguientes son opcionales al enviar solicitudes de detección automática.</span><span class="sxs-lookup"><span data-stu-id="86909-110">The following HTTP headers are optional when sending Autodiscover requests.</span></span>
  
<span data-ttu-id="86909-111">**La tabla 1. Encabezados de solicitud HTTP**</span><span class="sxs-lookup"><span data-stu-id="86909-111">**Table 1. HTTP request headers**</span></span>

|<span data-ttu-id="86909-112">**Header**</span><span class="sxs-lookup"><span data-stu-id="86909-112">**Header**</span></span>|<span data-ttu-id="86909-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="86909-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="86909-114">X-MapiHttpCapability</span><span class="sxs-lookup"><span data-stu-id="86909-114">X-MapiHttpCapability</span></span>  <br/> |<span data-ttu-id="86909-115">Si está presente y establecido en "1", indica que el cliente está solicitando información que puede usar para conectarse al servidor mediante el protocolo HTTP/MAPI.</span><span class="sxs-lookup"><span data-stu-id="86909-115">If present and set to "1", indicates that the client is requesting information that can be used to connect to the server by using the MAPI/HTTP protocol.</span></span> <span data-ttu-id="86909-116">Este encabezado es aplicable a los clientes que implementan el protocolo HTTP/MAPI.</span><span class="sxs-lookup"><span data-stu-id="86909-116">This header is applicable to clients that implement the MAPI/HTTP protocol.</span></span>  <br/> |
|<span data-ttu-id="86909-117">X-ClientCanHandle</span><span class="sxs-lookup"><span data-stu-id="86909-117">X-ClientCanHandle</span></span>  <br/> |<span data-ttu-id="86909-118">Este encabezado contiene una lista delimitada por comas de las capacidades que admite el cliente.</span><span class="sxs-lookup"><span data-stu-id="86909-118">This header contains a comma-delimited list of capabilities that the client supports.</span></span> <span data-ttu-id="86909-119">Los valores posibles se especifican en la tabla 2.</span><span class="sxs-lookup"><span data-stu-id="86909-119">The possible values are specified in Table 2.</span></span>  <br/> |
   
<span data-ttu-id="86909-120">**Tabla 2. Valores de encabezado X-ClientCanHandle**</span><span class="sxs-lookup"><span data-stu-id="86909-120">**Table 2. X-ClientCanHandle header values**</span></span>

|<span data-ttu-id="86909-121">**Valor de X-ClientCanHandle (entre mayúsculas y minúsculas)**</span><span class="sxs-lookup"><span data-stu-id="86909-121">**X-ClientCanHandle value (case-insensitive)**</span></span>|<span data-ttu-id="86909-122">**Versión de servidor mínimo**</span><span class="sxs-lookup"><span data-stu-id="86909-122">**Minimum server version**</span></span>|<span data-ttu-id="86909-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="86909-123">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="86909-124">Negociar</span><span class="sxs-lookup"><span data-stu-id="86909-124">Negotiate</span></span>  <br/> |<span data-ttu-id="86909-125">15.00.0995.014</span><span class="sxs-lookup"><span data-stu-id="86909-125">15.00.0995.014</span></span>  <br/> |<span data-ttu-id="86909-126">Si este valor está presente, el servidor devolverá un valor de "Negotiate" en el elemento [AuthPackage (POX)](authpackage-pox.md) si el servidor está configurado para aceptar la autenticación Negotiate.</span><span class="sxs-lookup"><span data-stu-id="86909-126">If this value is present, the server will return a value of "Negotiate" in the [AuthPackage (POX)](authpackage-pox.md) element if the server is configured to accept Negotiate authentication.</span></span> <span data-ttu-id="86909-127">Si este valor no está presente, el servidor no devolverá un valor de "Negotiate" en el elemento **AuthPackage** .</span><span class="sxs-lookup"><span data-stu-id="86909-127">If this value is not present, the server will not return a value of "Negotiate" in the **AuthPackage** element.</span></span>  <br/> |
|<span data-ttu-id="86909-128">ExHttpInfo</span><span class="sxs-lookup"><span data-stu-id="86909-128">ExHttpInfo</span></span>  <br/> |<span data-ttu-id="86909-129">15.00.0995.014</span><span class="sxs-lookup"><span data-stu-id="86909-129">15.00.0995.014</span></span>  <br/> |<span data-ttu-id="86909-130">Si este valor está presente, el servidor devolverá un elemento de [Protocolo (POX)](protocol-pox.md) con un elemento de [Tipo (POX)](type-pox.md) se establece en "EXHTTP" si el servidor está configurado para aceptar conexiones RPC/HTTP.</span><span class="sxs-lookup"><span data-stu-id="86909-130">If this value is present, the server will return a [Protocol (POX)](protocol-pox.md) element with a [Type (POX)](type-pox.md) element set to "EXHTTP" if the server is configured to accept RPC/HTTP connections.</span></span> <span data-ttu-id="86909-131">Si este valor no está presente, el servidor no devolverá un elemento de **protocolo** con un elemento de **tipo** establecido en "EXHTTP".</span><span class="sxs-lookup"><span data-stu-id="86909-131">If this value is not present, the server will not return a **Protocol** element with a **Type** element set to "EXHTTP".</span></span>  <br/> |
   
### <a name="request-elements"></a><span data-ttu-id="86909-132">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="86909-132">Request elements</span></span>

<span data-ttu-id="86909-133">En el cuerpo de la solicitud se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="86909-133">The following elements are used in the request body:</span></span>
  
- [<span data-ttu-id="86909-134">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="86909-134">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
    
- [<span data-ttu-id="86909-135">Solicitud (POX)</span><span class="sxs-lookup"><span data-stu-id="86909-135">Request (POX)</span></span>](request-pox.md)
    
- [<span data-ttu-id="86909-136">AcceptableResponseSchema (POX)</span><span class="sxs-lookup"><span data-stu-id="86909-136">AcceptableResponseSchema (POX)</span></span>](acceptableresponseschema-pox.md)
    
- [<span data-ttu-id="86909-137">EMailAddress (POX)</span><span class="sxs-lookup"><span data-stu-id="86909-137">EMailAddress (POX)</span></span>](emailaddress-pox.md)
    
> [!NOTE]
> <span data-ttu-id="86909-138">El elemento [LegacyDN (POX)](legacydn-pox.md) puede utilizarse en lugar del elemento [EMailAddress (POX)](emailaddress-pox.md) .</span><span class="sxs-lookup"><span data-stu-id="86909-138">The [LegacyDN (POX)](legacydn-pox.md) element can be used in place of the [EMailAddress (POX)](emailaddress-pox.md) element.</span></span> 
  
### <a name="version-differences"></a><span data-ttu-id="86909-139">Diferencias de versión</span><span class="sxs-lookup"><span data-stu-id="86909-139">Version differences</span></span>

<span data-ttu-id="86909-140">El encabezado X-MapiHttpCapability está disponible en Office 365, Exchange Online, locales y en las versiones de Exchange comenzando por creación 15.00.0847.032 (Exchange Server 2013 SP1).</span><span class="sxs-lookup"><span data-stu-id="86909-140">The X-MapiHttpCapability header is available in Office 365, Exchange Online, and on-premises versions of Exchange starting with build 15.00.0847.032 (Exchange Server 2013 SP1).</span></span>
  
<span data-ttu-id="86909-141">El encabezado X-ClientCanHandle está disponible en Office 365, Exchange Online, locales y en versiones de Exchange inicio con compilación 15.00.0995.014.</span><span class="sxs-lookup"><span data-stu-id="86909-141">The X-ClientCanHandle header is available in Office 365, Exchange Online, and on-premises versions of Exchange starting with build 15.00.0995.014.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="86909-142">Ver también</span><span class="sxs-lookup"><span data-stu-id="86909-142">See also</span></span>



[<span data-ttu-id="86909-143">Respuesta de detección automática POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="86909-143">POX Autodiscover response for Exchange</span></span>](pox-autodiscover-response-for-exchange.md)


[<span data-ttu-id="86909-144">Referencia de servicio web POX de detección automática de Exchange</span><span class="sxs-lookup"><span data-stu-id="86909-144">POX Autodiscover web service reference for Exchange</span></span>](pox-autodiscover-web-service-reference-for-exchange.md)
  
[<span data-ttu-id="86909-145">Elementos de Autodiscover XML POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="86909-145">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

