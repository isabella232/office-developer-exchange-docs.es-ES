---
title: NewReminderTime
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ff1b6b1c-3557-41d4-8aa6-9528fdb3a21a
description: El elemento NewReminderTime especifica una nueva hora para un aviso.
ms.openlocfilehash: a10f7e481b474501f33dba4c09060766568952b0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465957"
---
# <a name="newremindertime"></a><span data-ttu-id="5661e-103">NewReminderTime</span><span class="sxs-lookup"><span data-stu-id="5661e-103">NewReminderTime</span></span>

<span data-ttu-id="5661e-104">El elemento **NewReminderTime** especifica una nueva hora para un aviso.</span><span class="sxs-lookup"><span data-stu-id="5661e-104">The **NewReminderTime** element specifies a new time for a reminder.</span></span> 
  
```XML
<NewReminderTime/>
```

 <span data-ttu-id="5661e-105">**string**</span><span class="sxs-lookup"><span data-stu-id="5661e-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5661e-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="5661e-106">Attributes and elements</span></span>

<span data-ttu-id="5661e-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="5661e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5661e-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="5661e-108">Attributes</span></span>

<span data-ttu-id="5661e-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="5661e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5661e-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5661e-110">Child elements</span></span>

<span data-ttu-id="5661e-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="5661e-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5661e-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5661e-112">Parent elements</span></span>

[<span data-ttu-id="5661e-113">ReminderItemAction</span><span class="sxs-lookup"><span data-stu-id="5661e-113">ReminderItemAction</span></span>](reminderitemaction.md)
  
## <a name="text-value"></a><span data-ttu-id="5661e-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="5661e-114">Text value</span></span>

<span data-ttu-id="5661e-115">El valor de texto del elemento **NewReminderTime** es una nueva hora para el aviso.</span><span class="sxs-lookup"><span data-stu-id="5661e-115">The text value of the **NewReminderTime** element is a new time for the reminder.</span></span> <span data-ttu-id="5661e-116">El elemento **NewReminderTime** se utiliza cuando el elemento [ActionType](actiontype-reminderactiontype.md) se establece en **SNOOZE**para retrasar el aviso.</span><span class="sxs-lookup"><span data-stu-id="5661e-116">The **NewReminderTime** element is used when the [ActionType](actiontype-reminderactiontype.md) element is set to **Snooze**, in order to delay the reminder.</span></span> <span data-ttu-id="5661e-117">El valor de **NewReminderTime** debe ser mayor que el valor de [ReminderTime](remindertime.md) devuelto por la [operación GetReminders](getreminders-operation.md).</span><span class="sxs-lookup"><span data-stu-id="5661e-117">The value of the **NewReminderTime** must be greater than the [ReminderTime](remindertime.md) returned by the [GetReminders operation](getreminders-operation.md).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5661e-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5661e-118">Remarks</span></span>

<span data-ttu-id="5661e-119">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="5661e-119">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="5661e-120">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="5661e-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5661e-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="5661e-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5661e-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="5661e-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5661e-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="5661e-123">Schema Name</span></span>  <br/> |<span data-ttu-id="5661e-124">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="5661e-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="5661e-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="5661e-125">Validation File</span></span>  <br/> |<span data-ttu-id="5661e-126">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="5661e-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5661e-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="5661e-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="5661e-128">Falso</span><span class="sxs-lookup"><span data-stu-id="5661e-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5661e-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="5661e-129">See also</span></span>



[<span data-ttu-id="5661e-130">ReminderItemAction</span><span class="sxs-lookup"><span data-stu-id="5661e-130">ReminderItemAction</span></span>](reminderitemaction.md)


- [<span data-ttu-id="5661e-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="5661e-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

