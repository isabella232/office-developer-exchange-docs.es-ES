---
title: AssociatedCalendarItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AssociatedCalendarItemId
api_type:
- schema
ms.assetid: 5b29898c-ea59-4e6a-914c-c011ec754032
description: El elemento AssociatedCalendarItemId representa el elemento de calendario que está asociado con un MeetingMessage, MeetingRequest, MeetingResponse, MeetingCancellation o ReminderMessageData.
ms.openlocfilehash: 816372c38243ba0fe5a7606c264dd1c5107350f2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460886"
---
# <a name="associatedcalendaritemid"></a><span data-ttu-id="16838-103">AssociatedCalendarItemId</span><span class="sxs-lookup"><span data-stu-id="16838-103">AssociatedCalendarItemId</span></span>

<span data-ttu-id="16838-104">El **elemento AssociatedCalendarItemId** representa el elemento de calendario que está asociado con un [MeetingMessage](meetingmessage.md), [MeetingRequest](meetingrequest.md), [MeetingResponse](meetingresponse.md), [MeetingCancellation](meetingcancellation.md)o [ReminderMessageData](remindermessagedata.md).</span><span class="sxs-lookup"><span data-stu-id="16838-104">The **AssociatedCalendarItemId** element represents the calendar item that is associated with a [MeetingMessage](meetingmessage.md), [MeetingRequest](meetingrequest.md), [MeetingResponse](meetingresponse.md), [MeetingCancellation](meetingcancellation.md), or [ReminderMessageData](remindermessagedata.md).</span></span>
  
```XML
<AssociatedCalendarItemId Id="" ChangeKey=""/>
```

 <span data-ttu-id="16838-105">**ItemIdType**</span><span class="sxs-lookup"><span data-stu-id="16838-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="16838-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="16838-106">Attributes and elements</span></span>

<span data-ttu-id="16838-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="16838-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="16838-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="16838-108">Attributes</span></span>

|<span data-ttu-id="16838-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="16838-109">**Attribute**</span></span>|<span data-ttu-id="16838-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="16838-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="16838-111">**Id**</span><span class="sxs-lookup"><span data-stu-id="16838-111">**Id**</span></span> <br/> |<span data-ttu-id="16838-112">Identifica el elemento de calendario que está asociado con la reunión.</span><span class="sxs-lookup"><span data-stu-id="16838-112">Identifies the calendar item that is associated with meeting.</span></span>  <br/> |
|<span data-ttu-id="16838-113">**ChangeKey**</span><span class="sxs-lookup"><span data-stu-id="16838-113">**ChangeKey**</span></span> <br/> |<span data-ttu-id="16838-114">Identifica una versión específica del elemento de calendario que está asociada a una reunión.</span><span class="sxs-lookup"><span data-stu-id="16838-114">Identifies a specific version of the calendar item that is associated with a meeting.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="16838-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="16838-115">Child elements</span></span>

<span data-ttu-id="16838-116">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="16838-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="16838-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="16838-117">Parent elements</span></span>

<span data-ttu-id="16838-118">[MeetingMessage](meetingmessage.md)  |  Propiedad [MeetingRequest](meetingrequest.md)  |  [MeetingResponse](meetingresponse.md)  |  [MeetingCancellation](meetingcancellation.md)  |  [ReminderMessageData](remindermessagedata.md)</span><span class="sxs-lookup"><span data-stu-id="16838-118">[MeetingMessage](meetingmessage.md) | [MeetingRequest](meetingrequest.md) | [MeetingResponse](meetingresponse.md) | [MeetingCancellation](meetingcancellation.md) | [ReminderMessageData](remindermessagedata.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="16838-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="16838-119">Remarks</span></span>

<span data-ttu-id="16838-120">Las versiones de Exchange que comienzan con el número de compilación 15.00.0913.09 pueden incluir el elemento **AssociatedCalendarItemId** como elemento secundario del elemento **ReminderMessageData** .</span><span class="sxs-lookup"><span data-stu-id="16838-120">Versions of Exchange starting with build number 15.00.0913.09 can include the **AssociatedCalendarItemId** element as a child element of the **ReminderMessageData** element.</span></span> 
  
<span data-ttu-id="16838-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="16838-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="16838-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="16838-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="16838-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="16838-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="16838-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="16838-124">Schema Name</span></span>  <br/> |<span data-ttu-id="16838-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="16838-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="16838-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="16838-126">Validation File</span></span>  <br/> |<span data-ttu-id="16838-127">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="16838-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="16838-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="16838-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="16838-129">Falso</span><span class="sxs-lookup"><span data-stu-id="16838-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="16838-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="16838-130">See also</span></span>

- [<span data-ttu-id="16838-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="16838-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

