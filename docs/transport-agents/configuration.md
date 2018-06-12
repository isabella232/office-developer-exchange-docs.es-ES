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
ms.openlocfilehash: 342e52e879534b6a130d286d358138c6095e4563
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763345"
---
# <a name="configuration"></a><span data-ttu-id="08723-103">configuración</span><span class="sxs-lookup"><span data-stu-id="08723-103">configuration</span></span>
  
<span data-ttu-id="08723-104">**Se aplica a:** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="08723-104">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="08723-105">El elemento de **configuración** es el elemento raíz para el archivo de configuración de los agentes.</span><span class="sxs-lookup"><span data-stu-id="08723-105">The **configuration** element is the root element for the agents configuration file.</span></span> 
  
- [<span data-ttu-id="08723-106">configuración</span><span class="sxs-lookup"><span data-stu-id="08723-106">configuration</span></span>](configuration.md) 
- [<span data-ttu-id="08723-107">mexRuntime</span><span class="sxs-lookup"><span data-stu-id="08723-107">mexRuntime</span></span>](mexruntime.md)
  
```XML
<configuration>
      <mexRuntime/>
</configuration>
```

<span data-ttu-id="08723-108">**configurationType (complexType)**</span><span class="sxs-lookup"><span data-stu-id="08723-108">**configurationType (complexType)**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="08723-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="08723-109">Attributes and elements</span></span>

<span data-ttu-id="08723-110">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="08723-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="08723-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="08723-111">Attributes</span></span>

<span data-ttu-id="08723-112">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="08723-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="08723-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="08723-113">Child elements</span></span>

|<span data-ttu-id="08723-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="08723-114">**Element**</span></span>|<span data-ttu-id="08723-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="08723-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="08723-116">mexRuntime</span><span class="sxs-lookup"><span data-stu-id="08723-116">mexRuntime</span></span>](mexruntime.md) <br/> |<span data-ttu-id="08723-117">Contiene elementos que definen la información de configuración de supervisión del agente y la información de configuración de SMTP y agentes de enrutamiento que se instalan.</span><span class="sxs-lookup"><span data-stu-id="08723-117">Contains elements that define configuration information for agent monitoring and configuration information for SMTP and routing agents that are installed.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="08723-118">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="08723-118">Parent elements</span></span>

<span data-ttu-id="08723-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="08723-119">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="08723-120">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="08723-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="08723-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="08723-121">Namespace</span></span>  <br/> |<span data-ttu-id="08723-122">Este archivo no define un espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="08723-122">This file does not define a namespace.</span></span>  <br/> |
|<span data-ttu-id="08723-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="08723-123">Schema Name</span></span>  <br/> |<span data-ttu-id="08723-124">No está disponible.</span><span class="sxs-lookup"><span data-stu-id="08723-124">Not available.</span></span>  <br/> |
|<span data-ttu-id="08723-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="08723-125">Validation File</span></span>  <br/> |<span data-ttu-id="08723-126">No está disponible.</span><span class="sxs-lookup"><span data-stu-id="08723-126">Not available.</span></span>  <br/> |
|<span data-ttu-id="08723-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="08723-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="08723-128">Falso.</span><span class="sxs-lookup"><span data-stu-id="08723-128">False.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="08723-129">Ver también</span><span class="sxs-lookup"><span data-stu-id="08723-129">See also</span></span>

- [<span data-ttu-id="08723-130">Elementos del archivo de configuración de los agentes para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="08723-130">Agents configuration file elements for Exchange 2013</span></span>](agents-configuration-file-elements-for-exchange-2013.md)

