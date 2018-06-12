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
ms.openlocfilehash: 25a60b44dbdca89d431dc202f06acb3055958a72
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836109"
---
# <a name="isteamtask"></a><span data-ttu-id="4fb1d-103">IsTeamTask</span><span class="sxs-lookup"><span data-stu-id="4fb1d-103">IsTeamTask</span></span>

<span data-ttu-id="4fb1d-104">El elemento **IsTeamTask** indica si la tarea es propiedad de un equipo.</span><span class="sxs-lookup"><span data-stu-id="4fb1d-104">The **IsTeamTask** element indicates whether the task is owned by a team.</span></span> 
  
```xml
<IsTeamTask/>
```

 <span data-ttu-id="4fb1d-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="4fb1d-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4fb1d-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="4fb1d-106">Attributes and elements</span></span>

<span data-ttu-id="4fb1d-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="4fb1d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4fb1d-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="4fb1d-108">Attributes</span></span>

<span data-ttu-id="4fb1d-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4fb1d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4fb1d-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4fb1d-110">Child elements</span></span>

<span data-ttu-id="4fb1d-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4fb1d-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4fb1d-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="4fb1d-112">Parent elements</span></span>

|<span data-ttu-id="4fb1d-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="4fb1d-113">**Element**</span></span>|<span data-ttu-id="4fb1d-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4fb1d-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4fb1d-115">Tarea</span><span class="sxs-lookup"><span data-stu-id="4fb1d-115">Task</span></span>](task.md) <br/> |<span data-ttu-id="4fb1d-116">Representa una tarea en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="4fb1d-116">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4fb1d-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="4fb1d-117">Text value</span></span>

<span data-ttu-id="4fb1d-118">El valor de texto representa un valor booleano que indica si una tarea es propiedad de un equipo.</span><span class="sxs-lookup"><span data-stu-id="4fb1d-118">The text value represents a Boolean value that indicates whether a task is owned by a team.</span></span> <span data-ttu-id="4fb1d-119">Se trata de una propiedad de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4fb1d-119">This is a read-only property.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4fb1d-120">Notas</span><span class="sxs-lookup"><span data-stu-id="4fb1d-120">Remarks</span></span>

<span data-ttu-id="4fb1d-121">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="4fb1d-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4fb1d-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="4fb1d-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4fb1d-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4fb1d-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4fb1d-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="4fb1d-124">Schema Name</span></span>  <br/> |<span data-ttu-id="4fb1d-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="4fb1d-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="4fb1d-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="4fb1d-126">Validation File</span></span>  <br/> |<span data-ttu-id="4fb1d-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4fb1d-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4fb1d-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="4fb1d-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="4fb1d-129">False</span><span class="sxs-lookup"><span data-stu-id="4fb1d-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4fb1d-130">Ver también</span><span class="sxs-lookup"><span data-stu-id="4fb1d-130">See also</span></span>



- [<span data-ttu-id="4fb1d-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="4fb1d-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="4fb1d-132">Creación de tareas</span><span class="sxs-lookup"><span data-stu-id="4fb1d-132">Creating Tasks</span></span>](http://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx)
  
[<span data-ttu-id="4fb1d-133">Eliminación de tareas</span><span class="sxs-lookup"><span data-stu-id="4fb1d-133">Deleting Tasks</span></span>](http://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

