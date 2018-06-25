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
description: El elemento de tipo identifica el tipo de la cuenta de correo configurada.
ms.openlocfilehash: 6e1349769c6a5349304f576419e0c609d3edd9a0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840735"
---
# <a name="type-pox"></a><span data-ttu-id="644eb-103">Tipo (POX)</span><span class="sxs-lookup"><span data-stu-id="644eb-103">Type (POX)</span></span>

<span data-ttu-id="644eb-104">El elemento de **tipo** identifica el tipo de la cuenta de correo configurada.</span><span class="sxs-lookup"><span data-stu-id="644eb-104">The **Type** element identifies the type of the configured mail account.</span></span> 
  
[<span data-ttu-id="644eb-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="644eb-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="644eb-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="644eb-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="644eb-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="644eb-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="644eb-108">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="644eb-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="644eb-109">Tipo (POX)</span><span class="sxs-lookup"><span data-stu-id="644eb-109">Type (POX)</span></span>](type-pox.md)
  
```XML
<Type>WEB or EXCH or EXPR or EXHTTP</Type>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="644eb-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="644eb-110">Attributes and elements</span></span>

<span data-ttu-id="644eb-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="644eb-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="644eb-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="644eb-112">Attributes</span></span>

<span data-ttu-id="644eb-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="644eb-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="644eb-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="644eb-114">Child elements</span></span>

<span data-ttu-id="644eb-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="644eb-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="644eb-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="644eb-116">Parent elements</span></span>

|<span data-ttu-id="644eb-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="644eb-117">**Element**</span></span>|<span data-ttu-id="644eb-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="644eb-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="644eb-119">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="644eb-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="644eb-120">Contiene las especificaciones para conectar a un cliente con el servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="644eb-120">Contains the specifications for connecting a client to the Exchange server.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="644eb-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="644eb-121">Text value</span></span>

<span data-ttu-id="644eb-122">El valor de texto representa el tipo de cuenta de correo.</span><span class="sxs-lookup"><span data-stu-id="644eb-122">The text value represents the type of mail account.</span></span> <span data-ttu-id="644eb-123">En la siguiente tabla se enumera los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="644eb-123">The following table lists the possible values.</span></span>
  
|<span data-ttu-id="644eb-124">**Valor**</span><span class="sxs-lookup"><span data-stu-id="644eb-124">**Value**</span></span>|<span data-ttu-id="644eb-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="644eb-125">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="644eb-126">EXCH</span><span class="sxs-lookup"><span data-stu-id="644eb-126">EXCH</span></span>  <br/> |<span data-ttu-id="644eb-127">El protocolo que se usa para conectarse al servidor es RPC de Exchange.</span><span class="sxs-lookup"><span data-stu-id="644eb-127">The protocol that is used to connect to the server is Exchange RPC.</span></span>  <br/> |
|<span data-ttu-id="644eb-128">EXHTTP</span><span class="sxs-lookup"><span data-stu-id="644eb-128">EXHTTP</span></span>  <br/> |<span data-ttu-id="644eb-129">El protocolo que se usa para conectarse a las conexiones RPC/HTTP del servidor.</span><span class="sxs-lookup"><span data-stu-id="644eb-129">The protocol that is used to connect to the server RPC/HTTP connections.</span></span>  <br/> |
|<span data-ttu-id="644eb-130">EXPR</span><span class="sxs-lookup"><span data-stu-id="644eb-130">EXPR</span></span>  <br/> |<span data-ttu-id="644eb-131">El protocolo que se usa para conectarse al servidor es RPC de Exchange a través de HTTP, utilizando un servidor proxy RPC.</span><span class="sxs-lookup"><span data-stu-id="644eb-131">The protocol that is used to connect to the server is Exchange RPC over HTTP, using an RPC proxy server.</span></span>  <br/> <span data-ttu-id="644eb-132">Esto solo es aplicable cuando el elemento [AccountType (POX)](accounttype-pox.md) está establecido en correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="644eb-132">This is only applicable when the [AccountType (POX)](accounttype-pox.md) element is set to email.</span></span>  <br/> |
|<span data-ttu-id="644eb-133">WEB</span><span class="sxs-lookup"><span data-stu-id="644eb-133">WEB</span></span>  <br/> |<span data-ttu-id="644eb-134">Correo electrónico se obtiene acceso desde un explorador Web mediante el uso de la dirección URL que se especifica en el elemento de [Servidor (POX)](server-pox.md) .</span><span class="sxs-lookup"><span data-stu-id="644eb-134">E-mail is accessed from a Web browser by using the URL that is specified in the [Server (POX)](server-pox.md) element.</span></span>  <br/> <span data-ttu-id="644eb-135">Esto solo es aplicable cuando el elemento [AccountType (POX)](accounttype-pox.md) está establecido en correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="644eb-135">This is only applicable when the [AccountType (POX)](accounttype-pox.md) element is set to email.</span></span>  <br/> |
   
### <a name="version-differences"></a><span data-ttu-id="644eb-136">Diferencias de versión</span><span class="sxs-lookup"><span data-stu-id="644eb-136">Version differences</span></span>

<span data-ttu-id="644eb-137">Office 365, Exchange Online y versiones locales de inicio de Exchange con creación 15.00.0995.014 devuelto un valor de "EXHTTP" sólo si el servidor está configurado para aceptar conexiones RPC/HTTP y el cliente incluye un encabezado [X-ClientCanHandle](pox-autodiscover-request-for-exchange.md) que contiene "ExHttpInfo".</span><span class="sxs-lookup"><span data-stu-id="644eb-137">Office 365, Exchange Online, and on-premises versions of Exchange starting with build 15.00.0995.014 return a value of "EXHTTP" only if the server is configured to accept RPC/HTTP connections and the client includes an [X-ClientCanHandle](pox-autodiscover-request-for-exchange.md) header that contains "ExHttpInfo".</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="644eb-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="644eb-138">See also</span></span>



[<span data-ttu-id="644eb-139">Elementos de Autodiscover XML POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="644eb-139">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

