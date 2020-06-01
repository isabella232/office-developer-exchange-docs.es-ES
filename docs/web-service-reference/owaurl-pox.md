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
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457266"
---
# <a name="owaurl-pox"></a><span data-ttu-id="62712-103">OWAUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="62712-103">OWAUrl (POX)</span></span>

<span data-ttu-id="62712-104">El elemento **OWAUrl** describe la dirección URL y el esquema de autenticación que se usa para obtener acceso a un equipo concreto que ejecuta Microsoft Exchange Server 2007 que tiene instalada la función de servidor acceso de clientes que hospeda Outlook Web Access.</span><span class="sxs-lookup"><span data-stu-id="62712-104">The **OWAUrl** element describes the URL and authentication schema that is used to access a particular computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed that hosts Outlook Web Access.</span></span> 
  
[<span data-ttu-id="62712-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="62712-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="62712-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="62712-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="62712-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="62712-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="62712-108">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="62712-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="62712-109">Interno (POX)</span><span class="sxs-lookup"><span data-stu-id="62712-109">Internal (POX)</span></span>](internal-pox.md)
  
[<span data-ttu-id="62712-110">OWAUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="62712-110">OWAUrl (POX)</span></span>](owaurl-pox.md)
  
```xml
<OWAUrl AuthenticationMethod=""/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="62712-111">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="62712-111">Attributes and elements</span></span>

<span data-ttu-id="62712-112">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="62712-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="62712-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="62712-113">Attributes</span></span>

|<span data-ttu-id="62712-114">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="62712-114">**Attribute**</span></span>|<span data-ttu-id="62712-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="62712-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="62712-116">**AuthenticationMethod**</span><span class="sxs-lookup"><span data-stu-id="62712-116">**AuthenticationMethod**</span></span> <br/> |<span data-ttu-id="62712-117">Describe los métodos de autenticación para obtener acceso a Outlook Web Access.</span><span class="sxs-lookup"><span data-stu-id="62712-117">Describes the authentication methods for accessing Outlook Web Access.</span></span>  <br/> |
   
#### <a name="authenticationmethod-attribute"></a><span data-ttu-id="62712-118">Atributo AuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="62712-118">AuthenticationMethod Attribute</span></span>

|<span data-ttu-id="62712-119">**Valor**</span><span class="sxs-lookup"><span data-stu-id="62712-119">**Value**</span></span>|<span data-ttu-id="62712-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="62712-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="62712-121">WindowsIntegrated</span><span class="sxs-lookup"><span data-stu-id="62712-121">WindowsIntegrated</span></span>  <br/> |<span data-ttu-id="62712-122">Autenticación de Windows integrada.</span><span class="sxs-lookup"><span data-stu-id="62712-122">Integrated Windows authentication.</span></span>  <br/> |
|<span data-ttu-id="62712-123">FBA</span><span class="sxs-lookup"><span data-stu-id="62712-123">FBA</span></span>  <br/> |<span data-ttu-id="62712-124">Autenticación basada en formularios.</span><span class="sxs-lookup"><span data-stu-id="62712-124">Forms-based authentication.</span></span>  <br/> |
|<span data-ttu-id="62712-125">NTLM</span><span class="sxs-lookup"><span data-stu-id="62712-125">NTLM</span></span>  <br/> |<span data-ttu-id="62712-126">Autenticación NTLM.</span><span class="sxs-lookup"><span data-stu-id="62712-126">NTLM authentication.</span></span>  <br/> |
|<span data-ttu-id="62712-127">Digest</span><span class="sxs-lookup"><span data-stu-id="62712-127">Digest</span></span>  <br/> |<span data-ttu-id="62712-128">Autenticación implícita.</span><span class="sxs-lookup"><span data-stu-id="62712-128">Digest authentication.</span></span>  <br/> |
|<span data-ttu-id="62712-129">Básica</span><span class="sxs-lookup"><span data-stu-id="62712-129">Basic</span></span>  <br/> |<span data-ttu-id="62712-130">Autenticación básica.</span><span class="sxs-lookup"><span data-stu-id="62712-130">Basic authentication.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="62712-131">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="62712-131">Child elements</span></span>

<span data-ttu-id="62712-132">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="62712-132">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="62712-133">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="62712-133">Parent elements</span></span>

|<span data-ttu-id="62712-134">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="62712-134">**Element**</span></span>|<span data-ttu-id="62712-135">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="62712-135">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="62712-136">Interno (POX)</span><span class="sxs-lookup"><span data-stu-id="62712-136">Internal (POX)</span></span>](internal-pox.md) <br/> |<span data-ttu-id="62712-137">Contiene la colección de direcciones URL de Outlook Web Access a las que se puede conectar un cliente cuando está dentro del firewall.</span><span class="sxs-lookup"><span data-stu-id="62712-137">Contains the collection of Outlook Web Access URLs that a client can connect to when it is inside the firewall.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="62712-138">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="62712-138">Text value</span></span>

<span data-ttu-id="62712-139">El valor de texto representa la dirección URL del servicio de Outlook Web Access en un servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="62712-139">The text value represents the URL for the Outlook Web Access service on a Client Access server.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="62712-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="62712-140">See also</span></span>



[<span data-ttu-id="62712-141">Elementos XML de detección automática de POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="62712-141">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

