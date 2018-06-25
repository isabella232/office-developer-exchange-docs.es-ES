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
description: El elemento OWAUrl describe la dirección URL y el esquema de autenticación que se usa para tener acceso a un determinado equipo que ejecuta Microsoft Exchange Server 2007 que tiene el rol de servidor de acceso de cliente instalado que aloja Outlook Web Access.
ms.openlocfilehash: 93d03506e2a74aa1b4ef6d2a49ccbda01cfc1f9a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836673"
---
# <a name="owaurl-pox"></a><span data-ttu-id="af38e-103">OWAUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="af38e-103">OWAUrl (POX)</span></span>

<span data-ttu-id="af38e-104">El elemento **OWAUrl** describe la dirección URL y el esquema de autenticación que se usa para tener acceso a un determinado equipo que ejecuta Microsoft Exchange Server 2007 que tiene el rol de servidor de acceso de cliente instalado que aloja Outlook Web Access.</span><span class="sxs-lookup"><span data-stu-id="af38e-104">The **OWAUrl** element describes the URL and authentication schema that is used to access a particular computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed that hosts Outlook Web Access.</span></span> 
  
[<span data-ttu-id="af38e-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="af38e-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="af38e-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="af38e-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="af38e-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="af38e-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="af38e-108">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="af38e-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="af38e-109">Interno (POX)</span><span class="sxs-lookup"><span data-stu-id="af38e-109">Internal (POX)</span></span>](internal-pox.md)
  
[<span data-ttu-id="af38e-110">OWAUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="af38e-110">OWAUrl (POX)</span></span>](owaurl-pox.md)
  
```xml
<OWAUrl AuthenticationMethod=""/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="af38e-111">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="af38e-111">Attributes and elements</span></span>

<span data-ttu-id="af38e-112">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="af38e-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="af38e-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="af38e-113">Attributes</span></span>

|<span data-ttu-id="af38e-114">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="af38e-114">**Attribute**</span></span>|<span data-ttu-id="af38e-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="af38e-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="af38e-116">**AuthenticationMethod**</span><span class="sxs-lookup"><span data-stu-id="af38e-116">**AuthenticationMethod**</span></span> <br/> |<span data-ttu-id="af38e-117">Describe los métodos de autenticación para obtener acceso a Outlook Web Access.</span><span class="sxs-lookup"><span data-stu-id="af38e-117">Describes the authentication methods for accessing Outlook Web Access.</span></span>  <br/> |
   
#### <a name="authenticationmethod-attribute"></a><span data-ttu-id="af38e-118">Atributo AuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="af38e-118">AuthenticationMethod Attribute</span></span>

|<span data-ttu-id="af38e-119">**Valor**</span><span class="sxs-lookup"><span data-stu-id="af38e-119">**Value**</span></span>|<span data-ttu-id="af38e-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="af38e-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="af38e-121">WindowsIntegrated</span><span class="sxs-lookup"><span data-stu-id="af38e-121">WindowsIntegrated</span></span>  <br/> |<span data-ttu-id="af38e-122">Autenticación integrada de Windows.</span><span class="sxs-lookup"><span data-stu-id="af38e-122">Integrated Windows authentication.</span></span>  <br/> |
|<span data-ttu-id="af38e-123">FBA</span><span class="sxs-lookup"><span data-stu-id="af38e-123">FBA</span></span>  <br/> |<span data-ttu-id="af38e-124">Autenticación basada en formularios.</span><span class="sxs-lookup"><span data-stu-id="af38e-124">Forms-based authentication.</span></span>  <br/> |
|<span data-ttu-id="af38e-125">NTLM</span><span class="sxs-lookup"><span data-stu-id="af38e-125">NTLM</span></span>  <br/> |<span data-ttu-id="af38e-126">Autenticación NTLM.</span><span class="sxs-lookup"><span data-stu-id="af38e-126">NTLM authentication.</span></span>  <br/> |
|<span data-ttu-id="af38e-127">Implícita</span><span class="sxs-lookup"><span data-stu-id="af38e-127">Digest</span></span>  <br/> |<span data-ttu-id="af38e-128">Autenticación implícita.</span><span class="sxs-lookup"><span data-stu-id="af38e-128">Digest authentication.</span></span>  <br/> |
|<span data-ttu-id="af38e-129">Básica</span><span class="sxs-lookup"><span data-stu-id="af38e-129">Basic</span></span>  <br/> |<span data-ttu-id="af38e-130">Autenticación básica.</span><span class="sxs-lookup"><span data-stu-id="af38e-130">Basic authentication.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="af38e-131">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="af38e-131">Child elements</span></span>

<span data-ttu-id="af38e-132">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="af38e-132">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="af38e-133">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="af38e-133">Parent elements</span></span>

|<span data-ttu-id="af38e-134">**Element**</span><span class="sxs-lookup"><span data-stu-id="af38e-134">**Element**</span></span>|<span data-ttu-id="af38e-135">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="af38e-135">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="af38e-136">Interno (POX)</span><span class="sxs-lookup"><span data-stu-id="af38e-136">Internal (POX)</span></span>](internal-pox.md) <br/> |<span data-ttu-id="af38e-137">Contiene la colección de direcciones URL de Outlook Web Access que un cliente puede conectarse a cuando está dentro del firewall.</span><span class="sxs-lookup"><span data-stu-id="af38e-137">Contains the collection of Outlook Web Access URLs that a client can connect to when it is inside the firewall.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="af38e-138">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="af38e-138">Text value</span></span>

<span data-ttu-id="af38e-139">El valor de texto representa la dirección URL del servicio de Outlook Web Access en un servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="af38e-139">The text value represents the URL for the Outlook Web Access service on a Client Access server.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="af38e-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="af38e-140">See also</span></span>



[<span data-ttu-id="af38e-141">Elementos de Autodiscover XML POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="af38e-141">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

