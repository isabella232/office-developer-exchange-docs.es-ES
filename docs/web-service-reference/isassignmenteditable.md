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
ms.openlocfilehash: 91922c4d6abd4d88ac9e36dd3d4c0224fc1ee716
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835992"
---
# <a name="isassignmenteditable"></a><span data-ttu-id="cb958-103">IsAssignmentEditable</span><span class="sxs-lookup"><span data-stu-id="cb958-103">IsAssignmentEditable</span></span>

<span data-ttu-id="cb958-104">El elemento **IsAssignmentEditable** representa el tipo de tarea.</span><span class="sxs-lookup"><span data-stu-id="cb958-104">The **IsAssignmentEditable** element represents the task type.</span></span> 
  
```xml
<IsAssignmentEditable/>
```

 <span data-ttu-id="cb958-105">**número entero**</span><span class="sxs-lookup"><span data-stu-id="cb958-105">**integer**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cb958-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="cb958-106">Attributes and elements</span></span>

<span data-ttu-id="cb958-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="cb958-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cb958-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="cb958-108">Attributes</span></span>

<span data-ttu-id="cb958-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="cb958-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cb958-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="cb958-110">Child elements</span></span>

<span data-ttu-id="cb958-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="cb958-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="cb958-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="cb958-112">Parent elements</span></span>

|<span data-ttu-id="cb958-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="cb958-113">**Element**</span></span>|<span data-ttu-id="cb958-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cb958-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cb958-115">Tarea</span><span class="sxs-lookup"><span data-stu-id="cb958-115">Task</span></span>](task.md) <br/> |<span data-ttu-id="cb958-116">Representa una tarea en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="cb958-116">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="cb958-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="cb958-117">Text value</span></span>

<span data-ttu-id="cb958-118">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="cb958-118">This property is read-only.</span></span> <span data-ttu-id="cb958-119">En la siguiente tabla se enumera los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="cb958-119">The following table lists the possible values.</span></span>
  
|<span data-ttu-id="cb958-120">**Valor**</span><span class="sxs-lookup"><span data-stu-id="cb958-120">**Value**</span></span>|<span data-ttu-id="cb958-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cb958-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cb958-122">0</span><span class="sxs-lookup"><span data-stu-id="cb958-122">0</span></span>  <br/> |<span data-ttu-id="cb958-123">El valor predeterminado para todos los elementos de tarea.</span><span class="sxs-lookup"><span data-stu-id="cb958-123">The default for all task items.</span></span>  <br/> |
|<span data-ttu-id="cb958-124">1</span><span class="sxs-lookup"><span data-stu-id="cb958-124">1</span></span>  <br/> |<span data-ttu-id="cb958-125">Una solicitud de tarea.</span><span class="sxs-lookup"><span data-stu-id="cb958-125">A task request.</span></span>  <br/> |
|<span data-ttu-id="cb958-126">2</span><span class="sxs-lookup"><span data-stu-id="cb958-126">2</span></span>  <br/> |<span data-ttu-id="cb958-127">Aceptación de una tarea desde un destinatario de una solicitud de tarea.</span><span class="sxs-lookup"><span data-stu-id="cb958-127">A task acceptance from a recipient of a task request.</span></span>  <br/> |
|<span data-ttu-id="cb958-128">3</span><span class="sxs-lookup"><span data-stu-id="cb958-128">3</span></span>  <br/> |<span data-ttu-id="cb958-129">Rechazo de una tarea desde un destinatario de una solicitud de tarea.</span><span class="sxs-lookup"><span data-stu-id="cb958-129">A task declination from a recipient of a task request.</span></span>  <br/> |
|<span data-ttu-id="cb958-130">4</span><span class="sxs-lookup"><span data-stu-id="cb958-130">4</span></span>  <br/> |<span data-ttu-id="cb958-131">Una actualización de una solicitud de tarea anterior.</span><span class="sxs-lookup"><span data-stu-id="cb958-131">An update to a previous task request.</span></span>  <br/> |
|<span data-ttu-id="cb958-132">5</span><span class="sxs-lookup"><span data-stu-id="cb958-132">5</span></span>  <br/> |<span data-ttu-id="cb958-133">No se usa.</span><span class="sxs-lookup"><span data-stu-id="cb958-133">Not used.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cb958-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cb958-134">Remarks</span></span>

<span data-ttu-id="cb958-135">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="cb958-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cb958-136">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="cb958-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cb958-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="cb958-137">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="cb958-138">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="cb958-138">Schema Name</span></span>  <br/> |<span data-ttu-id="cb958-139">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="cb958-139">Types schema</span></span>  <br/> |
|<span data-ttu-id="cb958-140">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="cb958-140">Validation File</span></span>  <br/> |<span data-ttu-id="cb958-141">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="cb958-141">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="cb958-142">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="cb958-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="cb958-143">False</span><span class="sxs-lookup"><span data-stu-id="cb958-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cb958-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="cb958-144">See also</span></span>



- [<span data-ttu-id="cb958-145">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="cb958-145">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

