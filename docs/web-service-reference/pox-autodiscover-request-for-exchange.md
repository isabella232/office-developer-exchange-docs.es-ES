---
title: Solicitud de detección automática de POX para Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 75671b1d-f35b-497b-8d8c-706f3f2535fd
description: La solicitud de detección automática contiene una consulta para la configuración de acceso de cliente de un usuario.
ms.openlocfilehash: b2138f9813c7b75aef9afb90089b9b874aac7532
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461670"
---
# <a name="pox-autodiscover-request-for-exchange"></a><span data-ttu-id="8781e-103">Solicitud de detección automática de POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="8781e-103">POX Autodiscover request for Exchange</span></span>

<span data-ttu-id="8781e-104">La solicitud de detección automática contiene una consulta para la configuración de acceso de cliente de un usuario.</span><span class="sxs-lookup"><span data-stu-id="8781e-104">The Autodiscover request contains a query for a user's client access configuration.</span></span>
  
## <a name="autodiscover-request-example"></a><span data-ttu-id="8781e-105">Ejemplo de solicitud de detección automática</span><span class="sxs-lookup"><span data-stu-id="8781e-105">Autodiscover request example</span></span>

### <a name="description"></a><span data-ttu-id="8781e-106">Description</span><span class="sxs-lookup"><span data-stu-id="8781e-106">Description</span></span>

<span data-ttu-id="8781e-107">El siguiente ejemplo de XML muestra un cuerpo de solicitud de detección automática.</span><span class="sxs-lookup"><span data-stu-id="8781e-107">The following XML example shows an Autodiscover request body.</span></span>
  
### <a name="code"></a><span data-ttu-id="8781e-108">Código</span><span class="sxs-lookup"><span data-stu-id="8781e-108">Code</span></span>

```XML
<Autodiscover xmlns="https://schemas.microsoft.com/exchange/autodiscover/outlook/requestschema/2006">
   <Request>
     <EMailAddress>user@contoso.com</EMailAddress>
     <AcceptableResponseSchema>https://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a</AcceptableResponseSchema>
   </Request>
 </Autodiscover>
```

### <a name="request-headers"></a><span data-ttu-id="8781e-109">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8781e-109">Request Headers</span></span>

<span data-ttu-id="8781e-110">Los siguientes encabezados HTTP son opcionales al enviar solicitudes de detección automática.</span><span class="sxs-lookup"><span data-stu-id="8781e-110">The following HTTP headers are optional when sending Autodiscover requests.</span></span>
  
<span data-ttu-id="8781e-111">**Tabla 1. Encabezados de solicitud HTTP**</span><span class="sxs-lookup"><span data-stu-id="8781e-111">**Table 1. HTTP request headers**</span></span>

|<span data-ttu-id="8781e-112">**Header**</span><span class="sxs-lookup"><span data-stu-id="8781e-112">**Header**</span></span>|<span data-ttu-id="8781e-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8781e-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8781e-114">X-MapiHttpCapability</span><span class="sxs-lookup"><span data-stu-id="8781e-114">X-MapiHttpCapability</span></span>  <br/> |<span data-ttu-id="8781e-115">Si está presente y se establece en "1", indica que el cliente está solicitando información que se puede usar para conectarse al servidor mediante el protocolo MAPI/HTTP.</span><span class="sxs-lookup"><span data-stu-id="8781e-115">If present and set to "1", indicates that the client is requesting information that can be used to connect to the server by using the MAPI/HTTP protocol.</span></span> <span data-ttu-id="8781e-116">Este encabezado se aplica a los clientes que implementan el protocolo MAPI/HTTP.</span><span class="sxs-lookup"><span data-stu-id="8781e-116">This header is applicable to clients that implement the MAPI/HTTP protocol.</span></span>  <br/> |
|<span data-ttu-id="8781e-117">X-ClientCanHandle</span><span class="sxs-lookup"><span data-stu-id="8781e-117">X-ClientCanHandle</span></span>  <br/> |<span data-ttu-id="8781e-118">Este encabezado contiene una lista delimitada por comas de las funciones que admite el cliente.</span><span class="sxs-lookup"><span data-stu-id="8781e-118">This header contains a comma-delimited list of capabilities that the client supports.</span></span> <span data-ttu-id="8781e-119">Los valores posibles se especifican en la tabla 2.</span><span class="sxs-lookup"><span data-stu-id="8781e-119">The possible values are specified in Table 2.</span></span>  <br/> |
   
<span data-ttu-id="8781e-120">**Tabla 2. Valores del encabezado X-ClientCanHandle**</span><span class="sxs-lookup"><span data-stu-id="8781e-120">**Table 2. X-ClientCanHandle header values**</span></span>

