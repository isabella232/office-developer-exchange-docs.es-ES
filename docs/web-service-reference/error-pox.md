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
description: El elemento error contiene una respuesta de error de detección automática.
ms.openlocfilehash: 1a1a3e83898674e605921cb75371036a8a561a95
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530652"
---
# <a name="error-pox"></a><span data-ttu-id="4927c-103">Error (POX)</span><span class="sxs-lookup"><span data-stu-id="4927c-103">Error (POX)</span></span>

<span data-ttu-id="4927c-104">El elemento **error** contiene una respuesta de error de detección automática.</span><span class="sxs-lookup"><span data-stu-id="4927c-104">The **Error** element contains an Autodiscover error response.</span></span> 
  
[<span data-ttu-id="4927c-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="4927c-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="4927c-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="4927c-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="4927c-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="4927c-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="4927c-108">Error (POX)</span><span class="sxs-lookup"><span data-stu-id="4927c-108">Error (POX)</span></span>](error-pox.md)
  
```xml
<Error Time="" Id="">
   <ErrorCode/>
   <Message/>
   <DebugData/>
</Error>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="4927c-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="4927c-109">Attributes and elements</span></span>

<span data-ttu-id="4927c-110">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="4927c-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4927c-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="4927c-111">Attributes</span></span>

|<span data-ttu-id="4927c-112">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="4927c-112">**Attribute**</span></span>|<span data-ttu-id="4927c-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4927c-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4927c-114">Hora</span><span class="sxs-lookup"><span data-stu-id="4927c-114">Time</span></span>  <br/> |<span data-ttu-id="4927c-115">Representa la hora en que se devolvió la respuesta de error.</span><span class="sxs-lookup"><span data-stu-id="4927c-115">Represents the time when the error response was returned.</span></span>  <br/> |
|<span data-ttu-id="4927c-116">Id</span><span class="sxs-lookup"><span data-stu-id="4927c-116">Id</span></span>  <br/> |<span data-ttu-id="4927c-117">Representa un hash del nombre del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="4927c-117">Represents a hash of the name of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4927c-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4927c-118">Child elements</span></span>

|<span data-ttu-id="4927c-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="4927c-119">**Element**</span></span>|<span data-ttu-id="4927c-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4927c-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4927c-121">ErrorCode (POX)</span><span class="sxs-lookup"><span data-stu-id="4927c-121">ErrorCode (POX)</span></span>](errorcode-pox.md) <br/> |<span data-ttu-id="4927c-122">Contiene el código de error para una respuesta de detección automática de errores.</span><span class="sxs-lookup"><span data-stu-id="4927c-122">Contains the error code for an error Autodiscover response.</span></span>  <br/> |
|[<span data-ttu-id="4927c-123">Mensaje (POX)</span><span class="sxs-lookup"><span data-stu-id="4927c-123">Message (POX)</span></span>](message-pox.md) <br/> |<span data-ttu-id="4927c-124">Contiene el mensaje de error de una respuesta de detección automática de errores.</span><span class="sxs-lookup"><span data-stu-id="4927c-124">Contains the error message for an error Autodiscover response.</span></span>  <br/> |
|[<span data-ttu-id="4927c-125">DebugData (POX)</span><span class="sxs-lookup"><span data-stu-id="4927c-125">DebugData (POX)</span></span>](debugdata-pox.md) <br/> |<span data-ttu-id="4927c-126">Contiene los datos de depuración para una respuesta de detección automática de errores.</span><span class="sxs-lookup"><span data-stu-id="4927c-126">Contains the debug data for an error Autodiscover response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4927c-127">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="4927c-127">Parent elements</span></span>

|<span data-ttu-id="4927c-128">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="4927c-128">**Element**</span></span>|<span data-ttu-id="4927c-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4927c-129">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4927c-130">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="4927c-130">Account (POX)</span></span>](account-pox.md) <br/> |<span data-ttu-id="4927c-131">Contiene una respuesta de error de detección automática.</span><span class="sxs-lookup"><span data-stu-id="4927c-131">Contains an Autodiscover error response.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4927c-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="4927c-132">See also</span></span>



[<span data-ttu-id="4927c-133">Elementos XML de detección automática de POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="4927c-133">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

