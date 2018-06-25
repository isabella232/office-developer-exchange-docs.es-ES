---
title: Estado
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Status
api_type:
- schema
ms.assetid: 80121e41-291b-4fc0-a55e-6f677d4b5fb5
description: El elemento Status representa el estado de un elemento de tarea.
ms.openlocfilehash: 224b61913a5ae8e5b4aa0d756a9f2488df2741bd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837584"
---
# <a name="status"></a><span data-ttu-id="d1435-103">Estado</span><span class="sxs-lookup"><span data-stu-id="d1435-103">Status</span></span>

<span data-ttu-id="d1435-104">El elemento **Status** representa el estado de un elemento de tarea.</span><span class="sxs-lookup"><span data-stu-id="d1435-104">The **Status** element represents the status of a task item.</span></span> 
  
```xml
<Status/>
```

 <span data-ttu-id="d1435-105">**TaskStatusType**</span><span class="sxs-lookup"><span data-stu-id="d1435-105">**TaskStatusType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d1435-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d1435-106">Attributes and elements</span></span>

<span data-ttu-id="d1435-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d1435-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d1435-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="d1435-108">Attributes</span></span>

<span data-ttu-id="d1435-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d1435-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d1435-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d1435-110">Child elements</span></span>

<span data-ttu-id="d1435-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d1435-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d1435-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d1435-112">Parent elements</span></span>

|<span data-ttu-id="d1435-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="d1435-113">**Element**</span></span>|<span data-ttu-id="d1435-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d1435-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d1435-115">Tarea</span><span class="sxs-lookup"><span data-stu-id="d1435-115">Task</span></span>](task.md) <br/> |<span data-ttu-id="d1435-116">Representa una tarea en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d1435-116">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d1435-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="d1435-117">Text value</span></span>

<span data-ttu-id="d1435-118">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="d1435-118">A text value is required.</span></span> <span data-ttu-id="d1435-119">Los siguientes son los posibles valores de texto para este elemento:</span><span class="sxs-lookup"><span data-stu-id="d1435-119">The following are the possible text values for this element:</span></span>
  
- <span data-ttu-id="d1435-120">No iniciado</span><span class="sxs-lookup"><span data-stu-id="d1435-120">NotStarted</span></span>
    
- <span data-ttu-id="d1435-121">InProgress</span><span class="sxs-lookup"><span data-stu-id="d1435-121">InProgress</span></span>
    
- <span data-ttu-id="d1435-122">Completed</span><span class="sxs-lookup"><span data-stu-id="d1435-122">Completed</span></span>
    
- <span data-ttu-id="d1435-123">WaitingOnOthers</span><span class="sxs-lookup"><span data-stu-id="d1435-123">WaitingOnOthers</span></span>
    
- <span data-ttu-id="d1435-124">Aplazado</span><span class="sxs-lookup"><span data-stu-id="d1435-124">Deferred</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d1435-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d1435-125">Remarks</span></span>

<span data-ttu-id="d1435-126">Configuración de [CompleteDate](completedate.md) tiene el mismo efecto que si se establece [PercentComplete](percentcomplete.md) en 100 o **estado** en **completada**.</span><span class="sxs-lookup"><span data-stu-id="d1435-126">Setting [CompleteDate](completedate.md) has the same effect as setting [PercentComplete](percentcomplete.md) to 100 or **Status** to **Completed**.</span></span> <span data-ttu-id="d1435-127">En una solicitud que conjuntos de al menos dos de estas propiedades, la última propiedad procesada determinará el valor que se establece para estos elementos.</span><span class="sxs-lookup"><span data-stu-id="d1435-127">In a request that sets at least two of these properties, the last processed property will determine the value that is set for these elements.</span></span> <span data-ttu-id="d1435-128">Por ejemplo, si **PercentComplete** es 100, **CompleteDate** es 1/1/2007 y **estado** es NotStarted y las propiedades se transmiten en este orden, el efecto será establecer el **estado** de la tarea en NotStarted, el **CompleteDate **en **null**y **PercentComplete** en 0.</span><span class="sxs-lookup"><span data-stu-id="d1435-128">For example, if **PercentComplete** is 100, **CompleteDate** is 1/1/2007, and **Status** is NotStarted, and the properties are streamed in this order, the effect will be to set the **Status** of the task to NotStarted, the **CompleteDate** to **null**, and the **PercentComplete** to 0.</span></span> 
  
<span data-ttu-id="d1435-129">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="d1435-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d1435-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d1435-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d1435-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d1435-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d1435-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d1435-132">Schema Name</span></span>  <br/> |<span data-ttu-id="d1435-133">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="d1435-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="d1435-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d1435-134">Validation File</span></span>  <br/> |<span data-ttu-id="d1435-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d1435-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d1435-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d1435-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="d1435-137">False</span><span class="sxs-lookup"><span data-stu-id="d1435-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d1435-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="d1435-138">See also</span></span>



- [<span data-ttu-id="d1435-139">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="d1435-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="d1435-140">Creación de tareas</span><span class="sxs-lookup"><span data-stu-id="d1435-140">Creating Tasks</span></span>](http://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx)
  
[<span data-ttu-id="d1435-141">Eliminación de tareas</span><span class="sxs-lookup"><span data-stu-id="d1435-141">Deleting Tasks</span></span>](http://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

