---
title: ReminderGroup
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3e23c2a1-05d8-4fec-897c-f684a5b97e4c
description: El elemento ReminderGroup especifica si el aviso es para un elemento de calendario o una tarea.
ms.openlocfilehash: d9d31cdab482d04149428021ad44cc742108053a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837060"
---
# <a name="remindergroup"></a><span data-ttu-id="df177-103">ReminderGroup</span><span class="sxs-lookup"><span data-stu-id="df177-103">ReminderGroup</span></span>

<span data-ttu-id="df177-104">El elemento **ReminderGroup** especifica si el aviso es para un elemento de calendario o una tarea.</span><span class="sxs-lookup"><span data-stu-id="df177-104">The **ReminderGroup** element specifies whether the reminder is for a calendar item or a task.</span></span> 
  
```XML
<ReminderGroup> Calendar | Task </ReminderGroup>
```

 <span data-ttu-id="df177-105">**ReminderGroupType**</span><span class="sxs-lookup"><span data-stu-id="df177-105">**ReminderGroupType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="df177-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="df177-106">Attributes and elements</span></span>

<span data-ttu-id="df177-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="df177-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="df177-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="df177-108">Attributes</span></span>

<span data-ttu-id="df177-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="df177-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="df177-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="df177-110">Child elements</span></span>

<span data-ttu-id="df177-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="df177-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="df177-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="df177-112">Parent elements</span></span>

[<span data-ttu-id="df177-113">Aviso</span><span class="sxs-lookup"><span data-stu-id="df177-113">Reminder</span></span>](reminder.md)
  
## <a name="text-value"></a><span data-ttu-id="df177-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="df177-114">Text value</span></span>

<span data-ttu-id="df177-115">El valor de texto del elemento **ReminderGroup** es el tipo de grupo del aviso.</span><span class="sxs-lookup"><span data-stu-id="df177-115">The text value of the **ReminderGroup** element is the group type of the reminder.</span></span> <span data-ttu-id="df177-116">El valor de texto del **calendario** especifica que es un aviso de un elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="df177-116">The text value of **Calendar** specifies that the reminder is for a calendar item.</span></span> <span data-ttu-id="df177-117">El valor de texto de **tarea** especifica que es un aviso de un elemento de tarea.</span><span class="sxs-lookup"><span data-stu-id="df177-117">The text value of **Task** specifies that the reminder is for a task item.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="df177-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="df177-118">Remarks</span></span>

<span data-ttu-id="df177-119">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="df177-119">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="df177-120">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="df177-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="df177-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="df177-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="df177-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="df177-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="df177-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="df177-123">Schema Name</span></span>  <br/> |<span data-ttu-id="df177-124">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="df177-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="df177-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="df177-125">Validation File</span></span>  <br/> |<span data-ttu-id="df177-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="df177-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="df177-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="df177-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="df177-128">False</span><span class="sxs-lookup"><span data-stu-id="df177-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="df177-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="df177-129">See also</span></span>



[<span data-ttu-id="df177-130">Aviso</span><span class="sxs-lookup"><span data-stu-id="df177-130">Reminder</span></span>](reminder.md)


- [<span data-ttu-id="df177-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="df177-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

