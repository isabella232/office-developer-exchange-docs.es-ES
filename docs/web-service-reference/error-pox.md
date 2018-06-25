---
title: Error (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 91c63b62-ab68-4c32-a2f7-5a87c188335b
description: El elemento de Error contiene una respuesta de error de detección automática.
ms.openlocfilehash: 3135a352365fe3000ce2d202ad78452d5c8ccc7f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764434"
---
# <a name="error-pox"></a><span data-ttu-id="bd18d-103">Error (POX)</span><span class="sxs-lookup"><span data-stu-id="bd18d-103">Error (POX)</span></span>

<span data-ttu-id="bd18d-104">El elemento de **Error** contiene una respuesta de error de detección automática.</span><span class="sxs-lookup"><span data-stu-id="bd18d-104">The **Error** element contains an Autodiscover error response.</span></span> 
  
[<span data-ttu-id="bd18d-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="bd18d-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="bd18d-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="bd18d-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="bd18d-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="bd18d-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="bd18d-108">Error (POX)</span><span class="sxs-lookup"><span data-stu-id="bd18d-108">Error (POX)</span></span>](error-pox.md)
  
```xml
<Error Time="" Id="">
   <ErrorCode/>
   <Message/>
   <DebugData/>
</Error>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="bd18d-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="bd18d-109">Attributes and elements</span></span>

<span data-ttu-id="bd18d-110">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="bd18d-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bd18d-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="bd18d-111">Attributes</span></span>

|<span data-ttu-id="bd18d-112">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="bd18d-112">**Attribute**</span></span>|<span data-ttu-id="bd18d-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bd18d-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bd18d-114">Time</span><span class="sxs-lookup"><span data-stu-id="bd18d-114">Time</span></span>  <br/> |<span data-ttu-id="bd18d-115">Representa la hora cuando se devolvió la respuesta de error.</span><span class="sxs-lookup"><span data-stu-id="bd18d-115">Represents the time when the error response was returned.</span></span>  <br/> |
|<span data-ttu-id="bd18d-116">Id</span><span class="sxs-lookup"><span data-stu-id="bd18d-116">Id</span></span>  <br/> |<span data-ttu-id="bd18d-117">Representa un valor hash del nombre del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="bd18d-117">Represents a hash of the name of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="bd18d-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="bd18d-118">Child elements</span></span>

|<span data-ttu-id="bd18d-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="bd18d-119">**Element**</span></span>|<span data-ttu-id="bd18d-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bd18d-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bd18d-121">ErrorCode (POX)</span><span class="sxs-lookup"><span data-stu-id="bd18d-121">ErrorCode (POX)</span></span>](errorcode-pox.md) <br/> |<span data-ttu-id="bd18d-122">Contiene el código de error de un error de respuesta de detección automática.</span><span class="sxs-lookup"><span data-stu-id="bd18d-122">Contains the error code for an error Autodiscover response.</span></span>  <br/> |
|[<span data-ttu-id="bd18d-123">Mensaje (POX)</span><span class="sxs-lookup"><span data-stu-id="bd18d-123">Message (POX)</span></span>](message-pox.md) <br/> |<span data-ttu-id="bd18d-124">Contiene el mensaje de error de un error de respuesta de detección automática.</span><span class="sxs-lookup"><span data-stu-id="bd18d-124">Contains the error message for an error Autodiscover response.</span></span>  <br/> |
|[<span data-ttu-id="bd18d-125">DebugData (POX)</span><span class="sxs-lookup"><span data-stu-id="bd18d-125">DebugData (POX)</span></span>](debugdata-pox.md) <br/> |<span data-ttu-id="bd18d-126">Contiene los datos de depuración de un error de respuesta de detección automática.</span><span class="sxs-lookup"><span data-stu-id="bd18d-126">Contains the debug data for an error Autodiscover response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="bd18d-127">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="bd18d-127">Parent elements</span></span>

|<span data-ttu-id="bd18d-128">**Element**</span><span class="sxs-lookup"><span data-stu-id="bd18d-128">**Element**</span></span>|<span data-ttu-id="bd18d-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bd18d-129">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bd18d-130">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="bd18d-130">Account (POX)</span></span>](account-pox.md) <br/> |<span data-ttu-id="bd18d-131">Contiene una respuesta de error de detección automática.</span><span class="sxs-lookup"><span data-stu-id="bd18d-131">Contains an Autodiscover error response.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bd18d-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="bd18d-132">See also</span></span>



[<span data-ttu-id="bd18d-133">Elementos de Autodiscover XML POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="bd18d-133">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

