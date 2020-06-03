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
ms.openlocfilehash: be6f4a7d7e9d495ed7b42ed40c60f016468e8c2c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529871"
---
# <a name="remindergroup"></a><span data-ttu-id="ce2ab-103">ReminderGroup</span><span class="sxs-lookup"><span data-stu-id="ce2ab-103">ReminderGroup</span></span>

<span data-ttu-id="ce2ab-104">El elemento **ReminderGroup** especifica si el aviso es para un elemento de calendario o una tarea.</span><span class="sxs-lookup"><span data-stu-id="ce2ab-104">The **ReminderGroup** element specifies whether the reminder is for a calendar item or a task.</span></span> 
  
```XML
<ReminderGroup> Calendar | Task </ReminderGroup>
```

 <span data-ttu-id="ce2ab-105">**ReminderGroupType**</span><span class="sxs-lookup"><span data-stu-id="ce2ab-105">**ReminderGroupType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ce2ab-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ce2ab-106">Attributes and elements</span></span>

<span data-ttu-id="ce2ab-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ce2ab-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ce2ab-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="ce2ab-108">Attributes</span></span>

<span data-ttu-id="ce2ab-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="ce2ab-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ce2ab-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ce2ab-110">Child elements</span></span>

<span data-ttu-id="ce2ab-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="ce2ab-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ce2ab-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ce2ab-112">Parent elements</span></span>

[<span data-ttu-id="ce2ab-113">Aviso</span><span class="sxs-lookup"><span data-stu-id="ce2ab-113">Reminder</span></span>](reminder.md)
  
## <a name="text-value"></a><span data-ttu-id="ce2ab-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="ce2ab-114">Text value</span></span>

<span data-ttu-id="ce2ab-115">El valor de texto del elemento **ReminderGroup** es el tipo de grupo del aviso.</span><span class="sxs-lookup"><span data-stu-id="ce2ab-115">The text value of the **ReminderGroup** element is the group type of the reminder.</span></span> <span data-ttu-id="ce2ab-116">El valor de texto de **Calendar** especifica que el aviso es para un elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="ce2ab-116">The text value of **Calendar** specifies that the reminder is for a calendar item.</span></span> <span data-ttu-id="ce2ab-117">El valor de texto de la **tarea** especifica que el aviso es para un elemento de tarea.</span><span class="sxs-lookup"><span data-stu-id="ce2ab-117">The text value of **Task** specifies that the reminder is for a task item.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ce2ab-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ce2ab-118">Remarks</span></span>

<span data-ttu-id="ce2ab-119">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ce2ab-119">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="ce2ab-120">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="ce2ab-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ce2ab-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ce2ab-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ce2ab-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="ce2ab-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ce2ab-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ce2ab-123">Schema Name</span></span>  <br/> |<span data-ttu-id="ce2ab-124">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="ce2ab-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="ce2ab-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ce2ab-125">Validation File</span></span>  <br/> |<span data-ttu-id="ce2ab-126">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="ce2ab-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ce2ab-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ce2ab-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="ce2ab-128">Falso</span><span class="sxs-lookup"><span data-stu-id="ce2ab-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ce2ab-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="ce2ab-129">See also</span></span>



[<span data-ttu-id="ce2ab-130">Aviso</span><span class="sxs-lookup"><span data-stu-id="ce2ab-130">Reminder</span></span>](reminder.md)


- [<span data-ttu-id="ce2ab-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="ce2ab-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

