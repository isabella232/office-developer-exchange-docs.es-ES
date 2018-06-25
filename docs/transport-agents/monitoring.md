---
title: supervisión
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
ms.openlocfilehash: 1b5484467def0bf3d22ba0707357977d5ed461ff
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763371"
---
# <a name="monitoring"></a><span data-ttu-id="6e715-103">supervisión</span><span class="sxs-lookup"><span data-stu-id="6e715-103">monitoring</span></span>
  
<span data-ttu-id="6e715-104">**Se aplica a:** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="6e715-104">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="6e715-105">El elemento de **supervisión** contiene información de configuración que define cómo y cuándo el servicio de transporte de Front-End o el servicio de transporte supervisa a los agentes que se instalan.</span><span class="sxs-lookup"><span data-stu-id="6e715-105">The **monitoring** element contains configuration information that defines how and when the Front End transport service or the Transport service monitors agents that are installed.</span></span> 
  
- [<span data-ttu-id="6e715-106">configuración</span><span class="sxs-lookup"><span data-stu-id="6e715-106">configuration</span></span>](configuration.md)  
- [<span data-ttu-id="6e715-107">mexRuntime</span><span class="sxs-lookup"><span data-stu-id="6e715-107">mexRuntime</span></span>](mexruntime.md)  
- [<span data-ttu-id="6e715-108">supervisión</span><span class="sxs-lookup"><span data-stu-id="6e715-108">monitoring</span></span>](monitoring.md)
  
```XML
<monitoring>
   <agentExecution/>
   <messageSnapshot/>
</monitoring>
```

<span data-ttu-id="6e715-109">**monitoringType (complexType)**</span><span class="sxs-lookup"><span data-stu-id="6e715-109">**monitoringType (complexType)**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="6e715-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="6e715-110">Attributes and elements</span></span>

<span data-ttu-id="6e715-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="6e715-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6e715-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="6e715-112">Attributes</span></span>

<span data-ttu-id="6e715-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="6e715-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6e715-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6e715-114">Child elements</span></span>

|<span data-ttu-id="6e715-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="6e715-115">**Element**</span></span>|<span data-ttu-id="6e715-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6e715-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6e715-117">agentExecution</span><span class="sxs-lookup"><span data-stu-id="6e715-117">agentExecution</span></span>](agentexecution.md) <br/> |<span data-ttu-id="6e715-118">Define el tiempo, en milisegundos, para el acceso de cliente o el servidor de buzones que hay que esperar un agente devolver desde un evento antes de que escribe en el registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="6e715-118">Defines the time, in milliseconds, for the Client Access or the Mailbox server to wait for an agent to return from an event before it writes to the event log.</span></span>  <br/> |
|[<span data-ttu-id="6e715-119">messageSnapshot</span><span class="sxs-lookup"><span data-stu-id="6e715-119">messageSnapshot</span></span>](messagesnapshot.md) <br/> |<span data-ttu-id="6e715-120">Contiene un atributo que especifica si está habilitada la característica de seguimiento de canalización para el acceso de cliente o el servidor de buzones.</span><span class="sxs-lookup"><span data-stu-id="6e715-120">Contains an attribute that specifies whether the pipeline tracing feature is enabled for the Client Access or the Mailbox server.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6e715-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6e715-121">Parent elements</span></span>

|<span data-ttu-id="6e715-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="6e715-122">**Element**</span></span>|<span data-ttu-id="6e715-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6e715-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6e715-124">mexRuntime</span><span class="sxs-lookup"><span data-stu-id="6e715-124">mexRuntime</span></span>](mexruntime.md) <br/> |<span data-ttu-id="6e715-125">Contiene elementos que definen la información de configuración de supervisión del agente y la información de configuración de SMTP y agentes de enrutamiento que se instalan.</span><span class="sxs-lookup"><span data-stu-id="6e715-125">Contains elements that define configuration information for agent monitoring and configuration information for SMTP and routing agents that are installed.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="6e715-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="6e715-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6e715-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6e715-127">Namespace</span></span>  <br/> |<span data-ttu-id="6e715-128">Este archivo no define un espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="6e715-128">This file does not define a namespace.</span></span>  <br/> |
|<span data-ttu-id="6e715-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="6e715-129">Schema Name</span></span>  <br/> |<span data-ttu-id="6e715-130">No está disponible.</span><span class="sxs-lookup"><span data-stu-id="6e715-130">Not available.</span></span>  <br/> |
|<span data-ttu-id="6e715-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="6e715-131">Validation File</span></span>  <br/> |<span data-ttu-id="6e715-132">No está disponible.</span><span class="sxs-lookup"><span data-stu-id="6e715-132">Not available.</span></span>  <br/> |
|<span data-ttu-id="6e715-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="6e715-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="6e715-134">Falso.</span><span class="sxs-lookup"><span data-stu-id="6e715-134">False.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6e715-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="6e715-135">See also</span></span>

- [<span data-ttu-id="6e715-136">Elementos del archivo de configuración de los agentes para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="6e715-136">Agents configuration file elements for Exchange 2013</span></span>](agents-configuration-file-elements-for-exchange-2013.md)

