---
title: InternalUrl (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4649baa9-eec9-426d-952b-361818c25fe0
description: El elemento InternalUrl contiene la dirección URL para conectar un cliente al servidor de la libreta de direcciones o al buzón de un usuario desde dentro de la organización del usuario mediante el protocolo MAPI/HTTP.
ms.openlocfilehash: 9c6ba621a681ec54d88089de6b7ae1eefdebc679
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465579"
---
# <a name="internalurl-pox"></a><span data-ttu-id="b357e-103">InternalUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="b357e-103">InternalUrl (POX)</span></span>

<span data-ttu-id="b357e-104">El elemento **InternalUrl** contiene la dirección URL para conectar un cliente al servidor de la libreta de direcciones o al buzón de un usuario desde dentro de la organización del usuario mediante el protocolo MAPI/http.</span><span class="sxs-lookup"><span data-stu-id="b357e-104">The **InternalUrl** element contains the URL for connecting a client to the address book server or a user's mailbox from inside the user's organization by using the MAPI/HTTP protocol.</span></span> 
  
```XML
<InternalUrl/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="b357e-105">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b357e-105">Attributes and elements</span></span>

<span data-ttu-id="b357e-106">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b357e-106">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b357e-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="b357e-107">Attributes</span></span>

<span data-ttu-id="b357e-108">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="b357e-108">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b357e-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b357e-109">Child elements</span></span>

<span data-ttu-id="b357e-110">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="b357e-110">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b357e-111">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b357e-111">Parent elements</span></span>

|<span data-ttu-id="b357e-112">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b357e-112">**Element**</span></span>|<span data-ttu-id="b357e-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b357e-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b357e-114">AddressBook (POX)</span><span class="sxs-lookup"><span data-stu-id="b357e-114">AddressBook (POX)</span></span>](addressbook-pox.md) <br/> |<span data-ttu-id="b357e-115">Contiene las especificaciones para conectar un cliente al servidor de libreta de direcciones mediante el protocolo MAPI/HTTP.</span><span class="sxs-lookup"><span data-stu-id="b357e-115">Contains the specifications for connecting a client to the address book server by using the MAPI/HTTP protocol.</span></span>  <br/> |
|[<span data-ttu-id="b357e-116">MailStore (POX)</span><span class="sxs-lookup"><span data-stu-id="b357e-116">MailStore (POX)</span></span>](mailstore-pox.md) <br/> |<span data-ttu-id="b357e-117">Contiene las especificaciones para conectar un cliente al buzón de correo del usuario mediante el protocolo MAPI/HTTP.</span><span class="sxs-lookup"><span data-stu-id="b357e-117">Contains the specifications for connecting a client to the user's mailbox by using the MAPI/HTTP protocol.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b357e-118">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="b357e-118">Text value</span></span>

<span data-ttu-id="b357e-119">El valor de texto representa una dirección URL que se puede usar para obtener acceso a un servidor de libreta de direcciones o a un buzón de correo de un usuario desde dentro de la organización del usuario.</span><span class="sxs-lookup"><span data-stu-id="b357e-119">The text value represents a URL that can be used to access an address book server or user's mailbox from inside the user's organization.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b357e-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b357e-120">Remarks</span></span>

<span data-ttu-id="b357e-121">El elemento **InternalUrl** puede estar presente en una respuesta que tiene un elemento [Protocol (POX)](protocol-pox.md) con un valor de atributo de **tipo** de "mapiHttp".</span><span class="sxs-lookup"><span data-stu-id="b357e-121">The **InternalUrl** element can be present in a response that has a [Protocol (POX)](protocol-pox.md) element with a **Type** attribute value of "mapiHttp".</span></span> 
  
<span data-ttu-id="b357e-122">El elemento **InternalUrl** está disponible para clientes que implementan el protocolo MAPI/http y tienen como objetivo Exchange Online, Exchange online como parte de Office 365 y versiones locales de Exchange que comienzan con la compilación 15.00.0847.032 (Exchange Server 2013 SP1).</span><span class="sxs-lookup"><span data-stu-id="b357e-122">The **InternalUrl** element is available to clients that implement the MAPI/HTTP protocol and target Exchange Online, Exchange Online as part of Office 365, and on-premises versions of Exchange starting with build 15.00.0847.032 (Exchange Server 2013 SP1).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b357e-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="b357e-123">See also</span></span>



[<span data-ttu-id="b357e-124">Elementos XML de detección automática de POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="b357e-124">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

