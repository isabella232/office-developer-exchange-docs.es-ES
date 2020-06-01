---
title: Avisos
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 19294300-ab84-4784-8aa7-3395a08de640
description: El elemento Reminders especifica los avisos devueltos en la respuesta a una solicitud GetReminders.
ms.openlocfilehash: 1ddf1c10872dcce103919dbed3d1c5e04cdfca74
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458498"
---
# <a name="reminders"></a><span data-ttu-id="b1c8e-103">Avisos</span><span class="sxs-lookup"><span data-stu-id="b1c8e-103">Reminders</span></span>

<span data-ttu-id="b1c8e-104">El elemento **Reminders** especifica los avisos devueltos en la respuesta a una solicitud **GetReminders** .</span><span class="sxs-lookup"><span data-stu-id="b1c8e-104">The **Reminders** element specifies the reminders returned in the response to a **GetReminders** request.</span></span> 
  
```XML
<Reminders>
   <Reminder></Reminder>
</Reminders>
```

 <span data-ttu-id="b1c8e-105">**ArrayOfRemindersType**</span><span class="sxs-lookup"><span data-stu-id="b1c8e-105">**ArrayOfRemindersType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b1c8e-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b1c8e-106">Attributes and elements</span></span>

<span data-ttu-id="b1c8e-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b1c8e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b1c8e-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="b1c8e-108">Attributes</span></span>

<span data-ttu-id="b1c8e-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="b1c8e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b1c8e-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b1c8e-110">Child elements</span></span>

[<span data-ttu-id="b1c8e-111">Aviso</span><span class="sxs-lookup"><span data-stu-id="b1c8e-111">Reminder</span></span>](reminder.md)
  
### <a name="parent-elements"></a><span data-ttu-id="b1c8e-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b1c8e-112">Parent elements</span></span>

[<span data-ttu-id="b1c8e-113">GetRemindersResponse</span><span class="sxs-lookup"><span data-stu-id="b1c8e-113">GetRemindersResponse</span></span>](getremindersresponse.md)
  
## <a name="remarks"></a><span data-ttu-id="b1c8e-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b1c8e-114">Remarks</span></span>

<span data-ttu-id="b1c8e-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b1c8e-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="b1c8e-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="b1c8e-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b1c8e-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b1c8e-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b1c8e-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="b1c8e-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b1c8e-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b1c8e-119">Schema Name</span></span>  <br/> |<span data-ttu-id="b1c8e-120">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="b1c8e-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b1c8e-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b1c8e-121">Validation File</span></span>  <br/> |<span data-ttu-id="b1c8e-122">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="b1c8e-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b1c8e-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b1c8e-123">Can be Empty</span></span>  <br/> |<span data-ttu-id="b1c8e-124">Falso</span><span class="sxs-lookup"><span data-stu-id="b1c8e-124">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b1c8e-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="b1c8e-125">See also</span></span>



[<span data-ttu-id="b1c8e-126">GetRemindersResponse</span><span class="sxs-lookup"><span data-stu-id="b1c8e-126">GetRemindersResponse</span></span>](getremindersresponse.md)


- [<span data-ttu-id="b1c8e-127">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="b1c8e-127">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

