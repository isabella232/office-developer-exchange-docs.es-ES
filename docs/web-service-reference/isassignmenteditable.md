---
title: IsAssignmentEditable
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsAssignmentEditable
api_type:
- schema
ms.assetid: 0ddf9181-f65e-4ad6-ad69-7b074ea0f2e7
description: El elemento IsAssignmentEditable representa el tipo de tarea.
ms.openlocfilehash: 5eb091b24e2c97f7aa6072044fed998b6c9c1651
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468057"
---
# <a name="isassignmenteditable"></a><span data-ttu-id="8d934-103">IsAssignmentEditable</span><span class="sxs-lookup"><span data-stu-id="8d934-103">IsAssignmentEditable</span></span>

<span data-ttu-id="8d934-104">El elemento **IsAssignmentEditable** representa el tipo de tarea.</span><span class="sxs-lookup"><span data-stu-id="8d934-104">The **IsAssignmentEditable** element represents the task type.</span></span> 
  
```xml
<IsAssignmentEditable/>
```

 <span data-ttu-id="8d934-105">**entero**</span><span class="sxs-lookup"><span data-stu-id="8d934-105">**integer**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8d934-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="8d934-106">Attributes and elements</span></span>

<span data-ttu-id="8d934-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="8d934-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8d934-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="8d934-108">Attributes</span></span>

<span data-ttu-id="8d934-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="8d934-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8d934-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8d934-110">Child elements</span></span>

<span data-ttu-id="8d934-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="8d934-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8d934-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="8d934-112">Parent elements</span></span>

|<span data-ttu-id="8d934-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="8d934-113">**Element**</span></span>|<span data-ttu-id="8d934-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8d934-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8d934-115">Tarea</span><span class="sxs-lookup"><span data-stu-id="8d934-115">Task</span></span>](task.md) <br/> |<span data-ttu-id="8d934-116">Representa una tarea del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="8d934-116">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="8d934-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="8d934-117">Text value</span></span>

<span data-ttu-id="8d934-118">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="8d934-118">This property is read-only.</span></span> <span data-ttu-id="8d934-119">En la siguiente tabla se enumeran los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="8d934-119">The following table lists the possible values.</span></span>
  
|<span data-ttu-id="8d934-120">**Valor**</span><span class="sxs-lookup"><span data-stu-id="8d934-120">**Value**</span></span>|<span data-ttu-id="8d934-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8d934-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8d934-122">comprendi</span><span class="sxs-lookup"><span data-stu-id="8d934-122">0</span></span>  <br/> |<span data-ttu-id="8d934-123">El valor predeterminado para todos los elementos de tarea.</span><span class="sxs-lookup"><span data-stu-id="8d934-123">The default for all task items.</span></span>  <br/> |
|<span data-ttu-id="8d934-124">1 </span><span class="sxs-lookup"><span data-stu-id="8d934-124">1</span></span>  <br/> |<span data-ttu-id="8d934-125">Una solicitud de tarea.</span><span class="sxs-lookup"><span data-stu-id="8d934-125">A task request.</span></span>  <br/> |
|<span data-ttu-id="8d934-126">segundo</span><span class="sxs-lookup"><span data-stu-id="8d934-126">2</span></span>  <br/> |<span data-ttu-id="8d934-127">Una aceptación de tarea de un destinatario de una solicitud de tarea.</span><span class="sxs-lookup"><span data-stu-id="8d934-127">A task acceptance from a recipient of a task request.</span></span>  <br/> |
|<span data-ttu-id="8d934-128">3</span><span class="sxs-lookup"><span data-stu-id="8d934-128">3</span></span>  <br/> |<span data-ttu-id="8d934-129">Disminución de una tarea de un destinatario de una solicitud de tarea.</span><span class="sxs-lookup"><span data-stu-id="8d934-129">A task declination from a recipient of a task request.</span></span>  <br/> |
|<span data-ttu-id="8d934-130">4 </span><span class="sxs-lookup"><span data-stu-id="8d934-130">4</span></span>  <br/> |<span data-ttu-id="8d934-131">Una actualización de una solicitud de tarea anterior.</span><span class="sxs-lookup"><span data-stu-id="8d934-131">An update to a previous task request.</span></span>  <br/> |
|<span data-ttu-id="8d934-132">5 </span><span class="sxs-lookup"><span data-stu-id="8d934-132">5</span></span>  <br/> |<span data-ttu-id="8d934-133">No se usa.</span><span class="sxs-lookup"><span data-stu-id="8d934-133">Not used.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8d934-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8d934-134">Remarks</span></span>

<span data-ttu-id="8d934-135">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="8d934-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8d934-136">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="8d934-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8d934-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="8d934-137">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8d934-138">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="8d934-138">Schema Name</span></span>  <br/> |<span data-ttu-id="8d934-139">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="8d934-139">Types schema</span></span>  <br/> |
|<span data-ttu-id="8d934-140">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="8d934-140">Validation File</span></span>  <br/> |<span data-ttu-id="8d934-141">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="8d934-141">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8d934-142">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="8d934-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="8d934-143">Falso</span><span class="sxs-lookup"><span data-stu-id="8d934-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8d934-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="8d934-144">See also</span></span>



- [<span data-ttu-id="8d934-145">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="8d934-145">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

