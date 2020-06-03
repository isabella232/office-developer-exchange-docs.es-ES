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
ms.openlocfilehash: 457257e59fb37659daf2f91b0fa5dfced5c48c03
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44446493"
---
# <a name="agentexecution"></a><span data-ttu-id="02326-103">agentExecution</span><span class="sxs-lookup"><span data-stu-id="02326-103">agentExecution</span></span>
  
<span data-ttu-id="02326-104">**Se aplica a:** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="02326-104">**Applies to:** Exchange Server 2013</span></span> 
  
<span data-ttu-id="02326-105">El elemento **agentExecution** define el tiempo, en milisegundos, para que el servidor de acceso de cliente o de buzones de correo espere a que un agente vuelva de un evento antes de escribir en el registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="02326-105">The **agentExecution** element defines the time, in milliseconds, for the Client Access or Mailbox server to wait for an agent to return from an event before it writes to the event log.</span></span> 
  
- [<span data-ttu-id="02326-106">configuración</span><span class="sxs-lookup"><span data-stu-id="02326-106">configuration</span></span>](configuration.md)  
- [<span data-ttu-id="02326-107">monitor</span><span class="sxs-lookup"><span data-stu-id="02326-107">monitoring</span></span>](monitoring.md)
- [<span data-ttu-id="02326-108">agentExecution</span><span class="sxs-lookup"><span data-stu-id="02326-108">agentExecution</span></span>](agentexecution.md)
  
```XML
<agentExecution timeLimitInMilliseconds="" />
```

<span data-ttu-id="02326-109">**agentExecutionType (complexType)**</span><span class="sxs-lookup"><span data-stu-id="02326-109">**agentExecutionType (complexType)**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="02326-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="02326-110">Attributes and elements</span></span>

<span data-ttu-id="02326-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="02326-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="02326-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="02326-112">Attributes</span></span>

|<span data-ttu-id="02326-113">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="02326-113">**Attribute**</span></span>|<span data-ttu-id="02326-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="02326-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="02326-115">**timeLimitInMilliseconds**</span><span class="sxs-lookup"><span data-stu-id="02326-115">**timeLimitInMilliseconds**</span></span> <br/> |<span data-ttu-id="02326-116">Un valor entero positivo que especifica el tiempo en milisegundos que debe transcurrir para que el servidor espere a que un agente vuelva de un evento antes de escribir una advertencia en el registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="02326-116">A positive integer value that specifies the time, in milliseconds, for the server to wait for an agent to return from an event before it writes a warning to the event log.</span></span> <span data-ttu-id="02326-117">El rendimiento puede disminuir si este valor es demasiado pequeño.</span><span class="sxs-lookup"><span data-stu-id="02326-117">Performance can decrease if this value is too small.</span></span> <span data-ttu-id="02326-118">El valor sugerido para este atributo es 300.000, que equivale a 5 minutos.</span><span class="sxs-lookup"><span data-stu-id="02326-118">The suggested value for this attribute is 300,000, which equates to 5 minutes.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="02326-119">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="02326-119">Child elements</span></span>

<span data-ttu-id="02326-120">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="02326-120">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="02326-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="02326-121">Parent elements</span></span>

|<span data-ttu-id="02326-122">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="02326-122">**Element**</span></span>|<span data-ttu-id="02326-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="02326-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="02326-124">monitor</span><span class="sxs-lookup"><span data-stu-id="02326-124">monitoring</span></span>](monitoring.md) <br/> |<span data-ttu-id="02326-125">Contiene información de configuración que define cómo y cuándo el servicio de transporte front-end o el servicio de transporte supervisa los agentes que están instalados.</span><span class="sxs-lookup"><span data-stu-id="02326-125">Contains configuration information that defines how and when the Front End Transport service or the Transport service monitors agents that are installed.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="02326-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="02326-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="02326-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="02326-127">Namespace</span></span>  <br/> |<span data-ttu-id="02326-128">Este archivo no define un espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="02326-128">This file does not define a namespace.</span></span>  <br/> |
|<span data-ttu-id="02326-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="02326-129">Schema Name</span></span>  <br/> |<span data-ttu-id="02326-130">No disponible.</span><span class="sxs-lookup"><span data-stu-id="02326-130">Not available.</span></span>  <br/> |
|<span data-ttu-id="02326-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="02326-131">Validation File</span></span>  <br/> |<span data-ttu-id="02326-132">No disponible.</span><span class="sxs-lookup"><span data-stu-id="02326-132">Not available.</span></span>  <br/> |
|<span data-ttu-id="02326-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="02326-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="02326-134">Falso.</span><span class="sxs-lookup"><span data-stu-id="02326-134">False.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="02326-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="02326-135">See also</span></span>

- [<span data-ttu-id="02326-136">Elementos del archivo de configuración de agentes para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="02326-136">Agents configuration file elements for Exchange 2013</span></span>](agents-configuration-file-elements-for-exchange-2013.md)

