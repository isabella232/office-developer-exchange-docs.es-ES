---
title: OWAUrl (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 450b86a1-1722-49f5-b541-16c1edc3db7a
description: El elemento OWAUrl describe la dirección URL y el esquema de autenticación que se usa para obtener acceso a un equipo concreto que ejecuta Microsoft Exchange Server 2007 que tiene instalada la función de servidor acceso de clientes que hospeda Outlook Web Access.
ms.openlocfilehash: c0728af063cfbf1353eb7d3b81f5fcfe8b398f7d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457266"
---
# <a name="owaurl-pox"></a><span data-ttu-id="a0fc3-103">OWAUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="a0fc3-103">OWAUrl (POX)</span></span>

<span data-ttu-id="a0fc3-104">El elemento **OWAUrl** describe la dirección URL y el esquema de autenticación que se usa para obtener acceso a un equipo concreto que ejecuta Microsoft Exchange Server 2007 que tiene instalada la función de servidor acceso de clientes que hospeda Outlook Web Access.</span><span class="sxs-lookup"><span data-stu-id="a0fc3-104">The **OWAUrl** element describes the URL and authentication schema that is used to access a particular computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed that hosts Outlook Web Access.</span></span> 
  
[<span data-ttu-id="a0fc3-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="a0fc3-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="a0fc3-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="a0fc3-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="a0fc3-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="a0fc3-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="a0fc3-108">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="a0fc3-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="a0fc3-109">Interno (POX)</span><span class="sxs-lookup"><span data-stu-id="a0fc3-109">Internal (POX)</span></span>](internal-pox.md)
  
[<span data-ttu-id="a0fc3-110">OWAUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="a0fc3-110">OWAUrl (POX)</span></span>](owaurl-pox.md)
  
```xml
<OWAUrl AuthenticationMethod=""/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="a0fc3-111">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a0fc3-111">Attributes and elements</span></span>

<span data-ttu-id="a0fc3-112">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a0fc3-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a0fc3-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="a0fc3-113">Attributes</span></span>

|<span data-ttu-id="a0fc3-114">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="a0fc3-114">**Attribute**</span></span>|<span data-ttu-id="a0fc3-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a0fc3-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a0fc3-116">**AuthenticationMethod**</span><span class="sxs-lookup"><span data-stu-id="a0fc3-116">**AuthenticationMethod**</span></span> <br/> |<span data-ttu-id="a0fc3-117">Describe los métodos de autenticación para obtener acceso a Outlook Web Access.</span><span class="sxs-lookup"><span data-stu-id="a0fc3-117">Describes the authentication methods for accessing Outlook Web Access.</span></span>  <br/> |
   
#### <a name="authenticationmethod-attribute"></a><span data-ttu-id="a0fc3-118">Atributo AuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="a0fc3-118">AuthenticationMethod Attribute</span></span>

|<span data-ttu-id="a0fc3-119">**Valor**</span><span class="sxs-lookup"><span data-stu-id="a0fc3-119">**Value**</span></span>|<span data-ttu-id="a0fc3-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a0fc3-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a0fc3-121">WindowsIntegrated</span><span class="sxs-lookup"><span data-stu-id="a0fc3-121">WindowsIntegrated</span></span>  <br/> |<span data-ttu-id="a0fc3-122">Autenticación de Windows integrada.</span><span class="sxs-lookup"><span data-stu-id="a0fc3-122">Integrated Windows authentication.</span></span>  <br/> |
|<span data-ttu-id="a0fc3-123">FBA</span><span class="sxs-lookup"><span data-stu-id="a0fc3-123">FBA</span></span>  <br/> |<span data-ttu-id="a0fc3-124">Autenticación basada en formularios.</span><span class="sxs-lookup"><span data-stu-id="a0fc3-124">Forms-based authentication.</span></span>  <br/> |
|<span data-ttu-id="a0fc3-125">NTLM</span><span class="sxs-lookup"><span data-stu-id="a0fc3-125">NTLM</span></span>  <br/> |<span data-ttu-id="a0fc3-126">Autenticación NTLM.</span><span class="sxs-lookup"><span data-stu-id="a0fc3-126">NTLM authentication.</span></span>  <br/> |
|<span data-ttu-id="a0fc3-127">Digest</span><span class="sxs-lookup"><span data-stu-id="a0fc3-127">Digest</span></span>  <br/> |<span data-ttu-id="a0fc3-128">Autenticación implícita.</span><span class="sxs-lookup"><span data-stu-id="a0fc3-128">Digest authentication.</span></span>  <br/> |
|<span data-ttu-id="a0fc3-129">Básica</span><span class="sxs-lookup"><span data-stu-id="a0fc3-129">Basic</span></span>  <br/> |<span data-ttu-id="a0fc3-130">Autenticación básica.</span><span class="sxs-lookup"><span data-stu-id="a0fc3-130">Basic authentication.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a0fc3-131">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a0fc3-131">Child elements</span></span>

<span data-ttu-id="a0fc3-132">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="a0fc3-132">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a0fc3-133">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a0fc3-133">Parent elements</span></span>

|<span data-ttu-id="a0fc3-134">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a0fc3-134">**Element**</span></span>|<span data-ttu-id="a0fc3-135">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a0fc3-135">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a0fc3-136">Interno (POX)</span><span class="sxs-lookup"><span data-stu-id="a0fc3-136">Internal (POX)</span></span>](internal-pox.md) <br/> |<span data-ttu-id="a0fc3-137">Contiene la colección de direcciones URL de Outlook Web Access a las que se puede conectar un cliente cuando está dentro del firewall.</span><span class="sxs-lookup"><span data-stu-id="a0fc3-137">Contains the collection of Outlook Web Access URLs that a client can connect to when it is inside the firewall.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a0fc3-138">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="a0fc3-138">Text value</span></span>

<span data-ttu-id="a0fc3-139">El valor de texto representa la dirección URL del servicio de Outlook Web Access en un servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="a0fc3-139">The text value represents the URL for the Outlook Web Access service on a Client Access server.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a0fc3-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="a0fc3-140">See also</span></span>



[<span data-ttu-id="a0fc3-141">Elementos XML de detección automática de POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="a0fc3-141">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

