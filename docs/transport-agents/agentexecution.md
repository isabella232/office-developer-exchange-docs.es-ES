---
title: agentExecution
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- agentExecution
api_type:
- schema
ms.assetid: 600c4690-941c-45af-a906-5528748d09cd
description: 'Última modificación: 17 de septiembre de 2015'
ms.openlocfilehash: 5848d52a68c8c3f747614015e49becb34bc4cfd8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763341"
---
# <a name="agentexecution"></a><span data-ttu-id="2eccd-103">agentExecution</span><span class="sxs-lookup"><span data-stu-id="2eccd-103">agentExecution</span></span>
  
<span data-ttu-id="2eccd-104">**Se aplica a:** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="2eccd-104">**Applies to:** Exchange Server 2013</span></span> 
  
<span data-ttu-id="2eccd-105">El elemento **agentExecution** define el tiempo, en milisegundos, para el servidor de acceso de cliente o buzón de correo que hay que esperar un agente devolver desde un evento antes de que escribe en el registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="2eccd-105">The **agentExecution** element defines the time, in milliseconds, for the Client Access or Mailbox server to wait for an agent to return from an event before it writes to the event log.</span></span> 
  
- [<span data-ttu-id="2eccd-106">configuración</span><span class="sxs-lookup"><span data-stu-id="2eccd-106">configuration</span></span>](configuration.md)  
- [<span data-ttu-id="2eccd-107">supervisión</span><span class="sxs-lookup"><span data-stu-id="2eccd-107">monitoring</span></span>](monitoring.md)
- [<span data-ttu-id="2eccd-108">agentExecution</span><span class="sxs-lookup"><span data-stu-id="2eccd-108">agentExecution</span></span>](agentexecution.md)
  
```XML
<agentExecution timeLimitInMilliseconds="" />
```

<span data-ttu-id="2eccd-109">**agentExecutionType (complexType)**</span><span class="sxs-lookup"><span data-stu-id="2eccd-109">**agentExecutionType (complexType)**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="2eccd-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="2eccd-110">Attributes and elements</span></span>

<span data-ttu-id="2eccd-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="2eccd-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2eccd-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="2eccd-112">Attributes</span></span>

|<span data-ttu-id="2eccd-113">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="2eccd-113">**Attribute**</span></span>|<span data-ttu-id="2eccd-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2eccd-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2eccd-115">**timeLimitInMilliseconds**</span><span class="sxs-lookup"><span data-stu-id="2eccd-115">**timeLimitInMilliseconds**</span></span> <br/> |<span data-ttu-id="2eccd-116">Un valor entero positivo que especifica el tiempo, en milisegundos, para el servidor que hay que esperar un agente devolver desde un evento antes de que escribe una advertencia en el registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="2eccd-116">A positive integer value that specifies the time, in milliseconds, for the server to wait for an agent to return from an event before it writes a warning to the event log.</span></span> <span data-ttu-id="2eccd-117">El rendimiento puede disminuir si este valor es demasiado pequeña.</span><span class="sxs-lookup"><span data-stu-id="2eccd-117">Performance can decrease if this value is too small.</span></span> <span data-ttu-id="2eccd-118">El valor sugerido para este atributo es 300.000, que equivale a 5 minutos.</span><span class="sxs-lookup"><span data-stu-id="2eccd-118">The suggested value for this attribute is 300,000, which equates to 5 minutes.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="2eccd-119">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2eccd-119">Child elements</span></span>

<span data-ttu-id="2eccd-120">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="2eccd-120">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2eccd-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="2eccd-121">Parent elements</span></span>

|<span data-ttu-id="2eccd-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="2eccd-122">**Element**</span></span>|<span data-ttu-id="2eccd-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2eccd-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2eccd-124">supervisión</span><span class="sxs-lookup"><span data-stu-id="2eccd-124">monitoring</span></span>](monitoring.md) <br/> |<span data-ttu-id="2eccd-125">Contiene información de configuración que define cómo y cuándo el servicio de transporte Front-End o el servicio de transporte supervisa a los agentes que se instalan.</span><span class="sxs-lookup"><span data-stu-id="2eccd-125">Contains configuration information that defines how and when the Front End Transport service or the Transport service monitors agents that are installed.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="2eccd-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="2eccd-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2eccd-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2eccd-127">Namespace</span></span>  <br/> |<span data-ttu-id="2eccd-128">Este archivo no define un espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="2eccd-128">This file does not define a namespace.</span></span>  <br/> |
|<span data-ttu-id="2eccd-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="2eccd-129">Schema Name</span></span>  <br/> |<span data-ttu-id="2eccd-130">No está disponible.</span><span class="sxs-lookup"><span data-stu-id="2eccd-130">Not available.</span></span>  <br/> |
|<span data-ttu-id="2eccd-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="2eccd-131">Validation File</span></span>  <br/> |<span data-ttu-id="2eccd-132">No está disponible.</span><span class="sxs-lookup"><span data-stu-id="2eccd-132">Not available.</span></span>  <br/> |
|<span data-ttu-id="2eccd-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="2eccd-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="2eccd-134">Falso.</span><span class="sxs-lookup"><span data-stu-id="2eccd-134">False.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2eccd-135">Ver también</span><span class="sxs-lookup"><span data-stu-id="2eccd-135">See also</span></span>

- [<span data-ttu-id="2eccd-136">Elementos del archivo de configuración de los agentes para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="2eccd-136">Agents configuration file elements for Exchange 2013</span></span>](agents-configuration-file-elements-for-exchange-2013.md)

