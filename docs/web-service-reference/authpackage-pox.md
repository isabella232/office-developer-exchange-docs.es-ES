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
description: El elemento AuthPackage especifica el esquema de autenticación que se usa cuando se realiza en el servidor de Exchange que tenga instalado el rol de servidor de buzón de correo.
ms.openlocfilehash: 120ec00ac82166ae2002a8fbac0edf9a1e23afc7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763584"
---
# <a name="authpackage-pox"></a><span data-ttu-id="11a2a-103">AuthPackage (POX)</span><span class="sxs-lookup"><span data-stu-id="11a2a-103">AuthPackage (POX)</span></span>

<span data-ttu-id="11a2a-104">El elemento **AuthPackage** especifica el esquema de autenticación que se usa cuando se realiza en el servidor de Exchange que tenga instalado el rol de servidor de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="11a2a-104">The **AuthPackage** element specifies the authentication scheme that is used when authenticating against the Exchange server that has the Mailbox server role installed.</span></span> 
  
- [<span data-ttu-id="11a2a-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="11a2a-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
- [<span data-ttu-id="11a2a-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="11a2a-106">Response (POX)</span></span>](response-pox.md)
  
- [<span data-ttu-id="11a2a-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="11a2a-107">Account (POX)</span></span>](account-pox.md)
  
- [<span data-ttu-id="11a2a-108">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="11a2a-108">Protocol (POX)</span></span>](protocol-pox.md)
  
- [<span data-ttu-id="11a2a-109">AuthPackage (POX)</span><span class="sxs-lookup"><span data-stu-id="11a2a-109">AuthPackage (POX)</span></span>](authpackage-pox.md)
  
```xml
<AuthPackage>basic or kerb or kerbntlm or ntlm or certificate or negotiate or nego2</AuthPackage>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="11a2a-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="11a2a-110">Attributes and elements</span></span>

<span data-ttu-id="11a2a-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="11a2a-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="11a2a-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="11a2a-112">Attributes</span></span>

<span data-ttu-id="11a2a-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="11a2a-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="11a2a-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="11a2a-114">Child elements</span></span>

<span data-ttu-id="11a2a-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="11a2a-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="11a2a-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="11a2a-116">Parent elements</span></span>

|<span data-ttu-id="11a2a-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="11a2a-117">**Element**</span></span>|<span data-ttu-id="11a2a-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="11a2a-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="11a2a-119">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="11a2a-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="11a2a-120">Contiene las especificaciones para conectar a un cliente con el servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="11a2a-120">Contains the specifications for connecting a client to the Client Access server.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="11a2a-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="11a2a-121">Text value</span></span>

<span data-ttu-id="11a2a-122">El valor de texto especifica el esquema de autenticación que se usa cuando se realiza en el servidor de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="11a2a-122">The text value specifies the authentication scheme that is used when authenticating against the Mailbox server.</span></span> <span data-ttu-id="11a2a-123">Los valores posibles son:</span><span class="sxs-lookup"><span data-stu-id="11a2a-123">The following are the possible values:</span></span>
  
- <span data-ttu-id="11a2a-124">básica</span><span class="sxs-lookup"><span data-stu-id="11a2a-124">basic</span></span>
- <span data-ttu-id="11a2a-125">Kerbtray</span><span class="sxs-lookup"><span data-stu-id="11a2a-125">kerb</span></span>
- <span data-ttu-id="11a2a-126">kerbntlm</span><span class="sxs-lookup"><span data-stu-id="11a2a-126">kerbntlm</span></span>
- <span data-ttu-id="11a2a-127">NTLM</span><span class="sxs-lookup"><span data-stu-id="11a2a-127">ntlm</span></span>
- <span data-ttu-id="11a2a-128">certificado</span><span class="sxs-lookup"><span data-stu-id="11a2a-128">certificate</span></span>
- <span data-ttu-id="11a2a-129">negociar</span><span class="sxs-lookup"><span data-stu-id="11a2a-129">negotiate</span></span>
- <span data-ttu-id="11a2a-130">nego2</span><span class="sxs-lookup"><span data-stu-id="11a2a-130">nego2</span></span>
    
## <a name="remarks"></a><span data-ttu-id="11a2a-131">Notas</span><span class="sxs-lookup"><span data-stu-id="11a2a-131">Remarks</span></span>

<span data-ttu-id="11a2a-132">El elemento **AuthPackage** solo se usa cuando el elemento de [Tipo (POX)](type-pox.md) tiene un valor de texto de EXCH o EXPR.</span><span class="sxs-lookup"><span data-stu-id="11a2a-132">The **AuthPackage** element is only used when the [Type (POX)](type-pox.md) element has a text value of EXCH or EXPR.</span></span> 
  
### <a name="version-differences"></a><span data-ttu-id="11a2a-133">Diferencias de versión</span><span class="sxs-lookup"><span data-stu-id="11a2a-133">Version differences</span></span>

<span data-ttu-id="11a2a-134">Office 365, Exchange Online y versiones locales de inicio de Exchange con creación 15.00.0995.014 devuelto un valor de "negociar" sólo si el servidor está configurado para usar la autenticación Negotiate y el cliente incluye un encabezado [X-ClientCanHandle](pox-autodiscover-request-for-exchange.md) que contiene "Negotiate".</span><span class="sxs-lookup"><span data-stu-id="11a2a-134">Office 365, Exchange Online, and on-premises versions of Exchange starting with build 15.00.0995.014 return a value of "negotiate" only if the server is configured to use Negotiate authentication and the client includes a [X-ClientCanHandle](pox-autodiscover-request-for-exchange.md) header that contains "Negotiate".</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="11a2a-135">Ver también</span><span class="sxs-lookup"><span data-stu-id="11a2a-135">See also</span></span>

- [<span data-ttu-id="11a2a-136">Elementos de Autodiscover XML POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="11a2a-136">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

