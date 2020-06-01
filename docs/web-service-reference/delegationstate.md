---
title: DelegationState
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DelegationState
api_type:
- schema
ms.assetid: 9dbb83ed-1ded-48f3-8e06-2489fc8b28d5
description: El elemento DelegationState representa el estado de una tarea delegada.
ms.openlocfilehash: b938b5a2240283c265006dd47cd6ff475ad80978
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457371"
---
# <a name="delegationstate"></a><span data-ttu-id="4a395-103">DelegationState</span><span class="sxs-lookup"><span data-stu-id="4a395-103">DelegationState</span></span>

<span data-ttu-id="4a395-104">El elemento **DelegationState** representa el estado de una tarea delegada.</span><span class="sxs-lookup"><span data-stu-id="4a395-104">The **DelegationState** element represents the status of a delegated task.</span></span> 
  
```xml
<DelegationState/>
```

<span data-ttu-id="4a395-105">**TaskDelegateStateType**</span><span class="sxs-lookup"><span data-stu-id="4a395-105">**TaskDelegateStateType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="4a395-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="4a395-106">Attributes and elements</span></span>

<span data-ttu-id="4a395-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="4a395-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4a395-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="4a395-108">Attributes</span></span>

<span data-ttu-id="4a395-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="4a395-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4a395-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4a395-110">Child elements</span></span>

<span data-ttu-id="4a395-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="4a395-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4a395-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="4a395-112">Parent elements</span></span>

|<span data-ttu-id="4a395-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="4a395-113">**Element**</span></span>|<span data-ttu-id="4a395-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4a395-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4a395-115">Tarea</span><span class="sxs-lookup"><span data-stu-id="4a395-115">Task</span></span>](task.md) <br/> |<span data-ttu-id="4a395-116">Representa una tarea del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="4a395-116">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4a395-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="4a395-117">Text value</span></span>

<span data-ttu-id="4a395-118">Se trata de una propiedad de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4a395-118">This is a read-only property.</span></span> <span data-ttu-id="4a395-119">Los valores posibles son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="4a395-119">The following are the possible values:</span></span>
  
- <span data-ttu-id="4a395-120">NoMatch</span><span class="sxs-lookup"><span data-stu-id="4a395-120">NoMatch</span></span>
    
- <span data-ttu-id="4a395-121">OwnNew</span><span class="sxs-lookup"><span data-stu-id="4a395-121">OwnNew</span></span>
    
- <span data-ttu-id="4a395-122">Estatal</span><span class="sxs-lookup"><span data-stu-id="4a395-122">Owned</span></span>
    
- <span data-ttu-id="4a395-123">Aceptadas</span><span class="sxs-lookup"><span data-stu-id="4a395-123">Accepted</span></span>
    
- <span data-ttu-id="4a395-124">Rechazado</span><span class="sxs-lookup"><span data-stu-id="4a395-124">Declined</span></span>
    
- <span data-ttu-id="4a395-125">Max</span><span class="sxs-lookup"><span data-stu-id="4a395-125">Max</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4a395-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4a395-126">Remarks</span></span>

<span data-ttu-id="4a395-127">Los servicios web Exchange de Microsoft Exchange Server 2007 no admiten asignaciones de tareas.</span><span class="sxs-lookup"><span data-stu-id="4a395-127">Exchange Web Services in Microsoft Exchange Server 2007 does not support task assignments.</span></span>
  
<span data-ttu-id="4a395-128">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Exchange 2007 y que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="4a395-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4a395-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="4a395-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4a395-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="4a395-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4a395-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="4a395-131">Schema Name</span></span>  <br/> |<span data-ttu-id="4a395-132">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="4a395-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="4a395-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="4a395-133">Validation File</span></span>  <br/> |<span data-ttu-id="4a395-134">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="4a395-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4a395-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="4a395-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="4a395-136">Falso</span><span class="sxs-lookup"><span data-stu-id="4a395-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4a395-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="4a395-137">See also</span></span>

- [<span data-ttu-id="4a395-138">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="4a395-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

