---
title: Libreta de direcciones (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b2d62fd0-741c-4a41-9762-cc7d0ff01c9c
description: El elemento de la libreta de direcciones contiene las especificaciones para conectar a un cliente con el servidor de la libreta de direcciones mediante el protocolo HTTP/MAPI.
ms.openlocfilehash: c30f0ee7c36de7e63157d07d003a11187d661fd7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763411"
---
# <a name="addressbook-pox"></a><span data-ttu-id="8ef3b-103">Libreta de direcciones (POX)</span><span class="sxs-lookup"><span data-stu-id="8ef3b-103">AddressBook (POX)</span></span>

<span data-ttu-id="8ef3b-104">El elemento de la **Libreta de direcciones** contiene las especificaciones para conectar a un cliente con el servidor de la libreta de direcciones mediante el protocolo HTTP/MAPI.</span><span class="sxs-lookup"><span data-stu-id="8ef3b-104">The **AddressBook** element contains the specifications for connecting a client to the address book server by using the MAPI/HTTP protocol.</span></span> 
  
[<span data-ttu-id="8ef3b-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="8ef3b-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="8ef3b-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="8ef3b-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="8ef3b-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="8ef3b-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="8ef3b-108">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="8ef3b-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="8ef3b-109">Libreta de direcciones (POX)</span><span class="sxs-lookup"><span data-stu-id="8ef3b-109">AddressBook (POX)</span></span>](addressbook-pox.md)
  
```XML
<AddressBook>
   <ExternalUrl/>
   <InternalUrl/>
</AddressBook>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="8ef3b-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="8ef3b-110">Attributes and elements</span></span>

<span data-ttu-id="8ef3b-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="8ef3b-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8ef3b-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="8ef3b-112">Attributes</span></span>

<span data-ttu-id="8ef3b-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="8ef3b-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8ef3b-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8ef3b-114">Child elements</span></span>

|<span data-ttu-id="8ef3b-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="8ef3b-115">**Element**</span></span>|<span data-ttu-id="8ef3b-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8ef3b-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8ef3b-117">ExternalUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="8ef3b-117">ExternalUrl (POX)</span></span>](externalurl-pox.md) <br/> |<span data-ttu-id="8ef3b-118">Contiene la dirección URL que se debe utilizar para tener acceso a la libreta de direcciones desde fuera de la red de la organización mediante el protocolo HTTP/MAPI.</span><span class="sxs-lookup"><span data-stu-id="8ef3b-118">Contains the URL that should be used to access the address book from outside the organization's network by using the MAPI/HTTP protocol.</span></span>  <br/> |
|[<span data-ttu-id="8ef3b-119">InternalUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="8ef3b-119">InternalUrl (POX)</span></span>](internalurl-pox.md) <br/> |<span data-ttu-id="8ef3b-120">Contiene la dirección URL que se debe utilizar para tener acceso a la libreta de direcciones desde dentro de la red de la organización mediante el protocolo HTTP/MAPI.</span><span class="sxs-lookup"><span data-stu-id="8ef3b-120">Contains the URL that should be used to access the address book from inside the organization's network by using the MAPI/HTTP protocol.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8ef3b-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="8ef3b-121">Parent elements</span></span>

|<span data-ttu-id="8ef3b-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="8ef3b-122">**Element**</span></span>|<span data-ttu-id="8ef3b-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8ef3b-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8ef3b-124">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="8ef3b-124">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="8ef3b-125">Contiene las especificaciones para conectar a un cliente con el servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="8ef3b-125">Contains the specifications for connecting a client to the Client Access server.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8ef3b-126">Notas</span><span class="sxs-lookup"><span data-stu-id="8ef3b-126">Remarks</span></span>

<span data-ttu-id="8ef3b-127">El elemento de la **Libreta de direcciones** está presente en una respuesta que tiene un elemento de [Protocolo (POX)](protocol-pox.md) con un valor de atributo de **tipo** de "mapiHttp".</span><span class="sxs-lookup"><span data-stu-id="8ef3b-127">The **AddressBook** element is present in a response that has a [Protocol (POX)](protocol-pox.md) element with a **Type** attribute value of "mapiHttp".</span></span> 
  
<span data-ttu-id="8ef3b-128">El elemento de la **Libreta de direcciones** está disponible para los clientes que implementan el protocolo HTTP/MAPI y destino Exchange Online, Exchange Online como parte de Office 365, y las versiones locales de Exchange a partir creación 15.00.0847.032 (Exchange Server 2013 SP1) .</span><span class="sxs-lookup"><span data-stu-id="8ef3b-128">The **AddressBook** element is available to clients that implement the MAPI/HTTP protocol and target Exchange Online, Exchange Online as part of Office 365, and on-premises versions of Exchange starting with build 15.00.0847.032 (Exchange Server 2013 SP1).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8ef3b-129">Ver también</span><span class="sxs-lookup"><span data-stu-id="8ef3b-129">See also</span></span>

- [<span data-ttu-id="8ef3b-130">Elementos de Autodiscover XML POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="8ef3b-130">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

