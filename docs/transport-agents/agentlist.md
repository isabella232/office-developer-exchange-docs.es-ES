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
ms.openlocfilehash: 99e4e24c3bca77c7e7d5f2c59bb21cee1317fed2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44446395"
---
# <a name="agentlist"></a><span data-ttu-id="22bc5-103">agentList</span><span class="sxs-lookup"><span data-stu-id="22bc5-103">agentList</span></span>
  
<span data-ttu-id="22bc5-104">**Se aplica a:** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="22bc5-104">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="22bc5-105">El elemento **agentList** contiene un elemento [Agent](agent.md) para cada agente instalado.</span><span class="sxs-lookup"><span data-stu-id="22bc5-105">The **agentList** element contains an [agent](agent.md) element for each installed agent.</span></span> 
  
- [<span data-ttu-id="22bc5-106">configuración</span><span class="sxs-lookup"><span data-stu-id="22bc5-106">configuration</span></span>](configuration.md)
- [<span data-ttu-id="22bc5-107">mexRuntime</span><span class="sxs-lookup"><span data-stu-id="22bc5-107">mexRuntime</span></span>](mexruntime.md)
- [<span data-ttu-id="22bc5-108">agentList</span><span class="sxs-lookup"><span data-stu-id="22bc5-108">agentList</span></span>](agentlist.md)
  
```XML
<agentList>
      <agent/>
</agentList>
```

<span data-ttu-id="22bc5-109">**agentListType (complexType)**</span><span class="sxs-lookup"><span data-stu-id="22bc5-109">**agentListType (complexType)**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="22bc5-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="22bc5-110">Attributes and elements</span></span>

<span data-ttu-id="22bc5-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="22bc5-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="22bc5-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="22bc5-112">Attributes</span></span>

<span data-ttu-id="22bc5-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="22bc5-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="22bc5-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="22bc5-114">Child elements</span></span>

|<span data-ttu-id="22bc5-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="22bc5-115">**Element**</span></span>|<span data-ttu-id="22bc5-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="22bc5-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="22bc5-117">Representante</span><span class="sxs-lookup"><span data-stu-id="22bc5-117">agent</span></span>](agent.md) <br/> |<span data-ttu-id="22bc5-118">Contiene información de configuración acerca de un agente instalado.</span><span class="sxs-lookup"><span data-stu-id="22bc5-118">Contains configuration information about an installed agent.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="22bc5-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="22bc5-119">Parent elements</span></span>

|<span data-ttu-id="22bc5-120">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="22bc5-120">**Element**</span></span>|<span data-ttu-id="22bc5-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="22bc5-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="22bc5-122">mexRuntime</span><span class="sxs-lookup"><span data-stu-id="22bc5-122">mexRuntime</span></span>](mexruntime.md) <br/> |<span data-ttu-id="22bc5-123">Contiene elementos que definen la información de configuración para la supervisión de agentes y la información de configuración acerca de los agentes instalados.</span><span class="sxs-lookup"><span data-stu-id="22bc5-123">Contains elements that define configuration information for agent monitoring and configuration information about installed agents.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="22bc5-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="22bc5-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="22bc5-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="22bc5-125">Namespace</span></span>  <br/> |<span data-ttu-id="22bc5-126">Este archivo no define un espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="22bc5-126">This file does not define a namespace.</span></span>  <br/> |
|<span data-ttu-id="22bc5-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="22bc5-127">Schema Name</span></span>  <br/> |<span data-ttu-id="22bc5-128">No disponible.</span><span class="sxs-lookup"><span data-stu-id="22bc5-128">Not available.</span></span>  <br/> |
|<span data-ttu-id="22bc5-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="22bc5-129">Validation File</span></span>  <br/> |<span data-ttu-id="22bc5-130">No disponible.</span><span class="sxs-lookup"><span data-stu-id="22bc5-130">Not available.</span></span>  <br/> |
|<span data-ttu-id="22bc5-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="22bc5-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="22bc5-132">Falso.</span><span class="sxs-lookup"><span data-stu-id="22bc5-132">False.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="22bc5-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="22bc5-133">See also</span></span>

- [<span data-ttu-id="22bc5-134">Elementos del archivo de configuración de agentes para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="22bc5-134">Agents configuration file elements for Exchange 2013</span></span>](agents-configuration-file-elements-for-exchange-2013.md)

