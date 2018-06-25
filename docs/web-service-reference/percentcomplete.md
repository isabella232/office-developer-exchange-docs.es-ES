---
title: PercentComplete
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PercentComplete
api_type:
- schema
ms.assetid: 58a67f8a-c4dc-42dc-97ae-a9e5cc672d2d
description: El elemento PercentComplete describe el estado de finalización de una tarea.
ms.openlocfilehash: 18e53221ecdf60df195445ed7692c03795bdcc1e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836717"
---
# <a name="percentcomplete"></a><span data-ttu-id="0cd00-103">PercentComplete</span><span class="sxs-lookup"><span data-stu-id="0cd00-103">PercentComplete</span></span>

<span data-ttu-id="0cd00-104">El elemento **PercentComplete** describe el estado de finalización de una tarea.</span><span class="sxs-lookup"><span data-stu-id="0cd00-104">The **PercentComplete** element describes the completion status of a task.</span></span> 
  
```xml
<PercentComplete/>
```

 <span data-ttu-id="0cd00-105">**doble**</span><span class="sxs-lookup"><span data-stu-id="0cd00-105">**double**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0cd00-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="0cd00-106">Attributes and elements</span></span>

<span data-ttu-id="0cd00-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="0cd00-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0cd00-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="0cd00-108">Attributes</span></span>

<span data-ttu-id="0cd00-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0cd00-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0cd00-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0cd00-110">Child elements</span></span>

<span data-ttu-id="0cd00-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0cd00-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0cd00-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0cd00-112">Parent elements</span></span>

|<span data-ttu-id="0cd00-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="0cd00-113">**Element**</span></span>|<span data-ttu-id="0cd00-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0cd00-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0cd00-115">Tarea</span><span class="sxs-lookup"><span data-stu-id="0cd00-115">Task</span></span>](task.md) <br/> |<span data-ttu-id="0cd00-116">Representa una tarea en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="0cd00-116">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0cd00-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="0cd00-117">Text value</span></span>

<span data-ttu-id="0cd00-118">Se requiere un valor de texto que representa un número entero entre 0 y 100.</span><span class="sxs-lookup"><span data-stu-id="0cd00-118">A text value that represents an integer between 0 and 100 is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0cd00-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0cd00-119">Remarks</span></span>

<span data-ttu-id="0cd00-120">Si se establece **PercentComplete** en 100 tiene el mismo efecto que establecer el elemento [CompleteDate](completedate.md) o establecer el elemento de [estado](status.md) en **completada**.</span><span class="sxs-lookup"><span data-stu-id="0cd00-120">Setting **PercentComplete** to 100 has the same effect as setting the [CompleteDate](completedate.md) element or setting the [Status](status.md) element to **Completed**.</span></span> <span data-ttu-id="0cd00-121">En una solicitud que conjuntos de al menos dos de estas propiedades, la última propiedad procesada determinará el valor que se establece para estos elementos.</span><span class="sxs-lookup"><span data-stu-id="0cd00-121">In a request that sets at least two of these properties, the last processed property will determine the value that is set for these elements.</span></span> <span data-ttu-id="0cd00-122">Por ejemplo, si **PercentComplete** es 100, [CompleteDate](completedate.md) es el 1 de enero de 2007 y [estado](status.md) es no iniciado y las propiedades se transmiten en este orden, el efecto será establecer el [estado](status.md) de la tarea en NotStarted, el [ CompleteDate](completedate.md) en **null**y **PercentComplete** en 0.</span><span class="sxs-lookup"><span data-stu-id="0cd00-122">For example, if **PercentComplete** is 100, [CompleteDate](completedate.md) is January 1, 2007, and [Status](status.md) is NotStarted, and the properties are streamed in this order, the effect will be to set the [Status](status.md) of the task to NotStarted, the [CompleteDate](completedate.md) to **null**, and the **PercentComplete** to 0.</span></span> 
  
<span data-ttu-id="0cd00-123">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="0cd00-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0cd00-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0cd00-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0cd00-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0cd00-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0cd00-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="0cd00-126">Schema Name</span></span>  <br/> |<span data-ttu-id="0cd00-127">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="0cd00-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="0cd00-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="0cd00-128">Validation File</span></span>  <br/> |<span data-ttu-id="0cd00-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0cd00-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0cd00-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="0cd00-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="0cd00-131">False</span><span class="sxs-lookup"><span data-stu-id="0cd00-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0cd00-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="0cd00-132">See also</span></span>



- [<span data-ttu-id="0cd00-133">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="0cd00-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="0cd00-134">Creación de tareas</span><span class="sxs-lookup"><span data-stu-id="0cd00-134">Creating Tasks</span></span>](http://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx)
  
[<span data-ttu-id="0cd00-135">Eliminación de tareas</span><span class="sxs-lookup"><span data-stu-id="0cd00-135">Deleting Tasks</span></span>](http://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

