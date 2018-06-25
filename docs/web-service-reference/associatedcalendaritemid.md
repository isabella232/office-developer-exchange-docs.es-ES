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
ms.openlocfilehash: 4445da88d6fec42c1e02cd8de4d2e423485a4472
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763564"
---
# <a name="associatedcalendaritemid"></a><span data-ttu-id="511aa-103">AssociatedCalendarItemId</span><span class="sxs-lookup"><span data-stu-id="511aa-103">AssociatedCalendarItemId</span></span>

<span data-ttu-id="511aa-104">El elemento **AssociatedCalendarItemId** representa el elemento de calendario que está asociado con un [MeetingMessage](meetingmessage.md), [MeetingRequest](meetingrequest.md), [MeetingResponse](meetingresponse.md), [MeetingCancellation](meetingcancellation.md)o [ReminderMessageData](remindermessagedata.md).</span><span class="sxs-lookup"><span data-stu-id="511aa-104">The **AssociatedCalendarItemId** element represents the calendar item that is associated with a [MeetingMessage](meetingmessage.md), [MeetingRequest](meetingrequest.md), [MeetingResponse](meetingresponse.md), [MeetingCancellation](meetingcancellation.md), or [ReminderMessageData](remindermessagedata.md).</span></span>
  
```XML
<AssociatedCalendarItemId Id="" ChangeKey=""/>
```

 <span data-ttu-id="511aa-105">**ItemIdType**</span><span class="sxs-lookup"><span data-stu-id="511aa-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="511aa-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="511aa-106">Attributes and elements</span></span>

<span data-ttu-id="511aa-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="511aa-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="511aa-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="511aa-108">Attributes</span></span>

|<span data-ttu-id="511aa-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="511aa-109">**Attribute**</span></span>|<span data-ttu-id="511aa-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="511aa-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="511aa-111">**Id**</span><span class="sxs-lookup"><span data-stu-id="511aa-111">**Id**</span></span> <br/> |<span data-ttu-id="511aa-112">Identifica el elemento de calendario que está asociado a la reunión.</span><span class="sxs-lookup"><span data-stu-id="511aa-112">Identifies the calendar item that is associated with meeting.</span></span>  <br/> |
|<span data-ttu-id="511aa-113">**ChangeKey**</span><span class="sxs-lookup"><span data-stu-id="511aa-113">**ChangeKey**</span></span> <br/> |<span data-ttu-id="511aa-114">Identifica una versión específica del elemento de calendario que está asociado a una reunión.</span><span class="sxs-lookup"><span data-stu-id="511aa-114">Identifies a specific version of the calendar item that is associated with a meeting.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="511aa-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="511aa-115">Child elements</span></span>

<span data-ttu-id="511aa-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="511aa-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="511aa-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="511aa-117">Parent elements</span></span>

<span data-ttu-id="511aa-118">[MeetingMessage](meetingmessage.md) | [MeetingRequest](meetingrequest.md) | [MeetingResponse](meetingresponse.md) | [MeetingCancellation](meetingcancellation.md) | [ReminderMessageData](remindermessagedata.md)</span><span class="sxs-lookup"><span data-stu-id="511aa-118">[MeetingMessage](meetingmessage.md) | [MeetingRequest](meetingrequest.md) | [MeetingResponse](meetingresponse.md) | [MeetingCancellation](meetingcancellation.md) | [ReminderMessageData](remindermessagedata.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="511aa-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="511aa-119">Remarks</span></span>

<span data-ttu-id="511aa-120">Las versiones de Exchange, comenzando por el número de compilación 15.00.0913.09 pueden incluir el elemento **AssociatedCalendarItemId** como un elemento secundario del elemento **ReminderMessageData** .</span><span class="sxs-lookup"><span data-stu-id="511aa-120">Versions of Exchange starting with build number 15.00.0913.09 can include the **AssociatedCalendarItemId** element as a child element of the **ReminderMessageData** element.</span></span> 
  
<span data-ttu-id="511aa-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="511aa-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="511aa-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="511aa-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="511aa-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="511aa-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="511aa-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="511aa-124">Schema Name</span></span>  <br/> |<span data-ttu-id="511aa-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="511aa-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="511aa-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="511aa-126">Validation File</span></span>  <br/> |<span data-ttu-id="511aa-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="511aa-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="511aa-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="511aa-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="511aa-129">False</span><span class="sxs-lookup"><span data-stu-id="511aa-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="511aa-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="511aa-130">See also</span></span>

- [<span data-ttu-id="511aa-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="511aa-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