|<span data-ttu-id="8781e-121">**Valor X-ClientCanHandle (sin distinción entre mayúsculas y minúsculas)**</span><span class="sxs-lookup"><span data-stu-id="8781e-121">**X-ClientCanHandle value (case-insensitive)**</span></span>|<span data-ttu-id="8781e-122">**Versión mínima del servidor**</span><span class="sxs-lookup"><span data-stu-id="8781e-122">**Minimum server version**</span></span>|<span data-ttu-id="8781e-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8781e-123">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8781e-124">Negociar</span><span class="sxs-lookup"><span data-stu-id="8781e-124">Negotiate</span></span>  <br/> |<span data-ttu-id="8781e-125">15.00.0995.014</span><span class="sxs-lookup"><span data-stu-id="8781e-125">15.00.0995.014</span></span>  <br/> |<span data-ttu-id="8781e-126">Si este valor está presente, el servidor devolverá un valor de "Negotiate" en el elemento [AuthPackage (POX)](authpackage-pox.md) si el servidor está configurado para aceptar la autenticación Negotiate.</span><span class="sxs-lookup"><span data-stu-id="8781e-126">If this value is present, the server will return a value of "Negotiate" in the [AuthPackage (POX)](authpackage-pox.md) element if the server is configured to accept Negotiate authentication.</span></span> <span data-ttu-id="8781e-127">Si este valor no está presente, el servidor no devolverá un valor de "Negotiate" en el elemento **AuthPackage** .</span><span class="sxs-lookup"><span data-stu-id="8781e-127">If this value is not present, the server will not return a value of "Negotiate" in the **AuthPackage** element.</span></span>  <br/> |
|<span data-ttu-id="8781e-128">ExHttpInfo</span><span class="sxs-lookup"><span data-stu-id="8781e-128">ExHttpInfo</span></span>  <br/> |<span data-ttu-id="8781e-129">15.00.0995.014</span><span class="sxs-lookup"><span data-stu-id="8781e-129">15.00.0995.014</span></span>  <br/> |<span data-ttu-id="8781e-130">Si este valor está presente, el servidor devolverá un elemento de [Protocolo (POX)](protocol-pox.md) con un elemento [Type (POX)](type-pox.md) establecido en "exhttp" si el servidor está configurado para aceptar conexiones RPC/HTTP.</span><span class="sxs-lookup"><span data-stu-id="8781e-130">If this value is present, the server will return a [Protocol (POX)](protocol-pox.md) element with a [Type (POX)](type-pox.md) element set to "EXHTTP" if the server is configured to accept RPC/HTTP connections.</span></span> <span data-ttu-id="8781e-131">Si este valor no está presente, el servidor no devolverá un elemento **Protocol** con un elemento **Type** establecido en "exhttp".</span><span class="sxs-lookup"><span data-stu-id="8781e-131">If this value is not present, the server will not return a **Protocol** element with a **Type** element set to "EXHTTP".</span></span>  <br/> |
   
### <a name="request-elements"></a><span data-ttu-id="8781e-132">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="8781e-132">Request elements</span></span>

<span data-ttu-id="8781e-133">Los siguientes elementos se usan en el cuerpo de la solicitud:</span><span class="sxs-lookup"><span data-stu-id="8781e-133">The following elements are used in the request body:</span></span>
  
- [<span data-ttu-id="8781e-134">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="8781e-134">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
    
- [<span data-ttu-id="8781e-135">Solicitud (POX)</span><span class="sxs-lookup"><span data-stu-id="8781e-135">Request (POX)</span></span>](request-pox.md)
    
- [<span data-ttu-id="8781e-136">AcceptableResponseSchema (POX)</span><span class="sxs-lookup"><span data-stu-id="8781e-136">AcceptableResponseSchema (POX)</span></span>](acceptableresponseschema-pox.md)
    
- [<span data-ttu-id="8781e-137">EMailAddress (POX)</span><span class="sxs-lookup"><span data-stu-id="8781e-137">EMailAddress (POX)</span></span>](emailaddress-pox.md)
    
> [!NOTE]
> <span data-ttu-id="8781e-138">El elemento [LegacyDN (POX)](legacydn-pox.md) se puede usar en vez del elemento [EmailAddress (POX)](emailaddress-pox.md) .</span><span class="sxs-lookup"><span data-stu-id="8781e-138">The [LegacyDN (POX)](legacydn-pox.md) element can be used in place of the [EMailAddress (POX)](emailaddress-pox.md) element.</span></span> 
  
### <a name="version-differences"></a><span data-ttu-id="8781e-139">Diferencias de versión</span><span class="sxs-lookup"><span data-stu-id="8781e-139">Version differences</span></span>

<span data-ttu-id="8781e-140">El encabezado X-MapiHttpCapability está disponible en Office 365, Exchange Online y las versiones locales de Exchange a partir de la compilación 15.00.0847.032 (Exchange Server 2013 SP1).</span><span class="sxs-lookup"><span data-stu-id="8781e-140">The X-MapiHttpCapability header is available in Office 365, Exchange Online, and on-premises versions of Exchange starting with build 15.00.0847.032 (Exchange Server 2013 SP1).</span></span>
  
<span data-ttu-id="8781e-141">El encabezado X-ClientCanHandle está disponible en Office 365, Exchange Online y las versiones locales de Exchange a partir de la compilación 15.00.0995.014.</span><span class="sxs-lookup"><span data-stu-id="8781e-141">The X-ClientCanHandle header is available in Office 365, Exchange Online, and on-premises versions of Exchange starting with build 15.00.0995.014.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8781e-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="8781e-142">See also</span></span>



[<span data-ttu-id="8781e-143">Respuesta de detección automática de POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="8781e-143">POX Autodiscover response for Exchange</span></span>](pox-autodiscover-response-for-exchange.md)


[<span data-ttu-id="8781e-144">Referencia de servicio Web de detección automática de POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="8781e-144">POX Autodiscover web service reference for Exchange</span></span>](pox-autodiscover-web-service-reference-for-exchange.md)
  
[<span data-ttu-id="8781e-145">Elementos XML de detección automática de POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="8781e-145">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

