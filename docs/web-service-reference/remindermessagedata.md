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
ms.openlocfilehash: f2632062cd02581c426f7dbfa2a33d53e5594d72
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458554"
---
# <a name="remindermessagedata"></a><span data-ttu-id="5eb19-103">ReminderMessageData</span><span class="sxs-lookup"><span data-stu-id="5eb19-103">ReminderMessageData</span></span>

<span data-ttu-id="5eb19-104">El elemento **ReminderMessageData** especifica los datos en un mensaje de aviso.</span><span class="sxs-lookup"><span data-stu-id="5eb19-104">The **ReminderMessageData** element specifies the data in a reminder message.</span></span> 
  
```XML
<ReminderMessageData>
   <ReminderText></ReminderText>
   <Location></Location>
   <StartTime></StartTime>
   <EndTime></EndTime>
   <AssociatedCalendarItemId></AssociatedCalendarItemId>
</ReminderMessageData>

```

 <span data-ttu-id="5eb19-105">**ReminderMessageDataType**</span><span class="sxs-lookup"><span data-stu-id="5eb19-105">**ReminderMessageDataType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5eb19-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="5eb19-106">Attributes and elements</span></span>

<span data-ttu-id="5eb19-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="5eb19-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5eb19-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="5eb19-108">Attributes</span></span>

<span data-ttu-id="5eb19-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="5eb19-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5eb19-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5eb19-110">Child elements</span></span>

<span data-ttu-id="5eb19-111">[ReminderText](remindertext.md)  |  [Ubicación](location.md)  |  [StartTime (ReminderMessageDataType)](starttime-remindermessagedatatype.md)  |  [EndTime (ReminderMessageDataType)](endtime-remindermessagedatatype.md)  |  [AssociatedCalendarItemId](associatedcalendaritemid.md)</span><span class="sxs-lookup"><span data-stu-id="5eb19-111">[ReminderText](remindertext.md) | [Location](location.md) | [StartTime (ReminderMessageDataType)](starttime-remindermessagedatatype.md) | [EndTime (ReminderMessageDataType)](endtime-remindermessagedatatype.md) | [AssociatedCalendarItemId](associatedcalendaritemid.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5eb19-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5eb19-112">Parent elements</span></span>

[<span data-ttu-id="5eb19-113">Mensaje</span><span class="sxs-lookup"><span data-stu-id="5eb19-113">Message</span></span>](message-ex15websvcsotherref.md)
  
## <a name="remarks"></a><span data-ttu-id="5eb19-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5eb19-114">Remarks</span></span>

<span data-ttu-id="5eb19-115">Este elemento se incorporó en Exchange Server 2013 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="5eb19-115">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="5eb19-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="5eb19-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
<span data-ttu-id="5eb19-117">Las versiones de Exchange que comienzan con el número de compilación 15.00.0913.09 pueden incluir el elemento **AssociatedCalendarItemId** como elemento secundario del elemento **ReminderMessageData** .</span><span class="sxs-lookup"><span data-stu-id="5eb19-117">Versions of Exchange starting with build number 15.00.0913.09 can include the **AssociatedCalendarItemId** element as a child element of the **ReminderMessageData** element.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="5eb19-118">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="5eb19-118">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5eb19-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="5eb19-119">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5eb19-120">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="5eb19-120">Schema Name</span></span>  <br/> |<span data-ttu-id="5eb19-121">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="5eb19-121">Types schema</span></span>  <br/> |
|<span data-ttu-id="5eb19-122">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="5eb19-122">Validation File</span></span>  <br/> |<span data-ttu-id="5eb19-123">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="5eb19-123">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5eb19-124">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="5eb19-124">Can be Empty</span></span>  <br/> |<span data-ttu-id="5eb19-125">Verdadero</span><span class="sxs-lookup"><span data-stu-id="5eb19-125">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5eb19-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="5eb19-126">See also</span></span>



[<span data-ttu-id="5eb19-127">Mensaje</span><span class="sxs-lookup"><span data-stu-id="5eb19-127">Message</span></span>](message-ex15websvcsotherref.md)


- [<span data-ttu-id="5eb19-128">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="5eb19-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

