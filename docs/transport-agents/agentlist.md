---
title: agentList
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- agentList
api_type:
- schema
ms.assetid: e877b7ef-e303-4270-964d-8d116ff2a865
description: 'Última modificación: 17 de septiembre de 2015'
ms.openlocfilehash: 7dd9d48356932c82dbc048a85b9f02437c6366de
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763343"
---
# <a name="agentlist"></a><span data-ttu-id="37e2d-103">agentList</span><span class="sxs-lookup"><span data-stu-id="37e2d-103">agentList</span></span>
  
<span data-ttu-id="37e2d-104">**Se aplica a:** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="37e2d-104">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="37e2d-105">El elemento **agentList** contiene un elemento de [agente](agent.md) para cada agente instalado.</span><span class="sxs-lookup"><span data-stu-id="37e2d-105">The **agentList** element contains an [agent](agent.md) element for each installed agent.</span></span> 
  
- [<span data-ttu-id="37e2d-106">configuración</span><span class="sxs-lookup"><span data-stu-id="37e2d-106">configuration</span></span>](configuration.md)
- [<span data-ttu-id="37e2d-107">mexRuntime</span><span class="sxs-lookup"><span data-stu-id="37e2d-107">mexRuntime</span></span>](mexruntime.md)
- [<span data-ttu-id="37e2d-108">agentList</span><span class="sxs-lookup"><span data-stu-id="37e2d-108">agentList</span></span>](agentlist.md)
  
```XML
<agentList>
      <agent/>
</agentList>
```

<span data-ttu-id="37e2d-109">**agentListType (complexType)**</span><span class="sxs-lookup"><span data-stu-id="37e2d-109">**agentListType (complexType)**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="37e2d-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="37e2d-110">Attributes and elements</span></span>

<span data-ttu-id="37e2d-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="37e2d-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="37e2d-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="37e2d-112">Attributes</span></span>

<span data-ttu-id="37e2d-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="37e2d-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="37e2d-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="37e2d-114">Child elements</span></span>

|<span data-ttu-id="37e2d-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="37e2d-115">**Element**</span></span>|<span data-ttu-id="37e2d-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="37e2d-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="37e2d-117">agente</span><span class="sxs-lookup"><span data-stu-id="37e2d-117">agent</span></span>](agent.md) <br/> |<span data-ttu-id="37e2d-118">Contiene información de configuración acerca de un agente instalado.</span><span class="sxs-lookup"><span data-stu-id="37e2d-118">Contains configuration information about an installed agent.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="37e2d-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="37e2d-119">Parent elements</span></span>

|<span data-ttu-id="37e2d-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="37e2d-120">**Element**</span></span>|<span data-ttu-id="37e2d-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="37e2d-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="37e2d-122">mexRuntime</span><span class="sxs-lookup"><span data-stu-id="37e2d-122">mexRuntime</span></span>](mexruntime.md) <br/> |<span data-ttu-id="37e2d-123">Contiene elementos que definen la información de configuración de supervisión del agente y la información de configuración acerca de los agentes instalados.</span><span class="sxs-lookup"><span data-stu-id="37e2d-123">Contains elements that define configuration information for agent monitoring and configuration information about installed agents.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="37e2d-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="37e2d-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="37e2d-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="37e2d-125">Namespace</span></span>  <br/> |<span data-ttu-id="37e2d-126">Este archivo no define un espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="37e2d-126">This file does not define a namespace.</span></span>  <br/> |
|<span data-ttu-id="37e2d-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="37e2d-127">Schema Name</span></span>  <br/> |<span data-ttu-id="37e2d-128">No está disponible.</span><span class="sxs-lookup"><span data-stu-id="37e2d-128">Not available.</span></span>  <br/> |
|<span data-ttu-id="37e2d-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="37e2d-129">Validation File</span></span>  <br/> |<span data-ttu-id="37e2d-130">No está disponible.</span><span class="sxs-lookup"><span data-stu-id="37e2d-130">Not available.</span></span>  <br/> |
|<span data-ttu-id="37e2d-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="37e2d-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="37e2d-132">Falso.</span><span class="sxs-lookup"><span data-stu-id="37e2d-132">False.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="37e2d-133">Ver también</span><span class="sxs-lookup"><span data-stu-id="37e2d-133">See also</span></span>

- [<span data-ttu-id="37e2d-134">Elementos del archivo de configuración de los agentes para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="37e2d-134">Agents configuration file elements for Exchange 2013</span></span>](agents-configuration-file-elements-for-exchange-2013.md)

