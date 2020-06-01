---
title: ExternalUrl (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3b647d88-6feb-40d7-9299-b2ca47b707db
description: El elemento ExternalUrl contiene la dirección URL para conectar un cliente al servidor de la libreta de direcciones o al buzón de un usuario desde fuera de la organización del usuario mediante el protocolo MAPI/HTTP.
ms.openlocfilehash: 94265051be68ed06d1dab8d46dd4ce29d8694c93
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457959"
---
# <a name="externalurl-pox"></a><span data-ttu-id="f6e0b-103">ExternalUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="f6e0b-103">ExternalUrl (POX)</span></span>

<span data-ttu-id="f6e0b-104">El elemento **ExternalUrl** contiene la dirección URL para conectar un cliente al servidor de la libreta de direcciones o al buzón de un usuario desde fuera de la organización del usuario mediante el protocolo MAPI/http.</span><span class="sxs-lookup"><span data-stu-id="f6e0b-104">The **ExternalUrl** element contains the URL for connecting a client to the address book server or a user's mailbox from outside the user's organization by using the MAPI/HTTP protocol.</span></span> 
  
```XML
<ExternalUrl/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="f6e0b-105">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f6e0b-105">Attributes and elements</span></span>

<span data-ttu-id="f6e0b-106">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f6e0b-106">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f6e0b-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="f6e0b-107">Attributes</span></span>

<span data-ttu-id="f6e0b-108">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="f6e0b-108">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f6e0b-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f6e0b-109">Child elements</span></span>

<span data-ttu-id="f6e0b-110">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="f6e0b-110">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f6e0b-111">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f6e0b-111">Parent elements</span></span>

|<span data-ttu-id="f6e0b-112">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f6e0b-112">**Element**</span></span>|<span data-ttu-id="f6e0b-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f6e0b-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f6e0b-114">AddressBook (POX)</span><span class="sxs-lookup"><span data-stu-id="f6e0b-114">AddressBook (POX)</span></span>](addressbook-pox.md) <br/> |<span data-ttu-id="f6e0b-115">Contiene las especificaciones para conectar un cliente al servidor de libreta de direcciones mediante el protocolo MAPI/HTTP.</span><span class="sxs-lookup"><span data-stu-id="f6e0b-115">Contains the specifications for connecting a client to the address book server by using the MAPI/HTTP protocol.</span></span>  <br/> |
|[<span data-ttu-id="f6e0b-116">MailStore (POX)</span><span class="sxs-lookup"><span data-stu-id="f6e0b-116">MailStore (POX)</span></span>](mailstore-pox.md) <br/> |<span data-ttu-id="f6e0b-117">Contiene las especificaciones para conectar un cliente al buzón de correo del usuario mediante el protocolo MAPI/HTTP.</span><span class="sxs-lookup"><span data-stu-id="f6e0b-117">Contains the specifications for connecting a client to the user's mailbox by using the MAPI/HTTP protocol.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f6e0b-118">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="f6e0b-118">Text value</span></span>

<span data-ttu-id="f6e0b-119">El valor de texto representa una dirección URL que puede usarse para obtener acceso a un servidor de libreta de direcciones o a un buzón de correo del usuario desde fuera de la organización del usuario.</span><span class="sxs-lookup"><span data-stu-id="f6e0b-119">The text value represents a URL that can be used to access an address book server or user's mailbox from outside the user's organization.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f6e0b-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f6e0b-120">Remarks</span></span>

<span data-ttu-id="f6e0b-121">El elemento **ExternalUrl** puede estar presente en una respuesta que tiene un elemento [Protocol (POX)](protocol-pox.md) con un valor de atributo de **tipo** de "mapiHttp".</span><span class="sxs-lookup"><span data-stu-id="f6e0b-121">The **ExternalUrl** element can be present in a response that has a [Protocol (POX)](protocol-pox.md) element with a **Type** attribute value of "mapiHttp".</span></span> 
  
<span data-ttu-id="f6e0b-122">El elemento **ExternalUrl** está disponible para los clientes que implementan el protocolo MAPI/http y tienen como objetivo Exchange Online, Exchange online como parte de Office 365 y las versiones locales de Exchange a partir de Build 15.00.0847.032 (exchange Server 2013 SP1).</span><span class="sxs-lookup"><span data-stu-id="f6e0b-122">The **ExternalUrl** element is available to clients that implement the MAPI/HTTP protocol and target Exchange Online, Exchange Online as part of Office 365, and on-premises versions of Exchange starting with build 15.00.0847.032 (Exchange Server 2013 SP1).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f6e0b-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="f6e0b-123">See also</span></span>



[<span data-ttu-id="f6e0b-124">Elementos XML de detección automática de POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="f6e0b-124">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

