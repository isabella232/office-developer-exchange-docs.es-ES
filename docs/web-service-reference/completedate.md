---
title: CompleteDate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CompleteDate
api_type:
- schema
ms.assetid: b2b53b87-6a0b-4a55-bcfc-3bf67d3c1700
description: El elemento CompleteDate representa la fecha en que se completó un elemento.
ms.openlocfilehash: 00a1ec25be737ec0a5cc874063e1bce19a96cee0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763751"
---
# <a name="completedate"></a><span data-ttu-id="d67a7-103">CompleteDate</span><span class="sxs-lookup"><span data-stu-id="d67a7-103">CompleteDate</span></span>

<span data-ttu-id="d67a7-104">El elemento **CompleteDate** representa la fecha en que se completó un elemento.</span><span class="sxs-lookup"><span data-stu-id="d67a7-104">The **CompleteDate** element represents the date on which an item was completed.</span></span> 
  
```xml
<CompleteDate/>
```

 <span data-ttu-id="d67a7-105">**DateTime**</span><span class="sxs-lookup"><span data-stu-id="d67a7-105">**DateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d67a7-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d67a7-106">Attributes and elements</span></span>

<span data-ttu-id="d67a7-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d67a7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d67a7-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="d67a7-108">Attributes</span></span>

<span data-ttu-id="d67a7-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d67a7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d67a7-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d67a7-110">Child elements</span></span>

<span data-ttu-id="d67a7-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d67a7-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d67a7-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d67a7-112">Parent elements</span></span>

|<span data-ttu-id="d67a7-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="d67a7-113">**Element**</span></span>|<span data-ttu-id="d67a7-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d67a7-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d67a7-115">Tarea</span><span class="sxs-lookup"><span data-stu-id="d67a7-115">Task</span></span>](task.md) <br/> |<span data-ttu-id="d67a7-116">Representa una tarea en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d67a7-116">Represents a task in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="d67a7-117">Flag</span><span class="sxs-lookup"><span data-stu-id="d67a7-117">Flag</span></span>](flag.md) <br/> |<span data-ttu-id="d67a7-118">Especifica una marca en un elemento de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="d67a7-118">Specifies a flag on a mailbox item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d67a7-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="d67a7-119">Text value</span></span>

<span data-ttu-id="d67a7-120">Si se usa este elemento, es necesario un valor de texto que representa la fecha y hora.</span><span class="sxs-lookup"><span data-stu-id="d67a7-120">A text value that represents the date and time is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d67a7-121">Notas</span><span class="sxs-lookup"><span data-stu-id="d67a7-121">Remarks</span></span>

<span data-ttu-id="d67a7-122">Configuración de **CompleteDate** tiene el mismo efecto que si se establece [PercentComplete](percentcomplete.md) en 100 o [estado](status.md) en **completada**.</span><span class="sxs-lookup"><span data-stu-id="d67a7-122">Setting **CompleteDate** has the same effect as setting [PercentComplete](percentcomplete.md) to 100 or [Status](status.md) to **Completed**.</span></span> <span data-ttu-id="d67a7-123">En una solicitud que conjuntos de al menos dos de estas propiedades, la última propiedad procesada determinará el valor que se establece para estos elementos.</span><span class="sxs-lookup"><span data-stu-id="d67a7-123">In a request that sets at least two of these properties, the last processed property will determine the value that is set for these elements.</span></span> <span data-ttu-id="d67a7-124">Por ejemplo, si [PercentComplete](percentcomplete.md) es 100, **CompleteDate** es el 1 de enero de 2007 y [el estado](status.md) es **no iniciado**y las propiedades se transmiten en ese orden, el efecto será establecer el [estado](status.md) de la tarea a **NotStarted **, la [CompleteDate](completedate.md) en **null**y [PercentComplete](percentcomplete.md) en 0.</span><span class="sxs-lookup"><span data-stu-id="d67a7-124">For example, if [PercentComplete](percentcomplete.md) is 100, **CompleteDate** is January 1, 2007, and [Status](status.md) is **NotStarted**, and the properties are streamed in that order, the effect will be to set the [Status](status.md) of the task to **NotStarted**, the [CompleteDate](completedate.md) to **null**, and [PercentComplete](percentcomplete.md) to 0.</span></span> 
  
<span data-ttu-id="d67a7-125">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="d67a7-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d67a7-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d67a7-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d67a7-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d67a7-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d67a7-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d67a7-128">Schema Name</span></span>  <br/> |<span data-ttu-id="d67a7-129">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="d67a7-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="d67a7-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d67a7-130">Validation File</span></span>  <br/> |<span data-ttu-id="d67a7-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d67a7-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d67a7-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d67a7-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="d67a7-133">False</span><span class="sxs-lookup"><span data-stu-id="d67a7-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d67a7-134">Ver también</span><span class="sxs-lookup"><span data-stu-id="d67a7-134">See also</span></span>



- [<span data-ttu-id="d67a7-135">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="d67a7-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="d67a7-136">Creación de tareas</span><span class="sxs-lookup"><span data-stu-id="d67a7-136">Creating Tasks</span></span>](http://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx)
  
[<span data-ttu-id="d67a7-137">Eliminación de tareas</span><span class="sxs-lookup"><span data-stu-id="d67a7-137">Deleting Tasks</span></span>](http://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

