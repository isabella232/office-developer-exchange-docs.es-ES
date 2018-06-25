---
title: mexRuntime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- mexRuntime
api_type:
- schema
ms.assetid: eabb2f12-10a7-4ce2-ae4b-9c04010c765f
description: 'Última modificación: 17 de septiembre de 2015'
ms.openlocfilehash: 4a34eedfc16d64cbfa67003ed23cf6eba2bb4bad
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763375"
---
# <a name="mexruntime"></a><span data-ttu-id="a6b6a-103">mexRuntime</span><span class="sxs-lookup"><span data-stu-id="a6b6a-103">mexRuntime</span></span>
  
<span data-ttu-id="a6b6a-104">**Se aplica a:** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="a6b6a-104">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="a6b6a-105">El elemento **mexRuntime** contiene elementos que definen la información de configuración de supervisión del agente y la información de configuración de SMTP y agentes de enrutamiento que se instalan.</span><span class="sxs-lookup"><span data-stu-id="a6b6a-105">The **mexRuntime** element contains elements that define configuration information for agent monitoring and configuration information for SMTP and routing agents that are installed.</span></span> 
  
- [<span data-ttu-id="a6b6a-106">configuración</span><span class="sxs-lookup"><span data-stu-id="a6b6a-106">configuration</span></span>](configuration.md)  
- [<span data-ttu-id="a6b6a-107">mexRuntime</span><span class="sxs-lookup"><span data-stu-id="a6b6a-107">mexRuntime</span></span>](mexruntime.md)
  
```XML
<mexRuntime>
   <monitoring/>
   <agentList/>
</mexRuntime>
```

<span data-ttu-id="a6b6a-108">**mexRuntimeType (complexType)**</span><span class="sxs-lookup"><span data-stu-id="a6b6a-108">**mexRuntimeType (complexType)**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="a6b6a-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a6b6a-109">Attributes and elements</span></span>

<span data-ttu-id="a6b6a-110">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a6b6a-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a6b6a-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="a6b6a-111">Attributes</span></span>

<span data-ttu-id="a6b6a-112">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a6b6a-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a6b6a-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a6b6a-113">Child elements</span></span>

|<span data-ttu-id="a6b6a-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="a6b6a-114">**Element**</span></span>|<span data-ttu-id="a6b6a-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a6b6a-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a6b6a-116">supervisión</span><span class="sxs-lookup"><span data-stu-id="a6b6a-116">monitoring</span></span>](monitoring.md) <br/> |<span data-ttu-id="a6b6a-117">Contiene información de configuración que define cómo y cuándo transporte supervisa a los agentes que se instalan.</span><span class="sxs-lookup"><span data-stu-id="a6b6a-117">Contains configuration information that defines how and when transport monitors agents that are installed.</span></span>  <br/> |
|[<span data-ttu-id="a6b6a-118">agentList</span><span class="sxs-lookup"><span data-stu-id="a6b6a-118">agentList</span></span>](agentlist.md) <br/> |<span data-ttu-id="a6b6a-119">Contiene un elemento de [agente](agent.md) para cada agente que se instala.</span><span class="sxs-lookup"><span data-stu-id="a6b6a-119">Contains an [agent](agent.md) element for each agent that is installed.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a6b6a-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a6b6a-120">Parent elements</span></span>

|<span data-ttu-id="a6b6a-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="a6b6a-121">**Element**</span></span>|<span data-ttu-id="a6b6a-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a6b6a-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a6b6a-123">configuración</span><span class="sxs-lookup"><span data-stu-id="a6b6a-123">configuration</span></span>](configuration.md) <br/> |<span data-ttu-id="a6b6a-124">El elemento raíz para el archivo de configuración de los agentes.</span><span class="sxs-lookup"><span data-stu-id="a6b6a-124">The root element for the agents configuration file.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="a6b6a-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a6b6a-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a6b6a-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a6b6a-126">Namespace</span></span>  <br/> |<span data-ttu-id="a6b6a-127">Este archivo no define un espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="a6b6a-127">This file does not define a namespace.</span></span>  <br/> |
|<span data-ttu-id="a6b6a-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a6b6a-128">Schema Name</span></span>  <br/> |<span data-ttu-id="a6b6a-129">No está disponible.</span><span class="sxs-lookup"><span data-stu-id="a6b6a-129">Not available.</span></span>  <br/> |
|<span data-ttu-id="a6b6a-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a6b6a-130">Validation File</span></span>  <br/> |<span data-ttu-id="a6b6a-131">No está disponible.</span><span class="sxs-lookup"><span data-stu-id="a6b6a-131">Not available.</span></span>  <br/> |
|<span data-ttu-id="a6b6a-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a6b6a-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="a6b6a-133">Falso.</span><span class="sxs-lookup"><span data-stu-id="a6b6a-133">False.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a6b6a-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="a6b6a-134">See also</span></span>

- [<span data-ttu-id="a6b6a-135">Elementos del archivo de configuración de los agentes para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="a6b6a-135">Agents configuration file elements for Exchange 2013</span></span>](agents-configuration-file-elements-for-exchange-2013.md)

