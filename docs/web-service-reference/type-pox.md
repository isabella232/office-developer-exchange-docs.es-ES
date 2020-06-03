---
title: Tipo (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 9a627244-554f-4223-b9d8-a601b81a4a1a
description: El elemento Type identifica el tipo de cuenta de correo configurada.
ms.openlocfilehash: ad3570094ebe28498dfdc375cf7fc255434ba20d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465103"
---
# <a name="type-pox"></a><span data-ttu-id="f47c3-103">Tipo (POX)</span><span class="sxs-lookup"><span data-stu-id="f47c3-103">Type (POX)</span></span>

<span data-ttu-id="f47c3-104">El elemento **Type** identifica el tipo de cuenta de correo configurada.</span><span class="sxs-lookup"><span data-stu-id="f47c3-104">The **Type** element identifies the type of the configured mail account.</span></span> 
  
[<span data-ttu-id="f47c3-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="f47c3-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="f47c3-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="f47c3-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="f47c3-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="f47c3-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="f47c3-108">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="f47c3-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="f47c3-109">Tipo (POX)</span><span class="sxs-lookup"><span data-stu-id="f47c3-109">Type (POX)</span></span>](type-pox.md)
  
```XML
<Type>WEB or EXCH or EXPR or EXHTTP</Type>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="f47c3-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f47c3-110">Attributes and elements</span></span>

<span data-ttu-id="f47c3-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f47c3-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f47c3-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="f47c3-112">Attributes</span></span>

<span data-ttu-id="f47c3-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="f47c3-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f47c3-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f47c3-114">Child elements</span></span>

<span data-ttu-id="f47c3-115">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="f47c3-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f47c3-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f47c3-116">Parent elements</span></span>

|<span data-ttu-id="f47c3-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f47c3-117">**Element**</span></span>|<span data-ttu-id="f47c3-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f47c3-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f47c3-119">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="f47c3-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="f47c3-120">Contiene las especificaciones para conectar un cliente al servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="f47c3-120">Contains the specifications for connecting a client to the Exchange server.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f47c3-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="f47c3-121">Text value</span></span>

<span data-ttu-id="f47c3-122">El valor de texto representa el tipo de cuenta de correo.</span><span class="sxs-lookup"><span data-stu-id="f47c3-122">The text value represents the type of mail account.</span></span> <span data-ttu-id="f47c3-123">En la siguiente tabla se enumeran los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="f47c3-123">The following table lists the possible values.</span></span>
  
|<span data-ttu-id="f47c3-124">**Valor**</span><span class="sxs-lookup"><span data-stu-id="f47c3-124">**Value**</span></span>|<span data-ttu-id="f47c3-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f47c3-125">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f47c3-126">EXCH</span><span class="sxs-lookup"><span data-stu-id="f47c3-126">EXCH</span></span>  <br/> |<span data-ttu-id="f47c3-127">El protocolo que se usa para conectarse al servidor es RPC de Exchange.</span><span class="sxs-lookup"><span data-stu-id="f47c3-127">The protocol that is used to connect to the server is Exchange RPC.</span></span>  <br/> |
|<span data-ttu-id="f47c3-128">Exhttp</span><span class="sxs-lookup"><span data-stu-id="f47c3-128">EXHTTP</span></span>  <br/> |<span data-ttu-id="f47c3-129">Protocolo que se usa para conectarse a las conexiones RPC/HTTP del servidor.</span><span class="sxs-lookup"><span data-stu-id="f47c3-129">The protocol that is used to connect to the server RPC/HTTP connections.</span></span>  <br/> |
|<span data-ttu-id="f47c3-130">EXPRESIÓN</span><span class="sxs-lookup"><span data-stu-id="f47c3-130">EXPR</span></span>  <br/> |<span data-ttu-id="f47c3-131">El protocolo que se usa para conectarse al servidor es Exchange RPC sobre HTTP, mediante un servidor proxy RPC.</span><span class="sxs-lookup"><span data-stu-id="f47c3-131">The protocol that is used to connect to the server is Exchange RPC over HTTP, using an RPC proxy server.</span></span>  <br/> <span data-ttu-id="f47c3-132">Esto solo es aplicable cuando el elemento [AccountType (POX)](accounttype-pox.md) se establece en email.</span><span class="sxs-lookup"><span data-stu-id="f47c3-132">This is only applicable when the [AccountType (POX)](accounttype-pox.md) element is set to email.</span></span>  <br/> |
|<span data-ttu-id="f47c3-133">WEB</span><span class="sxs-lookup"><span data-stu-id="f47c3-133">WEB</span></span>  <br/> |<span data-ttu-id="f47c3-134">Se obtiene acceso al correo electrónico desde un explorador Web con la dirección URL especificada en el elemento [servidor (POX)](server-pox.md) .</span><span class="sxs-lookup"><span data-stu-id="f47c3-134">E-mail is accessed from a Web browser by using the URL that is specified in the [Server (POX)](server-pox.md) element.</span></span>  <br/> <span data-ttu-id="f47c3-135">Esto solo es aplicable cuando el elemento [AccountType (POX)](accounttype-pox.md) se establece en email.</span><span class="sxs-lookup"><span data-stu-id="f47c3-135">This is only applicable when the [AccountType (POX)](accounttype-pox.md) element is set to email.</span></span>  <br/> |
   
### <a name="version-differences"></a><span data-ttu-id="f47c3-136">Diferencias de versión</span><span class="sxs-lookup"><span data-stu-id="f47c3-136">Version differences</span></span>

<span data-ttu-id="f47c3-137">Office 365, Exchange Online y versiones locales de Exchange que comienzan con la compilación 15.00.0995.014 devuelven un valor de "exhttp" solo si el servidor está configurado para aceptar conexiones RPC/HTTP y el cliente incluye un encabezado [X-ClientCanHandle](pox-autodiscover-request-for-exchange.md) que contiene "ExHttpInfo".</span><span class="sxs-lookup"><span data-stu-id="f47c3-137">Office 365, Exchange Online, and on-premises versions of Exchange starting with build 15.00.0995.014 return a value of "EXHTTP" only if the server is configured to accept RPC/HTTP connections and the client includes an [X-ClientCanHandle](pox-autodiscover-request-for-exchange.md) header that contains "ExHttpInfo".</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f47c3-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="f47c3-138">See also</span></span>



[<span data-ttu-id="f47c3-139">Elementos XML de detección automática de POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="f47c3-139">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

