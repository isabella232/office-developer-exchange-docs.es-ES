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
ms.openlocfilehash: b7dd2f18bd3ef6addeb6d3a7b004510f35b9cb3d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456888"
---
# <a name="percentcomplete"></a><span data-ttu-id="e4836-103">PercentComplete</span><span class="sxs-lookup"><span data-stu-id="e4836-103">PercentComplete</span></span>

<span data-ttu-id="e4836-104">El elemento **PercentComplete** describe el estado de finalización de una tarea.</span><span class="sxs-lookup"><span data-stu-id="e4836-104">The **PercentComplete** element describes the completion status of a task.</span></span> 
  
```xml
<PercentComplete/>
```

 <span data-ttu-id="e4836-105">**hacer**</span><span class="sxs-lookup"><span data-stu-id="e4836-105">**double**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e4836-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e4836-106">Attributes and elements</span></span>

<span data-ttu-id="e4836-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e4836-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e4836-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="e4836-108">Attributes</span></span>

<span data-ttu-id="e4836-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="e4836-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e4836-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e4836-110">Child elements</span></span>

<span data-ttu-id="e4836-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="e4836-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e4836-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e4836-112">Parent elements</span></span>

|<span data-ttu-id="e4836-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e4836-113">**Element**</span></span>|<span data-ttu-id="e4836-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e4836-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e4836-115">Tarea</span><span class="sxs-lookup"><span data-stu-id="e4836-115">Task</span></span>](task.md) <br/> |<span data-ttu-id="e4836-116">Representa una tarea del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e4836-116">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e4836-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="e4836-117">Text value</span></span>

<span data-ttu-id="e4836-118">Un valor de texto que representa un entero entre 0 y 100 es necesario.</span><span class="sxs-lookup"><span data-stu-id="e4836-118">A text value that represents an integer between 0 and 100 is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e4836-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e4836-119">Remarks</span></span>

<span data-ttu-id="e4836-120">Establecer **PercentComplete** en 100 tiene el mismo efecto que establecer el elemento [CompleteDate](completedate.md) o establecer el elemento [status](status.md) en **completed**.</span><span class="sxs-lookup"><span data-stu-id="e4836-120">Setting **PercentComplete** to 100 has the same effect as setting the [CompleteDate](completedate.md) element or setting the [Status](status.md) element to **Completed**.</span></span> <span data-ttu-id="e4836-121">En una solicitud que establece al menos dos propiedades, la última propiedad procesada determinará el valor que se establece para estos elementos.</span><span class="sxs-lookup"><span data-stu-id="e4836-121">In a request that sets at least two of these properties, the last processed property will determine the value that is set for these elements.</span></span> <span data-ttu-id="e4836-122">Por ejemplo, si **PercentComplete** es 100, [CompleteDate](completedate.md) es el 1 de enero de 2007 y [status](status.md) es NotStarted, y las propiedades se transmiten en este orden, el efecto será establecer el [Estado](status.md) de la tarea en notstarted, [CompleteDate](completedate.md) en **null**y **PercentComplete** en 0.</span><span class="sxs-lookup"><span data-stu-id="e4836-122">For example, if **PercentComplete** is 100, [CompleteDate](completedate.md) is January 1, 2007, and [Status](status.md) is NotStarted, and the properties are streamed in this order, the effect will be to set the [Status](status.md) of the task to NotStarted, the [CompleteDate](completedate.md) to **null**, and the **PercentComplete** to 0.</span></span> 
  
<span data-ttu-id="e4836-123">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="e4836-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e4836-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e4836-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e4836-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="e4836-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e4836-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e4836-126">Schema Name</span></span>  <br/> |<span data-ttu-id="e4836-127">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="e4836-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="e4836-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e4836-128">Validation File</span></span>  <br/> |<span data-ttu-id="e4836-129">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="e4836-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e4836-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e4836-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="e4836-131">Falso</span><span class="sxs-lookup"><span data-stu-id="e4836-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e4836-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="e4836-132">See also</span></span>



- [<span data-ttu-id="e4836-133">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="e4836-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="e4836-134">Creación de tareas</span><span class="sxs-lookup"><span data-stu-id="e4836-134">Creating Tasks</span></span>](https://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx)
  
[<span data-ttu-id="e4836-135">Eliminación de tareas</span><span class="sxs-lookup"><span data-stu-id="e4836-135">Deleting Tasks</span></span>](https://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

