---
title: Aviso
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 54dd748a-23a5-4ea2-88f2-b74c68a3c48f
description: El elemento de aviso especifica un aviso para una tarea o un elemento de calendario.
ms.openlocfilehash: cfa1160bd25f5045a3da5a98f081c9dcb3debe7b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837056"
---
# <a name="reminder"></a><span data-ttu-id="6c939-103">Aviso</span><span class="sxs-lookup"><span data-stu-id="6c939-103">Reminder</span></span>

<span data-ttu-id="6c939-104">El elemento de **aviso** especifica un aviso para una tarea o un elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="6c939-104">The **Reminder** element specifies a reminder for a task or a calendar item.</span></span> 
  
```XML
<Reminder>
   <Subject></Subject>
   <Location></Location>
   <ReminderTime></ReminderTime>
   <StartDate></StartDate>
   <EndDate></EndDate>
   <ItemId></ItemId>
   <RecurringMasterItemId></RecurringMasterItemId>
   <ReminderGroup></ReminderGroup>
   <UID></UID>
</Reminder>

```

 <span data-ttu-id="6c939-105">**ReminderType**</span><span class="sxs-lookup"><span data-stu-id="6c939-105">**ReminderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6c939-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="6c939-106">Attributes and elements</span></span>

<span data-ttu-id="6c939-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="6c939-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6c939-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="6c939-108">Attributes</span></span>

<span data-ttu-id="6c939-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="6c939-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6c939-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6c939-110">Child elements</span></span>

<span data-ttu-id="6c939-111">[Asunto](subject.md) | [ubicación](location.md) | [ReminderTime](remindertime.md) | [StartDate](startdate.md) | [EndDate (ReminderType)](enddate-remindertype.md) | [ItemId](itemid.md) | [RecurringMasterItemId (ItemIdType)](recurringmasteritemid-itemidtype.md)  |  [ReminderGroup](remindergroup.md) | [UID](uid.md)</span><span class="sxs-lookup"><span data-stu-id="6c939-111">[Subject](subject.md) | [Location](location.md) | [ReminderTime](remindertime.md) | [StartDate](startdate.md) | [EndDate (ReminderType)](enddate-remindertype.md) | [ItemId](itemid.md) | [RecurringMasterItemId (ItemIdType)](recurringmasteritemid-itemidtype.md) | [ReminderGroup](remindergroup.md) | [UID](uid.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6c939-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6c939-112">Parent elements</span></span>

[<span data-ttu-id="6c939-113">Reminders</span><span class="sxs-lookup"><span data-stu-id="6c939-113">Reminders</span></span>](reminders.md)
  
## <a name="remarks"></a><span data-ttu-id="6c939-114">Notas</span><span class="sxs-lookup"><span data-stu-id="6c939-114">Remarks</span></span>

<span data-ttu-id="6c939-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6c939-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="6c939-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="6c939-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6c939-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="6c939-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6c939-118">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6c939-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6c939-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="6c939-119">Schema Name</span></span>  <br/> |<span data-ttu-id="6c939-120">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="6c939-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="6c939-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="6c939-121">Validation File</span></span>  <br/> |<span data-ttu-id="6c939-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6c939-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6c939-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="6c939-123">Can be Empty</span></span>  <br/> |<span data-ttu-id="6c939-124">False</span><span class="sxs-lookup"><span data-stu-id="6c939-124">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6c939-125">Ver también</span><span class="sxs-lookup"><span data-stu-id="6c939-125">See also</span></span>



[<span data-ttu-id="6c939-126">Reminders</span><span class="sxs-lookup"><span data-stu-id="6c939-126">Reminders</span></span>](reminders.md)


- [<span data-ttu-id="6c939-127">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="6c939-127">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

