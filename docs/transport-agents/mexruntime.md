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
ms.openlocfilehash: f192965a8375eb46d1ca5b46d3b768a3299c284d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461838"
---
# <a name="mexruntime"></a><span data-ttu-id="64ce3-103">mexRuntime</span><span class="sxs-lookup"><span data-stu-id="64ce3-103">mexRuntime</span></span>
  
<span data-ttu-id="64ce3-104">**Se aplica a:** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="64ce3-104">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="64ce3-105">El elemento **mexRuntime** contiene elementos que definen la información de configuración para la supervisión de agentes y la información de configuración para SMTP y los agentes de enrutamiento que están instalados.</span><span class="sxs-lookup"><span data-stu-id="64ce3-105">The **mexRuntime** element contains elements that define configuration information for agent monitoring and configuration information for SMTP and routing agents that are installed.</span></span> 
  
- [<span data-ttu-id="64ce3-106">configuración</span><span class="sxs-lookup"><span data-stu-id="64ce3-106">configuration</span></span>](configuration.md)  
- [<span data-ttu-id="64ce3-107">mexRuntime</span><span class="sxs-lookup"><span data-stu-id="64ce3-107">mexRuntime</span></span>](mexruntime.md)
  
```XML
<mexRuntime>
   <monitoring/>
   <agentList/>
</mexRuntime>
```

<span data-ttu-id="64ce3-108">**mexRuntimeType (complexType)**</span><span class="sxs-lookup"><span data-stu-id="64ce3-108">**mexRuntimeType (complexType)**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="64ce3-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="64ce3-109">Attributes and elements</span></span>

<span data-ttu-id="64ce3-110">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="64ce3-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="64ce3-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="64ce3-111">Attributes</span></span>

<span data-ttu-id="64ce3-112">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="64ce3-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="64ce3-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="64ce3-113">Child elements</span></span>

|<span data-ttu-id="64ce3-114">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="64ce3-114">**Element**</span></span>|<span data-ttu-id="64ce3-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="64ce3-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="64ce3-116">monitor</span><span class="sxs-lookup"><span data-stu-id="64ce3-116">monitoring</span></span>](monitoring.md) <br/> |<span data-ttu-id="64ce3-117">Contiene información de configuración que define cómo y cuándo transporte los agentes instalados.</span><span class="sxs-lookup"><span data-stu-id="64ce3-117">Contains configuration information that defines how and when transport monitors agents that are installed.</span></span>  <br/> |
|[<span data-ttu-id="64ce3-118">agentList</span><span class="sxs-lookup"><span data-stu-id="64ce3-118">agentList</span></span>](agentlist.md) <br/> |<span data-ttu-id="64ce3-119">Contiene un elemento [Agent](agent.md) para cada agente instalado.</span><span class="sxs-lookup"><span data-stu-id="64ce3-119">Contains an [agent](agent.md) element for each agent that is installed.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="64ce3-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="64ce3-120">Parent elements</span></span>

|<span data-ttu-id="64ce3-121">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="64ce3-121">**Element**</span></span>|<span data-ttu-id="64ce3-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="64ce3-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="64ce3-123">configuración</span><span class="sxs-lookup"><span data-stu-id="64ce3-123">configuration</span></span>](configuration.md) <br/> |<span data-ttu-id="64ce3-124">El elemento raíz del archivo de configuración de agentes.</span><span class="sxs-lookup"><span data-stu-id="64ce3-124">The root element for the agents configuration file.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="64ce3-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="64ce3-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="64ce3-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="64ce3-126">Namespace</span></span>  <br/> |<span data-ttu-id="64ce3-127">Este archivo no define un espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="64ce3-127">This file does not define a namespace.</span></span>  <br/> |
|<span data-ttu-id="64ce3-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="64ce3-128">Schema Name</span></span>  <br/> |<span data-ttu-id="64ce3-129">No disponible.</span><span class="sxs-lookup"><span data-stu-id="64ce3-129">Not available.</span></span>  <br/> |
|<span data-ttu-id="64ce3-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="64ce3-130">Validation File</span></span>  <br/> |<span data-ttu-id="64ce3-131">No disponible.</span><span class="sxs-lookup"><span data-stu-id="64ce3-131">Not available.</span></span>  <br/> |
|<span data-ttu-id="64ce3-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="64ce3-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="64ce3-133">Falso.</span><span class="sxs-lookup"><span data-stu-id="64ce3-133">False.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="64ce3-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="64ce3-134">See also</span></span>

- [<span data-ttu-id="64ce3-135">Elementos del archivo de configuración de agentes para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="64ce3-135">Agents configuration file elements for Exchange 2013</span></span>](agents-configuration-file-elements-for-exchange-2013.md)

