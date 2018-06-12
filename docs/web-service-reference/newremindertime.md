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
ms.openlocfilehash: 9f3f509942c673c916cc646cd9519240aef6ea06
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836531"
---
# <a name="newremindertime"></a><span data-ttu-id="d2422-103">NewReminderTime</span><span class="sxs-lookup"><span data-stu-id="d2422-103">NewReminderTime</span></span>

<span data-ttu-id="d2422-104">El elemento **NewReminderTime** especifica una nueva hora para un aviso.</span><span class="sxs-lookup"><span data-stu-id="d2422-104">The **NewReminderTime** element specifies a new time for a reminder.</span></span> 
  
```XML
<NewReminderTime/>
```

 <span data-ttu-id="d2422-105">**string**</span><span class="sxs-lookup"><span data-stu-id="d2422-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d2422-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d2422-106">Attributes and elements</span></span>

<span data-ttu-id="d2422-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d2422-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d2422-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="d2422-108">Attributes</span></span>

<span data-ttu-id="d2422-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d2422-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d2422-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d2422-110">Child elements</span></span>

<span data-ttu-id="d2422-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d2422-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d2422-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d2422-112">Parent elements</span></span>

[<span data-ttu-id="d2422-113">ReminderItemAction</span><span class="sxs-lookup"><span data-stu-id="d2422-113">ReminderItemAction</span></span>](reminderitemaction.md)
  
## <a name="text-value"></a><span data-ttu-id="d2422-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="d2422-114">Text value</span></span>

<span data-ttu-id="d2422-115">El valor de texto del elemento **NewReminderTime** es una nueva hora para el aviso.</span><span class="sxs-lookup"><span data-stu-id="d2422-115">The text value of the **NewReminderTime** element is a new time for the reminder.</span></span> <span data-ttu-id="d2422-116">El elemento **NewReminderTime** se usa cuando se establece el elemento de [ActionType](actiontype-reminderactiontype.md) para **Posponer**, con el fin de retraso el aviso.</span><span class="sxs-lookup"><span data-stu-id="d2422-116">The **NewReminderTime** element is used when the [ActionType](actiontype-reminderactiontype.md) element is set to **Snooze**, in order to delay the reminder.</span></span> <span data-ttu-id="d2422-117">El valor de la **NewReminderTime** debe ser mayor que el [ReminderTime](remindertime.md) devuelto por la [operación de GetReminders](getreminders-operation.md).</span><span class="sxs-lookup"><span data-stu-id="d2422-117">The value of the **NewReminderTime** must be greater than the [ReminderTime](remindertime.md) returned by the [GetReminders operation](getreminders-operation.md).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d2422-118">Notas</span><span class="sxs-lookup"><span data-stu-id="d2422-118">Remarks</span></span>

<span data-ttu-id="d2422-119">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d2422-119">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="d2422-120">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="d2422-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d2422-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d2422-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d2422-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d2422-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d2422-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d2422-123">Schema Name</span></span>  <br/> |<span data-ttu-id="d2422-124">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="d2422-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="d2422-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d2422-125">Validation File</span></span>  <br/> |<span data-ttu-id="d2422-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d2422-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d2422-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d2422-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="d2422-128">False</span><span class="sxs-lookup"><span data-stu-id="d2422-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d2422-129">Ver también</span><span class="sxs-lookup"><span data-stu-id="d2422-129">See also</span></span>



[<span data-ttu-id="d2422-130">ReminderItemAction</span><span class="sxs-lookup"><span data-stu-id="d2422-130">ReminderItemAction</span></span>](reminderitemaction.md)


- [<span data-ttu-id="d2422-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="d2422-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

