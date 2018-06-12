---
title: InternalUrl (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4649baa9-eec9-426d-952b-361818c25fe0
description: El elemento InternalUrl contiene la dirección URL para conectar a un cliente con el servidor de la libreta de direcciones o buzón de un usuario desde dentro de la organización del usuario mediante el protocolo HTTP/MAPI.
ms.openlocfilehash: 3823236081961128b31bb2c0f563062897c55814
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19835950"
---
# <a name="internalurl-pox"></a><span data-ttu-id="01a81-103">InternalUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="01a81-103">InternalUrl (POX)</span></span>

<span data-ttu-id="01a81-104">El elemento **InternalUrl** contiene la dirección URL para conectar a un cliente con el servidor de la libreta de direcciones o buzón de un usuario desde dentro de la organización del usuario mediante el protocolo HTTP/MAPI.</span><span class="sxs-lookup"><span data-stu-id="01a81-104">The **InternalUrl** element contains the URL for connecting a client to the address book server or a user's mailbox from inside the user's organization by using the MAPI/HTTP protocol.</span></span> 
  
```XML
<InternalUrl/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="01a81-105">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="01a81-105">Attributes and elements</span></span>

<span data-ttu-id="01a81-106">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="01a81-106">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="01a81-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="01a81-107">Attributes</span></span>

<span data-ttu-id="01a81-108">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="01a81-108">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="01a81-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="01a81-109">Child elements</span></span>

<span data-ttu-id="01a81-110">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="01a81-110">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="01a81-111">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="01a81-111">Parent elements</span></span>

|<span data-ttu-id="01a81-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="01a81-112">**Element**</span></span>|<span data-ttu-id="01a81-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="01a81-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="01a81-114">Libreta de direcciones (POX)</span><span class="sxs-lookup"><span data-stu-id="01a81-114">AddressBook (POX)</span></span>](addressbook-pox.md) <br/> |<span data-ttu-id="01a81-115">Contiene las especificaciones para conectar a un cliente con el servidor de la libreta de direcciones mediante el protocolo HTTP/MAPI.</span><span class="sxs-lookup"><span data-stu-id="01a81-115">Contains the specifications for connecting a client to the address book server by using the MAPI/HTTP protocol.</span></span>  <br/> |
|[<span data-ttu-id="01a81-116">Almacenamiento de correo (POX)</span><span class="sxs-lookup"><span data-stu-id="01a81-116">MailStore (POX)</span></span>](mailstore-pox.md) <br/> |<span data-ttu-id="01a81-117">Contiene las especificaciones para conectar a un cliente con el buzón del usuario mediante el protocolo HTTP/MAPI.</span><span class="sxs-lookup"><span data-stu-id="01a81-117">Contains the specifications for connecting a client to the user's mailbox by using the MAPI/HTTP protocol.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="01a81-118">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="01a81-118">Text value</span></span>

<span data-ttu-id="01a81-119">El valor de texto representa una dirección URL que se puede usar para tener acceso al buzón del usuario desde dentro de la organización del usuario o un servidor de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="01a81-119">The text value represents a URL that can be used to access an address book server or user's mailbox from inside the user's organization.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="01a81-120">Notas</span><span class="sxs-lookup"><span data-stu-id="01a81-120">Remarks</span></span>

<span data-ttu-id="01a81-121">El elemento **InternalUrl** puede estar presente en una respuesta que tiene un elemento de [Protocolo (POX)](protocol-pox.md) con un valor de atributo de **tipo** de "mapiHttp".</span><span class="sxs-lookup"><span data-stu-id="01a81-121">The **InternalUrl** element can be present in a response that has a [Protocol (POX)](protocol-pox.md) element with a **Type** attribute value of "mapiHttp".</span></span> 
  
<span data-ttu-id="01a81-122">El elemento **InternalUrl** está disponible para los clientes que implementan el protocolo HTTP/MAPI y destino Exchange Online, Exchange Online como parte de Office 365, y las versiones locales de Exchange a partir creación 15.00.0847.032 (Exchange Server 2013 SP1) .</span><span class="sxs-lookup"><span data-stu-id="01a81-122">The **InternalUrl** element is available to clients that implement the MAPI/HTTP protocol and target Exchange Online, Exchange Online as part of Office 365, and on-premises versions of Exchange starting with build 15.00.0847.032 (Exchange Server 2013 SP1).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="01a81-123">Ver también</span><span class="sxs-lookup"><span data-stu-id="01a81-123">See also</span></span>



[<span data-ttu-id="01a81-124">Elementos de Autodiscover XML POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="01a81-124">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

