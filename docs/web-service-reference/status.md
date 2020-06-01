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
description: El elemento status representa el estado de un elemento de tarea.
ms.openlocfilehash: 5d022827990b96fd8790ae9566ef49028ebe404c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459962"
---
# <a name="status"></a><span data-ttu-id="49bad-103">Estado</span><span class="sxs-lookup"><span data-stu-id="49bad-103">Status</span></span>

<span data-ttu-id="49bad-104">El elemento **status** representa el estado de un elemento de tarea.</span><span class="sxs-lookup"><span data-stu-id="49bad-104">The **Status** element represents the status of a task item.</span></span> 
  
```xml
<Status/>
```

 <span data-ttu-id="49bad-105">**TaskStatusType**</span><span class="sxs-lookup"><span data-stu-id="49bad-105">**TaskStatusType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="49bad-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="49bad-106">Attributes and elements</span></span>

<span data-ttu-id="49bad-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="49bad-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="49bad-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="49bad-108">Attributes</span></span>

<span data-ttu-id="49bad-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="49bad-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="49bad-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="49bad-110">Child elements</span></span>

<span data-ttu-id="49bad-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="49bad-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="49bad-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="49bad-112">Parent elements</span></span>

|<span data-ttu-id="49bad-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="49bad-113">**Element**</span></span>|<span data-ttu-id="49bad-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="49bad-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="49bad-115">Tarea</span><span class="sxs-lookup"><span data-stu-id="49bad-115">Task</span></span>](task.md) <br/> |<span data-ttu-id="49bad-116">Representa una tarea del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="49bad-116">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="49bad-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="49bad-117">Text value</span></span>

<span data-ttu-id="49bad-118">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="49bad-118">A text value is required.</span></span> <span data-ttu-id="49bad-119">A continuación se muestran los valores de texto posibles para este elemento:</span><span class="sxs-lookup"><span data-stu-id="49bad-119">The following are the possible text values for this element:</span></span>
  
- <span data-ttu-id="49bad-120">NotStarted</span><span class="sxs-lookup"><span data-stu-id="49bad-120">NotStarted</span></span>
    
- <span data-ttu-id="49bad-121">InProgress</span><span class="sxs-lookup"><span data-stu-id="49bad-121">InProgress</span></span>
    
- <span data-ttu-id="49bad-122">Completed</span><span class="sxs-lookup"><span data-stu-id="49bad-122">Completed</span></span>
    
- <span data-ttu-id="49bad-123">WaitingOnOthers</span><span class="sxs-lookup"><span data-stu-id="49bad-123">WaitingOnOthers</span></span>
    
- <span data-ttu-id="49bad-124">Diferido</span><span class="sxs-lookup"><span data-stu-id="49bad-124">Deferred</span></span>
    
## <a name="remarks"></a><span data-ttu-id="49bad-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="49bad-125">Remarks</span></span>

<span data-ttu-id="49bad-126">La configuración de [CompleteDate](completedate.md) tiene el mismo efecto que establecer [PercentComplete](percentcomplete.md) en 100 o **status** en **completed**.</span><span class="sxs-lookup"><span data-stu-id="49bad-126">Setting [CompleteDate](completedate.md) has the same effect as setting [PercentComplete](percentcomplete.md) to 100 or **Status** to **Completed**.</span></span> <span data-ttu-id="49bad-127">En una solicitud que establece al menos dos propiedades, la última propiedad procesada determinará el valor que se establece para estos elementos.</span><span class="sxs-lookup"><span data-stu-id="49bad-127">In a request that sets at least two of these properties, the last processed property will determine the value that is set for these elements.</span></span> <span data-ttu-id="49bad-128">Por ejemplo, si **PercentComplete** es 100, **CompleteDate** es 1/1/2007 y **status** es NotStarted y las propiedades se transmiten en este orden, el efecto será establecer el **Estado** de la tarea en notstarted, **CompleteDate** en **null**y **PercentComplete** en 0.</span><span class="sxs-lookup"><span data-stu-id="49bad-128">For example, if **PercentComplete** is 100, **CompleteDate** is 1/1/2007, and **Status** is NotStarted, and the properties are streamed in this order, the effect will be to set the **Status** of the task to NotStarted, the **CompleteDate** to **null**, and the **PercentComplete** to 0.</span></span> 
  
<span data-ttu-id="49bad-129">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="49bad-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="49bad-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="49bad-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="49bad-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="49bad-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="49bad-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="49bad-132">Schema Name</span></span>  <br/> |<span data-ttu-id="49bad-133">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="49bad-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="49bad-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="49bad-134">Validation File</span></span>  <br/> |<span data-ttu-id="49bad-135">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="49bad-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="49bad-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="49bad-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="49bad-137">Falso</span><span class="sxs-lookup"><span data-stu-id="49bad-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="49bad-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="49bad-138">See also</span></span>



- [<span data-ttu-id="49bad-139">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="49bad-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="49bad-140">Creación de tareas</span><span class="sxs-lookup"><span data-stu-id="49bad-140">Creating Tasks</span></span>](https://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx)
  
[<span data-ttu-id="49bad-141">Eliminación de tareas</span><span class="sxs-lookup"><span data-stu-id="49bad-141">Deleting Tasks</span></span>](https://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

