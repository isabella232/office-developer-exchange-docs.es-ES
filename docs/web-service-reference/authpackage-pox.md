---
title: AuthPackage (POX)
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 709dbe53-6141-41f8-a2b9-a399bae47991
description: El elemento AuthPackage especifica el esquema de autenticación que se usa al autenticar en el servidor de Exchange que tiene instalado el rol de servidor buzón de correo.
ms.openlocfilehash: 5317cf49d354a558417829e1d1b5b67cd6874309
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459107"
---
# <a name="authpackage-pox"></a><span data-ttu-id="19c95-103">AuthPackage (POX)</span><span class="sxs-lookup"><span data-stu-id="19c95-103">AuthPackage (POX)</span></span>

<span data-ttu-id="19c95-104">El elemento **AuthPackage** especifica el esquema de autenticación que se usa al autenticar en el servidor de Exchange que tiene instalado el rol de servidor buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="19c95-104">The **AuthPackage** element specifies the authentication scheme that is used when authenticating against the Exchange server that has the Mailbox server role installed.</span></span> 
  
- [<span data-ttu-id="19c95-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="19c95-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
- [<span data-ttu-id="19c95-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="19c95-106">Response (POX)</span></span>](response-pox.md)
  
- [<span data-ttu-id="19c95-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="19c95-107">Account (POX)</span></span>](account-pox.md)
  
- [<span data-ttu-id="19c95-108">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="19c95-108">Protocol (POX)</span></span>](protocol-pox.md)
  
- [<span data-ttu-id="19c95-109">AuthPackage (POX)</span><span class="sxs-lookup"><span data-stu-id="19c95-109">AuthPackage (POX)</span></span>](authpackage-pox.md)
  
```xml
<AuthPackage>basic or kerb or kerbntlm or ntlm or certificate or negotiate or nego2</AuthPackage>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="19c95-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="19c95-110">Attributes and elements</span></span>

<span data-ttu-id="19c95-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="19c95-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="19c95-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="19c95-112">Attributes</span></span>

<span data-ttu-id="19c95-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="19c95-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="19c95-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="19c95-114">Child elements</span></span>

<span data-ttu-id="19c95-115">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="19c95-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="19c95-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="19c95-116">Parent elements</span></span>

|<span data-ttu-id="19c95-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="19c95-117">**Element**</span></span>|<span data-ttu-id="19c95-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="19c95-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="19c95-119">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="19c95-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="19c95-120">Contiene las especificaciones para conectar un cliente al servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="19c95-120">Contains the specifications for connecting a client to the Client Access server.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="19c95-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="19c95-121">Text value</span></span>

<span data-ttu-id="19c95-122">El valor de texto especifica el esquema de autenticación que se usa al autenticar en el servidor de buzones de correo.</span><span class="sxs-lookup"><span data-stu-id="19c95-122">The text value specifies the authentication scheme that is used when authenticating against the Mailbox server.</span></span> <span data-ttu-id="19c95-123">Los valores posibles son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="19c95-123">The following are the possible values:</span></span>
  
- <span data-ttu-id="19c95-124">elementos</span><span class="sxs-lookup"><span data-stu-id="19c95-124">basic</span></span>
- <span data-ttu-id="19c95-125">kerbtray</span><span class="sxs-lookup"><span data-stu-id="19c95-125">kerb</span></span>
- <span data-ttu-id="19c95-126">kerbntlm</span><span class="sxs-lookup"><span data-stu-id="19c95-126">kerbntlm</span></span>
- <span data-ttu-id="19c95-127">NTLM</span><span class="sxs-lookup"><span data-stu-id="19c95-127">ntlm</span></span>
- <span data-ttu-id="19c95-128">certificado</span><span class="sxs-lookup"><span data-stu-id="19c95-128">certificate</span></span>
- <span data-ttu-id="19c95-129">negociar</span><span class="sxs-lookup"><span data-stu-id="19c95-129">negotiate</span></span>
- <span data-ttu-id="19c95-130">nego2</span><span class="sxs-lookup"><span data-stu-id="19c95-130">nego2</span></span>
    
## <a name="remarks"></a><span data-ttu-id="19c95-131">Comentarios</span><span class="sxs-lookup"><span data-stu-id="19c95-131">Remarks</span></span>

<span data-ttu-id="19c95-132">El elemento **AuthPackage** solo se usa cuando el elemento [Type (POX)](type-pox.md) tiene un valor de texto de EXCH o expr.</span><span class="sxs-lookup"><span data-stu-id="19c95-132">The **AuthPackage** element is only used when the [Type (POX)](type-pox.md) element has a text value of EXCH or EXPR.</span></span> 
  
### <a name="version-differences"></a><span data-ttu-id="19c95-133">Diferencias de versión</span><span class="sxs-lookup"><span data-stu-id="19c95-133">Version differences</span></span>

<span data-ttu-id="19c95-134">Office 365, Exchange Online y versiones locales de Exchange que comienzan con la compilación 15.00.0995.014 devuelven un valor de "Negotiate" solo si el servidor está configurado para usar la autenticación Negotiate y el cliente incluye un encabezado [X-ClientCanHandle](pox-autodiscover-request-for-exchange.md) que contiene "Negotiate".</span><span class="sxs-lookup"><span data-stu-id="19c95-134">Office 365, Exchange Online, and on-premises versions of Exchange starting with build 15.00.0995.014 return a value of "negotiate" only if the server is configured to use Negotiate authentication and the client includes a [X-ClientCanHandle](pox-autodiscover-request-for-exchange.md) header that contains "Negotiate".</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="19c95-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="19c95-135">See also</span></span>

- [<span data-ttu-id="19c95-136">Elementos XML de detección automática de POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="19c95-136">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

