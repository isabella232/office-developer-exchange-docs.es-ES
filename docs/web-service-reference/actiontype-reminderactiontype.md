---
title: ActionType (ReminderActionType)
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0ffcdcf4-8ea3-483c-bb7f-0cd84126120c
description: El elemento ActionType especifica la acción que se realizará en el aviso.
ms.openlocfilehash: 361259f733756995fae2c2c2390013a728e475a4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763385"
---
# <a name="actiontype-reminderactiontype"></a><span data-ttu-id="38e8c-103">ActionType (ReminderActionType)</span><span class="sxs-lookup"><span data-stu-id="38e8c-103">ActionType (ReminderActionType)</span></span>

<span data-ttu-id="38e8c-104">El elemento **ActionType** especifica la acción que se realizará en el aviso.</span><span class="sxs-lookup"><span data-stu-id="38e8c-104">The **ActionType** element specifies the action to take on the reminder.</span></span> 
  
```XML
<ActionType> Dismiss | Snooze </ActionType>
```

 <span data-ttu-id="38e8c-105">**ReminderActionType**</span><span class="sxs-lookup"><span data-stu-id="38e8c-105">**ReminderActionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="38e8c-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="38e8c-106">Attributes and elements</span></span>

<span data-ttu-id="38e8c-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="38e8c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="38e8c-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="38e8c-108">Attributes</span></span>

<span data-ttu-id="38e8c-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="38e8c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="38e8c-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="38e8c-110">Child elements</span></span>

<span data-ttu-id="38e8c-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="38e8c-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="38e8c-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="38e8c-112">Parent elements</span></span>

[<span data-ttu-id="38e8c-113">ReminderItemAction</span><span class="sxs-lookup"><span data-stu-id="38e8c-113">ReminderItemAction</span></span>](reminderitemaction.md)
  
## <a name="text-value"></a><span data-ttu-id="38e8c-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="38e8c-114">Text value</span></span>

<span data-ttu-id="38e8c-115">El valor de texto del elemento **ActionType** especifica la acción que se realizará en el aviso.</span><span class="sxs-lookup"><span data-stu-id="38e8c-115">The text value of the **ActionType** element specifies the action to take on the reminder.</span></span> <span data-ttu-id="38e8c-116">El valor de texto de **Dismiss** indica que se debe descartar el aviso.</span><span class="sxs-lookup"><span data-stu-id="38e8c-116">The text value of **Dismiss** indicates the reminder should be dismissed.</span></span> <span data-ttu-id="38e8c-117">El valor de texto de **Posponer** indica que el aviso se debería retrasar hasta el tiempo especificado por el elemento [NewReminderTime](newremindertime.md) .</span><span class="sxs-lookup"><span data-stu-id="38e8c-117">The text value of **Snooze** indicates that the reminder should be delayed until the time specified by the [NewReminderTime](newremindertime.md) element.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="38e8c-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="38e8c-118">Remarks</span></span>

<span data-ttu-id="38e8c-119">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="38e8c-119">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="38e8c-120">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="38e8c-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="38e8c-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="38e8c-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="38e8c-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="38e8c-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="38e8c-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="38e8c-123">Schema Name</span></span>  <br/> |<span data-ttu-id="38e8c-124">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="38e8c-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="38e8c-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="38e8c-125">Validation File</span></span>  <br/> |<span data-ttu-id="38e8c-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="38e8c-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="38e8c-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="38e8c-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="38e8c-128">False</span><span class="sxs-lookup"><span data-stu-id="38e8c-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="38e8c-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="38e8c-129">See also</span></span>

- [<span data-ttu-id="38e8c-130">ReminderItemAction</span><span class="sxs-lookup"><span data-stu-id="38e8c-130">ReminderItemAction</span></span>](reminderitemaction.md)
- [<span data-ttu-id="38e8c-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="38e8c-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

