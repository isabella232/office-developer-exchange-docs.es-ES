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
ms.openlocfilehash: fff3d5d3105bf63c9cdd34cbcf828d57ca287b86
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461425"
---
# <a name="completedate"></a><span data-ttu-id="349f0-103">CompleteDate</span><span class="sxs-lookup"><span data-stu-id="349f0-103">CompleteDate</span></span>

<span data-ttu-id="349f0-104">El elemento **CompleteDate** representa la fecha en que se completó un elemento.</span><span class="sxs-lookup"><span data-stu-id="349f0-104">The **CompleteDate** element represents the date on which an item was completed.</span></span> 
  
```xml
<CompleteDate/>
```

 <span data-ttu-id="349f0-105">**DateTime**</span><span class="sxs-lookup"><span data-stu-id="349f0-105">**DateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="349f0-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="349f0-106">Attributes and elements</span></span>

<span data-ttu-id="349f0-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="349f0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="349f0-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="349f0-108">Attributes</span></span>

<span data-ttu-id="349f0-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="349f0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="349f0-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="349f0-110">Child elements</span></span>

<span data-ttu-id="349f0-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="349f0-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="349f0-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="349f0-112">Parent elements</span></span>

|<span data-ttu-id="349f0-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="349f0-113">**Element**</span></span>|<span data-ttu-id="349f0-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="349f0-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="349f0-115">Tarea</span><span class="sxs-lookup"><span data-stu-id="349f0-115">Task</span></span>](task.md) <br/> |<span data-ttu-id="349f0-116">Representa una tarea del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="349f0-116">Represents a task in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="349f0-117">Flag</span><span class="sxs-lookup"><span data-stu-id="349f0-117">Flag</span></span>](flag.md) <br/> |<span data-ttu-id="349f0-118">Especifica una marca en un elemento de buzón.</span><span class="sxs-lookup"><span data-stu-id="349f0-118">Specifies a flag on a mailbox item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="349f0-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="349f0-119">Text value</span></span>

<span data-ttu-id="349f0-120">Si se usa este elemento, se necesita un valor de texto que represente la fecha y la hora.</span><span class="sxs-lookup"><span data-stu-id="349f0-120">A text value that represents the date and time is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="349f0-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="349f0-121">Remarks</span></span>

<span data-ttu-id="349f0-122">La configuración de **CompleteDate** tiene el mismo efecto que establecer [PercentComplete](percentcomplete.md) en 100 o [status](status.md) en **completed**.</span><span class="sxs-lookup"><span data-stu-id="349f0-122">Setting **CompleteDate** has the same effect as setting [PercentComplete](percentcomplete.md) to 100 or [Status](status.md) to **Completed**.</span></span> <span data-ttu-id="349f0-123">En una solicitud que establece al menos dos propiedades, la última propiedad procesada determinará el valor que se establece para estos elementos.</span><span class="sxs-lookup"><span data-stu-id="349f0-123">In a request that sets at least two of these properties, the last processed property will determine the value that is set for these elements.</span></span> <span data-ttu-id="349f0-124">Por ejemplo, si [PercentComplete](percentcomplete.md) es 100, **CompleteDate** es el 1 de enero de 2007 y [status](status.md) es **NotStarted**, y las propiedades se transmiten en ese orden, el efecto será establecer el [Estado](status.md) de la tarea en **notstarted**, [CompleteDate](completedate.md) en **null**y [PercentComplete](percentcomplete.md) en 0.</span><span class="sxs-lookup"><span data-stu-id="349f0-124">For example, if [PercentComplete](percentcomplete.md) is 100, **CompleteDate** is January 1, 2007, and [Status](status.md) is **NotStarted**, and the properties are streamed in that order, the effect will be to set the [Status](status.md) of the task to **NotStarted**, the [CompleteDate](completedate.md) to **null**, and [PercentComplete](percentcomplete.md) to 0.</span></span> 
  
<span data-ttu-id="349f0-125">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="349f0-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="349f0-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="349f0-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="349f0-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="349f0-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="349f0-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="349f0-128">Schema Name</span></span>  <br/> |<span data-ttu-id="349f0-129">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="349f0-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="349f0-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="349f0-130">Validation File</span></span>  <br/> |<span data-ttu-id="349f0-131">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="349f0-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="349f0-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="349f0-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="349f0-133">Falso</span><span class="sxs-lookup"><span data-stu-id="349f0-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="349f0-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="349f0-134">See also</span></span>



- [<span data-ttu-id="349f0-135">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="349f0-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="349f0-136">Creación de tareas</span><span class="sxs-lookup"><span data-stu-id="349f0-136">Creating Tasks</span></span>](https://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx)
  
[<span data-ttu-id="349f0-137">Eliminación de tareas</span><span class="sxs-lookup"><span data-stu-id="349f0-137">Deleting Tasks</span></span>](https://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

