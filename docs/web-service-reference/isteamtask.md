---
title: IsTeamTask
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsTeamTask
api_type:
- schema
ms.assetid: af0095da-e5bb-4138-a01c-c203f1a5a33f
description: El elemento IsTeamTask indica si la tarea es propiedad de un equipo.
ms.openlocfilehash: 27b5efbac028dbe7cf5858b198e3a33f9f6cdc86
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468449"
---
# <a name="isteamtask"></a><span data-ttu-id="c3165-103">IsTeamTask</span><span class="sxs-lookup"><span data-stu-id="c3165-103">IsTeamTask</span></span>

<span data-ttu-id="c3165-104">El elemento **IsTeamTask** indica si la tarea es propiedad de un equipo.</span><span class="sxs-lookup"><span data-stu-id="c3165-104">The **IsTeamTask** element indicates whether the task is owned by a team.</span></span> 
  
```xml
<IsTeamTask/>
```

 <span data-ttu-id="c3165-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="c3165-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c3165-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c3165-106">Attributes and elements</span></span>

<span data-ttu-id="c3165-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c3165-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c3165-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c3165-108">Attributes</span></span>

<span data-ttu-id="c3165-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c3165-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c3165-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c3165-110">Child elements</span></span>

<span data-ttu-id="c3165-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c3165-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c3165-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c3165-112">Parent elements</span></span>

|<span data-ttu-id="c3165-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c3165-113">**Element**</span></span>|<span data-ttu-id="c3165-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c3165-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c3165-115">Tarea</span><span class="sxs-lookup"><span data-stu-id="c3165-115">Task</span></span>](task.md) <br/> |<span data-ttu-id="c3165-116">Representa una tarea del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c3165-116">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c3165-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="c3165-117">Text value</span></span>

<span data-ttu-id="c3165-118">El valor de texto representa un valor booleano que indica si una tarea es propiedad de un equipo.</span><span class="sxs-lookup"><span data-stu-id="c3165-118">The text value represents a Boolean value that indicates whether a task is owned by a team.</span></span> <span data-ttu-id="c3165-119">Se trata de una propiedad de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c3165-119">This is a read-only property.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c3165-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c3165-120">Remarks</span></span>

<span data-ttu-id="c3165-121">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="c3165-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c3165-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c3165-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c3165-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="c3165-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c3165-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c3165-124">Schema Name</span></span>  <br/> |<span data-ttu-id="c3165-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="c3165-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="c3165-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c3165-126">Validation File</span></span>  <br/> |<span data-ttu-id="c3165-127">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="c3165-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c3165-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c3165-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="c3165-129">Falso</span><span class="sxs-lookup"><span data-stu-id="c3165-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c3165-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="c3165-130">See also</span></span>



- [<span data-ttu-id="c3165-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="c3165-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="c3165-132">Creación de tareas</span><span class="sxs-lookup"><span data-stu-id="c3165-132">Creating Tasks</span></span>](https://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx)
  
[<span data-ttu-id="c3165-133">Eliminación de tareas</span><span class="sxs-lookup"><span data-stu-id="c3165-133">Deleting Tasks</span></span>](https://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

