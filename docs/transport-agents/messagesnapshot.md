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
ms.openlocfilehash: 8a58444580c803efb7312df95d75d697bc42e8e0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461845"
---
# <a name="messagesnapshot"></a><span data-ttu-id="eb37e-103">messageSnapshot</span><span class="sxs-lookup"><span data-stu-id="eb37e-103">messageSnapshot</span></span>

<span data-ttu-id="eb37e-104">**Se aplica a:** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="eb37e-104">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="eb37e-105">El elemento **messageSnapshot** contiene un atributo que especifica si la característica de seguimiento de canalización está habilitada para el servidor de Exchange que tiene instalado el rol de servidor acceso de cliente o buzón.</span><span class="sxs-lookup"><span data-stu-id="eb37e-105">The **messageSnapshot** element contains an attribute that specifies whether the pipeline tracing feature is enabled for the Exchange server that has the Client Access or the Mailbox server role installed.</span></span> 
  
- [<span data-ttu-id="eb37e-106">configuración</span><span class="sxs-lookup"><span data-stu-id="eb37e-106">configuration</span></span>](configuration.md)  
- [<span data-ttu-id="eb37e-107">mexRuntime</span><span class="sxs-lookup"><span data-stu-id="eb37e-107">mexRuntime</span></span>](mexruntime.md) 
- [<span data-ttu-id="eb37e-108">monitor</span><span class="sxs-lookup"><span data-stu-id="eb37e-108">monitoring</span></span>](monitoring.md) 
- [<span data-ttu-id="eb37e-109">messageSnapshot</span><span class="sxs-lookup"><span data-stu-id="eb37e-109">messageSnapshot</span></span>](messagesnapshot.md)
  
```XML
<messageSnapshot enabled="" />
```

<span data-ttu-id="eb37e-110">**messageSnapshotType (Boolean)**</span><span class="sxs-lookup"><span data-stu-id="eb37e-110">**messageSnapshotType (Boolean)**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="eb37e-111">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="eb37e-111">Attributes and elements</span></span>

<span data-ttu-id="eb37e-112">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="eb37e-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="eb37e-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="eb37e-113">Attributes</span></span>

|<span data-ttu-id="eb37e-114">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="eb37e-114">**Attribute**</span></span>|<span data-ttu-id="eb37e-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="eb37e-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="eb37e-116">**enabled**</span><span class="sxs-lookup"><span data-stu-id="eb37e-116">**enabled**</span></span> <br/> |<span data-ttu-id="eb37e-117">Un valor booleano que indica si la característica de seguimiento de canalización está habilitada para el servidor de acceso de cliente o de buzones.</span><span class="sxs-lookup"><span data-stu-id="eb37e-117">A Boolean value that indicates whether the pipeline tracing feature is enabled for the Client Access or the Mailbox server.</span></span> <span data-ttu-id="eb37e-118">El valor es **true** si está habilitado el seguimiento de canalización; de lo contrario, el valor es **false** o el elemento no está presente.</span><span class="sxs-lookup"><span data-stu-id="eb37e-118">The value is **true** if pipeline tracing is enabled; otherwise, the value is **false** or the element is not present.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="eb37e-119">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="eb37e-119">Child elements</span></span>

<span data-ttu-id="eb37e-120">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="eb37e-120">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="eb37e-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="eb37e-121">Parent elements</span></span>

|<span data-ttu-id="eb37e-122">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="eb37e-122">**Element**</span></span>|<span data-ttu-id="eb37e-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="eb37e-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="eb37e-124">monitor</span><span class="sxs-lookup"><span data-stu-id="eb37e-124">monitoring</span></span>](monitoring.md) <br/> |<span data-ttu-id="eb37e-125">Contiene información de configuración que define cómo y cuándo el servicio de transporte supervisa los agentes que están instalados.</span><span class="sxs-lookup"><span data-stu-id="eb37e-125">Contains configuration information that defines how and when the transport service monitors agents that are installed.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="eb37e-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="eb37e-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="eb37e-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="eb37e-127">Namespace</span></span>  <br/> |<span data-ttu-id="eb37e-128">Este archivo no define un espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="eb37e-128">This file does not define a namespace.</span></span>  <br/> |
|<span data-ttu-id="eb37e-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="eb37e-129">Schema Name</span></span>  <br/> |<span data-ttu-id="eb37e-130">No disponible.</span><span class="sxs-lookup"><span data-stu-id="eb37e-130">Not available.</span></span>  <br/> |
|<span data-ttu-id="eb37e-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="eb37e-131">Validation File</span></span>  <br/> |<span data-ttu-id="eb37e-132">No disponible.</span><span class="sxs-lookup"><span data-stu-id="eb37e-132">Not available.</span></span>  <br/> |
|<span data-ttu-id="eb37e-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="eb37e-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="eb37e-134">Falso.</span><span class="sxs-lookup"><span data-stu-id="eb37e-134">False.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="eb37e-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="eb37e-135">See also</span></span>

- [<span data-ttu-id="eb37e-136">Elementos del archivo de configuración de agentes para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="eb37e-136">Agents configuration file elements for Exchange 2013</span></span>](agents-configuration-file-elements-for-exchange-2013.md)

