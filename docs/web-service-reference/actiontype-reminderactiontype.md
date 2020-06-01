---
title: ActionType (ReminderActionType)
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0ffcdcf4-8ea3-483c-bb7f-0cd84126120c
description: El elemento ActionType especifica la acción que se llevará a cabo en el aviso.
ms.openlocfilehash: 5c62b2dd945b23a5ff2bb824385c45dbc617a5a5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465061"
---
# <a name="actiontype-reminderactiontype"></a><span data-ttu-id="43d12-103">ActionType (ReminderActionType)</span><span class="sxs-lookup"><span data-stu-id="43d12-103">ActionType (ReminderActionType)</span></span>

<span data-ttu-id="43d12-104">El elemento **ActionType** especifica la acción que se llevará a cabo en el aviso.</span><span class="sxs-lookup"><span data-stu-id="43d12-104">The **ActionType** element specifies the action to take on the reminder.</span></span> 
  
```XML
<ActionType> Dismiss | Snooze </ActionType>
```

 <span data-ttu-id="43d12-105">**ReminderActionType**</span><span class="sxs-lookup"><span data-stu-id="43d12-105">**ReminderActionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="43d12-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="43d12-106">Attributes and elements</span></span>

<span data-ttu-id="43d12-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="43d12-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="43d12-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="43d12-108">Attributes</span></span>

<span data-ttu-id="43d12-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="43d12-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="43d12-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="43d12-110">Child elements</span></span>

<span data-ttu-id="43d12-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="43d12-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="43d12-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="43d12-112">Parent elements</span></span>

[<span data-ttu-id="43d12-113">ReminderItemAction</span><span class="sxs-lookup"><span data-stu-id="43d12-113">ReminderItemAction</span></span>](reminderitemaction.md)
  
## <a name="text-value"></a><span data-ttu-id="43d12-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="43d12-114">Text value</span></span>

<span data-ttu-id="43d12-115">El valor de texto del elemento **ActionType** especifica la acción que se llevará a cabo en el aviso.</span><span class="sxs-lookup"><span data-stu-id="43d12-115">The text value of the **ActionType** element specifies the action to take on the reminder.</span></span> <span data-ttu-id="43d12-116">El valor de texto **descartado** indica que el aviso debe descartarse.</span><span class="sxs-lookup"><span data-stu-id="43d12-116">The text value of **Dismiss** indicates the reminder should be dismissed.</span></span> <span data-ttu-id="43d12-117">El valor de texto de **SNOOZE** indica que el aviso debe retrasarse hasta el tiempo especificado por el elemento [NewReminderTime](newremindertime.md) .</span><span class="sxs-lookup"><span data-stu-id="43d12-117">The text value of **Snooze** indicates that the reminder should be delayed until the time specified by the [NewReminderTime](newremindertime.md) element.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="43d12-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="43d12-118">Remarks</span></span>

<span data-ttu-id="43d12-119">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="43d12-119">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="43d12-120">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="43d12-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="43d12-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="43d12-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="43d12-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="43d12-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="43d12-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="43d12-123">Schema Name</span></span>  <br/> |<span data-ttu-id="43d12-124">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="43d12-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="43d12-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="43d12-125">Validation File</span></span>  <br/> |<span data-ttu-id="43d12-126">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="43d12-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="43d12-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="43d12-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="43d12-128">Falso</span><span class="sxs-lookup"><span data-stu-id="43d12-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="43d12-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="43d12-129">See also</span></span>

- [<span data-ttu-id="43d12-130">ReminderItemAction</span><span class="sxs-lookup"><span data-stu-id="43d12-130">ReminderItemAction</span></span>](reminderitemaction.md)
- [<span data-ttu-id="43d12-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="43d12-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

