---
title: Externa (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8eed1f79-6eb3-4a88-80fb-d4edf9f34fda
description: El elemento external contiene una colección de direcciones URL que un cliente puede usar para conectarse a Exchange desde fuera de la red de la organización.
ms.openlocfilehash: 45d7e72c5a43c5c468c1edd303a5e5ea8c2cb62e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457973"
---
# <a name="external-pox"></a><span data-ttu-id="ad6e6-103">Externa (POX)</span><span class="sxs-lookup"><span data-stu-id="ad6e6-103">External (POX)</span></span>

<span data-ttu-id="ad6e6-104">El elemento **external** contiene una colección de direcciones URL que un cliente puede usar para conectarse a Exchange desde fuera de la red de la organización.</span><span class="sxs-lookup"><span data-stu-id="ad6e6-104">The **External** element contains a collection of URLs that a client can use to connect to Exchange from outside of the organization's network.</span></span> 
  
[<span data-ttu-id="ad6e6-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="ad6e6-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="ad6e6-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="ad6e6-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="ad6e6-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="ad6e6-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="ad6e6-108">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="ad6e6-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="ad6e6-109">Externa (POX)</span><span class="sxs-lookup"><span data-stu-id="ad6e6-109">External (POX)</span></span>](external-pox.md)
  
```XML
<External>
   <OWAUrl/>
   <Protocol>
      <Type/>
      <ASUrl/>
   </Protocol>
</External>

```

## <a name="attributes-and-elements"></a><span data-ttu-id="ad6e6-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ad6e6-110">Attributes and elements</span></span>

<span data-ttu-id="ad6e6-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ad6e6-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ad6e6-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="ad6e6-112">Attributes</span></span>

<span data-ttu-id="ad6e6-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="ad6e6-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ad6e6-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ad6e6-114">Child elements</span></span>

|<span data-ttu-id="ad6e6-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ad6e6-115">**Element**</span></span>|<span data-ttu-id="ad6e6-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ad6e6-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ad6e6-117">OWAUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="ad6e6-117">OWAUrl (POX)</span></span>](owaurl-pox.md) <br/> |<span data-ttu-id="ad6e6-118">Describe la dirección URL y el esquema de autenticación que se usa para obtener acceso a un equipo concreto que ejecuta Microsoft Exchange Server que tiene instalada la función de servidor acceso de clientes que hospeda Outlook Web Access.</span><span class="sxs-lookup"><span data-stu-id="ad6e6-118">Describes the URL and authentication schema that is used to access a particular computer that is running Microsoft Exchange Server that has the Client Access server role installed that hosts Outlook Web Access.</span></span>  <br/> |
|[<span data-ttu-id="ad6e6-119">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="ad6e6-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="ad6e6-120">Contiene las especificaciones para conectar un cliente al equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="ad6e6-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span> <span data-ttu-id="ad6e6-121">Este elemento **Protocol** solo tiene dos elementos secundarios: un elemento [Type (POX)](type-pox.md) que especifica el protocolo de conexión y un elemento [ASUrl (POX)](asurl-pox.md) , especificando el extremo de EWS para el servicio Web de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="ad6e6-121">This **Protocol** element has only two child elements: a [Type (POX)](type-pox.md) element specifying the connection protocol, and an [ASUrl (POX)](asurl-pox.md) element, specifying the EWS endpoint for the Availability web service.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ad6e6-122">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ad6e6-122">Parent elements</span></span>

|<span data-ttu-id="ad6e6-123">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ad6e6-123">**Element**</span></span>|<span data-ttu-id="ad6e6-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ad6e6-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ad6e6-125">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="ad6e6-125">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="ad6e6-126">Contiene las especificaciones para conectar un cliente al equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="ad6e6-126">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ad6e6-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ad6e6-127">Remarks</span></span>

<span data-ttu-id="ad6e6-128">El elemento **external** es un elemento secundario opcional del elemento **Protocol** .</span><span class="sxs-lookup"><span data-stu-id="ad6e6-128">The **External** element is an optional child element of the **Protocol** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ad6e6-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="ad6e6-129">See also</span></span>



[<span data-ttu-id="ad6e6-130">Elementos XML de detección automática de POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="ad6e6-130">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

