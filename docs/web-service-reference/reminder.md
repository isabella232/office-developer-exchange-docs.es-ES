---
title: Recordatorio
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 54dd748a-23a5-4ea2-88f2-b74c68a3c48f
description: El elemento Reminder especifica un aviso para una tarea o un elemento de calendario.
ms.openlocfilehash: 71e54d920a169b8060d22bb7d7d294208c344c2e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457490"
---
# <a name="reminder"></a><span data-ttu-id="418e5-103">Recordatorio</span><span class="sxs-lookup"><span data-stu-id="418e5-103">Reminder</span></span>

<span data-ttu-id="418e5-104">El elemento **Reminder** especifica un aviso para una tarea o un elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="418e5-104">The **Reminder** element specifies a reminder for a task or a calendar item.</span></span> 
  
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

 <span data-ttu-id="418e5-105">**ReminderType**</span><span class="sxs-lookup"><span data-stu-id="418e5-105">**ReminderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="418e5-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="418e5-106">Attributes and elements</span></span>

<span data-ttu-id="418e5-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="418e5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="418e5-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="418e5-108">Attributes</span></span>

<span data-ttu-id="418e5-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="418e5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="418e5-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="418e5-110">Child elements</span></span>

<span data-ttu-id="418e5-111">[Asunto](subject.md)  |  [Ubicación](location.md)  |  [ReminderTime](remindertime.md)  |  [StartDate](startdate.md)  |  [EndDate (ReminderType)](enddate-remindertype.md)  |  [Itemid](itemid.md)  |  [RecurringMasterItemId (ItemIdType)](recurringmasteritemid-itemidtype.md)  |  [ReminderGroup](remindergroup.md)  |  [UID](uid.md)</span><span class="sxs-lookup"><span data-stu-id="418e5-111">[Subject](subject.md) | [Location](location.md) | [ReminderTime](remindertime.md) | [StartDate](startdate.md) | [EndDate (ReminderType)](enddate-remindertype.md) | [ItemId](itemid.md) | [RecurringMasterItemId (ItemIdType)](recurringmasteritemid-itemidtype.md) | [ReminderGroup](remindergroup.md) | [UID](uid.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="418e5-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="418e5-112">Parent elements</span></span>

[<span data-ttu-id="418e5-113">Avisos</span><span class="sxs-lookup"><span data-stu-id="418e5-113">Reminders</span></span>](reminders.md)
  
## <a name="remarks"></a><span data-ttu-id="418e5-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="418e5-114">Remarks</span></span>

<span data-ttu-id="418e5-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="418e5-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="418e5-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="418e5-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="418e5-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="418e5-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="418e5-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="418e5-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="418e5-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="418e5-119">Schema Name</span></span>  <br/> |<span data-ttu-id="418e5-120">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="418e5-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="418e5-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="418e5-121">Validation File</span></span>  <br/> |<span data-ttu-id="418e5-122">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="418e5-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="418e5-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="418e5-123">Can be Empty</span></span>  <br/> |<span data-ttu-id="418e5-124">Falso</span><span class="sxs-lookup"><span data-stu-id="418e5-124">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="418e5-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="418e5-125">See also</span></span>



[<span data-ttu-id="418e5-126">Avisos</span><span class="sxs-lookup"><span data-stu-id="418e5-126">Reminders</span></span>](reminders.md)


- [<span data-ttu-id="418e5-127">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="418e5-127">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

