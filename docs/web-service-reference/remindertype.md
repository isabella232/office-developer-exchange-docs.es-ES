---
title: ReminderType
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bfaf84eb-271a-4728-84fc-a20205a100bd
description: El elemento ReminderType especifica el tipo de avisos para devolver.
ms.openlocfilehash: 11739d2068a1009b2840b2169e86b113151cbfa9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837077"
---
# <a name="remindertype"></a><span data-ttu-id="ed6da-103">ReminderType</span><span class="sxs-lookup"><span data-stu-id="ed6da-103">ReminderType</span></span>

<span data-ttu-id="ed6da-104">El elemento **ReminderType** especifica el tipo de avisos para devolver.</span><span class="sxs-lookup"><span data-stu-id="ed6da-104">The **ReminderType** element specifies the type of reminders to return.</span></span> 
  
```XML
<ReminderType> All | Current | Old </ReminderType>
```

 <span data-ttu-id="ed6da-105">**string**</span><span class="sxs-lookup"><span data-stu-id="ed6da-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ed6da-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ed6da-106">Attributes and elements</span></span>

<span data-ttu-id="ed6da-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ed6da-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ed6da-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="ed6da-108">Attributes</span></span>

<span data-ttu-id="ed6da-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ed6da-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ed6da-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ed6da-110">Child elements</span></span>

<span data-ttu-id="ed6da-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ed6da-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ed6da-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ed6da-112">Parent elements</span></span>

[<span data-ttu-id="ed6da-113">GetReminders</span><span class="sxs-lookup"><span data-stu-id="ed6da-113">GetReminders</span></span>](getreminders.md)
  
## <a name="text-value"></a><span data-ttu-id="ed6da-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="ed6da-114">Text value</span></span>

<span data-ttu-id="ed6da-115">El valor de texto del elemento **ReminderType** es el tipo de avisos para devolver **todos los**, **actual**o **anterior**.</span><span class="sxs-lookup"><span data-stu-id="ed6da-115">The text value of the **ReminderType** element is the type of reminders to return, either **All**, **Current**, or **Old**.</span></span> <span data-ttu-id="ed6da-116">**Todos los** es el valor recomendado para este elemento.</span><span class="sxs-lookup"><span data-stu-id="ed6da-116">**All** is the recommended value for this element.</span></span> <span data-ttu-id="ed6da-117">Para obtener más información acerca de la relación entre el elemento de **ReminderType** y los elementos [BeginTime](begintime.md) y [EndTime](endtime-remindermessagedatatype.md) , vea [GetReminders operación](getreminders-operation.md).</span><span class="sxs-lookup"><span data-stu-id="ed6da-117">For more information about the relationship between the **ReminderType** element and the [BeginTime](begintime.md) and [EndTime](endtime-remindermessagedatatype.md) elements, see [GetReminders operation](getreminders-operation.md).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ed6da-118">Notas</span><span class="sxs-lookup"><span data-stu-id="ed6da-118">Remarks</span></span>

<span data-ttu-id="ed6da-119">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ed6da-119">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="ed6da-120">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="ed6da-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ed6da-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ed6da-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ed6da-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ed6da-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ed6da-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ed6da-123">Schema Name</span></span>  <br/> |<span data-ttu-id="ed6da-124">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="ed6da-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ed6da-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ed6da-125">Validation File</span></span>  <br/> |<span data-ttu-id="ed6da-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ed6da-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ed6da-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ed6da-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="ed6da-128">False</span><span class="sxs-lookup"><span data-stu-id="ed6da-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ed6da-129">Ver también</span><span class="sxs-lookup"><span data-stu-id="ed6da-129">See also</span></span>



[<span data-ttu-id="ed6da-130">GetReminders</span><span class="sxs-lookup"><span data-stu-id="ed6da-130">GetReminders</span></span>](getreminders.md)


- [<span data-ttu-id="ed6da-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="ed6da-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

