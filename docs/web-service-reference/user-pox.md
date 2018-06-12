---
title: Usuario (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 7c42b516-77f6-4aee-99d8-b866d82d793a
description: El elemento de usuario proporciona información específica del usuario.
ms.openlocfilehash: 3f90ff0cc00170170c7304f2a19fe1d7abd9d1bc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840896"
---
# <a name="user-pox"></a><span data-ttu-id="b1f41-103">Usuario (POX)</span><span class="sxs-lookup"><span data-stu-id="b1f41-103">User (POX)</span></span>

<span data-ttu-id="b1f41-104">El elemento de **usuario** proporciona información específica del usuario.</span><span class="sxs-lookup"><span data-stu-id="b1f41-104">The **User** element provides user-specific information.</span></span> 
  
[<span data-ttu-id="b1f41-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="b1f41-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="b1f41-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="b1f41-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="b1f41-107">Usuario (POX)</span><span class="sxs-lookup"><span data-stu-id="b1f41-107">User (POX)</span></span>](user-pox.md)
  
```xml
<User>
   <DisplayName/>
   <LegacyDN/>
   <DeploymentId/>
   <AutoDiscoverSMTPAddress/>
</User>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="b1f41-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b1f41-108">Attributes and elements</span></span>

<span data-ttu-id="b1f41-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b1f41-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b1f41-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="b1f41-110">Attributes</span></span>

<span data-ttu-id="b1f41-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b1f41-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b1f41-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b1f41-112">Child elements</span></span>

|<span data-ttu-id="b1f41-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="b1f41-113">**Element**</span></span>|<span data-ttu-id="b1f41-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b1f41-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b1f41-115">DisplayName (cadena)</span><span class="sxs-lookup"><span data-stu-id="b1f41-115">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="b1f41-116">Representa el nombre para mostrar del usuario.</span><span class="sxs-lookup"><span data-stu-id="b1f41-116">Represents the user's display name.</span></span>  <br/> |
|[<span data-ttu-id="b1f41-117">LegacyDN (POX)</span><span class="sxs-lookup"><span data-stu-id="b1f41-117">LegacyDN (POX)</span></span>](legacydn-pox.md) <br/> |<span data-ttu-id="b1f41-118">Identifica el buzón de un usuario por su nombre distintivo (DN) heredado.</span><span class="sxs-lookup"><span data-stu-id="b1f41-118">Identifies a user's mailbox by legacy distinguished name.</span></span>  <br/> |
|[<span data-ttu-id="b1f41-119">DeploymentId (POX)</span><span class="sxs-lookup"><span data-stu-id="b1f41-119">DeploymentId (POX)</span></span>](deploymentid-pox.md) <br/> |<span data-ttu-id="b1f41-120">Identifica de forma exclusiva el bosque de Exchange.</span><span class="sxs-lookup"><span data-stu-id="b1f41-120">Uniquely identifies the Exchange forest.</span></span>  <br/> |
|[<span data-ttu-id="b1f41-121">AutoDiscoverSMTPAddress (POX)</span><span class="sxs-lookup"><span data-stu-id="b1f41-121">AutoDiscoverSMTPAddress (POX)</span></span>](autodiscoversmtpaddress-pox.md) <br/> |<span data-ttu-id="b1f41-122">Contiene una dirección SMTP del usuario que se usa para el proceso de detección automática.</span><span class="sxs-lookup"><span data-stu-id="b1f41-122">Contains the user's SMTP address that is used for the Autodiscover process.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b1f41-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b1f41-123">Parent elements</span></span>

|<span data-ttu-id="b1f41-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="b1f41-124">**Element**</span></span>|<span data-ttu-id="b1f41-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b1f41-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b1f41-126">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="b1f41-126">Response (POX)</span></span>](response-pox.md) <br/> |<span data-ttu-id="b1f41-127">Contiene la respuesta del servicio Detección automática.</span><span class="sxs-lookup"><span data-stu-id="b1f41-127">Contains the response from the Autodiscover service.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b1f41-128">Notas</span><span class="sxs-lookup"><span data-stu-id="b1f41-128">Remarks</span></span>

<span data-ttu-id="b1f41-129">Las respuestas y solicitudes de detección automática deben ser con codificación UTF-8.</span><span class="sxs-lookup"><span data-stu-id="b1f41-129">Autodiscover requests and responses must be UTF-8 encoded.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b1f41-130">Ver también</span><span class="sxs-lookup"><span data-stu-id="b1f41-130">See also</span></span>



[<span data-ttu-id="b1f41-131">Elementos de Autodiscover XML POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="b1f41-131">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

