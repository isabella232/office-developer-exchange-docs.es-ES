---
title: MailStore (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: af338f99-9e62-4124-9bff-8d7cc2008161
description: El elemento MailStore contiene las especificaciones para conectar un cliente al buzón de correo del usuario mediante el protocolo MAPI/HTTP.
ms.openlocfilehash: 635228fcfeb3ad791c845050b82666a6e060b229
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459794"
---
# <a name="mailstore-pox"></a><span data-ttu-id="02c62-103">MailStore (POX)</span><span class="sxs-lookup"><span data-stu-id="02c62-103">MailStore (POX)</span></span>

<span data-ttu-id="02c62-104">El elemento **MailStore** contiene las especificaciones para conectar un cliente al buzón de correo del usuario mediante el protocolo MAPI/http.</span><span class="sxs-lookup"><span data-stu-id="02c62-104">The **MailStore** element contains the specifications for connecting a client to the user's mailbox by using the MAPI/HTTP protocol.</span></span> 
  
[<span data-ttu-id="02c62-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="02c62-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="02c62-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="02c62-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="02c62-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="02c62-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="02c62-108">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="02c62-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="02c62-109">MailStore (POX)</span><span class="sxs-lookup"><span data-stu-id="02c62-109">MailStore (POX)</span></span>](mailstore-pox.md)
  
```XML
<MailStore>
   <ExternalUrl/>
   <InternalUrl/>
</MailStore>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="02c62-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="02c62-110">Attributes and elements</span></span>

<span data-ttu-id="02c62-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="02c62-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="02c62-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="02c62-112">Attributes</span></span>

<span data-ttu-id="02c62-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="02c62-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="02c62-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="02c62-114">Child elements</span></span>

|<span data-ttu-id="02c62-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="02c62-115">**Element**</span></span>|<span data-ttu-id="02c62-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="02c62-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="02c62-117">ExternalUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="02c62-117">ExternalUrl (POX)</span></span>](externalurl-pox.md) <br/> |<span data-ttu-id="02c62-118">Contiene la dirección URL que se debe usar para obtener acceso al buzón de correo del usuario desde fuera de la red de la organización por medio del protocolo MAPI/HTTP.</span><span class="sxs-lookup"><span data-stu-id="02c62-118">Contains the URL that should be used to access the user's mailbox from outside the organization's network by means of the MAPI/HTTP protocol.</span></span>  <br/> |
|[<span data-ttu-id="02c62-119">InternalUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="02c62-119">InternalUrl (POX)</span></span>](internalurl-pox.md) <br/> |<span data-ttu-id="02c62-120">Contiene la dirección URL que se debe usar para obtener acceso al buzón de correo del usuario desde dentro de la red de la organización por medio del protocolo MAPI/HTTP.</span><span class="sxs-lookup"><span data-stu-id="02c62-120">Contains the URL that should be used to access the user's mailbox from inside the organization's network by means of the MAPI/HTTP protocol.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="02c62-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="02c62-121">Parent elements</span></span>

|<span data-ttu-id="02c62-122">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="02c62-122">**Element**</span></span>|<span data-ttu-id="02c62-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="02c62-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="02c62-124">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="02c62-124">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="02c62-125">Contiene las especificaciones para conectar un cliente al servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="02c62-125">Contains the specifications for connecting a client to the Client Access server.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="02c62-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="02c62-126">Remarks</span></span>

<span data-ttu-id="02c62-127">El elemento **MailStore** está presente en una respuesta que tiene un elemento [Protocol (POX)](protocol-pox.md) con un valor de atributo de **tipo** de "mapiHttp".</span><span class="sxs-lookup"><span data-stu-id="02c62-127">The **MailStore** element is present in a response that has a [Protocol (POX)](protocol-pox.md) element with a **Type** attribute value of "mapiHttp".</span></span> 
  
<span data-ttu-id="02c62-128">El elemento **MailStore** está disponible para los clientes que implementan el protocolo MAPI/http y tienen como objetivo Exchange Online, Exchange online como parte de Office 365 y las versiones locales de Exchange que comienzan con la compilación 15.00.0847.032 (exchange Server 2013 SP1).</span><span class="sxs-lookup"><span data-stu-id="02c62-128">The **MailStore** element is available to clients that implement the MAPI/HTTP protocol and target Exchange Online, Exchange Online as part of Office 365, and on-premises versions of Exchange starting with build 15.00.0847.032 (Exchange Server 2013 SP1).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="02c62-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="02c62-129">See also</span></span>



[<span data-ttu-id="02c62-130">Elementos XML de detección automática de POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="02c62-130">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

