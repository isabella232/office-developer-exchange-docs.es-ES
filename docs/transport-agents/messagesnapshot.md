---
title: messageSnapshot
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- messageSnapshot
api_type:
- schema
ms.assetid: f157e44c-b950-463f-b086-31d5da94b7ff
description: 'Última modificación: 17 de septiembre de 2015'
ms.openlocfilehash: 4b814def8eef8fb452d2e754c5f6787d644055f7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763372"
---
# <a name="messagesnapshot"></a><span data-ttu-id="ad76f-103">messageSnapshot</span><span class="sxs-lookup"><span data-stu-id="ad76f-103">messageSnapshot</span></span>

<span data-ttu-id="ad76f-104">**Se aplica a:** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="ad76f-104">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="ad76f-105">El elemento **messageSnapshot** contiene un atributo que especifica si está habilitada la característica de seguimiento de canalización para el servidor de Exchange que tiene el acceso de cliente o el rol de servidor de buzón de correo instalado.</span><span class="sxs-lookup"><span data-stu-id="ad76f-105">The **messageSnapshot** element contains an attribute that specifies whether the pipeline tracing feature is enabled for the Exchange server that has the Client Access or the Mailbox server role installed.</span></span> 
  
- [<span data-ttu-id="ad76f-106">configuración</span><span class="sxs-lookup"><span data-stu-id="ad76f-106">configuration</span></span>](configuration.md)  
- [<span data-ttu-id="ad76f-107">mexRuntime</span><span class="sxs-lookup"><span data-stu-id="ad76f-107">mexRuntime</span></span>](mexruntime.md) 
- [<span data-ttu-id="ad76f-108">supervisión</span><span class="sxs-lookup"><span data-stu-id="ad76f-108">monitoring</span></span>](monitoring.md) 
- [<span data-ttu-id="ad76f-109">messageSnapshot</span><span class="sxs-lookup"><span data-stu-id="ad76f-109">messageSnapshot</span></span>](messagesnapshot.md)
  
```XML
<messageSnapshot enabled="" />
```

<span data-ttu-id="ad76f-110">**messageSnapshotType (booleano)**</span><span class="sxs-lookup"><span data-stu-id="ad76f-110">**messageSnapshotType (Boolean)**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="ad76f-111">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ad76f-111">Attributes and elements</span></span>

<span data-ttu-id="ad76f-112">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ad76f-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ad76f-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="ad76f-113">Attributes</span></span>

|<span data-ttu-id="ad76f-114">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="ad76f-114">**Attribute**</span></span>|<span data-ttu-id="ad76f-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ad76f-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ad76f-116">**habilitado**</span><span class="sxs-lookup"><span data-stu-id="ad76f-116">**enabled**</span></span> <br/> |<span data-ttu-id="ad76f-117">Un valor booleano que indica si está habilitada la característica de seguimiento de canalización para el acceso de cliente o el servidor de buzones.</span><span class="sxs-lookup"><span data-stu-id="ad76f-117">A Boolean value that indicates whether the pipeline tracing feature is enabled for the Client Access or the Mailbox server.</span></span> <span data-ttu-id="ad76f-118">El valor es **true** si está habilitado el seguimiento de canalización; de lo contrario, el valor es **false** o el elemento no está presente.</span><span class="sxs-lookup"><span data-stu-id="ad76f-118">The value is **true** if pipeline tracing is enabled; otherwise, the value is **false** or the element is not present.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ad76f-119">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ad76f-119">Child elements</span></span>

<span data-ttu-id="ad76f-120">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ad76f-120">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ad76f-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ad76f-121">Parent elements</span></span>

|<span data-ttu-id="ad76f-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="ad76f-122">**Element**</span></span>|<span data-ttu-id="ad76f-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ad76f-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ad76f-124">supervisión</span><span class="sxs-lookup"><span data-stu-id="ad76f-124">monitoring</span></span>](monitoring.md) <br/> |<span data-ttu-id="ad76f-125">Contiene información de configuración que define cómo y cuándo el servicio de transporte supervisa a los agentes que se instalan.</span><span class="sxs-lookup"><span data-stu-id="ad76f-125">Contains configuration information that defines how and when the transport service monitors agents that are installed.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="ad76f-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ad76f-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ad76f-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ad76f-127">Namespace</span></span>  <br/> |<span data-ttu-id="ad76f-128">Este archivo no define un espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="ad76f-128">This file does not define a namespace.</span></span>  <br/> |
|<span data-ttu-id="ad76f-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ad76f-129">Schema Name</span></span>  <br/> |<span data-ttu-id="ad76f-130">No está disponible.</span><span class="sxs-lookup"><span data-stu-id="ad76f-130">Not available.</span></span>  <br/> |
|<span data-ttu-id="ad76f-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ad76f-131">Validation File</span></span>  <br/> |<span data-ttu-id="ad76f-132">No está disponible.</span><span class="sxs-lookup"><span data-stu-id="ad76f-132">Not available.</span></span>  <br/> |
|<span data-ttu-id="ad76f-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ad76f-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="ad76f-134">Falso.</span><span class="sxs-lookup"><span data-stu-id="ad76f-134">False.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ad76f-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="ad76f-135">See also</span></span>

- [<span data-ttu-id="ad76f-136">Elementos del archivo de configuración de los agentes para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="ad76f-136">Agents configuration file elements for Exchange 2013</span></span>](agents-configuration-file-elements-for-exchange-2013.md)

