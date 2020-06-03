---
title: AddressBook (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b2d62fd0-741c-4a41-9762-cc7d0ff01c9c
description: El elemento AddressBook contiene las especificaciones para conectar un cliente al servidor de libreta de direcciones mediante el protocolo MAPI/HTTP.
ms.openlocfilehash: 0967ac123cd3bb0086fd004ea0d0d37c08d2e037
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463639"
---
# <a name="addressbook-pox"></a><span data-ttu-id="01482-103">AddressBook (POX)</span><span class="sxs-lookup"><span data-stu-id="01482-103">AddressBook (POX)</span></span>

<span data-ttu-id="01482-104">El elemento **AddressBook** contiene las especificaciones para conectar un cliente al servidor de libreta de direcciones mediante el protocolo MAPI/http.</span><span class="sxs-lookup"><span data-stu-id="01482-104">The **AddressBook** element contains the specifications for connecting a client to the address book server by using the MAPI/HTTP protocol.</span></span> 
  
[<span data-ttu-id="01482-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="01482-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="01482-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="01482-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="01482-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="01482-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="01482-108">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="01482-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="01482-109">AddressBook (POX)</span><span class="sxs-lookup"><span data-stu-id="01482-109">AddressBook (POX)</span></span>](addressbook-pox.md)
  
```XML
<AddressBook>
   <ExternalUrl/>
   <InternalUrl/>
</AddressBook>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="01482-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="01482-110">Attributes and elements</span></span>

<span data-ttu-id="01482-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="01482-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="01482-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="01482-112">Attributes</span></span>

<span data-ttu-id="01482-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="01482-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="01482-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="01482-114">Child elements</span></span>

|<span data-ttu-id="01482-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="01482-115">**Element**</span></span>|<span data-ttu-id="01482-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="01482-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="01482-117">ExternalUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="01482-117">ExternalUrl (POX)</span></span>](externalurl-pox.md) <br/> |<span data-ttu-id="01482-118">Contiene la dirección URL que se debe usar para obtener acceso a la libreta de direcciones desde fuera de la red de la organización mediante el protocolo MAPI/HTTP.</span><span class="sxs-lookup"><span data-stu-id="01482-118">Contains the URL that should be used to access the address book from outside the organization's network by using the MAPI/HTTP protocol.</span></span>  <br/> |
|[<span data-ttu-id="01482-119">InternalUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="01482-119">InternalUrl (POX)</span></span>](internalurl-pox.md) <br/> |<span data-ttu-id="01482-120">Contiene la dirección URL que se debe usar para obtener acceso a la libreta de direcciones desde el interior de la red de la organización mediante el protocolo MAPI/HTTP.</span><span class="sxs-lookup"><span data-stu-id="01482-120">Contains the URL that should be used to access the address book from inside the organization's network by using the MAPI/HTTP protocol.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="01482-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="01482-121">Parent elements</span></span>

|<span data-ttu-id="01482-122">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="01482-122">**Element**</span></span>|<span data-ttu-id="01482-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="01482-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="01482-124">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="01482-124">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="01482-125">Contiene las especificaciones para conectar un cliente al servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="01482-125">Contains the specifications for connecting a client to the Client Access server.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="01482-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="01482-126">Remarks</span></span>

<span data-ttu-id="01482-127">El elemento **AddressBook** está presente en una respuesta que tiene un elemento [Protocol (POX)](protocol-pox.md) con un valor de atributo de **tipo** de "mapiHttp".</span><span class="sxs-lookup"><span data-stu-id="01482-127">The **AddressBook** element is present in a response that has a [Protocol (POX)](protocol-pox.md) element with a **Type** attribute value of "mapiHttp".</span></span> 
  
<span data-ttu-id="01482-128">El elemento **AddressBook** está disponible para clientes que implementan el protocolo MAPI/http y tienen como objetivo Exchange Online, Exchange online como parte de Office 365 y versiones locales de Exchange que comienzan con la compilación 15.00.0847.032 (Exchange Server 2013 SP1).</span><span class="sxs-lookup"><span data-stu-id="01482-128">The **AddressBook** element is available to clients that implement the MAPI/HTTP protocol and target Exchange Online, Exchange Online as part of Office 365, and on-premises versions of Exchange starting with build 15.00.0847.032 (Exchange Server 2013 SP1).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="01482-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="01482-129">See also</span></span>

- [<span data-ttu-id="01482-130">Elementos XML de detección automática de POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="01482-130">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

