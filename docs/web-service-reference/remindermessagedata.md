---
title: ReminderMessageData
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 04dd4987-baaf-4ebe-ae58-ad962c2f8fa1
description: El elemento ReminderMessageData especifica los datos en un mensaje de aviso.
ms.openlocfilehash: a1d01dd24030b047bd8ad025f3e1cebed0da8e29
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837067"
---
# <a name="remindermessagedata"></a><span data-ttu-id="c4a53-103">ReminderMessageData</span><span class="sxs-lookup"><span data-stu-id="c4a53-103">ReminderMessageData</span></span>

<span data-ttu-id="c4a53-104">El elemento **ReminderMessageData** especifica los datos en un mensaje de aviso.</span><span class="sxs-lookup"><span data-stu-id="c4a53-104">The **ReminderMessageData** element specifies the data in a reminder message.</span></span> 
  
```XML
<ReminderMessageData>
   <ReminderText></ReminderText>
   <Location></Location>
   <StartTime></StartTime>
   <EndTime></EndTime>
   <AssociatedCalendarItemId></AssociatedCalendarItemId>
</ReminderMessageData>

```

 <span data-ttu-id="c4a53-105">**ReminderMessageDataType**</span><span class="sxs-lookup"><span data-stu-id="c4a53-105">**ReminderMessageDataType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c4a53-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c4a53-106">Attributes and elements</span></span>

<span data-ttu-id="c4a53-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c4a53-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c4a53-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c4a53-108">Attributes</span></span>

<span data-ttu-id="c4a53-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c4a53-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c4a53-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c4a53-110">Child elements</span></span>

<span data-ttu-id="c4a53-111">[ReminderText](remindertext.md) | [ubicación](location.md) | [StartTime (ReminderMessageDataType)](starttime-remindermessagedatatype.md) | [EndTime (ReminderMessageDataType)](endtime-remindermessagedatatype.md) | [AssociatedCalendarItemId](associatedcalendaritemid.md)</span><span class="sxs-lookup"><span data-stu-id="c4a53-111">[ReminderText](remindertext.md) | [Location](location.md) | [StartTime (ReminderMessageDataType)](starttime-remindermessagedatatype.md) | [EndTime (ReminderMessageDataType)](endtime-remindermessagedatatype.md) | [AssociatedCalendarItemId](associatedcalendaritemid.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c4a53-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c4a53-112">Parent elements</span></span>

[<span data-ttu-id="c4a53-113">Message</span><span class="sxs-lookup"><span data-stu-id="c4a53-113">Message</span></span>](message-ex15websvcsotherref.md)
  
## <a name="remarks"></a><span data-ttu-id="c4a53-114">Notas</span><span class="sxs-lookup"><span data-stu-id="c4a53-114">Remarks</span></span>

<span data-ttu-id="c4a53-115">Este elemento se incorporó en Exchange Server 2013 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="c4a53-115">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="c4a53-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="c4a53-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
<span data-ttu-id="c4a53-117">Las versiones de Exchange, comenzando por el número de compilación 15.00.0913.09 pueden incluir el elemento **AssociatedCalendarItemId** como un elemento secundario del elemento **ReminderMessageData** .</span><span class="sxs-lookup"><span data-stu-id="c4a53-117">Versions of Exchange starting with build number 15.00.0913.09 can include the **AssociatedCalendarItemId** element as a child element of the **ReminderMessageData** element.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="c4a53-118">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c4a53-118">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c4a53-119">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c4a53-119">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c4a53-120">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c4a53-120">Schema Name</span></span>  <br/> |<span data-ttu-id="c4a53-121">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="c4a53-121">Types schema</span></span>  <br/> |
|<span data-ttu-id="c4a53-122">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c4a53-122">Validation File</span></span>  <br/> |<span data-ttu-id="c4a53-123">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c4a53-123">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c4a53-124">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c4a53-124">Can be Empty</span></span>  <br/> |<span data-ttu-id="c4a53-125">Verdadero</span><span class="sxs-lookup"><span data-stu-id="c4a53-125">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c4a53-126">Ver también</span><span class="sxs-lookup"><span data-stu-id="c4a53-126">See also</span></span>



[<span data-ttu-id="c4a53-127">Message</span><span class="sxs-lookup"><span data-stu-id="c4a53-127">Message</span></span>](message-ex15websvcsotherref.md)


- [<span data-ttu-id="c4a53-128">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="c4a53-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

