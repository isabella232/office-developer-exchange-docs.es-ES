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
description: El elemento User proporciona información específica del usuario.
ms.openlocfilehash: 8f53319bcf34595305748adafc9aa1e25283611e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530221"
---
# <a name="user-pox"></a><span data-ttu-id="8f278-103">Usuario (POX)</span><span class="sxs-lookup"><span data-stu-id="8f278-103">User (POX)</span></span>

<span data-ttu-id="8f278-104">El elemento **User** proporciona información específica del usuario.</span><span class="sxs-lookup"><span data-stu-id="8f278-104">The **User** element provides user-specific information.</span></span> 
  
[<span data-ttu-id="8f278-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="8f278-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="8f278-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="8f278-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="8f278-107">Usuario (POX)</span><span class="sxs-lookup"><span data-stu-id="8f278-107">User (POX)</span></span>](user-pox.md)
  
```xml
<User>
   <DisplayName/>
   <LegacyDN/>
   <DeploymentId/>
   <AutoDiscoverSMTPAddress/>
</User>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="8f278-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="8f278-108">Attributes and elements</span></span>

<span data-ttu-id="8f278-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="8f278-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8f278-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="8f278-110">Attributes</span></span>

<span data-ttu-id="8f278-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="8f278-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8f278-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8f278-112">Child elements</span></span>

|<span data-ttu-id="8f278-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="8f278-113">**Element**</span></span>|<span data-ttu-id="8f278-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8f278-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8f278-115">DisplayName (cadena)</span><span class="sxs-lookup"><span data-stu-id="8f278-115">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="8f278-116">Representa el nombre para mostrar del usuario.</span><span class="sxs-lookup"><span data-stu-id="8f278-116">Represents the user's display name.</span></span>  <br/> |
|[<span data-ttu-id="8f278-117">LegacyDN (POX)</span><span class="sxs-lookup"><span data-stu-id="8f278-117">LegacyDN (POX)</span></span>](legacydn-pox.md) <br/> |<span data-ttu-id="8f278-118">Identifica el buzón de un usuario mediante el nombre distintivo heredado.</span><span class="sxs-lookup"><span data-stu-id="8f278-118">Identifies a user's mailbox by legacy distinguished name.</span></span>  <br/> |
|[<span data-ttu-id="8f278-119">DeploymentId (POX)</span><span class="sxs-lookup"><span data-stu-id="8f278-119">DeploymentId (POX)</span></span>](deploymentid-pox.md) <br/> |<span data-ttu-id="8f278-120">Identifica de forma exclusiva el bosque de Exchange.</span><span class="sxs-lookup"><span data-stu-id="8f278-120">Uniquely identifies the Exchange forest.</span></span>  <br/> |
|[<span data-ttu-id="8f278-121">AutoDiscoverSMTPAddress (POX)</span><span class="sxs-lookup"><span data-stu-id="8f278-121">AutoDiscoverSMTPAddress (POX)</span></span>](autodiscoversmtpaddress-pox.md) <br/> |<span data-ttu-id="8f278-122">Contiene la dirección SMTP del usuario que se usa para el proceso de detección automática.</span><span class="sxs-lookup"><span data-stu-id="8f278-122">Contains the user's SMTP address that is used for the Autodiscover process.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8f278-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="8f278-123">Parent elements</span></span>

|<span data-ttu-id="8f278-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="8f278-124">**Element**</span></span>|<span data-ttu-id="8f278-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8f278-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8f278-126">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="8f278-126">Response (POX)</span></span>](response-pox.md) <br/> |<span data-ttu-id="8f278-127">Contiene la respuesta del servicio Detección automática.</span><span class="sxs-lookup"><span data-stu-id="8f278-127">Contains the response from the Autodiscover service.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8f278-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8f278-128">Remarks</span></span>

<span data-ttu-id="8f278-129">Las solicitudes y respuestas de detección automática deben tener codificación UTF-8.</span><span class="sxs-lookup"><span data-stu-id="8f278-129">Autodiscover requests and responses must be UTF-8 encoded.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8f278-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="8f278-130">See also</span></span>



[<span data-ttu-id="8f278-131">Elementos XML de detección automática de POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="8f278-131">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

