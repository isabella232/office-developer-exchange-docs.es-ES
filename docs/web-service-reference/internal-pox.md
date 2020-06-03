---
title: Interno (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 69c22546-ebd6-4a03-b0b4-bbac72ec5551
description: El elemento Internal contiene la colección de direcciones URL que puede usar un cliente para conectarse a Exchange desde dentro de la red de la organización.
ms.openlocfilehash: 8164a018a11f9bae9c3abcbfebf6cf0694ca4183
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465600"
---
# <a name="internal-pox"></a><span data-ttu-id="82561-103">Interno (POX)</span><span class="sxs-lookup"><span data-stu-id="82561-103">Internal (POX)</span></span>

<span data-ttu-id="82561-104">El elemento **Internal** contiene la colección de direcciones URL que puede usar un cliente para conectarse a Exchange desde dentro de la red de la organización.</span><span class="sxs-lookup"><span data-stu-id="82561-104">The **Internal** element contains the collection of URLs that a client can use to connect to Exchange from inside the organization's network.</span></span> 
  
[<span data-ttu-id="82561-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="82561-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="82561-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="82561-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="82561-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="82561-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="82561-108">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="82561-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="82561-109">Interno (POX)</span><span class="sxs-lookup"><span data-stu-id="82561-109">Internal (POX)</span></span>](internal-pox.md)
  
```xml
<Internal>
   <OWAUrl/>
   <Protocol>
      <Type/>
      <ASUrl/>
   </Protocol>
</Internal>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="82561-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="82561-110">Attributes and elements</span></span>

<span data-ttu-id="82561-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="82561-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="82561-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="82561-112">Attributes</span></span>

<span data-ttu-id="82561-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="82561-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="82561-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="82561-114">Child elements</span></span>

|<span data-ttu-id="82561-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="82561-115">**Element**</span></span>|<span data-ttu-id="82561-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="82561-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="82561-117">OWAUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="82561-117">OWAUrl (POX)</span></span>](owaurl-pox.md) <br/> |<span data-ttu-id="82561-118">Describe la dirección URL y el esquema de autenticación que se usa para obtener acceso a un equipo concreto que ejecuta Microsoft Exchange Server que tiene instalada la función de servidor acceso de clientes que hospeda Outlook Web Access.</span><span class="sxs-lookup"><span data-stu-id="82561-118">Describes the URL and authentication schema that is used to access a particular computer that is running Microsoft Exchange Server that has the Client Access server role installed that hosts Outlook Web Access.</span></span>  <br/> |
|[<span data-ttu-id="82561-119">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="82561-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="82561-120">Contiene las especificaciones para conectar un cliente al equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="82561-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span> <span data-ttu-id="82561-121">Este elemento **Protocol** solo tiene dos elementos secundarios: un elemento [Type (POX)](type-pox.md) que especifica el protocolo de conexión y un elemento [ASUrl (POX)](asurl-pox.md) , especificando el extremo de EWS para el servicio Web de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="82561-121">This **Protocol** element has only two child elements: a [Type (POX)](type-pox.md) element specifying the connection protocol, and an [ASUrl (POX)](asurl-pox.md) element, specifying the EWS endpoint for the Availability web service.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="82561-122">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="82561-122">Parent elements</span></span>

|<span data-ttu-id="82561-123">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="82561-123">**Element**</span></span>|<span data-ttu-id="82561-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="82561-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="82561-125">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="82561-125">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="82561-126">Contiene las especificaciones para conectar un cliente al equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="82561-126">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="82561-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="82561-127">Remarks</span></span>

<span data-ttu-id="82561-128">El elemento **Internal** es un elemento secundario opcional del elemento **Protocol** .</span><span class="sxs-lookup"><span data-stu-id="82561-128">The **Internal** element is an optional child element of the **Protocol** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="82561-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="82561-129">See also</span></span>



[<span data-ttu-id="82561-130">Elementos XML de detección automática de POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="82561-130">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

