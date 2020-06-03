---
title: Notificaciones
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Notifications
api_type:
- schema
ms.assetid: 153cc420-d2fe-42f1-afb2-9a31ee09a750
description: El elemento Notifications contiene una matriz de información sobre la suscripción y los eventos que se han producido desde la última notificación.
ms.openlocfilehash: 88fc56ba6e672e3dea7a1d31f7cc1fda018b9a15
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462622"
---
# <a name="notifications"></a><span data-ttu-id="627b2-103">Notificaciones</span><span class="sxs-lookup"><span data-stu-id="627b2-103">Notifications</span></span>

<span data-ttu-id="627b2-104">El elemento **Notifications** contiene una matriz de información sobre la suscripción y los eventos que se han producido desde la última notificación.</span><span class="sxs-lookup"><span data-stu-id="627b2-104">The **Notifications** element contains an array of information about the subscription and the events that have occurred since the last notification.</span></span> 
  
```xml
<Notifications>
   <Notification/>
</Notifications>
```

 <span data-ttu-id="627b2-105">**NonEmptyArrayOfNotificationsType**</span><span class="sxs-lookup"><span data-stu-id="627b2-105">**NonEmptyArrayOfNotificationsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="627b2-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="627b2-106">Attributes and elements</span></span>

<span data-ttu-id="627b2-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="627b2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="627b2-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="627b2-108">Attributes</span></span>

<span data-ttu-id="627b2-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="627b2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="627b2-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="627b2-110">Child elements</span></span>

|<span data-ttu-id="627b2-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="627b2-111">**Element**</span></span>|<span data-ttu-id="627b2-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="627b2-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="627b2-113">Notificación</span><span class="sxs-lookup"><span data-stu-id="627b2-113">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="627b2-114">Contiene información sobre la suscripción y los eventos que se han producido desde la última notificación.</span><span class="sxs-lookup"><span data-stu-id="627b2-114">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="627b2-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="627b2-115">Parent elements</span></span>

|<span data-ttu-id="627b2-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="627b2-116">**Element**</span></span>|<span data-ttu-id="627b2-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="627b2-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="627b2-118">GetStreamingEventsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="627b2-118">GetStreamingEventsResponseMessage</span></span>](getstreamingeventsresponsemessage.md) <br/> |<span data-ttu-id="627b2-119">Contiene el estado y el resultado de una sola solicitud de [operación GetStreamingEvents](getstreamingevents-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="627b2-119">Contains the status and result of a single [GetStreamingEvents operation](getstreamingevents-operation.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="627b2-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="627b2-120">Text value</span></span>

<span data-ttu-id="627b2-121">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="627b2-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="627b2-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="627b2-122">Remarks</span></span>

<span data-ttu-id="627b2-123">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange. este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="627b2-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="627b2-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="627b2-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="627b2-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="627b2-125">Namespace</span></span>  <br/> |<span data-ttu-id="627b2-126">https://schemas.microsoft.com/exchange/services/2006/messages y https://schemas.microsoft.com/exchange/services/2006/types</span><span class="sxs-lookup"><span data-stu-id="627b2-126">https://schemas.microsoft.com/exchange/services/2006/messages and https://schemas.microsoft.com/exchange/services/2006/types</span></span>  <br/> |
|<span data-ttu-id="627b2-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="627b2-127">Schema Name</span></span>  <br/> |<span data-ttu-id="627b2-128">Esquema de mensajes; Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="627b2-128">Messages schema; Types schema</span></span>  <br/> |
|<span data-ttu-id="627b2-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="627b2-129">Validation File</span></span>  <br/> |<span data-ttu-id="627b2-130">Messages. xsd; Types. xsd</span><span class="sxs-lookup"><span data-stu-id="627b2-130">Messages.xsd; Types.xsd</span></span>  <br/> |
|<span data-ttu-id="627b2-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="627b2-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="627b2-132">Falso</span><span class="sxs-lookup"><span data-stu-id="627b2-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="627b2-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="627b2-133">See also</span></span>



[<span data-ttu-id="627b2-134">Operación GetFolder</span><span class="sxs-lookup"><span data-stu-id="627b2-134">GetFolder operation</span></span>](getfolder-operation.md)
  
[<span data-ttu-id="627b2-135">Operación DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="627b2-135">DeleteFolder operation</span></span>](deletefolder-operation.md)
  
[<span data-ttu-id="627b2-136">Operación MoveFolder</span><span class="sxs-lookup"><span data-stu-id="627b2-136">MoveFolder operation</span></span>](movefolder-operation.md)
  
[<span data-ttu-id="627b2-137">Operación CopyFolder</span><span class="sxs-lookup"><span data-stu-id="627b2-137">CopyFolder operation</span></span>](copyfolder-operation.md)
  
[<span data-ttu-id="627b2-138">Operación subscribe</span><span class="sxs-lookup"><span data-stu-id="627b2-138">Subscribe operation</span></span>](subscribe-operation.md)

