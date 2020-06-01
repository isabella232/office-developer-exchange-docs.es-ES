---
title: configuración
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- configuration
api_type:
- schema
ms.assetid: 6fc04e4d-657a-4999-9431-186ccb7832b5
description: 'Última modificación: 17 de septiembre de 2015'
ms.openlocfilehash: b886851b9a0c17d58428f49281d664930d0e4070
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461565"
---
# <a name="configuration"></a><span data-ttu-id="7a6ec-103">configuración</span><span class="sxs-lookup"><span data-stu-id="7a6ec-103">configuration</span></span>
  
<span data-ttu-id="7a6ec-104">**Se aplica a:** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="7a6ec-104">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="7a6ec-105">El elemento **Configuration** es el elemento raíz del archivo de configuración de agentes.</span><span class="sxs-lookup"><span data-stu-id="7a6ec-105">The **configuration** element is the root element for the agents configuration file.</span></span> 
  
- [<span data-ttu-id="7a6ec-106">configuración</span><span class="sxs-lookup"><span data-stu-id="7a6ec-106">configuration</span></span>](configuration.md) 
- [<span data-ttu-id="7a6ec-107">mexRuntime</span><span class="sxs-lookup"><span data-stu-id="7a6ec-107">mexRuntime</span></span>](mexruntime.md)
  
```XML
<configuration>
      <mexRuntime/>
</configuration>
```

<span data-ttu-id="7a6ec-108">**configurationType (complexType)**</span><span class="sxs-lookup"><span data-stu-id="7a6ec-108">**configurationType (complexType)**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="7a6ec-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="7a6ec-109">Attributes and elements</span></span>

<span data-ttu-id="7a6ec-110">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="7a6ec-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7a6ec-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="7a6ec-111">Attributes</span></span>

<span data-ttu-id="7a6ec-112">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="7a6ec-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7a6ec-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7a6ec-113">Child elements</span></span>

|<span data-ttu-id="7a6ec-114">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7a6ec-114">**Element**</span></span>|<span data-ttu-id="7a6ec-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7a6ec-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7a6ec-116">mexRuntime</span><span class="sxs-lookup"><span data-stu-id="7a6ec-116">mexRuntime</span></span>](mexruntime.md) <br/> |<span data-ttu-id="7a6ec-117">Contiene elementos que definen la información de configuración para la supervisión de agentes y la información de configuración para SMTP y los agentes de enrutamiento que están instalados.</span><span class="sxs-lookup"><span data-stu-id="7a6ec-117">Contains elements that define configuration information for agent monitoring and configuration information for SMTP and routing agents that are installed.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7a6ec-118">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7a6ec-118">Parent elements</span></span>

<span data-ttu-id="7a6ec-119">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="7a6ec-119">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7a6ec-120">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7a6ec-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7a6ec-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="7a6ec-121">Namespace</span></span>  <br/> |<span data-ttu-id="7a6ec-122">Este archivo no define un espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="7a6ec-122">This file does not define a namespace.</span></span>  <br/> |
|<span data-ttu-id="7a6ec-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="7a6ec-123">Schema Name</span></span>  <br/> |<span data-ttu-id="7a6ec-124">No disponible.</span><span class="sxs-lookup"><span data-stu-id="7a6ec-124">Not available.</span></span>  <br/> |
|<span data-ttu-id="7a6ec-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="7a6ec-125">Validation File</span></span>  <br/> |<span data-ttu-id="7a6ec-126">No disponible.</span><span class="sxs-lookup"><span data-stu-id="7a6ec-126">Not available.</span></span>  <br/> |
|<span data-ttu-id="7a6ec-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="7a6ec-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="7a6ec-128">Falso.</span><span class="sxs-lookup"><span data-stu-id="7a6ec-128">False.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7a6ec-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="7a6ec-129">See also</span></span>

- [<span data-ttu-id="7a6ec-130">Elementos del archivo de configuración de agentes para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="7a6ec-130">Agents configuration file elements for Exchange 2013</span></span>](agents-configuration-file-elements-for-exchange-2013.md)

