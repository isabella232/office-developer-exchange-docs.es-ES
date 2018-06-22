---
title: DelegationState
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DelegationState
api_type:
- schema
ms.assetid: 9dbb83ed-1ded-48f3-8e06-2489fc8b28d5
description: El elemento DelegationState representa el estado de una tarea delegada.
ms.openlocfilehash: 00b0e41ae223f1c70f9a3a21662e8858f8690a86
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764072"
---
# <a name="delegationstate"></a><span data-ttu-id="99131-103">DelegationState</span><span class="sxs-lookup"><span data-stu-id="99131-103">DelegationState</span></span>

<span data-ttu-id="99131-104">El elemento **DelegationState** representa el estado de una tarea delegada.</span><span class="sxs-lookup"><span data-stu-id="99131-104">The **DelegationState** element represents the status of a delegated task.</span></span> 
  
```xml
<DelegationState/>
```

<span data-ttu-id="99131-105">**TaskDelegateStateType**</span><span class="sxs-lookup"><span data-stu-id="99131-105">**TaskDelegateStateType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="99131-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="99131-106">Attributes and elements</span></span>

<span data-ttu-id="99131-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="99131-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="99131-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="99131-108">Attributes</span></span>

<span data-ttu-id="99131-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="99131-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="99131-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="99131-110">Child elements</span></span>

<span data-ttu-id="99131-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="99131-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="99131-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="99131-112">Parent elements</span></span>

|<span data-ttu-id="99131-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="99131-113">**Element**</span></span>|<span data-ttu-id="99131-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="99131-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="99131-115">Tarea</span><span class="sxs-lookup"><span data-stu-id="99131-115">Task</span></span>](task.md) <br/> |<span data-ttu-id="99131-116">Representa una tarea en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="99131-116">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="99131-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="99131-117">Text value</span></span>

<span data-ttu-id="99131-118">Se trata de una propiedad de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="99131-118">This is a read-only property.</span></span> <span data-ttu-id="99131-119">Los valores posibles son:</span><span class="sxs-lookup"><span data-stu-id="99131-119">The following are the possible values:</span></span>
  
- <span data-ttu-id="99131-120">NoMatch</span><span class="sxs-lookup"><span data-stu-id="99131-120">NoMatch</span></span>
    
- <span data-ttu-id="99131-121">OwnNew</span><span class="sxs-lookup"><span data-stu-id="99131-121">OwnNew</span></span>
    
- <span data-ttu-id="99131-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="99131-122">Owned</span></span>
    
- <span data-ttu-id="99131-123">Aceptado</span><span class="sxs-lookup"><span data-stu-id="99131-123">Accepted</span></span>
    
- <span data-ttu-id="99131-124">Rechazado</span><span class="sxs-lookup"><span data-stu-id="99131-124">Declined</span></span>
    
- <span data-ttu-id="99131-125">Max</span><span class="sxs-lookup"><span data-stu-id="99131-125">Max</span></span>
    
## <a name="remarks"></a><span data-ttu-id="99131-126">Notas</span><span class="sxs-lookup"><span data-stu-id="99131-126">Remarks</span></span>

<span data-ttu-id="99131-127">Servicios Web de Exchange en Microsoft Exchange Server 2007 no es compatible con las asignaciones de tareas.</span><span class="sxs-lookup"><span data-stu-id="99131-127">Exchange Web Services in Microsoft Exchange Server 2007 does not support task assignments.</span></span>
  
<span data-ttu-id="99131-128">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Exchange 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="99131-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="99131-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="99131-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="99131-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="99131-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="99131-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="99131-131">Schema Name</span></span>  <br/> |<span data-ttu-id="99131-132">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="99131-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="99131-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="99131-133">Validation File</span></span>  <br/> |<span data-ttu-id="99131-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="99131-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="99131-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="99131-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="99131-136">False</span><span class="sxs-lookup"><span data-stu-id="99131-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="99131-137">Ver también</span><span class="sxs-lookup"><span data-stu-id="99131-137">See also</span></span>

- [<span data-ttu-id="99131-138">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="99131-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

