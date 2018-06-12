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
description: El elemento interno contiene la colección de direcciones URL que puede utilizar un cliente para conectarse a Exchange desde dentro de la red de la organización.
ms.openlocfilehash: 0dc5b679af98b52f15ef3b40181c2d97f102f373
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19835946"
---
# <a name="internal-pox"></a><span data-ttu-id="8859e-103">Interno (POX)</span><span class="sxs-lookup"><span data-stu-id="8859e-103">Internal (POX)</span></span>

<span data-ttu-id="8859e-104">El elemento **interno** contiene la colección de direcciones URL que puede utilizar un cliente para conectarse a Exchange desde dentro de la red de la organización.</span><span class="sxs-lookup"><span data-stu-id="8859e-104">The **Internal** element contains the collection of URLs that a client can use to connect to Exchange from inside the organization's network.</span></span> 
  
[<span data-ttu-id="8859e-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="8859e-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="8859e-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="8859e-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="8859e-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="8859e-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="8859e-108">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="8859e-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="8859e-109">Interno (POX)</span><span class="sxs-lookup"><span data-stu-id="8859e-109">Internal (POX)</span></span>](internal-pox.md)
  
```xml
<Internal>
   <OWAUrl/>
   <Protocol>
      <Type/>
      <ASUrl/>
   </Protocol>
</Internal>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="8859e-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="8859e-110">Attributes and elements</span></span>

<span data-ttu-id="8859e-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="8859e-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8859e-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="8859e-112">Attributes</span></span>

<span data-ttu-id="8859e-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="8859e-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8859e-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8859e-114">Child elements</span></span>

|<span data-ttu-id="8859e-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="8859e-115">**Element**</span></span>|<span data-ttu-id="8859e-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8859e-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8859e-117">OWAUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="8859e-117">OWAUrl (POX)</span></span>](owaurl-pox.md) <br/> |<span data-ttu-id="8859e-118">Describe la dirección URL y el esquema de autenticación que se usa para tener acceso a un determinado equipo que ejecuta a Microsoft Exchange Server que tiene el rol de servidor de acceso de cliente instalado que aloja Outlook Web Access.</span><span class="sxs-lookup"><span data-stu-id="8859e-118">Describes the URL and authentication schema that is used to access a particular computer that is running Microsoft Exchange Server that has the Client Access server role installed that hosts Outlook Web Access.</span></span>  <br/> |
|[<span data-ttu-id="8859e-119">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="8859e-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="8859e-120">Contiene las especificaciones para conectar a un cliente en el equipo que ejecuta Microsoft Exchange Server que tiene instalada la función del servidor acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="8859e-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span> <span data-ttu-id="8859e-121">Este elemento de **protocolo** tiene sólo dos elementos secundarios: un elemento de [Tipo (POX)](type-pox.md) que especifica el protocolo de conexión y un elemento [ASUrl (POX)](asurl-pox.md) , que especifica el extremo EWS para el servicio web de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="8859e-121">This **Protocol** element has only two child elements: a [Type (POX)](type-pox.md) element specifying the connection protocol, and an [ASUrl (POX)](asurl-pox.md) element, specifying the EWS endpoint for the Availability web service.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8859e-122">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="8859e-122">Parent elements</span></span>

|<span data-ttu-id="8859e-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="8859e-123">**Element**</span></span>|<span data-ttu-id="8859e-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8859e-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8859e-125">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="8859e-125">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="8859e-126">Contiene las especificaciones para conectar a un cliente en el equipo que ejecuta Microsoft Exchange Server que tiene instalada la función del servidor acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="8859e-126">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8859e-127">Notas</span><span class="sxs-lookup"><span data-stu-id="8859e-127">Remarks</span></span>

<span data-ttu-id="8859e-128">El elemento **interno** es un elemento secundario opcional del elemento **Protocol** .</span><span class="sxs-lookup"><span data-stu-id="8859e-128">The **Internal** element is an optional child element of the **Protocol** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8859e-129">Ver también</span><span class="sxs-lookup"><span data-stu-id="8859e-129">See also</span></span>



[<span data-ttu-id="8859e-130">Elementos de Autodiscover XML POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="8859e-130">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

