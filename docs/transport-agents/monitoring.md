---
title: monitor
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- monitoring
api_type:
- schema
ms.assetid: 350d7b46-9260-41a7-8613-3cb8cc1b29a5
description: 'Última modificación: 17 de septiembre de 2015'
ms.openlocfilehash: 5614ac2c6428da9b6845769a9335486d3ded5754
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455831"
---
# <a name="monitoring"></a><span data-ttu-id="7706d-103">monitor</span><span class="sxs-lookup"><span data-stu-id="7706d-103">monitoring</span></span>
  
<span data-ttu-id="7706d-104">**Se aplica a:** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="7706d-104">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="7706d-105">El elemento **Monitoring** contiene información de configuración que define cómo y cuándo el servicio de transporte front-end o el servicio de transporte supervisa los agentes que están instalados.</span><span class="sxs-lookup"><span data-stu-id="7706d-105">The **monitoring** element contains configuration information that defines how and when the Front End transport service or the Transport service monitors agents that are installed.</span></span> 
  
- [<span data-ttu-id="7706d-106">configuración</span><span class="sxs-lookup"><span data-stu-id="7706d-106">configuration</span></span>](configuration.md)  
- [<span data-ttu-id="7706d-107">mexRuntime</span><span class="sxs-lookup"><span data-stu-id="7706d-107">mexRuntime</span></span>](mexruntime.md)  
- [<span data-ttu-id="7706d-108">monitor</span><span class="sxs-lookup"><span data-stu-id="7706d-108">monitoring</span></span>](monitoring.md)
  
```XML
<monitoring>
   <agentExecution/>
   <messageSnapshot/>
</monitoring>
```

<span data-ttu-id="7706d-109">**monitoringType (complexType)**</span><span class="sxs-lookup"><span data-stu-id="7706d-109">**monitoringType (complexType)**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="7706d-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="7706d-110">Attributes and elements</span></span>

<span data-ttu-id="7706d-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="7706d-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7706d-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="7706d-112">Attributes</span></span>

<span data-ttu-id="7706d-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="7706d-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7706d-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7706d-114">Child elements</span></span>

|<span data-ttu-id="7706d-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7706d-115">**Element**</span></span>|<span data-ttu-id="7706d-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7706d-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7706d-117">agentExecution</span><span class="sxs-lookup"><span data-stu-id="7706d-117">agentExecution</span></span>](agentexecution.md) <br/> |<span data-ttu-id="7706d-118">Define el tiempo, en milisegundos, para el acceso de cliente o el servidor de buzones que se va a esperar a que un agente vuelva de un evento antes de escribir en el registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="7706d-118">Defines the time, in milliseconds, for the Client Access or the Mailbox server to wait for an agent to return from an event before it writes to the event log.</span></span>  <br/> |
|[<span data-ttu-id="7706d-119">messageSnapshot</span><span class="sxs-lookup"><span data-stu-id="7706d-119">messageSnapshot</span></span>](messagesnapshot.md) <br/> |<span data-ttu-id="7706d-120">Contiene un atributo que especifica si la característica de seguimiento de canalización está habilitada para el servidor de acceso de cliente o de buzones.</span><span class="sxs-lookup"><span data-stu-id="7706d-120">Contains an attribute that specifies whether the pipeline tracing feature is enabled for the Client Access or the Mailbox server.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7706d-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7706d-121">Parent elements</span></span>

|<span data-ttu-id="7706d-122">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7706d-122">**Element**</span></span>|<span data-ttu-id="7706d-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7706d-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7706d-124">mexRuntime</span><span class="sxs-lookup"><span data-stu-id="7706d-124">mexRuntime</span></span>](mexruntime.md) <br/> |<span data-ttu-id="7706d-125">Contiene elementos que definen la información de configuración para la supervisión de agentes y la información de configuración para SMTP y los agentes de enrutamiento que están instalados.</span><span class="sxs-lookup"><span data-stu-id="7706d-125">Contains elements that define configuration information for agent monitoring and configuration information for SMTP and routing agents that are installed.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="7706d-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7706d-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7706d-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="7706d-127">Namespace</span></span>  <br/> |<span data-ttu-id="7706d-128">Este archivo no define un espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="7706d-128">This file does not define a namespace.</span></span>  <br/> |
|<span data-ttu-id="7706d-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="7706d-129">Schema Name</span></span>  <br/> |<span data-ttu-id="7706d-130">No disponible.</span><span class="sxs-lookup"><span data-stu-id="7706d-130">Not available.</span></span>  <br/> |
|<span data-ttu-id="7706d-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="7706d-131">Validation File</span></span>  <br/> |<span data-ttu-id="7706d-132">No disponible.</span><span class="sxs-lookup"><span data-stu-id="7706d-132">Not available.</span></span>  <br/> |
|<span data-ttu-id="7706d-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="7706d-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="7706d-134">Falso.</span><span class="sxs-lookup"><span data-stu-id="7706d-134">False.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7706d-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="7706d-135">See also</span></span>

- [<span data-ttu-id="7706d-136">Elementos del archivo de configuración de agentes para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="7706d-136">Agents configuration file elements for Exchange 2013</span></span>](agents-configuration-file-elements-for-exchange-2013.md)

