---
title: ProposedStart (MeetingRegistrationResponseObjectType)
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8c58cef7-bc43-493a-a323-ba4dc6a33704
description: El elemento ProposedStart (MeetingRegistrationResponseObjectType) especifica propuesto hora de inicio de un asistente nuevo para una reunión.
ms.openlocfilehash: db03d1b5e79ed53313cff9677687647f24e90756
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836905"
---
# <a name="proposedstart-meetingregistrationresponseobjecttype"></a><span data-ttu-id="f0bfa-103">ProposedStart (MeetingRegistrationResponseObjectType)</span><span class="sxs-lookup"><span data-stu-id="f0bfa-103">ProposedStart (MeetingRegistrationResponseObjectType)</span></span>

<span data-ttu-id="f0bfa-104">El elemento **ProposedStart (MeetingRegistrationResponseObjectType)** especifica propuesto hora de inicio de un asistente nuevo para una reunión.</span><span class="sxs-lookup"><span data-stu-id="f0bfa-104">The **ProposedStart (MeetingRegistrationResponseObjectType)** element specifies an attendee's proposed new start time for a meeting.</span></span> 
  
```XML
<ProposedStart />
```

 <span data-ttu-id="f0bfa-105">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="f0bfa-105">**dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f0bfa-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f0bfa-106">Attributes and elements</span></span>

<span data-ttu-id="f0bfa-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f0bfa-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f0bfa-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="f0bfa-108">Attributes</span></span>

<span data-ttu-id="f0bfa-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f0bfa-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f0bfa-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f0bfa-110">Child elements</span></span>

<span data-ttu-id="f0bfa-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f0bfa-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f0bfa-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f0bfa-112">Parent elements</span></span>

<span data-ttu-id="f0bfa-113">[AcceptItem](acceptitem.md) | [TentativelyAcceptItem](tentativelyacceptitem.md) | [DeclineItem](declineitem.md)</span><span class="sxs-lookup"><span data-stu-id="f0bfa-113">[AcceptItem](acceptitem.md) | [TentativelyAcceptItem](tentativelyacceptitem.md) | [DeclineItem](declineitem.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="f0bfa-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="f0bfa-114">Text value</span></span>

<span data-ttu-id="f0bfa-115">El valor de texto del elemento **ProposedStart (MeetingRegistrationResponseObjectType)** es la fecha de inicio propuesta y la hora de la reunión.</span><span class="sxs-lookup"><span data-stu-id="f0bfa-115">The text value of the **ProposedStart (MeetingRegistrationResponseObjectType)** element is the proposed start date and time of the meeting.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f0bfa-116">Notas</span><span class="sxs-lookup"><span data-stu-id="f0bfa-116">Remarks</span></span>

<span data-ttu-id="f0bfa-117">Este elemento se incorporó en Exchange Server 2013 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="f0bfa-117">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="f0bfa-118">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="f0bfa-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f0bfa-119">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f0bfa-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f0bfa-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f0bfa-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f0bfa-121">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f0bfa-121">Schema Name</span></span>  <br/> |<span data-ttu-id="f0bfa-122">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="f0bfa-122">Types schema</span></span>  <br/> |
|<span data-ttu-id="f0bfa-123">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f0bfa-123">Validation File</span></span>  <br/> |<span data-ttu-id="f0bfa-124">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f0bfa-124">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f0bfa-125">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f0bfa-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="f0bfa-126">Verdadero</span><span class="sxs-lookup"><span data-stu-id="f0bfa-126">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f0bfa-127">Ver también</span><span class="sxs-lookup"><span data-stu-id="f0bfa-127">See also</span></span>



[<span data-ttu-id="f0bfa-128">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="f0bfa-128">AcceptItem</span></span>](acceptitem.md)
  
[<span data-ttu-id="f0bfa-129">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="f0bfa-129">DeclineItem</span></span>](declineitem.md)
  
[<span data-ttu-id="f0bfa-130">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="f0bfa-130">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md)


- [<span data-ttu-id="f0bfa-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="f0bfa-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

