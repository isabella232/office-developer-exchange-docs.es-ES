---
title: Almacenamiento de correo (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: af338f99-9e62-4124-9bff-8d7cc2008161
description: El elemento de almacenamiento de correo contiene las especificaciones para conectar a un cliente con el buzón del usuario mediante el protocolo HTTP/MAPI.
ms.openlocfilehash: 4c82c7b61752cf7d91287a3968f6c642f4943855
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836301"
---
# <a name="mailstore-pox"></a><span data-ttu-id="a8840-103">Almacenamiento de correo (POX)</span><span class="sxs-lookup"><span data-stu-id="a8840-103">MailStore (POX)</span></span>

<span data-ttu-id="a8840-104">El elemento de **almacenamiento de correo** contiene las especificaciones para conectar a un cliente con el buzón del usuario mediante el protocolo HTTP/MAPI.</span><span class="sxs-lookup"><span data-stu-id="a8840-104">The **MailStore** element contains the specifications for connecting a client to the user's mailbox by using the MAPI/HTTP protocol.</span></span> 
  
[<span data-ttu-id="a8840-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="a8840-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="a8840-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="a8840-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="a8840-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="a8840-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="a8840-108">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="a8840-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="a8840-109">Almacenamiento de correo (POX)</span><span class="sxs-lookup"><span data-stu-id="a8840-109">MailStore (POX)</span></span>](mailstore-pox.md)
  
```XML
<MailStore>
   <ExternalUrl/>
   <InternalUrl/>
</MailStore>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="a8840-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a8840-110">Attributes and elements</span></span>

<span data-ttu-id="a8840-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a8840-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a8840-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="a8840-112">Attributes</span></span>

<span data-ttu-id="a8840-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a8840-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a8840-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a8840-114">Child elements</span></span>

|<span data-ttu-id="a8840-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="a8840-115">**Element**</span></span>|<span data-ttu-id="a8840-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a8840-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a8840-117">ExternalUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="a8840-117">ExternalUrl (POX)</span></span>](externalurl-pox.md) <br/> |<span data-ttu-id="a8840-118">Contiene la dirección URL que se debe utilizar para tener acceso al buzón del usuario desde fuera de la red de la organización por medio del protocolo HTTP/MAPI.</span><span class="sxs-lookup"><span data-stu-id="a8840-118">Contains the URL that should be used to access the user's mailbox from outside the organization's network by means of the MAPI/HTTP protocol.</span></span>  <br/> |
|[<span data-ttu-id="a8840-119">InternalUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="a8840-119">InternalUrl (POX)</span></span>](internalurl-pox.md) <br/> |<span data-ttu-id="a8840-120">Contiene la dirección URL que se debe utilizar para tener acceso al buzón del usuario desde dentro de la red de la organización por medio del protocolo HTTP/MAPI.</span><span class="sxs-lookup"><span data-stu-id="a8840-120">Contains the URL that should be used to access the user's mailbox from inside the organization's network by means of the MAPI/HTTP protocol.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a8840-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a8840-121">Parent elements</span></span>

|<span data-ttu-id="a8840-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="a8840-122">**Element**</span></span>|<span data-ttu-id="a8840-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a8840-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a8840-124">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="a8840-124">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="a8840-125">Contiene las especificaciones para conectar a un cliente con el servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="a8840-125">Contains the specifications for connecting a client to the Client Access server.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a8840-126">Notas</span><span class="sxs-lookup"><span data-stu-id="a8840-126">Remarks</span></span>

<span data-ttu-id="a8840-127">El elemento de **almacenamiento de correo** está presente en una respuesta que tiene un elemento de [Protocolo (POX)](protocol-pox.md) con un valor de atributo de **tipo** de "mapiHttp".</span><span class="sxs-lookup"><span data-stu-id="a8840-127">The **MailStore** element is present in a response that has a [Protocol (POX)](protocol-pox.md) element with a **Type** attribute value of "mapiHttp".</span></span> 
  
<span data-ttu-id="a8840-128">El elemento de **almacenamiento de correo** está disponible para los clientes que implementan el protocolo HTTP/MAPI y destino Exchange Online, Exchange Online como parte de Office 365, y las versiones locales de Exchange a partir creación 15.00.0847.032 (Exchange Server 2013 SP1).</span><span class="sxs-lookup"><span data-stu-id="a8840-128">The **MailStore** element is available to clients that implement the MAPI/HTTP protocol and target Exchange Online, Exchange Online as part of Office 365, and on-premises versions of Exchange starting with build 15.00.0847.032 (Exchange Server 2013 SP1).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a8840-129">Ver también</span><span class="sxs-lookup"><span data-stu-id="a8840-129">See also</span></span>



[<span data-ttu-id="a8840-130">Elementos de Autodiscover XML POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="a8840-130">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

