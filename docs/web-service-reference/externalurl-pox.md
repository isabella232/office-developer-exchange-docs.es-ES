---
title: ExternalUrl (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3b647d88-6feb-40d7-9299-b2ca47b707db
description: El elemento ExternalUrl contiene la dirección URL para conectar a un cliente con el servidor de la libreta de direcciones o buzón de un usuario desde fuera de la organización del usuario mediante el protocolo HTTP/MAPI.
ms.openlocfilehash: 603e2109e7b3c98acdd4cbc13df81ed9717630ec
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764570"
---
# <a name="externalurl-pox"></a><span data-ttu-id="55b9e-103">ExternalUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="55b9e-103">ExternalUrl (POX)</span></span>

<span data-ttu-id="55b9e-104">El elemento **ExternalUrl** contiene la dirección URL para conectar a un cliente con el servidor de la libreta de direcciones o buzón de un usuario desde fuera de la organización del usuario mediante el protocolo HTTP/MAPI.</span><span class="sxs-lookup"><span data-stu-id="55b9e-104">The **ExternalUrl** element contains the URL for connecting a client to the address book server or a user's mailbox from outside the user's organization by using the MAPI/HTTP protocol.</span></span> 
  
```XML
<ExternalUrl/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="55b9e-105">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="55b9e-105">Attributes and elements</span></span>

<span data-ttu-id="55b9e-106">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="55b9e-106">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="55b9e-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="55b9e-107">Attributes</span></span>

<span data-ttu-id="55b9e-108">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="55b9e-108">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="55b9e-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="55b9e-109">Child elements</span></span>

<span data-ttu-id="55b9e-110">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="55b9e-110">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="55b9e-111">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="55b9e-111">Parent elements</span></span>

|<span data-ttu-id="55b9e-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="55b9e-112">**Element**</span></span>|<span data-ttu-id="55b9e-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="55b9e-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="55b9e-114">Libreta de direcciones (POX)</span><span class="sxs-lookup"><span data-stu-id="55b9e-114">AddressBook (POX)</span></span>](addressbook-pox.md) <br/> |<span data-ttu-id="55b9e-115">Contiene las especificaciones para conectar a un cliente con el servidor de la libreta de direcciones mediante el protocolo HTTP/MAPI.</span><span class="sxs-lookup"><span data-stu-id="55b9e-115">Contains the specifications for connecting a client to the address book server by using the MAPI/HTTP protocol.</span></span>  <br/> |
|[<span data-ttu-id="55b9e-116">Almacenamiento de correo (POX)</span><span class="sxs-lookup"><span data-stu-id="55b9e-116">MailStore (POX)</span></span>](mailstore-pox.md) <br/> |<span data-ttu-id="55b9e-117">Contiene las especificaciones para conectar a un cliente con el buzón del usuario mediante el protocolo HTTP/MAPI.</span><span class="sxs-lookup"><span data-stu-id="55b9e-117">Contains the specifications for connecting a client to the user's mailbox by using the MAPI/HTTP protocol.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="55b9e-118">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="55b9e-118">Text value</span></span>

<span data-ttu-id="55b9e-119">El valor de texto representa una dirección URL que se puede usar para tener acceso al buzón del usuario desde fuera de la organización del usuario o un servidor de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="55b9e-119">The text value represents a URL that can be used to access an address book server or user's mailbox from outside the user's organization.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="55b9e-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="55b9e-120">Remarks</span></span>

<span data-ttu-id="55b9e-121">El elemento **ExternalUrl** puede estar presente en una respuesta que tiene un elemento de [Protocolo (POX)](protocol-pox.md) con un valor de atributo de **tipo** de "mapiHttp".</span><span class="sxs-lookup"><span data-stu-id="55b9e-121">The **ExternalUrl** element can be present in a response that has a [Protocol (POX)](protocol-pox.md) element with a **Type** attribute value of "mapiHttp".</span></span> 
  
<span data-ttu-id="55b9e-122">El elemento **ExternalUrl** está disponible para los clientes que implementan el protocolo HTTP/MAPI y destino Exchange Online, Exchange Online como parte de Office 365, y las versiones locales de Exchange a partir creación 15.00.0847.032 (Exchange Server 2013 SP1) .</span><span class="sxs-lookup"><span data-stu-id="55b9e-122">The **ExternalUrl** element is available to clients that implement the MAPI/HTTP protocol and target Exchange Online, Exchange Online as part of Office 365, and on-premises versions of Exchange starting with build 15.00.0847.032 (Exchange Server 2013 SP1).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="55b9e-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="55b9e-123">See also</span></span>



[<span data-ttu-id="55b9e-124">Elementos de Autodiscover XML POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="55b9e-124">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

